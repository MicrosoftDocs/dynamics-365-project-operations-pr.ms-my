---
title: Sebut harga - Konsep utama - ringan
description: Artikel ini memberikan maklumat tentang menggunakan sebut harga projek dalam Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8c2f009b7a0bebbf6a49bf942dd19f97205072e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916989"
---
# <a name="concepts-unique-to-project-quotes"></a>Konsep unik untuk Sebut harga projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_


Berikut ialah konsep utama untuk diketahui sebelum anda mula menggunakan sebut harga projek dalam Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unit pengkontrakan

Unit pengkontrakan mewakili divisyen atau amalan yang memiliki penghantaran projek. Anda boleh menyediakan kos sumber untuk setiap unit pengkontrakan. Apabila anda menentukan kos sumber untuk sumber dalam unit pengkontrakan, anda juga akan dapat menyediakan kadar kos yang berbeza untuk sumber yang unit pengkontrakan ini pinjam daripadanya atau divisyen atau amalan lain dalam perusahaan. Ini dirujuk sebagai harga pindahan, peminjaman sumber atau harga pertukaran. Apabila anda menyediakan kos peminjaman sumber daripada divisyen lain, anda juga boleh memilih untuk menyediakan kadar kos tersebut dalam mata wang sumber yang memberi pinjaman.

## <a name="cost-currency"></a>Mata wang kos

Mata wang kos dalam Project Operations ialah mata wang yang digunakan untuk melaporkan kos. Mata wang ini diperoleh daripada mata wang yang dilampirkan pada medan **Unit pengkontrakan** pada sebut harga, kontrak dan projek. Kos boleh dilog dalam sebarang mata wang terhadap projek. Walau bagaimanapun, terdapat pertukaran mata wang daripada kos mata wang telah direkodkan, untuk mata wang kos projek.

Disebabkan kadar pertukaran dalam platform CDS tidak boleh menjadi berkesan tarikh, jumlah pada skrin untuk kos mungkin berubah dari masa ke masa jika anda mengemas kini kadar pertukaran mata wang. Walau bagaimanapun, kos yang direkodkan dalam pangkalan data kekal tidak berubah kerana amaun disimpan dalam mata wang yang dikenakan kepada mereka.

## <a name="sales-currency"></a>Mata wang jualan

Mata wang jualan dalam Project Operations ialah mata wang yang digunakan dalam amaun jualan anggaran dan sebenar yang direkodkan dan ditunjukkan. Ia juga merupakan mata wang yang digunakan untuk menginvois urus niaga dengan pelanggan. Pada sebut harga projek, nilai lalai mata wang jualan adalah daripada rekod pelanggan atau akaun dan boleh diubah apabila sebut harga dicipta. Selepas sebut harga disimpan, mata wang jualan tidak boleh diubah. Nilai lalai senarai harga produk dan projek berdasarkan mata wang jualan bagi sebut harga.

Tidak seperti kos, nilai jualan hanya boleh direkodkan dalam mata wang Jualan.

## <a name="billing-method"></a>Kaedah pengebilan

Projek biasanya mempunyai yuran tetap dan model pengkontrakan berdasarkan penggunaan. Ini diwakili dalam Project Operations sebagai **Kaedah Pengebilan** dan mempunyai dua nilai, masa dan bahan serta harga tetap.

- **Masa dan bahan:** Ini ialah model pengkontrakan berdasarkan penggunaan iaitu setiap kos yang dikenakan disandarkan oleh hasil yang sepadan. Ketika anda menganggarkan atau mengenakan lebih banyak kos, jualan anggaran dan sebenar yang sepadan juga akan meningkat. Anda boleh menentukan tidak melebihi had pada baris sebut harga yang mempunyai kaedah pengebilan ini. Ini akan mengehadkan hasil sebenar. Anggaran hasil tidak dipengaruhi oleh tidak melebihi had.
- **Harga tetap:** Ini ialah model kontrak yuran tetap yang menunjukkan nilai jualan tidak akan bergantung kepada kos yang dikenakan. Nilai jualan adalah tetap dan tidak berubah ketika anda menganggarkan atau mengenakan lebih banyak kos.

