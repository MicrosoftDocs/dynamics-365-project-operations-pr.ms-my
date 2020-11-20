---
title: Mencipta pendahuluan ad hoc dalam kontrak - ringan
description: Topik ini memberikan maklumat tentang mewujudkan pendahuluan pada kontrak yang diperlukan.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181373"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Mencipta pendahuluan ad hoc dalam kontrak - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Microsoft Dynamics 365 Project Operations menyokong senario penginvoisan yang melibatkan prapembayaran dan pendahuluan. Proses untuk menggunakan **Pendahuluan** dalam **Project Operations** adalah sama dengan kontrak **Retainer**. 

Lengkapkan langkah berikut kepada invois pelanggan untuk pendahuluan.

1. Pergi ke halaman **Kontrak Projek** dan kemudian pilih tab **Pendahulaun dan Retainer**.
2. Dalam subgrid yang menyenaraikan semua pendahuluan yang dicatatkan sebelum ini dan prapembayaran, pilih **+ Retainer kontrak Projek Baharu**. 

    Borang **Cipta pantas** dibuka untuk merekodkan bayaran prapembayaran atau pendahuluan.
    
3. Jadual di bawah senarai medan untuk merekodkan pendahuluan dan pertimbangan perlu diingati apabila anda mencipta yang baharu:

    | Medan | Penerangan  | Kesan hiliran |
    | --- | --- | --- |
    | **Pelanggan Kontrak Projek** | Medan ini menunjukkan pelanggan dalam kontrak yang akan diinvois untuk pendahuluan ini. | Jika anda mempunyai berbilang pelanggan dalam kontrak dan jika anda mahu menginvois setiap daripada mereka untuk jumlah retainer atau pendahuluan tertentu, cipta pendahuluan untuk setiap pelanggan secara individu. |
    | **Perihalan** | Perihalan tujuan atau masa pendahuluan untuk membantu mengenalpasti pendahuluan ini. | Perihalan ini dipaparkan pada baris invois untuk pendahuluan ini. |
    | **Amaun** | Jumlah untuk prapembayaran atau pendahuluan. | Jumlah ini dipaparkan pada baris invois untuk pendahuluan ini. |
    | **Tarikh Invois** | Tarikh pendahuluan ini diinvoiskan kepada pelanggan. | Ini ialah tarikh untuk proses penciptaan invois automatik untuk mencipta baris invois untuk pendahuluan ini. |
    | **Status Invois** | Ini ialah tetapan pilihan yang menunjukkan sama ada pendahuluan ini ditambah kepada invois draf untuk pelanggan ini. Nilai kemungkinan adalah:</br>- **Tidak bersedia untuk diinvois**</br>- **Sedia untuk invois** | Apabila pendahuluan atau prapembayaran ditandakan sebagai **Bersedia untuk invois**, ia ditambah sebagai masa baris pada invois draf. Hanya pendahuluan invois penuh boleh digunakan untuk menyelaraskan dengan kos projek untuk tempoh invois yang akan datang. |

4. Pilih **Simpan dan tutup** pada dialog cipta pantas untuk merekod pendahuluan atau prapembayaran.
