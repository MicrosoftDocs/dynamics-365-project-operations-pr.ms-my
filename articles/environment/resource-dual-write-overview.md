---
title: Integrasi dwi tulis Project Operations
description: Artikel ini memberikan gambaran keseluruhan bagi integrasi dwi tulis Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927983"
---
# <a name="project-operations-dual-write-integration-overview"></a>Gambaran keseluruhan integrasi dwi tulis Project Operations

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Project Operations menggunakan [keupayaan dwi tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) untuk menyegerakkan data merentasi Microsoft Dataverse dan Dynamics 365 Finance.

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