## <a name="project-price-lists"></a>Senarai harga projek

Senarai harga projek ialah senarai harga yang digunakan untuk harga lalai, bukan kadar kos, untuk masa, perbelanjaan dan komponen berkaitan projek yang lain. Mungkin terdapat berbilang senarai harga dan setiap senarai boleh mempunyai keberkesanan tarikhnya sendiri untuk setiap sebut harga projek. Penindihan keberkesanan tarikh pada senarai harga projek tidak disokong dalam Project Operations.

## <a name="product-price-lists"></a>Senarai harga produk

Senarai harga produk ialah senarai harga yang digunakan untuk harga lalai, bukan kadar kos, untuk baris berdasarkan produk pada sebut harga. Hanya terdapat satu senarai harga produk setiap sebut harga.

## <a name="transaction-classes"></a>Kelas transaksi

Project Operations menyokong empat jenis kelas transaksi:

- Masa
- Perbelanjaan
- Bahan
- Yuran

Nilai kos dan jualan boleh dianggarkan dan dikenakan pada kelas transaksi Masa, Perbelanjaan dan Bahan. Yuran ialah hanya hasil kelas transaksi.

## <a name="work-entities-and-billing-entities"></a>Entiti kerja dan entiti pengebilan

Entiti yang mewakili kerja ialah Projek dan Tugas. Entiti yang mewakili pengebilan ialah baris Sebut Harga dan baris Kontrak. Anda boleh memautkan entiti kerja yang berbeza kepada pilihan pengebilan dengan mengaitkannya dengan baris Sebut Harga atau Kontrak.

## <a name="multi-customer-deals"></a>Urus niaga berbilang pelanggan

Urus niaga berbilang pelanggan berlaku apabila terdapat lebih daripada satu pelanggan untuk diinvoiskan. Contoh biasa bagi perkara ini termasuk:

- **Perusahaan OEM dan rakan kongsinya:** Rakan kongsi dan penjual menjual produk dengan perkhidmatan ditambahkan nilai. Ini biasanya senario yang semasa urus niaga tertentu dengan pelanggan berlaku, OEM menawarkan untuk membiayai bahagian projek. 

- **Projek sektor awam:** Berbilang jabatan kerajaan tempatan bersetuju untuk membiayai projek dan diinvoiskan mengikut pecahan yang dipersetujui sebelumnya. Contohnya, unit pentadbiran sekolah tempatan dan jabatan kerajaan bandar atau tempatan bersetuju untuk membiayai pembinaan kolam renang.

## <a name="invoice-schedules"></a>Jadual invois

Jadual invois adalah khusus untuk setiap baris sebut harga dan juga pilihan. Jadual invois dicipta berdasarkan tarikh mula dan tamat tertentu dan kekerapan invois. Jadual invois digunakan dalam peringkat kontrak apabila proses ciptaan invois automatik dikonfigurasikan. Dalam peringkat sebut harga, jadual adalah pilihan. Apabila jadual invois dicipta dalam peringkat **Sebut Harga**, ia disalin kepada kontrak projek yang dicipta apabila sebut harga projek dimenangi.

## <a name="changes-from-dynamics-365-sales-quote"></a>Perubahan daripada sebut harga Dynamics 365 Sales:

Sebut harga Project Operations dibina pada sebut harga Dynamics 365 Sales. Walau bagaimanapun, terdapat beberapa perbezaan yang penting dalam kefungsian yang patut anda ketahui:

- Tindakan **Semak Semula** dan **Aktifkan** tidak disokong.
- Sebut harga Project Operations mempunyai dua jenis baris yang berbeza. Satu adalah untuk projek dan satu lagi untuk produk.
- Sebut harga Project Operations mempunyai borang dan elemen UI, peraturan perniagaan, logik perniagaan dalam pasang masuk dan skrip bahagian klien mereka sendiri yang menjadikannya unik daripada sebut harga Sales.

Untuk sebab ini, penggunaan sebut harga Sales dan sebut harga Project Operations secara bergantian tidak disyorkan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
