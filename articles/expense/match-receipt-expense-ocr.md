---
title: Padankan resit dengan perbelanjaan menggunakan OCR
description: Topik ini menyediakan maklumat tentang pemprosesan pengecaman aksara optik (OCR) untuk resit.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897012"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Padankan resit dengan perbelanjaan menggunakan OCR

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Entri perbelanjaan telah dipertingkatkan melalui pengenalan pemprosesan pengecaman aksara optik (OCR) untuk resit. Fungsian ini direka bentuk untuk meningkatkan pengalaman pengguna semasa mencipta laporan perbelanjaan.

## <a name="key-features"></a>Ciri utama

- Sistem mengekstrak nama saudagar, tarikh dan amaun jumlah daripada resit.
- Sistem akan cuba memadankan resit yang tidak dilampirkan untuk transaksi perbelanjaan tidak dilampirkan.
- Anda boleh mencipta transaksi perbelanjaan secara manual daripada resit.

## <a name="attach-receipts-to-an-expense-report"></a>Lampirkan resit ke laporan perbelanjaan

Untuk melampirkan resit secara automatik termasuk transaksi kad kredit apabila laporan perbelanjaan dicipta, lengkapkan langkah berikut.

  1. Buka ruang kerja **Pengurusan perbelanjaan**.
  2. Pada tab **Resit**, sahkan resit tidak dilampirkan wujud. Anda juga boleh muat naik resit pada tab **Resit**.
  3. Pada tab **Perbelanjaan**, sahkan perbelanjaan tidak dilampirkan wujud. Kebiasaannya, pentadbir perbelanjaan mengimport perbelanjaan ini daripada pembekal kad kredit.
  4. Pilih **Laporan perbelanjaan baharu**. Perhatikan bahawa anda boleh memasukkan perbelanjaan dan resit, kini juga, apabila anda mencipta laporan perbelanjaan. Jika anda menambah kedua-dua perbelanjaan dan resit, pemadanan automatik bagi resit berbanding perbelanjaan dicetuskan.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Cipta dan padan resit ke laporan perbelanjaan
Untuk mencipta perbelanjaan atau memadankan perbelanjaan daripada resit, lengkapkan langkah berikut.

  1. Pada laporan perbelanjaan, pada tab **Resit**, lampirkan resit dengan memilih **Tambah resit**.
  2. Di bawah imej yang dimuat naik resit, perhatikan pilihan **Cipta** dan **Padan**.

      - Pilih **Cipta** untuk mencipta transaksi perbelanjaan yang dimasukkan secara manual dan isikan nilai yang diekstrak daripada resit.
      - Jika anda memilih **Padan**, sistem cuba memadankan perbelanjaan sedia ada kepada resit.

## <a name="installation"></a>Pemasangan

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

## <a name="frequently-asked-questions"></a>Soalan lazim

**Adakah Microsoft menggunakan data saya untuk modelnya?**

Tidak, Microsoft telah membina model pembelajaran mesin umum untuk perkhidmatan pemprosesan penerimaannya. Model ini tidak berasaskan pada resit yang anda muat naik.

**Di manakah ciri ini tersedia dan diproses?**

Pada masa ini, Amerika Syarikat disokong.

**Di manakah resit saya pergi?**

Kewangan akan menghubungi Perkhidmatan Kognitif untuk mengekstrak data medan. Perkhidmatan Kognitif akan menyimpan salinan resit anda untuk tempoh masa hingga 24 jam selepas pemprosesan berlaku. Selepas pemprosesan selesai, Perkhidmatan Kognitif akan mengalih keluar resit. Resit masih disimpan dalam Kewangan.

Untuk maklumat lanjut, lihat [Dayakan pemahaman resit dengan keupayaan baharu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
