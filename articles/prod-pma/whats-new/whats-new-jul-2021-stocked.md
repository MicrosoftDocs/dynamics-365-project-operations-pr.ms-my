---
title: Ciri baharu atau perubahan dalam Project Operations, Julai 2021 untuk senario berdasarkan distok/pengeluaran
description: Artikel ini memberikan maklumat mengenai kemas kini kualiti yang tersedia dalam keluaran Operasi Projek Julai 2021 untuk senario berasaskan stok / pengeluaran.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028851"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Ciri baharu atau perubahan dalam Project Operations, Julai 2021 untuk senario berdasarkan distok/pengeluaran

_**Digunakan Pada:** Project Operations untuk senario berasaskan stok/pengeluaran_

Artikel ini terpakai kepada komponen dan versi berikut Dynamics 365 Project Operations:

- Pengurusan projek dan perakaunan dalam persekitaran Dynamics 365 Finance versi 10.0.20
 
### <a name="quality-updates"></a>Kemas kini kualiti
                                                                                                                                                                                  
| Bahagian ciri                      | Nombor rujukan| Kemas kini kualiti                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengurusan projek dan perakaunan | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Rekod komitmen kos daripada permintaan pembelian dikosongkan sebaik sahaja pesanan pembelian dikeluarkan daripada isu permintaan pembelian.                                                                           |
| Pengurusan projek dan perakaunan | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Pengesahan belanjawan berlaku dua kali dalam permintaan pembelian. Duplikasi ini bermaksud bahawa permintaan tidak boleh ditutup dan pesanan pembelian yang sepadan tidak dicipta.                                                                                                                        |
| Pengurusan projek dan perakaunan | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Peraturan pengebilan **Peratusan untuk dibilkan** tidak dapat dilengkapkan kerana isu pembundaran.                                                                              |
| Pengurusan projek dan perakaunan | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Apabila anda melaraskan transaksi dan peratusan mempunyai perpuluhan, harga kos dan jualan tidak dilaraskan dengan betul.                                      |
| Pengurusan projek dan perakaunan | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Penjelajah sumber perakaunan menunjukkan jam untuk baris perakam waktu tunggal untuk berbilang baris perakam waktu dengan aktiviti berbeza.                                      |
| Pengurusan projek dan perakaunan | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Pandangan yang disimpan dan pemeribadian butiran baris perakam waktu menyebabkan sistem sentiasa membuka butiran untuk perakam waktu pertama dalam senarai apabila mencuba untuk membuka perakam waktu.  |
| Pengurusan projek dan perakaunan | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Nod akar projek hilang dan rekod struktur pecahan kerja dipadamkan selepas import.                                                                                             |
| Pengurusan projek dan perakaunan | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Apabila item diterima dan dikeluarkan secara separa daripada keperluan   item, sistem mengemas kini baki penggunaan belanjawan yang salah. |
| Pengurusan projek dan perakaunan | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Pesanan pembelian pengekalan projek tidak menunjukkan jumlah dengan betul dalam anak tetingkap **Jumlah** atau grid **Invois belum selesai** grid.                                                                  |
| Pengurusan projek dan perakaunan | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Apabila menutup inventori, pelarasan kos item projek disiarkan pada akaun baki dan bukannya akaun keuntungan atau kerugian.                                                            |
| Pengurusan projek dan perakaunan | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Baucar transaksi disiarkan projek dan anggaran baucar menggunakan USD sebagai mata wang perakaunan tetapi amaun menunjukkan apa yang akan setara dengan CAD.              |
| Pengurusan projek dan perakaunan | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Kod komited dengan keperluan item dan pesanan pembelian adalah   salah dalam proses invois pesanan pembelian dengan resit produk bahagian dan penginvoisan bahagian.       |
| Pengurusan projek dan perakaunan | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Pelarasan projek tidak mengemas kini amaun jualan dengan kos tidak langsung   dengan betul.                                                                                    |
| Pengurusan projek dan perakaunan | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Jadual **Perakam Waktu** tiada hubungan yang ditakrifkan dengan pandangan **Pekerja/Sumber**.                                                                                   |
| Pengurusan projek dan perakaunan | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Tidak dapat mengisi medan **Nombor aktiviti** apabila anda memilihnya daripada menu juntai bawah untuk perakam waktu antara syarikat.                                                                 |
| Pengurusan projek dan perakaunan | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Anda tidak boleh menambahkan medan **Tujuan** atau **Perihalan aktiviti** diperibadikan untuk halaman berikut: **Transaksi disiarkan projek**, **Penciptaan cadangan invois** atau **Cadangan invois**.  |
| Pengurusan projek dan perakaunan | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Kawalan tarikh penghantaran yang salah diberikan apabila anda mencipta keperluan item dengan menggunakan pengurusan data (**ProjSalesItemRequirementEntity**).                                              |
| Pengurusan projek dan perakaunan | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Apabila anda memilih ID kontrak projek dalam Finance, persekitaran bersepadu Project Operations membuka halaman untuk mencipta rekod baharu dan bukannya membuka kontrak projek sedia ada.                                                                                                                 |
| Pengurusan projek dan   perakaunan | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Label, "@SYS4083080" ("Tidak dapat mencari rekod Pekerja unik   yang sesuai dengan nilai yang dimasukkan") tidak diterjemahkan kepada Bahasa Denmark.                                |
| Pengurusan projek dan perakaunan | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Medan **Kumpulan cukai jualan item** tidak boleh diedit dalam cadangan invois.                                                                               |
| Pengurusan projek dan perakaunan | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Kos komited telah terlebih catat dengan amaun cukai bukan pemotongan.                                                                                                    |
| Pengurusan projek dan perakaunan | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Penyiaran perakam waktu antara syarikat dengan berbilang projek dan   dimensi kewangan berbeza menjana nilai yang tidak dijangka dalam lejar umum.                             |
| Pengurusan projek dan perakaunan | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Baris cadangan invois diduplikasikan disebabkan berbilang tika proses berkala **Import daripada pemeringkatan** yang berjalan pada masa yang sama.                                      |
| Pengurusan projek dan perakaunan | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Terdapat ralat dalam penyiaran cadangan invois nota kredit, jadi   transaksi pada baucar tidak akan seimbang.    |
| Pengurusan projek dan perakaunan | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Kos komited projek menjadi tidak betul selepas invois belum selesai ditangguhkan dikeluarkan.                                                                             |
| Pengurusan projek dan   perakaunan | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Anda tidak boleh mencipta nota kredit untuk pesanan jualan projek apabila cukai berada dalam mata wang berbeza daripada mata wang syarikat.                                      |
| Pengurusan projek dan perakaunan | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Pemadaman kontrak juga memadamkan alamat berkaitan dengan pelanggan.                                                                                     |
| Pengurusan projek dan perakaunan | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Cadangan invois yang terhasil daripada pembetulan transaksi masa negatif tidak boleh disiarkan.                                                                    |
| Perjalanan dan Perbelanjaan                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Cukai dikira secara berbeza dalam laporan perbelanjaan.                                                                                                                  |
| Perjalanan dan Perbelanjaan                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Kemas kini keluaran **DB72_Expense.updateTrvExpTransProjTransId()**   tidak membenarkan **trvExpTrans.ReferenceDataAreaId** mencipta jujukan nombor baharu.                    |
| Perjalanan dan Perbelanjaan                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Amaun yang difailkan tidak ditunjukkan dengan medan mandatori.                                                                                                             |
| Perjalanan dan Perbelanjaan                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Penambahbaikan dalam prestasi lampiran perbelanjaan pada laporan perbelanjaan yang menggunakan antara muka pengguna Digambarkan Semula Perbelanjaan.                                                            |
| Perjalanan dan Perbelanjaan                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Anda boleh memadamkan laporan perbelanjaan yang disiarkan.                                                                                           |
| Perjalanan dan Perbelanjaan                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Mesej dasar perbelanjaan dipaparkan beberapa kali.                                                                                                       |
| Perjalanan dan Perbelanjaan                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Medan **Kaedah pembayaran** disertakan pada anak tetingkap **Perbelanjaan baharu**.                                                                                                      |
| Perjalanan dan Perbelanjaan                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Alat **Tetap semula status dokumen Perbelanjaan** hendaklah menetapkan semula status laporan perbelanjaan kepada **Draf** jika aliran kerja tidak ditemui. 

### <a name="regulatory-updates"></a>Kemas kini kawal selia
Untuk maklumat tentang kemas kini kawal selia untuk aplikasi kewangan dan operasi, lihat [Kemas kini kawal selia](/dynamics365/finance/localizations/regulatory-updates). Anda juga boleh mendaftar masuk ke Lifecycle Services (LCS) dan melihat kemas kini kawal selia yang dirancang menggunakan alat Carian isu. Carian isu membolehkan anda membuat carian mengikut negara, jenis ciri dan keluaran.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
