---
title: Konsep unik untuk sebut harga berdasarkan projek
description: Artikel ini menyediakan maklumat tentang petikan projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824339"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konsep unik untuk sebut harga berdasarkan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Sebelum anda mula menggunakan sebut harga projek dalam Microsoft Dynamics 365 Project Operations, anda harus mengetahui konsep utama berikut.

## <a name="owning-company"></a>Syarikat pemilikan

Syarikat yang memiliki mewakili entiti undang-undang yang memiliki penghantaran projek. Pelanggan pada sebut harga harus menjadi pelanggan yang sah dalam entiti undang-undang tersebut dalam aplikasi kewangan dan operasi. Mata wang syarikat yang memiliki dan mata wang unit kontrak yang dipilih pada sebut harga berasaskan projek mesti sepadan.

## <a name="contracting-unit"></a>Unit pengkontrakan

Unit kontrak mewakili bahagian atau amalan yang memiliki penyampaian projek. Anda boleh menyediakan kos sumber untuk setiap unit pengkontrakan. Apabila anda menentukan kos sumber untuk sumber dalam unit kontrak, anda boleh menetapkan kadar kos yang berbeza untuk sumber yang dipinjam oleh unit kontrak daripada, atau untuk bahagian atau amalan lain dalam perusahaan. Kadar kos ini dirujuk sebagai harga pemindahan, pinjaman sumber, atau harga pertukaran. Apabila anda menubuhkan kos meminjam sumber dari bahagian lain, anda boleh menetapkan kadar kos dalam mata wang bahagian pinjaman.

## <a name="cost-currency"></a>Mata wang kos

Mata wang kos dalam Operasi Projek adalah mata wang yang kos dilaporkan. Mata wang ini diperoleh daripada mata wang yang dilampirkan pada medan unit **Kontrak pada** sebut harga, kontrak dan projek. Kos terhadap projek boleh direkodkan dalam mana-mana mata wang. Walau bagaimanapun, terdapat penukaran mata wang dari mata wang yang kosnya direkodkan dalam mata wang kos projek.

Oleh kerana kadar pertukaran pada platform tidak boleh berkuat kuasa tarikh, jumlah kos pada Dataverse skrin mungkin berubah dari semasa ke semasa jika anda mengemas kini kadar pertukaran mata wang. Walau bagaimanapun, kos yang direkodkan dalam pangkalan data kekal tidak berubah, kerana jumlahnya disimpan dalam mata wang yang mereka tanggung.

## <a name="sales-currency"></a>Mata wang jualan

Mata wang jualan dalam Operasi Projek adalah mata wang yang anggaran dan jumlah jualan sebenar direkodkan dan ditunjukkan dalam. Ia juga merupakan mata wang yang diinvois oleh pelanggan untuk perjanjian itu. Untuk sebut harga projek, mata wang jualan lalai ditetapkan daripada rekod pelanggan atau akaun dan ia boleh diubah apabila sebut harga dibuat. Walau bagaimanapun, mata wang jualan tidak boleh diubah selepas sebut harga disimpan. Senarai harga produk dan projek lalai ditetapkan berdasarkan mata wang jualan sebut harga.

Tidak seperti kos, nilai jualan boleh direkodkan **hanya** dalam mata wang jualan.

## <a name="billing-method"></a>Kaedah pengebilan

Projek biasanya mempunyai model kontrak yuran tetap dan berasaskan penggunaan. Dalam Operasi Projek, model kontrak projek diwakili oleh kaedah pengebilan. Kaedah pengebilan mempunyai dua nilai: masa dan bahan dan harga tetap.

- **Masa dan bahan** - Model kontrak berasaskan penggunaan di mana setiap kos yang ditanggung disokong oleh pendapatan yang sepadan. Ketika anda menganggarkan atau mengenakan lebih banyak kos, jualan anggaran dan aktual yang sepadan juga akan meningkat. Anda boleh menentukan tidak melebihi had pada baris sebut harga yang mempunyai kaedah pengebilan ini. Dengan cara ini, anda boleh mengehadkan pendapatan sebenar. Anggaran pendapatan tidak terjejas oleh had tidak melebihi had.
- **Harga**  tetap- Model kontrak yuran tetap di mana nilai jualan adalah bebas daripada kos yang ditanggung. Nilai jualan adalah tetap dan tidak berubah ketika anda menganggarkan atau mengenakan lebih banyak kos.

## <a name="project-price-lists"></a>Senarai harga projek

