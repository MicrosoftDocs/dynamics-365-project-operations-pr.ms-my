---
title: Integrasi dwi tulis Project Operations
description: Topik ini memberikan gambaran keseluruhan bagi integrasi dwi tulis Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582767"
---
# <a name="project-operations-dual-write-integration-overview"></a>Gambaran keseluruhan integrasi dwi tulis Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Operasi Projek menggunakan [keupayaan](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) dwi-tulis untuk menyegerakkan data merentasi Microsoft Dataverse dan Dynamics 365 Finance.

Ilustrasi berikut menunjukkan cara data disegerakkan sebagai sebahagian daripada integrasi ini antara Dataverse dan Kewangan.

![Gambaran keseluruhan aliran data Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations pada Dataverse menyediakan antara muka pengguna moden (UI) dan kebolehpanjangan mudah tanpa kod/kod rendah menggunakan keupayaan Power Platform. Pengurus Projek, pengurus Sumber, ahli pasukan Projek dan persona pejabat depan yang lain, melaksanakan aktiviti mereka dalam Project Operations pada Dataverse.

Project Operations dalam Kewangan menyediakan perakaunan projek dan sokongan pengiktirafan hasil. Pasang masuk Project Operations ke kerangka kerja kewangan dalam Kewangan untuk pengiraan cukai jualan, kadar pertukaran mata wang, pelaporan dimensi kewangan dan banyak lagi. Pengalaman akauntan Projek kebanyakannya berasaskan dalam kewangan.

Integrasi Project Operations terdiri daripada integrasi komponen berikut:


- [Persediaan Project Operations dan integrasi data konfigurasi](resource-dual-write-setup-integration.md) 
- [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md)
- [Invois projek](resource-dual-write-project-invoice.md)
- [Pengurusan perbelanjaan](resource-dual-write-expense.md)
- [Invois vendor](resource-dual-write-vendor-invoice.md)
