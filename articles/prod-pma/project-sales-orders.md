---
title: Projek pesanan jualan untuk projek masa dan bahan
description: Topik ini menjelaskan cara untuk mencipta pesanan jualan berasaskan projek untuk projek masa dan bahan.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289065"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projek pesanan jualan untuk projek masa dan bahan

[!include[banner](../includes/banner.md)]

Topik ini menerangkan cara untuk mencipta pesanan jualan untuk projek. Pesanan jualan hanya boleh dicipta untuk projek jenis **masa dan bahan**.

Jika projek masa dan bahan mempunyai pelbagai sumber pembiayaan pada kontrak projek, anda mesti mendayakan **Benarkan pesanan jualan untuk projek dengan pelbagai sumber pembiayaan** parameter pada halaman **Pengurusan projek dan parameter perakaunan**. 

> [!NOTE]
> - Sokongan untuk pesanan jualan projek dengan sumber pembiayaan tersedia bermula dengan keluaran aplikasi 10.0.2 dan lebih tinggi.
> - Parameter untuk mendayakan sokongan untuk pesanan jualan projek dengan pelbagai sumber pembiayaan akan dialih keluar dalam gelombang keluaran April 2020, yang mana kefungsian akan sentiasa didayakan.

Anda boleh mencipta pesanan jualan berasaskan projek dalam dua cara:

- Pergi ke projek itu sendiri. Pada Anak Tetingkap Tindakan, pilih **Urus > tugas Item > Pesanan jualan**. Maklumat projek akan menjadi lalai kepada pesanan jualan daripada projek. Jika kontrak projek mempunyai lebih daripada satu sumber pembiayaan, anda akan perlu untuk memilih sumber pembiayaan untuk menetapkan pelanggan bagi pesanan jualan. Jika terdapat hanya satu pembiayaan untuk projek itu, pelanggan akan ditetapkan secara automatik.
- Pergi ke halaman senarai **Semua pesanan jualan** dan cipta pesanan jualan baharu. Anda akan perlu untuk memilih projek bagi pesanan jualan. Selepas projek itu dipilih, pelanggan akan ditetapkan daripada sumber pembiayaan atau anda akan perlu untuk memilih sumber pembiayaan jika kontrak projek mempunyai pelbagai sumber pembiayaan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]