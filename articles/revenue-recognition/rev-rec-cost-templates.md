---
title: Sediakan templat kos
description: Topik ini memberikan maklumat tentang cara mencipta dan menggunakan templat kos dalam Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993567"
---
# <a name="set-up-cost-templates"></a>Sediakan templat kos

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Topik ini memberikan maklumat tentang cara mencipta dan menggunakan templat kos dalam Project Operations. Templat kos menentukan:

- Kategori projek untuk ramalan dan transaksi sebenar akan dimasukkan dalam peratusan pengiraan siap projek. Nilai peratusan siap digunakan untuk mengira jumlah hasil yang dikenal pasti.
- Sama ada peratusan siap boleh diubah suai jika ia dikira secara automatik.
- Sama ada peratusan siap dikira berdasarkan jumlah atau unit.

## <a name="cost-template-example"></a>Contoh templat kos

Anda sedang bekerja pada projek reka bentuk tapak web untuk pelanggan yang anda mengenakan bayaran rata USD 10,000. Anda meramalkan bahawa ia akan mengambil masa 100 jam (USD 5,000) untuk melengkapkan projek. Anda juga meramalkan dua tiket penerbangan dan empat malam di hotel untuk lawatan ke tapak pelanggan (USD 1,800). Ini menyebabkan jumlah kos yang diramalkan adalah USD 6,800.

Apabila anda menjalankan proses pengiktirafan hasil harga tetap untuk membuat anggaran pada akhir bulan, anda mendapati bahawa anda telah bekerja 35 jam pada projek itu. Ini tidak lagi termasuk kos penerbangan atau hotel. Anda juga mempunyai pembantu melakukan lima jam penyelidikan untuk projek itu pada kos USD 100, yang belum dirancang oleh anda.

Apabila anda mengira nilai siap peratus untuk projek ini, anda mempunyai pilihan berikut:

- Adakah anda mahu memasukkan semua kos (jam dan perbelanjaan) atau hanya jam?
- Adakah anda mahu memasukkan semua kos atau jam yang dirancang sahaja?
- Adakah anda mahu mengira peratusan yang lengkap berdasarkan kos dolar jam yang dirancang (USD 5,000) atau hanya pada bilangan jam (100)?

Jawapan anda kepada soalan ini menentukan pilihan yang anda tetapkan pada templat kos dan kategori yang anda pilih pada templat kos.

Jadual berikut menggambarkan hasil kaedah yang berbeza bagi mengira nilai siap peratus untuk senario ini.

| Siap berdasarkan pada | Kos dolar atau unit | Peratus siap | Pengiraan |
| --- | --- | --- | --- |
| Semua jam, tiada perbelanjaan | Kos dolar | 37% 35 x USD 50 + USD 100 = USD 1,850 USD 1,850/USD 5,000 |
| Semua jam, tiada perbelanjaan | Unit | 40% | 40 jam/100 jam (termasuk lima jam tidak dirancang) |
| Jam dirancang, tiada perbelanjaan | Kos dolar atau unit | 35% | 35/100 jam atau 35 x USD 50/5,000 |
| Semua jam dan perbelanjaan | Kos dolar | 27.2% | USD 1,850/USD 6,800 |

Menentukan pendekatan yang perlu diambil untuk mencipta templat kos boleh bergantung pada beberapa pertimbangan:

