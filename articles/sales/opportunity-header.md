---
title: Pengepala peluang/ringkasan
description: Topik ini memberikan maklumat tentang urus niaga berdasarkan projek dan baris peluang berdasarkan projek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908401"
---
# <a name="opportunity-headersummary"></a>Pengepala peluang/ringkasan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Pengepala peluang, atau ringkasan, merakam keseluruhan maklumat tentang urus niaga berdasarkan projek yang berkenaan dengan semua baris pada peluang berdasarkan projek.

Peluang berdasarkan projek dalam Dynamics 365 Project Operations ialah sambungan peluang dalam Dynamics 365 Sales. Sambungan ini memberikan kefungsian tambahan yang khusus kepada dan diperlukan untuk peluang berdasarkan projek. Sambungan ini boleh termasuk medan baharu dan tindakan reben yang tersedia dalam peluang berdasarkan projek. Anda boleh mendapatkan beberapa medan, kefungsian dan logik lalai yang tersedia dalam Sales yang tidak tersedia dalam Project Operations.

Jadual yang berikut mengandungi medan dalam peluang berdasarkan projek yang sama ada unik kepada Project Operations atau mempunyai beberapa perubahan penting dalam tingkah laku daripada Peluang dalam Sales.

| **Medan** | **Lokasi** | **Keterkaitan, tujuan dan panduan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Jenis | Tab umum (tersembunyi) | Medan set pilihan ini mempunyai pilihan berikut:</br>- Berdasarkan kerja (hanya tersedia dengan Project Operations)</br>- Berasaskan item (tersedia hanya apabila Project Operations and Sales dipasang)</br>- Berasaskan perkhidmatan penyelenggaraan (tersedia apabila Field Service dipasang) | Apabila anda menggunakan Project Operations, nilai medan ini ditetapkan kepada **Berdasarkan kerja** secara automatik yang mengklasifikasikan Peluang sebagai berdasarkan projek. Peluang seharusnya berdasarkan projek untuk mendayakan semua sambungan khusus projek dan kefungsian dalam proses jualan hiliran untuk urus niaga ini. |
| Syarikat Pemilikan | Tab umum | Ini ialah syarikat atau entiti undang-undang yang akan menyampaikan projek kepada pelanggan. | Maklumat medan ini akan disalin kepada medan yang sepadan pada sebut harga Projek yang dicipta daripada Peluang ini. |
| Orang Hubungan | Tab umum | Rujukan kepada kenalan utama pelanggan untuk urus niaga ini. | |
| Akaun | Tab umum | Rujukan kepada syarikat atau rekod akaun pelanggan. | |
| Pengurus Akaun | Tab umum | Nama Pengurus akaun untuk peluang berdasarkan projek ini. | Pengurus akaun bertanggungjawab untuk menguruskan perhubungan dengan pelanggan melalui pelengkapan projek ini. Berdasarkan sumber boleh ditempah yang terikat kepada Pengurus akaun, unit pengkontrakan dilalaikan. |
| Unit Pengkontrakan | Tab umum | Unit organisasi yang bertanggungjawab untuk penyampaian projek yang berkaitan dengan urus niaga ini. | Unit pengkontrakan ialah divisyen syarikat yang akan melengkapkan projek selepas urus niaga ditutup. Setiap unit pengkontrakan mempunyai mata wang dan mata wang ini digunakan untuk melaporkan kos anggaran dan sebenar yang berlaku semasa projek. |

Untuk semua medan dan bahagian lain pada tab **Ringkasan** peluang, lihat [Cipta atau edit peluang (Jualan dan Hab Jualan)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
