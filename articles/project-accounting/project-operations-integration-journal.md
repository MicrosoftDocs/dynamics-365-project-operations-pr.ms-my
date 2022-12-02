---
title: Jurnal integrasi dalam Project Operations
description: Artikel ini menyediakan maklumat tentang bekerja dengan jurnal Integrasi dalam Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541089"
---
# <a name="integration-journal-in-project-operations"></a>Jurnal integrasi dalam Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Entri masa, perbelanjaan, yuran dan bahan mencipta transaksi **Aktual** yang mewakili pandangan operasi bagi kerja yang diselesaikan terhadap projek. Dynamics 365 Project Operations menyediakan akauntan dengan alat untuk menyemak semula transaksi dan melaraskan atribut perakaunan seperti yang diperlukan. Selepas kajian semula dan pelarasan selesai, transaksi akan disiarkan ke sub lejar Projek dan Lejar Am. Akauntan boleh melaksanakan aktiviti ini menggunakan jurnal **Integrasi Project Operations** (**Dynamics 365 Finance** > **Pengurusan projek dan perakaunan** > **Jurnal** >  jurnal **Integrasi Project Operations**.

![Aliran jurnal integrasi.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Cipta rekod dalam jurnal integrasi Project Operations

Rekod dalam jurnal integrasi Project Operations dicipta menggunakan proses berkala, **Import daripada jadual pemeringkatan**. Anda boleh menjalankan proses ini dengan pergi ke **Dynamics 365 Finance** > **Pengurusan projek dan perakaunan** > **Berkala** > **Integrasi Project Operations** > **Import daripada jadual pemeringkatan**. Anda boleh menjalankan proses secara interaktif atau mengkonfigurasi proses untuk berjalan dalam latar belakang apabila diperlukan.

Apabila proses berkala berjalan, sebarang aktual yang belum ditambah ke jurnal integrasi Project Operations ditemui. Baris jurnal untuk setiap transaksi aktual dicipta.
Sistem mengumpul baris jurnal ke dalam jurnal berasingan berasaskan pada nilai yang dipilih dalam medan **Unit berkala pada jurnal Integrasi Project Operations** (tab **Finance** > **Pengurusan projek dan perakaunan** > **Persediaan** > **Parameter pengurusan projek dan perakaunan**, **Project Operations pada Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk medan ini termasuk:

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
    - Jika **Kategori transaksi** tidak ditetapkan dalam aktual Projek, sistem menggunakan nilai dalam medan **Lalai kategori projek** pada tab **Project Operations pada Dynamics 365 Customer Engagement** pada halaman **Parameter pengurusan projek dan perakaunan**.
  - Medan **Sumber** mewakili sumber projek berkaitan dengan transaksi ini. Sumber digunakan sebagai rujukan dalam cadangan invois Projek kepada pelanggan.
  - Medan **Kadar pertukaran** lalai daripada **Kadar pertukaran mata wang** yang ditetapkan dalam Dynamics 365 Finance. Jika tetapan kadar pertukaran hilang, proses berkala **Import daripada pemeringkatan** tidak akan menambah rekod ke jurnal dan mesej ralat akan ditambah ke log pelaksanaan kerja.
  - Medan **Sifat baris** mewakili jenis pengebilan dalam aktual Projek. Sifat baris dan pemetaan jenis pengebilan ditakrifkan pada tab **Project Operations pada Dynamics 365 Customer Engagement** pada halaman **Parameter pengurusan projek dan perakaunan**.

Hanya atribut perakaunan berikut boleh dikemaskini dalam baris jurnal integrasi Project Operations:

- **Kumpulan cukai jualan pengebilan** dan **Kumpulan cukai jualan item pengebilan**
- **Dimensi kewangan** (menggunakan tindakan **Agihkan amaun**)

Garisan jurnal integrasi boleh dipadamkan. Walau bagaimanapun, mana-mana baris yang tidak disiarkan akan dimasukkan ke dalam jurnal sekali lagi selepas anda menjalankan semula proses berkala **Import daripada pemeringkatan**.

### <a name="post-the-project-operations-integration-journal"></a>Siarkan jurnal integrasi Project Operations

Apabila anda menyiarkan jurnal integrasi, sub lejar projek dan transaksi lejar am dicipta. Ini digunakan dalam penginvoisan pelanggan hiliran, pengiktirafan hasil dan pelaporan kewangan.

Jurnal integrasi Project Operations yang dipilih boleh disiarkan dengan menggunakan **Siar** pada halaman jurnal integrasi Project Operations. Semua Jurnal boleh disiarkan secara automatik dengan menjalankan proses di **Berkala** > **integrasi Project Operations** > **Siarkan jurnal integrasi Project Operations**.

Siaran boleh dilaksanakan secara interaktif atau dalam kelompok. Harap maklum bahawa semua jurnal yang mempunyai lebih daripada 100 baris akan disiarkan dalam kelompok secara automatik. Untuk prestasi yang lebih baik apabila jurnal yang mempunyai banyak baris disiarkan dalam kelompok, dayakan ciri **Siarkan jurnal integrasi Project Operations menggunakan berbilang tugas kelompok** dalam ruang kerja **Pengurusan ciri**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Pindahkan semua baris yang mempunyai ralat penyiaran kepada jurnal baharu

> [!NOTE]
> Untuk menggunakan keupayaan ini, dayakan ciri **Pindahkan semua baris dengan ralat penyiaran kepada jurnal integrasi Project Operations baharu** ciri dalam ruang kerja **Pengurusan ciri**.

Ciri ini membantu dalam meningkatkan pengalaman dengan jurnal integrasi Project Operations. Apabila didayakan, isu pemasaan dwitulis dan isu persediaan tidak lagi menghalang jurnal yang sah daripada disiarkan. Semasa penyiaran ke jurnal integrasi Project Operations, sistem mengesahkan setiap baris dalam jurnal. Ia menyiarkan semua baris yang tidak mempunyai ralat dan mencipta jurnal baharu untuk semua baris yang mempunyai ralat penyiaran.

Untuk menyemak jurnal yang mempunyai baris ralat penyiaran, pergi ke **Pengurusan projek dan perakaunan** \> **Jurnal** \> **Jurnal integrasi Project Operations** dan tapis senarai jurnal dengan menggunakan medan **Jurnal asal**. Ilustrasi berikut menunjukkan contoh apabila jurnal pada halaman **Jurnal integrasi Project Operations** telah ditapis dengan cara ini.

![Jurnal asal ditunjukkan pada halaman jurnal integrasi Project Operations.](./media/transferLines-originalJournal.png)

Jika kerja kelompok secara berkala dikonfigurasikan untuk menyiarkan jurnal integrasi, penyiaran akan dicuba semula dan jurnal akan disiarkan jika isu pemasaan telah dibetulkan. Mana-mana jurnal yang tinggal hendaklah disiasat secara manual dengan menyemak log dan mengambil apa-apa tindakan yang diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
