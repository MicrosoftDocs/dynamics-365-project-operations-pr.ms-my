---
title: Bangunkan templat projek dengan Salin Projek
description: Topik ini menyediakan maklumat tentang cara untuk mencipta templat projek menggunakan tindakan tersuai Salin Projek.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081168"
---
# <a name="develop-project-templates-with-copy-project"></a>Bangunkan templat projek dengan Salin Projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menyokong keupayaan untuk menyalin projek dan menukarkan mana-mana tugasan kembali kepada sumber generik yang mewakili peranan. Pelanggan boleh menggunakan kefungsian ini untuk membina templat projek asas.

Apabila anda memilih **Salin Projek** , status projek sasaran akan dikemas kini. Gunakan **Sebab Status** untuk menentukan apabila tindakan salin selesai. Memilih **Salin Projek** juga mengemas kini tarikh mula projek kepada tarikh mula semasa jika tiada tarikh sasaran dikesan dalam entiti projek sasaran.

## <a name="copy-project-custom-action"></a>Tindakan tersuai Salin Projek 

### <a name="name"></a>Nama 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parameter input
Terdapat tiga parameter input:

| Parameter          | Jenis   | Nilai                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Jalur | **{"removeNamedResources":true}** atau **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Rujukan Entiti | Projek Sumber |
| Sasaran             | Rujukan Entiti | Projek Sasaran |


- **{"clearTeamsAndAssignments":true}** : Tingkah laku lalai untuk Projek untuk Web dan akan mengalih keluar semua tugasan dan ahli pasukan.
- **{"removeNamedResources":true}** Tingkah laku lalai untuk Project Operations dan akan menukar tugasan kembali kepada sumber generik.

Untuk mendapatkan lebih banyak lalai pada tindakan, lihat [Gunakan tindakan API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Tentukan medan untuk disalin 
Apabila tindakan dipanggil, **Salin Projek** akan melihat pandangan projek **Lajur Salin Projek** untuk menentukan medan untuk disalin apabila projek dicipta.
