---
title: Urus tunggakan pengebilan
description: Artikel ini memberikan maklumat tentang cara melihat dan menyelesaikan tunggakan pengebilan dalam Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929389"
---
# <a name="manage-billing-backlog"></a>Urus tunggakan pengebilan

_ **Gunakan Pada:** Operasi Projek untuk senario berasaskan sumber/bukan stok

Dynamics 365 Project Operations mempunyai pandangan khusus untuk membantu menguruskan tunggakan pengebilan. Untuk menguruskan tunggakan pengebilan, pilih pautan dalam bahagian **Jualan**, di bawah **Pengebilan**. 

Pandangan berikut tersedia:

- Retainer dan Pendahuluan
- Retainer dan Pendahuluan Tersedia
- Pencapaian Penting Harga Tetap
- Tunggakan Pengebilan Masa dan Bahan

## <a name="retainers-and-advances"></a>Retainer dan Pendahuluan

Pandangan **Retainer dan Pendahuluan** menyenaraikan retainer dan pendahuluan merentasi semua kontrak projek. Selepas retainer atau pendahuluan diinvoiskan, jumlah pendahuluan akan tersedia untuk digunakan.

## <a name="available-retainers-and-advances"></a>Retainer dan Pendahuluan Tersedia

Pandangan **Retainer dan Pendahuluan Tersedia** menyenaraikan semua retainer dan pendahuluan tersedia merentasi semua kontrak projek. Selepas retainer atau pendahuluan diinvoiskan, jumlah pendahuluan akan tersedia untuk digunakan dan ditambah pada senarai. Selepas jumlah retainer atau pendahuluan digunakan sepenuhnya, ia akan dialih keluar daripada senarai.

## <a name="fixed-price-milestones"></a>Pencapaian Penting Harga Tetap

Pandangan **Pencapaian Harga Tetap** menyenaraikan semua pencapaian harga tetap merentasi semua baris kontrak projek. Daripada pandangan ini, pencapaian tunggal atau berbilang boleh ditandakan sebagai **Sedia untuk diinvois** atau **Tidak sedia untuk diinvois**. Menandakan pencapaian sebagai **Sedia untuk Diinvois** tersedia untuk diletakkan pada invois draf.

Apabila baris kontrak berbilang pelanggan mempunyai kaedah pengebilan harga tetap, pencapaian dicipta untuk setiap pelanggan pada baris kontrak. Pencapaian boleh dicipta kemudian dibahagikan kepada rekod pencapaian khusus pelanggan individu. Pecahan ini adalah dalaman dan selaras dengan pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan pada baris kontrak. Dalam pandangan **Pencapaian Harga Tetap**, anda akan melihat rekod pencapaian khusus pelanggan individu. Setiap rekod penting pencapaian ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini. Apabila satu atau lebih pecahan pencapaian yang berkaitan ditandakan sebagai **Sedia untuk Diinvois**, status pengepala akan dikemas kini kepada **Sedang berjalan** daripada **Belum Dimulakan**. Apabila semua pecahan pencapaian diinvois, status pencapaian pengepala akan dikemas kini kepada **Selesai**.

Pencapaian pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod dikemas kini kepada **Invois Pelanggan Disiarkan**. 

> [!NOTE] 
> Jangan kemas kini nilai status ini dengan menggunakan kod tersuai. Project Operations tidak berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.

## <a name="time-and-material-billing-backlog"></a>Tunggakan Pengebilan Masa dan Bahan

Pandangan **Tunggakan Pengebilan Masa dan Bahan** menyenaraikan semua aktual jualan yang tidak dibilkan pada semua kontrak projek dalam sistem yang belum diinvoiskan. Jualan sebenar belum dibilkan tunggal atau berbilang boleh ditandakan sebagai **Bersedia untuk Diinvois** atau **Tidak Bersedia untuk Diinvois** daripada pandangan ini. Menanda jualan sebenar belum dibilkan sebagai **Bersedia untuk Diinvois** menjadikan ia tersedia untuk dimasukkan pada invois draf.

Aktual jualan yang belum dibilkan dengan status **Tidak Melebihi** bagi **Gagal** tidak boleh ditandakan sebagai **Sedia untuk Diinvois**. Jika aktual perlu ditandakan sebagai **Sedia untuk Diinvois**, tetapkan semula status pada aktual lain pada baris kontrak yang terikat dan kemudian menilai semula status **Tidak Boleh Dilebihi**.

Jika baris kontrak berbilang pelanggan mempunyai kaedah pengebilan masa dan bahan, apabila masa dan perbelanjaan diluluskan, satu aktual jualan yang tidak dibilkan dicipta untuk setiap pelanggan pada baris kontrak mengikut pecahan peratusan pengebilan yang ditakrifkan untuk setiap pelanggan. Dalam pandangan **Tunggakan Pengebilan Masa dan Bahan**, anda akan melihat aktual jualan yang tidak dibilkan khusus pelanggan individu. Setiap rekod jualan sebenar belum dibilkan ini boleh ditandakan sebagai **Bersedia untuk Diinvois** secara berasingan daripada pandangan ini.

Aktual jualan belum dibilkan pada invois draf ditunjukkan dalam pandangan ini dengan status pengebilan **Invois Pelanggan Dicipta**. Apabila invois draf disahkan, status pengebilan pada rekod ini dikemas kini kepada **Invois Pelanggan Disiarkan**. 

> [!NOTE] 
> Jangan kemas kini nilai status ini dengan menggunakan kod tersuai. Project Operations tidak berfungsi dengan betul apabila nilai status ini dikemas kini dengan kod tersuai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
