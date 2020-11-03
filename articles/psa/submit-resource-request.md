---
title: Menyerahkan permintaan sumber
description: Topik ini memberikan maklumat mengenai mengemukakan permintaan untuk sumber projek.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081321"
---
# <a name="submitting-a-resource-request"></a>Menyerahkan permintaan sumber

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda boleh menyerahkan keperluan sumber yang dijana sebagai permintaan sumber. Permintaan kemudian dihantar kepada pengurus sumber untuk memenuhi keperluan.

1. Dalam Project Service Automation (PSA) pada halaman **Projek** , klik tab **Pasukan** untuk melihat senarai sumber boleh ditempah. 
2. Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian klik **Serahkan Permintaan.**

![Menyerahkan permintaan sumber](media/RM-how-to-18.png)

Status permintaan ahli pasukan generik akan bertukar kepada **Diserahkan.**

Selepas permintaan dipenuhi oleh pengurus sumber, sumber generik akan digantikan dengan sumber yang dinamakan jika pengurus sumber memenuhi permintaan dengan tempahan sumber yang dinamakan. Jika tidak, sumber generik akan kekal pada pasukan dan status permintaan akan berubah untuk **Keperluan Menyemak Semula** , jika pengurus sumber telah mencadangkan sumber yang dinamakan.
