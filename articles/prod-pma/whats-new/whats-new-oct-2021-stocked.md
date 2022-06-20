---
title: Apa yang baru atau berubah dalam Operasi Projek, Oktober 2021 untuk senario berasaskan stok/pengeluaran
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Oktober 2021 Operasi Projek untuk senario berasaskan stok / pengeluaran.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933687"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Apa yang baru atau berubah dalam Operasi Projek, Oktober 2021 untuk senario berasaskan stok/pengeluaran

_**Digunakan Pada:** Project Operations untuk senario berasaskan stok/pengeluaran_

Artikel ini terpakai kepada komponen dan versi Microsoft Dynamics 365 Project Operations berikut :

- Pengurusan projek dan perakaunan dalam persekitaran yang Dynamics 365 Finance versi 10.0.22
 
## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
|--------------|------------------|----------------|
| Pengurusan projek dan perakaunan | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Kerja projek dalam proses (WIP) dan jumlah hasil terakru tidak diterbalikkan dengan betul apabila invois pelanggan antara syarikat disiarkan. |
| Pengurusan projek dan perakaunan | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Fungsi **Cegah penutupan projek jika transaksi terbuka wujud** tidak berfungsi. |
| Pengurusan projek dan perakaunan | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikasi pengebilan pada invois teks percuma tidak mengisi dimensi secara automatik daripada projek apabila fungsi tersebut didayakan. |
| Pengurusan projek dan perakaunan | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dalam senario bukan antara syarikat, WIP dan jumlah hasil terakru tidak diterbalikkan dengan betul apabila invois projek disiarkan. |
| Pengurusan projek dan perakaunan | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Nilai debit dan kredit ditukar apabila Microsoft Excel tambahan digunakan dengan jurnal Perbelanjaan Projek dan medan jenis **akaun Offset disetkan** kepada **Project**. |
| Pengurusan projek dan perakaunan | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Jumlah yang disiarkan dalam urus niaga projek adalah berlebihan pada pesanan pembelian projek yang termasuk item stok dan yang mempunyai jumlah cukai yang tidak boleh ditolak apabila **UseTax** ditandakan. |
| Pengurusan projek dan perakaunan | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem ini membahagikan jumlah antara laporan keuntungan dan kerugian projek dan laporan WIP projek. |
| Pengurusan projek dan perakaunan | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventori di tangan tidak betul selepas keperluan item yang sebahagiannya dikembalikan diselaraskan. |
| Pengurusan projek dan perakaunan | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nama sumber diduplikasi dalam Operasi Projek apabila ia diedit dalam Microsoft Project. |
| Pengurusan projek dan perakaunan | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Laporan perbelanjaan antara syarikat yang mempunyai Akaun yang perlu dibayar antara syarikat yang belum selesai kos invois vendor pertama kali diposkan ke **jenis pengeposan kos** Project WIP. Walau bagaimanapun, semasa pemprosesan, kos yang berkaitan dengan anggaran diposkan ke **jenis pengeposan kos** Projek dan bukannya jenis pengeposan kos **Intercompany yang dijangkakan**. |
| Pengurusan projek dan perakaunan | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hasil pengekalan vendor dalam transaksi perbelanjaan projek tidak ditunjukkan. |
| Pengurusan projek dan perakaunan | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Lembaran masa mesti membundarkan jumlah transaksi dalam mata wang transaksi kepada bilangan tempat perpuluhan yang ditentukan pada semua pengedaran perakaunan dan entri peruntukan jurnal umum. |
| Pengurusan projek dan perakaunan | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Kuantiti keperluan item projek dikemas kini secara automatik apabila pesanan yang dirancang ditegakkan. |
| Pengurusan projek dan perakaunan | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Nombor baucar, baki vendor jenis transaksi, dan nombor akaun tidak boleh diterbalikkan pada invois prabayar pesanan pembelian. |
| Pengurusan projek dan perakaunan | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Invois vendor antara syarikat rosak apabila penyepaduan invois vendor dihidupkan. |
| Pengurusan projek dan perakaunan | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Apabila anda mencipta jurnal perbelanjaan Projek, amaun kos ditunjukkan dalam medan **Kredit**. |
| Pengurusan projek dan perakaunan | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Syarat pembayaran pada invois projek tidak berfungsi seperti yang diharapkan. |
| Pengurusan projek dan perakaunan | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Baucar lembaran masa mungkin digunakan semula apabila jujukan nombor disediakan sebagai berterusan. |
| Pengurusan projek dan perakaunan | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PERANCIS: Logik **amaun** pengekalan manual tidak sepadan dengan **logik Amaun** pengekalan automatik dalam cadangan invois kontrak Projek. |
| Pengurusan projek dan perakaunan | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Apabila pengekalan vendor dikeluarkan, pengeposan baucar mempunyai baris tambahan yang salah. |
| Pengurusan projek dan perakaunan | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Apabila medan Tarikh** invois pada **halaman Cipta cadangan** invois diubah, ralat berikut mungkin berlaku: "Rujukan objek tidak ditetapkan kepada tika objek." |
| Pengurusan projek dan perakaunan | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ralat berlaku apabila anda cuba meluluskan lembaran masa daripada **aliran kerja TSLine** dan terdapat dasar lembaran masa untuk hari Sabtu dan Ahad. |
| Pengurusan projek dan perakaunan | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Jenis item projek baki permulaan dikecualikan daripada **ringkasan** transaksi cadangan Invois apabila jumlah invois cadangan invois cadangan dikira. |
| Pengurusan projek dan perakaunan | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jika kos penggunaan pada pesanan pengeluaran projek adalah 0 (sifar), ralat berikut berlaku apabila anda cuba menganggarkan: "Cuba untuk membahagikan dengan sifar." |
| Pengurusan projek dan perakaunan | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikasi Mudah Alih Project Timesheet untuk Android berhenti bertindak balas. Isu ini berkaitan **dengan TimeEntryDataManager ArgumentNullException**. |
| Pengurusan projek dan perakaunan | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnal integrasi Project Operations gagal apabila anda menyiarkannya, kerana akaun hilang dimensi. Walau bagaimanapun, akaun yang hilang dimensi bukanlah akaun yang anda siarkan. |
| Pengurusan projek dan perakaunan | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Penapis **ToDate** dalam carian tidak dikosongkan apabila ia dialih **keluar daripada kotak dialog Pilih** pada **halaman Kos** siaran. |
| Pengurusan projek dan perakaunan | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Tetapkan semula semua pengedaran** gagal dan menunjukkan ralat untuk lembaran masa yang dicipta untuk projek jenis **Masa sahaja**. |
| Pengurusan projek dan perakaunan | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Projek** tidak boleh diedit pada invois vendor yang belum selesai apabila kategori perolehan diuntukkan kepada item. |
| Pengurusan projek dan perakaunan | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Anak tetingkap navigasi hilang jika anda tidak log masuk ke Project Operations Dataverse. |
| Pengurusan projek dan perakaunan | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Untuk transaksi pelarasan projek antara syarikat, terdapat isu-isu di syarikat destinasi. |
| Pengurusan projek dan perakaunan | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Kos yang komited untuk projek mengira kuantiti dan harga kos yang salah jika pesanan pembelian diproses oleh **proses** akhir tahun pesanan pembelian dalam lejar umum. |
| Pengurusan projek dan perakaunan | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Apabila pesanan pengeluaran projek yang mempunyai pesanan berkualiti dilaporkan selesai, ralat berikut berlaku: "Tiada transaksi maya yang ditandakan dengan transaksi inventori." |
| Pengurusan projek dan perakaunan | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Apabila invois akaun yang berkaitan dengan projek yang perlu dibayar disiarkan, ralat berikut berlaku: "Projek teks yang dikira - kos - item tidak wujud." |
| Pengurusan projek dan perakaunan | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Kos tidak langsung dua kali ganda apabila anda mengumpul pendapatan secara manual. |
| Pengurusan projek dan perakaunan | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Pendapatan terakru dan pengeposan WIP tidak menghasilkan transaksi. |
| Pengurusan projek dan perakaunan | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Pengaktifan harga belum selesai gagal untuk item kos standard apabila pesanan pembelian projek yang diterima wujud. |
| Pengurusan projek dan perakaunan | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai terbalik WIP daripada pengeposan invois berbeza daripada nilai WIP yang diposkan asal daripada entri masa. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Terdapat isu pengeposan untuk hasil invois projek dalam kes penahan yang digunakan di mana transaksi pada baucar tidak seimbang. |
| Pengurusan projek dan perakaunan | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Penciptaan anggaran selepas cadangan invois disiarkan menyekat import garisan pembetulan dalam Operasi Projek. |
| Pengurusan projek dan perakaunan | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pengubahsuaian rekod pencapaian invois sepenuhnya tidak boleh dilakukan. |
| Pengurusan projek dan perakaunan | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Apabila caj automatik digunakan, invois pelanggan antara syarikat untuk lembaran masa tidak dapat disiarkan dan mesej ralat ditunjukkan. |
| Pengurusan projek dan perakaunan | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamat pada subprojek tidak dikemas kini dengan betul. |
| Pengurusan projek dan perakaunan | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Harga kos pada keperluan item dikemas kini dengan harga belian untuk pesanan pembelian yang disatukan. |
| Pengurusan projek dan perakaunan | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Kos yang disiarkan tidak betul selepas harga pembelian dikemas kini dan parameter **Aktifkan pengurusan** perubahan didayakan. |
| Perjalanan dan Perbelanjaan | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua perbelanjaan pengguna boleh dilihat apabila anda mencari kategori dalam aplikasi mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang tidak betul pada transaksi vendor dan transaksi cukai jualan disiarkan dari perbelanjaan yang dibuat dari transaksi kad kredit. |
| Perjalanan dan Perbelanjaan | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Mesej amaran yang tidak berkaitan ditunjukkan apabila anda menyegar semula halaman laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pelulus interim yang salah digunakan apabila anda memadamkan pelulus interim dan kemudian menghantar semula melalui aliran kerja. |
| Perjalanan dan Perbelanjaan | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ralat pengeposan berlaku yang berkaitan dengan persediaan perbatuan. |
| Perjalanan dan Perbelanjaan | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Pengagihan tidak mengemas kini entiti undang-undang apabila transaksi yang tidak terikat ditambahkan semula pada laporan perbelanjaan atas perbelanjaan antara syarikat. |

### <a name="regulatory-updates"></a>Kemas kini kawal selia

Untuk maklumat tentang kemas kini kawal selia untuk aplikasi Kewangan dan Operasi, lihat [Kemas kini kawal selia](/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh log masuk ke Microsoft Dynamics Perkhidmatan Kitaran Hayat (LCS) dan menggunakan alat carian Isu untuk melihat kemas kini kawal selia yang dirancang. Carian isu membolehkan anda mencari mengikut negara atau rantau, jenis ciri dan keluaran.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
