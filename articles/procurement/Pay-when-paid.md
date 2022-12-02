---
title: Pembayaran vendor bayar apabila dibayar
description: Topik ini menerangkan cara menggunakan senario bayar apabila dibayar (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Pembayaran vendor bayar apabila dibayar

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menerangkan cara menggunakan senario bayar apabila dibayar (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Cipta pesanan pembelian yang mempunyai terma PWP

Apabila anda menyiarkan invois daripada vendor, jika vendor tertakluk kepada terma PWP, terma tersebut ditunjukkan pada baris pesanan pembelian (PO). Untuk mencipta PO yang mempunyai terma PWP, ikuti langkah ini.

1. Dalam Microsoft Dynamics 365 Finance, ikut satu atau lebih langkah ini:

    - Pergi ke **Perolehan dan penyumberan** \> **Pesanan pembelian** \> **Semua pesanan pembelian**. Pada Anak Tetingkap Tindakan, pilih **Baharu**. Dalam kotak dialog **Cipta pesanan pembelian**, pilih vendor yang terma PWP disediakan pada projek, masukkan maklumat lain yang diperlukan dan kemudian pilih **OK**.
    - Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek**. Pada Anak Tetingkap Tindakan, pilih tab **Urus**, pilih **Tugas item**. Pilih pesanan pembelian. Pilih vendor yang terma PWP disediakan pada projek dan kemudian pilih **OK**.

2. Pada halaman **Pesanan pembelian**, pada Fast Tab **Baris pesanan pembelian**, pilih **Tambah baris** untuk mencipta baris perintah pembelian.
3. Pilih nombor item atau kategori perolehan dan masukkan butiran lain yang diperlukan. Semak butiran baris PO untuk vendor.

    Pilihan **Bayar apabila dibayar** dipilih secara automatik dan nilai dalam medan **peratusan ambang PWP** akan disalin secara automatik daripada medan **peratusan ambang PWP** pada halaman **Projek**.

4. Jika anda tidak mahu menggunakan terma PWP kepada vendor untuk baris PO, kosongkan pilihan **bayar apabila dibayar**. Dalam kes ini, medan **peratusan ambang PWP** untuk baris PO akan ditetapkan semula kepada **0** (sifar).
5. Pada halaman **Pesanan pembelian**, pada Anak Tetingkap Tindakan, pada tab **Beli**, pilih **Sahkan** untuk mengesahkan pesanan pembelian.
6. Pada Anak Tetingkap Tindakan, pada tab **Invois**, pilih **Invois** untuk menjana invois untuk pesanan pembelian.

## <a name="create-a-project-invoice-proposal"></a>Cipta cadangan invois projek

Cadangan invois projek digunakan untuk mencipta invois projek untuk pelanggan. Dalam senario PWP, pembayaran vendor bergantung kepada pembayaran pelanggan mengikut tetapan PWP. Walau bagaimanapun, terdapat pilihan yang membolehkan anda mengeluarkan bayaran tanpa bayaran pelanggan seperti yang anda perlukan. Untuk mencipta invois projek untuk pelanggan, ikut langkah ini.

1. Dalam aplikasi Customer Engagement, pergi ke **Projek** \> **Projek** dan pilih projek.
2. Pada tab **Aktual**, pilih baris aktual yang dijana oleh PO yang mempunyai jenis transaksi **Jualan belum dibilkan**. Kemudian pilih **Sedia untuk invois**.
3. Pergi ke **Jualan** \> **Jualan** \> **Kontrak projek** dan pilih kontrak projek.
4. Pada Anak Tetingkap Tindakan, pilih **Invois** untuk menjana invois pelanggan.
5. Dalam Finance, pergi ke **Pengurusan projek dan perakaunan** \> **Berkala** \> **Import daripada jadual pemeringkatan** dan pilih **OK** untuk menjana jurnal integrasi Project Operations.
6. Pergi ke **Pengurusan projek dan perakaunan** \> **Invois projek** \> **Cadangan invois projek** dan pilih **Siar** untuk menyiarkan cadangan invois yang dijana untuk projek.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kemas kini pembayaran pelanggan dan bayar vendor tersebut

Apabila vendor melengkapkan kerjanya pada projek dan menghantar invois kepada anda, anda mesti menyemak semula status projek dan invois pelanggan untuk menentukan sama ada terma PWP dipenuhi untuk projek tersebut. Jika terma PWP untuk vendor dipenuhi, anda boleh menentukan baris yang ada pada invois vendor perlu dibayar, berdasarkan pembayaran pelanggan untuk projek tersebut. Jika anda memutuskan untuk membayar vendor walaupun terma PWP tidak dipenuhi, anda boleh mengganti terma PWP pada halaman **Invois vendor dengan bayar apabila dibayar**.

1. Dalam Finance, pergi ke **Pengurusan projek dan perakaunan** \> **Projek** \> **Semua projek** dan pilih projek.
2. Pada Anak Tetingkap Tindakan, pilih **Kawalan** dan kemudian pilih **Invois vendor** untuk menunjukkan semua invois vendor yang telah dijana untuk projek.
3. Pada halaman **Invois vendor dengan bayar apabila dibayar**, dalam medan carian, masukkan nilai untuk mencari invois vendor yang anda mahu semak semula dan kemudian pilih **Carian**.
4. Pilih pilihan **Bayar apabila dibayar** untuk melihat hanya invois PWP.
5. Pada Fast Tab **Baris invois vendor**, pilih baris yang anda mahu keluarkan untuk bayaran.
6. Pilih **Keluarkan bayaran vendor**. Pilihan **Bayar apabila dibayar** dikosongkan dan nilai medan **Bersedia untuk pembayaran** ditukar kepada **Ya**.
