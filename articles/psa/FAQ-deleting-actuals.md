---
title: Mengapakah saya tidak dapat memadamkan rekod daripada entiti aktual?
description: Topik ini memberikan maklumat tentang sebab anda tidak boleh merekod daripada entiti aktual.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148969"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Mengapakah saya tidak dapat memadamkan rekod daripada entiti Aktual?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) tidak membenarkan anda memadam aktual kerana mereka berfungsi sebagai sumber kebenaran untuk transaksi yang mempunyai implikasi kewangan kepada sistem hiliran, seperti lejar am. Jika aktual boleh dipadamkan, integriti transaksi pelaporan kewangan boleh dipersoalkan. Untuk mewujudkan jejak audit, pelanggan hendaklah menggunakan jurnal untuk mencipta transaksi pampasan.

