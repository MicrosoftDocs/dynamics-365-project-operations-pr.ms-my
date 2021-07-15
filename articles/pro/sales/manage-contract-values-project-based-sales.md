---
title: Gambaran keseluruhan baris kontrak berdasarkan projek
description: Topik ini menyediakan maklumat tentang menggunakan baris kontrak berdasarkan projek.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369927"
---
# <a name="project-based-contract-lines-overview"></a>Gambaran keseluruhan baris kontrak berdasarkan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Baris kontrak berasaskan projek dalam Dynamics 365 Project Operations direka untuk memegang anggaran dan perjanjian pengebilan untuk komponen khusus kerja projek yang terlibat. Struktur baris kontrak berasaskan projek diperluaskan untuk anggaran projek dan senario pengebilan dengan konsep berikut:

- Kaedah pengebilan
- Pemetaan projek dan tugas
- Kelas transaksi yang disertakan
- Had yang tidak boleh melebihi
- Persediaan boleh dikenakan caj
- Anggaran menggunakan butiran baris kontrak
- Pelanggan baris kontrak

Jadual berikut termasuk medan pada tab **Jadual** untuk baris kontrak berasaskan projek yang membantu menyediakan asas bagi penhaturan pengebilan dan anggaran yang terperinci dan berasas untuk kerja berasaskan projek.

| Medan | Penerangan  | Kesan hiliran |
| --- | --- | --- |
| **Nama** | Nama baris kontrak. Ini mengenal pasti komponen berasingan untuk kontrak yang sedang dianggarkan. Untuk kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada nilai yang sepadan dengan baris sebut harga berasaskan projek. | Nama disalin kepada baris invois projek yang dicipta daripada baris kontrak ini apabila invois dicipta. |
| **Kaedah Pengebilan** | Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Ini ialah set pilihan yang mewakili dua model kontrak utama yang disokong oleh Project Operations:</br>- **Harga Tetap**</br>- **Masa dan Bahan** | Berdasarkan kaedah pengebilan bagi baris kontrak rujukan, transaksi sebenar akan diproses. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan masa dan material, rekod aktual kos dan jualan yang tidak dibilkan dicipta. Jika baris kontrak yang dirujuk oleh aktual mempunyai kaedah pengebilan harga tetap, hanya aktual kos dicipta. |
| **Project** | Gunakan medan ini untuk mengenal pasti projek yang akan digunakan untuk menyampaikan kerja pada penglibatan ini. | Nilai ini akan digunakan bersama **Tugas yang disertakan** dan **Kelas Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Tugas yang Disertakan** | Menunjukkan sama ada baris kontrak ini termasuk semua tugas projek untuk projek yang dipilih atau hanya subset tugas. Ia ialah set pilihan yang mempunyai nilai mungkin berikut:</br>- **Semua Tugas Projek**</br>- **Tugas Projek Terpilih Sahaja**. Nilai kosong dalam medan ini adalah sama dengan memilih **Semua Tugas Projek**. | Jika **Tugas yang Dipilih Sahaja** dipilih, anda boleh memilih tugas khusus dan dikaitkan kepada baris kontrak ini pada tab **Persediaan Pengebilan Tugas** pada halaman **Projek**. Nilai ini akan digunakan bersempena dengan **Projek** dan kelas **Transaksi yang Disertakan** untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Masa** | Nilai **Ya**/**Tidak** menunjukkan jika transaksi masa atau kos buruh pada projek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tiada** menunjukkan bahawa transaksi masa atau kos buruh tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Perbelanjaan** | Nilai **Ya**/**Tidak** menunjukkan jika kos perbelanjaan pada projek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tiada** menunjukkan bahawa kos perbelanjaan tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan. | Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Bahan** | Nilai **Ya**/**Tidak** menunjukkan jika kos bahan pada projek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahawa kos bahan tidak akan disertakan pada baris kontrak ini. Nilai **Ya** menunjukkan bahawa kos perbelanjaan akan dimasukkan. | Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Termasuk Yuran** | Nilai **Ya**/**Tidak** menunjukkan jika yuran bagi projek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tiada** menunjukkan bahawa yuran tidak akan dimasukkan ke dalam baris kontrak ini. Nilai **Ya** menunjukkan bahawa transaksi masa atau kos buruh akan dimasukkan. | Nilai ini digunakan bersama projek untuk menyelesaikan rujukan baris kontrak pada rekod baris aktual atau anggaran. |
| **Amaun Dikontrakkan** | Pada baris kontrak harga tetap, amaun ini yang dipersetujui yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada baris kontrak masa dan bahan, amaun ini ialah nilai anggaran yang akan diinvoiskan kepada pelanggan untuk semua komponen kerja yang berkaitan dengan baris kontrak ini. Pada kontrak projek yang dicipta daripada sebut harga, nilai ini akan disalin daripada medan yang sepadan pada baris sebut harga. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana amaun sebelum cukai pada pencapaian pengebilan berkala. |
| **Anggaran Cukai** | Pengguna boleh mengedit medan ini untuk memasukkan anggaran jumlah cukai pada baris kontrak. Apabila baris kontrak berasaskan projek mempunyai butiran baris, medan ini dikunci untuk pengeditan dan diringkaskan daripada jumlah cukai pada butiran baris kontrak. | Apabila baris kontrak mempunyai butiran baris, nilai ini boleh diubah suai dengan mengubah jumlah cukai pada butiran baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana cukai pada pencapaian pengebilan berkala. |
| **Amaun Kontrak selepas Cukai** | Amaun baris kontrak selepas cukai. Medan ini ialah baca sahaja dan dikira sebagai **Amaun Kontrak + Cukai**. | Pada baris kontrak harga tetap, nilai ini digunakan untuk menjana pencapaian pengebilan berkala. |
| **Had Tidak Boleh Dilebihi** | Pengguna boleh mengedit medan ini dan ia hanya tersedia untuk baris kontrak berdasarkan projek yang menetapkan kaedah pengebilan kepada masa dan bahan. | Pengguna boleh mengedit medan ini. Apabila aktual untuk masa dan bahan merujuk kepada baris kontrak ini untuk masa dan bahan, jumlah bagi aktual dinilai dengan had tidak melebihi pada baris kontrak ini selepas mengira jumlah yang sudah dibelanjakan dan dilakukan. Penilaian ini diselesaikan selepas amaun yang telah dibelanjakan dan dilakukan diambil kira. |
| **Belanjawan Pelanggan** | Medan ini boleh diedit dan disalin daripada medan sepadan pada baris sebut harga jika kontrak dicipta daripada sebut harga. | Medan ini hanya digunakan untuk maklumat dan tidak mempunyai sebarang kepentingan hiliran. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Peraturan pengesahan untuk pilihan pada tab Umum baris kontrak berasaskan projek

