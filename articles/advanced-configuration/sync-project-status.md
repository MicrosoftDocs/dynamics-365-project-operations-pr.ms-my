---
title: Segerakkan Status Projek untuk mengelakkan entri ke projek ditutup
description: Artikel ini menerangkan cara untuk menyegerakkan Status Projek untuk mengelakkan entri terhadap projek tidak aktif atau tertutup.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348110"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Segerakkan Status Projek untuk mengelakkan entri ke projek ditutup

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="scenario"></a>Senario

Contoso bersiaran langsung dengan Microsoft Dynamics 365 Project Operations untuk senario sumber/bukan stok. Sebagai sebahagian daripada aktiviti perniagaan biasa, projek boleh dilengkapkan atau ditahan. Anda boleh menyahaktifkan projek untuk memastikan tiada perbelanjaan atau invois dijana.

## <a name="solution"></a>Penyelesaian

### <a name="prerequisites"></a>Prasyarat

-   Microsoft Dynamics 365 Finance 10.0.29 atau lebih baharu mesti dipasang.
-   Peta Dwi Tulis 1.0.0.3 untuk Projek V2 (msdyn\_projects) mesti dipasang atau dikonfigurasikan secara manual seperti yang diterangkan di bawah.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Cipta versi kemas kini peta dwi tulis Projects V2 penyepaduan Project Operations

Untuk mengemas kini peta dwi tulis Projects V2 Project Operations:

1. Pergi ke ruang kerja **Pengurusan data** dan pilih **Dwi tulis**.
2. Pilih jubin **Dwi tulis**.
3. daripada lajur T **Peta jadual**, cari dan pilih **Project V2 (msdyn\_projects)**, kemudian pilih Berhenti.
4. Pilih nama Peta untuk membuka peta, kemudian pilih **[Tiada]**.
5. Daripada Pilih kotak dialog lajur, pilih **statecode \[Status Projek\]**, kemudian pilih OK. Anda boleh menaip jenis **keadaan** dalam nilai penapis untuk mengecilkan senarai.
6.  Pilih **Tambah atau edit transformasi** dalam lajur **jenis peta** untuk mengedit transformasi.
7.  Daripada **Jenis transformasi** pilih **ValueMap**.
8.  Pilih **Tambah pemetaan nilai**, kemudian tambah **Kekunci** dan **Nilai** berikut:

   Kekunci       | Nilai 
   ----------|-------
   InProcess | 0     
   selesai | 1     

![Syot layar menunjukkan Pemetaan dwi tulis](media/projectstage-dw-mapping.png)

9. Pilih **Simpan**.
10. Dari bahagian atas halaman **Dwi tulis > Projects V2 (msdyn_projects)**, pilih **Simpan Sebagai**.
11. Daripada **Tambah jadual** dalam medan **Penerbit**, pilih **Penerbit Lalai CDS**.
12. Tetapkan medan **Versi** kepada 1.0.0.3.
13. Taip **Perihalan**, kemudian pilih **Simpan**.
14. Daripada bahagian atas halaman **Dwi tulis > Projects V2 (msdyn_projects)**, pilih **Jalankan** untuk memulakan peta, kemudian pilih **Ya** jika diminta untuk mengesahkan sebelum berjalan. 

### <a name="close-a-newly-completed-project"></a>Tutup projek yang baru siap

Dynamics 365 Finance menggunakan medan **peringkat projek** untuk membezakan antara projek **dalam proses** atau **selesai**. Projek yang **Selesai** tidak boleh menanggung perbelanjaan atau diinvois kepada pelanggan.

1. Buka projek untuk menyahaktifkan.
2. Daripada reben, pilih **Nyahaktifkan**.

> [!NOTE]
> Anda boleh sama ada menyahaktifkan atau menutup projek kerana projek akan berkelakuan sama dalam konteks Kewangan.

3. Dalam Kewangan, buka halaman **Semua senarai projek**.
4. Sahkan projek yang dinyahaktifkan tidak muncul dalam senarai.
5. Dalam penapis **tunjukkan projek** di atas senarai, ubah nilai daripada **Aktif** kepada **Semua**.
6. Anda kini akan melihat projek yang dinyahaktifkan.

Jika anda cuba untuk log masa atau perbelanjaan terhadap projek ini dalam Kewangan, anda tidak boleh melihat projek untuk pemilihan. Jika anda memasukkan nombor projek secara manual pada perbelanjaan, anda akan melihat mesej seperti "Peringkat projek yang selesai tidak membenarkan rakaman dalam projek". Fungsi penginvoisan dan pengebilan lain sepatutnya dinyahdayakan kerana fungsi ini akan berada dalam konteks projek tertutup.

