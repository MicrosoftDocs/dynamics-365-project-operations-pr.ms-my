---
title: Konfigurasi komponen boleh dituntut bagi baris kontrak berdasarkan projek - ringan
description: Topik ini memberikan maklumat tentang cara untuk menambah komponen boleh dituntut kepada baris kontrak dalam Operasi Projek.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 46429c94ca9aa1ebbbe9fc689a9a5bd6c52dc59e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177162"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurasi komponen boleh dituntut bagi baris kontrak berdasarkan projek - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Baris kontrak berasaskan projek mempunyai komponen *disertakan* dan komponen *boleh dituntut*.

Komponen yang disertakan ialah komponen yang tertakluk kepada:

  - Kaedah pengebilan dan pecahan pelanggan
  - Had yang tidak melebihi 
  - Tetapan kekerapan invois ditakrifkan pada baris kontrak berasaskan projek

Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**. Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris kontrak:

  - Boleh dituntut
  - Tidak boleh dituntut

Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.

Boleh dituntut ditakrifkan pada tugas untuk baris kontrak projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian. Jika medan **Tugas Termasuk** pada baris kontrak adalah kosong atau ditetapkan kepada **Seluruh projek**, tab **Tugas boleh dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada peranan untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Masa**. Jika medan **Sertakan Masa** pada baris kontrak ditetapkan kepada **Tidak**, tab **Peranan boleh dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada kategori transaksi untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Perbelanjaan**. Jika medan **Sertakan Perbelanjaan** ditetapkan kepada **Tidak**, tab **Kategori boleh dituntut** tidak akan tersedia.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Kemas kini tugas projek sebagai boleh dituntut atau tidak boleh dituntut

Satu tugas projek boleh dituntut atau tidak boleh dituntut pada baris kontrak khusus yang membuat persediaan yang mungkin berikut:

Jika baris kontrak berasaskan projek termasuk **Masa** dan tugas tertentu, **T1** dikaitkan dengannya sebagai boleh dituntut. Jika terdapat baris kontrak kedua yang termasuk **Perbelanjaan**, anda boleh mengaitkan tugas T1 pada baris kontrak sebagai tidak boleh dituntut. Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan tidak boleh dituntut.

Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada tugas baris kontrak sub. Sebagai alternatif, anda boleh mengemas kini medan **Jenis Pengebilan** pada sub persediaan Pengebilan tugas bagi projek yang menunjukkan baris kontrak yang berkaitan dengan tugas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Kemas kini peranan sebagai boleh dituntut atau tidak boleh dituntut

Peranan boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.

Jenis pengebilan peranan boleh dikonfigurasikan pada tab **Peranan Boleh Dituntut** bagi baris kontrak. Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi sebagai boleh dituntut atau tidak boleh dituntut

Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.

Jenis pengebilan transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** bagi baris kontrak berasaskan projek. Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.

### <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan

Anggaran atau yang dicipta sebenar untuk masa hanya akan dianggap boleh dituntut jika **Masa** dimasukkan dalam baris kontrak, dan jika **Tugas** dan **Peranan** dikonfigurasikan sebagai boleh dituntut ke atas baris kontrak.

Anggaran atau yang dicipta sebenar untuk perbelajaan hanya akan dianggap boleh dituntut jika **Perbelanjaan** dimasukkan dalam baris kontrak dan jika kategori **Tugas** dan **Transaksi** dikonfigurasikan sebagai boleh dituntut ke atas baris kontrak.


| Termasuk Masa | Termasuk Perbelanjaan | Termasuk Tugas | Peranan           | Kategori       | Tugas                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ya           | Ya              | Keseluruhan projek | Boleh dituntut     | Boleh dituntut     | Pengebilan pada Masa sebenar: **Boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar: **Boleh dituntut**           |
| Ya           | Ya              | Tugas terpilih | Boleh dituntut     | Boleh dituntut     | Pengebilan pada Masa sebenar: **Boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar: **Boleh dituntut**           |
| Ya           | Ya              | Tugas terpilih | Tidak boleh dituntut | Boleh dituntut     | Pengebilan pada Masa sebenar: **Tidak boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar: **Boleh dituntut**       |
| Ya           | Ya              | Tugas terpilih | Boleh dituntut     | Boleh dituntut     | Pengebilan pada Masa sebenar: **Tidak boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar:   **Tidak boleh dituntut** |
| Ya           | Ya              | Tugas terpilih | Tidak boleh dituntut | Boleh dituntut     | Pengebilan pada Masa sebenar: **Tidak boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar:   **Tidak boleh dituntut** |
| Ya           | Ya              | Tugas terpilih | Tidak boleh dituntut | Tidak boleh dituntut | Pengebilan pada Masa sebenar: **Tidak boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar:   **Tidak boleh dituntut** |
| Tidak            | Ya              | Keseluruhan projek | Tidak boleh ditetapkan   | Boleh dituntut     | Pengebilan pada Masa sebenar: **Tidak tersedia**</br>Jenis pengebilan pada Perbelanjaan sebenar: **Boleh dituntut**          |
| Tidak            | Ya              | Keseluruhan projek | Tidak boleh ditetapkan   | Tidak boleh dituntut | Pengebilan pada Masa sebenar: **Tidak tersedia**</br> Jenis pengebilan pada Perbelanjaan sebenar: **Tidak boleh dituntut**     |
| Ya           | Tidak               | Keseluruhan projek | Boleh dituntut     | Tidak boleh ditetapkan   | Pengebilan pada Masa sebenar: **Boleh dituntut** </br> Jenis pengebilan pada Perbelanjaan sebenar: **Tidak tersedia**        |
| Ya           | Tidak               | Keseluruhan projek | Tidak boleh dituntut | Tidak boleh ditetapkan   | Pengebilan pada Masa sebenar: **Tidak boleh dituntut** </br>Jenis pengebilan pada Perbelanjaan sebenar: **Tidak   tersedia**   |
