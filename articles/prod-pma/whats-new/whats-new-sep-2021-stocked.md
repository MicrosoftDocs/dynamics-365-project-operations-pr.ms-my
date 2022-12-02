---
title: Perkara baharu atau perubahan dalam Project Operations, September 2021 untuk senario berasaskan stok/pengeluaran
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran September 2021 bagi Project Operations untuk senario berasaskan stok/pengeluaran.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029863"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Perkara baharu atau perubahan dalam Project Operations, September 2021 untuk senario berasaskan stok/pengeluaran

_**Digunakan Pada:** Project Operations untuk senario berasaskan stok/pengeluaran_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.21
 
## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
|---|---|---|
| Pengurusan projek dan perakaunan | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jika peranan Pengurus pembelian diberikan akses kepada satu entiti sah, ia juga mendapat akses kepada semua projek dalam semua entiti yang sah. |
| Pengurusan projek dan perakaunan | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Isu pembundaran cukai nilai ditambah (VAT) berlaku semasa nota kredit diselesaikan terhadap invois projek asal. |
| Pengurusan projek dan perakaunan | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Gunakan belanjawan projek alternatif untuk pengesahan belanjawan. |
| Pengurusan projek dan perakaunan | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Kumpulan harga **Harga jualan jam** tidak dikira pada struktur pecahan kerja untuk sebut harga projek. |
| Pengurusan projek dan perakaunan | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Anggaran penghapusan gagal apabila ciri **Dayakan mata wang kontrak projek untuk anggaran pengiraan** didayakan. |
| Pengurusan projek dan perakaunan | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Pemfaktoran cukai jualan mengikut kuantiti ditambah kepada amaun harga jualan apabila menggunakan cukai digunakan pada kumpulan cukai jualan bagi jurnal perbelanjaan Projek. |
| Pengurusan projek dan perakaunan | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Cukai bersyarat tidak dikira dengan betul untuk pembayaran terakhir apabila pengekalan vendor dan prabayaran digunakan pada invois pesanan pembelian. |
| Pengurusan projek dan perakaunan | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Jejak pelarasan tidak berfungsi untuk jurnal baki Permulaan. |
| Pengurusan projek dan perakaunan | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Peruntukan semakan belanjawan Projek mengikut tempoh** dibahagikan merentas semua tempoh belanjawan. Apabila peruntukan diserahkan, rekod tidak dikosongkan. |
| Pengurusan projek dan perakaunan | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Siaran kerja sedang berjalan (WIP) ke lejar umum mempunyai amaun yang salah. |
| Pengurusan projek dan perakaunan | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Kelulusan jurnal jam Projek tidak berfungsi. |
| Pengurusan projek dan perakaunan | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Harga jualan pelarasan projek tidak dikemas kini dengan kos tidak langsung apabila had pembiayaan tidak ditandakan. |
| Pengurusan projek dan perakaunan | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Keperluan item tidak boleh dicipta apabila pengepala jadual Jualan diinvoiskan dan pesanan pembelian sandaran untuk baris sedia ada telah dimuktamadkan. |
| Pengurusan projek dan perakaunan | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Jumlah pengekalan untuk peraturan pengebilan yang mempunyai pencapaian untuk projek berbeza tidak disiarkan dalam ID projek yang sama yang telah dipilih untuk pencapaian. Sebaliknya, ia disiarkan dengan projek pertama. |
| Pengurusan projek dan perakaunan | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Apabila anda memilih **Set dimensi kewangan** pada cadangan invois, ralat berikut berlaku: "Tidak dapat melakukan penukaran jenis jenis 'Dynamics.AX.Application.FormIntControl' kepada jenis 'Dynamics.AX.Application.FormStringControl'." |
| Pengurusan projek dan perakaunan | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Laporan **invois Projek** melangkau baris. |
| Pengurusan projek dan perakaunan | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Ralat berlaku apabila anda mengira kawalan kos untuk projek pelaburan. |
| Pengurusan projek dan perakaunan | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Kaedah **ProjTable::InitFromCustTable - canDeletePostalAddress** menyebabkan isu prestasi. |
| Pengurusan projek dan perakaunan | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Mesej ralat sepatutnya lebih jelas daripada "Ralat tidak diduga." |
| Pengurusan projek dan perakaunan | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Invois Projek yang menyiarkan kerja kelompok memproses dan menyiarkan cadangan invois walaupun jika baris invois belum dijana. |
| Pengurusan projek dan perakaunan | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Isu pembundaran berlaku apabila kunci konfigurasi lesen sektor Awam dimatikan. Kos atau harga jualan yang salah dijana pada jam lembaran waktu untuk kontrak yang mempunyai berbilang sumber pengasas. |
| Pengurusan projek dan perakaunan | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Harga jualan projek pada pesanan pembelian projek yang diinvoiskan tidak dikira dengan betul apabila model harga jualan ialah **Nisbah caruman**. |
| Pengurusan projek dan perakaunan | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem tidak mengambil kira hari aktif di antaranya apabila mengira kadar buruh yang berkesan untuk pekerja. |
| Pengurusan projek dan perakaunan | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Ralat penyiaran berlaku pada lembaran masa antara syarikat kerana ralat pengesahan yang berikut: "Tiada rakan kongsi perdagangan dikonfigurasikan untuk entiti sah." |
| Pengurusan projek dan perakaunan | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Perihalan daripada pesanan pembelian yang mempunyai kategori perbelanjaan tidak diambil dalam senarai transaksi projek yang disiarkan. |
| Pengurusan projek dan perakaunan | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Terdapat penukaran yang tidak betul pada jurnal Item yang disiarkan ke projek. |
| Pengurusan projek dan perakaunan | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Anda boleh mengesahkan pesanan pembelian walaupun telah melebihi had pembiayaan. |
| Pengurusan projek dan perakaunan | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Bahagian **Pembetulan/Batal invois** pada invois teks percuma akan hilang apabila ID projek dipilih. |
| Pengurusan projek dan perakaunan | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Terdapat isu prestasi apabila cadangan invois projek disiarkan daripada pesanan jualan projek yang merangkumi item dalam stok. |
| Pengurusan projek dan perakaunan | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Invois pembelian projek tidak boleh disiarkan kerana ralat berikut berlaku: "Fungsi AccDistProcessorProjectExtension.createForProjectRevenueLine telah salah dipanggil." |
| Pengurusan projek dan perakaunan | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Kemas kini kepada penciptaan kerja kelompok anggaran projek untuk menyokong pelaksanaan berbilang subtugas. |
| Pengurusan projek dan perakaunan | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status lembaran masa tidak boleh dikemas kini kepada **Draf** apabila aliran kerja tersekat dalam keadaan **Dibatalkan**. |
| Pengurusan projek dan perakaunan | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Amaun pengekalan tidak dikira dalam cadangan invois nota kredit jika terdapat berbilang baris. |
| Pengurusan projek dan perakaunan | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Apabila anda cuba mengubah amaun pada invois yang dijana daripada pesanan pembelian, ralat berikut berlaku: "Transaksi pada baucar tidak seimbang seperti XX/XX/XXXX. (mata wang perakaunan: 0.00 - mata wang pelaporan: 0.01)." |
| Pengurusan projek dan perakaunan | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Terdapat isu prestasi apabila cadangan invois projek disiarkan dalam mod kelompok, kerana cantuman dengan **GeneralJournalAccountEntry**. |
| Pengurusan projek dan perakaunan | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Terdapat isu prestasi apabila lembaran masa disiarkan. |
| Pengurusan projek dan perakaunan | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hierarki anggaran kos bagi struktur pecahan kerja tidak selaras dengan betul selepas semua tugas dikembangkan atau selepas tugas tunggal dikembangkan secara manual. |
| Pengurusan projek dan perakaunan | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Templat Excel sebut harga projek tidak boleh ditambah ke menu **Buka dalam Excel**. |
| Pengurusan projek dan perakaunan | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Nombor pengecualian cukai untuk entiti sah tidak disertakan pada invois projek bercetak. |
| Pengurusan projek dan perakaunan | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Ralat Tiada data kewangan dikemas kini dalam unit inventori apabila projek dilaraskan berhubung dengan baris kredit. |
| Pengurusan projek dan perakaunan | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Selepas anda menggunakan KB 461935, anda tidak boleh menyiarkan anggaran jika anda bertukar kepada jujukan nombor berterusan. |
| Pengurusan projek dan perakaunan | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** menyebabkan aplikasi mudah alih lembaran masa Projek untuk Android berhenti bertindak balas. |
| Pengurusan projek dan perakaunan | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai terbalik WIP daripada penyiaran invois berbeza daripada nilai WIP yang disiarkan pada asalnya daripada entri masa. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Dalam kes retainer yang digunakan, transaksi pada baucar tidak seimbang apabila hasil yang diinvoiskan untuk projek disiarkan. |
| Pengurusan projek dan perakaunan | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Apabila ciri **Peningkatan prestasi penjadualan sumber Projek** didayakan, nilai perpuluhan tidak dibundarkan dengan betul untuk ketersediaan dan kapasiti sumber. |
| Pengurusan projek dan perakaunan | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Apabila ciri **Cipta anggaran projek menggunakan berbilang tugas kelompok** didayakan, penciptaan anggaran dalam kelompok yang mempunyai berbilang subtugas berfungsi hanya untuk tempoh semasa. |
| Perjalanan dan Perbelanjaan | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Dasar permintaan perjalanan diabaikan untuk aliran kerja diluluskan tanpa ralat. |
| Perjalanan dan Perbelanjaan | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikasi Perbelanjaan Mudah Alih tidak menyimpan maklumat berikut pada baris perbelanjaan:</p><ul><li>ID projek</li><li>Sama ada perbelanjaan boleh dibilkan atau tidak</li><li>Nombor aktiviti</li></ul> |
| Perjalanan dan Perbelanjaan | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Medan **Resit yang dilampirkan** ditetapkan kepada **Ya** walaupun tiada resit dilampirkan kepada baris perbelanjaan. |
| Perjalanan dan Perbelanjaan | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Ralat berlaku apabila anda mengubah kategori perbelanjaan kepada **Peribadi**. |
| Perjalanan dan Perbelanjaan | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Anda tidak boleh melampirkan resit dan mengedit perbelanjaan induk selepas transaksi kad kredit dibahagikan kepada perbelanjaan peribadi . |
| Perjalanan dan Perbelanjaan | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Dasar perbelanjaan untuk transaksi antara syarikat yang mempunyai ID projek tidak berfungsi dengan betul. |
| Perjalanan dan Perbelanjaan | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Maklumat tarikh penyiaran hilang untuk laporan perbelanjaan yang disiarkan. |
| Perjalanan dan Perbelanjaan | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Terdapat isu kaedah pembayaran dalam aplikasi mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Permintaan perjalanan yang dicipta untuk seorang pekerja boleh digunakan untuk laporan perbelanjaan pekerja lain sebelum tarikh perwakilan. |
| Perjalanan dan Perbelanjaan | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Apabila anda mencipta perbelanjaan, perubahan kepada nilai dimensi kewangan tidak dikemas kini dengan betul pada tahap pengedaran perakaunan dalam ruang kerja **pengurusan Perbelanjaan**. |
| Perjalanan dan Perbelanjaan | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status kelulusan baris perbelanjaan utama tidak segerak dengan status kelulusan aliran kerja baris yang diperincikan. |
| Perjalanan dan Perbelanjaan | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ralat berlaku jika anda menyiarkan laporan perbelanjaan dan pemulihan cukai didayakan. |
| Perjalanan dan Perbelanjaan | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Wakil tidak boleh memadam dokumen perbelanjaan untuk pekerja yang ditamatkan. |
| Perjalanan dan Perbelanjaan | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Pemadaman baris perbelanjaan mengambil masa lebih lama daripada yang dijangkakan dan menjejaskan prestasi. |
| Perjalanan dan Perbelanjaan | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** menyebabkan rekod **TaxUncommitted** yang yatim, kerana hanya **SourceDocumentLine** dipadamkan. |
| Perjalanan dan Perbelanjaan | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** tidak membenarkan **trvExpTrans.ReferenceDataAreaId** untuk mencipta jujukan nombor baharu. |

## <a name="regulatory-updates"></a>Kemas kini kawal selia

Untuk mendapatkan maklumat tentang kemas kini kawal selia untuk aplikasi kewangan dan operasi, lihat [Kemas kini kawal selia](/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh mendaftar masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan Alat carian isu untuk melihat kemas kini kawal selia yang dirancang. Carian isu membolehkan anda membuat carian mengikut negara atau rantau, jenis ciri dan keluaran.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
