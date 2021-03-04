---
title: Pendahuluan tunai
description: Topik ini memberikan maklumat tentang pendahuluan tunai.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098895"
---
# <a name="cash-advance"></a>Pendahuluan tunai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Pendahuluan tunai membolehkan pekerja meminjam wang daripada syarikat mereka sebelum menanggung sebarang perbelanjaan. Apabila pendahuluan tunai yang diminta diluluskan dan dibayar, pekerja boleh menggunakan wang tersebut untuk perbelanjaan perniagaan yang mungkin akan ditanggung. 

## <a name="create-and-submit-a-cash-advance-request"></a>Cipta dan serahkan permintaan pendahuluan tunai
Untuk mencipta pendahuluan tunai baharu dan serahkan permintaan pendahuluan tunai, lakukan yang berikut: 

1. Di bawah **Perbelanjaan Saya**, pilih **Pendahuluan tunai** > **Baharu**. 
2. Pada halaman **Permintaan pendahuluan tunai baharu**, masukkan tujuan perbelanjaan dan pilih lokasi tempat perbelanjaan akan ditanggung.
3. Masukkan jumlah yang diminta dan mata wang, dan kemudian pilih **Simpan**. 
4. Apabila anda bersedia untuk menyerahkan permintaan pendahuluan tunai, pada halaman **Permintaan pendahuluan tunai**, pilih **Aliran kerja** > **Serah**.

## <a name="modify-a-cash-advance-request"></a>Ubah suai permintaan pendahuluan tunai

Anda boleh mengubah suai permintaan pendahuluan tunai jika ia belum diserahkan untuk kelulusan.

1. Di bawah **Perbelanjaan Saya: Pendahuluan Tunai**, cari dan pilih pendahuluan tunai yang anda mahu edit.
2. Pilih **Edit** dan buat perubahan yang perlu pada permintaan pendahuluan tunai. 
3. Pilih **Simpan dan tutup**.


## <a name="view-cash-advance-requests"></a>Lihat permintaan pendahuluan tunai
Anda boleh menyemak senarai semua pendahuluan tunai yang dalam draf, diserahkan, dalam semakan atau dibayar di bawah **Perbelanjaan Saya: Pendahuluan Tunai**. 

## <a name="approve-cash-advance-requests"></a>Luluskan permintaan pendahuluan tunai

Pengurus atau pengguna yang dikonfigurasikan sebagai pelulus dalam aliran kerja akan dapat meluluskan pendahuluan tunai yang diserahkan kepada mereka untuk disemak. 

1. Untuk meluluskan pendahuluan tunai, di bawah **Proses pendahuluan tunai**, pilih **Pendahuluan tunai untuk semakan saya**.
2. Pilih pendahuluan tunai yang anda perlu semak dan pilih **Luluskan**.  

## <a name="pay-cash-advances"></a>Bayar pendahuluan tunai 
Prosedur berikut biasanya diselesaikan oleh akauntan atau pengguna dengan keizinan perakaunan.

1. Untuk menyiarkan pendahuluan tunai yang diluluskan, pilih **Pendahuluan tunai yang diluluskan** dan kemudian pilih **Bayar dan pindahkan**.  
2. Berikan butiran jurnal untuk pendahuluan tunai dan kemudian pilih **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Serahkan laporan perbelanjaan terhadap pendahuluan tunai yang telah dibayar 

Apabila anda mencipta dan menyerahkan laporan perbelanjaan untuk pendahuluan tunai yang telah anda terima, perbelanjaan akan dilaraskan secara automatik terhadap pendahuluan. Jika pendahuluan tunai anda lebih besar daripada jumlah yang dibelanjakan, anda mesti mengembalikan baki kepada syarikat menggunakan kategori perbelanjaan **Pulangan tunai**. Jika pendahuluan tunai berbayar syarikat adalah kurang daripada jumlah yang anda telah belanjakan, syarikat mesti membayar balik baki tersebut. 

### <a name="example"></a>Contoh
Anda merancang untuk melakukan perjalanan dari Seattle ke Bandar New York untuk persidangan. Anda mencipta permintaan pendahuluan tunai untuk 3000.00 USD berdasarkan anggaran kos tiket persidangan, penerbangan, hotel, makanan dan teksi. Anda tidak akan dibayar melainkan pengurus anda meluluskan permintaan ini. Selepas pengurus anda meluluskan, pendahuluan tunai yang diminta dibayar sebanyak 3000.00 USD ke dalam akaun bank anda. Anda kemudiannya menghadiri persidangan itu. Selepas menyelesaikan perjalanan, anda mendapati bahawa jumlah perbelanjaan hanya 2790.00 USD. Pilih **Tunai** dalam medan **Kaedah pembayaran** dan serahkan perbelanjaan anda untuk 2790.00 USD. Jumlah perbelanjaan yang diserahkan anda dilaraskan secara automatik dengan pendahuluan tunai sebanyak 3000.00 USD yang dipinjamkan kepada anda. Anda kini berhutang baku 210.00 USD (3000.00 - 2790.00), yang anda boleh kembalikan kepada syarikat menggunakan kategori perbelanjaan **Pulang tunai**.

