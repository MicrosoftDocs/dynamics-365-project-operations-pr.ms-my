---
title: Ciri baharu Julai 2021 - Project Operations pelaksanaan ringan
description: Topik ini menyediakan maklumat mengenai kemas kini berkualiti yang tersedia dalam keluaran Julai 2021 Project Operations pelaksanaan ringan.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009227"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Ciri baharu Julai 2021 - Project Operations pelaksanaan ringan

_Gunakan Pada: Pelaksanaan lite - urusan dengan invois proforma_

Topik ini digunakan pada komponen dan versi Dynamics 365 Project Operations berikut:

  - Project Operations dalam persekitaran Dataverse versi 4.12.0.148 atau 4.12.0.152.

## <a name="quality-updates"></a>Kemas kini kualiti
| **Bahagian ciri**              | **Nombor rujukan** | **Kemas kini kualiti**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengebilan dan Penentuan Harga           | 2224046              | Medan **Kelas Transaksi** boleh diedit pada tab **Butiran Baris Sebut Harga** tetapi dikunci jika anda bekerja daripada halaman **Butiran Baris Sebut Harga**.                                                                     |
| Pengebilan dan Penentuan Harga           | 2224400              | Tindakan **Tutup Sebut Harga Sebagai Menang** gagal apabila sebut harga tidak mempunyai pencapaian tarikh.                                                                                                                                    |
| Pengebilan dan Penentuan Harga           | 2234089              | Apabila anda memasukkan perihalan produk secara manual, ia dikosongkan selepas anda memasukkan kuantiti untuk anggaran material.                                                                                                                         |
| Pengebilan dan Penentuan Harga           | 2234100              | Grid **Persediaan Pengebilan Tugas** tidak termasuk lajur **Material** dan nilainya pada tab **Pengebilan Tugas** projek.                                                                                                       |
| Pengebilan dan Penentuan Harga           | 2277409              | ID produk tidak tersedia pada butiran baris kontrak untuk baris jenis bahan.                                                                                                                                        |
| Pengebilan dan Penentuan Harga           | 2281728              | Mencipta baris kontrak tidak semestinya menilai semula aktual yang menyebabkan peningkatan ketara dalam volum data, yang memberi kesan kepada prestasi.                                                                                |
| Pengebilan dan Penentuan Harga           | 2298668              | Baris jurnal yang berkaitan dengan perbelanjaan yang ditarik balik dan dipadamkan tidak dialih keluar.                                                                                                                                     |
| Pengebilan dan Penentuan Harga           | 2300192              | Apabila berbilang pengguna mengedit invois, butiran baris invois baharu boleh dicipta pada invois yang disahkan.                                                                                   |
| Pengebilan dan Penentuan Harga           | 2301569              | Invois tidak boleh dibetulkan jika penahan amaun \$0 telah dikenakan.                                                                                                                                        |
| Pengebilan dan Penentuan Harga           | 2307965              | Ralat berlaku jika harga kategori dicipta dengan nilai yang tidak ditemui.                                                                                                                           |
| Pengebilan dan Penentuan Harga           | 2326870              | Ralat berlaku dalam **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** jika **producttypecode** adalah nol.                                                                            |
| Pengebilan dan Penentuan Harga           | 2332732              | Ralat berlaku jika pencapaian baris kontrak dicipta tanpa baris pesanan.                                                                                                                |
| Perancangan dan Penjejakan Projek | 2181094              | API Penjadualan Projek kini menyokong Log PSS dan Log Operation Set yang disimpan selama 90 hari.                                                                                                                  |
| Perancangan dan Penjejakan Projek | 2254201              | Label **Mod Jadual** dikemas kini dengan butiran yang menghuraikan penetapan logik lalai.                                                                                                                                      |
| Perancangan dan Penjejakan Projek | 2300252              | Cache respons **openProject** dikemas kini dan memasukkan pemilik token dalam kunci cache, **Url asas** dan **Url Segmen** supaya **Url Permintaan** boleh sentiasa dikira semula jika **Url asas** berubah. |
| Perancangan dan Penjejakan Projek | 2301312              | **msdyn_membershipstatus** telah dialih keluar daripada pandangan **Ahli Pasukan Projek**.                                                                                                                                        |
| Perancangan dan Penjejakan Projek | 2302759              | Produk tidak semestinya diambil pada tab **Tugasan Sumber**, **Anggaran** dan **Anggaran Perbelanjaan**.                                                                                                        |
| Perancangan dan Penjejakan Projek | 2308050              | **CopyProject** gagal dengan ralat, “Gagal mendapatkan token untuk berbual dengan perkhidmatan jauh”.                                                                                                                           |
| Perancangan dan Penjejakan Projek | 2322650              | Pandangan **Senarai Tugas Projek** telah dikemas kini untuk memaparkan tarikh tugas secara lalai.                                                                                                            |
| Perancangan dan Penjejakan Projek | 2327266              | **CopyProject** menjana ralat, "Kunci tidak ditemui dalam kamus" ketika menyalin anggaran.                                                                                                      |
| Perancangan dan Penjejakan Projek | 2328123              | **CopyProject** menjana ralat, "Gagal mendapatkan token untuk berbual dengan perkhidmatan jauh".                                                                                                                          |
| Perancangan dan Penjejakan Projek | 2336258              | **CopyProject** menyalin secara tidak betul nama kedudukan sumber.                                                                                                                                                 |
| Pengebilan dan Penentuan Harga           | 2224476              | Medan **Sumber Boleh Ditempah** tidak ditetapkan kepada pengguna dilog masuk secara lalai pada halaman **Penggunaan Bahan**.                                                                                                            |
| Pengurusan Sumber           | 2277249              | Ralat berlaku apabila keperluan sumber bukan berdasarkan projek dikemas kini.                                                                                                            |
| Pengurusan Sumber           | 2323869              | Penggunaan sumber tidak mengenal pasti sumber yang ditapis dengan betul.                                                                                                                                             |
| Masa dan Perbelanjaan              | 2176538              | Operator penapis yang tidak betul dikenakan kepada kawalan **Entri Masa**.                                                                                                                                                   |
| Masa dan Perbelanjaan              | 2177462              | Pemadaman entri masa dalam grid tidak mengemas kini status butang **Serah**, **Tarik Balik**, **Padam** dan **Entri Edit** seperti dijangka.                                                                                        |
| Masa dan Perbelanjaan              | 2299985              | **TimeEntriesImportFromResourceAssignment** tidak mengekalkan masa mula/tamat daripada kontur tugasan.                                                                                                  |
| Masa dan Perbelanjaan              | 2318426              | Selepas entri masa diserahkan, medan dikunci masih boleh diedit.                                                                                                                                   |
| Masa dan Perbelanjaan              | 2323749              | Ralat berlaku apabila perbelanjaan dicipta daripada tab **Berkaitan** bagi sumber boleh ditempah.                                                                                                      |
| Masa dan Perbelanjaan              | 2327678              | Apabila anda mencipta entri masa daripada tab **Berkaitan** bagi sumber boleh ditempah tidak dihantar ke kawalan entri masa.                                                                            |
| Umum                       | 2296857              | Penjejakan kemajuan untuk kerja yang memakan masa lama.                                                                                                                                                                        |
| Umum                       | 2253682              | Penyelesaian dwi tulis Project Operations tidak boleh dipasang apabila teras dwi tulis dipasang dalam persekitaran tanpa penyelesaian pengorkestraan dwi tulis.                                                |
| Umum                       | 2316420              | Peruntukan teras Project Service gagal jika unit perniagaan pengguna aplikasi berubah.                                                                                                                     |
| Umum                       | 2376405              | Masalah kemas kini berpandukan penerbit tetap (Kemas kini kualiti tersedia dalam versi 4.12.0.152)                                                                                                                     |
