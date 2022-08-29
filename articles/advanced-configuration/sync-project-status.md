---
title: Menyegerakkan Status Projek untuk mengelakkan kemasukan terhadap projek yang ditutup
description: Artikel ini menerangkan cara menyegerakkan Status Projek untuk mengelakkan entri terhadap projek yang tidak aktif atau tertutup.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Menyegerakkan Status Projek untuk mengelakkan kemasukan terhadap projek yang ditutup

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="scenario"></a>Senario

Contoso disiarkan secara langsung dengan Microsoft Dynamics 365 Project Operations untuk senario sumber/bukan stok. Sebagai sebahagian daripada aktiviti perniagaan biasa, projek boleh disiapkan atau ditangguhkan. Anda boleh menyahaktifkan projek untuk memastikan tiada perbelanjaan atau invois dijana.

## <a name="solution"></a>Penyelesaian

### <a name="prerequisites"></a>Prasyarat

-   Microsoft Dynamics 365 Kewangan 10.0.29 atau lebih baru mesti dipasang.
-   Peta Dwi Tulis 1.0.0.3 untuk Projek V2 (projek msdyn\_) mesti dipasang atau dikonfigurasikan secara manual seperti yang diterangkan di bawah.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Mencipta versi terkini peta dwi-tulis Project Operations V2

Untuk mengemas kini peta dwi-tulis Projek Operasi Projek V2:

1. Pergi ke **Ruang Kerja pengurusan** data dan pilih **Dwi tulis**.
2. **Pilih jubin Dwi tulis**.
3. Daripada lajur Peta Jadual T **, cari dan pilih** Projek V2 (projek msdyn **)\_, kemudian pilih** Berhenti.
4. Pilih nama peta untuk membuka peta dan kemudian pilih **[Tiada]**.
5. Daripada kotak dialog Pilih lajur, pilih **Statecode \[Status\]** Projek kemudian pilih OK. Anda boleh menaip **keadaan** dalam nilai penapis untuk menyempitkan senarai.
6.  Pilih **Tambah atau edit transformasi** dalam **lajur jenis** peta untuk mengedit transformasi.
7.  Daripada **Ubah jenis** pilih **ValueMap**.
8.  Pilih **Tambah pemetaan** nilai kemudian tambah Kekunci **dan** Nilai **berikut**:

   Kekunci       | Nilai 
   ----------|-------
   InProcess | 0     
   selesai | 1     

![Petikan skrin menunjukkan Pemetaan Dwi-tulis](media/projectstage-dw-mapping.png)

9. Pilih **Simpan**.
10. Dari bahagian atas **halaman Dwi-tulis > Projek V2 (msdyn_projects**), pilih **Simpan Sebagai**.
11. Daripada **Tambah jadual** dalam **medan Publisher**, pilih **CDS Default Publisher**.
12. Setkan medan **Versi** kepada 1.0.0.3.
13. **Taipkan Perihalan** kemudian pilih **Simpan**.
14. Dari bahagian atas **halaman Dwi-tulis > Projects V2 (msdyn_projects**), pilih **Jalankan** untuk memulakan peta, dan kemudian mazhab **Ya** jika diminta mengesahkan sebelum dijalankan. 

### <a name="close-a-newly-completed-project"></a>Tutup projek yang baru siap

Dynamics 365 Finance menggunakan **medan peringkat** projek untuk membezakan antara projek **dalam proses** atau **selesai**. **Projek siap** tidak boleh menanggung perbelanjaan atau diinvois kepada pelanggan.

1. Buka projek untuk menyahaktifkan.
2. Daripada reben, pilih **Nyahaktifkan**.

> [!NOTE]
> Anda boleh sama ada menyahaktifkan atau menutup projek kerana kedua-duanya akan berkelakuan sama dalam konteks Kewangan.

3. Dalam Kewangan, buka **halaman senarai** Semua projek.
4. Sahkan projek yang dinyahaktifkan tidak muncul dalam senarai.
5. **Dalam penapis tunjukkan projek** di atas senarai, ubah nilai daripada **Aktif** kepada **Semua**.
6. Anda kini akan melihat projek yang dinyahaktifkan.

Jika anda cuba log masa atau perbelanjaan terhadap projek ini dalam Kewangan, anda tidak sepatutnya melihat projek untuk pemilihan. Jika anda memasukkan nombor projek secara manual dengan perbelanjaan, anda akan melihat mesej seperti "Peringkat projek selesai tidak membenarkan rakaman dalam projek". Invois dan fungsi pengebilan lain harus dilumpuhkan kerana ia akan berada dalam konteks projek tertutup.

