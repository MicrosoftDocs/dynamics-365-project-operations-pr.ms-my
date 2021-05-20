---
title: Integrasi invois projek
description: Topik ini menyediakan maklumat tentang integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955799"
---
# <a name="project-invoice-integration"></a>Integrasi invois projek

Topik ini menyediakan maklumat tentang integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.

Dalam Project Operations, pengurus Projek mengurus tunggakan pengebilan projek dan mencipta invois proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan pada invois proforma ini, kerani Akaun belum diterima atau akauntan Projek mencipta invois bersemuka dengan pelanggan. Integrasi dwi-tulis memastikan butiran invois proforma disegerakkan ke aplikasi Finance and Operations. Selepas invois bersemuka dengan pelanggan disiarkan, sistem mengemas kini projek aktual yang berkaitan dalam Dataverse dengan butiran perakaunan. Grafik berikut memberikan gambaran keseluruhan konseptual peringkat tinggi bagi integrasi ini.

   ![Integrasi invois projek](./media/DW5Invoicing.png)

Selepas pengurus Projek mengesahkan invois proforma dalam Dataverse, maklumat pengepala invois proforma disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual dwi tulis, **Cadangan invois Projek V2 (invois)**. Ini adalah integrasi sehala daripada Dataverse ke aplikasi Finance and Operations. Mencipta atau memadam cadangan invois Projek secara langsung dalam aplikasi Finance and Operations tidak disokong.

Pengesahan invois dalam Dataverse juga mencetuskan logik perniagaan untuk mencipta rekod berkaitan pengebilan dalam entiti **Aktual**. Rekod ini disegerakkan ke Finance and Operations menggunakan peta jadual dwi tulis, **Aktual integrasi Project Operations (msdyn\_actuals).** Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md). 

Baris cadangan invois Projek dicipta oleh proses berkala, **Import daripada pementasan**. Proses ini adalah berdasarkan pada butiran aktual jualan yang dibilkan dalam jadual **Pementasan aktual**. Untuk maklumat lanjut, lihat [Urus cadangan invois projek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
