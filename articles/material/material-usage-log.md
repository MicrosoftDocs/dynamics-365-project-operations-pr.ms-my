---
title: Penggunaan bahan rekod pada projek dan tugas projek
description: Topik ini menyediakan maklumat tentang cara untuk log penggunaan bahan untuk projek dan tugas projek.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 60aed9aa82eeb0339e71b0171719e765a63d91e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579685"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Penggunaan bahan rekod pada projek dan tugas projek

_**Gunakan pada:** Project Operations untuk senario berdasarkan sumber/bukan stok, Pelaksanaan ringan - urusan untuk penginvoisan proforma_

Apabila pasukan projek menyelesaikan tugas pada projek, mereka menghabiskan atau menggunakan bahan. Log penggunaan bahan menyediakan cara merekodkan penggunaan ini supaya ia boleh diluluskan oleh pengurus projek dan akhirnya diinvois kepada pelanggan. 

Untuk merekodkan penggunaan katalog atau bahan masukan manual dan serahkan kepada pelulus, ikut langkah ini: 

1. Dalam anak tetingkap navigasi, pilih **Penggunaan Bahan** dan kemudian pilih **Baharu**.
2. Pada halaman **Penggunaan Bahan Baharu**, masukkan maklumat penggunaan bahan yang diperlukan dan kemudian pilih **Simpan**.

Jadual berikut menyediakan maklumat tentang medan pada halaman **Log Penggunaan Bahan**. 

| **Medan** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- |
| Penerangan | Perihalan tentang penggunaan bahan tertentu. | Tiada kesan hiliran untuk medan ini. |
| Tarikh | Tarikh bahan dijangka akan digunakan. | Tiada kesan hiliran untuk medan ini. |
| Project | Projek senarai yang aktif. | Memilih projek untuk log penggunaan bahan memberikan kesan pada medan **Tugas** untuk menunjukkan tugas yang ada pada projek sahaja. |
| Tugas | Senarai tugas untuk projek termasuk kerja ringkasan dan nod daun. | Memilih tugas untuk log penggunaan bahan memberikan kesan pada kos bahan aktual dan jualan bahan aktual untuk tugas. Jika medan ini kosong, kos penggunaan bahan dan jualan yang sepadan dijejaki dan diringkaskan hanya di peringkat projek. |
| Pilih Produk | Tentukan jika penggunaan bahan ini untuk produk (katalog) **Sedia ada** atau produk **Masukan manual**. | Medan ini menentukan jenis produk. |
| Produk | ID produk daripada katalog produk. Apabila anda memilih ID produk, medan **Pilih Produk** mengemas kini secara automatik kepada **Produk sedia ada**. ID digunakan untuk mendapatkan kembali harga kos dan jualan daripada senarai harga. | Tiada kesan hiliran untuk medan ini. |
| Perihalan Produk Masukan Manual | Medan teks untuk masukan manual nama produk. Medan ini hanya tersedia apabila anda memilih produk **Masukan Manual** dalam medan **Pilih produk**.| Tiada kesan hiliran untuk medan ini. |
| Sumber Boleh Ditempah| Sumber yang menggunakan bahan ini pada projek. Lalai untuk medan ini ialah sumber boleh ditempah bagi pengguna dilog masuk, tetapi boleh ditukar kepada penggunaan rekod bagi pihak ahli lain pada pasukan projek. | Tiada kesan hiliran untuk medan ini. |
| Kumpulan unit | Nilai lalai dalam medan ini diambil daripada kumpulan unit yang ditetapkan sebagai lalai pada produk katalog. Anda boleh mengemas kini medan ini untuk memilih kumpulan unit lain. | Tiada kesan hiliran untuk medan ini. |
| Unit | Nilai lalai dalam medan ini ialah unit lalai produk yang dipilih. Anda boleh mengemas kini medan ini untuk memilih unit lain. | Menukar unit mengakibatkan harga unit dan kos lalai yang berbeza. |
| Kuantiti | Kuantiti produk yang telah digunakan pada projek atau tugas projek. | Tiada kesan hiliran untuk medan ini. |
| Kos Unit | Kos unit bagi gabungan produk dan unit yang dipilih seperti yang ditetapkan dalam senarai harga kos yang berkenaan. | Kos unit sentiasa ditunjukkan dalam mata wang kos projek. Jika tiada kos unit untuk gabungan produk dan unit dalam senarai harga, kos unit akan ditetapkan lalai kepada 0.00. |
| Jumlah Kos | Amaun kos yang dikira sebagai kuantiti \* kos unit.| Amaun kos sentiasa ditunjukkan dalam mata wang kos projek. |


## <a name="submit-material-usage-for-review-and-approval"></a>Serahkan penggunaan bahan untuk semakan dan kelulusan 
Selepas anda merekodkan semua penggunaan bahan anda dan anda bersedia untuk ia diluluskan, anda mesti menyerahkan maklumat penggunaan untuk semakan.

1. Pergi ke **Log Penggunaan Bahan** dan pilih satu atau lebih entri. Atau, pilih semua rekod penggunaan bahan dengan menggunakan kotak semak pada pengepala.
2. Pilih **Serahkan**. Sistem memproses entri yang dipilih dan kemudian mencipta permintaan kelulusan penggunaan bahan.

## <a name="recall-a-material-usage-log"></a>Panggil balik log penggunaan bahan

Apabila perlu, anda boleh memanggil balik penggunaan bahan yang diserahkan. Masa yang diperlukan untuk memanggil balik entri penggunaan bahan bergantung pada peringkat kelulusan.  Jika pelulus belum meluluskan entri itu, tarik balik boleh berlaku dengan serta-merta. Walau bagaimanapun, jika entri telah diluluskan, pelulus diminta untuk meluluskan tarik balik dan membalikkan transaksi tersebut.

1. Pergi ke **Penggunaan Bahan** dan dalam senarai log penggunaan material, pilih penggunaan bahan untuk dipanggil balik.
2. Pilih **Tarik balik**. Jika entri penggunaan bahan belum diluluskan lagi, sistem memanggil balik dengan segera. Jika entri material telah diluluskan, permintaan panggil balik dicipta untuk memberitahu pelulus yang anda mahu panggil balik penggunaan bahan. Pelulus akan mengesahkan yang pembalikan boleh dilakukan dan entri akan dikembalikan.

## <a name="delete-a-material-usage-log"></a>Padamkan log penggunaan bahan

Anda boleh memadamkan log penggunaan bahan yang belum diserahkan. Untuk memadamkan log penggunaan bahan yang telah diserahkan, anda mesti memanggil balik terlebih dahulu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
