---
title: Anggaran projek dan integrasi aktual
description: Topik ini menyediakan maklumat tentang integrasi dwi tulis Project Operations untuk anggaran atau aktual projek.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955800"
---
# <a name="project-estimates-and-actuals-integration"></a>Anggaran projek dan integrasi aktual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menyediakan maklumat tentang integrasi dwi tulis Project Operations untuk anggaran atau aktual projek.

## <a name="project-estimates"></a>Anggaran projek

Buruh projek, perbelanjaan dan anggaran bahan dicipta dan dikekalkan dalam Microsoft Dataverse dan disegerakkan ke aplikasi Finance and Operations untuk tujuan perakaunan. Cipta, kemas kini dan padam operasi tidak disokong melalui aplikasi Finance and Operations.

Mencipta anggaran memerlukan konfigurasi perakaunan yang sah untuk projek. Projek yang berkaitan dengan baris kontrak mesti mempunyai kos projek yang sah dan profil hasil yang ditakrifkan dalam kos Projek dan peraturan profil hasil. Untuk maklumat lanjut, lihat [Konfigurasi perakaunan untuk projek boleh dibil](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Anggaran buruh

Anggaran buruh dicipta oleh Pengurus Projek atau pengurus Sumber yang juga memperuntukkan sumber generik atau dinamakan ke tugas projek. Rekod penugasan sumber boleh disemak pada tab **Penugasan sumber** pada halaman **Butiran Projek** dalam Dataverse. Rekod penugasan sumber dalam Dataverse mencipta rekod ramalan jam dalam aplikasi Finance and Operations menggunakan **Entiti integrasi Project Operations untuk anggaran jam (msdyn\_resourceassignments)**.

   ![Integrasi anggaran buruh](./Media/DW4LaborEstimates.png)

Dwi tulis menyegerakkan rekod penugasan sumber ke jadual pementasan (**ProjCDSEstimateHoursImport**) dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan (**ProjForecastEmpl**).

Akauntan projek menyemak rekod jam ramalan yang dicipta dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Semua projek** > **Pelan** > **Ramalan jam**.

## <a name="expense-estimates"></a>Anggaran perbelanjaan

Anggaran perbelanjaan dicipta oleh pengurus Projek pada tab **Anggaran perbelanjaan** pada halaman **Butiran Projek** dalam Dataverse. Rekod anggaran perbelanjaan disimpan dalam entiti **Baris Anggaran** dalam Dataverse. Rekod anggaran ini mempunyai kelas transaksi, **Perbelanjaan** dan disegerakkan ke rekod ramalan perbelanjaan dalam aplikasi Finance and Operations menggunakan **Entiti integrasi Project Operations untuk anggaran perbelanjaan (msdyn\_estimatelines)**.

   ![Integrasi anggaran perbelanjaan](./Media/DW4ExpenseEstimates.png)

Dwi tulis menyegerakkan rekod ramalan perbelanjaan ke jadual pementasan, **ProjCDSEstimateExpenseImport)** dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan (**ProjForecastCost**). Baris anggaran menyimpan anggaran jualan dan rekod anggaran kos secara berasingan. Logik perniagaan dalam aplikasi Finance and Operations mengisi rekod ramalan Perbelanjaan tunggal menggunakan butiran dalam jadual pementasan.

Akauntan projek boleh menyemak rekod ramalan perbelanjaan dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Semua projek** > **Pelan** > **Ramalan perbelanjaan**.

## <a name="material-estimates"></a>Anggaran bahan

Anggaran bahan dicipta oleh pengurus Projek pada tab **Anggaran Bahan** pada halaman **Butiran Projek** dalam Dataverse. Rekod anggaran bahan disimpan dalam entiti **Baris Anggaran** dalam Dataverse. Rekod anggaran ini mempunyai kelas transaksi, **Bahan** dan disegerakkan ke rekod ramalan item dalam aplikasi Finance and Operations menggunakan **Jadual integrasi Project Operations untuk anggaran bahan (msdyn\_estimatelines)**.

   ![Integrasi anggaran bahan](./Media/DW4MaterialEstimates.png)

