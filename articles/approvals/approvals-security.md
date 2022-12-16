---
title: Keselamatan dan kelulusan
description: Artikel ini memberikan maklumat tentang persediaan keselamatan untuk bekerja dengan kelulusan dalam Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841935"
---
# <a name="security-and-approvals"></a>Keselamatan dan kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Microsoft Dynamics 365 Project Operations menggunakan dua peranan keselamatan untuk membenarkan kelulusan masa, perbelanjaan dan entri bahan:

- Pelulus Projek
- Pentadbir Pelulus Projek

## <a name="project-approver"></a>Pelulus Projek

Anda mesti mempunyai peranan keselamatan **Pelulus Projek** untuk meluluskan masa, perbelanjaan dan entri bahan. Anda juga mesti mempunyai akses kepada entiti berkaitan yang berkenaan, seperti **Projek**. Akses boleh diuntukkan oleh seseorang yang mempunyai peranan **Pengurus Projek** projek. Selain itu, anda mestilah merupakan ahli pasukan projek dan ditandakan sebagai pelulus.

Untuk meluluskan entri bukan projek, anda mestilah merupakan pengurus penyerah.

## <a name="project-approver-admin"></a>Pentadbir Pelulus Projek

> [!NOTE]
> Ciri [Set kelulusan](approval-sets.md) mesti didayakan sebelum anda boleh menggunakan fungsi Pentadbir Pelulus Projek.

Peranan keselamatan **Pentadbir Pelulus Projek** membolehkan pengguna untuk memintas dasar dan membenarkan kelulusan entri merentas semua projek. Penugasan peranan ini akan memintas logik pensahihan yang memerlukan keahlian pasukan dan ditandakan sebagai pelulus. Anda mesti mempunyai akses kepada jadual berkaitan yang berkenaan, seperti **Projek**, melalui peranan keselamatan yang ditugaskan kepada anda.

Konteks pengguna SYSTEM melepasi pensahihan dengan cara yang sama seperti peranan keselamatan Pentadbir Pelulus Projek.
