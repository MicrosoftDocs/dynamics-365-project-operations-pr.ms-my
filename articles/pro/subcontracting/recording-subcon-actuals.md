---
title: Merekod masa, perbelanjaan dan penggunaan bahan untuk komponen yang disubkontrak
description: Artikel ini menjelaskan cara masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dijejak oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522525"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Merekod masa, perbelanjaan dan penggunaan bahan pada projek untuk komponen subkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini menjelaskan cara masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dijejak oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kos untuk masa subkontraktor pada projek
Dalam Project Operations, pekerja kontrak boleh merekodkan masa ke atas projek dengan cara yang sama sebagai pekerja. Apabila memasukkan masa pada projek dan/atau tugas projek, pekerja kontrak boleh memilih subkontrak khusus dan baris subkontrak.

Apabila masa yang diserahkan oleh pekerja kontrak diluluskan, kos projek direkodkan menggunakan kadar kos unit yang ditetapkan untuk sumber pekerja kontrak pada bahagian **Harga peranan** senarai harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kos perbelanjaan subkontrak pada projek
Apabila memasukkan perbelanjaan yang ditanggung atas projek, anda boleh memilih subkontrak dan baris subkontrak pada entri perbelanjaan. 

Apabila entri perbelanjaan ini diserahkan dan diluluskan, kos perbelanjaan direkodkan pada projek berdasarkan kos unit yang ditetapkan untuk kategori urus niaga tersebut dalam bahagian **Harga kategori** senarai harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kos bahan subkontrak pada projek
Apabila memasukkan penggunaan bahan yang ditanggung atas projek, anda boleh memilih subkontrak dan baris subkontrak pada log penggunaan bahan. Apabila log penggunaan bahan diserahkan dan diluluskan, kos bahan direkodkan pada projek berdasarkan kos unit yang ditetapkan untuk produk tersebut dalam bahagian **Item senarai harga** senarai harga subkontrak.

Penggunaan bahan juga boleh direkodkan untuk produk masukan manual pada projek. Jenis penggunaan bahan ini juga boleh dikaitkan dengan subkontrak dan baris subkontrak. Semasa merekodkan penggunaan bahan untuk produk masukan manual, anda perlu memasukkan kos seunit produk masukan manual. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
