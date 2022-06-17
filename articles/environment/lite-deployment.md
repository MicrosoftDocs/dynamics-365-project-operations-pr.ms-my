---
title: Laksanakan Project Operations - lite
description: Artikel ini memberikan maklumat tentang cara memasang penggunaan Project Operations lite - berurusan dengan invois proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930329"
---
# <a name="deploy-project-operations---lite"></a>Laksanakan Project Operations - lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_



Project Operations menyokong berbilang model pelaksanaan. Untuk menentukan model pelaksanaan terbaik, lihat [Jenis pelaksanaan](determine-deployment-type.md).


> [!IMPORTANT]
> Pelaksanaan ini, pelaksanaan Lite – urusan untuk penginvoisan proforma, keputusan dalam **Dataverse satu-satunya pelaksanaan Project Operations**.

- [Pasang Operasi Projek ke dalam persekitaran baru Dataverse](#new)
- [Pasang ke dalam persekitaran sedia ada Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Pasang Operasi Projek ke persekitaran baru Dataverse

1. [Sebagai Global atau Power Platform Pentadbir](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cipta persekitaran baru Dataverse dalam [pusat](https://admin.powerplatform.com) pentadbiran PowerPlatform. Pastikan Cipta **pangkalan data untuk persekitaran** ini dan **Dynamics 365 Apps** didayakan. Untuk mendapatkan maklumat lanjut, lihat [Cipta dan urus persekitaran dalam pusat pentadbir Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pilih **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Pasang Project Operations ke persekitaran sedia ada Dataverse
1. Pastikan persekitaran tidak dikonfigurasikan dengan [dwi-tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) kerana pemasangan kemudiannya akan memasang [Operasi Projek untuk keupayaan senario](project-operations-integrated-deployment-overview.md) berasaskan sumber/tidak berstok.
2. Sebagai [Pentadbir global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cari persekitaran dalam [Pusat pentadbir Power Platform](https://admin.powerplatform.com) di tempat anda mahu memasang Project Operations.
3. Pasang **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365. Untuk mendapatkan maklumat lanjut, lihat [Urus aplikasi Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
