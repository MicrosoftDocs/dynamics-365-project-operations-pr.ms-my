---
title: Anggaran projek dan integrasi aktual
description: Artikel ini memberikan maklumat mengenai integrasi dwi-tulis Project Operations untuk anggaran projek dan sebenar.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029091"
---
# <a name="project-estimates-and-actuals-integration"></a>Anggaran projek dan integrasi aktual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini memberikan maklumat mengenai integrasi dwi-tulis Project Operations untuk anggaran projek dan sebenar.

## <a name="project-estimates"></a>Anggaran projek

Buruh projek, perbelanjaan dan anggaran material dicipta dan dikekalkan Microsoft Dataverse dan disegerakkan kepada aplikasi kewangan dan operasi untuk tujuan perakaunan. Buat, kemas kini dan padamkan operasi tidak disokong melalui aplikasi kewangan dan operasi.

Mencipta anggaran memerlukan konfigurasi perakaunan yang sah untuk projek. Projek yang berkaitan dengan baris kontrak mesti mempunyai kos projek yang sah dan profil hasil yang ditakrifkan dalam kos Projek dan peraturan profil hasil. Untuk maklumat lanjut, lihat [Konfigurasi perakaunan untuk projek boleh dibil](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Anggaran buruh

Anggaran buruh dicipta oleh Pengurus Projek atau pengurus Sumber yang juga memperuntukkan sumber generik atau dinamakan ke tugas projek. Rekod penugasan sumber boleh disemak pada tab **Penugasan sumber** pada halaman **Butiran Projek** dalam Dataverse. Rekod tugasan sumber dalam Dataverse mencipta rekod ramalan jam dalam aplikasi kewangan dan operasi menggunakan **entiti integrasi Project Operations untuk anggaran jam (penyerahan sumber msdyn\_)**.

   ![Integrasi anggaran buruh.](./Media/DW4LaborEstimates.png)

Dwi tulis menyegerakkan rekod penugasan sumber ke jadual pementasan (**ProjCDSEstimateHoursImport**) dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan (**ProjForecastEmpl**).

Akauntan Projek menyemak rekod jam ramalan yang dicipta dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan Projek dan perakaunan** > **Semua projek** > **Plan** > **Hour ramalan**.

## <a name="expense-estimates"></a>Anggaran perbelanjaan

Anggaran perbelanjaan dicipta oleh pengurus Projek pada tab **Anggaran perbelanjaan** pada halaman **Butiran Projek** dalam Dataverse. Rekod anggaran perbelanjaan disimpan dalam entiti **Baris Anggaran** dalam Dataverse. Rekod anggaran ini mempunyai kelas transaksi, **Perbelanjaan** dan disegerakkan ke rekod ramalan perbelanjaan dalam aplikasi kewangan dan operasi menggunakan **entiti integrasi Project Operations untuk anggaran perbelanjaan (garis anggaran msdyn\_)**.

   ![Integrasi anggaran perbelanjaan.](./Media/DW4ExpenseEstimates.png)

Dwi tulis menyegerakkan rekod ramalan perbelanjaan ke jadual pementasan, **ProjCDSEstimateExpenseImport)** dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan (**ProjForecastCost**). Baris anggaran menyimpan anggaran jualan dan rekod anggaran kos secara berasingan. Logik perniagaan dalam aplikasi kewangan dan operasi mengisi rekod ramalan Perbelanjaan tunggal menggunakan perincian ini dalam jadual pementasan.

Akauntan Projek boleh menyemak rekod ramalan perbelanjaan dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan Projek dan perakaunan** > **Semua ramalan** > **Perbelanjaan Pelan** > **projek**.

## <a name="material-estimates"></a>Anggaran bahan

Anggaran bahan dicipta oleh pengurus Projek pada tab **Anggaran Bahan** pada halaman **Butiran Projek** dalam Dataverse. Rekod anggaran bahan disimpan dalam entiti **Baris Anggaran** dalam Dataverse. Rekod anggaran ini mempunyai kelas transaksi, **Bahan dan disegerakkan ke rekod ramalan item dalam aplikasi kewangan dan operasi menggunakan** jadual integrasi Projek untuk anggaran bahan (garis anggaran msdyn **)\_**.

   ![Integrasi anggaran bahan.](./Media/DW4MaterialEstimates.png)

