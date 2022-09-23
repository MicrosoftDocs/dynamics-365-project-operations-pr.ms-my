---
title: Keselamatan dan kelulusan
description: Artikel ini menyediakan maklumat tentang persediaan keselamatan untuk bekerja dengan kelulusan dalam Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525410"
---
# <a name="security-and-approvals"></a>Keselamatan dan kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Microsoft Dynamics 365 Project Operations menggunakan dua peranan keselamatan untuk membolehkan kelulusan entri masa, perbelanjaan dan bahan:

- Pelulus Projek
- Pentadbir Pelulus Projek

## <a name="project-approver"></a>Pelulus Projek

Anda mesti mempunyai **Approver** Projek peranan keselamatan untuk meluluskan masa, perbelanjaan, dan penyertaan bahan projek. Anda juga mesti mempunyai akses kepada entiti berkaitan yang berkaitan, seperti **Projek**. Capaian tersebut boleh diperuntukkan oleh seseorang yang mempunyai **peranan Pengurus** Projek. Di samping itu, anda mesti menjadi ahli pasukan projek dan ditandakan sebagai pelulus.

Untuk meluluskan penyertaan bukan projek, anda mestilah pengurus pengirim.

## <a name="project-approver-admin"></a>Pentadbir Pelulus Projek

> [!NOTE]
> Ciri [set](approval-sets.md) Kelulusan mesti didayakan sebelum anda boleh menggunakan kefungsian Pentadbir Pelulus Projek.

**Pentadbir** Pelulus Projek peranan keselamatan membenarkan pengguna memintas dasar dan membenarkan kelulusan penyertaan merentas semua projek. Penyerahan peranan ini akan memintas logik pengesahan yang memerlukan keahlian pasukan dan ditandakan sebagai pelulus. Anda mesti mempunyai akses kepada entiti berkaitan yang berkaitan, seperti **Project**. Capaian tersebut boleh diperuntukkan oleh seseorang yang mempunyai **peranan Pengurus** Projek.

Konteks pengguna SYSTEM memintas pengesahan dengan cara yang sama seperti peranan keselamatan Pentadbir Approver Projek.
