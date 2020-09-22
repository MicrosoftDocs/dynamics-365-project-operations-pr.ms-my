---
title: Projek pesanan jualan untuk projek masa dan bahan
description: Topik ini menjelaskan cara untuk mencipta pesanan jualan berasaskan projek untuk projek masa dan bahan.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753860"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projek pesanan jualan untuk projek masa dan bahan

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Topik ini menerangkan cara untuk mencipta pesanan jualan untuk projek. Pesanan jualan hanya boleh dicipta untuk projek jenis **masa dan bahan**.

Jika projek masa dan bahan mempunyai pelbagai sumber pembiayaan pada kontrak projek, anda mesti mendayakan **Benarkan pesanan jualan untuk projek dengan pelbagai sumber pembiayaan** parameter pada halaman **Pengurusan projek dan parameter perakaunan**. 

> [!NOTE]
> - Sokongan untuk pesanan jualan projek dengan sumber pembiayaan tersedia bermula dengan keluaran aplikasi 10.0.2 dan lebih tinggi.
> - Parameter untuk mendayakan sokongan untuk pesanan jualan projek dengan pelbagai sumber pembiayaan akan dialih keluar dalam gelombang keluaran April 2020, yang mana kefungsian akan sentiasa didayakan.

Anda boleh mencipta pesanan jualan berasaskan projek dalam dua cara:

- Pergi ke projek itu sendiri. Pada Anak Tetingkap Tindakan, pilih **Urus > tugas Item > Pesanan jualan**. Maklumat projek akan menjadi lalai kepada pesanan jualan daripada projek. Jika kontrak projek mempunyai lebih daripada satu sumber pembiayaan, anda akan perlu untuk memilih sumber pembiayaan untuk menetapkan pelanggan bagi pesanan jualan. Jika terdapat hanya satu pembiayaan untuk projek itu, pelanggan akan ditetapkan secara automatik.
- Pergi ke halaman senarai **Semua pesanan jualan** dan cipta pesanan jualan baharu. Anda akan perlu untuk memilih projek bagi pesanan jualan. Selepas projek itu dipilih, pelanggan akan ditetapkan daripada sumber pembiayaan atau anda akan perlu untuk memilih sumber pembiayaan jika kontrak projek mempunyai pelbagai sumber pembiayaan.

