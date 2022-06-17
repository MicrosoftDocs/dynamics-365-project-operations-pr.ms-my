---
title: Penarikan balik entri yang diluluskan sebelumnya
description: Artikel ini menerangkan cara ahli pasukan projek boleh meminta penarikan balik rekod masa, perbelanjaan dan penggunaan bahan yang telah diserahkan dan diluluskan sebelum ini dan cara pengurus projek boleh meluluskan atau menolak permintaan penarikan balik.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930375"
---
# <a name="recall-previously-approved-entries"></a>Penarikan balik entri yang diluluskan sebelumnya

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Ahli pasukan projek yang menyerahkan masa, perbelanjaan atau entri penggunaan bahan boleh menarik balik entri tersebut selepas ia diluluskan. Proses penarikan balik mempunyai dua langkah utama:

1. Penyerah meminta tarik balik.
2. Pelulus meluluskan permintaan penarikan balik.

## <a name="request-a-recall"></a>Meminta tarik balik

Ikuti langkah ini untuk meminta penarikan balik entri masa, perbelanjaan atau penggunaan bahan yang diluluskan.

1. Ikuti salah satu langkah ini, bergantung pada jenis entri yang anda ingin ingat:

    - Untuk entri masa, pergi ke **Projek** \> **Kemasukan Masa Kerja** \> **Saya** dan pilih semua entri masa untuk gabungan tertentu projek dan tugas. Secara alternatif, dalam grid, pilih sel individu untuk masa pada tarikh tertentu bagi projek tertentu.
    - Untuk entri perbelanjaan, pergi ke **Projek** \> **Perbelanjaan Kerja Saya** \> **dan** pilih baris untuk entri perbelanjaan untuk ditarik balik.
    - Untuk entri penggunaan bahan, pergi ke **Projek** \> **Log Penggunaan Bahan Kerja** \> **Saya**, dan pilih baris untuk entri penggunaan bahan untuk ditarik balik.

2. Pilih **Tarik balik**. Kotak dialog pengesahan muncul. Jika entri masa, perbelanjaan atau penggunaan bahan yang dipilih telah diluluskan, anda digesa untuk memasukkan sebab penarikan balik.
3. Masukkan sebab untuk tarik balik dan kemudian pilih **OK** untuk mengesahkan operasi. Sistem menghantar kepada individu yang meluluskan entri tersebut permintaan untuk meluluskan tarik balik.

> [!IMPORTANT]
> Anda tidak boleh mencipta permintaan penarikan balik untuk masa, perbelanjaan atau entri penggunaan bahan yang diluluskan yang telah diinvois kepada pelanggan. Jika anda mencuba, anda menerima mesej yang menyatakan bahawa masa, perbelanjaan atau entri penggunaan bahan tidak boleh ditarik balik kerana ia telah diinvois. Dalam kes ini, anda boleh meminta penarikan balik entri hanya jika invois pembetulan digunakan untuk mengeluarkan kredit penuh atau bayaran balik kepada pelanggan pada invois asal.

## <a name="approve-or-reject-a-recall-request"></a>Luluskan atau tolak permintaan tarik balik

Ikuti langkah ini untuk meluluskan atau menolak permintaan tarik balik.

1. Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.
2. Pada halaman senarai **Kelulusan**, tukar pandangan kepada **Permintaan tarik balik untuk kelulusan**. Senarai permintaan tarik balik yang diserahkan ditunjukkan.
3. Pilih satu atau lebih entri dan kemudian pilih sama ada **Luluskan** atau **Tolak**.
4. Jika anda memilih **Luluskan**, anda menerima mesej amaran yang menerangkan tentang kesan kelulusan tersebut. Pilih **OK** untuk mengesahkan operasi. Permintaan tarik balik diluluskan.

    –atau–

    Jika anda memilih **Tolak**, permintaan tarik balik ditolak.

> [!IMPORTANT]
> Apabila penarikan balik diluluskan, sama seperti apabila ia diminta, sistem menyemak sebarang aktiviti invois pada masa, perbelanjaan atau entri penggunaan bahan. Jika entri telah diinvois atau jika ia berada pada invois draf, pelulus menerima mesej ralat yang menyatakan bahawa masa atau perbelanjaan tidak boleh diluluskan untuk ditarik balik kerana ia telah diinvois. Dalam kes ini, pelulus boleh meluluskan penarikan balik hanya jika invois pembetulan digunakan untuk mengeluarkan kredit penuh atau bayaran balik kepada pelanggan pada invois asal.

## <a name="impact-of-a-recall-request"></a>Kesan daripada permintaan tarik balik

Apabila kelulusan ditarik balik, terdapat kesan operasi dan kesan kewangan.

### <a name="operational-impact"></a>Kesan operasi

Jika permintaan tarik balik diluluskan, rekod kelulusan akan ditandakan sebagai **Ditolak.** Status entri ditukar kepada sama ada **Dikembalikan** atau **Ditolak**, bergantung kepada sama ada kemasukan masa atau kemasukan perbelanjaan atau penggunaan bahan.

Ahli pasukan projek boleh melihat entri, mengedit dan kemudian menghantar semula entri, atau memadam sepenuhnya entri.

Jika permintaan tarik balik ditolak, status entri masih **Diluluskan** dan entri tersebut tidak boleh diedit oleh ahli pasukan projek atau pelulus bagi projek tersebut.

### <a name="financial-impact"></a>Kesan kewangan

Jika permintaan tarik balik diluluskan, aktual yang berkaitan dengan kos dan jualan dikemas kini dengan cara berikut:

- Medan **Status Pelarasan** dikemas kini kepada **Dilaraskan**.
- Medan **Status Pengebilan** dikemas kini kepada **Dibatalkan**.

Seterusnya, entri balikan dicipta dalam jadual Aktual. Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar. Satu-satunya nilai yang tidak disalin adalah nilai kuantiti. Sebaliknya, nilai ini dibalikkan. Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**. Medan **Status Pelarasan** pada aktual yang diterbalikkan ditetapkan kepada **Tidak boleh diselaraskan** dan medan **Status pengebilan** ditetapkan kepada **Dibatalkan**. Disebabkan perubahan ini, perbelanjaan yang direkodkan dan tunggakan hasil pada projek tidak lagi menjelaskan jumlah yang diwakili oleh aktual ini.

Jika permintaan tarik balik ditolak, tiada kesan kewangan pada projek tersebut.

## <a name="changes-to-time-entry-records"></a>Perubahan pada rekod entri masa

Ilustrasi berikut menunjukkan perubahan yang berlaku untuk entri masa yang diluluskan dan rekod kelulusan yang sepadan apabila ia ditarik balik.

![Peralihan keadaan kemasukan masa.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Perubahan kepada rekod kemasukan perbelanjaan dan penggunaan bahan

Ilustrasi berikut menunjukkan perubahan yang berlaku untuk perbelanjaan yang diluluskan dan entri penggunaan bahan dan rekod kelulusan yang sepadan apabila ia ditarik balik.

![Peralihan keadaan kemasukan perbelanjaan.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
