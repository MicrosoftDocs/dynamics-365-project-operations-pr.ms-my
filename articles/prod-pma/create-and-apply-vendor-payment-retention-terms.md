---
title: Cipta dan gunakan terma pengekalan pembayaran vendor
description: Topik ini memberikan maklumat tentang cara menyediakan dan mengekalkan terma pengekalan untuk pembayaran vendor.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 4ff725512aa0bcc87ff4670d6bb072f3bf780786c1f71b332914887f4d4ccf13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991227"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Cipta dan gunakan terma pengekalan pembayaran vendor

[!include [banner](../includes/banner.md)] 

Menyediakan terma pengekalan pembayaran vendor untuk projek berguna apabila organisasi anda mahu mengekalkan sebahagian daripada pembayaran yang dibuat kepada vendor. Contohnya, apabila anda ingin menangguhkan pembayaran kepada vendor sehingga produk yang dihantar memenuhi jangkaan anda. Terma pengekalan pembayaran vendor dapat ditentukan semasa anda merundingkan kontrak vendor.

## <a name="create-vendor-payment-retention-terms"></a>Cipta terma pengekalan pembayaran vendor

Anda boleh memasukkan peratusan pembayaran vendor untuk pengekalan dan peratusan jumlah dikekalkan sebelumnya yang akan dikeluarkan. Jumlah dikekalkan secara automatik pada invois vendor sehingga kontrak mencapai tahap penyelesaian yang ditentukan. Selepas anda menyediakan terma pengekalan, anda boleh menggunakannya pada sebarang projek untuk vendor tersebut.

Gunakan langkah berikut untuk menyediakan dan mengekalkan terma pengekalan untuk pembayaran vendor. 

1. Pergi ke **Pengurusan dan perakaunan projek** > **Pengekalan** > **Terma pengekalan pembayaran vendor**.
2. Pilih **Baharu** untuk menambah terma pengekalan vendor yang baharu. Nilai **ID peraturan** untuk terma baharu akan dimasukkan secara automatik. 
3. Masukkan perihalan ringkas dalam medan **Perihalan** dan pada FastTab **Terma**, pilih **Tambah baris** untuk memasukkan nilai terma bagi yang berikut:

   - **Peratusan unit yang dihantar**: Masukkan peratusan siap untuk terma tersebut. Jumlah dikekalkan secara automatik pada invois vendor sehingga peringkat penyiapan projek sama dengan peratusan yang ditentukan. Contohnya, jika anda memasukkan 50.00, jumlah dikekalkan sehingga projek tersebut 50 peratus selesai.
   - **Peratusan untuk dikekalkan**: Masukkan peratusan jumlah invois vendor untuk dikekalkan. Contohnya, jika anda memasukkan 10.00, maka 10 peratus daripada jumlah pada invois vendor dikekalkan sehingga projek mencapai peratusan penyiapan seperti yang ditetapkan dalam **medan Peratusan unit yang dihantar**.
   - **Peratusan untuk dikeluarkan**: Pilih **Tambah baris** untuk memasukkan peratusan mana-mana jumlah dikekalkan sebelum ini yang akan dikeluarkan untuk peringkat penyiapan projek yang dipilih.

> [!NOTE]
> Jika anda mempunyai lebih daripada satu pencapaian untuk peringkat penyiapan projek yang berbeza, masukkan baris terma pengekalan vendor yang berasingan bagi setiap peraturan pengekalan. Setiap baris boleh menentukan peratusan pengekalan yang berbeza dan peratusan keluaran yang berbeza bagi setiap peringkat penyiapan projek yang ditetapkan.

Selepas anda mencipta terma pengekalan vendor untuk vendor, anda boleh menggunakan terma tersebut untuk projek.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Gunakan terma pengekalan vendor pada projek

1. Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Semua projek** dan buka projek dari halaman senarai projek.
2. Pada FastTab **Perjanjian vendor**, pilih **Tambah baris**.
3. Dalam **medan Kod akaun**, pilih salah satu daripada pilihan berikut: 

   - **Jadual**: Terma pengekalan vendor digunakan pada vendor tunggal.
   - **Kumpulan**: Terma pengekalan vendor digunakan pada semua vendor dalam kumpulan vendor.
   - **Semua**: Terma pengekalan vendor digunakan pada semua vendor.

4. Dalam **medan Vendor/Kumpulan vendor**, pilih vendor atau kumpulan vendor yang menggunakan terma pengekalan vendor. Jika anda memilih **Semua** dalam langkah sebelumnya, medan ini tidak tersedia.
5. Dalam **medan Terma pengekalan vendor**, pilih terma pengekalan yang anda cipta dalam prosedur sebelumnya.
6. Jika projek tersebut juga mempunyai terma bayar apabila dibayar (PWP) yang disediakan untuk vendor, masukkan peratusan ambang untuk projek dalam medan **Peratusan ambang PWP**.

Terma pengekalan vendor juga dipaparkan pada pesanan pembelian yang anda cipta untuk vendor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]