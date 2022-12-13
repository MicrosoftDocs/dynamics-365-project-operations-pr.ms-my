---
title: Butiran pengepala untuk sebut harga projek
description: Artikel ini memberikan maklumat mengenai maklumat dan tetapan yang berkaitan dan memberikan kesan kepada sebut harga projek. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 645fcd38aa8307c9f5cfd6772c843dee2cf9055c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824832"
---
# <a name="header-details-for-project-quotes"></a>Butiran pengepala untuk sebut harga projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan tentang maklumat yang berkaitan dengan sebut harga projek. Ini termasuk tetapan yang memberi kesan kepada semua baris sebut harga, dan maklumat mengenai sebut harga yang diringkaskan merentasi semua item baris untuk memacu KPI sebut harga projek.

Jadual berikut menyenaraikan medan maklumat ringkasan pada sebut harga projek yang unik kepada Dynamics 365 Project Operations atau mempunyai beberapa perubahan penting dalam tingkah laku daripada sebut harga Dynamics 365 Sales.

| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Jenis | Tab ringkasan (tersembunyi) | Medan set pilihan ini mengolah pilihan berikut:</br>- -Berasaskan kerja (tersedia hanya apabila Project Operations dipasang)</br>- Berasaskan item (tersedia hanya apabila Project Operations and Sales dipasang)</br>- Perkhidmatan berasaskan penyelenggaraan (tersedia apabila Dynamics 365 Field Service dipasang) | Apabila anda menggunakan aplikasi Operasi Projek, nilai medan ini ditetapkan secara automatik kepada **berdasarkan kerja**. Ini mengklasifikasikan sebut harga sebagai sebut harga berasaskan projek. Sebut harga sepatutnya berasaskan projek untuk mendayakan semua sambungan dan fungsi khusus projek. |
| Pelanggan Berpotensi | Tab ringkasan | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. | Mata wang pada sebut harga projek telah dilalaikan berdasarkan mata wang pelanggan. Walau bagaimana pun, ini boleh diubah sebelum sebut harga disimpan. |
| Pengurus Akaun | Tab ringkasan | Nama pengurus akaun untuk urusan ini. Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. | Pengurus akaun bertanggungjawab untuk menguruskan perhubungan dengan pelanggan melalui pelengkapan projek ini. Berdasarkan rekod sumber boleh ditempah yang terikat dengan Pengurus Akaun, unit kontrak lalai pada sebut harga projek. |
| Unit Pengkontrakan | Tab ringkasan | Unit organisasi yang bertanggungjawab untuk menyiapkan projek atau projek yang berkaitan dengan sebut harga ini. Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. | Unit kontrak adalah bahagian syarikat yang akan melaksanakan projek selepas urusan ditutup. Setiap unit kontrak mempunyai mata wang dan mata wang ini digunakan untuk melaporkan anggaran dan kos sebenar yang ditanggung semasa pelaksanaan projek. |
| Senarai harga produk | Tab ringkasan | Ini ialah senarai harga yang digunakan untuk harga lalai pada baris sebut harga berasaskan produk. Senarai pilihan untuk medan ini menunjukkan senarai harga yang mana senarai harga mata wang sepadan dengan mata wang pada sebut harga. Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. Medan pada peluang ini dilalaikan daripada rekod akaun tetapi boleh ditukar. | Apabila sebut harga dimenangi, nilai medan akan disalin ke kontrak projek yang dicipta. |
| Mata wang | Tab ringkasan | Ini menunjukkan mata wang yang akan digunakan untuk melaporkan nilai bagi urusan ini. Ini juga merupakan mata wang yang pelanggan akan diinvois jika urusan itu dimenangi. Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. Medan pada peluang ini dilalaikan daripada rekod akaun tetapi boleh ditukar oleh pengguna. | Selepas sebut harga disimpan, medan ini tidak lagi boleh diedit. Ini digunakan untuk melalaikan senarai harga produk dan projek pada sebut harga. Mata wang pada sebut harga digunakan untuk dipadankan dengan mata wang pada senarai harga. |
| Had yang tidak boleh melebihi | Tab ringkasan | Ini menunjukkan had yang dirundingkan pada nilai terakhir yang pelanggan bersetuju untuk urusan ini. | Had ini dinilai semasa pelaksanaan dan diguna pakai merentasi semua item baris dan projek berkaitan dengan urusan ini. |
| Tarikh penghantaran yang diminta | Tab ringkasan | Apabila sebut harga dicipta daripada peluang, medan ini disalin daripada medan berkaitan dengan peluang. | Tarikh ini digunakan sebagai tarikh akhir untuk menjana jadual invois. |

Di bawah adalah tab dan KPI yang tersedia pada sebut harga projek yang unik untuk Operasi Projek atau mempunyai beberapa perubahan penting dalam tingkah laku daripada sebut harga jualan:

| **Medan** | **Lokasi** | **Perihalan** |
| --- | --- | --- |
| Analisis keuntungan | Tab pada Sebut Harga | Tan menunjukkan metrik berikut:</br>- Jumlah kos boleh dituntut</br></br>- Jumlah kos tidak boleh dituntut</br>- Jumlah hasil</br>- Jumlah hasil (asas)</br>- Margin kasar</br>- Margin kasar dilaraskan|
| Perbandingan untuk Jangkaan Pelanggan | Tab pada Sebut Harga | Tab ini menunjukkan metrik berikut:</br>- Anggaran selesai</br>- Pelengkapan Yang Diminta</br>- Belanjawan pelanggan</br>- Nilai sebut harga |
| Analisis sebut harga | Tab pada Sebut Harga | Tab ini meringkaskan KPI teratas berikut untuk sebut harga projek</br>- Perbandingan kepada pelanggan jangkaan belanjawan dan jadual</br>- Margin kasar</br>- Margin kasar dilaraskan |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
