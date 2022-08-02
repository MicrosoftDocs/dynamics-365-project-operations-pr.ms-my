---
title: Aplikasi mudah alih lembaran masa projek
description: Artikel ini memberikan maklumat mengenai Microsoft Dynamics 365 Project Timesheet aplikasi mudah alih. Aplikasi mudah alih Lembaran masa Projek membolehkan pengguna untuk menyerahkan dan meluluskan lembaran masa untuk projek pada peranti mudah alih mereka.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110986"
---
# <a name="project-timesheet-mobile-application"></a>Aplikasi mudah alih lembaran masa projek

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Gambaran keseluruhan

Aplikasi Microsoft Dynamics 365 Project Timesheet mudah alih membolehkan pengguna menyerahkan dan meluluskan lembaran masa untuk projek pada peranti mudah alih mereka (iPhone atau Android). Aplikasi mudah alih ini memaparkan fungsi lembaran masa yang berada dalam bidang pengurusan Projek dan perakaunan Dynamics 365 Finance. Ia membantu meningkatkan produktiviti dan kecekapan pengguna, dan juga membolehkan kemasukan dan kelulusan lembaran masa projek tepat pada masanya.

## <a name="download-and-install-the-mobile-app"></a>Muat turun dan pasang tambahan aplikasi mudah alih

Muat turun dan pasang aplikasi mudah alih Microsoft Dynamics 365 Project Timesheet untuk Android atau iPhone daripada gedung mudah alih untuk peranti anda.

## <a name="enable-the-app"></a>Dayakan aplikasi 

Dalam Kewangan, aplikasi mudah alih Lembaran masa Projek mesti didayakan. Untuk mendayakan fungsi, pergi ke **Parameter pengurusan projek dan perakaunan \> Lembaran masa** dan pilih **Dayakan parameter Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Selesaikan isu daftar masuk

**Isu:** Semasa daftar masuk ke aplikasi Project Timesheet Mobile, pengguna menerima mesej ralat yang menyatakan bahawa mereka "tidak dapat mengakses aplikasi '2bc50526-cdc3-4e36-a970-c284c34cbd6e' dalam penyewa tersebut."

**Isu:** Semasa daftar masuk ke aplikasi Project Timesheet Mobile, pengguna menerima ralat yang menyerupai salah satu contoh berikut:

- "AADSTS50020: Akaun pengguna '[nama pengguna]' daripada pembekal identiti 'https://sts.windows.net/[id aplikasi]' tidak wujud dalam penyewa '[id penyewa]' dan tidak boleh mengakses aplikasi '[id aplikasi]' dalam penyewa itu."
- "Akaun pengguna terpilih tidak wujud dalam penyewa '[id penyewa]' dan tidak dapat mengakses aplikasi '[id aplikasi]' dalam penyewa itu."

**Penjelasan:** Isu-isu ini disebabkan oleh perubahan yang dibuat kepada Azure Active Directory (Azure AD) pada Mei 2022 dan yang berkaitan dengan pengguna luaran. Oleh kerana perubahan ini tidak dibuat untuk membiayai dan mengendalikan aplikasi, ia boleh mempengaruhi pelanggan pada mana-mana versi platform atau aplikasi.

**Betulkan:** Semua pengguna luaran mesti dijemput ke penyewa melalui Azure AD. Untuk maklumat lanjut, lihat [Jemput pengguna dengan Azure Active Directory kerjasama](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration) B2B.

## <a name="sign-in-to-the-app"></a>Daftar masuk ke aplikasi

1.  Mulakan peranti mudah alih anda.

2.  Masukkan URL Kewangan anda.

3.  Kali pertama anda mendaftar masuk, anda akan diprom untuk nama pengguna dan kata laluan anda. Masukkan kelayakan anda.

4. Anda akan log masuk ke syarikat lalai anda.

## <a name="submit-a-project-timesheet"></a>Mengemukakan lembaran masa projek

Anda boleh mencipta dan menyerahkan masa projek dalam aplikasi. Anda boleh menyimpan masa yang baharu untuk mendapatkan maklumat daripada tempoh masa sebelumnya, baris yang disimpan atau tugasan projek. Jika anda ditetapkan sebagai wakil, anda juga boleh memasukkan lembaran masa untuk pekerja lain. Untuk mencipta lembaran masa sebagai wakil, pilih butang **Menu** kemudian pilih nama sumber.

