---
title: Merekod masa, perbelanjaan dan penggunaan bahan untuk komponen yang disubkontrak
description: Artikel ini menerangkan bagaimana masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dijejaki oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927661"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Merakam masa, perbelanjaan, dan penggunaan bahan pada projek untuk komponen subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan bagaimana masa, perbelanjaan dan penggunaan bahan yang direkodkan pada projek daripada komponen subkontrak dijejaki oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kos untuk masa subkontraktor pada projek
Dalam Operasi Projek, pekerja kontrak boleh merekodkan masa pada projek dengan cara yang sama seperti pekerja. Apabila memasukkan masa pada projek dan/atau tugas projek, pekerja kontrak boleh memilih garis subkontrak dan subkontrak tertentu.

Apabila masa yang dikemukakan oleh pekerja kontrak diluluskan, kos projek direkodkan menggunakan kadar kos unit yang ditetapkan untuk sumber pekerja kontrak tersebut **di bahagian Harga** Peranan senarai harga belian pada subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kos untuk perbelanjaan subkontrak untuk projek
Apabila memasukkan perbelanjaan yang ditanggung untuk projek, anda boleh memilih garis subkontrak dan subkontrak pada kemasukan perbelanjaan. 

Apabila kemasukan perbelanjaan ini dikemukakan dan diluluskan, kos perbelanjaan direkodkan pada projek berdasarkan kos unit yang disediakan untuk kategori transaksi tersebut **dalam bahagian Harga** Kategori senarai harga belian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kos untuk bahan subkontrak pada projek
Apabila memasukkan penggunaan bahan pada projek, anda boleh memilih garis subkontrak dan subkontrak pada log penggunaan bahan. Apabila log penggunaan bahan dihantar dan diluluskan, kos bahan direkodkan pada projek berdasarkan kos unit yang disediakan untuk produk tersebut **dalam bahagian Item** senarai harga senarai Harga senarai harga subkontrak.

Penggunaan bahan juga boleh direkodkan untuk menulis-dalam produk pada projek. Penggunaan bahan jenis ini juga boleh dikaitkan dengan garis subkontrak dan subkontrak. Apabila merakam penggunaan bahan untuk produk tulis, anda perlu memasukkan kos per unit produk tulis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
