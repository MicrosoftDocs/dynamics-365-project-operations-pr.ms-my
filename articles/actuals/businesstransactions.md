---
title: Urus niaga perniagaan dalam Project Operations
description: Artikel ini memberikan gambaran keseluruhan tentang konsep urus niaga perniagaan dalam Microsoft Dynamics 365 Project Operations.
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

Dalam Microsoft Dynamics 365 Project Operations, *urus niaga perniagaan* ialah konsep abstrak yang tidak diwakili oleh apa-apa entiti. Walau bagaimanapun, beberapa medan dan proses biasa pada entiti direka bentuk untuk menggunakan konsep transaksi perniagaan. Entiti berikut menggunakan pengabstrakan ini:

- Butiran baris sebut harga
- Butiran baris kontrak
- Garisan anggaran
- Garisan jurnal
- Sebenar

Daripada entiti ini, Butiran baris sebut harga, Butiran baris kontrak dan Baris anggaran dipetakan ke *fasa anggaran* dalam kitaran hayat projek. Garisan jurnal dan Entiti aktual dipetakan ke *fasa pelaksanaan* dalam kitaran hayat projek.

Project Operations menganggap rekod dalam kesemua lima entiti ini sebagai urus niaga perniagaan. Satu-satunya perbezaan adalah bahawa rekod dalam entiti yang dipetakan ke fasa anggaran (Butiran baris sebut harga, Butiran baris kontrak dan Baris anggaran) dianggap *ramalan kewangan*, manakala rekod dalam entiti yang dipetakan ke fasa pelaksanaan (Garisan jurnal dan Aktual)dianggap sebagai *fakta kewangan* yang telah berlaku.

Untuk mendapatkan maklumat lanjut, lihat [Anggaran](../project-management/estimating-projects-overview.md) dan [Aktual](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsep yang unik untuk transaksi perniagaan

Konsep berikut adalah unik kepada konsep transaksi perniagaan:

- Jenis transaksi
- Kelas transaksi
- Asal transaksi
- Sambungan transaksi

### <a name="transaction-type"></a>Jenis transaksi

Jenis transaksi mewakili masa dan konteks kesan kewangan ke atas projek. Ini ditakrifkan oleh set pilihan yang mempunyai nilai disokong berikut dalam Project Operations:

- Kos
- Kontrak projek
- Jualan belum dibilkan
- Jualan dibilkan
- Jualan antara organisasi
- Kos unit persumberan

### <a name="transaction-class"></a>Kelas transaksi

Kelas transaksi mewakili jenis kos berbeza yang berlaku pada projek. Ini ditakrifkan oleh set pilihan yang mempunyai nilai disokong berikut dalam Project Operations:

- Masa
- Perbelanjaan
- Bahan
- Yuran
- Pencapaian
- Cukai

> [!NOTE]
> Nilai **Pencapaian** biasanya digunakan oleh logik perniagaan untuk pengebilan harga tetap dalam Project Operations.

### <a name="transaction-origin"></a>Asal transaksi

Asal urus niaga ialah entiti yang menyimpan asal setiap asal urus niaga perniagaan untuk membantu dalam pelaporan dan keupayaan kesan. Apabila pelaksanaan projek dimulakan, setiap urus niaga perniagaan mencipta urus niaga perniagaan lain yang akan menghasilkan satu lagi urus niaga perniagaan dan seterusnya.

### <a name="transaction-connection"></a>Sambungan transaksi

Sambungan urus niaga ialah entiti yang menyimpan hubungan antara dua urus niaga perniagaan yang sama seperti kos dan aktual jualan berkaitan atau pembalikan urus niaga yang dicetuskan oleh aktiviti pengebilan seperti pengesahan invois atau pembetulan invois.

Bersama-sama, asal Urus Niaga dan entiti sambungan Urus Niaga membantu anda menjejaki perhubungan antara urus niaga perniagaan dengan tindakan yang menyebabkan penciptaan urus niaga perniagaan khusus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
