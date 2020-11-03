---
title: Pendahuluan tunai
description: Topik ini memberikan maklumat tentang pendahuluan tunai.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081111"
---
# <a name="cash-advance"></a>Pendahuluan tunai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Pendahuluan tunai membolehkan pekerja meminjam wang daripada syarikat mereka sebelum menanggung sebarang perbelanjaan. Apabila pendahuluan tunai yang diminta diluluskan dan dibayar, pekerja boleh menggunakan wang tersebut untuk perbelanjaan perniagaan yang mungkin akan ditanggung. 

## <a name="create-and-submit-a-cash-advance-request"></a>Cipta dan serahkan permintaan pendahuluan tunai

1. Di bawah **Perbelanjaan Saya** , pilih **Pendahuluan tunai** > **Baharu** untuk mencipta pendahuluan tunai baharu. 
2. Pada halaman **Permintaan pendahuluan tunai baharu** , masukkan tujuan perbelanjaan dan pilih lokasi tempat perbelanjaan akan ditanggung.
3. Masukkan jumlah yang diminta dan mata wang, dan kemudian pilih **Simpan**. 
4. Apabila anda bersedia untuk menyerahkan permintaan pendahuluan tunai, pada halaman **Permintaan pendahuluan tunai** , pilih **Aliran kerja** > **Serah**.

## <a name="modify-a-cash-advance-request"></a>Ubah suai permintaan pendahuluan tunai

Anda boleh mengubah suai permintaan pendahuluan tunai jika ia belum diserahkan untuk kelulusan.

1. Di bawah **Perbelanjaan Saya: Pendahuluan Tunai** , cari dan pilih pendahuluan tunai yang anda mahu edit.
2. Pilih **Edit** dan buat perubahan yang perlu pada permintaan pendahuluan tunai. 
3. Pilih **Simpan dan tutup**.


## <a name="view-cash-advance-requests"></a>Lihat permintaan pendahuluan tunai
Anda boleh menyemak senarai semua pendahuluan tunai yang dalam draf, diserahkan, dalam semakan atau dibayar di bawah **Perbelanjaan Saya: Pendahuluan Tunai**. 

## <a name="approve-cash-advance-requests"></a>Luluskan permintaan pendahuluan tunai

Pengurus atau pengguna yang dikonfigurasikan sebagai pelulus dalam aliran kerja akan dapat meluluskan pendahuluan tunai yang diserahkan kepada mereka untuk disemak. 

1. Untuk meluluskan pendahuluan tunai, di bawah **Proses pendahuluan tunai** , pilih **Pendahuluan tunai untuk semakan saya**.
2. Pilih pendahuluan tunai yang anda perlu semak dan pilih **Luluskan**.  

## <a name="pay-cash-advances"></a>Bayar pendahuluan tunai 
Prosedur berikut biasanya diselesaikan oleh akauntan atau pengguna dengan keizinan perakaunan.

1. Untuk menyiarkan pendahuluan tunai yang diluluskan, pilih **Pendahuluan tunai yang diluluskan** dan kemudian pilih **Bayar dan pindahkan**.  
2. Berikan butiran jurnal untuk pendahuluan tunai dan kemudian pilih **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Serahkan laporan perbelanjaan terhadap pendahuluan tunai yang telah dibayar 

Apabila anda mencipta dan menyerahkan laporan perbelanjaan bagi pendahuluan tunai yang anda telah terima, perbelanjaan akan diselaraskan secara automatik terhadap pendahuluan tersebut. Jika pendahuluan tunai anda lebih besar daripada jumlah yang dibelanjakan, anda mesti mengembalikan baki kepada syarikat menggunakan kategori perbelanjaan **Pulangan tunai**. Jika pendahuluan tunai yang telah dibayar syarikat adalah kurang daripada jumlah yang anda belanjakan, syarikat mesti membayar balik baki tersebut kepada anda. 

### <a name="example"></a>Contoh
Anda merancang untuk membuat perjalanan bagi satu persidangan dari Seattle ke New York City. Anda membuat permintaan pendahuluan tunai untuk 3000.00 USD kerana anda telah menganggarkan kos tiket persidangan, penerbangan, hotel, makanan dan teksi yang lebih kurang jumlah ini. Anda tidak akan dibayar melainkan pengurus anda meluluskan permintaan ini. Selepas pengurus anda meluluskan, pendahuluan tunai yang diminta dibayar sebanyak 3000.00 USD ke dalam akaun bank anda. Anda kemudiannya menghadiri persidangan itu. Selepas menyelesaikan perjalanan, anda mendapati bahawa jumlah perbelanjaan hanya 2790.00 USD. Pilih **Tunai** dalam medan **Kaedah pembayaran** dan serahkan perbelanjaan anda untuk 2790.00 USD. Jumlah perbelanjaan yang diserahkan anda dilaraskan secara automatik dengan pendahuluan tunai sebanyak 3000.00 USD yang dipinjamkan kepada anda. Anda kini berhutang sebanyak 210.00 USD (3000.00-2790.00) kepada syarikat, yang anda boleh kembali kepada syarikat menggunakan kategori perbelanjaan **Pulangan tunai**. 
