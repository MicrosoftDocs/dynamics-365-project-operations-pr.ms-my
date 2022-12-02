---
title: Integrasi pengurusan perbelanjaan
description: Artikel ini menyediakan maklumat tentang integrasi laporan perbelanjaan dalam Project Operations menggunakan dwi tulis.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da37adcf63a10b9f245283d377e70fd08b3aa9c5
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528006"
---
# <a name="expense-management-integration"></a>Integrasi pengurusan perbelanjaan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini menyediakan maklumat tentang integrasi laporan perbelanjaan dalam Project Operations [pelaksanaan perbelanjaan penuh](../expense/expense-overview.md) menggunakan dwi tulis.

## <a name="expense-categories"></a>Kategori perbelanjaan

Dalam pelaksanaan perbelanjaan penuh, kategori perbelanjaan dicipta dan dikekalkan dalam aplikasi kewangan dan operasi. Untuk mencipta kategori perbelanjaan baharu, lengkapkan langkah berikut:

1. Dalam Microsoft Dataverse, cipta kategori **Transaksi**. Integrasi dwi tulis akan menyegerakkan kategori urus niaga ini ke aplikasi kewangan dan operasi. Untuk maklumat lanjut, lihat [Konfigurasi kategori projek](/dynamics365/project-operations/project-accounting/configure-project-categories) dan [Persediaan dan konfigurasi integrasi data Project Operations](resource-dual-write-setup-integration.md). Hasil daripada integrasi ini, sistem mencipta empat rekod kategori dikongsi dalam aplikasi kewangan dan operasi.
2. Dalam Kewangan, pergi ke **Pengurusan perbelanjaan** > **Persediaan** > **Kategori dikongsi** dan pilih kategori dikongsi dengan kelas transaksi **Perbelanjaan**. Tetapkan parameter **Boleh digunakan dalam Perbelanjaan** ke **Benar** dan takrifkan jenis perbelanjaan untuk digunakan.
3. Menggunakan rekod kategori dikongsi ini, cipta kategori perbelanjaan baharu dengan pergi ke **Pengurusan perbelanjaan** > **Sediakan** > **Kategori perbelanjaan** dan memilih **Baharu**. Apabila rekod disimpan, dwi tulis menggunakan peta jadual, **Entiti eksport kategori perbelanjaan projek integrasi Project Operations (msdyn\_expensecategories)** untuk menyegerakkan rekod ini ke Dataverse.

  ![Integrasi kategori perbelanjaan.](./media/DW6ExpenseCategories.png)

Kategori perbelanjaan dalam aplikasi kewangan dan operasi ialah syarikat atau entiti undang-undang khusus. Terdapat rekod khusus entiti undang-undang yang berasingan dan bersesuaian dalam Dataverse. Apabila pengurus projek menganggarkan perbelanjaan, mereka tidak boleh memilih kategori perbelanjaan yang dicipta untuk projek yang dimiliki oleh syarikat berbeza berbanding syarikat yang memiliki projek yang sedang mereka usahakan. 

## <a name="expense-reports"></a>Laporan perbelanjaan

Laporan perbelanjaan dicipta dan diluluskan dalam aplikasi kewangan dan operasi. Untuk maklumat lanjut, lihat [Cipta dan proses laporan perbelanjaan dalam Dynamics 365 Project Operations](/training/modules/create-process-expense-reports/). Selepas laporan perbelanjaan diluluskan oleh pengurus Projek, laporan perbelanjaan akan disiarkan ke lejar umum. Dalam Project Operations, baris laporan perbelanjaan berkaitan projek disiarkan menggunakan peraturan penyiaran khas:

  - Kos berkaitan projek (termasuk cukai tidak dapat dipulihkan) tidak akan disiarkan dengan serta-merta ke akaun kos projek dalam lejar umum tetapi sebaliknya disiarkan ke akaun integrasi perbelanjaan. Akaun ini dikonfigurasikan dalam tab **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek**, **Project Operations pada Dynamics 365 Customer engagement**.
  - Dwi tulis disegerakkan ke Dataverse menggunakan peta jadual **Entiti eksport perbelanjaan projek integrasi Project Operations (msdyn\_expenses)**.
  - Sublejar cukai, sublejar vendor dan siaran kewangan lain direkodkan sebagaimana yang berkenaan pada masa laporan perbelanjaan disiarkan.

  ![Integrasi laporan perbelanjaan.](./media/DW6ExpenseReports.png)

Apabila rekod ditulis ke entiti **Perbelanjaan** dalam Dataverse, sistem mencetuskan proses kelulusan automatik bagi rekod. Jika perlu, status proses kelulusan automatik boleh disemak dalam Dataverse dengan pergi ke **Tetapan lanjutan** > **Sistem** > **Kerja sistem**. Selepas kelulusan selesai, rekod kelas transaksi perbelanjaan dicipta dalam entiti **Aktual**.

Aktual berkaitan perbelanjaan kemudiannya diproses menggunakan peta jadual dwi tulis **Aktual integrasi Project Operations (msdyn\_actuals)**. Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md).

Proses berkala, **Import daripada pementasan** mencipta baris jurnal berkaitan laporan Perbelanjaan dalam jurnal integrasi Project Operations. Akaun ofset lalai ke akaun integrasi perbelanjaan. Jurnal integrasi Penyiaran mengosongkan baki akaun untuk transaksi perbelanjaan dan memindahkan amaun perbelanjaan ke akaun kos projek. Sistem juga mencipta transaksi sublejar projek untuk tujuan penginvoisan hiliran dan pengiktirafan hasil.
