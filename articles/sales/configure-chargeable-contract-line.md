---
title: Konfigurasikan komponen boleh dicaj bagi baris kontrak projek
description: Topik ini menyediakan maklumat tentang komponen termasuk, boleh dituntut dan tidak boleh dituntut pada baris kontrak.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858349"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurasikan komponen boleh dicaj bagi baris kontrak projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Baris kontrak berasaskan projek mempunyai konsep komponen termasuk, boleh dituntut dan tidak boleh dituntut.

Komponen yang termasuk adalah tertakluk kepada kaedah pengebilan, pecahan pelanggan, had tidak melebihi dan tetapan kekerapan invois yang ditakrifkan pada baris kontrak berasaskan projek.

Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut mengemas kini medan **Jenis Pengebilan**.

Komponen boleh dituntut boleh ditakrifkan berdasarkan peranan dan kategori transaksi.

Untuk baris kontrak projek, boleh dituntut yang ditakrifkan berdasarkan peranan hanya dikenakan kepada kelas transaksi **Masa**. Jika **Termasuk Masa** ditetapkan kepada **Tidak** pada baris kontrak projek, tab **Peranan boleh dituntut** tidak tersedia.

Boleh dituntut ditakrifkan pada kategori transaksi untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Perbelanjaan**. Jika **Termasuk Perbelanjaan** ditetapkan kepada **Tidak** pada baris kontrak projek, tab **Kategori Boleh Dituntut** tidak tersedia.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Kemas kini peranan menjadi boleh dituntut atau tidak boleh dituntut

Peranan boleh dituntut atau tidak boleh dituntut berdasarkan baris kontrak berasaskan projek khusus.

Pada tab **Peranan Boleh Dituntut** baris kontrak berdasarkan projek, pada subgrid **Kategori Boleh Dituntut** dalam medan **Jenis Pengebilan**, kemas kini jenis pengebilan untuk peranan.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi menjadi boleh dituntut atau tidak boleh dituntut

Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut berdasarkan baris kontrak berasaskan projek khusus.

Pada tab **Kategori Boleh Dituntut** baris kontrak berdasarkan projek, pada subgrid **Kategori Boleh Dituntut** dalam medan **Jenis Pengebilan**, kemas kini jenis pengebilan untuk transaksi.

### <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan

Anggaran atau aktual dicipta untuk masa hanya akan dianggap boleh dituntut jika masa dimasukkan dalam baris kontrak, dan jika peranan dikonfigurasikan sebagai boleh dituntut pada baris kontrak.

Anggaran atau aktual yang dicipta untuk perbelajaan hanya akan dianggap boleh dituntut jika perbelanjaan dimasukkan dalam baris kontrak dan jika kategori transaksi dikonfigurasikan sebagai boleh dituntut pada baris kontrak.

| Termasuk masa | Termasuk perbelanjaan | Peranan | Kategori | Tugas |
| --- | --- | --- | --- | --- |
| Ya | Ya | Boleh dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Boleh dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tidak Boleh Dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tidak Boleh Dituntut | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Tidak | Ya | Tidak boleh ditetapkan | Boleh dituntut | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh Dituntut |
| Tidak | Ya | Tidak boleh ditetapkan | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Ya | Tidak | Boleh dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Boleh dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |
| Ya | Tidak | Tidak Boleh Dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br> Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
