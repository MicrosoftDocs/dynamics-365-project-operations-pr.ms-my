---
title: Cipta invois pelanggan dan vendor antara syarikat
description: Topik ini menyediakan maklumat tentang cara mencipta invois pelanggan dan vendor antara syarikat.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9448cb29adb4206efaabe3f313a1f619cd32b9be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591507"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Cipta invois pelanggan dan vendor antara syarikat

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Akauntan projek dalam entiti sah pinjaman mencipta invois pelanggan antara syarikat untuk kos projek yang dipindahkan ke entiti pinjaman. Selepas invois pelanggan antara syarikat telah diluluskan dan disiarkan, entiti sah pinjaman menghantar invois antara syarikat ke entiti sah pinjaman.

Akauntan projek untuk entiti sah pinjaman boleh menyediakan proses kelompok untuk menjana invois antara syarikat secara berulang. Akauntan projek menentukan kriteria, seperti projek khusus, untuk mencipta invois antara syarikat dalam kelompok.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Cipta invois pelanggan antara syarikat untuk transaksi projek secara manual 

Gunakan prosedur ini untuk mencipta invois pelanggan antara syarikat untuk transaksi projek secara manual. Cari masa yang disiarkan oleh pekerja pada projek dalam entiti sah pinjaman dan untuk perbelanjaan yang dikenakan oleh entiti sah anda bagi pihak entiti sah pinjaman. Anda boleh mencari dengan nama entiti sah, nombor kontrak projek, nombor projek, julat tarikh atau sebarang gabungan pilihan ini. Dalam hasil carian, pilih transaksi untuk menambah kepada invois antara syarikat. 

Langkah berikut mesti dilakukan dalam entiti perundangan pemberian pinjaman. 

1. Dalam Dynamics 365 Finance, pergi ke **Pengurusan Projek dan perakaunan** > **Invois** > **projek Invois pelanggan antara syarikat**. Pada halaman senarai **Invois pelanggan antara syarikat**, pada Anak Tetingkap Tindakan, pilih **Baharu.**
2. Pada halaman **Cipta invois antara syarikat**, dalam medan **Entiti sah**, pilih entiti sah pinjaman.
3. Pilihan: Masukkan kontrak projek tertentu dan nombor projek.
4. Kecilkan carian dengan memilih julat tarikh. Masukkan tarikh tertentu dalam medan **Tarikh mula** dan **Tarikh tamat**. Hanya transaksi antara syarikat yang disiarkan dalam julat tarikh ini dipaparkan dalam hasil carian.
5. Tetapkan **Parameter garisan jurnal lanjutan projek** ke **Ya** dan pilih **Carian**.
6. Dalam hasil carian, pilih transaksi untuk memasukkan dalam cadangan invois antara syarikat dan kemudian pilih **OK**.
7. Pada halaman **Invois pelanggan antara syarikat**, transaksi projek antara syarikat yang anda pilih daripada hasil carian dipaparkan. Untuk mengubah suai transaksi sebelum anda menghantar invois kepada entiti sah pinjaman, lakukan perkara berikut:
  
    1. Pada halaman **invois pelanggan antara syarikat**, buka butiran invois dan kemudian pilih **Tambah baris**.
    2. Untuk mengalih keluar baris, pilih baris dan kemudian klik **Alih keluar**.
    3. Lihat komen, sebab, dimensi kewangan dan maklumat lain tentang baris yang dipilih pada butiran baris invois.
    
8. Untuk menyiarkan invois pelanggan antara syarikat, pada Anak Tetingkap Tindakan, pilih **Siar**.

> [!NOTE]
> Jika organisasi anda memerlukan invois antara syarikat disemak sebelum invois itu disiarkan, pentadbir sistem mungkin menyediakan aliran kerja untuk invois antara syarikat. Jika aliran kerja tidak disediakan untuk invois antara syarikat, anda boleh menyiarkan invois antara syarikat.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Cipta kerja kelompok untuk invois antara syarikat

Anda boleh mencipta berbilang invois antara syarikat pada masa yang sama untuk semua entiti sah pinjaman. Menggunakan fungsi carian, anda boleh contohnya, mencari semua transaksi yang disiarkan oleh pekerja yang meminjam dan berkaitan dengan projek yang diuruskan oleh entiti sah yang lain. Kemudian, untuk setiap entiti sah pinjaman, anda boleh mencipta invois antara syarikat untuk transaksi yang diberikan dalam hasil carian.

1. Pergi ke **Pengurusan projek dan perakaunan** > **Berkala** > **Invois projek** > **Cipta invois pelanggan antara syarikat**.
2. Pada halaman **Cipta invois antara syarikat**, dalam medan **Syarikat**, pilih entiti sah untuk diinvois. Jika anda tidak memilih syarikat, semua transaksi yang memenuhi kriteria carian dipaparkan untuk semua entiti sah pinjaman.
3. Dalam **Cipta satu invois per**, pilih sama ada mahu mencipta invois untuk transaksi antara syarikat berdasarkan projek atau berdasarkan entiti sah pinjaman.
4. Pilihan: Untuk memilih kontrak projek dan projek tertentu untuk mencipta invois antara syarikat untuk, klik **Pilih**. Pada halaman **Pertanyaan**, dalam medan **Kriteria**, pilih kontrak projek, nombor projek atau kedua-duanya dan kemudian pilih **OK**.
5. Pada tab **kelompok**, sediakan proses kelompok untuk mencipta invois antara syarikat secara berulang. Untuk mendapatkan maklumat lanjut, lihat [Serahkan kerja pemprosesan kelompok daripada borang](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Untuk menyiarkan invois antara syarikat, pada Anak Tetingkap Tindakan, pilih **Siar**.

> [!NOTE]
> Jika organisasi anda memerlukan invois antara syarikat disemak sebelum invois itu disiarkan, pentadbir sistem mungkin menyediakan aliran kerja untuk invois antara syarikat. Jika aliran kerja tidak disediakan untuk invois antara syarikat, anda boleh menyiarkan invois antara syarikat.

## <a name="post-the-intercompany-vendor-invoice"></a>Siarkan invois vendor antara syarikat

Akauntan projek dalam entiti sah pinjaman boleh menyemak invois vendor antara syarikat yang belum selesai apabila invois pelanggan antara syarikat yang berkaitan disiarkan. Dalam Kewangan, dalam entiti sah pinjaman, pergi ke **Akaun belum bayar** > **Invois** > **Invois vendor yang belum selesai**. Nombor invois yang belum selesai akan dipadankan dengan nombor invois pelanggan antara syarikat. Sahkan bahawa invois tersebut betul dan kemudian siarkan invois. Menyiarkan invois vendor antara syarikat mencipta sublejar projek dan transaksi lejar umum yang menunjukkan kos transaksi dalam entiti sah pinjaman.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