Peraturan 1: Jika medan **Tugas yang Disertakan** kosong atau ditetapkan kepada **Semua Tugas Projek**, semua tugas projek akan dimasukkan ke dalam baris kontrak.

Peraturan 2: Apabila medan **Tugas yang Disertakan** kosong atau secara jelas ditetapkan kepada **Semua Tugas Projek**, projek dan kelas transaksi tertentu hanya boleh dimasukkan ke dalam satu baris kontrak berasaskan projek kontrak.

Peraturan 3: Apabila medan **Tugas yang Disertakan** ditetapkan kepada **Tugas Projek Terpilih Sahaja**, projek dan kelas transaksi tertentu boleh dimasukkan ke dalam berbilang baris kontrak berasaskan projek kontrak.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrak</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Baris kontrak</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Tugas yang disertakan</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Termasuk Masa</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Termasuk Perbelanjaan</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Termasuk Bahan</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sertakan</strong>
                </p>
                <p>
                    <strong>Yuran</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Sah / Tidak sah</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Sebab</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #2. Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #2. Masa, Perbelanjaan, Bahan dan Yuran projek P1 akan disertakan pada kedua-dua Baris kontrak CL1 dan CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Sah </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Masa, Bahan dan Yuran projek P1 disertakan dalam CL1.
                </p>
                <ul>
                    <li>
Perbelanjaan pada projek P1 termasuk dalam CL2.
                    </li>
                </ul>
                <p>
Tiada pertindihan dalam nilai yang disertakan pada setiap Baris kontrak dan oleh itu sah.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Tidak </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tugas terpilih sahaja </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak sah </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran Peraturan #2 </p>
                <p>
C1 termasuk Masa, Bahan, Perbelanjaan dan Yuran pada subset tugas projek P1.
                </p>
                <p>
CL2 termasuk Masa, Bahan, Perbelanjaan dan Yuran untuk seluruh projek P1 dan oleh itu bertindih dengan nilai yang dimasukkan dalam C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tugas terpilih sahaja </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Sah </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Setiap Peraturan #3 </p>
                <p>
C1 termasuk Masa, Perbelanjaan, Bahan dan Yuran pada subset tugas projek P1.
                </p>
                <p>
CL2 termasuk Masa, Perbelanjaan, Bahan dan Yuran untuk subset tugas projek P1.
                </p>
                <p>
Satu-satunya pengesahan tambahan ialah sekitar subset tugas pada CL1 berbeza daripada subset tugas pada CL2 untuk memastikan bahawa tiada pertindihan. Ini dilakukan oleh sistem apabila tugas dikaitkan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tugas terpilih sahaja </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
