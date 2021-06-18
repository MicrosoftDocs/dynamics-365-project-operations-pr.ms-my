---
title: Parameter integrasi Project Service Automation
description: Topik ini menerangkan cara mengkonfigurasi cara data lalai dimasukkan apabila anda mengintegrasikan Microsoft Dynamics 365 for Project Service Automation dengan Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9793b680fc2be3b300689c4aded8005470f30519
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006432"
---
# <a name="project-service-automation-integration-parameters"></a>Parameter integrasi Project Service Automation

[!include[banner](../includes/banner.md)]

Pada halaman **Parameter integrasi Project Service Automation**, anda boleh mengkonfigurasikan cara data lalai dimasukkan apabila anda mengintegrasikan Dynamics 365 Project Service Automation dengan Dynamics 365 Finance. Untuk projek berjaya disegerakkan daripada Project Service Automation ke Kewangan, anda mesti menetapkan medan berikut.

Untuk membuka halaman **Parameter integrasi Project Service Automation**, pergi ke **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Dynamics 365 for Project Service Automation parameter integrasi**. 

> [!NOTE]
> - Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.


| Tab                    | Medan                | Penerangan |
|------------------------|----------------------|-------------|
| Umum                | Jenis projek lalai | Pilih jenis projek lalai. Apabila projek disegerakkan daripada Project Service Automation, nilai ini akan digunakan jika anda tidak memberikan nilai lalai dalam templat integrasi. Semasa penyegerakan, medan **Jenis projek** bagi projek baharu ditetapkan kepada nilai ini. Walau bagaimanapun, nilai mungkin dikemas kini apabila baris kontrak projek disegerakkan daripada Project Service Automation. |
|                        | Kategori masa        | Pilih kategori masa lalai. Nilai ini digunakan apabila anggaran jam disegerakkan daripada Project Service Automation. Apabila anggaran dan aktual jam disegerakkan daripada automasi Project Service Automation, medan **Kategori** ramalan jam projek baharu dalam Kewangan ditetapkan kepada nilai ini. |
|                        | Kategori yuran         | Pilih kategori yuran lalai. Nilai ini digunakan apabila anggaran yuran disegerakkan daripada Project Service Automation. Apabila aktual yuran disegerakkan daripada Project Service Automation, medan **Kategori** transaksi yuran baharu dalam Kewangan ditetapkan kepada nilai ini. |
| Lalai kumpulan projek | Jenis projek         | Klik **Baharu** untuk menambahkan baris di mana anda boleh memilih jenis projek untuk menetapkan kumpulan projek lalai. Jenis projek tertentu boleh dipilih hanya pada satu masa dalam konfigurasi. |
|                        | Kumpulan projek        | Pilih kumpulan projek lalai untuk jenis projek yang dipilih. Apabila projek baharu disegerakkan dengan Project Service Automation, medan **Kumpulan projek** ditetapkan kepada nilai lalai untuk jenis projek jika anda tidak memberikan nilai lalai dalam templat integrasi. |
| Jenis pengebilan lalai  | Jenis pengebilan         | Klik **Baharu** untuk menambah baris di mana anda boleh memilih jenis pengebilan untuk menetapkan sifat barisan lalai. Jenis pengebilan tertentu boleh dipilih hanya pada satu masa dalam konfigurasi. |
|                        | Sifat baris        | Pilih sifat baris lalai untuk jenis pengebilan yang dipilih. Apabila jam anggaran baharu, anggaran perbelanjaan baharu atau aktual baharu disegerakkan daripada Project Service Automation, medan **Sifat baris** ditetapkan kepada nilai lalai untuk jenis pengebilan. |
| Penguncian fungsi  | Tidak berkenaan       | Pilih fungsi untuk menyahdayakan Kewangan untuk projek dan kontrak yang berasal daripada Project Service Automation. Sebagai contoh, anda boleh mematikan keupayaan untuk mengedit kontrak dan projek, mencipta struktur pecahan kerja, dan masukkan lembaran masa dalam Kewangan. Medan berkaitan perakaunan akan terus didayakan, walaupun ia tidak tersedia oleh tetapan parameter. Secara lalai, semua fungsi didayakan. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]