---
title: Batalkan kelulusan penyertaan yang diluluskan sebelum ini
description: Topik ini menerangkan cara pengurus projek boleh membatalkan kelulusan masa, perbelanjaan atau entri penggunaan bahan yang diluluskan sebelum ini.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584791"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Batalkan kelulusan penyertaan yang diluluskan sebelum ini

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pengurus projek atau pelulus yang telah meluluskan masa, perbelanjaan atau entri penggunaan bahan sebelum ini boleh membatalkan kelulusan mereka terhadap entri tersebut. 

Ikuti langkah ini untuk membatalkan kelulusan masa, perbelanjaan atau entri penggunaan bahan yang diluluskan sebelum ini.

1. Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.
2. Halaman **senarai Kelulusan** menunjukkan semua entri masa yang sedang menunggu kelulusan. Tukar pandangan kepada **kelulusan saya yang lalu**.
3. Pilih masa, perbelanjaan atau kelulusan bahan untuk dibatalkan. Kemudian, pada Anak Tetingkap Tindakan, pilih **Batalkan Kelulusan**.
4. Dalam kotak mesej pengesahan yang muncul, pilih **OK** untuk mengesahkan operasi.

> [!IMPORTANT]
> Anda tidak boleh membatalkan kelulusan masa, perbelanjaan dan entri penggunaan bahan yang telah diluluskan sebelum ini yang telah diinvois kepada pelanggan. Jika anda mencuba, anda menerima mesej yang menyatakan bahawa kelulusan tidak boleh dibatalkan kerana ia telah diinvois. Dalam kes ini, anda boleh membatalkan kelulusan hanya jika invois pembetulan digunakan untuk mengeluarkan kredit penuh atau bayaran balik kepada pelanggan pada invois asal.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Kesan membatalkan kelulusan kemasukan yang diluluskan sebelum ini

Apabila kelulusan dibatalkan, terdapat impak operasi dan impak kewangan.

### <a name="operational-impact"></a>Kesan operasi

Jika kelulusan penyertaan dibatalkan, rekod kelulusan ditandakan sebagai **Dihantar**. Status entri ditukar kepada **Dihantar**. Pada peringkat ini, ahli pasukan projek boleh menarik balik entri tanpa mengemukakan permintaan penarikan balik.

Pelulus boleh mengubah kuantiti **boleh dibilkan** dan **nilai jenis** pengebilan, dan kemudian meluluskan entri sekali lagi.

### <a name="financial-impact"></a>Kesan kewangan

Sekiranya kelulusan kemasukan dibatalkan, aktual yang sesuai untuk kos dan penjualan dikemas kini dengan cara berikut:

- Medan **Status Pelarasan** dikemas kini kepada **Dilaraskan**.
- Medan **Status Pengebilan** dikemas kini kepada **Dibatalkan**.

Seterusnya, entri balikan dicipta dalam jadual Aktual. Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar. Satu-satunya nilai yang tidak disalin adalah nilai kuantiti. Sebaliknya, nilai ini dibalikkan. Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**. Medan **Status Pelarasan** pada aktual yang diterbalikkan ditetapkan kepada **Tidak boleh diselaraskan** dan medan **Status pengebilan** ditetapkan kepada **Dibatalkan**. Disebabkan perubahan ini, perbelanjaan yang direkodkan dan tunggakan hasil pada projek tidak lagi menjelaskan jumlah yang diwakili oleh aktual ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
