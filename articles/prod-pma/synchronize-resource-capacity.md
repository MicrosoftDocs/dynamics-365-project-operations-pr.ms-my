---
title: Segerakkan kapasiti sumber
description: Topik ini memberikan maklumat mengenai cara menyegerakkan kapasiti sumber merentasi kalendar dan projek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081206"
---
# <a name="synchronize-resource-capacity"></a>Segerakkan kapasiti sumber

[!include [banner](../includes/banner.md)]

Proses untuk penyegerakan sumber membantu menjamin yang maklumat untuk kalendar dan kalendar asas masuk ke dalam penjadualan sumber projek. Jika kalendar diubah, proses membuat kemas kini yang diperlukan untuk penjadualan sumber projek. Proses ini juga membantu menambah baik prestasi, kerana maklumat sumber kalendar disegerakkan lebih awal. Oleh itu, kemas kini kepada maklumat penjadualan sumber berlaku lebih cepat. Kami mengesyorkan anda menjadualkan proses sebagai kelompok dan bukannya satu demi satu. Jika tidak, ada risiko bahawa seseorang akan melupakan tarikh yang terangkum apabila maklumat terakhir disegerakkan. Jika tarikh yang terangkum tidak digunakan, jurang boleh berlaku semasa tarikh penyegerakan.

![Penyegerakan kalendar](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Segerakkan gulungan kapasiti sumber

Proses penyegerakan direka untuk segerakkan semua maklumat kalendar sumber. Maklumat ini termasuk maklumat kalendar asas mengenai sebarang perubahan kepada jadual Kapasiti kalendar sumber projek. Jika sumber baharu ditambah dalam projek ini, penyegerakan membantu menjamin bahawa maklumat kalendar yang dikemas kini tersedia. Penyegerakan ini boleh dilakukan pada bila-bila masa.

Kami mengesyorkan agar anda menggunakan kelompok. Pilihan boleh tersedia semasa penyegerakan penempahan kapasiti.

1. Pilih **Pengurusan projek dan perakaunan** &gt; **Berkala** &gt; **Penyegerakan kapasiti** &gt; **Segerakkan gulungan kapasiti sumber**.
2. Tetapkan pilihan dalam jadual berikut.

    | Pilihan      | Penerangan |
    |-------------|-------------|
    | Kod tempoh | Secara alternatif pilih kod selang tarikh Lejar am untuk menetapkan tarikh mula dan tamat untuk proses penyegerakan untuk gulungan kapasiti sumber. |
    | Tarikh mula  | Masukkan tarikh mula untuk proses penyegerakan untuk gulungan kapasiti sumber. |
    | Tarikh tamat    | Masukkan tarikh tamat untuk proses penyegerakan untuk gulungan kapasiti sumber. |

[![Proses penyegerakan](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)