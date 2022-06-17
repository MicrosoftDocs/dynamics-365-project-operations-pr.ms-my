---
title: Gunakan persediaan tunjuk cara dan data konfigurasi - lite
description: Artikel ini menyediakan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Operasi Projek.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 68e504dd031596b295b1383a8e81621744cae8d2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922325"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Gunakan persediaan tunjuk cara dan data konfigurasi dalam untuk Project Operations - lite 

_**Pelaksanaan lite - urusan untuk penginvoisan proforma_



## <a name="prerequisites"></a>Prasyarat

Sebelum anda memulakan konfigurasi, anda mesti mempunyai persekitaran Common Data Service (CDS) yang diperuntukkan untuk Dynamics 365 Project Operations.


## <a name="instructions"></a>Arahan

1. Muat turun [Pakej Data Induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Menavigasi ke folder *ProjOpsSampleSetupData - CE hanya CMT* dan jalankan fail boleh laksana, *DataMigrationUtility*.
3. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

    ![Migrasi Konfigurasi.](./media/1ConfigurationMigration.png)

4. Pada halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Pelaksanaan**.
5. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
6. Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.

   ![Daftar Masuk Konfigurasi.](./media/2ConfigurationSignin.png)

7. Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.
8. Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* daripada folder tidak dibungkus, *ProjOpsSampleSetupData - CE hanya CMT*.

   ![Fail zip.](./media/3ZipFile.png)

   ![Pilih fail.](./media/4SelectAFile.png)

9. Selepas fail zip dipilih, pilih **Import Data**.

   ![Import data.](./media/5ImportData.png)

10. Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda. Selepas import selesai, keluar dari Wizard CMT. 
11. Semak organisasi anda untuk data dalam 18 entiti berikut:

    -   Mata wang
    -   Akaun
    -   Unit Organisasi
    -   Kenalan
    -   Unit
    -   Kumpulan Unit
    -   Senarai Harga
    -   Senarai Harga Parameter Projek 
    -   Kekerapan Invois
    -   Kategori Sumber Boleh Ditempah
    -   Kategori Transaksi
    -   Kategori Perbelanjaan
    -   Harga Peranan
    -   Harga Kategori Transaksi
    -   Ciri
    -   Sumber Boleh Ditempah
    -   Penyekutuan kategori sumber boleh ditempah
    -   Penyekutuan Cirian Sumber Boleh Ditempah

    ![Import Selesai.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
