---
title: Penggantian harga efektif tarikh
description: Artikel ini menerangkan cara menyediakan penggantian harga untuk harga tertentu dalam senarai harga.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446007"
---
# <a name="date-effective-price-overrides"></a>Penggantian harga efektif tarikh 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

*Penggantian harga efektif memberikan* cara untuk mengatasi atau mengubah harga tertentu dalam senarai harga. Sebagai contoh, anda mempunyai senarai harga standard yang berkuat kuasa dari 1 Januari 2022, hingga 31 Disember 2022. Senarai harga ini mempunyai harga untuk banyak peranan. Harga yang ditetapkan untuk **peranan Juruteknik** Rangkaian ialah 100 dolar AS (USD) sejam. Apabila juruteknik rangkaian mencatat masa antara 1 Januari 2022, dan 31 Disember 2022, masa itu berharga 100 USD. Pada 1 Oktober 2022, anda mesti menyesuaikan harga *hanya* untuk **peranan Juruteknik** Rangkaian, dari 100 USD sejam hingga 110 USD sejam. Ciri **Penggantian harga** efektif Tarikh membolehkan anda menyediakan perubahan ini sebagai penggantian baris untuk harga peranan tertentu tersebut. Oleh itu, anda tidak perlu menyalin keseluruhan senarai harga dan mengubah harga hanya satu baris itu.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Penggantian harga efektif tarikh untuk harga buruh

Proses penetapan harga efektif untuk masa buruh dalam sesuatu projek terdiri daripada dua langkah asas.

1. Dayakan **ciri penggantian** harga efektif Tarikh.
1. Sediakan penggantian harga efektif tarikh.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Mendayakan ciri Penggantian harga berkesan Tarikh

> [!NOTE]
> **Selepas ciri Penggantian harga** berkesan Tarikh didayakan, ia tidak boleh dinyahdayakan.

Untuk mendayakan **ciri Penggantian harga** berkesan tarikh, ikut langkah ini.

1. Pergi ke **Parameter** Tetapan \>**·**.
1. **Buka rekod Parameter**.
1. Pada Anak Tetingkap Tindakan, pada tab **Kawalan** Ciri, pilih **Dayakan penggantian** harga efektif tarikh.
1. Dalam kotak dialog pengesahan, pilih **OK**.
1. Selepas beberapa saat, muat semula penyemak imbas anda. Keupayaan override harga efektif tarikh kini boleh didapati. Anda akan tahu bahawa keupayaan ini telah didayakan jika **Dayakan tarikh harga efektif mengatasi** tidak lagi muncul pada Anak Tetingkap Tindakan.

### <a name="set-up-a-date-effective-price-override"></a>Sediakan penggantian harga efektif tarikh

Penggantian harga efektif tarikh boleh ditetapkan pada **senarai harga Kos**, **Jualan** atau **Pembelian**.

> [!NOTE]
>**Kelakuan penggantian harga efektif Tarikh pada** masa ini mempunyai had berikut:
>
> - Hanya harga peranan dan penanda harga peranan menyokong **ciri Tarikh harga efektif mengatasi** dalam Operasi Projek.
> - Apabila anda menyalin senarai harga dengan menggunakan **tindakan Salin** pada **halaman butiran** Senarai Harga, dan apabila anda membuat senarai harga projek daripada senarai harga standard atau tersuai semasa penciptaan kontrak, penggantian **harga efektif tarikh tidak** disalin daripada senarai harga sumber.

Untuk menyediakan penggantian harga efektif tarikh untuk harga peranan atau penanda harga peranan, ikut langkah ini.

