---
title: Sahkan invois proforma
description: Topik ini memberikan maklumat tentang mengesahkan invois proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128114"
---
# <a name="confirm-a-proforma-invoice"></a>Sahkan invois proforma

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Selepas invois proforma disahkan, status invois projek dikemas kini kepada **Disahkan**. Apabila invois disahkan, ia menjadi baca sahaja. Melangkah ke hadapan, invois hanya boleh diperbetulkan jika terdapat sebarang pembetulan atau kredit yang yang dimulakan oleh pelanggan, atau apabila invois tersebut ditanda sebagai berbayar.

Jadual berikut menyenaraikan aktual yang dicipta oleh sistem. Aktual ini dicipta apabila operasi tertentu dilaksanakan pada draf invois projek sebelum disahkan.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Senario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Aktual dicipta pada pengesahan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menginvoiskan transaksi masa tanpa sebarang pengeditan pada invois draf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan untuk jam dan amaun pada kelulusan masa asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Menginvoiskan transaksi masa yang diedit untuk mengurangkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan belum dibilkan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki jam dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibilkan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menginvoiskan transaksi masa yang diedit untuk meningkatkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan belum dibilkan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menginvoiskan transaksi perbelanjaan tanpa sebarang pengeditan pada invois draf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Menginvoiskan transaksi perbelanjaan yang diedit untuk mengurangkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki kuantiti dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibilkan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menginvoiskan transaksi perbelanjaan yang diedit untuk meningkatkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menginvoiskan bayaran.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk amaun bayaran pada garisan jurnal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan bagi kuantiti dan amaun pada garisan jurnal bayaran sebenar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Menginvoiskan pencapaian.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan untuk amaun pencapaian pada pencapaian asal pada baris kontrak projek.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]