---
title: Gambaran keseluruhan baris sebut harga projek
description: Topik ini menyediakan maklumat tentang menggunakan baris sebut harga projek untuk kerja projek.
author: rumant
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 07ee2e6a7823b25eacb1c7ad6180f8af571348bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587045"
---
# <a name="project-quote-lines-overview"></a>Gambaran keseluruhan baris sebut harga projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Baris sebut harga berasaskan projek direka untuk membantu menganggar kerja projek pada pembabitan. Struktur baris sebut harga berasaskan projek dilanjutkan untuk anggaran projek dengan konsep berikut:

- Kaedah Pengebilan
- Pemetaan Projek
- Termasuk kelas Transaksi
- Had yang tidak boleh Melebihi
- Persediaan boleh dikenakan caj
- Anggaran menggunakan Butiran Baris Sebut Harga
- Pelanggan baris Sebut Harga

Jadual berikut menyediakan maklumat mengenai medan pada tab **Umum** baris sebut harga berasaskan projek. Medan ini membantu menyediakan asas untuk anggaran terperinci dan dari bawah untuk kerja projek.

| **Medan** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- |
| Nama | Nama baris sebut harga yang sepatutnya boleh membantu anda mengenal pasti komponen tunggal sebut harga yang dianggarkan. | Disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Kaedah Pengebilan | Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan berkaitan dengan baris peluang. Medan ini merangkumi dua model kontrak utama yang disokong oleh Dynamics 365 Project Operations:</br>- Harga tetap</br>- Masa dan bahan.| Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Project | Gunakan medan pilihan ini untuk mengenal pasti projek yang akan digunakan untuk menyelesaikan kerja pada pembabitan ini. Apabila projek dipetakan kepada baris sebut harga, ia membantu dengan menyediakan tugas yang dikenakan caj dan juga dengan membawa anggaran berasaskan projek kepada baris sebut harga sebagai butiran baris sebut harga. Apabila projek tidak dipetakan kepada baris sebut harga berasaskan projek, anggaran perlu dicipta secara manual dengan mencipta setiap butiran baris sebut harga. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Termasuk Masa | Tanda **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh tidak akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Tidak** menunjukkan yang transaksi masa atau kos buruh akan dimasukkan dalam anggaran pada baris sebut harga ini. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Termasuk Perbelanjaan | Tanda **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Tidak** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Ya** menunjukkan yang kos perbelanjaan tidak akan dimasukkan dalam anggaran pada baris sebut harga ini. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Termasuk Yuran | Tanda **Ya**/**Tidak** menunjukkan jika bayaran pada projek terpilih akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Tidak** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini. Nilai **Ya** menunjukkan yang Bayaran tidak akan dimasukkan dalam anggaran pada baris sebut harga ini. | Nilai medan ini disalin kepada baris kontrak Projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Amaun Disebut Harga | Ini adalah jumlah yang akan disebutkan kepada pelanggan untuk semua kerja yang diramalkan pada garis sebut harga projek ini. Pada sebut harga dicipta daripada peluang, nilai ini disalin daripada medan **Bajet Pelanggan** pada baris peluang. Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris sebut harga. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Anggaran Cukai | Ini adalah medan boleh diedit untuk pengguna untuk menambah anggaran jumlah cukai pada baris sebut harga. Apabila baris sebut harga berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris sebut harga. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Jumlah Sebut Harga selepas Cukai | Medan ini adalah jumlah baris sebut harga selepas cukai dan baca sahaja. Jumlah dalam medan ini dikira sebagai *Jumlah Sebut Harga + Cukai*. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Had Tidak Boleh Dilebihi | Medan ini boleh diedit dan hanya tersedia pada baris sebut harga berasaskan projek yang mempunyai kaedah pengebilan **Masa dan Bahan**. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |
| Belanjawan Pelanggan | Medan ini boleh diedit dan disalin daripada medan berkaitan dengan baris peluang jika sebut harga dicipta daripada peluang. | Nilai medan ini disalin kepada baris kontrak projek yang dicipta daripada baris sebut harga ini apabila sebut harga dimenangi. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Peraturan pengesahan untuk medan pada tab Umum bagi baris sebut harga berasaskan projek

**Peraturan 1**: Kelas transaksi tertentu pada projek terpilih hanya boleh dimasukkan pada satu baris sebut harga berasaskan projek bagi sebut harga.

**Peraturan 2**: Jika peluang mempunyai berbilang sebut harga, boleh terdapat baris sebut harga daripada sebut harga berbeza yang semuanya merujuk kepada projek yang sama dan termasuk kelas transaksi yang sama.

**Peraturan 3**: Jika sebut harga tidak tergolong kepada peluang yang sama, ia tidak boleh termasuk projek dan kelas transaksi yang sama.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Peluang</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Sebut Harga</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Baris sebut harga</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Termasuk masa</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Termasuk perbelanjaan</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sertakan</strong>
                </p>
                <p>
                    <strong>bayaran</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Sah / Tidak sah</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Sebab</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #1. Masa, Perbelanjaan dan Bayaran pada projek P1 termasuk pada kedua-dua baris sebut harga QL1 dan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Tidak </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #1. Masa dan Bayaran pada projek P1 termasuk pada kedua-dua baris sebut harga QL1 dan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Tidak </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Masa dan bayaran pada projek P1 termasuk dalam QL1.
Perbelanjaan pada projek P1 termasuk dalam QL2.
Tiada pertindihan dalam sebarang yang dimasukkan pada setiap baris sebut harga, jadi ianya sah.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Tidak </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Tidak </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #1 di atas </p>
                <p>
Q1 termasuk Masa, Perbelanjaan dan Bayaran untuk seluruh projek P1.
                </p>
                <p>
QL2 termasuk Masa, Perbelanjaan dan Bayaran untuk seluruh projek P1 dan pertindihan dengan sebarang yang termasuk pada Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Berdasarkan Peraturan #2, Q1 dan Q2 adalah dua sebut harga pada peluang yang sama, jadi kedua-duanya boleh menganggar untuk komponen sama bagi projek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 pada Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Sah </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Berdasarkan Peraturan #3, Q1 dan Q2 adalah dua sebut harga pada peluang yang berbeza, jadi ia boleh menganggarkan untuk komponen sama bagi projek yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
S1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Tidak Sah </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
