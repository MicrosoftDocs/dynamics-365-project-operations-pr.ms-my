---
title: Menganggarkan baris sebut harga berdasarkan projek
description: Topik ini menyediakan maklumat tentang cara mencipta anggaran pada baris sebut harga berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273563"
---
# <a name="estimating-a-project-based-quote-line"></a>Menganggarkan baris sebut harga berdasarkan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Baris sebut harga berasaskan projek mempunyai butiran yang membantu menganggarkan kos dan potensi hasil kerja yang terlibat untuk menyampaikan baris sebut harga.

Untuk menganggarkan baris sebut harga berdasarkan projek, pada baris sebut harga berasaskan projek, pilih tab **Butiran Baris Sebut Harga**. Terdapat dua cara untuk mencipta anggaran pada baris sebut harga berasaskan projek:

- Buat secara manual anggaran secara langsung pada baris sebut harga menggunakan butiran baris sebut harga 
- Cipta projek dan pelan projek, dan kemudian kaitkan projek dan tugas pada projek ke baris sebut harga. Proses untuk mengimport anggaran ke atas pelan projek ke dalam garis sebut harga berdasarkan maklumat yang anda berikan akan didayakan.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Buat anggaran secara langsung pada baris sebut harga berasaskan projek

Untuk mencipta anggaran pada baris sebut harga berasaskan projek, pilih tab **Butiran Baris Sebut Harga**. Item baris yang anda cipta pada tab ini akan merumuskan nilai sebut harga untuk baris sebut harga ini. 

Untuk mencipta butiran baris sebut harga, pilih **+ Butiran baharu baris sebut harga** pada subgrid **Butiran Baris Sebut harga**. Gelangsar cipta pantas akan dibuka. Medan berikut pada borang **Baris Sebut Harga**:

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Penerangan  | Cipta cepat | Perihalan mengenai anggaran tertentu. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kelas Transaksi | Cipta cepat | Senarai juntai bawah ini menyediakan kelas transaksi yang dimasukkan pada tab **Umum** baris sebut harga berasaskan projek.  | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Peranan | Cipta cepat | Orang yang akan melaksanakan kerja ini atau menanggung perbelanjaan ini. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kategori | Cipta cepat | Kategori kerja atau perbelanjaan. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Tarikh Mula | Cipta cepat | Tarikh mula kerja. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Tarikh Tamat | Cipta cepat | Tarikh tamat kerja. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Unit Sumber | Cipta cepat | Unit sumber yang akan menanggung kos ini dan menyediakan sumber untuk mengusahakannya. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. Medan ini juga digunakan dalam mendapatkan kembali harga kos. |
| Jadual unit | Cipta cepat | Kumpulan unit kerja atau perbelanjaan. Unit yang tergolong dalam jadual seunit atau kumpulan unit. Contohnya, Batu dan KM ialah unit yang tergolong dalam kumpulan unit yang menggambarkan jarak. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Unit | Cipta cepat | Unit kerja atau perbelanjaan. | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Kuantiti | Cipta cepat | Kuantiti kerja atau perbelanjaan | Medan ini ingkar kepada butiran baris sebut harga yang berkaitan untuk kos yang dicipta secara automatik. |
| Harga unit | Cipta cepat | Kadar bil peranan yang menjalankan kerja atau harga Jualan kategori perbelanjaan. Medan ini lalai untuk masa berdasarkan kombinasi resourcing peranan dan unit pada senarai harga projek yang berkesan untuk tarikh mula. Untuk perbelanjaan, medan ini lalai daripada persediaan harga untuk kategori urus niaga dalam senarai harga projek yang berkesan untuk tarikh mula. Jika kaedah penetapan harga untuk kategori urus niaga tidak harga setiap unit, tidak ada lalai, medan ini dibiarkan kosong. | Kadar kos peranan yang melaksanakan kerja atau kos per unit kategori perbelanjaan. Medan ini lalai untuk Masa berdasarkan peranan dan sumber gabungan sumber pada harga unit Kontrak senarai harga Sebut Harga yang berkuat kuasa pada tarikh mula. Untuk perbelanjaan, bidang ini lalai dari penetapan harga untuk kategori urus niaga dalam senarai harga kos unit Kontrak yang berkuat kuasa pada tarikh mula. Jika kaedah penetapan harga untuk kategori transaksi bukan harga per unit, tidak ada default dan medan ini dibiarkan kosong. |
| Anggaran Cukai | Cipta cepat | Anda boleh memasukkan cukai anggaran secara manual untuk kerja atau perbelanjaan ini. | Tiada kesan hiliran bagi medan ini. |
| Amaun | Cipta cepat | Anda boleh memasukkan maklumat input secara manual ke medan ini jika medan **Kuantiti** dan **Harga** dibiarkan kosong. Jika medan ini tidak kosong, medan ini menjadi baca sahaja dan dikira sebagai (Kuantiti \* Harga unit) + Cukai. | Tiada kesan hiliran bagi medan ini. |

## <a name="update-prices-on-quote-line-details"></a>Kemas kini harga untuk butiran baris sebut harga

Jika anda telah mengubah harga pada senarai harga projek yang dilampirkan dengan sebut harga, atau pada senarai harga kos unit kontrak, anda boleh memilih **Mengira semula** pada halaman **Sebut harga**, untuk menyegarkan harganya pada butiran baris sebut harga individu untuk mencerminkan perubahan ini. Apabila anda memilih **Mengira semula**, amaran berlaku yang memberitahu anda bahawa harga pada butiran baris sebut harga untuk semua baris sebut harga pada sebut harga ini akan ditetapkan. Pilih **Ya**, untuk menyegarkan semula harga untuk jualan dan butiran baris sebut harga.

## <a name="access-quote-line-details-for-cost"></a>Akses butiran baris sebut harga untuk kos

Pada tab **Butiran baris sebut harga**, pilih baris dalam grid untuk mendayakan sesetengah tindakan pada bar alat subgrid. Tindakan pertama pada bar alat subgrid apabila butiran baris sebut harga dipilih adalah **Buka Butiran Kos**. Pilih **Buka Butiran Kos** untuk melihat kadar kos dan jumlah yang berkaitan untuk baris sebut harga ini.

> [!NOTE]
> Mengubah unit sumber, kuantiti, tarikh, peranan atau nilai kategori pada baris sebut harga butiran untuk kos akan mengubah nilai yang sesuai pada butiran baris sebut harga untuk jualan.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mata wang untuk butiran baris sebut harga kos dan jualan

Mata wang pada baris sebut harga butiran untuk jualan lalai dari senarai harga projek yang berkesan untuk tarikh mula butiran baris sebut harga.

Mata wang pada butiran baris sebut harga untuk kos lalai dari senarai harga unit kontrak sebut harga yang berkuat kuasa pada tarikh mula butiran sebut harga untuk kos.

Pengiraan keuntungan menukar jumlah pada butiran baris sebut harga untuk kos dan jualan ke asas mata wang persekitaran untuk melaporkan jumlah margin yang dianggarkan pada sebut harga tersebut.

Ini boleh menyebabkan ralat penggenapan mata wang dan berubah margin kerana kurangnya kadar pertukaran berkesan tarikh. Gunakan pengiraan ini pada sebut harga Projek hanya sebagai anggaran dan tidak benar statutori atau laporan lain yang memerlukan kejituan yang lebih tinggi pembundaran dan kesedaran tarikh berkuat kuasa untuk kadar pertukaran.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]