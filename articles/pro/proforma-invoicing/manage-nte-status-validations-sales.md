---
title: Urus status dan pengesahan yang tidak boleh melebihi
description: Topik ini menyediakan maklumat tentang semakan had tidak boleh dilebihi yang dilaksanakan dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130004"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Urus status dan pengesahan yang tidak boleh melebihi 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

## <a name="not-to-exceed-on-approvals"></a>Kelulusan tidak boleh dilebihi

Apabila entri masa atau perbelanjaan diserahkan, rekod kelulusan dicipta. Jika kelulusan boleh dituntut dan peta untuk masa dan baris kontrak bahan, sistem melengkapkan semakan pengesahan tidak boleh dilebihi pada peringkat berikut:

  - Semak had yang ditetapkan untuk pelanggan pada baris kontrak projek
  - Semak had yang ditetapkan pada baris kontrak
  - Semak had yang ditetapkan untuk pelanggan
  - Semak had yang ditetapkan pada kontrak

Semakan pada setiap peringkat melibatkan untuk memastikan jumlah nilai jualan ke atas kelulusan ini tidak akan melanggar had tidak boleh dilebihi pada peringkat tersebut selepas perakaunan untuk jumlah tunggakan pengebilan yang sudah direkodkan dan jumlah invois hingga kini pada peringkat tersebut.

Jika semakan lulus, kelulusan diberikan status pengesahan **Berjaya**.

Jika semakan gagal, kelulusan diberikan status pengesahan **Gagal**. Butiran penentusahan tidak boleh dilebihi akan memberitahu pengguna peringkat pengesahan yang gagal.

Apabila entri masa atau perbelanjaan yang diserahkan dianggap tidak boleh dituntut, status pengesahan tidak boleh dilebihi ditetapkan kepada **Tidak Berkenaan** dengan butiran penentusahan yang sama dengan **Tidak Berkenaan**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Tidak boleh dilebihi aktual jualan yang belum dibilkan

Apabila entri masa atau perbelanjaan diluluskan, kos dan rekod aktual jualan yang belum dibilkan dicipta. Jika aktual jualan yang belum dibilkan yang dicipta boleh dituntut dan memetakan kepada masa dan baris kontrak bahan, aplikasi menjalankan semakan pengesahan tidak boleh dilebihi pada peringkat berikut:

  - Semak had yang ditetapkan untuk pelanggan baris kontrak projek
  - Semak had yang ditetapkan pada baris kontrak
  - Semak had yang ditetapkan untuk pelanggan
  - Semak had yang ditetapkan pada kontrak

Semakan pada setiap peringkat memastikan jumlah nilai jualan ke atas aktual tidak akan melanggar had tidak boleh dilebihi pada peringkat tersebut selepas perakaunan untuk jumlah tunggakan pengebilan yang sudah direkodkan dan jumlah invois hingga kini pada peringkat tersebut.

Jika semakan lulus, aktual jualan yang belum dibilkan diberikan status tidak boleh dilebihi **Terikat**.

Jika semakan gagal, aktual jualan yang belum dibilkan diberikan status tidak boleh dilebihi **Gagal**. Butiran penentusahan memberitahu pengguna peringkat pengesahan yang gagal.

Apabila aktual jualan yang belum dibilkan dianggap tidak boleh dituntut atau percuma, jika tidak ada persediaan had tidak boleh dilebihi pada mana-mana empat peringkat atau jika aktual yang dicipta ialah Kos, Penahan, Unit Sumber atau Jualan Antara Organisasi, medan **Status Tidak Boleh Dilebihi** dan **Butiran Penentusahan Tidak Boleh Dilebihi** mesti ditetapkan kepada **Tidak Berkenaan**.

## <a name="reset-the-not-to-exceed-status"></a>Tetap semula status tidak boleh dilebihi

Anda boleh melakukan tetap semula status tidak boleh dilebihi secara pukal. Ini membolehkan Pengurus projek melaraskan pengesahan yang tidak boleh dilebihi untuk mengutamakan penginvoisan satu badan kerja, masa atau perbelanjaan daripada yang lain yang sudah dilakukan daripada jumlah yang tidak boleh dilebihi yang tersedia.

Selepas status tidak boleh dilebihi ditetapkan semula pada aktual jualan yang belum dibilkan, amaun terikat dikurangkan. Pengurus projek boleh memilih satu lagi badan kerja, masa atau perbelanjaan yang sebelum ini gagal untuk pengesahan tidak boleh dilebihi dan menilai semula badan tersebut. Dengan pengurangan dalam amaun terikat, aktual ini kini akan lulus pengesahan. Ini membantu Pengurus projek menggunakan lebih banyak pengaruh dan kawalan ke atas transaksi yang boleh diinvois untuk tempoh tersebut.

Untuk menetapkan semula status tidak boleh dilebihi, pilih satu atau lebih aktual daripada pandangan **Tunggakan Pengebilan Masa dan Bahan** atau **Aktual** dan kemudian pilih **Tetap Semula Status Tidak Boleh Dilebihi**.

Status tidak boleh dilebihi ditetapkan semula kepada **Tidak Dinilai** pada semua aktual terpilih yang berkaitan. Aktual yang mempunyai penetapan semula status tidak boleh dilebihi ialah aktual jualan yang belum dibilkan yang tidak diinvoiskan, bukan pada invois draf dan ditandakan sebagai boleh dituntut. Mana-mana aktual terpilih yang lain diabaikan.

## <a name="reevaluate-not-to-exceed-status"></a>Nilai semula status tidak boleh dilebihi

Anda boleh melakukan penilaian semula status tidak boleh dilebihi secara pukal. Penilaian semula status tidak boleh dilebihi berguna apabila:

  - Terdapat rundingan semula had tidak boleh dilebihi dengan pelanggan dan aktual perlu dinilai semula.
  - Pengurus projek mahu memperhalusi invois tunggakan jualan yang belum dibilkan dengan mengutamakan satu badan kerja daripada yang lain.

Untuk menilai semula status tidak boleh dilebihi, pilih satu atau lebih aktual daripada pandangan **Tunggakan Pengebilan Masa dan Bahan** atau **Aktual** dan kemudian pilih **Nilai Semula Status Tidak Boleh Dilebihi**.

Semua aktual terpilih yang berkaitan dengan had tidak boleh dilebihi akan dinilai terhadap persediaan had tidak boleh dilebihi. Aktual yang berkaitan untuk penilaian semula status tidak boleh dilebihi ialah aktual jualan yang belum dibilkan yang tidak diinvoiskan, bukan pada invois draf dan ditandakan sebagai boleh dituntut. Mana-mana pilihan aktual lain dipilih.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]