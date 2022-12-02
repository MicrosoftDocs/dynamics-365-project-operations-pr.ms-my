---
title: Gambaran keseluruhan mod pengurusan sumber
description: Artikel ini menyediakan maklumat mengenai kefungsian pengurusan Sumber dalam Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928443"
---
# <a name="resource-management-modes-overview"></a>Gambaran keseluruhan mod pengurusan sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Dynamics 365 Project Operations menyokong dua mod agar anda dapat melaksanakan aliran tempahan keseluruhan. Mod pengurusan ditakrifkan sebagai parameter projek dan boleh diubah suai jika perniagaan anda perlu berubah.    

## <a name="central-mode"></a>Mod tengah
Untuk organisasi yang memusatkan peruntukan bagi sumber untuk projek, mod Pusat menyediakan cara untuk memastikan Pengurus Projek boleh mentakrifkan keperluan sumber pada peringkat projek. Pemenuhan keperluan sumber ditugaskan kepada Resource Manager. Pengurus Projek boleh menerima atau menolak sumber yang dicadangkan oleh Resource Manager.

![Mod Tengah.](./media/resource-management-central.png)

Untuk menguruskan sumber dengan Mod Tengah, lihat:

- [Tugaskan sumber boleh ditempah generik kepada tugas dan jana keperluan sumber](/dynamics365/project-service/assign-generic-bookable-resource)
- [Tempah sumber dinamakan daripada keperluan sumber](/dynamics365/project-service/book-named-resource)
- [Serahkan permintaan sumber](/dynamics365/project-service/submit-resource-request)
- [Penuhi permintaan sumber](/dynamics365/project-service/resource-management-fulfill-requests)
- [Menerima atau menolak sumber projek yang dicadangkan daripada permintaan sumber](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mod hibrid
Untuk organisasi yang memerlukan fleksibiliti dalam peruntukan sumber, mod hibrid membolehkan kedua-dua Pengurus Projek dan Resource Manager keupayaan untuk menempah sumber.

![Mod Hibrid.](./media/resource-management-hybrid.png)

Selain daripada proses mod Pusat yang disokong, lihat artikel berikut untuk mengurus semua aliran penempahan lain yang disokong dalam mod Hibrid:

Tempah sumber secara langsung kepada projek:
- [Tempah sumber boleh ditempah dinamakan untuk pasukan projek dan menugaskan tugasan](/dynamics365/project-service/assign-named-bookable-resource)

Tempah sumber daripada keperluan sumber:
- [Tugaskan sumber boleh ditempah generik kepada tugas dan jana keperluan sumber](/dynamics365/project-service/assign-generic-bookable-resource)
- [Tempah sumber dinamakan daripada keperluan sumber](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]