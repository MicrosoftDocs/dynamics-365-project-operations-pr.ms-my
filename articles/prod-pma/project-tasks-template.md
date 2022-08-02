---
title: Segerakkan tugas projek secara langsung daripada Automasi Perkhidmatan Projek kepada kewangan dan operasi
description: Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan tugas projek terus dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028372"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Segerakkan tugas projek secara langsung daripada Automasi Perkhidmatan Projek kepada kewangan dan operasi

[!include[banner](../includes/banner.md)]

Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan tugas projek terus dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.
> - Jika anda menggunakan Enterprise Edition 7.3.0, selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian. Jika anda mesti tetap semula pengedaran perakaunan, kami mengesyorkan juga anda memasang KB 4131710.
> - Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation kepada Finance

Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat penyepaduan yang tersedia dengan ciri penyepaduan Data mendayakan aliran data tentang tugas projek daripada Project Service Automation kepada Kewangan.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Kewangan.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

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

## <a name="power-query"></a>Power Query

Anda mesti menggunakan Microsoft Power Query for Excel untuk menapis data jika syarat ini dipenuhi:

- Anda mempunyai rekod khusus sumber dalam tugas projek.

Jika anda mesti menggunakan Power Query, ikuti garis panduan ini:

- Templat tugas projek (PSA untuk Fin dan Ops) mempunyai penapis lalai yang mengecualikan rekod khusus sumber daripada tugas projek dengan tetapan penapis pada **IsLineTask** kepada **Palsu**. Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.

## <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam penyepaduan Data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]