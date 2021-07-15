---
title: Integrasi dwi tulis Project Operations
description: Topik ini memberikan gambaran keseluruhan bagi integrasi dwi tulis Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368442"
---
# <a name="project-operations-dual-write-integration-overview"></a>Gambaran keseluruhan integrasi dwi tulis Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Project Operations menggunakan [keupayaan dwi tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) untuk menyegerakkan data merentasi Microsoft Dataverse dan Dynamics 365 Finance.

Ilustrasi berikut menunjukkan cara data disegerakkan sebagai sebahagian daripada integrasi ini antara Dataverse dan Kewangan.

![Gambaran keseluruhan aliran data Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations pada Dataverse menyediakan antara muka pengguna moden (UI) dan kebolehpanjangan mudah tanpa kod/kod rendah menggunakan keupayaan Power Platform. Pengurus Projek, pengurus Sumber, ahli pasukan Projek dan persona pejabat depan yang lain, melaksanakan aktiviti mereka dalam Project Operations pada Dataverse.

Project Operations dalam Kewangan menyediakan perakaunan projek dan sokongan pengiktirafan hasil. Pasang masuk Project Operations ke kerangka kerja kewangan dalam Kewangan untuk pengiraan cukai jualan, kadar pertukaran mata wang, pelaporan dimensi kewangan dan banyak lagi. Pengalaman akauntan Projek kebanyakannya berasaskan dalam kewangan.

Integrasi Project Operations terdiri daripada integrasi komponen berikut:


- [Persediaan Project Operations dan integrasi data konfigurasi](resource-dual-write-setup-integration.md) 
- [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md)
- [Invois projek](resource-dual-write-project-invoice.md)
- [Pengurusan perbelanjaan](resource-dual-write-expense.md)
- [Invois vendor](resource-dual-write-vendor-invoice.md)
