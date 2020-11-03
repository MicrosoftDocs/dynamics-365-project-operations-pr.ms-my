---
title: Cipta invois proforma manual
description: Topik ini menyediakan maklumat tentang mencipta invois proforma.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 203b8a057d8ef3b699b20c4303061e622d2a3acd
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081458"
---
# <a name="create-a-manual-proforma-invoice"></a>Cipta invois proforma manual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Penginvoisan memberikan pengurus projek kelulusan tahap kedua sebelum mereka mencipta invois untuk pelanggan. Tahap pertama kelulusan dilengkapkan apabila entri masa dan perbelanjaan yang ahli pasukan projek serahkan telah diluluskan.

Dynamics 365 Project Operations tidak direka bentuk untuk menjana invois bersemuka dengan pelanggan untuk alasan berikut:

- Ia tidak mengandungi maklumat cukai.
- Ia tidak boleh menukar mata wang lain kepada mata wang penginvoisan menggunakan kadar tukaran yang dikongfigurasikan dengan betul.
- Ia tidak boleh memformatkan invois dengan betul agar ia boleh dicetak.

Sebaliknya, anda boleh menggunakan sistem kewangan atau perakaunan untuk mencipta invois bersemuka dengan pelanggan yang menggunakan maklumat daripada cadangan invois yang dijana.

## <a name="creating-project-invoices"></a>Mencipta invois projek

Invois projek boleh dicipta satu pada satu masa atau secara pukal. Anda boleh menciptanya secara manual, atau ia boleh dikongfigurasikan agar ia boleh dijana dalam jalanan automatik.

### <a name="manually-create-project-invoices"></a>Cipta invois projek secara manual 

Dari halaman senarai **Kontrak Projek** , anda boleh mencipta invois projek secara berasingan untuk setiap kontrak projek, atau anda boleh mencipta invois secara pukal untuk berbilang kontrak projek.

Ikuti langkah ini untuk mencipta invois untuk kontrak projek khusus.

- Dalam halaman senarai **Kontrak Projek** , buka kontrak projek, kemudian pilih **Cipta Invois**.

    Invois dijana untuk semua transaksi untuk kontrak projek terpilih yang mempunyai status **Sedia untuk Invois**. Transaksi ini termasuklah masa, perbelanjaan, pencapaian, dan baris kontrak berasaskan produk.

Ikuti langkah-langkah ini untuk mencipta invois secara pukal.

1. Dalam halaman senarai **Kontrak Projek** , pilih satu atau lebih kontrak projek yang anda mesti cipta invois, kemudian pilih **Cipta Invois Projek**.

    Satu mesej amaran menunjukkan bahawa mungkin terdapat penangguhan sebelum invois dicipta. Proses juga ditunjukkan.

2. Pilih **OK** untuk tutup kotak mesej.

    Invois dijana untuk semua transaksi untuk baris kontrak yang mempunyai status **Sedia untuk Invois**. Transaksi ini termasuklah masa, perbelanjaan, pencapaian, dan baris kontrak berasaskan produk.

3. Untuk melihat invois yang dijana, pergi ke **Jualan** \> **Pengebilan** \> **Invois**. Anda akan melihat invois untuk setiap kontrak projek.

### <a name="set-up-automated-creation-of-project-invoices"></a>Sediakan penciptaan automatik bagi invois projek 

Ikuti langkah ini untuk mengkonfigurasikan jalanan invois automatik.

1. Pergi ke **Tetapan** \> **Kerja Kelompok**.
2. Cipta kerja kelompok dan namakannya **Project Operations Mencipta Invois**. Nama kerja kelompok mestilah memasukkan terma "Cipta Invois".
3. Dalam medan **Jenis kerja** , pilih **Tiada**. Secara lalai, **Kekerapan Harian** dan pilihan **Adalah Aktif** ditetapkan kepada **Ya**.
4. Pilih **Jalankan Aliran Kerja**. Dalam kotak dialog **Cari Rekod** , anda akan melihat tiga aliran tugas:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pilih **ProcessRunCaller** , kemudian pilih **Tambah**.
6. Dalam kotak dialog seterusnya, pilih **OK**. Aliran tugas **Tidur** diikuti dengan aliran tugas **Proses**.

    Anda juga boleh memilih **ProcessRunner** dalam langkah 5. Kemudian, apabila anda pilih **OK** , aliran tugas **Proses** diikuti oleh aliran kerja **Tidur**.

