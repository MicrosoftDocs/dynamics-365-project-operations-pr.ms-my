---
title: Invois projek proforma
description: Topik ini menyediakan maklumat tentang invois projek proforma dalam Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1b839c3e40ddcfe1f07b0330a78c42851140d4bf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004047"
---
# <a name="proforma-project-pnvoices"></a>Invois projek proforma

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Penginvoisan projek proforma memberikan tahap kedua kelulusan kepada pengurus projek sebelum mereka mencipta invois untuk pelanggan. Tahap pertama kelulusan dilengkapkan apabila entri masa, perbelanjaan dan bahan yang ahli pasukan projek serahkan telah diluluskan.

Pelaksanaan Ringan Dynamics 365 Project Operations tidak direka untuk menjana invois berhadapan pelanggan. Senarai berikut menunjukkan sebab invois tidak boleh dijana:

- Tidak mengandungi maklumat cukai.
- Tidak boleh menukar mata wang lain kepada mata wang invois.
- Tidak dapat memformatkan invois dengan betul untuk percetakan.

Sebaliknya, anda boleh menggunakan sistem kewangan atau perakaunan untuk mencipta invois berhadapan pelanggan yang menggunakan maklumat dalam cadangan invois yang dijana.

## <a name="creating-project-invoices"></a>Mencipta invois projek

Invois projek boleh dicipta satu pada satu masa atau secara pukal. Anda boleh menciptanya secara manual, atau ia boleh dikongfigurasikan agar ia boleh dijana dalam jalanan automatik.

### <a name="manually-create-project-invoices"></a>Cipta invois projek secara manual 

Pada halaman senarai **Kontrak Projek**, anda boleh mencipta invois projek secara berasingan untuk setiap kontrak projek atau anda boleh mencipta invois secara pukal untuk berbilang kontrak projek.

   - Untuk mencipta invois bagi kontrak projek tertentu, pada halaman senarai **Kontrak Projek**, buka kontrak projek dan kemudian pilih **Cipta Invois**.

   Invois dijana untuk semua transaksi untuk kontrak projek terpilih yang mempunyai status **Sedia untuk Invois**. Transaksi ini termasuk masa, perbelanjaan, bahan, pencapaian, baris kontrak berdasarkan produk dan garisan jurnal jualan belum dibilkan lain yang mungkin telah disahkan.

Untuk mencipta invois secara pukal:

1. Pada halaman senarai **Kontrak Projek**, pilih satu atau lebih kontrak projek untuk mencipta invois, dan kemudian pilih **Cipta Invois Projek**.
2. Satu mesej amaran menunjukkan bahawa mungkin terdapat penangguhan sebelum invois dicipta. Proses juga ditunjukkan. Pilih **OK** untuk tutup kotak mesej.

   Invois dijana untuk semua transaksi untuk baris kontrak yang mempunyai status **Sedia untuk Invois**. Transaksi ini termasuk masa, perbelanjaan, bahan, pencapaian, baris kontrak berdasarkan produk dan garisan jurnal jualan belum dibilkan lain yang mungkin telah disahkan.

3. Lihat invois yang dijana dengan pergi ke **Jualan** \> **Pengebilan** \> **Invois**. Anda akan melihat invois untuk setiap kontrak projek.

### <a name="set-up-automated-creation-of-project-invoices"></a>Sediakan penciptaan automatik bagi invois projek 

Ikuti langkah ini untuk mengkonfigurasikan jalanan invois automatik.

1. Pergi ke **Tetapan** \> **Kerja Kelompok**.
2. Cipta kerja kelompok dan namakannya **Project Operations Mencipta Invois**. Nama kerja kelompok mestilah memasukkan terma "Cipta Invois".
3. Dalam medan **Jenis kerja**, pilih **Tiada**. Secara lalai, **Kekerapan Harian** dan pilihan **Adalah Aktif** ditetapkan kepada **Ya**.
4. Pilih **Jalankan Aliran Kerja**. Dalam kotak dialog **Cari Rekod**, anda akan melihat aliran tugas berikut:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller**, kemudian pilih **Tambah**.
6. Dalam kotak dialog seterusnya, pilih **OK**. Aliran tugas **Tidur** diikuti dengan aliran tugas **Proses**.

    Anda juga boleh memilih **ProcessRunner** dalam langkah 5. Kemudian, apabila anda pilih **OK**, aliran tugas **Proses** diikuti oleh aliran kerja **Tidur**.

