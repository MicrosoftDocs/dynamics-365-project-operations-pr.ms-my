---
title: Pengurusan subkontrak dalam Project Operations
description: Artikel ini memberikan gambaran keseluruhan proses pengurusan subkontrak hujung ke hujung yang biasa dalam organisasi berasaskan projek.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522337"
---
# <a name="subcontract-management-in-project-operations"></a>Pengurusan subkontrak dalam Project Operations


_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini memberikan gambaran keseluruhan proses pengurusan subkontrak hujung ke hujung dalam organisasi berasaskan projek. Subkontrak untuk perkhidmatan biasanya mengikut aliran proses perniagaan yang ditunjukkan dalam rajah berikut.

![Aliran proses subkontrak](../media/SubcontractingProcessFlow.png)

Senarai berikut memberikan penerangan langkah demi langkah proses subkontrak.

1. Pengurus projek mencipta subkontrak dengan vendor. Secara lalai, senarai harga yang dilampirkan pada rekod vendor digunakan untuk subkontrak. Akaun vendor mempunyai jenis hubungan **Vendor** atau **Pembekal**.
2. Pengurus projek boleh memperincikan semua pembelian sebagai item baris pada subkontrak. Baris subkontrak boleh untuk masa, perbelanjaan, atau produk. Kelas transaksi baris subkontrak menentukan tujuan baris.
3. Pengurus akaun vendor dan pengurus projek boleh melakukan pengulangan pada subkontrak. Penentuan harga boleh disesuaikan dalam senarai harga pembelian yang dilampirkan pada subkontrak.
4. Pada masa ini atau kemudian dalam proses ini, jika baris subkontrak adalah untuk masa, pengurus akaun vendor akan mengaitkan kenalan vendor dengan setiap baris subkontrak. Perkaitan ini memberikan maklumat kepada pengurus projek yang mengusahakan subkontrak tersebut. Apabila kenalan vendor dikaitkan dengan baris subkontrak, sistem akan mencipta sumber boleh ditempah daripada kenalan secara automatik, jika sumber boleh ditempah tidak wujud.
5. Kaedah pengebilan pada setiap baris subkontrak boleh **Harga Tetap** atau **Masa dan Bahan**. Untuk baris subkontrak harga tetap, jadual invois berasaskan pencapaian akan disediakan.
6.  Selepas subkontrak disediakan dan rundingan selesai, ia akan disahkan. Subkontrak yang disahkan tidak boleh diedit tetapi jika perubahan berlaku, subkontrak boleh 'dibuka semula untuk diedit', yang menetapkan status daripada **Disahkan** kembali kepada **Draf** dan rundingan boleh dibuka semula. 
7.  Apabila mencipta ahli pasukan generik dalam projek, ahli pasukan boleh dikaitkan dengan baris subkontrak. Ini menunjukkan keperluan menugaskan ahli pasukan generik dengan keupayaan subkontraktor.
8.  Ahli pasukan yang dinamakan boleh sama ada dicipta secara langsung pada projek atau dicipta dengan menempah mereka menggunakan pengalaman penjadualan sumber. Jika ahli pasukan projek yang dinamakan ialah pekerja kontrak, dia mungkin boleh dikaitkan kepada baris subkontrak. Ini akan menarik daripada kapasiti tersedia pada baris subkontrak.
9.  Sumber subkontraktor boleh mencatatkan masa, perbelanjaan dan penggunaan bahan pada projek dan tugas projek dan kemudian membuat penyerahan untuk kelulusan. Ini adalah sama untuk pekerja. Apabila merekodkan masa, pekerja kontrak boleh memilih subkontrak khusus dan baris subkontrak.
10. Setelah diluluskan, masa yang diluluskan oleh subkontrak akan merekodkan kos sebenar projek berdasarkan harga pembelian pekerja kontrak atau peranan yang dilakukan oleh mereka pada projek tersebut.
11. Invois vendor dan item baris invois vendor boleh direkodkan dalam sistem untuk kerja yang dilakukan oleh sumber vendor atau produk yang dihantar oleh vendor. Baris invois vendor mesti khusus kepada projek dan untuk kelas transaksi masa, perbelanjaan, produk/bahan, pencapaian atau yuran. Secara pilihan, baris invois vendor boleh merujuk baris subkontrak.
12. Sistem akan mengaitkan semua kos sebenar yang sepadan dengan baris subkontrak dan projek kepada invois vendor secara automatik. Ini akan memudahkan proses pemadanan dan pengesahan 3 hala.
13. Pengurus projek kemudian boleh menyemak projek yang dipadankan secara automatik, mengalih keluar atau menambah kos sebenar projek yang lain, dan melengkapkan proses pengesahan.
14. Melengkapkan proses pengesahan pada semua baris akan menandakan invois vendor sebagai **Sedia untuk Pembayaran**. Pada peringkat ini, invois vendor dan baris boleh dipindahkan kepada sistem Perakaunan atau Belum Bayar untuk memproses pembayaran kepada vendor. Kos projek yang direkodkan sebelum ini akan digantikan dan kos sebenar daripada baris invois vendor akan direkodkan pada projek.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Baris subkontrak berasaskan kuantiti dan baris subkontrak berasaskan kerja

Baris subkontrak boleh merupakan jenis berasaskan kuantiti atau berasaskan kerja. 

Apabila baris subkontrak adalah **berasaskan kuantiti**, kuantiti yang dibeli pada baris subkontrak untuk masa, perbelanjaan, atau bahan boleh digunakan pada mana-mana projek.

Apabila baris subkontrak adalah **berasaskan kerja**, baris subkontrak dipetakan kepada badan kerja yang diwakili oleh nod dalam pelan projek. Nilai baris subkontrak ialah jumlah semua komponen yang diperlukan untuk menghantar badan kerja tersebut. Ini dimodelkan sebagai butiran baris subkontrak dan boleh merupakan koleksi masa, perbelanjaan atau bahan. Untuk baris subkontrak berasaskan kerja, baris subkontrak juga dikhususkan untuk satu projek. Subkontrak jenis ini tidak disokong oleh Project Operations pada masa ini.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

