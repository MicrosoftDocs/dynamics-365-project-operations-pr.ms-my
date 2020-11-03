---
title: Gunakan tetapan demo dan data konfigurasi
description: Topik ini memberikan maklumat tentang cara menggunakan persediaan demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081093"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Gunakan persediaan demo dan data konfigurasi untuk pelaksanaan lite Project Operations - urusan untuk penginvoisan proforma

_**Pelaksanaan lite - urusan untuk penginvoisan proforma_

1. Muat turun [Pakej Data Induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigasi kepada folder *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan* dan jalankan fail yang boleh dilaksanakan, *DataMigrationUtility*.
3. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. Pada Halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Perlaksanaan**.
5. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
6. Pilih rantau penyewa anda, masukkan kelayakan anda dan kemudian pilih **Log masuk**.

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. Pada halaman 3, daripada senarai Organisasi pada Penyewa, pilih organisasi yang anda mahu import data demo dan pilih **Log masuk**.
8. Pada halaman 4, pilih fail zip, *MasterAndSetupData* daripada folder yang dibuka, *ProjOpsDemoDataSetupAndMaster - CMT Disepadukan*.

![Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. Selepas fail zip dipilih, pilih **Import Data**.

![Import data](./media/5ImportData.png)

10. Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda. Selepas import selesai, keluar dari Wizard CMT. 
11. Semak organisasi anda untuk data dalam 20 entiti berikut:

- Mata wang
- Unit Organisasi
- Orang Hubungan
- Cukai Kumpulan
- Kumpulan Pelanggan
- Unit
- Kumpulan Unit
- Senarai Harga
- Senarai Harga Parameter Projek
- Kekerapan Invois
- Butiran Kekerapan Invois
- Kategori Sumber Boleh Ditempah
- Kategori Transaksi
- Kategori Perbelanjaan
- Harga Peranan
- Harga Kategori Transaksi
- Ciri
- Sumber Boleh Ditempah
- Penyekutuan kategori sumber boleh ditempah
- Penyekutuan Cirian Sumber Boleh Ditempah

![Lengkapkan Import](./media/6CompleteImport.png)
