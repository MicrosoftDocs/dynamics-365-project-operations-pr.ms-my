---
title: Cipta invois berdasarkan projek pembetulan
description: Topik ini menyediakan maklumat tentang invois pembetulan dalam Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001634"
---
# <a name="create-corrective-project-based-invoices"></a>Cipta invois berdasarkan projek pembetulan 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Invois projek yang disahkan boleh dibetulkan untuk memproses perubahan atau kredit seperti yang dirundingkan dengan pelanggan dan pengurus projek.

Untuk mengedit invois yang disahkan, buka invois yang disahkan dan pilih **Betulkan Invois ini**. 

> [!NOTE]
> Pemilihan ini tidak tersedia kecuali invois projek disahkan.

Invois draf baharu dicipta daripada invois yang disahkan. Semua butiran baris invois daripada invois yang disahkan sebelum ini disalin ke draf baharu. Berikut ialah beberapa isi utama untuk membantu anda memahami lebih lanjut tentang butiran baris pada invois baharu yang dibetulkan:

- Semua kuantiti dikemas kini ke sifar. Ini menganggap bahawa semua item yang diinvois akan dikreditkan sepenuhnya. Jika perlu, anda boleh mengemas kini kuantiti ini secara manual untuk menunjukkan kuantiti yang diinvois dan bukan kuantiti yang dikreditkan. Berdasarkan pada kuantiti yang anda masukkan, aplikasi mengira kuantiti yang dikreditkan. Amaun ini ditunjukkan dalam aktual yang dicipta apabila invois dibetulkan disahkan. Jika anda membuat perubahan pada amaun cukai, anda mesti memasukkan jumlah cukai yang betul dan bukan jumlah cukai yang dikreditkan.
- Pembetulan pencapaian sentiasa diproses sebagai kredit penuh.
- Amaun retainer atau pendahuluan boleh dibetulkan jika pelanggan telah diinvoiskan dengan jumlah yang salah.
- Penyesuaian retainer dan pendahuluan boleh dibetulkan jika amaun yang salah digunakan untuk menyesuaikan terhadap caj ke atas invois yang disahkan sebelumnya.

> [!IMPORTANT]
> Butiran baris invois yang merupakan pembetulan kepada caj lain yang sudah diinvois mempunyai medan **Pembetulan** yang ditetapkan pada **Ya**. Invois yang mempunyai butiran baris invois dibetulkan mempunyai medan yang dipanggil **Mempunyai pembetulan** yang juga ditetapkan ke **Ya**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Aktual yang dicipta pada pengesahan invois pembetulan

Jadual berikut menyenaraikan aktual yang dicipta apabila invois pembetulan disahkan.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Senario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Aktual dicipta pada pengesahan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Sahkan pembetulan pendahuluan atau retainer diinvois.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian. Amaun ini adalah positif kerana ia bertujuan untuk membatalkan negatif yang dicipta apabila retainer atau pendahuluan diinvoiskan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual pembalikan jualan dibilkan dicipta untuk amaun pada retainer atau pendahuluan bagi membalikkan jualan dibilkan yang asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan baharu dicipta untuk amaun dibetulkan pada retainer atau baris invois dibetulkan berasaskan pendahuluan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan bagi amaun negatif retainer atau baris invois dibetulkan berasaskan pendahuluan yang akan digunakan untuk penyesuaian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Pengesahan pembetulan retainer atau pendahuluan sebelum ini yang disesuaikan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian. Amaun adalah positif dan bertujuan untuk membatalkan negatif yang dicipta apabila penyesuaian sebelum ini berlaku.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual pembalikan jualan dibilkan untuk amaun pada invois sebelum ini.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan baharu dicipta untuk amaun retainer dibetulkan yang digunakan pada invois dibetulkan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan dengan amaun negatif daripada retainer atau pendahuluan sisa dibetulkan yang akan digunakan untuk penyesuaian dalam invois kemudian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Penginvoisan kredit penuh bagi transaksi masa invois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk jam dan amaun pada butiran baris invois asal untuk masa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan baharu untuk jam dan amaun pada butiran baris invois asal untuk masa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Penginvoisan kredit separa pada transaksi masa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk jam dan amaun diinvoiskan pada butiran baris invois asal untuk masa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dicaj untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dicaj untuk baki jam dan amaun selepas menolak angka dibetulkan pada butiran baris invois.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Penginvoisan kredit penuh bagi transaksi perbelanjaan diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Penginvoisan kredit separa bagi transaksi perbelanjaan diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk perbelanjaan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois yang dibetulkan, pembalikan ini dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Penginvoisan kredit penuh bagi transaksi yuran diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Penginvoisan kredit separa bagi transaksi yuran diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk yuran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois pembetulan diedit, pembalikan ini dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Penginvoisan kredit penuh bagi pencapaian diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk amaun pada butiran baris invois asal untuk pencapaian.
                </p>
                <p>
Status invois pada pencapaian dikemas kini daripada <b>Invois pelanggan yang disiarkan</b> kepada <b>Sedia untuk Diinvois</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Penginvoisan kredit separa bagi pencapaian diinvois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tidak Disokong </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
