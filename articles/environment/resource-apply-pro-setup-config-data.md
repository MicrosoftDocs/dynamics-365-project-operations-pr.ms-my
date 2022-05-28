---
title: Sediakan dan gunakan data konfigurasi dalam Common Data Service
description: Topik ini memberikan maklumat tentang menyediakan dan menggunakan data konfigurasi dalam Operasi Projek.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6fb91de30a2414fa7dd8dba47b28cf4824948565
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594727"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Sediakan dan gunakan data konfigurasi dalam Common Data Service 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_



## <a name="prerequisites"></a>Prasyarat

Sebelum anda mula mengkonfigurasikan data dalam Common Data Service (CDS), prasyarat berikut mesti dipenuhi:

1.  Sediakan persekitaran CDS dan persekitaran yang Dynamics 365 Finance untuk Operasi Projek.
2.  Maklumat entiti undang-undang dari Dynamics 365 Finance dikongsi ke persekitaran CDS. Ini bermaksud bahawa entiti **Syarikat** dalam CDS mempunyai rekod syarikat berikut:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Memasang data persediaan dan konfigurasi

1. Muat turun, menyahsekat dan unzip [Pakej Data Persediaan dan Konfigurasi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Navigasi ke folder nyahzip dan jalankan fail boleh laku, *DataMigrationUtility*.
3. Pada halaman 1 dalam Wizard Penghijrahan Konfigurasi (CMT) Common Data Service, pilih **Import Data** dan kemudian pilih **Teruskan**.

![Migrasi Konfigurasi.](./media/1ConfigurationMigration.png)

4. Pada halaman 2 dalam Wizard CMT, pilih **Microsoft 365** sebagai **Jenis Pelaksanaan**.
5. Pilih **Paparkan senarai organisasi tersedia** dan kotak semak **Tunjukkan Lanjutan**.
6. Pilih rantau penyewa anda, masukkan kelayakan anda dan pilih **Log masuk**.

![Daftar Masuk Konfigurasi.](./media/2ConfigurationSignin.png)

7. Pada halaman 3, daripada senarai organisasi pada penyewa, pilih organisasi yang anda mahu import data demo ke dalam dan pilih **log masuk**.
8. Pada halaman 4, pilih fail zip, *SampleSetupAndConfigData* dari folder tak padat.

![Pilihan Fail Zip.](./media/3ZipFile.png)

![Pilih fail.](./media/4SelectAFile.png)

9. Selepas fail zip dipilih, pilih **Import Data**.

![Import Data.](./media/5ImportData.png)

10. Import akan berjalan selama kira-kira 2-10 minit bergantung pada kelajuan rangkaian anda. Selepas import selesai, keluar dari CMT Wizard. 
11. Semak organisasi anda untuk data dalam 26 entiti berikut:

  - Mata wang
  - Carta Akaun
  - Kalendar Fiskal
  - Jenis Kadar Tukaran Mata Wang
  - Hari Pembayaran
  - Jadual Pembayaran
  - Terma Pembayaran
  - Unit Organisasi
  - Kenalan
  - Cukai Kumpulan
  - Kumpulan Pelanggan
  - Kumpulan Vendor
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

![Import Selesai.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Kemas kini konfigurasi Operasi Projek

1. Navigasi ke persekitaran CE. Anda boleh menemuinya dengan membuka Pusat pentadbir [Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih persekitaran dan kemudian memilih **Persekitaran Terbuka**. 

![Persekitaran Terbuka.](./media/7OpenEnvironment.png)

2. Pergi ke **Sumber** > **Projek** dan kemudian pilih **Baharu** untuk mencipta sumber boleh ditempah untuk pengguna anda.

![Sumber Boleh Ditempah.](./media/8BookableResources.png)

3. Pada tab **Umum**, pilih pengguna pentadbir anda. Sahkan bahawa zon waktu sepadan dengan yang anda berada. 

![Sumber Boleh Ditempah Baharu.](./media/9NewBookableResource.png)

4. Pada tab **Penjadualan**, dalam medan **Syarikat**, pilih syarikat **USPM** dan kemudian pilih **Simpan**. 

![Tab Penjadualan.](./media/10SchedulingTab.png)

5. Pilih tab **Waktu kerja**.  

![Jam Kerja.](./media/11WorkHours.png)

6. Klik dua kali pada mana-mana nilai dalam kalendar dan pilih **Edit** > **Semua acara dalam siri ini**. 

![Kalendar Kerja.](./media/12WorkCalendar.png)

7. Tukar masa kerja ke lapan (8) jam hari kerja, tandakan hujung minggu sebagai hari bukan kerja, dan pastikan zon waktu sepadan dengan anda. 
8. Pilih **Simpan dan tutup**.

![Kemas kini Kalendar.](./media/13UpdateCalendar.png)

9. Pergi ke **Tetapan** > **Templat kalendar** dan pilih **Baharu**.
 
 ![Templat Kalendar.](./media/14CalendarTemplates.png)
 
 10. Masukkan nama, pilih sumber templat yang anda cipta dan kemudian pilih **Simpan**. 
 
 ![Simpan Templat Kalendar.](./media/15SaveCalendarTemplate.png)
 
 11. Pergi ke **Parameter** dan klik dua kali pada rekod. 
 
 ![Parameter Projek.](./media/16ProjectParameters.png)
 
12. Kemas kini medan berikut:

 - **Syarikat lalai**: USPM
 - **Unit Organisasi Lalai** : Contoso Robotics Global
 - **Frekuensi Invois**: Ketujuh dan Hari Terakhir
 - **Templat jam kerja**: Tukar ke templat yang anda cipta.

13. Pilih **Simpan**. 

![Parameter Projek yang Dikemas kini.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
