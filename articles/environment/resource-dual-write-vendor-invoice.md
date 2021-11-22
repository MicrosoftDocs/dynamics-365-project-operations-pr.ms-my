---
title: Integrasi invois vendor
description: Topik ini menyediakan maklumat tentang integrasi invois vendor dalam Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986502"
---
# <a name="vendor-invoice-integration"></a>Integrasi invois vendor

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Perolehan berkaitan projek dalam Dynamics 365 Project Operations boleh direkodkan dengan pergi ke **Akaun Belum Bayar** > **Invois** > **Invois vendor yang belum selesai** menggunakan dokumen invois vendor yang belum selesai. Untuk maklumat lanjut, lihat [Pembelian bahan bukan stok menggunakan invois vendor yang belum selesai](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Sebelum anda menggunakan kefungsian yang diterangkan dalam topik ini, semak dan gunakan konfigurasi yang diperlukan. Untuk maklumat lanjut, lihat [Dayakan bahan bukan stok dan invois vendor yang belum selesai](../procurement/configure-materials-nonstocked.md).

Dalam Project Operations, invois vendor berkaitan projek disiarkan menggunakan peraturan penyiaran khas:

- Kos berkaitan projek (termasuk cukai tidak dapat dipulihkan) tidak disiarkan dengan serta-merta ke akaun kos projek dalam lejar umum. Sebaliknya kos disiarkan ke **Akaun integrasi perolehan**. Akaun ini dikonfigurasi dalam **Pengurusan dan perakaunan projek** > **Persediaan** > **Parameter pengurusan dan perakaunan projek** pada **Project Operations pada tab Dynamics 365 Customer engagement**.
- Dwi tulis menyegerakkan butiran invois vendor ke Microsoft Dataverse menggunakan peta jadual berikut:

     - **Entiti eksport invois vendor projek integrasi Project Operations (msdyn_projectvendorinvoices)**: Peta jadual ini menyegerakkan maklumat pengepala invois vendor. Hanya invois vendor dengan sekurang-kurangnya satu baris yang mengandungi ID projek disegerakkan ke Dataverse.
     - **Entiti eksport baris vendor projek integrasi Project Operations (msdyn_projectvendorinvoices)**: Peta jadual ini menyegerakkan maklumat baris invois vendor. Hanya baris yang mengandungi ID projek disegerakkan ke Dataverse.

     > [!NOTE]
     > Butiran invois vendor dalam Dataverse tidak boleh diedit.

Sublejar cukai, sublejar vendor dan siaran kewangan lain direkodkan sebagaimana yang berkenaan dalam Dynamics 365 Finance apabila invois vendor disiarkan.

![Integrasi invois vendor.](media/DW7VendorInvoice.png)

Apabila rekod ditulis ke entiti **Invois vendor** dalam Dataverse, proses kelulusan automatik rekod bermula. Jika perlu, status proses kelulusan automatik boleh disemak dalam Dataverse dengan pergi ke **Tetapan lanjutan** > **Sistem** > **Kerja sistem**. Selepas kelulusan selesai, sistem mencipta rekod kelas transaksi bahan dalam entiti **Aktual**.

Aktual berkaitan bahan kemudiannya diproses menggunakan peta jadual dwi tulis **Aktual integrasi Project Operations (msdyn_actuals)**. Untuk maklumat lanjut, lihat [Anggaran dan aktual Projek](resource-dual-write-estimates-actuals.md).

Proses berkala, **Import daripada pementasan** mencipta baris jurnal integrasi Project Operations berkaitan invois vendor. Akaun ofset lalai ke akaun integrasi perolehan. Apabila jurnal integrasi disiarkan, baki akaun dikosongkan untuk transaksi invois vendor dan amaun baris dipindahkan ke akaun kos projek. Transaksi sublejar projek juga dicipta untuk tujuan penginvoisan hiliran dan pengiktirafan hasil.