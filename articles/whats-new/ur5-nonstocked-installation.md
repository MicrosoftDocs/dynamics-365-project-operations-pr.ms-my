---
title: Kemas kini Project Operations dalam persekitaran Kewangan anda
description: Topik ini memberikan maklumat tentang cara mengemas kini Operasi Projek dalam persekitaran Dynamics 365 Finance anda.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9cd562ac3360298796fbe34dbe2ac8708b00150f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579945"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Kemas kini Project Operations dalam persekitaran Kewangan anda

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Topik ini memberikan maklumat tentang cara mengemas kini Dynamics 365 Project Operations dalam persekitaran Dynamics 365 Finance anda. Terdapat tiga prosedur yang diperlukan untuk mengemas kini Project Operations kepada Kemas Kini 5 (UR5):

- [Import pakej ke dalam projek pratonton anda](#import)
- [Gunakan kemas kini](#apply)
- [Kemas kini persekitaran Dataverse anda](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Import pakej ke dalam projek LCS anda

1. Daftar masuk ke dalam [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sebagai Pemilik Projek atau pengurus Persekitaran.
2. Daripada senarai projek, pilih projek LCS anda.
3. Pada halaman **Projek**, dalam kumpulan **Persekitaran**, buka persekitaran yang anda mahu kemas kini.
4. Sahkan bahawa persekitaran sedang berjalan. Jika ini tidak bermula, mulakan persekitaran.
5. Dalam bahagian **Keluaran baharu** di bawah **Kemas kini tersedia**, pilih **Lihat kemas kini** untuk 10.0.15.

![Butang Lihat kemas kini.](media/view-update.png)

6. Pada halaman **Kemas kini binari**, pilih **Simpan pakej**.
7. Pada halaman **Semak dan simpan kemas kini**, pilih **Simpan pakej**.
8. Pada anak tetingkap **Simpan pakej pada pustaka eset** yang terbuka, masukkan nama pakej dan kemudian pilih **Simpan pakej**.
9. Apabila LCS selesai menyimpan pakej, butang **Selesai** didayakan. Pilih **Selesai**. LCS akan mengesahkan pakej. Pengesahan mengambil masa beberapa minit atau sehingga satu jam.


## <a name="apply-the-package-update"></a><a name="apply"></a>Gunakan kemas kini pakej

1. Dalam LCS, pada halaman **Butiran persekitaran**, pilih **Selenggara** > **Gunakan Kemas Kini**.
2. Daripada senarai, pilih pakej yang anda simpan lebih awal, kemudian pilih **Gunakan**.
3. Pilih **Ya** untuk mengesahkan yang anda mahu menggunakan pakej.

![Kotak dialog Sahkan pelaksanaan pakej.](media/confirm-package-deployment.png)

4. Pilih **Ya** untuk mengesahkan yang anda mahu mengemas kini aplikasi.

![Kotak dialog Sahkan kemas kini aplikasi.](media/confirm-application-update.png)

Kemas kini pelaksanaan dan aplikasi akan bermula. 

Pada halaman **Butiran persekitaran**, di penjuru kanan sebelah atas, status persekitaran akan mengemas kini kepada **Penservisan**. Dalam kira-kira dua jam, kemas kini akan selesai. Maklumat keluaran aplikasi akan dikemas kini kepada **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** dan status persekitaran akan dikemas kini kepada **Dilaksanakan**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Kemas kini persekitaran Dataverse anda

1. Daftar masuk ke [pusat pentadbiran Power Platform](https://admin.powerplatform.com/).
2. Dalam senarai, cari dan buka persekitaran yang anda gunakan untuk memasang Project Operations.
3. Pada halaman **Persekitaran**, pilih **Sumber** > **aplikasi Dynamics 365**.
4. Dalam senarai, cari **Microsoft Dynamics 365 Project Operations**, dan dalam lajur **Status**, pilih **Kemas Kini Tersedia**.
5. Pilih kotak semak **Saya bersetuju dengan syarat perkhidmatan**, kemudian pilih **Kemas kini**. Versi penyelesaian yang terkini akan dipasang.

Selepas pemasangan selesai, versi 4.5.0.134 anda akan dipasang.

## <a name="configure-new-features"></a>Konfigurasikan ciri baharu

### <a name="enable-dual-write-mapping"></a>Dayakan pemetaan dwitulis

Selepas anda melengkapkan kemas kini pada persekitaran Kewangan dan Dataverse, anda boleh mendayakan pemetaan dwitulis yang diperlukan. Selesaikan prosedur berikut untuk mendayakan pemetaan dwitulis.

- [Kemas kini tetapan keselamatan pada persekitaran Customer Engagement](#security)
- [Segar semula entiti data](#refresh)
- [Kemas kini dan jalankan pemetaan dwitulis](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Kemas kini tetapan keselamatan pada persekitaran Dataverse

Kemas kini berikut pada kelayakan keselamatan untuk entiti diperlukan sebagai sebahagian daripada kemas kini kepada UR5.

1. Dalam persekitaran Dataverse anda, pergi ke **Tetapan**, dan dalam kumpulan **Sistem**, pilih **Keselamatan**.

![Tetapan persekitaran Dataverse.](media/Picture21.png)

2. Pilih **Peranan Keselamatan**.
3. Daripada senarai peranan, pilih **pengguna aplikasi dwitulis** dan pilih tab **Entiti Tersuai**. 
4. Sahkan bahawa peranan mempunyai keizinan **Baca** dan **Tambah Pada** untuk:

      - **Jenis Kadar Tukaran Mata Wang**
      - **Carta Akaun** 
      - **Kalendar Fiskal** 
      - **Lejar**

5. Selepas peranan keselamatan dikemas kini, pergi ke **Tetapan** > **Keselamatan** > **Pasukan**. Sahkan bahawa peranan **pengguna aplikasi dwitulis** telah digunakan kepada pasukan. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Segar semula entiti data daripada kemas kini

1. Dalam persekitaran Kewangan anda, buka ruang kerja **Pengurusan data**, kemudian buka halaman **Parameter rangka kerja**.
2. Pada tab **Tetapan entiti**, pilih **Segar semula senarai entiti**.
3. Pilih **Tutup** untuk mengesahkan segar semula entiti.

 > [!NOTE]
 > Proses ini akan mengambil masa lebih kurang 20 minit untuk dilengkapkan. Anda akan dimaklumkan apabila segar semula selesai.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Kemas kini pemetaan dwitulis

1. Dalam ruang kerja **Pengurusan data**, pilih **Dwitulis**.
2. Pilih **Gunakan penyelesaian**, pilih kedua-dua penyelesaian dalam senarai, kemudian pilih **Gunakan**.
3. Pada halaman **Dwitulis**, pilih peta jadual berikut, kemudian pilih **Hentikan**.

    - **Aktual integrasi Project Operations (msdyn_actuals)**
    - **Kategori perbelanjaan projek integrasi Project Operations (msdyn_expensecategories)**
    - **Entiti eksport perbelanjaan projek aktual integrasi Project Operations (msdyn_expenses)**

4. Halaman **Versi peta jadual**, gunakan versi peta baharu pada setiap tiga entiti.
5. Pada halaman **Dwitulis**, pilih jalankan untuk mulakan semula peta.
6. Dari senarai peta, pilih peta **Ledger (msdyn_ledgers)** yang mempunyai semua prasyarat dan pilih kotak semak **Segerak awal**. 
7. **Dalam medan Induk untuk penyegerakan** awal, pilih **aplikasi** Kewangan dan Operasi dan kemudian pilih **Jalankan**.
 
 ![Penyegerakan peta lejar.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]