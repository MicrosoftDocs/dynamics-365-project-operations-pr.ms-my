---
title: Urus niaga perniagaan dalam Project Operations
description: Artikel ini memberikan gambaran keseluruhan konsep transaksi perniagaan dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923291"
---
# <a name="business-transactions-in-project-operations"></a>Urus niaga perniagaan dalam Project Operations

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Dalam Microsoft Dynamics 365 Project Operations, *transaksi* perniagaan ialah konsep abstrak yang tidak diwakili oleh mana-mana entiti. Walau bagaimanapun, beberapa medan dan proses biasa pada entiti direka bentuk untuk menggunakan konsep transaksi perniagaan. Entiti berikut menggunakan pengabstrakan ini:

- Butiran baris sebut harga
- Butiran baris kontrak
- Garisan anggaran
- Garisan jurnal
- Sebenar

Daripada entiti ini, butiran baris Sebut Harga, Butiran baris kontrak, dan garis Anggaran dipetakan ke *fasa* anggaran dalam kitaran hayat projek. Barisan Jurnal dan entiti Actuals dipetakan ke *fasa* pelaksanaan dalam kitaran hayat projek.

Operasi Projek menganggap rekod dalam kelima-lima entiti ini sebagai transaksi perniagaan. Satu-satunya perbezaan adalah bahawa rekod dalam entiti yang dipetakan ke fasa anggaran (Butiran baris sebut harga, butiran garis kontrak, dan garis Anggaran) dianggap sebagai *ramalan* kewangan, sedangkan rekod dalam entiti yang dipetakan ke fasa pelaksanaan (Garis jurnal dan Sebenar) dianggap sebagai *fakta* kewangan yang telah berlaku.

Untuk mendapatkan maklumat lanjut, lihat [Anggaran](../project-management/estimating-projects-overview.md) dan [Aktual](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi perniagaan

Konsep berikut adalah unik kepada konsep transaksi perniagaan:

- Jenis transaksi
- Kelas transaksi
- Asal transaksi
- Sambungan transaksi

### <a name="transaction-type"></a>Jenis transaksi

Jenis transaksi mewakili masa dan konteks kesan kewangan ke atas projek. Ia ditakrifkan oleh set pilihan yang mempunyai nilai yang disokong berikut dalam Operasi Projek:

- Kos
- Kontrak projek
- Jualan belum dibilkan
- Jualan dibilkan
- Jualan antara organisasi
- Kos unit persumberan

### <a name="transaction-class"></a>Kelas transaksi

Kelas transaksi mewakili jenis kos berbeza yang berlaku pada projek. Ia ditakrifkan oleh set pilihan yang mempunyai nilai yang disokong berikut dalam Operasi Projek:

- Masa
- Perbelanjaan
- Bahan
- Yuran
- Pencapaian
- Cukai

> [!NOTE]
> Nilai **Milestone** biasanya digunakan oleh logik perniagaan untuk pengebilan harga tetap dalam Operasi Projek.

### <a name="transaction-origin"></a>Asal transaksi

Asal transaksi adalah entiti yang menyimpan asal-usul setiap transaksi perniagaan untuk membantu pelaporan dan kebolehkesanan. Apabila pelaksanaan projek bermula, setiap transaksi perniagaan mencipta satu lagi transaksi perniagaan yang seterusnya akan membuat transaksi perniagaan lain, dan sebagainya.

### <a name="transaction-connection"></a>Sambungan transaksi

Sambungan transaksi ialah entiti yang menyimpan hubungan antara dua transaksi perniagaan yang serupa, seperti kos dan realisasi jualan yang berkaitan atau pembalikan transaksi yang dicetuskan oleh aktiviti pengebilan seperti pengesahan invois atau pembetulan invois.

Bersama-sama, asal Transaksi dan entiti sambungan Transaksi membantu anda menjejaki hubungan antara transaksi perniagaan dan tindakan yang menyebabkan transaksi perniagaan tertentu dibuat.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
