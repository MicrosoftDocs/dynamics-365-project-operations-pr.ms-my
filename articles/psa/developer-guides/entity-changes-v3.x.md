---
title: Perubahan entiti, kawalan dan antara muka pengguna (Project Service Automation 3.x)
description: Topik ini menerangkan perubahan penyelesaian untuk Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148744"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Perubahan entiti, kawalan dan antara muka pengguna (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Dengan keluasan Microsoft Dynamics Project Service Automation (PSA) 3.x, banyak perubahan telah dibuat ke atas entiti, kawalan, tontonan dan antara muka pengguna. Topik ini memberikan maklumat tentang perubahan penting ini.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Hubungan induk-anak untuk dokumen jualan, baris dokumen jualan, entiti butiran baris dokumen jualan
Dalam versi Dynamics 365 Project Service Automation (PSA) yang dikeluarkan sebelum versi 3.0, sesetengah hubungan antara dokumen jualan, baris dokumen jualan, dan entiti butiran baris dokumen jualan dilaksanakan melalui medan rentetan yang akan memegang wakil GUID rentetan untuk entiti berkaitan. Ini disebabkan pengehadan platform yang memerlukan kod tersuai penting pada pihak pelayan dan klien penyelesaian untuk menjadikan hubungan tersebut berfungsi seperti hubungan entiti Dynamics CRM biasa dan menjadikan medan rentetan berfungsi seperti medan carian.

PSA 3.0 telah dikemas kini untuk memanfaatkan hubungan entiti baharu antara dokumen jualan dan entiti baris dokumen jualan.

Disebabkan medan carian kini boleh digunakan untuk menunjukkan rujukan kepada entiti, medan yang memegang nilai rentetan GUID bagi entiti berkaitan dalam versi sebelumnya tidak lagi diperlukan, dan oleh itu telah ditamatkan. Kod pihak klien dan pelayan tersuai yang mengendalikan hubungan tersebut ditakrifkan oleh medan rentetan legasi juga telah ditamatkan.

### <a name="entity-schema-changes"></a>Perubahan skema entiti
Jadual berikut memberikan senarai satu demi satu untuk medan rentetan yang ditamatkan dan medan carian baharu untuk entiti. 

 Entiti |   Medan ditamatkan (Rentetan) | Medan baharu (Carian)
--- | --- | ---
butiran invois (Baris Invois) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Aktual) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Jadual Invois Baris Kontrak Projek) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Pencapaian Baris Kontrak Projek) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fakta) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Butiran Baris Invois) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Baris Jurnal) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Kategori Sumber Baris Kontrak Projek) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Butiran Baris Kontrak Projek) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Kategori Transaksi Baris Kontrak Projek) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Klasifikasi Transaksi Baris Kontrak Projek) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Jadual Invois Baris Sebut Harga) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Kategori Sumber Baris Sebut Harga) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Pencapaian Baris Sebut Harga) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Butiran Baris Sebut Harga) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Kategori Transaksi Baris Sebut Harga) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Klasifikasi Transaksi Baris Sebut Harga) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Baris Pesanan) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Pandangan dan kawalan tersuai ditamatkan
Pandangan dan kawalan tersuai berikut dan artifak berkaitan ini telah ditamatkan.

- Pandangan boleh dikenakan caj.
- Kawalan grid tersuai untuk menunjukkan butiran baris sebut harga pada halaman **Maklumat Projek** untuk baris sebut harga.
- Kawalan grid tersuai untuk menunjukkan butiran baris kontrak projek pada halaman **Maklumat Projek** untuk baris pesanan jualan.

> [!NOTE]
> Untuk senarai penuh sumber ditamatkan, lihat [Sumber Web Ditamatkan dalam Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul Aplikasi Antara Muka Klien Disatukan
Dengan pengenalan Modul Aplikasi Antara Muka Klien Disatukan (UCI), entri peta tapak PSA telah dialih keluar daripada sistem.  
Kefungsian berkaitan dengan penukaran borang untuk Peluang, Sebut Harga, Pesanan, Invois telah ditamatkan kerana ia tidak lagi diperlukan memandangkan Modul Aplikasi UCI memasukkan hanya versi PSA untuk borang.  

Sumber web berikut telah ditamatkan:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Untuk senarai penuh sumber ditamatkan, lihat [Sumber Web Ditamatkan dalam Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]