Dwi tulis menyegerakkan rekod anggaran bahan ke jadual pementasan **ProjForecastSalesImpor** dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan item (**ForecastSales**). Baris anggaran menyimpan anggaran jualan dan rekod anggaran kos secara berasingan. Logik perniagaan dalam aplikasi kewangan dan operasi mengisi satu rekod ramalan Item menggunakan perincian ini dalam jadual pementasan.

Akauntan Projek boleh menyemak rekod ramalan item dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan Projek dan perakaunan** > **Semua projek** > **Merancang** > **ramalan** Item.

## <a name="project-actuals"></a>Aktual projek

Aktual projek dicipta dalam Dataverse, berdasarkan pada masa, perbelanjaan, bahan dan aktiviti pengebilan. Semua atribut operasi transaksi ini termasuk kuantiti, harga kos, harga jualan dan projek yang direkod dalam entiti Dataverse ini. Untuk maklumat lanjut, lihat [Aktual](../actuals/actuals-overview.md). Rekod sebenar disegerakkan ke aplikasi kewangan dan operasi menggunakan peta **dwi-tulis Project Operations integrasi realisasi (msdyn\_ actuals)** untuk perakaunan hiliran.

   ![Integrasi aktual.](./Media/DW4Actuals.png)

Peta jadual **Aktual integrasi Project Operations** menyegerakkan semua rekod daripada entiti **Aktual** dalam Dataverse dengan atribut **Langkau Segerak (penggunaan dalaman sahaja)** ditetapkan ke **Palsu**. Nilai atribut ditetapkan dalam Dataverse secara automatik apabila rekod dicipta. Contoh atribut ini ditetapkan ke **Benar** adalah:

  - Kos projek aktual untuk transaksi antara syarikat. Untuk maklumat lanjut, lihat [Cipta transaksi antara syarikat](../project-accounting/create-intercompany-transactions.md). Rekod ini dilangkau kerana sistem mencipta semula kos projek sebenar dalam aplikasi kewangan dan operasi apabila invois vendor antara syarikat disiarkan.
  - Rekod jualan belum dibilkan negatif yang dicipta apabila invois proforma disahkan. Rekod ini dilangkau kerana subledger projek dalam aplikasi kewangan dan operasi tidak membalikkan rekod jualan yang tidak dibilkan semasa invois tetapi mengubah status kepada invois sepenuhnya.

Peta jadual dwi tulis menyegerakkan rekod aktual ke jadual pementasan **ProjCDSActualsImport**. Rekod ini diproses oleh proses berkala **Import daripada jadual pementasan** apabila mencipta baris jurnal integrasi Project Operations dan baris cadangan invois projek. Untuk maklumat lanjut, lihat [Jurnal integrasi dalam Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse juga merekodkan pautan antara transaksi aktual projek dalam entiti **Sambungan transaksi**. Untuk maklumat lanjut, lihat [Pautkan rekod aktual ke asal](../actuals/linkingactuals.md). Pautan antara transaksi sebenar juga disegerakkan ke aplikasi kewangan dan operasi menggunakan peta jadual dwi-tulis, **entiti Integrasi untuk hubungan transaksi projek (hubungan transaksi msdyn\_)**. Rekod ini digunakan oleh proses berkala, **Import daripada jadual pementasan** apabila mencipta baris jurnal integrasi Project Operations dan baris cadangan invois Projek.

Penyiaran jurnal integrasi Project Operations dan cadangan invois projek mencetuskan kemas kini dalam rekod yang berkaitan dalam jadual pementasan, **ProjCDSActualsImport**. Sistem menangkap dan merekod atribut perakaunan berikut untuk transaksi aktual:

- Amaun mata wang perakaunan
- Kadar pertukaran
- Nombor baucar
- Amaun cukai jualan

Peta jadual **Aktual Integrasi Project Operations** mengemas kini rekod aktual yang berkaitan dalam Dataverse dengan maklumat ini.
