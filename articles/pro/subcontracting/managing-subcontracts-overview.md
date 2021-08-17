---
title: Pengurusan subkontrak dalam Project Operations
description: Topik ini memberikan gambaran keseluruhan tentang proses pengurusan subkontrak hujung ke hujung dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994242"
---
# <a name="subcontract-management-in-project-operations"></a>Pengurusan subkontrak dalam Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Subkontrak dalam Microsoft Dynamics 365 Project Operations menyokong aliran proses perniagaan berikut.

![Aliran proses subkontrak](../media/SubcontractingProcessFlow.png)

Berikut ialah penerangan langkah demi langkah bagi proses subkontrak.

1. Pengurus projek mencipta subkontrak dengan vendor. Secara lalai, senarai harga yang dilampirkan pada rekod vendor digunakan untuk subkontrak. Akaun vendor mempunyai jenis hubungan **Vendor** atau **Pembekal**.
2. Pengurus projek boleh memperincikan semua pembelian sebagai item baris pada subkontrak. Baris subkontrak boleh untuk masa, perbelanjaan, atau produk. Kelas transaksi yang dipilih pada setiap baris subkontrak menentukan fungsi baris itu.
3. Pengurus akaun vendor dan pengurus projek boleh melakukan pengulangan pada subkontrak. Penentuan harga boleh disesuaikan dalam senarai harga pembelian yang dilampirkan pada subkontrak.
4. Pada tahap ini atau kemudian dalam proses, jika baris subkontrak adalah untuk masa, pengurus akaun vendor mengaitkan kenalan dengan setiap baris subkontrak. Perkaitan ini memberikan maklumat kepada pengurus projek yang mengusahakan subkontrak tersebut. Apabila kenalan dikaitkan dengan baris subkontrak, sistem secara automatik mencipta sumber yang boleh ditempah daripada kenalan, jika sumber yang boleh ditempah belum ada.
5. Kaedah pengebilan pada setiap baris subkontrak boleh **Harga Tetap** atau **Masa dan Bahan**. Untuk baris subkontrak harga tetap, anda boleh menyediakan jadual invois berdasarkan pencapaian.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
