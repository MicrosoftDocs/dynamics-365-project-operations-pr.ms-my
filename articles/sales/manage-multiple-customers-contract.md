---
title: Urus berbilang pelanggan pada kontrak projek
description: Topik ini menyediakan maklumat tentang cara mengurus berbilang pelanggan pada kontrak projek.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992082"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Urus berbilang pelanggan pada kontrak projek

Topik ini menyediakan maklumat tentang cara mengurus berbilang pelanggan pada kontrak projek. Anda boleh menggunakan kontrak projek apabila perjanjian kontrak untuk berbilang pelanggan diperlukan bagi membiayai perjanjian. Pada halaman **Kontrak Projek**, tab **Ringkasan** termasuk maklumat tentang pelanggan utama untuk urusan. Pelanggan lain yang mengambil bahagian dalam urusan boleh ditambah pada tab **Pelanggan**.

Semua pelanggan kontrak pada tab **Pelanggan** bagi kontrak projek adalah lalai kerana pelanggan baris kontrak pada mana-mana baris kontrak berasaskan projek baharu dicipta untuk kontrak projek. Mana-mana baris kontrak berasaskan projek sedia ada tidak mewarisi rekod pelanggan kontrak baharu yang dicipta pada masa kemudian.

Anda boleh menambah, mengemas kini atau memadam kontrak dan pelanggan baris kontrak pada bila-bila masa sebelum kontrak dimenangi. Pelanggan pada kontrak projek mesti disediakan sebagai pelanggan dalam syarikat yang memiliki atau entiti undnag-undang pada halaman **Pelanggan**. Entiti undang-undang disediakan dalam modul **Pengurusan dan perakauanan projek** bagi Dynamics 365 Project Operations dan tersedia sebagai syarikat dalam modul **Jualan Projek** dan **Penghantaran** bagi Project Operations.

## <a name="primary-customers"></a>Pelanggan utama

Bakal pelanggan pada tab **Ringkasan** kontrak projek ialah pelanggan utama kontrak. Anda tidak boleh mengemas kini pelanggan utama daripada senarai pelanggan kontrak. Jika anda cuba memadamkan pelanggan utama daripada senarai pelanggan pada kontrak, ralat akan berlaku yang mengatakan rekod pelanggan utama pada kontrak tidak boleh dipadamkan. Sebaliknya. ubah pelanggan dalam medan **Bakal Pelanggan** pada tab **Ringkasan** kontrak porjek. Apabila anda mengemas kini medan ini, pelanggan yang baharu dipilih ditambah sebagai pelanggan kontrak babahru dengan bendera **Utama** ditetapkan kepada **Ya**. Pelanggan utama sebelumnya masih lagi pelanggan pada kontrak, namun pelanggan tidak lagi menjadi pelanggan utama.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Cipta, kemas kini atau padamkan rekod pelanggan kontrak

Anda boleh mencipta, mengemas kini atau memadan pelanggan kontrak daripada tab **Pelanggan Kontrak** pada halaman **Kontrak**. Medan berikut disertakan dalam rekod pelanggan kontrak bagi kontrak projek.

| **Medan** | **Lokasi** | **Perihalan** | 
| --- | --- | --- | 
| Akaun | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Senaraikan semua akaun aktif. Medan ini dikunci selepas rekod dicipta. Untuk mengemas kini rekod, anda perlu memadam rekod dan cipta semula rekod. Jika anda telah merakam sebarang aktual atau rekod pelanggan kontrak ialah pelanggan utama, anda tidak boleh memadamkan rekod. Apabila baris kontrak dicipta, pelanggan kontrak disalin sebagai pelanggan baris kontrak. |
| Peratus Pecahan Bil | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Mewakili peratusan setiap transaksi jualan belum dibilkan yang diatribut kepada pelanggan kontrak. Apabila baris kontrak projek baharu dicipta, peratusan pecahan pengebilan disalin ke baharu bagi mana-mana baris kontrak yang dicipta dan kepada pelanggan baris kontrak projek. |
| Bil kepada Nama Kenalan | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Medan teks ini sepatutnya digunakan untuk mengenal pasti orang hubungan invois untuk pelanggan. Nilai lalai datang daripada rekod akaun yang berkaitan. Nama kenalan disalin ke **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan. |
| Nama Bil Kepada | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Gunakan medan teks ini untuk mengenal pasti orang hubungan invois untuk pelanggan. Nilai lalai datang daripada rekod akaun yang berkaitan. Nama disalin ke medan **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan. |
| Terma Pembayaran | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Nilai lalai datang daripada rekod akaun yang berkaitan. Terma disalin pada **Bil kepada Nama Kontrak** pada invois yang dijana untuk pelanggan. |
| Syarikat Pemilikan | Grid boleh diedit pada tab **Pelanggan Kontrak Projek** dan halaman utama dan cipta pantas untuk pelanggan kontrak projek. | Entiti undang-undang yang pelanggan sediakan dalam modul **Pengurusan dan perakaunan projek**. Medan ini adalah baca sahaja dan ditetapkan kepada syarikat pemilikan kontrak projek.</br>Senarai pelanggan untuk ditambah dalam medan **Akaun** sudah ditapis ke senarai daripada syarikat pemilikan dalam modul Project Operations **Pengurusan projek dan perakaunan**. Syarikat pemilikan adalah sama dengan entiti undang-undang dalam modul **Pengurusan dan perakaunan projek** Project Operations. Semua kos dan hasil yang terakru daripada projek tersebut diambil kira dalam lejar umum syarikat pemilikan. |
| Adakah Pembundaran | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Menunjukkan jika pelanggan ialah pelanggan pembundaran lalai untuk urusan. Hanya boleh ada seorang pelanggan pembundaran pada kontrak projek. Apabila kos dan jualan belum dibilkan berpecah pada kuantiti dan bakal pelanggan yang membawa kepada perbezaan pembundaran, perbezaan tersebut dikenakan kepada aktual yang memetakan kepada pelanggan tersebut. |
| Had Tidak Boleh Dilebihi | Grid boleh diedit pada tab **Pelanggan Kontrak** dan halaman utama dan cipta pantas untuk pelanggan kontrak. | Menunjukkan jika terdapat had yang dirundingkan atau had kepada jumlah keseluruhan yang akan diinvoiskan kepada pelanggan untuk penglibatan tersebut. Had tidak boleh dilebihi yang disediakan pada peringkat pelanggan kontrak dinilai berdasarkan pada aktual jualan belum dibilkan yang merujuk kepada pelanggan kontrak. |

## <a name="edit-billing-split-percentages"></a>Edit peratusan pecahan pengebilan

Anda boleh edit peratusan pecahan pengebilan dengan mengedit dalam grid. Apabila peratusan pecahan pengebilan tidak berjumlah 100 peratus, ralat berlaku. Selepas anda mengedit peratusan pecahan pengebilan, segar semula halaman **Kontrak Projek** untuk mengeluarkan ralat.

Anda juga boleh memilih **Agihkan Secara Sekata** pada subgrid pelanggan kontrak projek. Pecahan pengebilan diperuntukkan secara sekata kepada semua pelanggan pada kontrak projek. Jika terdapat mana-mana faktor pembundaran, faktor akan ditambah kepada pelanggan pembundaran. Salah seorang pelanggan kontrak sentiasa mempunyai bendera **Pembundaran** ditetapkan kepada **Ya**. Pelanggan itu ialah pelanggan pembundaran. Biasanya, pelanggan pembundaran juga merupakan pelanggan utama kontrak, tetapi tidak diperlukan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]