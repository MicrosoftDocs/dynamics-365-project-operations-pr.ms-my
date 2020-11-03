---
title: Gambaran keseluruhan pembantu jadual
description: Topik ini memberikan maklumat mengenai kerja dengan Pembantu jadual untuk menempah sumber.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081084"
---
# <a name="schedule-assistant-overview"></a>Gambaran keseluruhan pembantu jadual

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pembantu jadual digunakan untuk menempah sumber berdasarkan keperluan yang ditakrifkan oleh Pengurus projek. Pembantu jadual bergantung pada parameter yang disediakan dalam keperluan sumber untuk mencari sumber. Pembantu jadual mengesyorkan sumber yang sepadan dengan keperluan yang berkaitan, seperti masa windows atau kemahiran yang diperlukan.

Selepas sumber yang sesuai dikenal pasti, Sumber atau Pengurus projek boleh menempah sumber untuk kerja.

## <a name="prerequisites"></a>Prasyarat

Pembantu jadual merupakan sebahagian daripada penyelesaian Universal Resource Scheduling. Penyelesaian ini disertakan dan dipasang dengan Dynamics 365 Project Operations, Dynamics 365 Field Service, dan Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Keperluan sepadan dan sumber

Keperluan sumber yang dijana adalah berdasarkan butiran seperti:

-   Ciri
-   Peranan
-   Unit perniagaan
-   Keutamaan sumber
-   Usaha kontur
-   Zon masa

Pembantu jadual menggunakan butiran ini untuk menapis sumber.

## <a name="launch-the-schedule-assistant"></a>Lancarkan Pembantu jadual

Terdapat dua cara di mana pembantu jadual dilancarkan. Jika anda menggunakan mod hibrid, dalam grid ahli pasukan anda boleh memilih sebarang ahli pasukan dengan keperluan sumber yang tidak dipatuhi, dan kemudian pilih **Tempah**. Jika anda menggunakan mod pusat, Resource manager mencari dan memilih sumber.

## <a name="schedule-assistant-filters"></a>Penapis pembantu jadual

Selepas Pembantu jadual berjalan, butiran daripada keperluan sumber dipaparkan sebagai nilai yang ditapis dalam anak tetingkap kiri. Resource manager atau Pengurus projek boleh memperhalusi hasil dengan melaraskan penapis untuk memenuhi keperluan penjadualan.

Anak tetingkap penapis menunjukkan pilihan berkaitan kerja, termasuk:

-   Mula dan tamat bekerja
-   Ciri
-   Peranan
-   Unit organisasi
-   Syarikat persumberan
-   Jenis sumber
-   Sumber diutamakan
