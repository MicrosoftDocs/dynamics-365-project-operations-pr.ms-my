---
title: Batalkan kelulusan bagi entri yang diluluskan sebelum ini
description: Artikel ini menerangkan cara pengurus projek boleh membatalkan entri masa, perbelanjaan atau penggunaan bahan yang diluluskan sebelumnya.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930467"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Batalkan kelulusan bagi entri yang diluluskan sebelum ini

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Pengurus projek atau pelulus yang telah meluluskan entri masa, perbelanjaan atau penggunaan bahan sebelumnya boleh membatalkan kelulusan entri tersebut. 

Ikut langkah-langkah ini untuk membatalkan kelulusan entri masa, perbelanjaan atau penggunaan bahan yang diluluskan sebelumnya.

1. Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.
2. Halaman senarai **Kelulusan** menunjukkan semua entri masa yang sedang menunggu kelulusan. Tukar pandangan kepada **Kelulusan lalu saya**.
3. Pilih kelulusan masa, perbelanjaan atau material untuk dibatalkan. Kemudian, pada Anak Tetingkap Tindakan, pilih **Batalkan Kelulusan**.
4. Dalam kotak mesej pengesahan yang muncul, pilih **OK** untuk mengesahkan operasi.

> [!IMPORTANT]
> Anda tidak boleh membatalkan kelulusan entri masa, perbelanjaan dan penggunaan bahan yang diluluskan sebelum ini yang telah diinvoiskan kepada pelanggan. Jika anda cuba melakukannya, anda menerima mesej yang menyatakan bahawa kelulusan tidak boleh dibatalkan kerana ia sudah diinvois. Dalam kes ini, anda boleh membatalkan kelulusan hanya jika invois pembetulan digunakan untuk mengeluarkan kredit penuh atau bayaran balik kepada pelanggan pada invois asal.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Kesan pembatalan kelulusan entri yang telah diluluskan sebelumnya

Apabila kelulusan dibatalkan, terdapat impak operasi dan impak kewangan.

### <a name="operational-impact"></a>Kesan operasi

Jika kelulusan entri dibatalkan, rekod kelulusan akan ditanda sebagai **Diserahkan**. Status entri ditukar kepada **Diserahkan**. Dalam peringkat ini, ahli pasukan projek boleh memanggil balik entri tanpa menyerahkan permintaan panggilan balik.

Pelulus boleh mengubah nilai **Kuantiti boleh dibilkan** dan **Jenis pengebilan** dan kemudian meluluskan entri sekali lagi.

### <a name="financial-impact"></a>Kesan kewangan

Jika kelulusan entri dibatalkan, aktual yang berkaitan untuk kos dan jualan dikemas kini dengan cara berikut:

- Medan **Status Pelarasan** dikemas kini kepada **Dilaraskan**.
- Medan **Status Pengebilan** dikemas kini kepada **Dibatalkan**.

Seterusnya, entri balikan dicipta dalam jadual Aktual. Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar. Satu-satunya nilai yang tidak disalin adalah nilai kuantiti. Sebaliknya, nilai ini dibalikkan. Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**. Medan **Status Pelarasan** pada aktual yang diterbalikkan ditetapkan kepada **Tidak boleh diselaraskan** dan medan **Status pengebilan** ditetapkan kepada **Dibatalkan**. Disebabkan perubahan ini, perbelanjaan yang direkodkan dan tunggakan hasil pada projek tidak lagi menjelaskan jumlah yang diwakili oleh aktual ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
