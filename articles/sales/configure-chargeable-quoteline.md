---
title: Konfigurasikan komponen boleh dituntut bagi baris sebut harga berdasarkan projek
description: Topik ini memberikan maklumat tentang komponen yang disertakan, boleh dituntut dan tidak boleh dituntut pada baris sebut harga berdasarkan projek.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642554"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurasikan komponen boleh dituntut bagi baris sebut harga berdasarkan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Baris sebut harga berdasarkan projek boleh mengandungi komponen dan komponen boleh dituntut.

Komponen yang disertakan adalah tertakluk pada kaedah pengebilan, pecahan pelanggan, had tidak boleh melebihi dan tetapan kekerapan invois yang ditakrifkan pada baris sebut harga berdasarkan projek.
Subset komponen yang disertakan boleh ditandakan sebagai boleh dituntut dengan menggunakan **Jenis Pengebilan**. Anda boleh memilih salah satu daripada pilihan berikut dalam medan **Jenis Pengebilan** dalam konteks baris sebut harga:

   - Boleh dituntut
   - Tidak boleh dituntut

Komponen boleh dituntut boleh ditakrifkan pada peranan dan kategori transaksi.

Kebolehtuntutan yang ditakrifkan pada peranan untuk baris sebut harga projek hanya diguna pakai untuk kelas transaksi **Masa**. Jika baris sebut harga projek mempunyai **Termasuk Masa** = **Tidak**, tab **Peranan Boleh Dituntut** tidak tersedia.

Kebolehtuntutan yang ditakrifkan pada kategori transaksi untuk baris sebut harga projek hanya diguna pakai untuk kelas transaksi **Perbelanjaan**. Jika baris sebut harga projek mempunyai **Termasuk Perbelanjaan** = **Tidak**, tab **Kategori Boleh Dituntut** tidak tersedia.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Kemas kini peranan menjadi boleh dituntut atau tidak boleh dituntut
Peranan boleh dituntut atau tidak boleh dituntut pada baris sebut harga berdasarkan projek. Jenis pengebilan pada peranan boleh dikonfigurasikan pada tab **Peranan Boleh Dituntut** bagi baris sebut harga berdasarkan projek. Untuk berbuat demikian, kemas kini **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi menjadi boleh dituntut atau tidak boleh dituntut
Kategori transaksi boleh dituntut atau tidak boleh dituntut pada baris sebut harga berdasarkan projek. Jenis pengebilan pada transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** bagi baris sebut harga berdasarkan projek. Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**. 

## <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan

Anggaran atau yang dicipta sebenar untuk masa hanya akan dianggap boleh dituntut jika masa dimasukkan pada baris sebut harga dan jika peranan dikonfigurasikan sebagai boleh dituntut.
Anggaran atau yang dicipta sebenar untuk perbelanjaan hanya akan dianggap boleh dituntut jika perbelanjaan dimasukkan pada baris sebut harga dan jika kategori transaksi dikonfigurasikan sebagai boleh dituntut pada baris sebut harga. Jadual berikut menunjukkan cara kebolehtuntutan lalai pada setiap yang sebenar. Lalai adalah berdasarkan komponen yang disertakan dan jenis pengebilan yang disediakan pada baris sebut harga.

| Termasuk masa | Termasuk perbelanjaan | Peranan | Kategori | Tugas |
| --- | --- | --- | --- | --- |
| Ya | Ya | Boleh dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Boleh dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tidak Boleh Dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tidak Boleh Dituntut | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Tidak | Ya | Tidak boleh ditetapkan | Boleh dituntut | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Tidak | Ya | Tidak boleh ditetapkan | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Ya | Tidak | Boleh dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Boleh dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |
| Ya | Tidak | Tidak Boleh Dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br> Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |
