---
title: Perkara baharu atau perubahan dalam Project Operations, Oktober 2021 untuk senario berasaskan stok/pengeluaran
description: Artikel ini memberikan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Oktober 2021 bagi Project Operations untuk senario berasaskan stok/pengeluaran.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029954"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Perkara baharu atau perubahan dalam Project Operations, Oktober 2021 untuk senario berasaskan stok/pengeluaran

_**Digunakan Pada:** Project Operations untuk senario berasaskan stok/pengeluaran_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.22
 
## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
|--------------|------------------|----------------|
| Pengurusan projek dan perakaunan | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Kerja projek dalam proses (WIP) dan jumlah hasil terakru tidak boleh dibalikkan dengan betul apabila invois pelanggan antara syarikat disiarkan. |
| Pengurusan projek dan perakaunan | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Fungsi **Halang penutupan projek jika urus niaga terbuka wujud** tidak berfungsi. |
| Pengurusan projek dan perakaunan | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Pengelasan pengebilan pada invois teks bebas tidak mengisi dimensi secara automatik daripada projek apabila fungsi tersebut didayakan. |
| Pengurusan projek dan perakaunan | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dalam senario bukan antara syarikat, WIP dan jumlah hasil terakru tidak boleh dibalikkan dengan betul apabila invois projek disiarkan. |
| Pengurusan projek dan perakaunan | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Nilai debit dan kredit ditukar apabila tambahan Microsoft Excel digunakan dengan jurnal perbelanjaan Projek dan medan **Jenis akaun ofset** ditetapkan kepada **Projek**. |
| Pengurusan projek dan perakaunan | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Jumlah yang dicatatkan dalam urus niaga projek telah terlebih catat pada pesanan belian projek yang termasuk item berstok dan yang mempunyai jumlah cukai tidak boleh ditolak apabila **UseTax** ditandakan. |
| Pengurusan projek dan perakaunan | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem membahagikan jumlah antara laporan keuntungan dan kerugian projek dan laporan WIP projek. |
| Pengurusan projek dan perakaunan | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventori dalam tangan adalah salah selepas sebahagian keperluan item dikembalikan telah dilaraskan. |
| Pengurusan projek dan perakaunan | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nama sumber akan diduplikasi dalam Project Operations apabila diedit dalam Microsoft Project. |
| Pengurusan projek dan perakaunan | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Laporan perbelanjaan antara syarikat yang mempunyai Akaun belum bayar antara syarikat yang belum selesai kos invois vendor telah ditugaskan terlebih dahulu kepada jenis penyiaran **Kos WIP projek**. Walau bagaimanapun, semasa pemprosesan, kos berkaitan anggaran disiarkan kepada jenis penyiaran **Kos projek** dan bukannya jenis penyiaran **Kos antara syarikat** yang dijangkakan. |
| Pengurusan projek dan perakaunan | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Hasil pengekalan vendor dalam urus niaga perbelanjaan projek tidak ditunjukkan. |
| Pengurusan projek dan perakaunan | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Lebaran masa mesti membundarkan jumlah urus niaga dalam mata wang urus niaga kepada bilangan tempat perpuluhan yang ditentukan pada semua pengedaran perakaunan dan entri peruntukan jurnal umum. |
| Pengurusan projek dan perakaunan | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Kuantiti keperluan item projek dikemas kini secara automatik apabila pesanan yang dirancang adalah kukuh. |
| Pengurusan projek dan perakaunan | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Bilangan baucar, baki vendor jenis urus niaga dan nombor akaun tidak boleh dibalikkan pada invois prabayaran bagi pesanan belian. |
| Pengurusan projek dan perakaunan | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Invois vendor antara syarikat rosak apabila penyepaduan invois vendor dihidupkan. |
| Pengurusan projek dan perakaunan | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Apabila anda mencipta jurnal perbelanjaan Projek, jumlah kos ditunjukkan dalam medan **Kredit**. |
| Pengurusan projek dan perakaunan | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Terma pembayaran pada invois projek tidak berfungsi seperti yang dijangkakan. |
| Pengurusan projek dan perakaunan | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Baucar lembaran masa mungkin diguna semula apabila urutan nombor ditetapkan sebagai berterusan. |
| Pengurusan projek dan perakaunan | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PERANCIS: Logik **Jumlah pengekalan manual** tidak sepadan logik **Jumlah pengekalan automatik** dalam cadangan invois kontrak Projek. |
| Pengurusan projek dan perakaunan | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Apabila pengekalan vendor dikeluarkan, penyiaran baucar mempunyai baris tambahan yang salah. |
| Pengurusan projek dan perakaunan | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Apabila medan **Tarikh invois** pada halaman **Cipta cadangan invois** ditukar, ralat berikut mungkin berlaku: "Rujukan objek tidak ditetapkan kepada tika objek." |
| Pengurusan projek dan perakaunan | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ralat berlaku apabila anda cuba untuk meluluskan lembaran masa daripada aliran kerja **TSLine**, dan terdapat dasar lembaran masa untuk hari Sabtu dan Ahad. |
| Pengurusan projek dan perakaunan | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Jenis item projek baki mula dikecualikan daripada **Ringkasan urus niaga cadangan invois** apabila invois jumlah cadangan invois dikira. |
| Pengurusan projek dan perakaunan | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Jika kos penggunaan pada pesanan pengeluaran projek ialah 0 (sifar), ralat berikut berlaku apabila anda cuba untuk menganggarkan: "Percubaan untuk membahagi dengan sifar." |
| Pengurusan projek dan perakaunan | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikasi mudah alih Lembaran Masa Projek untuk Android berhenti memberikan respons. Isu berkaitan dengan **TimeEntryDataManager ArgumentNullException**. |
| Pengurusan projek dan perakaunan | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Jurnal penyepaduan Project Operations gagal apabila anda menyiarkannya kerana akaun tersebut tiada dimensi. Walau bagaimanapun, akaun yang tiada dimensi tidak mempunyai akaun yang anda siarkan. |
| Pengurusan projek dan perakaunan | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Penapis **ToDate** dalam carian tidak dikosongkan apabila dialih keluar daripada kotak dialog **Pilih** pada halaman **Kos siaran**. |
| Pengurusan projek dan perakaunan | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Tetapkan semula semua pengedaran** gagal dan menunjukkan ralat untuk lembaran masa yang dicipta untuk projek jenis **Masa sahaja**. |
| Pengurusan projek dan perakaunan | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Projek** tidak boleh diedit pada invois vendor yang belum selesai apabila kategori perolehan diuntukkan untuk item. |
| Pengurusan projek dan perakaunan | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Tiada anak tetingkap navigasi jika anda tidak didaftar masuk ke Project Operations Dataverse. |
| Pengurusan projek dan perakaunan | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Untuk urus niaga pelarasan projek antara syarikat, terdapat isu dalam syarikat destinasi. |
| Pengurusan projek dan perakaunan | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Kos komited untuk projek mengira kuantiti dan harga kos yang salah jika pesanan belian diproses oleh **Proses akhir tahun pesanan belian** dalam lejar Umum. |
| Pengurusan projek dan perakaunan | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Apabila pesanan pengeluaran projek yang mempunyai pesanan kualiti dilaporkan sebagai selesai, ralat berikut berlaku: "Tiada urus niaga maya yang bertanda dengan urus niaga inventori." |
| Pengurusan projek dan perakaunan | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Apabila invois Akaun belum bayar berkaitan projek disiarkan, ralat berikut berlaku: "Projek teks yang ditunjukkan - kos - item tidak wujud." |
| Pengurusan projek dan perakaunan | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Kos tidak langsung akan berganda apabila anda mengakru hasil secara manual. |
| Pengurusan projek dan perakaunan | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Hasil terakru dan penyiaran WIP tidak akan menghasilkan urus niaga. |
| Pengurusan projek dan perakaunan | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Pengaktifan harga yang belum selesai gagal untuk item kos standard apabila pesanan belian projek yang diterima wujud. |
| Pengurusan projek dan perakaunan | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Nilai terbalik WIP daripada penyiaran invois berbeza daripada nilai asal WIP yang disiarkan daripada entri masa. |
| Pengurusan projek dan perakaunan | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Terdapat isu penyiaran untuk hasil diinvois projek dalam kes retainer yang digunakan apabila urus niaga pada baucar tidak seimbang. |
| Pengurusan projek dan perakaunan | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Penciptaan anggaran selepas cadangan invois disiarkan untuk menyekat import baris pembetulan dalam Project Operations. |
| Pengurusan projek dan perakaunan | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Pengubahsuaian rekod pencapaian invois penuh tidak boleh dilakukan. |
| Pengurusan projek dan perakaunan | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Apabila caj automatik digunakan, invois pelanggan antara syarikat untuk lembaran masa tidak boleh disiarkan dan mesej ralat ditunjukkan. |
| Pengurusan projek dan perakaunan | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alamat pada subprojek tidak dikemas kini dengan betul. |
| Pengurusan projek dan perakaunan | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Harga kos untuk keperluan item dikemas kini dengan harga belian untuk pesanan belian yang disatukan. |
| Pengurusan projek dan perakaunan | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Kos yang disiarkan adalah salah selepas harga belian dikemas kini dan parameter **Aktifkan pengurusan perubahan** didayakan. |
| Perjalanan dan Perbelanjaan | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua perbelanjaan pengguna boleh dilihat apabila anda mencari kategori dalam aplikasi mudah alih Perbelanjaan. |
| Perjalanan dan Perbelanjaan | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah salah pada urus niaga vendor dan urus niaga cukai jualan disiarkan daripada perbelanjaan yang dicipta daripada urus niaga kad kredit. |
| Perjalanan dan Perbelanjaan | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Mesej amaran yang tidak relevan ditunjukkan apabila anda menyegar semula halaman laporan perbelanjaan. |
| Perjalanan dan Perbelanjaan | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pelulus interim yang salah digunakan apabila anda memadamkan pelulus interim, kemudian menyerahkan semula melalui aliran kerja. |
| Perjalanan dan Perbelanjaan | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ralat penyiaran berlaku yang berkaitan dengan persediaan perbatuan. |
| Perjalanan dan Perbelanjaan | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Pengedaran tidak mengemas kini entiti sah apabila transaksi yang belum dilampirkan ditambahkan semula pada laporan perbelanjaan pada perbelanjaan antara syarikat. |

### <a name="regulatory-updates"></a>Kemas kini kawal selia

Untuk mendapatkan maklumat tentang kemas kini kawal selia untuk aplikasi kewangan dan operasi, lihat [Kemas kini kawal selia](/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh mendaftar masuk ke Microsoft Dynamics Lifecycle Services (LCS) dan menggunakan Alat carian isu untuk melihat kemas kini kawal selia yang dirancang. Carian isu membolehkan anda membuat carian mengikut negara atau rantau, jenis ciri dan keluaran.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
