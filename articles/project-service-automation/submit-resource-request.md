---
title: Serahkan permintaan sumber
description: Topik ini memberikan maklumat mengenai mengemukakan permintaan untuk sumber projek.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753951"
---
# <a name="submit-a-resource-request"></a>Serahkan permintaan sumber

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda boleh menyerahkan keperluan sumber yang dijana sebagai permintaan sumber. Permintaan kemudian dihantar kepada pengurus sumber untuk memenuhi keperluan.

1. Dalam Project Service Automation (PSA) pada halaman **Projek**, klik tab **Pasukan** untuk melihat senarai sumber boleh ditempah. 
2. Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian klik **Serahkan Permintaan.**

![Menyerahkan permintaan sumber](media/RM-how-to-18.png)

Status permintaan ahli pasukan generik akan bertukar kepada **Diserahkan.**

Selepas permintaan dipenuhi oleh pengurus sumber, sumber generik akan digantikan dengan sumber yang dinamakan jika pengurus sumber memenuhi permintaan dengan tempahan sumber yang dinamakan. Jika tidak, sumber generik akan kekal pada pasukan dan status permintaan akan berubah untuk **Keperluan Menyemak Semula**, jika pengurus sumber telah mencadangkan sumber yang dinamakan.
