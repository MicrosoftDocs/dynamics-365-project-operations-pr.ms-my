---
title: Tarik balik entri masa atau perbelanjaan yang diluluskan
description: Topik ini memberikan maklumat tentang cara untuk menarik balik transaksi masa atau perbelanjaan yang diluluskan sebelumnya.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1a199985099745b2e62b844ef748ea2031054458
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283469"
---
# <a name="recall-approved-time-or-expense-entries"></a>Tarik balik entri masa atau perbelanjaan yang diluluskan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ahli pasukan projek atau orang lain yang menyerahkan entri masa atau perbelanjaan boleh menarik balik entri masa atau perbelanjaan selepas ia telah diluluskan. Proses untuk menarik balik entri masa atau perbelanjaan yang diluluskan mempunyai dua langkah:

1. Penyerah meminta tarik balik.
2. Pelulus meluluskan tarik balik.

## <a name="request-a-recall"></a>Meminta tarik balik

Ikut langkah ini untuk meminta tarik balik entri masa atau perbelanjaan yang diluluskan.

1. Untuk entri masa, pergi ke **Projek** \> **Kerja Saya** \> **Entri Masa**.

    –atau–

    Untuk entri perbelanjaan, pergi ke **Projek** \> **Kerja Saya** \> **Perbelanjaan**.

2. Untuk entri masa, pilih semua entri masa untuk gabungan projek dan tugas tertentu. Secara alternatif, dalam grid, pilih sel individu untuk masa pada tarikh tertentu bagi projek tertentu.

    –atau–

    Untuk entri perbelanjaan, pilih baris bagi entri perbelanjaan untuk tarik balik.

3. Pilih **Tarik balik**. Kotak dialog pengesahan muncul. Jika entri masa dan perbelanjaan yang dipilih sudah diluluskan, anda digesa untuk memasukkan sebab untuk tarik balik.
4. Masukkan sebab untuk tarik balik dan kemudian pilih **OK** untuk mengesahkan operasi. Sistem menghantar kepada individu yang meluluskan entri tersebut permintaan untuk meluluskan tarik balik.

> [!NOTE]
> Walaupun entri masa dan perbelanjaan yang diluluskan boleh ditarik balik, jika masa atau perbelanjaan yang diluluskan telah pun diinvoiskan kepada pelanggan, permintaan tarik balik tidak boleh dicipta. Pengguna yang cuba mencipta permintaan tarik balik akan menerima mesej yang menyatakan bahawa masa atau perbelanjaan tersebut tidak boleh ditarik balik kerana ia sudah diinvoiskan.

## <a name="approve-or-reject-a-recall-request"></a>Luluskan atau tolak permintaan tarik balik

Ikuti langkah ini untuk meluluskan atau menolak permintaan tarik balik.

1. Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.
2. Pada halaman senarai **Kelulusan**, tukar pandangan kepada **Permintaan tarik balik untuk kelulusan**. Senarai permintaan tarik balik yang diserahkan ditunjukkan.
3. Pilih satu atau lebih entri dan kemudian pilih sama ada **Luluskan** atau **Tolak**.
4. Jika anda memilih **Luluskan**, anda menerima mesej amaran yang menerangkan tentang kesan kelulusan tersebut. Pilih **OK** untuk mengesahkan operasi. Permintaan tarik balik diluluskan.

    –atau–

    Jika anda memilih **Tolak**, permintaan tarik balik ditolak.

> [!NOTE]
> Seperti apabila tarik balik diminta, apabila tarik balik diluluskan, sistem menyemak sebarang aktiviti penginvoisan pada entri masa atau perbelanjaan. Jika entri telah pun diinvoiskan, atau jika ia berada pada invois draf, pelulus akan menerima mesej ralat yang menyatakan bahawa masa atau perbelanjaan tersebut tidak boleh diluluskan untuk tarik balik kerana ia sudah diinvoiskan.

## <a name="impact-of-a-recall-request"></a>Kesan daripada permintaan tarik balik

Apabila kelulusan ditarik balik, terdapat kesan operasi dan kesan kewangan.

### <a name="operational-impact"></a>Kesan operasi

Jika permintaan tarik balik diluluskan, rekod kelulusan akan ditandakan sebagai **Ditolak.** Status entri ditukar kepada sama ada **Dikembalikan** atau **Ditolak**, bergantung pada sama ada ia ialah entri masa atau entri perbelanjaan.

Ahli pasukan projek boleh melihat entri, mengedit dan kemudian menghantar semula entri atau memadamkan entri sepenuhnya.

Jika permintaan tarik balik ditolak, status entri masih **Diluluskan** dan entri tersebut tidak boleh diedit oleh ahli pasukan projek atau pelulus bagi projek tersebut.

### <a name="financial-impact"></a>Kesan kewangan

Jika permintaan tarik balik diluluskan, aktual yang berkaitan dengan kos dan jualan dikemas kini dengan cara berikut:

- Medan **Status Pelarasan** dikemas kini kepada **Dilaraskan**.
- Medan **Status Pengebilan** dikemas kini kepada **Dibatalkan**.

Seterusnya, entri balikan dicipta dalam jadual Aktual. Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar. Satu-satunya nilai yang tidak disalin adalah nilai kuantiti. Sebaliknya, nilai ini dibalikkan. Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**. Medan **Status Pelarasan** pada aktual yang diterbalikkan ditetapkan kepada **Tidak boleh diselaraskan** dan medan **Status pengebilan** ditetapkan kepada **Dibatalkan**. Disebabkan perubahan ini, perbelanjaan yang direkodkan dan tunggakan hasil pada projek tidak lagi menjelaskan jumlah yang diwakili oleh aktual ini.

Jika permintaan tarik balik ditolak, tiada kesan kewangan pada projek tersebut.

## <a name="changes-to-time-entry-records"></a>Perubahan pada rekod entri masa

Ilustrasi berikut menunjukkan perubahan yang berlaku bagi entri masa yang diluluskan apabila ia ditarik balik.

![Peralihan keadaan Entri Masa](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Perubahan pada rekod entri perbelanjaan

Ilustrasi berikut menunjukkan perubahan yang berlaku bagi entri perbelanjaan yang diluluskan apabila ia ditarik balik.

![Peralihan keadaan Entri Perbelanjaan](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]