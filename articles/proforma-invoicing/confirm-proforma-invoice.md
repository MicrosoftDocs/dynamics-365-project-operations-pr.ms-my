---
title: Sahkan invois berdasarkan projek proforma
description: Topik ini menyediakan maklumat tentang pengesahan invois berdasarkan projek proforma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867142"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Sahkan invois berdasarkan projek proforma

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Selepas invois proforma disahkan, status invois projek dikemas kini kepada **Disahkan**. Apabila invois disahkan, ia menjadi baca sahaja. Melangkah ke hadapan, invois hanya boleh dibetulkan jika terdapat sebarang pembetulan atau kredit yang dimulakan oleh pelanggan.

Jadual berikut menyenaraikan aktual yang dicipta oleh sistem. Aktual ini dicipta apabila operasi tertentu dilaksanakan pada draf invois projek sebelum disahkan.

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
Menginvoiskan retainer atau pendahuluan </p>
            </td>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan bagi jenis, <strong>Retainer</strong> dibuat untuk jumlah dalam pendahuluan atau retainer.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan dengan amaun negatif retainer atau pendahuluan yang akan digunakan untuk penyesuaian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Selepas disesuaikan sepenuhnya retainer atau pendahuluan pada invois.
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
Aktual jualan dibilkan untuk amaun pada invois ini.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Selepas disesuaikan separuh retainer atau pendahuluan pada invois.
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
Aktual jualan dibilkan untuk amaun pada invois ini.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan negatif untuk baki amaun retainer atau pendahuluan akan digunakan untuk penyesuaian pada invois akan datang.
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
Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan, dan aktual jualan dibilkan yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki jam dan amaun selepas menolak angka yang dibetulkan pada butiran baris invois yang diedit, pembalikan aktual jualan dan aktual jualan dibilkan yang setara.
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
Penginvoisan transaksi bahan tanpa sebarang edit pada invois draf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk kuantiti dan amaun pada kelulusan penggunaan bahan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual jualan dibilkan untuk kuantiti dan amaun pada kelulusan penggunaan bahan asal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Penginvoisan transaksi bahan yang telah diedit untuk mengurangkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk kuantiti dan amaun pada kelulusan masa asal.
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
Penginvoisan transaksi bahan yang telah diedit untuk meningkatkan kuantiti.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan jualan belum dibilkan untuk kuantiti dan amaun pada kelulusan penggunaan bahan asal.
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
