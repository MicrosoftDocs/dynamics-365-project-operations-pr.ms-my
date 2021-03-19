---
title: Gambaran keseluruhan proses jualan
description: Topik ini memberikan maklumat tentang proses jualan asas.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277394"
---
# <a name="sales-process-overview"></a>Gambaran keseluruhan proses jualan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Proses jualan yang digunakan dalam organisasi berasaskan projek berbeza daripada proses jualan yang digunakan dalam organisasi berasaskan produk. Ini adalah kerana kitaran jualan untuk organisasi berasaskan projek adalah lebih lama dan memerlukan teknik anggaran tersuai untuk menganalisis dan mencipta sebut harga untuk setiap urusan. Dynamics 365 Project Operations menggunakan beberapa fungsi berikut yang digunakan dalam proses jualan:

- Rekod bakal pelanggan digunakan untuk menjejak proses jualan.
- Bakal pelanggan yang layak dijejak sebagai peluang.
- Semua artifak berkaitan untuk peluang adalah boleh diakses. Artifak ini termasuk pasukan jualan, pemegang kepentingan, kebarangkalian, penarafan, peringkat jualan dan proses perniagaan.
- Sebut harga berbilang dicipta untuk peluang.
- Sebut harga diberikan status, **Tutup sebagai Menang** untuk mencipta pesanan jualan. Dalam Project Operations, pesanan jualan disesuaikan dan dipanggil kontrak projek.

## <a name="estimate-a-sale"></a>Anggarkan jualan
Nilai jualan boleh dianggarkan berasaskan pada projek yang sebelum ini telah dihantar dan kerumitan projek. Untuk projek yang melibatkan sambungan kepada projek sebelumnya, atau projek di mana kepakaran penjual adalah template kerja yang tinggi dan terkenal digunakan, anda boleh menggunakan proses anggaran yang lebih mudah. Projek yang lebih rumit biasanya mempunyai proses pembelian yang lebih panjang. Oleh itu, terdapat lebih banyak peringkat dalam proses anggaran jualan. Pada awal proses, pasukan jualan menggunakan input pengurus akaun dan pakar perkara subjek (PKS) untuk mencipta anggaran tahap tinggi bagi setiap komponen kerja berbeza yang disebut harga. Komponen kerja ini diwakili oleh baris sebut harga. 

Anda boleh mencipta anggaran tahap tinggi sebut harga. Akhirnya, anggaran tahap tinggi akan digantikan dengan anggaran yang lebih terperinci berdasarkan pelan projek yang anda cipta dengan menggunakan templat projek yang diseragamkan. Templat ini membantu anda membina jadual dan menentukan nilai kewangan pada sebut harga dan komponennya (baris sebut harga). 

Anda boleh mencipta berbilang sebut harga untuk projek dan kumpulkan mereka di bawah rekod peluang tunggal. Akhirnya, salah satu daripada sebut harga ditanda **Ditutup sebagai Menang** dan kontrak projek atau pernyataan kerja (SOW) dicipta. Kontrak projek memegang nilai kontrak untuk setiap komponen (baris kontrak) yang diterima oleh pelanggan untuk penghantaran. SOW biasanya dicipta sebagai dokumen Microsoft Word. Semua invois yang dihantar kepada pelanggan melalui rujukan penghantaran projek kontrak projek atau SOW.

Anda juga boleh mencipta sebut harga alternatif di bawah satu rekod peluang atau menyediakan sistem supaya kontrak projek dicipta apabila sebut harga dimenangi. Dalam kes ini, anda boleh melampirkan dokumen Word yang mewakili SOW kepada rekod kontrak projek.

## <a name="configure-the-sales-process"></a>Konfigurasikan proses jualan
Anda boleh menggunakan aliran proses perniagaan untuk mengkonfigurasi proses jualan anda. Aliran ini menyediakan antara muka visual dipandu untuk menggerakkan urusan ke hadapan melalui peringkat proses jualan.

Sebagai contoh, syarikat anda mungkin mempunyai enam peringkat berikut dalam proses jualan:

1. Layakkan
2. Anggaran
3. Semakan dalama
4. Kontrak
5. Hantar
6. Tutup
 
Organisasi anda mungkin menggunakan entiti berbeza untuk mewakili urusan yang sama semasa ia berkembang. Pada awal proses jualan, urusan diwakili oleh entiti Peluang. Apabila masa berlalu dan butiran lanjut muncul, anda mungkin menggunakan anggaran peringkat tinggi untuk mencipta satu atau lebih sebut harga. Jika salah satu daripada sebut harga ini disemak oleh pemegang amanah pelanggan dan dalaman, entiti Sebut Harga mewakili urusan. Selepas pelanggan menerima sebut harga, kontrak projek atau SOW mewakili perjanjian tersebut. Untuk menyokong tingkah laku ini, BPFs berstruktur supaya setiap peringkat dalam proses dihubungkan kepada jadual pangkalan data yang berbeza.

Peringkat **Kelayakan** dalam proses jualan boleh disokong oleh entiti Peluang. Peringkat **Anggaran** dan **Semakan Dalaman** boleh disokong oleh entiti Sebut Harga. Peringkat **Kontrak**, **Penghantaran** dan **Tutup** boleh disokong oleh entiti Kontrak Projek.

Apabila anda memindahkan transaksi melalui peringkat, anda akan digesa untuk mencipta rekod entiti yang sesuai untuk membantu dan membimbing anda melalui proses. Peringkat boleh bersyarat. Contohnya, jika anda memerlukan semakan dalaman sebut harga hanya jika sebut harga menggunakan senarai harga tersuai, anda boleh mengkonfigurasi keadaan tersebut dalam peringkat proses perniagaan yang sesuai. Peringkat **Semakan Dalaman** kemudian ditunjukkan hanya untuk sebut harga yang menggunakan senarai harga tersuai. Untuk semua tawaran dan sebut harga lain, peringkat **Anggaran** diikuti oleh peringkat **Kontrak**.

> [!NOTE]
> Project Operations mempunyai halaman khusus untuk rekod Peluang, Sebut Harga dan Entiti Invois. Anda mesti mencipta rekod ini menggunakan halaman maklumat projek untuk entiti ini. Jika tidak, anda tidak akan dapat membuka rekod daripada halaman **Maklumat projek**. Jika anda mahu membuka rekod daripada halaman **Maklumat projek**, anda mesti memadam dan menciptanya semula menggunakan halaman **Maklumat projek** yang memastikan logik perniagaan untuk setiap jenis entiti ini bagi medan **Jenis** rekod ditetapkan dengan betul dan semua konsep mandatori dimulakan dengan betul.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Jejak semakan ke sebut harga dan rancangan projek dalam kitaran jualan
Dalam Project Operations, anda tidak boleh menjejak semakan yang dibuat kepada sebut harga. Sebaliknya, anda mesti menandakan sebut harga **Tutup sebagai Kalah** dan kemudian mencipta sebut harga baharu. Anda boleh menyalin sebut harga atau klon sebut harga berasaskan projek.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Jejak komen dan kelulusan sebut harga dan kontrak projek
Anda boleh mengurus semakan dan kelulusan sebut harga dan kontrak projek dengan menggunakan dinding rekod dan siaran. Organisasi anda boleh mencipta aliran kerja tersuai dan pasang masuk untuk menugas, menghala semula, meningkat dan mengurus pemberitahuan semakan dan kelulusan item kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]