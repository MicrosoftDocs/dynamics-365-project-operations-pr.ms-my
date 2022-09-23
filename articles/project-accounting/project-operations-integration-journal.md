---
title: Jurnal integrasi dalam Project Operations
description: Artikel ini menyediakan maklumat tentang bekerja dengan jurnal Integrasi dalam Operasi Projek.
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

Masa, perbelanjaan, yuran, dan penyertaan bahan membuat **Transaksi sebenar** yang mewakili pandangan operasi kerja yang diselesaikan terhadap projek. Dynamics 365 Project Operations menyediakan akauntan dengan alat untuk menyemak semula transaksi dan melaraskan atribut perakaunan seperti yang diperlukan. Selepas kajian semula dan pelarasan selesai, transaksi akan disiarkan ke sub lejar Projek dan Lejar Am. Akauntan boleh melakukan aktiviti ini menggunakan **jurnal Integrasi** Operasi Projek (**Dynamics 365 Finance** > **Projek pengurusan dan perakaunan** > **Jurnal** > **Operasi Projek Integrasi** jurnal.

![Aliran jurnal integrasi.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Cipta rekod dalam jurnal integrasi Project Operations

Rekod dalam jurnal integrasi Project Operations dicipta menggunakan proses berkala, **Import daripada jadual pemeringkatan**. Anda boleh menjalankan proses ini dengan pergi ke **Dynamics 365 Finance** > **Projek pengurusan dan perakaunan** > **Periodic** > **Project Operations Integration** > **Import dari jadual** pementasan. Anda boleh menjalankan proses secara interaktif atau mengkonfigurasi proses untuk berjalan dalam latar belakang apabila diperlukan.

Apabila proses berkala berjalan, sebarang aktual yang belum ditambah ke jurnal integrasi Project Operations ditemui. Baris jurnal untuk setiap transaksi aktual dicipta.
Sistem ini mengumpulkan garis jurnal ke dalam jurnal berasingan berdasarkan nilai yang dipilih dalam **unit Tempoh pada bidang jurnal** Integrasi Operasi Projek (**pengurusan Projek Kewangan** > **dan perakaunan** > **Persediaan** > **Projek pengurusan dan parameter** perakaunan, **Operasi Projek pada tab Dynamics 365 Customer Engagement**). Nilai yang mungkin untuk medan ini termasuk:

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
    - Jika **kategori** Transaksi tidak disetkan dalam Projek sebenar, sistem menggunakan nilai dalam **medan lalai** kategori Projek pada **tab Operasi Projek pada Dynamics 365 Customer Engagement** pada **halaman Parameter** pengurusan dan perakaunan Projek.
  - Medan **Sumber** mewakili sumber projek berkaitan dengan transaksi ini. Sumber digunakan sebagai rujukan dalam cadangan invois Projek kepada pelanggan.
  - Medan **kadar** Pertukaran lalai daripada **kadar** pertukaran Mata wang yang ditetapkan dalam Dynamics 365 Finance. Jika tetapan kadar pertukaran hilang, proses berkala **Import daripada pemeringkatan** tidak akan menambah rekod ke jurnal dan mesej ralat akan ditambah ke log pelaksanaan kerja.
  - Medan **Sifat baris** mewakili jenis pengebilan dalam aktual Projek. Pemetaan sifat baris dan jenis pengebilan ditakrifkan pada **Tab Operasi Projek pada Dynamics 365 Customer Engagement** pada **halaman Parameter** pengurusan dan perakaunan Projek.

Hanya atribut perakaunan berikut boleh dikemaskini dalam baris jurnal integrasi Project Operations:

- **Kumpulan cukai jualan pengebilan** dan **Kumpulan cukai jualan item pengebilan**
- **Dimensi kewangan** (menggunakan tindakan **Agihkan amaun**)

Baris jurnal integrasi boleh dipadamkan. Walau bagaimanapun, mana-mana baris yang tidak disiarkan akan dimasukkan ke dalam jurnal sekali lagi selepas anda menjalankan **semula Import daripada pementasan** proses berkala.

### <a name="post-the-project-operations-integration-journal"></a>Siarkan jurnal integrasi Operasi Projek

Apabila anda menyiarkan jurnal integrasi, sub lejar projek dan transaksi lejar am dicipta. Ini digunakan dalam penginvoisan pelanggan hiliran, pengiktirafan hasil dan pelaporan kewangan.

Jurnal integrasi Operasi Projek yang dipilih boleh disiarkan dengan menggunakan **Post** pada halaman jurnal integrasi Operasi Projek. Semua jurnal boleh disiarkan secara automatik dengan menjalankan proses di **jurnal** > **integrasi Operasi** > **Projek Berkala** Pasca Operasi Projek.

Posting boleh dilakukan secara interaktif atau dalam satu kumpulan. Perhatikan bahawa semua jurnal yang mempunyai lebih daripada 100 baris akan disiarkan secara automatik dalam satu kumpulan. Untuk prestasi yang lebih baik apabila jurnal yang mempunyai banyak baris disiarkan dalam kelompok, dayakan **jurnal penyepaduan Operasi Pasca Projek menggunakan pelbagai ciri tugas** kelompok dalam **ruang kerja pengurusan** Ciri. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Pindahkan semua baris yang mempunyai ralat penyiaran ke jurnal baru

> [!NOTE]
> Untuk menggunakan keupayaan ini, dayakan **Pindahkan semua baris dengan ralat pengeposan ke ciri jurnal** penyepaduan Operasi Projek baharu dalam **ruang kerja pengurusan** Ciri.

Ciri ini membantu meningkatkan pengalaman dengan jurnal integrasi Operasi Projek. Apabila diaktifkan, isu masa dwi-tulis dan isu persediaan tidak lagi menghalang jurnal yang sah daripada disiarkan. Semasa menyiarkan jurnal integrasi Operasi Projek, sistem mengesahkan setiap baris dalam jurnal. Ia menyiarkan semua baris yang tidak mempunyai kesilapan dan mencipta jurnal baru untuk semua baris yang mempunyai kesilapan penyiaran.

Untuk mengkaji semula jurnal yang mempunyai baris ralat penyiaran, pergi ke **jurnal** integrasi Pengurusan projek dan perakaunan \>**Journals** \>**Project** Operations, dan menapis senarai jurnal dengan menggunakan **bidang jurnal** Asal. Ilustrasi berikut menunjukkan contoh di mana jurnal pada **halaman jurnal** integrasi Operasi Projek telah ditapis dengan cara ini.

![Jurnal asal ditunjukkan di halaman jurnal integrasi Operasi Projek.](./media/transferLines-originalJournal.png)

Sekiranya kerja kelompok berkala dikonfigurasikan untuk menyiarkan jurnal integrasi, penyiaran akan ditembusi semula, dan jurnal akan disiarkan jika isu masa telah ditetapkan. Mana-mana jurnal yang tinggal perlu disiasat secara manual dengan menyemak balak dan mengambil tindakan yang diperlukan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
