---
title: Mencipta pendahuluan ad hoc pada kontrak
description: Artikel ini memberikan maklumat tentang penciptaan pendahuluan pada kontrak seperti yang diperlukan.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e450a17990c6fc783ddffdb05e1ab5b9429a3c1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922187"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Mencipta pendahuluan ad hoc pada kontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Microsoft Dynamics 365 Project Operations menyokong senario penginvoisan yang melibatkan prapembayaran dan pendahuluan. Proses untuk menggunakan **Pendahuluan** dalam **Project Operations** adalah sama dengan kontrak **Retainer**. 

Lengkapkan langkah berikut kepada invois pelanggan untuk pendahuluan.

1. Pergi ke halaman **Kontrak Projek** dan kemudian pilih tab **Pendahulaun dan Retainer**.
2. Dalam subgrid yang menyenaraikan semua pendahuluan yang dicatatkan sebelum ini dan prapembayaran, pilih **+ Retainer kontrak Projek Baharu**. 

    Borang **Cipta pantas** dibuka untuk merekodkan bayaran prapembayaran atau pendahuluan.
    
3. Jadual di bawah senarai medan untuk merekodkan pendahuluan dan pertimbangan perlu diingati apabila anda mencipta yang baharu:

    | Medan | Penerangan | Kesan hiliran |
    | --- | --- | --- |
    | **Pelanggan Kontrak Projek** | Medan ini menunjukkan pelanggan dalam kontrak yang akan diinvois untuk pendahuluan ini. | Jika anda mempunyai berbilang pelanggan dalam kontrak dan jika anda mahu menginvois setiap daripada mereka untuk jumlah retainer atau pendahuluan tertentu, cipta pendahuluan untuk setiap pelanggan secara individu. |
    | **Perihalan** | Perihalan tujuan atau masa pendahuluan untuk membantu mengenalpasti pendahuluan ini. | Perihalan ini dipaparkan pada baris invois untuk pendahuluan ini. |
    | **Amaun** | Jumlah untuk prapembayaran atau pendahuluan. | Jumlah ini dipaparkan pada baris invois untuk pendahuluan ini. |
    | **Tarikh Invois** | Tarikh pendahuluan ini diinvoiskan kepada pelanggan. | Ini ialah tarikh untuk proses penciptaan invois automatik untuk mencipta baris invois untuk pendahuluan ini. |
    | **Status Invois** | Ini ialah tetapan pilihan yang menunjukkan sama ada pendahuluan ini ditambah kepada invois draf untuk pelanggan ini. Nilai kemungkinan adalah:</br>- **Tidak bersedia untuk diinvois**</br>- **Sedia untuk invois** | Apabila pendahuluan atau prapembayaran ditandakan sebagai **Bersedia untuk invois**, ia ditambah sebagai masa baris pada invois draf. Hanya pendahuluan invois penuh boleh digunakan untuk menyelaraskan dengan kos projek untuk tempoh invois yang akan datang. |

4. Pilih **Simpan dan tutup** pada dialog cipta pantas untuk merekod pendahuluan atau prapembayaran.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]