Dwi tulis menyegerakkan rekod anggaran bahan ke jadual pementasan **ProjForecastSalesImpor** dan kemudian menggunakan logik perniagaan untuk mencipta dan mengemas kini rekod ramalan item (**ForecastSales**). Baris anggaran menyimpan anggaran jualan dan rekod anggaran kos secara berasingan. Logik perniagaan dalam aplikasi Finance and Operations mengisi rekod ramalan Item tunggal menggunakan butiran dalam jadual pementasan.

Akauntan Projek boleh menyemak rekod ramalan item dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Semua projek** > **Pelan** > **Ramalan item**.

## <a name="project-actuals"></a>Aktual projek

Aktual projek dicipta dalam Dataverse, berdasarkan pada masa, perbelanjaan, bahan dan aktiviti pengebilan. Semua atribut operasi transaksi ini termasuk kuantiti, harga kos, harga jualan dan projek yang direkod dalam entiti Dataverse ini. Untuk maklumat lanjut, lihat [Aktual](../actuals/actuals-overview.md). Rekod aktual ini disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual dwi tulis **Aktual integrasi Project Operations (msdyn\_actuals)** untuk perakaunan hiliran.

   ![Integrasi aktual](./Media/DW4Actuals.png)

Peta jadual **Aktual integrasi Project Operations** menyegerakkan semua rekod daripada entiti **Aktual** dalam Dataverse dengan atribut **Langkau Segerak (penggunaan dalaman sahaja)** ditetapkan ke **Palsu**. Nilai atribut ditetapkan dalam Dataverse secara automatik apabila rekod dicipta. Contoh atribut ini ditetapkan ke **Benar** adalah:

  - Kos projek aktual untuk transaksi antara syarikat. Untuk maklumat lanjut, lihat [Cipta transaksi antara syarikat](../project-accounting/create-intercompany-transactions.md). Rekod ini dilangkau kerana sistem mencipta semula kos projek aktual dalam aplikasi Finance and Operations apabila invois vendor antara syarikat disiarkan.
  - Rekod jualan belum dibilkan negatif yang dicipta apabila invois proforma disahkan. Rekod ini dilangkau kerana sublejar projek dalam aplikasi Finance and Operations tidak membalikkan semula rekod jualan belum dibilkan pada penginvoisan tetapi mengubah status ke diinvois sepenuhnya.

Peta jadual dwi tulis menyegerakkan rekod aktual ke jadual pementasan **ProjCDSActualsImport**. Rekod ini diproses oleh proses berkala **Import daripada jadual pementasan** apabila mencipta baris jurnal integrasi Project Operations dan baris cadangan invois projek. Untuk maklumat lanjut, lihat [Jurnal integrasi dalam Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse juga merekodkan pautan antara transaksi aktual projek dalam entiti **Sambungan transaksi**. Untuk maklumat lanjut, lihat [Pautkan rekod aktual ke asal](../actuals/linkingactuals.md). Pautan antara transaksi aktual juga disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual dwi tulis, **Entiti integrasi untuk perhubungan transaksi projek (msdyn\_transactionconnections)**. Rekod ini digunakan oleh proses berkala, **Import daripada jadual pementasan** apabila mencipta baris jurnal integrasi Project Operations dan baris cadangan invois Projek.

Penyiaran jurnal integrasi Project Operations dan cadangan invois projek mencetuskan kemas kini dalam rekod yang berkaitan dalam jadual pementasan, **ProjCDSActualsImport**. Sistem menangkap dan merekod atribut perakaunan berikut untuk transaksi aktual:

- Amaun mata wang perakaunan
- Kadar pertukaran
- Nombor baucar
- Amaun cukai jualan

Peta jadual **Aktual Integrasi Project Operations** mengemas kini rekod aktual yang berkaitan dalam Dataverse dengan maklumat ini.
