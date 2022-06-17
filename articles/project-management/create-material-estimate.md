---
title: Anggaran kewangan untuk bahan pada projek
description: Artikel ini memberikan maklumat mengenai menentukan atau menganggarkan bahan berasaskan projek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925713"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Anggaran kewangan untuk bahan pada projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations membolehkan pengurus Projek untuk menentukan kos bahan berdasarkan projek bagi setiap projek atau tugas. Setiap anggaran bahan boleh dikaitkan dengan tugas projek tertentu. Bahan yang digunakan pada projek boleh menjadi produk atau produk tulis dari katalog produk. Untuk setiap gabungan produk dan unit, harga boleh ditakrifkan dalam senarai harga projek untuk jualan dan senarai harga projek untuk kos.  

Lengkapkan langkah berikut untuk melihat, menambah atau memadamkan anggaran bahan projek.

1. Pergi ke **Projek** dan pilih projek yang anda mahu kemas kini.
2. Pada tab **Anggaran Bahan**, lihat senarai anggaran bahan projek.
3. Pilih **Anggaran Bahan Baharu** untuk mencipta anggaran bahan baharu. Atau, pilih anggaran bahan untuk memadamkan, dan kemudian pilih **Padamkan Anggaran Bahan**.

Jadual berikut menyediakan maklumat tentang medan pada **Baris Anggaran Bahan** pada Projek. 

| **Medan** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- |
| Tugas | Senaraikan tugas dalam projek. Ini termasuk ringkasan dan tugas nod daun. | Apabila anda memilih tugas untuk baris anggaran bahan, kos bahan yang dianggarkan dan jualan bahan yang dianggarkan untuk tugas terjejas. Jika medan ini kosong, anggaran bahan dijejaki dan diringkaskan hanya di peringkat projek. |
| Pilih Produk |  Anda boleh menentukan sama ada baris anggaran untuk produk (katalog) sedia ada atau masukan manual. | Medan ini menentukan jika anda memilih produk daripada produk katalog atau masukan manual. |
| Produk | ID produk daripada katalog produk. Apabila anda memilih ID produk, nilai dalam medan **Pilih Produk** dikemas kini secara automatik kepada **Produk sedia ada**. ID digunakan untuk mendapatkan kembali harga kos dan jualan daripada senarai harga. | Tiada kesan hiliran untuk medan ini. |
| Perihalan Produk Masukan Manual | Medan teks untuk masukan manual nama produk. Medan ini hendaklah digunakan apabila **Masukan Manual** dipilih dalam medan **Pilih Produk**.| Tiada kesan hiliran untuk medan ini. |
| Tarikh mula | Tarikh yang dijangkakan bagi bahan dijangka akan digunakan. | Tiada kesan hiliran untuk medan ini. |
| Kumpulan unit | Nilai lalai dalam medan ini diambil daripada kumpulan unit lalai pada produk katalog. Anda boleh mengemas kini medan ini untuk memilih kumpulan unit lain. | Tiada kesan hiliran untuk medan ini. |
| Unit | Nilai dalam medan ini diambil daripada unit lalai produk yang dipilih. Anda boleh mengemas kini medan ini untuk memilih unit lain. | Menukar unit mengakibatkan harga unit dan kos lalai yang berbeza. |
| Kuantiti | Kuantiti produk yang dianggarkan akan digunakan pada projek. | Tiada kesan hiliran untuk medan ini. |
| Kos Unit | Kos unit bagi gabungan produk dan unit yang dipilih seperti yang ditetapkan dalam senarai harga kos yang berkenaan. | Kos unit sentiasa ditunjukkan dalam mata wang kos projek. Jika tiada tetapan kos unit untuk gabungan persediaan produk dan unit dalam senarai harga, kos unit akan ditetapkan lalai kepada 0.00. |
| Harga Unit | Harga gabungan produk dan unit yang dipilih seperti yang ditetapkan dalam senarai harga jualan yang berkenaan. | Harga unit sentiasa ditunjukkan dalam mata wang jualan projek. Jika tiada persediaan harga unit untuk gabungan persediaan produk dan unit dalam senarai harga, maka harga unit akan ditetapkan lalai kepada 0.00.|
| Jumlah Kos | Amaun kos yang dikira sebagai kuantiti \* kos unit.| Amaun kos sentiasa ditunjukkan dalam mata wang kos projek. |
| Jumlah Jualan | Amaun jualan yang dikira sebagai kuantiti \* harga unit. | Amaun jualan sentiasa ditunjukkan dalam mata wang jualan projek. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