Aliran kerja **ProcessRunCaller** dan **ProcessRunner** mencipta invois. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** ialah aliran kerja yang mencipta invois. Aliran kerja ini memeriksa semua baris kontrak yang memerlukan penciptaan invois, kemudian cipta invois. Untuk menentukan baris kontrak yang memerlukan penciptaan invois, aliran kerja melihat pada tarikh jalanan invois untuk baris kontrak. Jika baris kontrak milik satu kontrak yang mempunyai tarikh jalanan invois sama, transaksi digabungkan ke dalam satu invois yang mempunyai dua baris invois. Jika tiada transaksi untuk penciptaan invois, tiada invois akan dicipta.

Selepas **ProcessRunner** selesai berjalan, ia memanggil **ProcessRunCaller**, memberikan masa akhir, dan ditutup. **ProcessRunCaller** kemudian memulakan pemasa yang berjalan 24 jam dari tarikh akhir khusus. Pada penghujung pemasa, **ProcessRunCaller** ditutup.

Kerja proses kelompok untuk mencipta invois adalah kerja berulang. Jika proses kelompok ini berjalan banyak kali, berbilang tika kerja dicipta dan boleh menyebabkan ralat. Untuk mengatasi isu ini, mulakan proses kelompok sekali sahaja, dan hanya mulakan semula jika ia berhenti berjalan.

> [!NOTE]
> Penginvoisan kelompok hanya berjalan untuk baris kontrak projek yang dikonfigurasikan oleh jadual invois. Baris kontrak dengan kaedah pengebilan harga tetap mesti mempunyai pencapaian yang dikonfigurasikan. Baris kontrak projek dengan kaedah pengebilan masa dan bahan akan memerlukan persediaan jadual invois berdasarkan tarikh. Perkara yang sama digunakan pada baris kontrak berasaskan projek.      
 
### <a name="edit-a-draft-invoice"></a>Edit invois draf

Apabila anda mencipta invois projek draf, semua transaksi jualan belum dibilkan yang dicipta apabila entri masa dan perbelanjaan diluluskan ditarik ke dalam invois. Anda boleh membuatk pelarasan berikut semasa invois masih dalam peringkat draf:

- Padam atau edit butiran baris invois.
- Edit atau selaraskan kuantiti dan jenis pengebilan.
- Terus menambah masa, perbelanjaan, bahan dan yuran sebagai transaksi dalam invois. Anda boleh menggunakan ciri ini jika baris invois dipetakan kepada baris kontrak yang membenarkan kelas transaksi ini.

Pilih **Sahkan** untuk mengesahkan invois. Tindakan ini merupakan tindakan sehala. Apabila anda memilih **Sahkan**, invois menjadikan baca sahaja dan mencipta aktual jualan dibilkan daripada setiap butiran baris invois untuk setiap baris invois. Jika butiran baris invois merujuk kepada aktual jualan belum dibilkan, aktual jualan belum dibilkan akan terbalik. Sebarang butiran baris invois yang dicipta daripada entri masa, perbelanjaan atau penggunaan bahan akan merujuk kepada aktual jualan belum dibilkan. Sistem integrasi lejar umum boleh menggunakan pembalikan ini untuk menterbalikkan kerja projek dalam kemajuan (WIP) untuk tujuan perakaunan.

### <a name="correct-a-confirmed-invoice"></a>Betulkan invois yang disahkan

Invois yang disahkan boleh diedit. Apabila anda membetulkan invois disahkan, invois pembetulan draf baharu dicipta. Disebabkan anggapan bahawa anda mahu menterbalikkan semua transaksi dan kuantiti daripada invois asal, invois pembetulan ini menyertakan semua transaksi daripada invois asal dan semua kuantiti padanya ialah sifar.

Jika terdapat transaksi yang tidak memerlukan pembetulan, anda boleh mengalih keluar transaksi daripada invois pembetulan draf. Jika anda mahu membalikkan atau mengembalikan hanya separuh kuantiti, anda boleh mengedit medan **Kuantiti** pada butiran baris. Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal. Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,

Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta. Jika kuantiti telah dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta. Contohnya, jika jualan dibilkan asal adalah untuk lapan jam dan butiran baris invois pembetulan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:

- Aktual jualan dibilkan untuk enam jam.
- Aktual jualan belum dibilkan untuk baki dua jam. Transaksi ini boleh dibilkan kemudian atau ditanda sebagai tidak boleh dituntut, bergantung pada rundingan dengan pelanggan.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
