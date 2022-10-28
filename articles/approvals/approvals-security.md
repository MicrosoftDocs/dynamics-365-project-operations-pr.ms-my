---
title: Keselamatan dan kelulusan
description: Artikel ini menyediakan maklumat tentang persediaan keselamatan untuk bekerja dengan kelulusan dalam Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709409"
---
# <a name="security-and-approvals"></a>Keselamatan dan kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Microsoft Dynamics 365 Project Operations menggunakan dua peranan keselamatan untuk membolehkan kelulusan masa, perbelanjaan dan entri bahan:

- Pelulus Projek
- Pentadbir Project Approver

## <a name="project-approver"></a>Pelulus Projek

Anda mesti mempunyai **peranan keselamatan Anggaran** Projek untuk meluluskan masa, perbelanjaan dan entri bahan projek. Anda juga mesti mempunyai akses kepada entiti berkaitan yang berkaitan, seperti **Projek**. Capaian tersebut boleh diperuntukkan oleh seseorang yang mempunyai **peranan Pengurus** Projek. Di samping itu, anda mesti menjadi ahli pasukan projek dan ditandakan sebagai pelulus.

Untuk meluluskan penyertaan bukan projek, anda mesti menjadi pengurus penyerah.

## <a name="project-approver-admin"></a>Pentadbir Project Approver

> [!NOTE]
> Ciri [Set](approval-sets.md) kelulusan mesti didayakan sebelum anda boleh menggunakan kefungsian Pentadbir Project Approver.

Pentadbir **Pelulus** Projek peranan keselamatan membolehkan pengguna memintas dasar dan membenarkan kelulusan penyertaan merentasi semua projek. Penugasan peranan ini akan memintas logik pengesahan yang memerlukan keahlian pasukan dan ditandakan sebagai pelulus. Anda mesti mempunyai capaian kepada jadual berkaitan yang berkaitan, seperti Project **, melalui** peranan keselamatan yang diperuntukkan kepada anda.

Konteks pengguna SYSTEM memintas pengesahan dengan cara yang sama seperti peranan keselamatan Pentadbir Pelulus Projek.