1. Buka halaman untuk senarai harga yang anda ingin sediakan penggantian harga efektif tarikh.
1. Pilih tab **Harga peranan** . Tab ini menyenaraikan semua **rekod harga** Peranan dalam senarai harga.
1. Pilih rekod harga **Peranan yang anda ingin sediakan harga penggantian tarikh efektif baharu untuk, dan kemudian dwiketik**(atau klik dua kali) **Harga peranan** untuk membuka **halaman Butiran** harga peranan.
1. Pilih tab **Penggantian berkesan** Tarikh. Grid pada tab ini menyenaraikan semua penggantian harga efektif tarikh untuk rekod harga **Peranan yang** dipilih.
1. Pada bar alat di atas grid, pilih **Penggantian harga peranan baru**. Penggelongsor **penggantian** harga peranan baharu dibuka.
1. Tentukan tarikh kuat kuasa, unit dan harga baru untuk penggantian harga. Kemudian pilih **Simpan** dan tutup borang.

> [!NOTE]
> - Penggantian harga efektif tarikh untuk harga peranan atau penanda harga peranan boleh digunakan untuk gabungan nilai dimensi harga yang sama yang wujud pada harga **Peranan induk** atau **baris penanda** harga Peranan.
> - Tarikh yang dipilih dalam **Berkuat Kuasa dari** bidang hendaklah dalam tarikh kuat kuasa senarai harga induk. Penggantian harga akan berkuat kuasa pada tarikh yang dipilih dalam **Berkesan dari** medan dan akan dikenakan sehingga akhir tarikh tamat senarai harga induk. Jika anda menetapkan penggantian harga efektif tarikh lain untuk harga peranan yang sama, penggantian harga pertama akan berkuat kuasa pada tarikh yang dipilih dalam **Medan Berkesan dari** dan akan terpakai sehingga permulaan penggantian kedua.

## <a name="examples"></a>Contoh

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Contoh 1: Menentukan kesan tarikh untuk harga peranan yang mempunyai penggantian harga peranan

Contoh berikut menunjukkan cara kesan tarikh ditentukan untuk harga peranan tertentu yang menggantikan penggantian harga peranan disediakan.

**Senarai harga A: 1 Januari hingga 30 Jun**

*Harga peranan*

| Harga peranan | Unit | Harga | Kesan ke atas harga untuk transaksi masuk |
|---|---|---|---|
| Juruteknik Rangkaian | Jam | 100 | Harga ini akan digunakan untuk sebarang transaksi di mana tarikh transaksi adalah antara 1 Januari dan 14 Mac. |

*Penggantian harga peranan*

| Berkesan dari | Unit | Harga | Kesan ke atas harga untuk transaksi masuk |
|---|---|---|---|
| Mac 15 | Jam | 110 | Harga ini akan digunakan untuk sebarang transaksi di mana tarikh transaksi adalah antara 15 Mac dan 30 Mac. |
| April 1 | Jam | 120 | Harga ini akan digunakan pada mana-mana transaksi di mana tarikh transaksi adalah antara 1 April dan 30 Jun. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Contoh 2: Menentukan kesan tarikh bagi penanda harga peranan yang mempunyai penanda harga peranan mengatasi

Contoh berikut menunjukkan cara kesan tarikh ditentukan untuk penanda harga peranan tertentu yang menggantikan penanda harga peranan disediakan.

**Senarai harga A: 1 Januari hingga 30 Jun**

*Harga peranan*

| Harga peranan | Jam kerja | Unit | Harga | Kesan ke atas harga untuk transaksi masuk |
|---|---|---|---|---|
| Juruteknik rangkaian | Tetap | Jam | 100 | Harga ini akan digunakan untuk sebarang transaksi di mana tarikh transaksi adalah antara 1 Januari dan 14 Mac. |

*Penanda harga peranan*

| Unit organisasi | Jam kerja | Tandakan % |
|---|---|---|
| Contoso AS | Kerja Lebih Masa | 10% |

*Penggantian penanda harga peranan*

| Berkesan dari | Harga | Kesan ke atas harga untuk transaksi masuk |
|---|---|---|
| Mac 15 | 20% | Peratus markup ini akan digunakan pada mana-mana transaksi di mana tarikh transaksi adalah antara 15 Mac dan 30 Mac. |
| April 1 | 25% | Markup ini akan digunakan pada mana-mana transaksi di mana tarikh transaksi adalah antara 1 April dan 30 Jun. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
