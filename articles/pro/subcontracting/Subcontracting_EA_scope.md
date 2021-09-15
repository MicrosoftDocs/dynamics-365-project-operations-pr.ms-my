---
title: Subkontrak dalam keluaran Capaian Awal Oktober 2021
description: Topik ini memberikan gambaran keseluruhan tentang keupayaan subkontrak dalam Project Operations yang merupakan sebahagian daripada keluaran capaian awal Oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383706"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Subkontrak dalam keluaran Capaian Awal Oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini memberikan gambaran keseluruhan tentang keupayaan subkontrak dalam Dynamics 365 Project Operations yang merupakan sebahagian daripada keluaran capaian awal Oktober 2021. Set ciri ini tidak sedia untuk pengeluaran atau persekitaran langsung, jadi ciri ini akan kekal dalam keluaran capaian awal sehingga set ciri penuh dikeluarkan. Kami amat menyarankan anda agar tidak menggunakan set ciri subkontrak untuk senario pengeluaran langsung sehingga sepanduk pratonton dialih keluar. 

Senarai berikut memberikan garis kasar tentang ciri yang kini tersedia dalam keluaran Capaian Awal Oktober 2021:

1. Pengurus projek mencipta subkontrak dengan vendor. Secara lalai, senarai harga yang dilampirkan pada rekod vendor digunakan untuk subkontrak. Akaun vendor mempunyai jenis hubungan **Vendor** atau **Pembekal**.

2. Pengurus projek boleh memperincikan semua pembelian sebagai item baris pada subkontrak. Baris subkontrak boleh untuk masa, perbelanjaan, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris.

3. Pengurus akaun vendor dan pengurus projek boleh melakukan pengulangan pada subkontrak. Penentuan harga boleh disesuaikan dalam senarai harga pembelian yang dilampirkan pada subkontrak.

4. Pada masa ini atau kemudian dalam proses ini, jika baris subkontrak adalah untuk masa, pengurus akaun vendor akan mengaitkan kenalan vendor dengan setiap baris subkontrak. Perkaitan ini memberikan maklumat kepada pengurus projek yang mengusahakan subkontrak tersebut. Apabila kenalan vendor dikaitkan dengan baris subkontrak, sistem akan mencipta sumber boleh ditempah daripada kenalan secara automatik, jika sumber boleh ditempah tidak wujud.

5. Kaedah pengebilan pada setiap baris subkontrak boleh **Harga Tetap** atau **Masa dan Bahan**. Untuk baris subkontrak harga tetap, jadual invois berasaskan pencapaian akan disediakan.

Langkah selebihnya dalam aliran proses perniagaan untuk subkontrak yang digariskan dalam Gambaran keseluruhan tidak tersedia pada masa ini. Oleh sebab fungsi baharu telah ditambah, topik ini akan dikemas kini. 

Ilustrasi berikut mewakili keluaran Capaian Awal Subkontrak berbanding dengan proses perniagaan hujung ke hujung.

![Aliran proses subkontrak](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Keluaran capaian awal baris subkontrak berasaskan kuantiti dan berasaskan kerja
Dalam keluaran Capaian Awal Oktober 2021, hanya baris subkontrak berasaskan kuantiti akan disokong. Ini bermakna bahawa baris subkontrak boleh digunakan untuk membeli masa, perbelanjaan, atau bahan daripada vendor tetapi bukan keseluruhan badan kerja. Ini juga bermaksud kuantiti yang dibeli (unit masa, perbelanjaan, atau kuantiti bahan) pada baris subkontrak boleh digunakan pada mana-mana projek dalam sistem.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