Aliran kerja **ProcessRunCaller** dan **ProcessRunner** mencipta invois. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** ialah aliran kerja yang sebenarnya mencipta invois. Ia merangkumi semua baris kontrak yang perlu dicipta invois, dan ia mencipta invois untuk baris tersebut. Untuk menentukan baris kontrak yang perlu dicipta invois, kerja dilihat pada tarikh jalanan invois untuk baris kontrak. Jika baris kontrak milik satu kontrak yang mempunyai tarikh jalanan invois sama, transaksi digabungkan ke dalam satu invois yang mempunyai dua baris invois. Jika tiada transaksi untuk dicipta invois, kerja melangkau penciptaan invois.

Selepas **ProcessRunner** selesai berjalan, ia memanggil **ProcessRunCaller** , memberikan masa akhir, dan ditutup. **ProcessRunCaller** kemudian memulakan pemasa yang berjalan 24 jam dari tarikh akhir khusus. Pada penghujung pemasa, **ProcessRunCaller** ditutup.

Kerja proses kelompok untuk mencipta invois adalah kerja berulang. Jika proses kelompok ini berjalan banyak kali, berbilang tika kerja dicipta dan menyebabkan ralat. Maka, anda perlu memulakan proses kelompol hanya satu kali, dan anda hendaklah mulakan semula jika ia berhenti berjalan.

> [!NOTE]
> Penginvoisan kelompok hanya berjalan untuk baris kontrak projek yang dikonfigurasikan oleh jadual invois. Baris kontrak dengan kaedah pengebilan harga tetap mesti mempunyai pencapaian yang dikonfigurasikan. Baris kontrak projek dengan kaedah pengebilan masa dan bahan akan memerlukan persediaan jadual invois berdasarkan tarikh. Perkara yang sama digunakan pada baris kontrak berasaskan projek.      
 
### <a name="edit-a-draft-invoice"></a>Edit invois draf

Apabila anda mencipta invois projek draf, semua transaksi jualan belum dibilkan yang dicipta apabila entri masa dan perbelanjaan diluluskan ditarik ke dalam invois. Anda boleh membuatk pelarasan berikut semasa invois masih dalam peringkat draf:

- Padam atau edit butiran baris invois.
- Edit atau selaraskan kuantiti dan jenis pengebilan.
- Terus menambah masa, perbelanjaan, dan yuran sebagai transaksi dalam invois. Anda boleh menggunakan ciri ini jika baris invois dipetakan kepada baris kontrak yang membenarkan kelas transaksi ini.

Pilih **Sahkan** untuk mengesahkan invois. Tindakan Sahkan adalah tindakah satu arah. Apabila anda pilih **Sahkan** , sistem menjadikan invois baca sahaja dan mencipta aktual jualan dibilkan dari setiap butiran baris invois untuk setiap baris invois. Jika butiran baris invois merujuk kepada aktual jualan belum dibilkan, sistem juga membalikkan aktual jualan belum dibilkan. (Sebarang butiran baris invois yang dicipta dari entri masa atau perbelanjaan akan merujuk kepada aktual jualan belum dibilkan). Sistem integrasi lejar am boleh menggunakan balikan ini untuk membalikkan projek yang sedang berjalan untuk tujuan perakaunan.

### <a name="correct-a-confirmed-invoice"></a>Betulkan invois yang disahkan

Invois yang disahkan boleh diedit (dibetulkan). Apabila anda membetulkan invois disahkan, invois pembetulan draf baharu dicipta. Disebabkan anggapan bahawa anda mahu membalikkan semua transaksi dan kuantiti daripada invois asal, invois pembetulan ini memasukkan semua transaksi daripada invois asal dan semua kuantiti padanya adalah 0 (sifar).

Jika sebarang transaksi tidak memerlukan pembetulan, anda boleh mengalih keluar daripada invois pembetulan draf. Jika anda mahu membalikkan atau mengembalikan hanya separuh kuantiti, anda boleh mengedit medan **Kuantiti** pada butiran baris. Jika anda membuka butiran baris invosi, anda boleh melihat kuantiti invois asal. Anda kemudian boleh mengedit kuantiti invois semasa, agar ia kurang daripada atau lebih daripada kuantiti invois asal,

Apabila anda mengesahkan invois pembetulan, aktual jualan dibilkan asal dibalikkan, dan aktual jualan dibilkan baharu dicipta. Jika kuantiti dikurangkan, perbezaan akan menyebabkan aktual jualan belum dibilkan baharu dicipta juga. Contohnya, jika jualan dibilkan asal adalah untuk 8 jam dan butiran baris invois yang diperbetulkan mempunyai kuantiti berkurangan sebanyak enam jam, baris jualan dibilkan asal dibalikkan dan dua aktual baharu dicipta:

- Aktual jualan dibilkan untuk enam jam.
- Aktual jualan belum dibilkan untuk baki dua jam. Transaksi ini boleh sama ada dibilkan kemudian atau ditanda sebagai bukan boleh dicaj, bergantung pada rundingan dengan pelanggan.
