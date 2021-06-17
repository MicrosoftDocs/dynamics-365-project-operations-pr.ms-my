---
title: Gunakan persediaan tunjuk cara dan data konfigurasi - lite
description: Topik ini memberikan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997162"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Gunakan persediaan tunjuk cara dan data konfigurasi dalam untuk Project Operations - lite 

_**Pelaksanaan lite - urusan untuk penginvoisan proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Prasyarat

Sebelum anda memulakan konfigurasi, anda mesti mempunyai persekitaran Common Data Service (CDS) yang diperuntukkan untuk Dynamics 365 Project Operations.


## <a name="instructions"></a>Arahan

1. Muat turun [Pakej Data Induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Menavigasi ke folder *ProjOpsSampleSetupData - CE hanya CMT* dan jalankan fail boleh laksana, *DataMigrationUtility*.
3. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

    ![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. Pada Halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Perlaksanaan**.
5. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
6. Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.

   ![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.
8. Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* daripada folder tidak dibungkus, *ProjOpsSampleSetupData - CE hanya CMT*.

   ![Fail Zip](./media/3ZipFile.png)

   ![Pilih fail](./media/4SelectAFile.png)

9. Selepas fail zip dipilih, pilih **Import Data**.

   ![Import data](./media/5ImportData.png)

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

    ![Lengkapkan Import](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
