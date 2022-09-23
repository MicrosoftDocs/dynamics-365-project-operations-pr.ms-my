---
title: Merekod masa, perbelanjaan dan penggunaan bahan untuk komponen yang disubkontrak
description: Artikel ini menerangkan cara masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dikesan oleh Microsoft Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Merekodkan masa, perbelanjaan dan penggunaan bahan pada projek untuk komponen subkontrak

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini menerangkan cara masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dikesan oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kos untuk masa subkontraktor pada projek
Dalam Operasi Projek, pekerja kontrak boleh merekodkan masa pada projek dengan cara yang sama seperti pekerja. Apabila memasukkan masa pada projek dan/atau tugas projek, pekerja kontrak boleh memilih garis subkontrak dan subkontrak tertentu.

Apabila masa yang dikemukakan oleh pekerja kontrak diluluskan, kos projek direkodkan menggunakan kadar kos unit yang ditetapkan untuk sumber pekerja kontrak itu **di bahagian Harga** peranan senarai harga pembelian di subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kos untuk perbelanjaan subkontrak ke atas projek
Apabila memasuki perbelanjaan yang ditanggung pada projek, anda boleh memilih garis subkontrak dan subkontrak pada kemasukan perbelanjaan. 

Apabila kemasukan perbelanjaan ini dikemukakan dan diluluskan, kos perbelanjaan direkodkan pada projek berdasarkan kos unit yang ditetapkan untuk kategori transaksi tersebut **dalam bahagian Harga** Kategori senarai harga pembelian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kos untuk bahan subkontrak pada projek
Apabila memasukkan penggunaan bahan pada projek, anda boleh memilih garis subkontrak dan subkontrak pada log penggunaan bahan. Apabila log penggunaan bahan dikemukakan dan diluluskan, kos bahan direkodkan pada projek berdasarkan kos unit yang ditetapkan untuk produk tersebut **dalam bahagian Item** senarai harga senarai harga dalam senarai harga subkontrak.

Penggunaan bahan juga boleh direkodkan untuk produk tulis dalam projek. Penggunaan bahan jenis ini juga boleh dipautkan kepada garis subkontrak dan subkontrak. Apabila merakam penggunaan bahan untuk produk tulis, anda perlu memasukkan kos seunit produk tulis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
