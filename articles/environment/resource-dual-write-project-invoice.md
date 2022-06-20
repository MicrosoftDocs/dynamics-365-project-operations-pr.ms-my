---
title: Integrasi invois projek
description: Artikel ini memberikan maklumat mengenai integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912113"
---
# <a name="project-invoice-integration"></a>Integrasi invois projek

Artikel ini memberikan maklumat mengenai integrasi dwi-tulis Project Operations untuk penginvoisan pelanggan.

Dalam Project Operations, pengurus Projek mengurus tunggakan pengebilan projek dan mencipta invois proforma untuk pelanggan dalam Microsoft Dataverse. Berdasarkan pada invois proforma ini, kerani Akaun belum diterima atau akauntan Projek mencipta invois bersemuka dengan pelanggan. Integrasi dwi-tulis memastikan butiran invois proforma disegerakkan ke aplikasi Kewangan dan Operasi. Selepas invois bersemuka dengan pelanggan disiarkan, sistem mengemas kini projek aktual yang berkaitan dalam Dataverse dengan butiran perakaunan. Grafik berikut memberikan gambaran keseluruhan konseptual peringkat tinggi bagi integrasi ini.

   ![Integrasi invois projek.](./media/DW5Invoicing.png)

Selepas pengurus Projek mengesahkan invois proforma dalam Dataverse, maklumat pengepala invois proforma disegerakkan ke apl Kewangan dan Operasi menggunakan peta jadual dwi-tulis, **Cadangan invois projek V2 (invois)**. Ini adalah integrasi sehala dari Dataverse aplikasi Kewangan dan Operasi. Mencipta atau memadamkan cadangan invois Projek secara langsung dalam app Kewangan dan Operasi tidak disokong.

Pengesahan invois dalam Dataverse juga mencetuskan logik perniagaan untuk mencipta rekod berkaitan pengebilan dalam entiti **Aktual**. Rekod-rekod ini disegerakkan ke Kewangan dan Operasi menggunakan peta jadual dwi-tulis, **realisasi integrasi Project Operations (msdyn\_ actuals).** Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md). 

Baris cadangan invois Projek dicipta oleh proses berkala, **Import daripada pementasan**. Proses ini adalah berdasarkan pada butiran aktual jualan yang dibilkan dalam jadual **Pementasan aktual**. Untuk maklumat lanjut, lihat [Urus cadangan invois projek](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
