---
title: Pemprosesan resit perbelanjaan
description: Topik ini menyediakan maklumat tentang pemprosesan pengecaman aksara optik (OCR) untuk resit. Ciri ini direka untuk menambah baik pengalamanan pengguna apabila laporan perbelanjaan dicipta dalam Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0d43c44bf4f2a58e3249d6cc1028353555cfd836580a802ad6e1878dc9b2e263
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001397"
---
# <a name="expense-receipt-processing"></a>Pemprosesan resit perbelanjaan

Entri perbelanjaan telah dipertingkatkan melalui pengenalan pemprosesan pengecaman aksara optik (OCR) untuk resit. Ciri ini direka untuk menambah baik pengalamanan pengguna apabila laporan perbelanjaan dicipta.

## <a name="key-features"></a>Ciri utama

- Nama peniaga, tarikh dan jumlah amaun diekstrak daripada resit.
- Ciri ini akan cuba memadankan resit yang tidak dilampirkan kepada transaksi perbelanjaan yang tidak dilampirkan.
- Pengguna boleh mencipta transaksi perbelanjaan yang dimasukkan secara manual daripada resit.

## <a name="usage-examples"></a>Contoh penggunaan

Untuk melampirkan resit secara automatik termasuk transaksi kad kredit apabila laporan perbelanjaan dicipta, lakukan langkah berikut:

  1. Buka ruang kerja **Pengurusan perbelanjaan**.
  2. Pada tab **Resit**, sahkan resit tidak dilampirkan wujud. Anda juga boleh muat naik resit pada tab **Resit**.
  3. Pada tab **Perbelanjaan**, sahkan perbelanjaan tidak dilampirkan wujud. Kebiasaannya, pentadbir perbelanjaan mengimport perbelanjaan ini daripada pembekal kad kredit.
  4. Pilih **Laporan perbelanjaan baharu**. Perhatikan bahawa anda boleh memasukkan perbelanjaan dan resit, kini juga, apabila anda mencipta laporan perbelanjaan. Jika anda menambah kedua-dua perbelanjaan dan resit, pemadanan automatik bagi resit berbanding perbelanjaan dicetuskan.

Untuk mencipta perbelanjaan atau memadankan perbelanjaan daripada resit, lakukan langkah berikut:

  1. Pada laporan perbelanjaan, pada tab **Resit**, lampirkan resit dengan memilih **Tambah resit**.
  2. Di bawah imej yang dimuat naik resit, perhatikan pilihan **Cipta** dan **Padan**.

      - Pilih **Cipta** untuk mencipta transaksi perbelanjaan yang dimasukkan secara manual dan isikan nilai yang diekstrak daripada resit.
      - Jika anda memilih **Padan**, sistem cuba memadankan perbelanjaan sedia ada kepada resit.

## <a name="installation"></a>Pemasangan

Ciri ini berfungsi bersama dengan ciri **Laporan perbelanjaan dibentuk semula** untuk membantu meringkaskan pengalaman perbelanjaan. Ciri ini hanya tersedia untuk persekitaran Peringkat 2+, yang merupakan Kotak pasir dan Pengeluaran.

Untuk menggunakan keupayaan perbelanjaan lanjutan ini, pasang tambahan Perkhidmatan Pengurusan Perbelanjaan for Microsoft Dynamics 365 Finance dan hidupkan ciri dalam tika anda. Anda boleh mengakses tambahan daripada projek anda dalam Microsoft Dynamics Lifecycle Services (LCS).

1. Log masuk ke dalam LCS dan buka persekitaran yang dikehendaki.
2. Pergi ke **Butiran penuh**.
3. Pilih **Kekalkan** atau tatal ke bawah ke FastTab **Tambahan persekitaran**.
4. Pilih **Pasangkan tambahan baharu**.
5. Pilih **Perkhidmatan Pengurusan Perbelanjaan**.
6. Ikuti panduan pemasangan dan bersetuju dengan terma dan syarat.
7. Pilih **Pasang**.

Dalam ruang kerja **Pengurusan ciri**, hidupkan ciri berikut:

- Laporan perbelanjaan digambarkan semula
- Padankan secara automatik dan cipta perbelanjaan daripada resit

Apabila anda menghidupkan ciri ini, tindakan berikut berlaku:

- Ruang kerja **Pengurusan perbelanjaan** sedia ada diganti dengan ruang kerja baharu.
- Item menu baharu untuk keterlihatan medan perbelanjaan ditambah.
- Anda masih boleh membuka halaman **Laporan perbelanjaan** dengan pergi ke **Pengurusan perbelanjaan > Perbelanjaan saya > Laporan perbelanjaan**.
- Aliran kerja dan sebarang kelulusan masih akan membawa anda ke halaman laporan perbelanjaan sedia ada.
- Resit akan diproses melalui Microsoft Azure Cognitive Services dan metadata akan diekstrak dan ditambah.
- Pilihan ditambah membolehkan anda mencipta laporan perbelanjaan yang merangkumi resit yang tidak dilampirkan dipadankan.
- Pilihan yang ditambahkan ke laporan perbelanjaan membolehkan anda mencipta baris perbelanjaan daripada resit atau cuba untuk memadankan resit sedia ada ke baris perbelanjaan sedia ada.

Untuk mendapatkan maklumat lanjut tentang ciri Laporan perbelanjaan dibentuk semula, lihat [Laporan perbelanjaan dibentuk semula](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Soalan lazim

**Adakah Microsoft menggunakan data saya untuk modelnya?**

Tidak, Microsoft telah membina model pembelajaran mesin umum untuk perkhidmatan pemprosesan penerimaannya. Model ini tidak berasaskan pada resit yang anda muat naik.

**Di manakah ciri ini tersedia dan diproses?**

Pada masa ini, Amerika Syarikat disokong.

**Di manakah resit saya pergi?**

Kewangan akan menghubungi Perkhidmatan Kognitif untuk mengekstrak data medan. Perkhidmatan Kognitif akan menyimpan salinan resit anda untuk tempoh masa hingga 24 jam selepas pemprosesan berlaku. Selepas pemprosesan selesai, Perkhidmatan Kognitif akan mengalih keluar resit. Resit masih disimpan dalam Kewangan.

Untuk maklumat lanjut, lihat [Dayakan pemahaman resit dengan keupayaan baharu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]