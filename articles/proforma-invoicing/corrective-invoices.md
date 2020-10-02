---
title: Invois yang diperbetulkan
description: Topik ini menyediakan maklumat tentang Invois yang diperbetulkan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898092"
---
# <a name="corrected-invoices"></a>Invois yang diperbetulkan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Invois yang disahkan boleh diedit. Apabila anda mengedit invois yang disahkan, draf Invois yang diperbetulkan dicipta. Oleh kerana anggapan bahawa anda mahu membalikkan semua transaksi dan kuantiti daripada invois asal, invois yang diperbetulkan memasukkan semua transaksi daripada invois asal dan semua kuantiti padanya adalah 0 (sifar).

Apabila transaksi tidak memerlukan pembetulan, anda boleh mengalih keluarnya daripada draf invois yang diperbetulkan. Untuk membalikkan atau mengembalikan hanya sebahagian kuantiti, anda boleh mengedit medan Kuantiti pada butiran baris. Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal. Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,

Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta. Jika kuantiti dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta juga. Contohnya, jika jualan dibilkan asal adalah untuk 8 jam dan butiran baris invois yang diperbetulkan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:

- Aktual jualan dibilkan untuk enam jam.
- Aktual jualan belum dibilkan untuk baki dua jam. Transaksi ini boleh sama ada dibilkan kemudian atau ditanda sebagai bukan boleh dicaj, bergantung pada rundingan dengan pelanggan.
