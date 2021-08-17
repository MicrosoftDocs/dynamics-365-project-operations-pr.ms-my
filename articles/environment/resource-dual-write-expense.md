---
title: Integrasi pengurusan perbelanjaan
description: Topik ini menyediakan maklumat tentang integrasi laporan perbelanjaan dalam Project Operations menggunakan dwi tulis.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986592"
---
# <a name="expense-management-integration"></a>Integrasi pengurusan perbelanjaan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menyediakan maklumat tentang integrasi laporan perbelanjaan dalam Project Operations [pelaksanaan perbelanjaan penuh](../expense/expense-overview.md) menggunakan dwi tulis.

## <a name="expense-categories"></a>Kategori perbelanjaan

Dalam pelaksanaan perbelanjaan penuh, kategori perbelanjaan dicipta dan dikekalkan dalam aplikasi Finance and Operations. Untuk mencipta kategori perbelanjaan baharu, lengkapkan langkah berikut:

1. Dalam Microsoft Dataverse, cipta kategori **Transaksi**. Integrasi dwi tulis akan menyegerakkan kategori transaksi ini ke aplikasi Finance and Operations. Untuk maklumat lanjut, lihat [Konfigurasi kategori projek](/dynamics365/project-operations/project-accounting/configure-project-categories) dan [Persediaan dan konfigurasi integrasi data Project Operations](resource-dual-write-setup-integration.md). Hasil daripada integrasi ini, sistem mencipta empat rekod kategori dikongsi dalam aplikasi Finance and Operations.
2. Dalam Kewangan, pergi ke **Pengurusan perbelanjaan** > **Persediaan** > **Kategori dikongsi** dan pilih kategori dikongsi dengan kelas transaksi **Perbelanjaan**. Tetapkan parameter **Boleh digunakan dalam Perbelanjaan** ke **Benar** dan takrifkan jenis perbelanjaan untuk digunakan.
3. Menggunakan rekod kategori dikongsi ini, cipta kategori perbelanjaan baharu dengan pergi ke **Pengurusan perbelanjaan** > **Sediakan** > **Kategori perbelanjaan** dan memilih **Baharu**. Apabila rekod disimpan, dwi tulis menggunakan peta jadual, **Entiti eksport kategori perbelanjaan projek integrasi Project Operations (msdyn\_expensecategories)** untuk menyegerakkan rekod ini ke Dataverse.

  ![Integrasi kategori perbelanjaan.](./media/DW6ExpenseCategories.png)

Kategori perbelanjaan dalam aplikasi Finance and Operations adalah syarikat atau entiti undang-undang khusus. Terdapat rekod khusus entiti undang-undang yang berasingan dan bersesuaian dalam Dataverse. Apabila pengurus projek menganggarkan perbelanjaan, mereka tidak boleh memilih kategori perbelanjaan yang dicipta untuk projek yang dimiliki oleh syarikat berbeza berbanding syarikat yang memiliki projek yang sedang mereka usahakan. 

## <a name="expense-reports"></a>Laporan perbelanjaan

Laporan perbelanjaan dicipta dan diluluskan dalam aplikasi Finance and Operations. Untuk maklumat lanjut, lihat [Cipta dan proses laporan perbelanjaan dalam Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Selepas laporan perbelanjaan diluluskan oleh pengurus Projek, laporan perbelanjaan akan disiarkan ke lejar umum. Dalam Project Operations, baris laporan perbelanjaan berkaitan projek disiarkan menggunakan peraturan penyiaran khas:

  - Kos berkaitan projek (termasuk cukai tidak dapat dipulihkan) tidak akan disiarkan dengan serta-merta ke akaun kos projek dalam lejar umum tetapi sebaliknya disiarkan ke akaun integrasi perbelanjaan. Akaun ini dikonfigurasikan dalam tab **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek**, **Project Operations pada Dynamics 365 Customer engagement**.
  - Dwi tulis disegerakkan ke Dataverse menggunakan peta jadual **Entiti eksport perbelanjaan projek integrasi Project Operations (msdyn\_expenses)**.
  - Sublejar cukai, sublejar vendor dan siaran kewangan lain direkodkan sebagaimana yang berkenaan pada masa laporan perbelanjaan disiarkan.

  ![Integrasi laporan perbelanjaan.](./media/DW6ExpenseReports.png)

Apabila rekod ditulis ke entiti **Perbelanjaan** dalam Dataverse, sistem mencetuskan proses kelulusan automatik bagi rekod. Jika perlu, status proses kelulusan automatik boleh disemak dalam Dataverse dengan pergi ke **Tetapan lanjutan** > **Sistem** > **Kerja sistem**. Selepas kelulusan selesai, rekod kelas transaksi perbelanjaan dicipta dalam entiti **Aktual**.

Aktual berkaitan perbelanjaan kemudiannya diproses menggunakan peta jadual dwi tulis **Aktual integrasi Project Operations (msdyn\_actuals)**. Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md).

Proses berkala, **Import daripada pementasan** mencipta baris jurnal berkaitan laporan Perbelanjaan dalam jurnal integrasi Project Operations. Akaun ofset lalai ke akaun integrasi perbelanjaan. Jurnal integrasi Penyiaran mengosongkan baki akaun untuk transaksi perbelanjaan dan memindahkan amaun perbelanjaan ke akaun kos projek. Sistem juga mencipta transaksi sublejar projek untuk tujuan penginvoisan hiliran dan pengiktirafan hasil.
