---
title: Sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Operasi Projek
description: Topik ini memberikan maklumat tentang menyediakan dan menggunakan data konfigurasi dalam Operasi Projek.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948990"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Sediakan dan gunakan data konfigurasi dalam Common Data Service untuk Operasi Projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="install-setup-and-configuration-data"></a>Memasang data persediaan dan konfigurasi

1. Muat turun, menyahsekat dan unzip [Pakej Data Persediaan dan Konfigurasi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Navigasi ke folder nyahzip dan jalankan fail boleh laku, *DataMigrationUtility*.
3. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. Pada halaman 2 dalam Wizard CMT, pilih **Office 365** sebagai **Jenis Pelaksanaan**.
5. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
6. Pilih rantau penyewa anda, masukkan kelayakan anda dan pilih **Log masuk**.

![Daftar Masuk Konfigurasi](./media/2ConfigurationSignin.png)

7. Pada halaman 3, daripada senarai organisasi pada penyewa, pilih organisasi yang anda mahu import data demo ke dalam dan pilih **log masuk**.
8. Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* dari folder tak padat.

![Pilihan Fail Zip](./media/3ZipFile.png)

![Pilih fail](./media/4SelectAFile.png)

9. Selepas fail zip dipilih, pilih **Import Data**.

![Import Data](./media/5ImportData.png)

10. Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda. Selepas import selesai, keluar dari CMT Wizard. 
11. Semak organisasi anda untuk data dalam 19 entiti berikut:

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

## <a name="update-project-operations-configurations"></a>Kemas kini konfigurasi Operasi Projek

1. Navigasi ke persekitaran CE. Anda boleh menemuinya dengan membuka Pusat pentadbir [Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih persekitaran dan kemudian memilih **Persekitaran Terbuka**. 

![Persekitaran Terbuka](./media/7OpenEnvironment.png)

2. Pergi ke **Sumber** > **Projek** dan kemudian pilih **Baharu** untuk mencipta sumber boleh ditempah untuk pengguna anda.

![Sumber Boleh Ditempah](./media/8BookableResources.png)

3. Pada tab **Umum**, pilih pengguna pentadbir anda. Sahkan bahawa zon waktu sepadan dengan yang anda berada. 

![Sumber Boleh Ditempah Baharu](./media/9NewBookableResource.png)

4. Pada tab **Penjadualan**, dalam medan **Syarikat**, pilih syarikat **USPM** dan kemudian pilih **Simpan**. 

![Tab Penjadualan](./media/10SchedulingTab.png)

5. Pilih tab **Waktu kerja**.  

![Jam Kerja](./media/11WorkHours.png)

6. Klik dua kali pada mana-mana nilai dalam kalendar dan pilih **Edit** > **Semua acara dalam siri ini**. 

![Kalendar Kerja](./media/12WorkCalendar.png)

7. Tukar masa kerja ke lapan (8) jam hari kerja, tandakan hujung minggu sebagai hari bukan kerja, dan pastikan zon waktu sepadan dengan anda. 
8. Pilih **Simpan dan tutup**.

![Kemas Kini Kalendar](./media/13UpdateCalendar.png)

9. Pergi ke **Tetapan** > **Templat kalendar** dan pilih **Baharu**.
 
 ![Templat Kalendar](./media/14CalendarTemplates.png)
 
 10. Masukkan nama, pilih sumber templat yang anda cipta dan kemudian pilih **Simpan**. 
 
 ![Simpan Templat Kalendar](./media/15SaveCalendarTemplate.png)
 
 11. Pergi ke **Parameter** dan klik dua kali pada rekod. 
 
 ![Parameter Projek](./media/16ProjectParameters.png)
 
12. Kemas kini medan berikut:

 - **Syarikat lalai**: USPM
 - **Unit Organisasi Lalai** : Contoso Robotics Global
 - **Frekuensi Invois**: Ketujuh dan Hari Terakhir
 - **Templat jam kerja**: Tukar ke templat yang anda cipta.

13. Pilih **Simpan**. 

![Parameter Projek Dikemas Kini](./media/17UpdatedProjectParameters.png)
