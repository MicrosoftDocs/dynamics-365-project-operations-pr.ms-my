---
title: Cipta kontrak lanjutan untuk pengebilan berdasarkan kemajuan
description: Artikel ini menerangkan cara untuk mencipta kontrak projek supaya anda boleh menjana invois untuk pelanggan, berdasarkan peratusan kerja yang diselesaikan.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26fe072b8241c7fdc96629f534e33a8fe53d3164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913677"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Cipta kontrak lanjutan untuk pengebilan berdasarkan kemajuan
[!include [banner](../includes/banner.md)]

Artikel ini menerangkan cara untuk mencipta kontrak projek supaya anda boleh mencipta invois untuk pelanggan, berdasarkan peratusan kerja yang diselesaikan. Amaun invois dikira secara automatik untuk kategori kerja belanjawan yang anda sediakan untuk projek. Masa invois ditetapkan apabila anda berunding kontrak projek dengan pelanggan.

Gunakan prosedur dalam artikel ini untuk menyediakan kontrak, projek berkaitan dan peraturan pengebilan yang mengira amaun invois untuk kategori kerja belanjawan yang anda sediakan untuk projek.

Selepas anda mencipta kontrak dan projek, anda boleh menyediakan butiran projek. Sebagai contoh, anda boleh mentakrifkan aktiviti dan tugaskan pekerja ke projek tersebut.

## <a name="example"></a>Contoh

Organisasi anda adalah sebuah firma pembangunan perisian. Anda bersetuju untuk membangunkan pakej perakaunan gaji untuk pelanggan bagi jumlah yuran 20,000 dolar AS (USD). Organisasi anda bersetuju untuk invois kepada pelanggan apabila anda melengkapkan peratusan khusus projek tersebut. Anda menyediakan kategori projek berikut untuk kerja, supaya anda boleh menggunakannya dalam proses pengebilan:

- Perundingan
- Reka bentuk
- Pemasangan

Anda juga menyediakan peraturan pengebilan yang mengira secara automatik amaun invois untuk peratusan kerja projek yang dilengkapkan dalam setiap kategori.

Pengurus belanjawan mencipta belanjawan untuk kategori projek. Amaun kerja yang lengkap dikira secara automatik sebagai peratusan kerja sebenar berbanding amaun yang diperuntukkan.

## <a name="prerequisites"></a>Prasyarat

Sebelum anda mencipta projek yang menggunakan peraturan pengebilan, anda mesti menyediakan jujukan nombor untuk peraturan pengebilan dan jurnal yuran yang digunakan untuk siaran pengebilan kemajuan.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Pengurusan dan parameter perakaunan projek**.
2. Pada halaman **Pengurusan dan parameter perakaunan projek**, pada tab **Jujukan nombor**, sediakan jujukan nombor yang anda mahu gunakan apabila peraturan pengebilan dicipta.
3. Pergi ke **Pengurusan dan perakaunan projek** \> **Jurnal** \> **Yuran**.
4. Pada halaman **Jurnal yuran**, pilih **Baharu**, dan masukkan nama jurnal.

## <a name="create-a-contract-for-progress-billings"></a>Cipta kontrak untuk pengebilan kemajuan

Gunakan prosedur ini untuk mencipta kontrak projek untuk projek harga tetap. Anda cipta invois projek apabila kerja yang selesai pada projek itu mencapai peratusan yang ditentukan.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Kontrak projek**.
2. Pada halaman **Kontrak projek**, pilih **Baharu**.
3. Dalam kotak dialog **Kontrak projek baharu**, tetapkan medan berikut:

    - **Nama**
    - **Jenis pembiayaan**
    - **Sumber pembiayaan**
    - **Mata wang jualan** – Secara lalai, mata wang ini digunakan untuk invois pelanggan yang berkaitan dengan kontrak projek. Walau bagaimanapun, anda boleh mengubah mata wang jualan pada invois pelanggan khusus.

4. Pilih **OK**. Maklumat disalin ke pengepala halaman **Kontrak projek**.
5. Pada halaman **Kontrak projek**, isi maklumat lain yang diperlukan untuk projek.

## <a name="create-a-project-for-progress-billings"></a>Cipta kontrak untuk pengebilan kemajuan

Ikuti langkah ini untuk mencipta projek dan sebarang subprojek yang berkaitan dengan kontrak projek.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek**.
2. Pada halaman **Semua projek**, pilih **Baharu**.
3. Dalam kotak dialog **Projek baharu**, dalam medan **Jenis projek**, pilih **Masa dan bahan**.
4. Pilih kumpulan projek. Kumpulan projek mentakrifkan maklumat penyiaran untuk projek yang ditugaskan kepada kumpulan.
5. Pilih **Cipta projek**.
6. Selepas projek dicipta, tetapkan peringkat projek untuk **Sedang berjalan**.

## <a name="create-a-budget-for-a-project"></a>Cipta belanjawan untuk projek

Kategori belanjawan digunakan untuk mengira secara automatik amaun invois untuk peratusan kerja yang dilengkapkan untuk setiap kategori. Ikuti langkah ini untuk mencipta kategori belanjawan untuk kos anggaran.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek**.
2. Pada halaman **Semua projek**, pilih dan buka projek yang anda mahu.
3. Pada halaman **Projek**, pada Anak Tetingkap Tindakan, pada tab **Pelan**, dalam kumpulan **Belanjawan**, pilih **Belanjawan projek**.
4. Pada halaman **Belanjawan projek**, masukkan kos anggaran untuk setiap kategori dalam projek.

## <a name="create-billing-rules-for-progress-billings"></a>Cipta peraturan pengebilan untuk pengebilan kemajuan

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Kontrak projek**.
2. Pada halaman **Kontrak projek**, pilih dan buka kontrak projek.
3. Pada halaman kontrak projek, pada FastTab **Peraturan pengebilan**, pilih **Tambah**.
4. Pada halaman **Peraturan pengebilan**, dalam medan **Jenis baris**, pilih **Kemajuan**.
5. Pada FastTab **Butiran baris peraturan pengebilan**, dalam medan **Nilai kontrak**, masukkan jumlah nilai kontrak.
6. Dalam medan **Kategori**, pilih kategori untuk siaran transaksi yuran.
7. Dalam medan **Projek**, pilih projek yang menggunakan peraturan pengebilan ini.
8. Pilihan: Tugaskan peraturan pengebilan kepada projek tambahan. Pada FastTab **Projek**, dalam bahagian **Projek tersedia**, pilih projek dan kemudian pilih butang anak panah kanan untuk menambah projek ke bahagian **Projek dipilih**.
9. Pilihan: Kira amaun peratusan yang ditahan pelanggan daripada pembayaran pada invois. Pada FastTab **Terma pengekalan pembayaran**, pilih sumber pembiayaan, dan kemudian, dalam medan **Peratusan pengekalan**, masukkan peratusan pengekalan.
10. Ulangi langkah ini untuk mencipta peraturan pengebilan tambahan untuk kontrak projek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]