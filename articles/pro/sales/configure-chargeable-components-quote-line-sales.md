---
title: Konfigurasikan komponen boleh dituntut bagi baris sebut harga
description: Topik ini menyediakan maklumat tentang menyediakan komponen boleh dituntut dan tidak boleh dituntut pada baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858304"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfigurasikan komponen boleh dikenakan bagi baris sebut harga 

_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_

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

Tugas projek boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berdasarkan projek khusus, yang memungkinkan persediaan yang berikut:

Jika baris sebut harga berasaskan projek termasuk **Masa** dan tugas **T1**, tugas itu dikaitkan dengan baris sebut harga sebagai boleh dituntut. Jika terdapat baris sebut harga kedua yang menyertakan **Perbelanjaan**, anda boleh mengaitkan tugas **T1** pada baris ssebut harga sebagai tidak boleh dituntut. Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan yang direkodkan pada tugas adalah tidak boleh dituntut.

Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Tugas Baris Sebut Harga**. Sebagai alternatif, anda boleh mengemas kini jenis pengebilan untuk tugas projek dalam medan **Jenis Pengebilan** pada subgrid pada penyediaan pengebilan tugas bagi projek yang menunjukkan baris sebut harga yang berkaitan dengan tugas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Kemas kini peranan menjadi boleh dituntut atau tidak boleh dituntut

Peranan boleh jadi boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berasaskan projek tertentu.

Jenis pengebilan tugas peranan boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Kemas kini kategori transaksi menjadi boleh dituntut atau tidak boleh dituntut

Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris sebut harga tertentu.

Jenis pengebilan tugas transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.

### <a name="resolve-chargeability"></a>Menyelesaikan kebolehtuntutan
Anggaran atau aktual yang dicipta untuk masa akan hanya dianggap boleh dituntut jika:

   - **Masa** disertakan pada baris sebut harga.
   - **Peranan** dikonfigurasikan sebagai boleh dituntut pada baris sebut harga.
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga. 

Jika ketiga-tiga perkara ini benar, **Tugas** juga dikonfigurasikan sebagai boleh dituntut. 

Anggaran atau aktual yang dicipta untuk perbelanjaan hanya dianggap boleh dituntut jika: 

   - **Perbelanjaan** disertakan pada baris sebut harga.
   - **Kategori transaksi** dikonfigurasikan sebagai boleh dituntut pada baris sebut harga.
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga.

Jika ketiga-tiga perkara ini benar, **Tugas** juga dikonfigurasikan sebagai boleh dituntut. 

Anggaran atau aktual yang dicipta untuk bahan akan hanya dianggap boleh dituntut jika:

   - **Bahan** disertakan pada baris sebut harga.
   - **Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga.

Jika kedua-dua perkara ini benar, **Tugas** juga harus dikonfigurasikan sebagai boleh dituntut. 


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
                    <strong>Kesan kebolehtuntutan</strong>
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
Pengebilan pada masa sebenar: Boleh dituntut </p>
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
Boleh dituntut </p>
            </td>
            <td width="350" valign="top">
                <p>
Pengebilan pada masa sebenar: Boleh dituntut </p>
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
