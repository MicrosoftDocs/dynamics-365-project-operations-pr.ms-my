---
title: Masa rakaman, perbelanjaan, dan penggunaan bahan untuk komponen subkontrak
description: Topik ini menerangkan bagaimana masa, perbelanjaan, dan penggunaan bahan yang direkodkan pada projek dari komponen subkontrak dijejaki oleh Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903733"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Masa rakaman, perbelanjaan, dan penggunaan bahan pada projek untuk komponen subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini menerangkan bagaimana masa, perbelanjaan, dan penggunaan bahan yang direkodkan pada projek dari komponen subkontrak dijejaki oleh Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kos untuk masa subkontraktor pada projek
Dalam Operasi Projek, pekerja kontrak boleh merakam masa projek dengan cara yang sama seperti pekerja. Apabila memasuki masa pada projek dan / atau tugas projek, pekerja kontrak boleh memilih garis subkontrak dan subkontrak tertentu.

Apabila masa yang dikemukakan oleh pekerja kontrak diluluskan, kos projek direkodkan menggunakan kadar kos unit yang ditetapkan untuk sumber pekerja kontrak tersebut di **bahagian Harga Peranan senarai harga pembelian di** subkontrak.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kos untuk perbelanjaan subkontrak pada projek
Apabila memasukkan perbelanjaan yang ditanggung ke atas projek, anda boleh memilih garis subkontrak dan subkontrak pada kemasukan perbelanjaan. 

Apabila kemasukan perbelanjaan ini dikemukakan dan diluluskan, kos perbelanjaan direkodkan pada projek berdasarkan kos unit yang ditetapkan untuk kategori transaksi tersebut di **bahagian Harga Kategori senarai harga** belian pada subkontrak.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kos untuk bahan subkontrak pada projek
Apabila memasukkan penggunaan bahan pada projek, anda boleh memilih garis subkontrak dan subkontrak pada log penggunaan bahan. Apabila log penggunaan bahan dikemukakan dan diluluskan, kos bahan direkodkan pada projek berdasarkan kos unit yang disediakan untuk produk tersebut dalam **bahagian Item senarai harga senarai harga** subkontrak.

Penggunaan bahan juga boleh direkodkan untuk produk bertulis pada projek. Jenis penggunaan bahan ini juga boleh dikaitkan dengan garis subkontrak dan subkontrak. Apabila merakam penggunaan bahan untuk produk penulisan, anda perlu memasukkan kos per unit produk tulis masuk. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
