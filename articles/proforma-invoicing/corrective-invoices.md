---
title: Pembetulan invois berdasarkan projek
description: Topik ini menyediakan maklumat tentang cara mencipta dan mengesahkan pembetulan invois berdasarkan projek dalam Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997167"
---
# <a name="corrective-project-based-invoices"></a>Pembetulan invois berdasarkan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Invois projek yang disahkan boleh dibetulkan untuk memproses perubahan atau kredit seperti yang dirundingkan dengan pelanggan dan pengurus projek.

Untuk mengedit invois yang disahkan, buka invois yang disahkan dan pilih **Betulkan Invois ini**. 

> [!NOTE]
> Pemilihan ini tidak tersedia melainkan invois projek disahkan atau invois berdasarkan projek mempunyai pendahuluan atau retainer atau penyesuaian pendahuluan atau retainer.

Invois draf baharu dicipta daripada invois yang disahkan. Semua butiran baris invois daripada invois yang disahkan sebelum ini disalin ke draf baharu. Berikut ialah beberapa perkara utama untuk memahami tentang butiran baris pada invois dibetulkan yang baharu:

- Semua kuantiti dikemas kini ke sifar. Dynamics 365 Project Operations menganggap bahawa semua item yang diinvois akan dikreditkan sepenuhnya. Jika perlu, anda boleh mengemas kini kuantiti ini secara manual untuk menunjukkan kuantiti yang diinvois dan bukan kuantiti yang dikreditkan. Berdasarkan pada kuantiti yang anda masukkan, aplikasi mengira kuantiti yang dikreditkan. Amaun ini ditunjukkan dalam aktual yang dicipta apabila invois dibetulkan disahkan. Jika anda membuat perubahan pada amaun cukai, anda mesti memasukkan jumlah cukai yang betul dan bukan jumlah cukai yang dikreditkan.
- Pembetulan pencapaian sentiasa diproses sebagai kredit penuh.


> [!IMPORTANT]
> Untuk butiran baris invois yang merupakan pembetulan kepada caj lain yang sudah diinvois, medan **Pembetulan** ditetapkan pada **Ya**. Untuk invois yang mempunyai butiran baris invois yang dibetulkan, medan **Memunyai pembetulan** ditetapkan pada **Ya**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Aktual dicipta apabila invois pembetulan disahkan

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
Penginvoisan kredit penuh transaksi bahan invois sebelum ini.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Penginvoisan kredit separa pada transaksi bahan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan dibilkan untuk kuantiti dan jumlah yang diinvois pada butiran baris invois asal untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan baharu belum dibilkan baharu yang boleh dicaj untuk kuantiti dan jumlah pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang setara.
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
Status invois pada pencapaian dikemas kini daripada <b>Invois Pelanggan yang Disiarkan</b> kepada <b>Sedia untuk Diinvois</b>.
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
Senario ini tidak disokong.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