- Jika anda memasukkan jam tidak dirancang dalam templat kos, anda berisiko mencapai 100 peratus siap sebelum projek selesai. Ini kerana jam sebenar akan lebih besar daripada jam yang dirancang. Jika anda menggunakan salah satu daripada dua kaedah pertama yang disenaraikan dalam jadual, anda perlu mengubah pelan (unit diramalkan) apabila anda menyedari penyelewengan. Dalam kes ini, anda akan menambah atau menolak jam berdasarkan pengetahuan anda tentang perkara yang diperlukan untuk menyelesaikan projek. Jika projek akan memerlukan lagi 65 jam untuk siap, anda akan menambah lima jam kepada pelan untuk jumlah sebanyak 105. Jika anda tahu bahawa pembantu anda akan melakukan lima jam lagi penyelidikan, jumlah tersebut akan menjadi 110 jam.
- Jika anda menggunakan kaedah ketiga yang disenaraikan dalam jadual, anda hanya akan mengemas kini jamu yang dirancang untuk masa anda sendiri bagi mengekalkan pengiraan peratusan siap dengan tepat. Keuntungan anda akan berubah apabila jam yang tidak dirancang dilog, tetapi anda akan kekal pada lintasan peratusan siap yang diketahui.
- Jika anda menggunakan kaedah keempat yang disenaraikan dalam jadual, risiko adalah perbelanjaan akan berlaku pada masa yang tidak teratur dan mungkin tidak ditunjukkan dalam pencapaian siap anda. Oleh itu, jika perbelanjaan dimasukkan, ia boleh menyebabkan peratus siap anda untuk turun naik lebih daripada yang diingini. Sebagai contoh, kerana anda belum menaiki penerbangan lagi, peratusan siap anda ialah 27 peratus dan bukannya 35 peratus atau 37 peratus jika asas pengiraan anda adalah pada masa sahaja. Jika anda telah membuat satu perjalanan selama dua malam dan telah meramalkan kos penerbangan dan hotel anda dengan tepat, peratusan siap akan menjadi 40.4 peratus (USD 1850 untuk buruh dan USD 900 untuk perbelanjaan = USD 2750/USD 6800 = 40.4 peratus). Oleh itu, perbelanjaan yang terlibat hanya untuk satu penerbangan akan mengubah peratus siap daripada 27 peratus kepada 40 peratus.

## <a name="create-cost-templates"></a>Cipta templat kos
Untuk mencipta templat kos, ikuti langkah-langkah berikut:

1. Untuk mengakses templat kos, dalam persekitaran Dynamics 365 Finance, pergi ke **Pengurusan projek dan perakaunan** > **Penyediaan** > **Anggaran** > **Templat kos**.
2. Pilih **Baharu** untuk mencipta templat kos baharu. Masukkan nama dan perihalan.
3. Berikan ID garisan kos untuk setiap jenis transaksi.
4. Pilih kaedah penyelesaian lalai:

  - **Automatik**: Peratusan siap dikira secara automatik pada projek. Nilai hasil tidak boleh ditukar.
  - **Manual**: Peratusan siap dikira secara automatik pada projek. Nilai hasil boleh ditukar.

  > [!NOTE]
  > Untuk pengiraan manual, peratusan siap dikekalkan dalam **Pengiraan manual** pada tab **Umum** pada halaman **Anggaran**.

5. Dalam **Siap berdasarkan pada**, pilih salah satu daripada nilai berikut:

  - **Jumlah**: Jumlah dalam mata wang perakaunan mengira peratusan siap.
  - **Unit**: Kuantiti mengira peratusan siap.
  - **Garisan lurus**: Sistem mengira peratusan siap berdasarkan asas berkadaran dengan menggunakan tarikh mula dan akhir projek untuk menentukan tempoh panjang projek.

6. Pilih **Garisan kos** untuk menyemak garisan kos bagi templat kos. Sekurang-kurangnya satu garisan kos diperlukan untuk setiap jenis transaksi. Walau bagaimanapun, anda boleh mencipta berbilang garisan kos untuk jenis transaksi yang sama dan menetapkan atribut yang dikehendaki untuk garisan ini.
7. Pada tab **Kategori**, pilih kategori projek yang akan disertakan dalam baris templat kos.
8. Pada tab **Umum**, pilih jika baris ini akan dimasukkan dalam pengiraan peratusan siap.
9. Pilih kaedah kos untuk siap yang digunakan apabila mengira peratusan siap.


[!INCLUDE[footer-include](../includes/footer-banner.md)]