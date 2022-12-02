---
title: Laksanakan Project Operations - lite
description: Artikel ini memberikan maklumat tentang cara memasang pelaksanaan Project Operations lite - urusan untuk penginvoisan proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930329"
---
# <a name="deploy-project-operations---lite"></a>Laksanakan Project Operations - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_



Project Operations menyokong berbilang model pelaksanaan. Untuk menentukan model pelaksanaan terbaik, lihat [Jenis pelaksanaan](determine-deployment-type.md).


> [!IMPORTANT]
> Pelaksanaan ini, pelaksanaan Lite – urusan untuk penginvoisan proforma, keputusan dalam **Dataverse satu-satunya pelaksanaan Project Operations**.

- [Pasang Project Operations ke dalam persekitaran Dataverse baharu](#new)
- [Pasang ke dalam persekitaran Dataverse sedia ada](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Pasang Project Operations ke dalam persekitaran Dataverse baharu

1. Sebagai [Pentadbir Global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cipta persekitaran Dataverse baharu dalam [pusat pentadbir PowerPlatform](https://admin.powerplatform.com). Pastikan bahawa **Cipta pangkalan data untuk persekitaran ini** dan **Aplikasi Dynamics 365** didayakan. Untuk mendapatkan maklumat lanjut, lihat [Cipta dan urus persekitaran dalam pusat pentadbir Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Pasang Project Operations ke dalam persekitaran Dataverse sedia ada
1. Pastikan bahawa persekitaran tidak dikonfigurasikan dengan [dwitulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) kerana pemasangan kemudiannya akan memasang keupayaan [Project Operations untuk senario berasaskan sumber/bukan stok](project-operations-integrated-deployment-overview.md).
2. Sebagai [Pentadbir global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cari persekitaran dalam [Pusat pentadbir Power Platform](https://admin.powerplatform.com) di tempat anda mahu memasang Project Operations.
3. Pasang **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365. Untuk mendapatkan maklumat lanjut, lihat [Urus aplikasi Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
