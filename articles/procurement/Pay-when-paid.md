---
title: Bayar apabila pembayaran vendor berbayar
description: Topik ini menerangkan cara menggunakan senario gaji apabila dibayar (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525389"
---
# <a name="pay-when-paid-vendor-payments"></a>Bayar apabila pembayaran vendor berbayar

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menerangkan cara menggunakan senario gaji apabila dibayar (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Mencipta pesanan pembelian yang mempunyai terma PWP

Apabila anda menyiarkan invois daripada vendor, jika vendor tertakluk kepada terma PWP, terma tersebut ditunjukkan pada baris pesanan pembelian (PO). Untuk mencipta PO yang mempunyai terma PWP, ikuti langkah ini.

1. Dalam Microsoft Dynamics 365 Kewangan, ikuti salah satu langkah berikut:

    - Pergi ke **Perolehan dan penyumberan** \> **Pesanan pembelian** \> **Semua pesanan pembelian**. Pada Anak Tetingkap Tindakan, pilih **Baharu**. Dalam kotak **dialog Cipta pesanan** pembelian, pilih vendor yang terma PWP disediakan pada projek, masukkan maklumat lain yang diperlukan kemudian pilih **OK**.
    - Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek**. Pada Anak Tetingkap Tindakan, pada tab **Urus**, pilih **Tugas Item**. Pilih pesanan pembelian. Pilih vendor yang mana terma PWP disediakan pada projek, dan kemudian pilih **OK**.

2. Pada halaman **Beli pesanan**, pada **Tab Pantas pesanan** Pembelian, pilih **Tambah baris** untuk mencipta talian pesanan pembelian.
3. Pilih nombor item atau kategori perolehan dan masukkan butiran lain yang diperlukan. Semak butiran baris PO untuk vendor.

    Pilihan **Bayar apabila dibayar** dipilih secara automatik dan nilai dalam medan **peratusan ambang PWP** akan disalin secara automatik daripada medan **peratusan ambang PWP** pada halaman **Projek**.

4. Jika anda tidak mahu menggunakan terma PWP kepada vendor untuk baris PO, kosongkan pilihan **bayar apabila dibayar**. Dalam kes ini, **medan peratusan** ambang PWP untuk talian PO akan ditetapkan semula kepada **0** (sifar).
5. Pada halaman **Beli pesanan**, pada Anak Tetingkap Tindakan, pada tab **Pembelian**, pilih **Sahkan** untuk mengesahkan pesanan pembelian.
6. Pada Anak Tetingkap Tindakan, pada tab **Invois**, pilih **Invois** untuk menjana invois bagi pesanan pembelian.

## <a name="create-a-project-invoice-proposal"></a>Cipta cadangan invois projek

Cadangan invois projek digunakan untuk membuat invois projek untuk pelanggan. Dalam senario PWP, pembayaran vendor bergantung kepada bayaran pelanggan mengikut tetapan PWP. Walau bagaimanapun, terdapat pilihan yang membolehkan anda melepaskan pembayaran tanpa pembayaran pelanggan seperti yang anda perlukan. Untuk membuat invois projek untuk pelanggan, ikut langkah ini.

1. Dalam aplikasi customer engagement, pergi ke **Projek Projek** \> **dan** pilih projek.
2. Pada tab **Sebenar**, pilih baris sebenar yang dijana oleh PO yang mempunyai **jenis transaksi jualan** belum dibil. Kemudian pilih **Sedia untuk invois**.
3. Pergi ke **kontrak** Projek Jualan \>**Jualan** \>**·**, dan pilih kontrak projek.
4. Pada Anak Tetingkap Tindakan, pilih **Invois** untuk menjana invois pelanggan.
5. Dalam Kewangan, pergi ke **Pengurusan projek dan perakaunan** \> **Import Berkala** \> **dari jadual** pementasan, dan pilih **OK** untuk menjana jurnal integrasi operasi Projek.
6. Pergi ke **Pengurusan projek dan perakaunan** \> **Invois projek** \> **Cadangan** invois projek, dan pilih **Hantar** untuk menyiarkan cadangan invois yang dihasilkan untuk projek.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kemas kini pembayaran pelanggan dan bayar vendor tersebut

Apabila vendor menyelesaikan kerjanya pada projek dan menghantar invois kepada anda, anda mesti menyemak status projek dan invois pelanggan untuk menentukan sama ada terma PWP dipenuhi untuk projek itu. Jika terma PWP untuk vendor dipenuhi, anda boleh menentukan baris yang ada pada invois vendor perlu dibayar, berdasarkan pembayaran pelanggan untuk projek tersebut. Jika anda memutuskan untuk membayar vendor walaupun terma PWP tidak dipenuhi, anda boleh mengganti terma PWP pada halaman **Invois vendor dengan bayar apabila dibayar**.

1. Dalam Kewangan, pergi ke **Projek pengurusan dan perakaunan** \> **Projek** \> **Semua projek**, dan pilih projek.
2. Pada Anak Tetingkap Tindakan, pilih **Kawalan**, kemudian pilih **Invois vendor** untuk menunjukkan semua invois vendor yang telah dijana untuk projek.
3. Pada halaman **Invois vendor dengan bayar apabila dibayar**, dalam medan carian, masukkan nilai untuk mencari invois vendor yang anda mahu semak semula dan kemudian pilih **Carian**.
4. Pilih pilihan **Bayar apabila dibayar** untuk melihat invois PWP sahaja.
5. **Pada baris invois Vendor** Tab Pantas, pilih baris yang ingin anda lepaskan untuk pembayaran.
6. Pilih **Pelepasan pembayaran** vendor. Pilihan **Bayar apabila dibayar** dikosongkan dan nilai medan **Bersedia untuk pembayaran** ditukar kepada **Ya**.
