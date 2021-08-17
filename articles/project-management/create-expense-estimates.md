---
title: Anggaran kewangan untuk perbelanjaan pada projek
description: Topik ini memberikan maklumat mengenai mentakrifkan atau menganggarkan perbelanjaan berasaskan projek.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f4d42724af61aa241671e8dacacbe2be5a7d531f55c2025a89ff777ac41e9b67
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987852"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Anggaran kewangan untuk perbelanjaan pada projek
_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations membolehkan pengurus Projek untuk menentukan perbelanjaan berdasarkan projek bagi setiap projek atau tugas. Setiap item perbelanjaan boleh dikaitkan dengan tugas projek tertentu. Perbelanjaan dikategorikan kepada kategori perbelanjaan yang berbeza, yang ditakrifkan di peringkat organisasi. Penetapan harga dan kos bagi setiap kategori perbelanjaan ditakrifkan dalam senarai harga. 

Lengkapkan langkah berikut untuk melihat, menambah atau memadamkan perbelanjaan projek.

1. Pergi ke **Projek** dan pilih projek yang anda mahu usahakan.
2. Pilih tab **Anggaran Projek** dan lihat senarai perbelanjaan projek.
3. Pilih **Perbelanjaan Baharu** untuk menambahkan perbelanjaan. Atau pilih satu belanja untuk dipadamkan dan kemudian pilih **Padamkan Perbelanjaan**.

Jadual berikut menyediakan maklumat tentang medan pada **Baris Anggaran Perbelanjaan** pada Projek. 

| **Medan** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- |
| Tugas | Senaraikan tugas dalam projek. Ini termasuk ringkasan dan tugas nod daun. | Memilih tugas untuk baris anggaran perbelanjaan akan memberikan kesan kepada kos perbelanjaan yang dianggarkan dan jualan perbelanjaan yang dianggarkan untuk tugas. Jika medan ini dibiarkan kosong, anggaran perbelanjaan dijejaki dan diringkaskan hanya di peringkat projek. |
| Kategori | Senarai kategori transaksi yang mempunyai kategori perbelanjaan dipautkan dalam aplikasi. | Memilih kategori mendorong penetapan harga dan kos pada baris anggaran perbelanjaan. |
| Tarikh mula | Tarikh teramal yang perbelanjaan akan berlaku. | Tiada kesan hiliran untuk medan ini. |
| Kumpulan unit | Nilai lalai dalam medan ini diambil daripada kumpulan unit yang ditetapkan sebagai lalai pada kategori yang dipilih. Anda boleh mengemas kini medan ini untuk memilih kumpulan unit lain. | Tiada kesan hiliran untuk medan ini. |
| Unit | Nilai dalam medan ini lalai untuk unit lalai kategori yang dipilih. Anda boleh mengemas kini medan ini untuk memilih unit lain. | Menukar unit mengakibatkan harga unit dan kos lalai yang berbeza. |
| Kuantiti | Kuantiti perbelanjaan yang dianggarkan akan ditanggung. | Tiada kesan hiliran untuk medan ini. |
| Kos Unit | Kos gabungan kategori dan unit yang dipilih seperti yang ditetapkan dalam senarai harga kos yang berkenaan | Kos unit sentiasa ditunjukkan dalam mata wang kos projek. |
| Harga Unit | Kos gabungan kategori dan unit yang dipilih seperti yang disediakan dalam senarai harga jualan yang berkenaan. | Harga unit sentiasa ditunjukkan dalam mata wang jualan projek. |
| Jumlah Kos | Amaun kos yang dikira sebagai kuantiti \* kos unit.| Amaun kos sentiasa ditunjukkan dalam mata wang kos projek. |
| Jumlah Jualan | Amaun jualan yang dikira sebagai kuantiti \* harga unit. | Amaun jualan sentiasa ditunjukkan dalam mata wang jualan projek. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
