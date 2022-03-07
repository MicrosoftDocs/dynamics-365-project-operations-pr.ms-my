---
title: Ganti senarai harga jualan projek
description: Topik ini menyediakan maklumat tentang mencipta senarai harga jualan tersuai.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b26947822eb8e87b3b36fcde9c99c6ee69375aa942a5641112b9b1109dcaa26c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009587"
---
# <a name="override-project-sales-price-lists"></a>Ganti senarai harga jualan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

## <a name="customer-specific-project-price-lists"></a>Senarai harga projek khusus pelanggan

Perjanjian harga khusus pelanggan boleh ditetapkan sebagai senarai harga projek pada rekod akaun dalam Dynamics 365 Project Operations.

Untuk menyediakan senarai harga projek khusus pelanggan, dalam kawasan **Jualan**, navigasi ke rekod akaun.

1. Buka halaman senarai **Akaun**.
2. Cari dan klik dua kali rekod pelanggan untuk membuka halaman butiran **Akaun**.
3. Pada tab **Senarai Harga Projek**, pilih **+ Senarai Harga Projek Baharu**.
4. Pada halaman **Senarai Harga Projek Baharu**, pilih senarai harga daripada juntai bawah. Hanya senarai harga yang mempunyai konteks ditetapkan ke **Jualan** dan mata wang yang sepadan dengan mata wang akaun dimasukkan.
5. Namakan perkaitan dan kemudian pilih **Simpan**. Senarai harga projek khusus pelanggan dicipta. Senarai harga ini akan digunakan untuk harga projek lalai pada sebut harga projek atau kontrak yang dicipta untuk pelanggan ini dengan tarikh sebut harga atau kontrak projek yang dicipta berada dalam penguatkuasaan tarikh senarai harga.

## <a name="custom-pricing-on-project-quotes"></a>Penetapan harga tersuai pada sebut harga projek

Pada sebut harga projek, anda boleh mempunyai penetapan harga projek yang bermula dengan senarai harga standard lalai yang dilalaikan daripada pelanggan atau daripada parameter projek.

Apabila anda memerlukan penetapan harga tersuai untuk kerja berkaitan projek pada sebut harga tertentu, anda boleh mendapatkannya daripada senarai harga projek entiti berkaitan.

Lengkapkan langkah berikut untuk menyediakan penetapan harga projek khusus sebut harga.

1. Buka sebut harga projek dan pilih tab **Senarai Harga Projek**.
2. Dalam sub grid, pilih **Cipta penetapan harga tersuai**.

Semua senarai harga projek yang dilampirkan pada sebut harga disalin ke senarai harga baharu. Nama senarai harga baharu menunjukkan nama sebut harga dengan cap masa tarikh untuk apabila senarai harga ini dicipta.

Anda boleh menggunakan setiap senarai harga itu dan membuat kemas kini untuk harga buruh (harga peranan) dan perbelanjaan (harga kategori). Harga ini hanya akan digunakan untuk sebut harga projek ini.

## <a name="price-lists-on-a-project-contract"></a>Senarai harga pada kontrak projek

Pada kontrak projek, penetapan harga projek sentiasa lalai sebagai senarai harga tersuai dengan nama kontrak dan cap masa tarikh dicipta ditambah kepada nama. Ini adalah benar sama ada kontrak dicipta apabila sebut harga dimenangi atau jika kontrak dicipta daripada awal. Jika perlu, anda boleh mengalih keluar perkaitan ini ke senarai harga tersuai dan mengaitkan senarai harga standard kepada kontrak projek.

Apabila anda mengaitkan senarai harga standard ke senarai harga projek pada sebut harga atau kontrak, sebarang perubahan yang dibuat pada harga dalam senarai harga akan memberi kesan kepada semua sebut harga dan kontrak yang menggunakan senarai harga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]