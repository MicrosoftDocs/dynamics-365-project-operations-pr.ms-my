---
title: Sediakan pengekalan vendor
description: Topik ini menerangkan cara menyediakan pengekalan vendor.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594612"
---
# <a name="set-up-vendor-retention"></a>Sediakan pengekalan vendor

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini memberikan maklumat tentang cara menyediakan pengekalan vendor.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Sediakan akaun pengekalan vendor dalam lejar Am

1. Dalam Dynamics 365 Finance, pergi ke **Lejar am** > **Penyediaan penyiaran** > **Akaun untuk transaksi automatik**.
2. Tambah baris baharu.
3. Dalam medan **Jenis penyiaran**, pilih **Pengekalan vendor**.
4. Pilih akaun utama untuk penyiaran pengekalan vendor.

## <a name="create-vendor-retention-terms"></a>Cipta terma pengekalan vendor

Gunakan halaman **Terma pengekalan vendor** untuk menyediakan dan mengekalkan terma pengekalan pembayaran vendor. Masukkan peratusan pembayaran vendor untuk dikekalkan dan peratusan jumlah yang dikekalkan sebelum ini untuk dilepaskan. Jumlah dikekalkan secara automatik pada invois vendor sehingga kontrak mencapai tahap penyelesaian yang ditentukan. Selepas terma pengekalan disediakan untuk vendor, anda boleh menggunakannya ke sebarang projek yang vendor gunakan.

1. Dalam kewangan, pergi ke **Pengurusan projek dan perakaunan** > **Sediakan** > **Pengekalan** > **Terma pengekalan pembayaran vendor**.
2. Pilih **Baharu** untuk menambah terma pengekalan vendor yang baharu. Nilai dalam medan **ID Peraturan** untuk terma baharu dimasukkan secara automatik. 
3. Dalam medan **Perihalan**, masukkan nama deskriptif untuk terma baharu.
4. Pada tab  **Terma**, pilih  **Tambah baris**  untuk memasukkan terma pengekalan vendor.
5. Dalam medan  **Peratusan unit dihantar**, masukkan peratusan pelengkapan untuk peraturan. Jumlah dikekalkan secara automatik pada invois vendor sehingga projek peringkat pelengkapan adalah bersamaan dengan peratusan yang anda masukkan. Contohnya, jika anda memasukkan 50.00, jumlah dikekalkan sehingga projek tersebut 50 peratus selesai.
6. Dalam medan  **Peratusan untuk dikekalkan**, masukkan peratusan jumlah invois vendor untuk dikekalkan. Contohnya, jika anda memasukkan 10.00 dalam medan ini, 10 peratus daripada jumlah pada invois vendor dikekalkan sehingga projek mencapai peratusan pelengkapan yang anda pilih dalam medan  **Peratusan unit dihantar**.
7. Dalam medan  **Peratusan untuk dilepaskan**, masukkan peratusan bagi mana-mana jumlah yang dikekalkan sebelum ini untuk dilepaskan pada peringkat pelengkapan projek yang dipilih.

> [!NOTE]
> Jika anda mempunyai lebih daripada satu pencapaian untuk peringkat pelengkapan projek yang berbeza, masukkan baris terma pengekalan vendor yang berasingan untuk setiap peraturan pengekalan. Setiap baris boleh menentukan peratusan yang berbeza untuk dikekalkan dan peratusan yang berbeza untuk dilepaskan bagi setiap peringkat yang ditetapkan untuk pelengkapan projek..

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Sediakan perjanjian vendor untuk projek

Sediakan terma pengekalan vendor yang digunakan untuk projek itu. Terma pengekalan vendor juga dipaparkan pada pesanan pembelian yang anda cipta untuk vendor.

1. Dalam Kewangan, pergi ke **Pengurusan projek dan perakaunan** > **Projek** > **Semua projek**. 
2. Pilih projek dan pada Anak Tetingkap Tindakan, pilih **Kumpulan projek** > **Perjanjian vendor**.
3. Pada halaman **Perjanjian vendor**, tambah baris baharu.
4. Dalam medan **Kod akaun**, pilih salah satu daripada pilihan berikut:
   - **Jadual**: Terma pengekalan vendor digunakan pada vendor tunggal.
   - **Kumpulan**: Terma pengekalan vendor digunakan pada semua vendor dalam kumpulan vendor.
   - **Semua**: Terma pengekalan vendor digunakan pada semua vendor.
5. Dalam medan **Vendor/Kumpulan vendor**, pilih vendor atau kumpulan vendor yang menggunakan terma pengekalan vendor. Jika anda memilih **Semua** dalam langkah sebelum ini, medan ini tidak tersedia.
6. Dalam medan **Terma pengekalan vendor**, pilih ID peraturan terma pengekalan untuk digunakan pada vendor ini.

