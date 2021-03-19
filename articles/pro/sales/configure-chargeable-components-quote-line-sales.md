---
title: Konfigurasikan komponen boleh dikenakan bagi baris sebut harga - ringan
description: Topik ini menyediakan maklumat tentang menyediakan komponen boleh dituntut dan tidak boleh dituntut pada baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273884"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurasikan komponen boleh dikenakan bagi baris sebut harga - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris sebut harga berasaskan projek mempunyai konsep komponen *disertakan* dan komponen *boleh dituntut*.

Komponen yang disertakan adalah tertakluk kepada:

  - Kaedah pengebilan dan pecahan pelanggan
  - Had yang tidak melebihi 
  - Tetapan kekerapan invois ditakrifkan pada baris sebut harga berasaskan projek

Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**. Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris sebut harga:

  - Boleh dituntut
  - Tidak boleh dituntut

Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.

Boleh dituntut ditakrifkan pada tugas untuk baris sebut harga projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian tersebut. Jika medan **Sertakan Tugas** ditetapkan kepada **Seluruh projek** atau dibiarkan kosong, tab **Tugas Boleh Dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada peranan untuk baris sebut harga dan hanay terpakai untuk kelas transaksi **Masa**. Jika medan, **Sertakan Masa** ditetapkan kepada **Tidak** pada baris projek, tab **Peranan Boleh Dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada kategori transaksi untuk baris sebut harga dan hanya terpakai untuk kelas transaksi **Perbelanjaan**. Jika medan, **Sertakan Perbelanjaan** ditetapkan kepada **Tidak** pada baris projek, tab **Kategori Boleh Dituntut** tidak akan tersedia.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Kemas kini tugas projek untuk menjadi boleh dituntut atau tidak boleh dituntut

Satu tugas projek boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berasaskan projek khusus yang membuat persediaan yang mungkin berikut:

Jika baris sebut harga berasaskan projek termasuk **Masa** dan tugas **T1**, tugas itu dikaitkan dengan baris sebut harga sebagai boleh dituntut. Jika terdapat baris sebut harga kedua yang menyertakan **Perbelanjaan**, anda boleh mengaitkan tugas **T1** pada baris ssebut harga sebagai tidak boleh dituntut. Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan yang direkodkan pada tugas adalah tidak boleh dituntut.

Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Tugas Baris Sebut Harga**. Sebagai alternatif, anda boleh mengemas kini jenis pengebilan untuk tugas projek dalam medan **Jenis Pengebilan** pada subgrid pada penyediaan pengebilan tugas bagi projek yang menunjukkan baris sebut harga yang berkaitan dengan tugas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Kemas kini peranan menjadi boleh dituntut atau tidak boleh dituntut

Peranan boleh jadi boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berasaskan projek tertentu.

Jenis pengebilan tugas peranan boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi menjadi boleh dituntut atau tidak boleh dituntut

Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris sebut harga tertentu.

Jenis pengebilan tugas transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.

### <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan
Anggaran atau yang dicipta sebenar untuk masa hanya akan dianggap boleh dituntut jika **Masa** dimasukkan dalam baris sebut harga, dan jika **Tugas** dan **Peranan** dikonfigurasikan sebagai boleh dituntut ke atas baris sebut harga.

Anggaran atau yang dicipta sebenar untuk perbelanjaan hanya akan dianggap boleh dituntut jika **Perbelanjaan** dimasukkan dalam baris sebut harga dan jika **Tugas** dan **Kategori Transaksi** dikonfigurasikan sebagai boleh dituntut ke atas baris sebut harga.

| Termasuk Masa | Termasuk Perbelanjaan | Tugas yang Disertakan | Peranan | Kategori | Tugas | Pengebilan |
| --- | --- | --- | --- | --- | --- | --- |
| Ya | Ya | Keseluruhan projek | Boleh dituntut | Boleh dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Boleh dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tugas terpilih sahaja | Boleh dituntut | Boleh dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Boleh dituntut</br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tugas terpilih sahaja | Tidak boleh dituntut | Boleh dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut</br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Ya | Ya | Tugas terpilih sahaja | Boleh dituntut | Boleh dituntut | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut</br> Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Ya | Ya | Tugas terpilih sahaja | Tidak Boleh Dituntut | Boleh dituntut | Tidak Boleh Dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut</br> Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Ya | Ya | Tugas terpilih sahaja | Tidak Boleh Dituntut | Tidak Boleh Dituntut | Boleh dituntut | Pengebilan pada masa sebenar: Tidak Boleh Dituntut</br> Jenis pengebilan pada perbelanjaan sebenar: Tidak Boleh Dituntut |
| Tidak | Ya | Keseluruhan projek | Tidak boleh ditetapkan | Boleh dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut |
| Tidak | Ya | Keseluruhan projek | Tidak boleh ditetapkan | Tidak boleh dituntut | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Tidak tersedia </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak boleh dituntut |
| Ya | Tidak | Keseluruhan projek | Boleh dituntut | Tidak boleh ditetapkan | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Boleh dituntut</br>Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |
| Ya | Tidak | Keseluruhan projek | Tidak boleh dituntut | Tidak boleh ditetapkan | Tidak boleh ditetapkan | Pengebilan pada masa sebenar: Tidak Boleh Dituntut </br>Jenis pengebilan pada perbelanjaan sebenar: Tidak tersedia |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]