Senarai harga projek ialah senarai harga yang digunakan untuk memasukkan harga lalai, bukan kadar kos, untuk masa, perbelanjaan dan komponen berkaitan projek lain. Mungkin terdapat berbilang senarai harga dan setiap senarai boleh mempunyai keberkesanan tarikhnya sendiri untuk setiap sebut harga projek. Operasi Projek tidak menyokong kesan tarikh bertindih untuk senarai harga projek.

## <a name="product-price-lists"></a>Senarai harga produk

Senarai harga produk adalah senarai harga yang digunakan untuk memasukkan harga lalai, bukan kadar kos, untuk baris berasaskan produk pada sebut harga. Terdapat hanya satu senarai harga produk bagi setiap sebut harga.

## <a name="transaction-classes"></a>Kelas transaksi

Project Operations menyokong empat jenis kelas transaksi:

- Masa
- Perbelanjaan
- Bahan
- Yuran

Kos dan nilai jualan boleh dianggarkan dan ditanggung pada **kelas** transaksi Masa, Perbelanjaan **,** dan **Bahan** . **Yuran** adalah kelas transaksi pendapatan sahaja.

## <a name="work-entities-and-billing-entities"></a>Entiti kerja dan entiti pengebilan

Projek dan Tugas adalah entiti yang mewakili kerja. Garis sebut harga dan talian Kontrak adalah entiti yang mewakili pengebilan. Anda boleh memautkan entiti kerja yang berbeza kepada pilihan pengebilan dengan mengaitkannya dengan baris Sebut Harga atau baris Kontrak.

## <a name="multi-customer-deals"></a>Urus niaga berbilang pelanggan

Tawaran berbilang pelanggan berlaku apabila terdapat lebih daripada satu pelanggan bagi setiap invois. Berikut adalah beberapa contoh biasa:

- **Pengilang peralatan asal (OEM) perusahaan dan rakan kongsi mereka- Rakan kongsi**  dan penjual semula menjual produk yang merangkumi perkhidmatan nilai tambah. Semasa perjanjian dengan pelanggan, OEM biasanya menawarkan untuk membiayai sebahagian daripada projek.
- **Projek**  sektor awam: Pelbagai jabatan kerajaan tempatan bersetuju membiayai sesuatu projek dan diinvois mengikut pecahan yang dipersetujui sebelum ini. Contohnya, unit pentadbiran sekolah tempatan dan jabatan kerajaan bandar atau tempatan bersetuju untuk membiayai pembinaan kolam renang.

## <a name="invoice-schedules"></a>Jadual invois

Jadual invois adalah khusus untuk setiap baris sebut harga dan merupakan pilihan. Jadual invois dibuat berdasarkan tarikh mula dan tamat tertentu serta kekerapan invois. Ia digunakan semasa peringkat kontrak, apabila proses penciptaan invois automatik dikonfigurasikan. Semasa peringkat sebut harga, jadual invois adalah pilihan. Jika ia dicipta semasa peringkat sebut harga, ia disalin ke kontrak projek yang dicipta apabila sebut harga projek dimenangi.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Perbezaan daripada sebut harga jualan Dynamics 365

Sebut harga Operasi Projek dibina pada sebut harga Jualan Dynamics 365. Walau bagaimanapun, terdapat beberapa perbezaan yang penting dalam kefungsian yang patut anda ketahui:

- Petikan Operasi Projek mempunyai dua jenis baris yang berbeza: satu untuk projek dan satu untuk produk.
- Petikan Operasi Projek mempunyai halaman dan elemen antara muka pengguna (UI) mereka sendiri, peraturan perniagaan, logik perniagaan dalam pemalam, dan skrip pihak klien yang menjadikannya berbeza daripada sebut harga Jualan.
- Dalam Jualan, anda boleh melampirkan berbilang pesanan pada sebut harga jualan tunggal. Dalam Operasi Projek, anda boleh melampirkan hanya satu kontrak projek pada sebut harga projek.
- Apabila anda memenangi sebut harga jualan, peluang yang berkaitan boleh kekal terbuka. Selepas sebut harga projek dimenangi, peluang yang berkaitan akan ditutup.
- Sebut harga jualan tidak termasuk beberapa bidang dan konsep yang disertakan dalam sebut harga projek. Medan termasuk **Unit Kontrak**, **Pengurus Akaun** dan **Bil kepada Nama Kenalan**.
- Sebut harga jualan dan sebut harga projek dikenal pasti oleh medan Jenis **berasaskan** set pilihan. Untuk sebut harga jualan, nilai medan ini adalah **berasaskan** item. Untuk sebut harga projek, nilainya adalah **berasaskan** Kerja.

Oleh kerana perbezaan ini, kami tidak mengesyorkan agar anda menggunakan sebut harga Jualan dan sebut harga Operasi Projek secara bergantian.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
