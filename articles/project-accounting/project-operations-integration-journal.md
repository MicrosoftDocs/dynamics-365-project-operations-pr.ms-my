---
title: Jurnal integrasi dalam Project Operations
description: Topik ini menyediakan maklumat tentang bekerja dengan jurnal integrasi dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948341"
---
# <a name="integration-journal-in-project-operations"></a>Jurnal integrasi dalam Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Entri masa dan perbelanjaan mencipta transaksi **Aktual** yang mewakili pandangan operasi bagi kerja yang diselesaikan terhadap projek. Dynamics 365 Project Operations menyediakan akauntan dengan alat untuk menyemak semula transaksi dan melaraskan atribut perakaunan seperti yang diperlukan. Selepas kajian semula dan pelarasan selesai, transaksi akan disiarkan ke sub lejar Projek dan Lejar Am. Akauntan boleh melaksanakan aktiviti ini menggunakan jurnal **Integrasi Project Operations**(**Dynamics 365 Finance** > **Pengurusan projek dan perakaunan** > **Jurnal** > **Integrasi Project Operations**.

![Aliran jurnal integrasi](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Cipta rekod dalam jurnal integrasi Project Operations

Rekod dalam jurnal integrasi Project Operations dicipta menggunakan proses berkala, **Import daripada jadual pemeringkatan**. Anda boleh menjalankan proses ini dengan pergi ke **Dynamics 365 Finance** > **Pengurusan projek dan perakaunan** > **Berkala** > **Integrasi Project Operations** > **Import daripada jadual pemeringkatan**. Anda boleh menjalankan proses secara interaktif atau mengkonfigurasi proses untuk berjalan dalam latar belakang apabila diperlukan.

Apabila proses berkala berjalan, sebarang aktual yang belum ditambah ke jurnal integrasi Project Operations ditemui. Baris jurnal untuk setiap transaksi aktual dicipta.
Sistem mengumpul baris jurnal ke dalam jurnal berasingan berasaskan pada nilai yang dipilih dalam medan **Unit berkala pada jurnal Integrasi Project Operations** (**Kewangan** > **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek**, tab **Project Operations pada Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk medan ini termasuk:

  - **Hari**: Aktual dikumpul mengikut tarikh transaksi. Jurnal berasingan dicipta untuk setiap hari.
  - **Bulan**: Aktual dikumpulkan mengikut bulan kalendar. Jurnal berasingan dicipta untuk setiap bulan.
  - **Tahun**: Aktual dikumpulkan mengikut tahun kalendar. Jurnal berasingan dicipta untuk setiap tahun.
  - **Semua**: Semua transaksi aktual disertakan dalam jurnal integrasi yang sama. Jika jurnal tidak tersedia apabila proses berkala berjalan, contohnya jika jurnal adalah dalam proses menyiarkan transaksi, jurnal baharu akan dicipta.

Baris jurnal dicipta berasaskan pada aktual projek. Senarai berikut termasuk beberapa peraturan lalai dan transformasi yang lebih penting:

  - Setiap transaksi aktual projek mempunyai baris dalam jurnal integrasi Project Operations. Transaksi jualan kos dan belum dibilkan untuk jenis pengebilan masa dan bahan ditunjukkan pada baris yang berasingan.
  - Medan **Tarikh** mewakili tarikh transaksi. Medan **Tarikh perakaunan** mewakili tarikh transaksi direkod ke lejar. Jika tarikh perakaunan adalah dalam [tempoh kewangan tertutup](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) dan parameter **Tetapkan tarikh perakaunan untuk membuka tempoh lejar secara automatik** ditetapkan pada tab **Kewangan** halaman **Parameter pengurusan projek dan perakaunan**, sistem akan melaraskan tarikh perakaunan transaksi ke tarikh pertama dalam tempoh lejar terbuka seterusnya.
  - Medan **Baucar** menunjukkan nombor baucar untuk setiap transaksi aktual. Jujukan nombor baucar ditakrifkan pada tab **Jujukan nombor** pada halaman **Parameter pengurusan projek dan perakaunan**. Setiap baris ditugaskan nombor baharu. Selepas baucar disiarkan, anda boleh melihat cara kos dan transaksi jualan tidak dibilkan dikaitkan dengan memilih **Baucar berkaitan** pada halaman **Transaksi baucar**.
  - Medan **Kategori** mewakili transaksi projek dan lalai berasaskan pada kategori transaksi untuk projek aktual berkaitan.
    - Jika **Kategori transaksi** ditetapkan dalam aktual Projek dan **Kategori projek** berkaitan wujud dalam entiti sah yang diberikan, kategori dilalaikan ke kategori projek ini.
    - Jika **Kategori transaksi** tidak disediakan dalam aktual Projek, sistem menggunakan nilai dalam medan **Kategori Project lalai** pada **Project Operations pada tab Dynamics 365 Customer Engagement** pada halaman **Parameter pengurusan projek dan perakaunan**.
  - Medan **Sumber** mewakili sumber projek berkaitan dengan transaksi ini. Sumber digunakan sebagai rujukan dalam cadangan invois Projek kepada pelanggan.
  - Medan **Kadar pertukaran** lalai daripada **Kadar pertukaran mata wang** ditetapkan dalam Dynamics 365 Finance. Jika tetapan kadar pertukaran hilang, proses berkala **Import daripada pemeringkatan** tidak akan menambah rekod ke jurnal dan mesej ralat akan ditambah ke log pelaksanaan kerja.
  - Medan **Sifat baris** mewakili jenis pengebilan dalam aktual Projek. Sifat baris dan pemetaan jenis pengebilan ditakrifkan pada tab **Project Operations pada Dynamics 365 Customer Engagement** pada halaman **Parameter pengurusan projek dan perakaunan**.

Hanya atribut perakaunan berikut boleh dikemaskini dalam baris jurnal integrasi Project Operations:

- **Kumpulan cukai jualan pengebilan** dan **Kumpulan cukai jualan item pengebilan**
- **Dimensi kewangan** (menggunakan tindakan **Agihkan amaun**)

Baris jurnal integrasi boleh dipadamkan, walau bagaimanapun sebarang baris yang belum disiarkan akan dimasukkan ke dalam jurnal sekali lagi selepas anda menjalankan semula proses berkala **Import daripada pemeringkatan**.

Apabila anda menyiarkan jurnal integrasi, sub lejar projek dan transaksi lejar am dicipta. Ini digunakan dalam penginvoisan pelanggan hiliran, pengiktirafan hasil dan pelaporan kewangan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]