Lembaran masa yang akan mencipta lembaran masa baharu untuk tempoh suku tahun, berdasarkan pada tarikh semasa. Minggu kerja akan dipaparkan. Jika tempoh masa heet meliputi beberapa minggu, anda boleh memilih satu lagi kerja minggu dari tab minggu kerja.
Jika suatu tempoh masa yang tidak wujud untuk tarikh semasa, ia akan dipaparkan. Jika anda perlu membuat lembaran masa baharu dalam tempoh lembaran masa yang berbeza, pilih butang **Menu** dan kemudian pilih **Lembaran masa baharu**.

Anda boleh memasukkan maklumat projek dengan mengklik tindakan **Tambah masa** atau tindakan **Masa salinan daripada**. Tindakan **Masa salinan daripada** akan menyalin maklumat baris projek, tetapi bukan masa. Menu **Masa salinan daripada** termasuk pilihan berikut:

- **Salin daripada lembaran masa sedia ada** -Salin baris garisan bawah dari lembaran masa sedia ada.

- **Salin daripada kegemaran** - Cipta baris lembaan masa baharu dengan menggunakan tetapan lembaran masa yang anda pilih sebagai kegemaran.

- **Salin daripada tugasan** - Cipta baris lembaran masa baharu daripada projek yang ditugaskan.

Maklumat projek yang dipaparkan bergantung pada parameter mudah alih yang anda takrifkan pada halaman **Pengurusan projek dan parameter perakaunan**.

Dalam medan **Entiti sah**, pilih entiti sah yang anda lakukan kerja projek. Medan **Entiti sah** tersedia hanya jika sokongan heet masa antara syarikat telah didayakan untuk entiti sah anda.

Pilih pelanggan yang berkaitan dengan projek untuk lembaran masa. Untuk keluaran awal pada Android, entri oleh pelanggan tidak disokong, kerana anda mesti memilih projek terlebih dahulu. Jika anda memilih projek itu dahulu, medan **Pelanggan** diisi secara automatik.

Dalam medan **Projek**, pilih projek yang anda masukkan masa. Medan **Pelanggan** diisi secara automatik.

Carian pelanggan dan projek membolehkan pencarian merentasi kedua-dua pelanggan dan projek.

Pilih maklumat dalam **Kategori**, **Aktiviti**, **Sifat baris**, **Kumpulan cukai jualan** dan **Item medan kumpulan cukai jualan** seperti yang diperlukan. Medan ini boleh ditulis ganti.

Medan **Sifat baris** akan ditetapkan kepada nilai lalai, berdasarkan parameter pengurusan projek dan perakaunan. Apabila parameter projek/kategori dan kategori didayakan, nilai **Sifat baris** akan ditetapkan kepada nilai lalai yang telah anda takrifkan untuk pengesahan ini. Apabila parameter projek/kategori dan kategori/sumber tidak didayakan **, nilai sifat** Baris akan lalai mengikut **medan sifat** Dayakan baris lalai pada **halaman Pengurusan Projek dan parameter** perakaunan. Nilai **Sifat baris** boleh ditulis ganti.

Pilih hari untuk menambah masa. Masukkan jumlah jam yang anda kerjakan setiap hari.

Untuk menambah komen tentang waktu perniagaan yang anda masukkan, klik **Tambah komen**, kemudian masukkan komen untuk khalayak dalaman, khalayak pelanggan atau kedua-duanya.
Komen dalaman boleh dilihat oleh pengurus projek. Komen pelanggan akan dimasukkan ke invois.

Untuk menyimpan baris sebagai kegemaran, pilih kotak semak dan kemudian klik **Simpan sebagai kegemaran**.

Dimensi kewangan dan sokongan lampiran tidak disediakan dalam aplikasi mudah alih.

Teruskan menambah baris projek mengikut keperluan untuk melengkapkan lembaran masa anda.

Klik **Serahkan** untuk menghantar lembaran masa ke aliran kerja kelulusan.

## <a name="review-timesheets"></a>Semak lembaran masa

Senarai lembaran masa yang perlu disemak semula tersedia pada menu. Opsyen ini hanya tersedia jika anda telah ditetapkan sebagai pelulus aliran kerja. Kedua-dua pengepala dan kelulusan baris disokong. Kelulusan peringkat baris menawarkan keupayaan untuk menandakan satu atau lebih baris untuk diluluskan. Selepas meneliti maklumat heet masa, klik **Luluskan**, **Wakil** atau **Kembali** untuk meneruskan aliran kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
