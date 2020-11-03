---
title: Gambaran Keseluruhan Project Service Automation
description: Topik ini memberikan maklumat mengenai Dynamics 365 Project Service Automation kepada penyelesaian integrasi Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081369"
---
# <a name="project-service-automation-overview"></a>Gambaran Keseluruhan Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation kepada penyelesaian integrasi Kewangan menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Dynamics 365 Finance dan Dynamics 365 Project Service Automation melalui Common Data Service. Templat integrasi yang tersedia dengan ciri integrasi Data mendayakan aliran projek, kontrak projek, baris kontrak projek, pencapaian baris kontrak projek, tugas projek, kategori transaksi perbelanjaan, anggaran jam dan anggaran perbelanjaan daripada Project Service Automation kepada Kewangan.

> [!NOTE]
> - Jika anda menggunakan versi 7.3.0, anda mesti memasang KB 4074835. Anda kemudian akan dapat mengintegrasikan projek harga tetap.
> - Jika anda menggunakan versi 7.3.0 dan anda sedang membawa transaksi yuran daripada Project Service Automation, anda mesti memasang KB 4345320 untuk memasukkan yuran tersebut dalam invois projek.
> - Jika anda menggunakan versi 8.0, anda akan dapat menggunakan integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi.
> - Jika anda menggunakan versi 8.0.1 atau kemudian, anda akan dapat menyegerakkan aktual.

Sebelum anda boleh mengintegrasikan kewangan Project Service Automation, anda mesti konfigurasikan parameter integrasi Project Service Automation. Untuk maklumat lanjut, lihat: [Parameter integrasi Project Service Automation](PSA-parameters.md).

Penyelesaian integrasi ini mendayakan penyegerakan langsung dalam senario berikut:

- Kekalkan kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Kekalkan projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Kekalkan baris kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Kekalkan pencapaian baris kontrak projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Kekalkan tugas projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Kekalkan kategori transaksi perbelanjaan dalam Kewangan, dan segerakkannya secara langsung daripada Kewangan ke Project Service Automation.
- Cipta anggaran jam projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Cipta anggaran perbelanjaan projek dalam Project Service Automation, dan segerakkannya secara langsung daripada Project Service Automation ke Kewangan.
- Cipta masa, perbelanjaan dan yuran aktual projek dalam Project Service Automation, dan cipta transaksi projek dalam jurnal integrasi Project Service Automation supaya dapat disiarkan dalam kewangan.

## <a name="data-synchronization"></a>Penyegerakan data

Ilustrasi berikut menunjukkan cara data disegerakkan sebagai sebahagian daripada integrasi antara Project Service Automation dan Kewangan.

> [!NOTE]
> Tidak semua templat kini tersedia. Templat akan dikeluarkan kerana ia dilengkapkan.

[![Integrasi Project Service Automation dengan Kewangan](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Keperluan sistem untuk kewangan

Untuk menggunakan Project Service Automation kepada penyelesaian integrasi Kewangan, anda mesti memasang Enterprise Edition 7.3 dengan Platform kemas kini 12 atau kemudian.

## <a name="system-requirements-for-project-service-automation"></a>Keperluan sistem untuk Project Service Automation

Untuk menggunakan Project Service Automation kepada penyelesaian integrasi Kewangan, anda mesti memasang komponen berikut:

- Dynamics 365 Project Service Automation versi 9.0.0.0 atau lebih terkini
- Prospek untuk penyelesaian tunai bagi Dynamics 365 Sales, versi 1.14.0.0 (v14) atau kemudian
- Project Service Automation kepada penyelesaian Kewangan untuk Dynamics 365 Project Service Automation versi 1.0.0.0 atau kemudian

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Pasang Project Service Automation kepada penyelesaian integrasi Kewangan dalam tika Project Service Automation anda

Muat turun Project Service Automation kepada penyelesaian integrasi Kewangan daripada [Pusat Muat Turun Microsoft](https://www.microsoft.com/download/details.aspx?id=57016), dan ikuti arahan yang disertakan dengan penyelesaian.