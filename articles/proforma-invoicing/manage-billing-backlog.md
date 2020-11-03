---
title: Urus tunggakan pengebilan
description: Topik ini memberikan maklumat tentang cara untuk melihat dan bekerja dengan tunggakan pengebilan dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088029"
---
# <a name="manage-the-billing-backlog"></a>Urus tunggakan pengebilan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations mempunyai dua pandangan yang ditetapkan untuk membantu anda bekerja dan menguruskan tunggakan pengebilan. Mereka adalah **Pencapaian Harga Tetap** dan **Tunggakan Pengebilan Masa dan Bahan** Untuk memilih pandangan, dalam kawasan Project Operations **Jualan** , pada halaman navigasi sebelah kiri, pilih **Pengebilan**. Pautan tunggakan pengebilan disimpan di situ.

## <a name="fixed-price-milestones"></a>Pencapaian Penting Harga Tetap

Pandangan ini menyenaraikan semua pencapaian harga tetap merentasi semua baris kontrak projek dalam sistem. Pencapaian tunggal atau berbilang boleh ditandakan sebagai **Bersedia untuk Diinvois** atau **Tidak Bersedia untuk Diinvois** daripada pandangan ini. Apabila anda menandakan pencapaian sebagai **Bersedia untuk Diinvois** , pencapaian menjadi tersedia untuk invois draf.

Apabila baris kontrak berbilang pelanggan mempunyai kaedah pengebilan harga tetap, satu pencapaian dicipta untuk setiap pelanggan pada baris kontrak. Pengguna mencipta pencapaian dan pencapaian itu berpecah kepada pelanggan=rekod pencapaian khusus secara dalaman, mengikut pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan pada baris kontrak. Dalam pandangan **Pencapaian Harga Tetap** , anda akan melihat rekod pencapaian khusus pelanggan individu. Setiap rekod penting pencapaian ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini. Apabila satu atau lebih daripada pecahan pencapaian yang berkaitan ditandakan sebagai **Bersedia untuk Diinvois** , pengepala bergerak ke status **Sedang Berjalan** daripada **Belum Dimulakan**. Apabila semua pecahan pencapaian telah diinvois, status pencapaian pengepala menjadi **Selesai**.

Pencapaian pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod ini dikemas kini kepada **Invois Disiarkan**. Mengemas kini nilai status ini dengan menggunakan kod tersuai tidak disyorkan. Project Operations tidak akan berfungsi dengan betul jika nilai status ini dikemas kini dengan kod tersuai.

## <a name="time-and-material-billing-backlog"></a>Tunggakan Pengebilan Masa dan Bahan

Pandangan ini menyenaraikan semua jualan sebenar belum dibilkan yang belum diinvoiskan merentasi semua kontrak projek dalam sistem. Jualan sebenar belum dibilkan tunggal atau berbilang boleh ditandakan sebagai **Bersedia untuk Diinvois** atau **Tidak Bersedia untuk Diinvois** daripada pandangan ini. Menanda jualan sebenar belum dibilkan sebagai **Bersedia untuk Diinvois** menjadikan ia tersedia untuk dimasukkan pada invois draf.

Jualan sebenar belum dibilkan yang mempunyai **Tidak Boleh Dilebihi** status **Gagal** tidak boleh ditandakan sebagai **Bersedia untuk Diinvois**. Jika aktual ini perlu ditandakan dengan sedemikian, tetapkan semula status pada aktual lain pada baris kontrak yang telah dilaksanakan, dan kemudian menilai status **Tidak Boleh Dilebihi**.

Dalam kes baris kontrak berbilang pelanggan yang mempunyai kaedah pengebilan masa dan bahan, apabila masa dan perbelanjaan diluluskan, jualan sebenar belum dibilkan dicipta untuk setiap pelanggan pada baris kontrak mengikut pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan pada baris kontrak. Dalam pandangan **Tunggakan Pengebilan Masa dan Bahan** , anda akan melihat jualan sebenar belum dibilkan khusus pelanggan individu ini. Setiap rekod jualan sebenar belum dibilkan ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini.

Jualan sebenar belum dibilkan pada invois draf ditunjukkan dalam pandangan ini dengan **Status Pengebilan** daripada **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod ini dikemas kini kepada **Invois Pelanggan Disiarkan**. Mengemas kini nilai status ini apabila ia dalam keadaan ini dengan menggunakan kod tersuai tidak disyorkan. Project Operations tidak akan berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.
