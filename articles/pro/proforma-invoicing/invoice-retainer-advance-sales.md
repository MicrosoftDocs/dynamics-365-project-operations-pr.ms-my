---
title: Menginvois retainer atau pendahuluan
description: Artikel ini memberikan maklumat tentang cara menginvois penahan atau pendahuluan dalam Operasi Projek.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 044186d5c7759866dec3883103acec19cb571c11
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914505"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Menginvois retainer atau pendahuluan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menyokong kontrak berasaskan pendahuluan dan pendahuluan satu kali. Pada kontrak projek, anda boleh merekod jadual retainer atau pendahuluan satu kali. Walau bagaimanapun, rakaman pada peringkat kontrak projek tidak akan membuat retainer atau pendahuluan boleh digunakan. Untuk menggunakan retainer atau pendahuluan pada invois yang benar-benar mengenakan bayaran kepada pelanggan, retainer atau pendahuluan mestilah diinvois terlebih dahulu.

Lengkapkan langkah yang berikut untuk mengeluarkan invois retainer atau pendahuluan.

1. Pilih **Jualan** > **Pengebilan** > **Retainer dan Pendahuluan**. 
2. Pada halaman **Pendahuluan dan Retainer**, gunakan penapis untuk memilih retainer khusus atau pendahuluan untuk diinvois dan menandakannya sebagai **Bersedia untuk Invois**.
3. Cipta invois sama ada secara manual daripada senarai **Kontrak Projek** atau halaman butiran. Retainer atau pendahuluan ditunjukkan pada invois Draf dalam bahagian **Pendahuluan dan Retainer** pada halaman **Invois**.
4. Sahkan invois. Ini akan membuat retainer atau pendahuluan boleh digunakan. Anda boleh mengesahkan invois pada halaman senarai **Retainer dan Pendahuluan**. Untuk Pendahuluan atau Retainer yang diinvoiskan, jumlah tersedia ditunjukkan dalam grid.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Cipta retainer atau pendahuluan daripada grid Invois

Anda boleh mencipta retainer atau pendahuluan secara langsung pada invois.

1. Pada invois draf, pada subgrid **Pendahuluan dan Retainer**, pilih **Baharu** untuk mencipta retainer atau pendahuluan baharu. 
2. Pada halaman **Cipta pantas**, tambah maklumat yang diperlukan dan kemudian pilih **Simpan**. Retainer atau pendahuluan dibuat pada kontrak projek yang berkaitan dengan invois. Retainer atau pendahuluan secara automatik ditandakan sebagai **Sedia untuk Invois** dan kemudian ditambahkan ke subgrid **Pendahuluan dan Retainer** pada halaman **Invois**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Selaraskan retainer atau pendahuluan yang diinvois

Selepas retainer atau pendahuluan diinvois, ia boleh digunakan atau diselaraskan dengan invois dengan masa, perbelanjaan, pencapaian atau caj berasaskan projek. Pelanggan akan melihat jumlah invois yang dikurangkan oleh jumlah retainer atau pendahuluan yang digunakan pada invois ini.

Pada setiap invois yang dijana untuk kontrak projek yang mempunyai redeomer invois atau pendahuluan, Project Operation secara automatik menggunakan retainer atau pendahuluan kepada invois.

Ini boleh dilihat dalam grid **Retainer dan Pendahuluan yang digunakan** pada halaman **Invois**. Jadual berikut menyediakan maklumat mengenai medan mengenai grid **Retainer dan Pendahuluan Digunakan** halaman **Invois Projek**.

| Medan | Lokasi | Penerangan | Kesan hiliran |
| --- | --- | --- | --- |
| Penerangan | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek** |Medan baca sahaja ini memberikan perihalan retainer atau pendahuluan yang digunakan pada invois ini. Nilai ini tidak dapat diubah pada invois. Nilai ini boleh dikemas kini pada subgrid pada halaman **Kontrak Projek**. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan retainer atau pendahuluan yang digunakan pada invois. |
| Dihantar Pada | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek**  | Medan baca sahaja ini memberikan tarikh invois retainer atau pendahuluan yang digunakan pada invois ini. Nilai ini tidak dapat diubah pada invois. Nilai ini boleh dikemas kini pada subgrid pada halaman **Kontrak Projek**. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan tarikh retainer atau pendahuluan diinvoiskan kali pertama kepada pengguna. |
| Amaun | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek**  | Medan baca sahaja ini memberikan jumlah invois retainer atau pendahuluan yang digunakan pada invois ini. Nilai ini tidak dapat diubah pada invois. Nilai ini boleh dikemas kini pada subgrid pada halaman **Kontrak Projek**. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan jumlah asal retainer atau pendahuluan yang dibayar oleh pelanggan. |
| Amaun Digunakan | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek**  | Medan baca sahaja ini memberikan nilai yang dikira yang meringkaskan jumlah retainer atau pendahuluan yang telah digunakan. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan jumlah daripada retainer atau pendahuluan yang telah digunakan. |
| Amaun Dilanjutkan | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek**  | Medan boleh diedit ini memberikan jumlah invois retainer atau pendahuluan yang sedang digunakan pada invois projek ini. Jumlah ini tidak boleh melebihi jumlah yang boleh didapati pada pendahuluan. Sistem secara automatik mengira ini sebagai perbezaan antara medan **Jumlah** dan **Jumlah digunakan** pada grid. Anda boleh mengurangkan jumlah ini untuk menggunakan kurang daripada jumlah yang ada, tetapi anda tidak boleh menambah jumlah itu untuk menggunakan lebih daripada jumlah yang ada. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan jumlah daripada retainer atau pendahuluan yang sedang digunakan pada invois. |
| Baki Jumlah Retainer. | Grid **Retainer dan Pendahuluan yang Digunakan** pada halaman **Invois Projek**  | Medan baca sahaja ini memberikan nilai kepada jumlah retainer atau pendahuluan yang akan tinggal selepas invois disahkan. | Medan ini boleh dipaparkan kepada pelanggan pada invois bercetak untuk menunjukkan jumlah yang akan tinggal daripada retainer atau pendahuluan selepas disahkan dan dibayar. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]