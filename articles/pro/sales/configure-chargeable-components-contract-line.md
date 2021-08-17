---
title: Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek
description: Topik ini memberikan maklumat tentang cara untuk menambah komponen boleh dituntut kepada baris kontrak dalam Operasi Projek.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003467"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek

_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_

Baris kontrak berasaskan projek mempunyai komponen *disertakan* dan komponen *boleh dituntut*.

Komponen yang disertakan ialah komponen yang tertakluk kepada:

  - Kaedah pengebilan dan pecahan pelanggan
  - Had yang tidak melebihi 
  - Tetapan kekerapan invois ditakrifkan pada baris kontrak berasaskan projek

Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**. Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris kontrak:

  - Boleh dituntut
  - Tidak boleh dituntut

Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.

Boleh dituntut ditakrifkan pada tugas untuk baris kontrak projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian. Jika medan **Tugas Termasuk** pada baris kontrak adalah kosong atau ditetapkan kepada **Keseluruhan projek**, tab **Tugas boleh dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada peranan untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Masa**. Jika medan **Sertakan Masa** pada baris kontrak ditetapkan kepada **Tidak**, tab **Peranan boleh dituntut** tidak akan tersedia.

Boleh dituntut ditakrifkan pada kategori transaksi untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Perbelanjaan**. Jika medan **Sertakan Perbelanjaan** ditetapkan kepada **Tidak**, tab **Kategori boleh dituntut** tidak akan tersedia.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Kemas kini tugas projek sebagai boleh dituntut atau tidak boleh dituntut

Tugas projek boleh dituntut atau tidak boleh dituntut pada baris kontrak khusus, yang memungkinkan persediaan yang berikut:

Jika baris kontrak berasaskan projek termasuk **Masa** dan tugas tertentu, **T1** dikaitkan dengannya sebagai boleh dituntut. Jika terdapat baris kontrak kedua yang termasuk **Perbelanjaan**, anda boleh mengaitkan tugas T1 pada baris kontrak sebagai tidak boleh dituntut. Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan tidak boleh dituntut.

Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada tugas baris kontrak sub. Sebagai alternatif, anda boleh mengemas kini medan **Jenis Pengebilan** pada sub persediaan Pengebilan tugas bagi projek yang menunjukkan baris kontrak yang berkaitan dengan tugas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Kemas kini peranan sebagai boleh dituntut atau tidak boleh dituntut

Peranan boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.

Jenis pengebilan peranan boleh dikonfigurasikan pada tab **Peranan Boleh Dituntut** bagi baris kontrak. Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi sebagai boleh dituntut atau tidak boleh dituntut

Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.

Jenis pengebilan transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** bagi baris kontrak berasaskan projek. Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.

### <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan

Anggaran atau aktual yang dicipta untuk masa hanya dianggap boleh dituntut jika:

   - **Masa** disertakan pada baris kontrak.
   - **Peranan** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak.
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang Dipilih** pada baris kontrak.
 
 Jika ketiga-tiga perkara ini benar, tugas itu dikonfigurasikan sebagai boleh dituntut. 

Anggaran atau aktual yang dicipta untuk perbelanjaan hanya dianggap boleh dituntut jika:

   - **Perbelanjaan** disertakan pada baris kontrak
   - **Kategori transaksi** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak
  
 Jika ketiga-tiga perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut. 

Anggaran atau aktual yang dicipta untuk bahan hanya dianggap boleh dituntut jika:

   - **Bahan** disertakan pada baris kontrak
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak

Jika kedua-dua perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Termasuk Masa</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Termasuk Perbelanjaan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Termasuk Bahan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tugas yang Disertakan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Peranan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tugas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Kesan Kebolehtuntutan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Tugas terpilih sahaja </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Tugas terpilih sahaja </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </p>
                <p>
Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Tugas terpilih sahaja </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: <strong>Boleh Dituntut</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Tugas terpilih sahaja </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: <strong> Tidak Boleh Dituntut</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Tugas terpilih sahaja </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak Boleh Dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Boleh dituntut</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </p>
                <p>
Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak boleh dituntut</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="70" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada masa sebenar: Boleh dituntut </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan: Boleh dituntut </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="70" valign="top">
                <p>
Boleh dituntut </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada masa sebenar: Boleh dituntut </p>
                <p>
Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut </p>
                <p>
Jenis pengebilan pada aktual bahan: <strong> Tidak tersedia</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Tidak</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan Projek </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Boleh Dituntut</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak boleh dituntut</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak boleh ditetapkan </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </p>
                <p>
Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak boleh dituntut </strong>
                </p>
                <p>
Jenis pengebilan pada aktual bahan:<strong> Tidak tersedia</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
