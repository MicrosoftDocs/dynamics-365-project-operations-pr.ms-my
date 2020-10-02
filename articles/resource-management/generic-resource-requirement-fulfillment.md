---
title: Pemenuhan keperluan sumber generik
description: Topik ini memberikan maklumat tentang menempah sumber bernama untuk keperluan sumber generik.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897597"
---
# <a name="generic-resource-requirement-fulfillment"></a>Pemenuhan keperluan sumber generik

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber.

1. Pada halaman **Projek**, pilih tab **Pasukan**.
2. Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian pilih **Tempah**. Atau buka keperluan sumber dan kemudian pilih **Tempah**.
3. Pada halaman **Pembantu Jadual**, pilih sumber dinamakan untuk menempah ke dalam pasukan projek anda dan kemudian pilih**Tempah**.

Apabila tempahan selesai dan diisi dengan sumber bernama, sumber generik digantikan dengan sumber bernama.

Tugasan ke atas jadual dikemas kini dengan sumber bernama juga.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Isi sumber generik dengan berbilang sumber bernama
Mengisi keperluan untuk sumber generik dengan berbilang sumber bernama adalah serupa dengan menugaskan sumber bernama tunggal. Contohnya, terdapat tugas yang mempunyai tempoh lima hari dan 120 jam usaha. Tugas ini tidak boleh diselesaikan oleh satu sumber yang bekerja 8 jam sehari selama lima hari seminggu yang biasa. 

Keperluan adalah untuk 120 jam bagi kejuruteraan robotik selama lima hari, yang mana 24 jam sehari.

Ini adalah contoh ketika sumber berbilang diperlukan untuk mengisi permintaan sumber generik. Anda perlu menempah berbilang sumber untuk mengisi keperluan.

Perbezaan utama dalam senario ini ialah bahawa sumber generik kekal dalam pasukan yang ditugaskan kepada tugas, dan ahli pasukan sumber bernama yang ditempah tidak ditugaskan sebagai sebahagian daripada kedudukan tersebut. Pengurus projek boleh menugaskan kerja sebagai sesuai kepada sumber bernama. Pandangan **Penyesuaian** boleh membantu pengurus projek dalam memecahkan tempahan di semua berbilang sumber untuk menugaskan tugasan. Ini tidak dilakukan secara automatik kerana dalam mana-mana senario yang lebih rumit daripada contoh mudah di atas seperti di mana anda mempunyai tugas yang memenuhi keperluan atau tujuan cara pengurus projek mahu menugaskan, perlu diandaikan oleh sistem. Oleh kerana sistem tidak boleh memahami tujuan, andaian mungkin akan berbeza daripada yang ditujukan dan hasil yang salah atau tidak dapat diramalkan akan berlaku. Hasil yang boleh dijangka ialah sumber generik kekal ditugaskan sehingga pengurus projek secara sengaja mencipta tugasan, dengan bantuan pandangan **Penyesuaian**.


