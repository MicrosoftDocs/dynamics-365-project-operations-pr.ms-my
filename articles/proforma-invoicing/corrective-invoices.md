---
title: Invois yang diperbetulkan
description: Topik ini menyediakan maklumat tentang Invois yang diperbetulkan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287834"
---
# <a name="corrected-invoices"></a>Invois yang diperbetulkan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Invois yang disahkan boleh diedit. Apabila anda mengedit invois yang disahkan, draf Invois yang diperbetulkan dicipta. Oleh kerana anggapan bahawa anda mahu membalikkan semua transaksi dan kuantiti daripada invois asal, invois yang diperbetulkan memasukkan semua transaksi daripada invois asal dan semua kuantiti padanya adalah 0 (sifar).

Apabila transaksi tidak memerlukan pembetulan, anda boleh mengalih keluarnya daripada draf invois yang diperbetulkan. Untuk membalikkan atau mengembalikan hanya sebahagian kuantiti, anda boleh mengedit medan Kuantiti pada butiran baris. Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal. Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,

Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta. Jika kuantiti dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta juga. Contohnya, jika jualan dibilkan asal adalah untuk 8 jam dan butiran baris invois yang diperbetulkan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:

- Aktual jualan dibilkan untuk enam jam.
- Aktual jualan belum dibilkan untuk baki dua jam. Transaksi ini boleh sama ada dibilkan kemudian atau ditanda sebagai bukan boleh dicaj, bergantung pada rundingan dengan pelanggan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]