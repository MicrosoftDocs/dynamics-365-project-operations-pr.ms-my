---
title: Gambaran keseluruhan proses penginvoisan
description: Artikel ini memberikan gambaran keseluruhan proses penginvoisan dalam Operasi Projek untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923107"
---
# <a name="invoicing-process-overview"></a>Gambaran keseluruhan proses penginvoisan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Project Operations untuk senario berdasarkan sumber/bukan stok menawarkan keupayaan yang komprehensif yang disesuaikan dengan keperluan pengurus Projek dan kerani Akaun belum terima/akauntan projek. Untuk proses penginvoisan, pengurus Projek menguruskan tunggakan pengebilan projek dan kerani Akaun belum terima/akauntan projek mencipta dokumen invois berdepan pelanggan yang patuh dan tepat.

![Rajah aliran penginvoisan.](./media/invoicing-flow.png)

Baris kontrak projek mentakrifkan kaedah pengebilan untuk transaksi projek berkaitan. Apabila pengurus Projek meluluskan transaksi masa dan perbelanjaan, sistem merekodkan transaksi dalam **entiti Project Actuals** dan menghantar maklumat kepada **modul pengurusan dan perakaunan** Projek dalam Dynamics 365 Finance. Akauntan Projek kemudiannya menyemak dan menyiarkan rekod menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Jurnal ini termasuk butiran perakaunan penting untuk aktual projek, seperti pengebilan, kumpulan cukai jualan, kumpulan cukai jualan item pengebilan dan dimensi kewangan.

Pengurus Projek boleh menyemak transaksi jualan yang tidak dibilkan menggunakan kaedah pengebilan masa dan bahan dalam [Tunggakan pengebilan masa dan bahan](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) dan pengebilan harga tetap [Pencapaian harga tetap](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Paparan ini membenarkan anda menapis dan memilih transaksi yang perlu dimasukkan dalam kitaran pengebilan seterusnya dan kemudian menanda sebagai **Sedia untuk Diinvoiskan**.

Anda boleh [mencipta invois proforma secara manual](../proforma-invoicing/create-manual-proforma-invoice.md) atau menggunakan [proses berkala](../proforma-invoicing/configure-automated-invoice-creation.md). Pengurus Projek boleh [melaraskan invois proforma draf](../proforma-invoicing/manage-proforma-invoice.md) sebagaimana yang diperlukan dan kemudian mengesahkannya.

Invois proforma yang disahkan dihantar kepada modul **Pengurusan dan perakaunan projek** dalam Kewangan. Akauntan Projek memformat dan mengemas kini kelulusan invois projek, dan kemudian menyiarkan dan mencetak dokumen. Invois projek yang disiarkan direkodkan dalam lejar Am serta sublejar Pelanggan dan Projek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]