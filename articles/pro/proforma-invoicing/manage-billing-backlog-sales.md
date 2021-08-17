---
title: Urus tunggakan pengebilan projek
description: Topik ini menyediakan maklumat tentang pelbagai pandangan yang tersedia untuk digunakan apabila menguruskan tunggakan pengebilan pada projek.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 27ef2ae90778394d15b979a13215c8f5af483cda0312682e9fc7256b8282b999
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988302"
---
# <a name="manage-project-billing-backlog"></a>Urus tunggakan pengebilan projek 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations mempunyai pandangan khusus untuk membantu menguruskan tunggakan pengebilan. Untuk menguruskan tunggakan pengebilan, pilih pautan dalam bahagian **Jualan**, di bawah **Pengebilan**. 

Pandangan berikut tersedia:

- Retainer dan Pendahuluan
- Retainer dan Pendahuluan Tersedia
- Pencapaian Penting Harga Tetap
- Tunggakan Pengebilan Produk
- Tunggakan Pengebilan Masa dan Bahan

## <a name="retainers-and-advances"></a>Retainer dan Pendahuluan

Pandangan **Retainer dan Pendahuluan** menyenaraikan semua retainer dan pendahuluan di semua kontrak projek dalam sistem. Selepas retainer atau pendahuluan diinvoiskan, jumlah pendahuluan akan tersedia untuk digunakan.

## <a name="available-retainers-and-advances"></a>Retainer dan Pendahuluan Tersedia

Pandangan **Retainer dan Pendahuluan yang Tersedia** menyenaraikan semua retainer dan pendahuluan yang tersedia di semua kontrak projek dalam sistem. Selepas retainer atau pendahuluan diinvoiskan, jumlah pendahuluan akan tersedia untuk digunakan dan ditambah pada senarai. Selepas jumlah retainer atau pendahuluan digunakan sepenuhnya, ia akan dialih keluar daripada senarai.

## <a name="fixed-price-milestones"></a>Pencapaian Penting Harga Tetap

Pandangan **Pencapaian Harga Tetap** menyenaraikan semua pencapaian harga tetap merentasi semua baris kontrak projek dalam sistem. Pencapaian tunggal atau berbilang boleh ditandakan sebagai **Sedia untuk Diinvois** atau **Tidak Sedia untuk Diinvois** daripada pandangan ini. Menandakan pencapaian sebagai **Sedia untuk Diinvois** tersedia untuk diletakkan pada invois draf.

Apabila baris kontrak berbilang pelanggan mempunyai kaedah pengebilan harga tetap, pencapaian dicipta untuk setiap pelanggan pada baris kontrak. Pencapaian boleh dicipta kemudian dibahagikan kepada rekod pencapaian khusus pelanggan individu. Pecahan ini adalah dalaman dan selaras dengan pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan pada baris kontrak. Dalam pandangan **Pencapaian Harga Tetap**, anda akan melihat rekod pencapaian khusus pelanggan individu. Setiap rekod penting pencapaian ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini. Apabila satu atau lebih daripada pecahan pencapaian yang berkaitan ditandakan sebagai **Sedia untuk Diinvois**, status pengepala dikemas kini kepada **Sedang Berjalan** daripada **Tidak Bermula**. Apabila semua pecahan pencapaian diinvoiskan, status pencapaian pengepala dikemas kini kepada **Selesai**.

Pencapaian pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod dikemas kini kepada **Invois Pelanggan Disiarkan**. Jangan kemas kini nilai status ini dengan menggunakan kod tersuai. Project Operations tidak berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.

## <a name="product-billing-backlog"></a>Tunggakan Pengebilan Produk

Pandangan **Tunggakan Pengebilan Produk** menyenaraikan semua baris kontrak berasaskan produk merentasi semua kontrak projek dalam sistem. Baris kontrak berasaskan produk yang tunggal atau berbilang boleh ditandakan sebagai **Sedia untuk Diinvois** atau **Tidak Sedia untuk Diinvois** daripada pandangan ini. Menandakan baris kontrak berasaskan produk sebagai **Sedia untuk Diinvois** menjadikan ia tersedia untuk diletakkan pada invois draf.

Baris kontrak berasaskan produk yang ada pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan yang Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod ini dikemas kini kepada **Invois Pelanggan Disiarkan**. Jangan kemas kini nilai status ini dengan menggunakan kod tersuai. Project Operations tidak berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.

## <a name="time-and-material-billing-backlog"></a>Tunggakan Pengebilan Masa dan Bahan

Pandangan **Tunggakan Pengebilan Masa dan Bahan** menyenaraikan semua aktual jualan yang tidak dibilkan pada semua kontrak projek dalam sistem yang belum diinvoiskan. Jualan sebenar belum dibilkan tunggal atau berbilang boleh ditandakan sebagai **Bersedia untuk Diinvois** atau **Tidak Bersedia untuk Diinvois** daripada pandangan ini. Menanda jualan sebenar belum dibilkan sebagai **Bersedia untuk Diinvois** menjadikan ia tersedia untuk dimasukkan pada invois draf.

Aktual jualan yang belum dibilkan dengan status **Tidak Melebihi** bagi **Gagal** tidak boleh ditandakan sebagai **Sedia untuk Diinvois**. Jika aktual perlu ditandakan sebagai **Sedia untuk Diinvois**, tetapkan semula status pada aktual lain pada baris kontrak yang dilakukan. dan kemudian nilai semula status **Tidak Melebihi**.

Jika baris kontrak berbilang pelanggan mempunyai kaedah pengebilan masa dan bahan, apabila masa dan perbelanjaan diluluskan, satu aktual jualan yang tidak dibilkan dicipta untuk setiap pelanggan pada baris kontrak mengikut pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan. Dalam pandangan **Tunggakan Pengebilan Masa dan Bahan**, anda akan melihat aktual jualan yang tidak dibilkan khusus pelanggan individu. Setiap rekod jualan sebenar belum dibilkan ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini.

Aktual jualan yang tidak dibilkan yang ada pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod ini dikemas kini kepada **Invois Pelanggan Disiarkan**. Jangan kemas kini nilai status ini menggunakan kod tersuai. Project Operations tidak berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
