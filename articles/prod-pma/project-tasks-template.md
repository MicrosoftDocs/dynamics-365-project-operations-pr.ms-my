---
title: Segerakkan tugas projek secara langsung daripada Project Service Automation kepada Finance and Operations
description: Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan tugas projek secara langsung daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081210"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Segerakkan tugas projek secara langsung daripada Project Service Automation kepada Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menerangkan templat dan tugas dasar yang digunakan untuk segerakkan tugas projek secara langsung daripada Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.
> - Jika anda menggunakan Enterprise Edition 7.3.0, selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian. Jika anda mesti tetap semula pengedaran perakaunan, kami mengesyorkan juga anda memasang KB 4131710.
> - Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation kepada Finance

Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat penyepaduan yang tersedia dengan ciri penyepaduan Data mendayakan aliran data tentang tugas projek daripada Project Service Automation kepada Kewangan.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk penyepaduan Project Service Automation dengan Kewangan](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Templat dan tugas

Untuk mengakses templat, dalam pusat pentadbir Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.

Templat dan tugas dasar berikut digunakan untuk segerakkan tugas projek daripada Project Service Automation kepada Kewangan:

- **Nama templat dalam penyepaduan Data:** Tugas projek (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:** Tugas projek

Sebelum penyegerakan tugas projek boleh berlaku, anda mesti segerakkan kontrak projek dan projek.

## <a name="entity-set"></a>Set entiti

| Project Service Automation | Kewangan                             |
|----------------------------|-------------------------------------|
| Tugas Projek              | Entiti penyepaduan untuk tugas projek |

## <a name="entity-flow"></a>Aliran entiti

Tugas projek diuruskan dalam Project Service Automation, dan ia disegerakkan kepada Kewangan sebagai aktiviti projek.

## <a name="prerequisites-and-mapping-setup"></a>Persediaan prasyarat dan pemetaan

Sebelum penyegerakan tugas projek boleh berlaku, anda mesti segerakkan kontrak projek dan projek.

## <a name="power-query"></a>Pertanyaan Kuasa

Anda mesti menggunakan Microsoft Power Query for Excel untuk menapis data jika syarat ini dipenuhi:

- Anda mempunyai rekod khusus sumber dalam tugas projek.

Jika anda mesti menggunakan Power Query, ikut garis panduan ini:

- Templat tugas projek (PSA untuk Fin dan Ops) mempunyai penapis lalai yang mengecualikan rekod khusus sumber daripada tugas projek dengan tetapan penapis pada **IsLineTask** kepada **Palsu**. Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.

## <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam penyepaduan Data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]