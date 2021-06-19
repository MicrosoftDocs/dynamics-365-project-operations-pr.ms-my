---
title: Selesaikan masalah kerja dalam grid Tugas
description: Topik ini menyediakan maklumat penyelesaian masalah yang diperlukan apabila menggunakan grid Tugas.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213411"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Selesaikan masalah kerja dalam grid Tugas 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Topik ini menerangkan cara menyelesaikan masalah yang anda mungkin alami ketika menggunakan pengurusan kos.

## <a name="enable-cookies"></a>Dayakan kuki

Project Operations memerlukan kuki pihak ketiga tersebut didayakan bagi memaparkan struktur pecahan kerja. Apabila kuki pihak ketiga tidak didayakan, anda tidak melihat tugas, tetapi anda akan melihat halaman kosong apabila anda memilih tab **Tugas** pada halaman **Projek**.

![Tab kosong apabila kuki pihak ketiga tidak didayakan](media/blankschedule.png)


### <a name="workaround"></a>Penyelesaian sementara
Untuk penyemak imbas Microsoft Edge atau Google Chrome, prosedur berikut menggariskan cara mengemas kini tetapan penyemak imbas anda untuk mendayakan kuki pihak ketiga.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Buka penyemak imbas Microsoft Edge anda.
2. Di penjuru sebelah kanan bahagian atas, pilih **elipsis** (...), dan kemudian pilih **Tetapan**.
3. Di bawah **Keizinan kuki dan tapak**, pilih **Kuki dan data tapak**.
4. Matikan **Sekat kuki pihak ketiga**.

#### <a name="google-chrome"></a>Google Chrome

1. Buka penyemak imbas Chrome anda.
2. Di penjuru sebelah kanan bahagian atas, pilih tiga titik menegak (...), dan kemudian pilih **Tetapan**.
3. Di bawah **Privasi dan keselamatan**, pilih **Kuki dan data tapak lain**.
4. Pilih **Benarkan semua kuki**.

> [!IMPORTANT]
> Jika anda menyekat kuki pihak ketiga, semua kuki dan data tapak daripada tapak lain akan disekat, sekalipun tapak itu dibenarkan pada senarai pengecualian anda.

## <a name="pex-endpoint"></a>Titik Tamat PEX

Project Operations memerlukan parameter projek merujuk Titik Tamat PEX. Titik tamat ini diperlukan untuk berkomunikasi dengan perkhidmatan yang digunakan untuk memaparkan struktur pecahan kerja. Jika parameter tidak didayakan, anda akan menerima ralat, "Parameter projek tidak sah". 

### <a name="workaround"></a>Penyelesaian sementara
 ![Medan Titik Tamat PEX pada parameter projek](media/projectparameter.png)

1. Tambah medan **Titik Tamat PEX** pada halaman **Parameter Projek**.
2. Kemas kini medan dengan nilai berikut: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`
3. Alih keluar medan daripada halaman **Parameter Projek**.

## <a name="privileges-for-project-for-the-web"></a>Kelayakan untuk Projek untuk Web

Project Operations bergantung pada perkhidmatan penjadualan luaran. Perkhidmatan memerlukan pengguna mempunyai beberapa peranan ditugaskan untuk membaca dan menulis entiti berkaitan dengan struktur pecahan kerja. Entiti ini termasuklah tugas projek, tugasan sumber dan kebersandaran tugas. Jika pengguna tidak boleh memaparkan struktur pecahan kerja apabila mereka pergi ke tab **Tugas**, ia mungkin disebabkan Projek untuk Project Operations belum didayakan. Pengguna mungkin menerima sama ada ralat peranan keselamatan atau ralat berkaitan dengan penafian akses.


## <a name="workaround"></a>Penyelesaian sementara

1. Pergi ke **Tetapan > Keselamatan > Pengguna > Pengguna Aplikasi**.  

   ![Pembaca aplikasi](media/applicationuser.jpg)
   
2. Klik dua kali rekod pengguna aplikasi untuk mengesahkan perkara berikut:

 - Pengguna mempunyai capaian kepada projek. Pengesahan ini lazimnya dilakukan bagi memastikan pengguna mempunyai peranan keselamatan **Pengurus Projek**.
 - Pengguna aplikasi Microsoft Project wujud dan dikonfigurasikan dengan betul.
 
3. Jika pengguna ini tidak wujud, anda boleh mencipta rekod pengguna baharu. Pilih **Pengguna Baharu**. Ubah borang entri kepada **Pengguna Aplikasi**, dan kemudian tambah **ID Aplikasi**.

   ![Butiran pengguna aplikasi](media/applicationuserdetails.jpg)

4. Sahkan bahawa pengguna telah ditugaskan lesen yang betul dan perkhidmatan didayakan dalam rancangan perkhidmatan untuk butiran lesen.
5. Sahkan bahawa pengguna boleh membuka project.microsoft.com.
6. Sahkan melalui parameter projek bahawa sistem sedang menghala kepada titik tamat projek yang betul.
7. Sahkan bahawa pengguna aplikasi projek dicipta.
8. Gunakan peranan keselamatan berikut kepada pengguna:

  - Pengguna Dataverse
  - Sistem Project Operations
  - Sistem Projek

## <a name="error-when-updating-the-work-breakdown-structure"></a>Ralat semasa mengemas kini struktur pecahan kerja

Apabila satu atau lebih kemas kini dibuat kepada struktur pecahan kerja, perubahan akhirnya gagal dan tidak disimpan. Ralat berlaku dalam grid jadual dan mencatatkan bahawa "Perubahan terkini yang anda buat tidak dapat disimpan."

### <a name="workaround"></a>Penyelesaian sementara

1. Sahkan bahawa pengguna telah ditugaskan lesen yang betul dan perkhidmatan didayakan dalam rancangan perkhidmatan untuk butiran lesen.
2. Sahkan bahawa pengguna boleh membuka project.microsoft.com.
3. Sahkan bahawa sistem sedang menghala kepada titik tamat projek yang betul.
4. Sahkan bahawa pengguna Aplikasi Projek telah dicipta.
5. Gunakan peranan keselamatan berikut kepada pengguna:
  
  - Pengguna Dataverse atau pengguna Pangkalan
  - Sistem Project Operations
  - Sistem Projek
  - Sistem Dwitulis Project Operations (Peranan ini diperlukan jika anda menggunakan senario berdasarkan sumber/bukan stok bagi Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
