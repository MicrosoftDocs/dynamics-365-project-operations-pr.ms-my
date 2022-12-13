---
title: Gunakan persediaan tunjuk cara dan data konfigurasi - lite
description: Artikel ini memberikan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811037"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Gunakan persediaan tunjuk cara dan data konfigurasi dalam untuk Project Operations - lite 

_**Pelaksanaan lite - urusan untuk penginvoisan proforma_



## <a name="prerequisites"></a>Prasyarat

Sebelum anda memulakan konfigurasi, anda mesti mempunyai persekitaran Dataverse yang diperuntukkan untuk Dynamics 365 Project Operations.


## <a name="instructions"></a>Arahan

1.  [Muat turun pakej data persediaan](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Menavigasi ke folder *ProjOpsSampleSetupData - CE hanya CMT* dan jalankan fail boleh laksana, *DataMigrationUtility*.
1. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

    ![Migrasi Konfigurasi.](./media/1ConfigurationMigration.png)

1. Pada halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Pelaksanaan**.
1. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
1. Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.

   ![Daftar Masuk Konfigurasi.](./media/2ConfigurationSignin.png)

1. Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.
1. Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* daripada folder tidak dibungkus, *ProjOpsSampleSetupData - CE hanya CMT*.

   ![Fail zip.](./media/3ZipFile.png)

   ![Pilih fail.](./media/4SelectAFile.png)

1. Selepas fail zip dipilih, pilih **Import Data**.

   ![Import data.](./media/5ImportData.png)

1. Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda. Selepas import selesai, keluar dari Wizard CMT. 
1. Semak organisasi anda untuk data dalam 18 entiti berikut:

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
