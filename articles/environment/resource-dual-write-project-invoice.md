---
title: Integrasi invois projek
description: Artikel ini menyediakan maklumat tentang integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029035"
---
# <a name="project-invoice-integration"></a>Integrasi invois projek

Artikel ini menyediakan maklumat tentang integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.

Dalam Project Operations, pengurus Projek mengurus tunggakan pengebilan projek dan mencipta invois proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan pada invois proforma ini, kerani Akaun belum diterima atau akauntan Projek mencipta invois bersemuka dengan pelanggan. Integrasi dwi tulis memastikan butiran invois proforma disegerakkan ke aplikasi kewangan dan operasi. Selepas invois bersemuka dengan pelanggan disiarkan, sistem mengemas kini projek aktual yang berkaitan dalam Dataverse dengan butiran perakaunan. Grafik berikut memberikan gambaran keseluruhan konseptual peringkat tinggi bagi integrasi ini.

   ![Integrasi invois projek.](./media/DW5Invoicing.png)

Selepas pengurus Projek mengesahkan invois proforma dalam Dataverse, maklumat pengepala invois proforma disegerakkan ke aplikasi kewangan dan operasi menggunakan peta jadual dwi tulis, **Cadangan invois projek V2 (invois)**. Ini adalah integrasi sehala daripada Dataverse ke aplikasi kewangan dan operasi. Mencipta atau memadam cadangan invois Projek secara langsung dalam aplikasi kewangan dan operasi tidak disokong.

Pengesahan invois dalam Dataverse juga mencetuskan logik perniagaan untuk mencipta rekod berkaitan pengebilan dalam entiti **Aktual**. Rekod ini disegerakkan ke kewangan dan operasi menggunakan peta jadual dwi tulis, **Aktual integrasi Project Operations (msdyn\_actuals).** Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md). 

Baris cadangan invois Projek dicipta oleh proses berkala, **Import daripada pementasan**. Proses ini adalah berdasarkan pada butiran aktual jualan yang dibilkan dalam jadual **Pementasan aktual**. Untuk maklumat lanjut, lihat [Urus cadangan invois projek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
