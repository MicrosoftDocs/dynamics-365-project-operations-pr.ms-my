---
title: Penggantian harga dikuatkuasakan tarikh
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
# <a name="date-effective-price-overrides"></a>Penggantian harga dikuatkuasakan tarikh 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

*Penggantian harga dikuatkuasakan tarikh* menyediakan cara untuk mengganti atau mengubah harga tertentu dalam senarai harga. Sebagai contoh, anda mempunyai senarai harga standard yang berkuat kuasa dari 1 Januari 2022, hingga 31 Disember 2022. Senarai harga ini mempunyai harga untuk banyak peranan. Harga yang ditetapkan untuk peranan **Juruteknik Rangkaian** ialah 100 US Dolar (USD) sejam. Apabila juruteknik rangkaian mengelog masa antara 1 Januari 2022 dan 31 Disember 2022, masa itu berharga 100USD. Pada 1 Oktober 2022, anda mesti melaraskan harga *hanya* untuk peranan **Juruteknik Rangkaian**, daripada 100USD sejam kepada 110USD sejam. Ciri **Penggantian harga dikuatkuasakan tarikh** membolehkan anda menyediakan perubahan ini sebagai ganti baris untuk harga peranan tertentu. Oleh itu, anda tidak perlu menyalin keseluruhan senarai harga dan mengubah harga hanya satu baris.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Penggantian harga dikuatkuasakan tarikh untuk harga buruh

Proses menyediakan penggantian harga dikuatkuasakan tarikh untuk masa buruh pada projek terdiri daripada dua langkah asas.

1. Dayakan ciri **Penggantian harga dikuatkuasakan tarikh**.
1. Sediakan penggantian harga dikuatkuasakan tarikh.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Dayakan ciri Penggantian harga dikuatkuasakan tarikh

> [!NOTE]
> Selepas ciri **Penggantian harga dikuatkuasakan tarikh** didayakan, ia tidak boleh dinyahdayakan.

Untuk mendayakan ciri **Penggantian harga dikuatkuasakan tarikh**, ikut langkah ini.

1. Pergi ke **Tetapan** \> **Parameter**.
1. Buka rekod **Parameter**.
1. Pada Anak Tetingkap Tindakan, pada tab **Kawalan Ciri**, pilih **Dayakan penggantian harga dikuatkuasakan tarikh**.
1. Dalam kotak dialog pengesahan, pilih **OK**.
1. Selepas beberapa ketika, segarkan semula pelayar anda. Keupayaan penggantian harga dikuatkuasakan tarikh kini sepatutnya tersedia. Anda akan tahu bahawa keupayaan ini telah didayakan jika **Dayakan penggantian harga dikuatkuasakan tarikh** tidak lagi muncul pada Anak Tetingkap Tindakan.

### <a name="set-up-a-date-effective-price-override"></a>Sediakan penggantian harga dikuatkuasakan tarikh

Penggantian harga dikuatkuasakan tarikh boleh disediakan pada senarai harga **Kos**, **Jualan** atau **Pembelian**.

> [!NOTE]
>Tingkah laku **Penggantian harga dikuatkuasakan tarikh** mempunyai pengehadan berikut pada masa ini:
>
> - Hanya harga peranan dan tokokan harga peranan menyokong ciri **Penggantian harga dikuatkuasakan tarikh** dalam Project Operations.
> - Apabila anda menyalin senarai harga dengan menggunakan tindakan **Salin** pada halaman **butiran Senarai Harga** dan apabila anda mencipta senarai harga projek daripada senarai harga standard atau tersuai semasa penciptaan kontrak, penggantian harga dikuatkuasakan tarikh **tidak** disalin daripada senarai harga sumber.

Untuk menyediakan penggantian harga dikuatkuasakan tarikh untuk harga peranan atau tokokan harga peranan, ikut langkah ini.

1. Buka halaman untuk senarai harga yang ingin anda sediakan penggantian harga dikuatkuasakan tarikh.
1. Pilih tab **Harga peranan**. Tab ini menyenaraikan semua rekod **Harga peranan** dalam senarai harga.
1. Pilih rekod **Harga peranan** yang ingin anda sediakan penggantian harga dikuatkuasakan tarikh dan kemudian dwiketik (atau dwiklik) **Harga peranan** untuk membuka halaman **butiran Harga peranan**.
1. Pilih tab **Penggantian dikuatkuasakan tarikh**. Grid pada tab ini menyenaraikan semua penggantian harga dikuatkuasakan tarikh untuk rekod **Harga peranan** yang dipilih.
1. Pada bar alat di atas grid, pilih **Penggantian harga peranan baharu**. Gelangsar **Penggantian harga peranan baharu** dibuka.
1. Tentukan tarikh berkuat kuasa dari, unit dan harga baharu untuk penggantian harga. Kemudian pilih **Simpan** dan tutup borang.

> [!NOTE]
> - Penggantian harga dikuatkuasakan tarikh untuk harga peranan atau tokokan harga peranan diguna pakai pada kombinasi sama nilai dimensi penetapan harga yang wujud pada **Harga peranan** induk atau baris **Tokokan harga peranan**.
> - Tarikh yang dipilih dalam medan **Berkuat kuasa dari** perlu berada dalam tarikh berkuat kuasa senarai bagi harga induk. Penggantian harga akan berkuat kuasa pada tarikh yang dipilih dalam medan **Berkuat kuasa dari** dan akan diguna pakai sehingga penghujung tarikh akhir senarai harga induk. Jika anda menyediakan penggantian harga dikuatkuasakan tarikh yang lain untuk harga peranan yang sama, penggantian harga pertama akan berkuat kuasa pada tarikh yang dipilih dalam medan **Berkuat kuasa dari** dan akan diguna pakai sehingga bermulanya penggantian kedua.

## <a name="examples"></a>Contoh

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Contoh 1: Menentukan penguatkuasaan tarikh untuk harga peranan yang mempunyai penggantian harga peranan

Contoh berikut menunjukkan cara penguatkuasaan tarikh ditentukan untuk harga peranan tertentu yang akan ditetapkan penggantian harga peranan.

**Senarai harga A: 1 Januari hingga 30 Jun**

*Harga peranan*

| Harga peranan | Unit | Harga | Kesan pada harga untuk transaksi masuk |
|---|---|---|---|
| Juruteknik Rangkaian | Jam | 100 | Harga ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 1 Januari hingga 14 Mac. |

*Penggantian harga peranan*

| Berkuat kuasa dari | Unit | Harga | Kesan pada harga untuk transaksi masuk |
|---|---|---|---|
| Mac 15 | Jam | 110 | Harga ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 15 Mac hingga 30 Mac. |
| April 1 | Jam | 120 | Harga ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 1 April hingga 30 Jun. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Contoh 2: Menentukan penguatkuasaan tarikh untuk tokokan harga peranan yang mempunyai penggantian tokokan harga peranan

Contoh berikut menunjukkan cara penguatkuasaan tarikh ditentukan untuk tokokan harga peranan tertentu yang akan ditetapkan penggantian tokokan harga peranan.

**Senarai harga A: 1 Januari hingga 30 Jun**

*Harga peranan*

| Harga peranan | Jam kerja | Unit | Harga | Kesan pada harga untuk transaksi masuk |
|---|---|---|---|---|
| Juruteknik rangkaian | Biasa | Jam | 100 | Harga ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 1 Januari hingga 14 Mac. |

*Tokokan harga peranan*

| Unit organisasi | Jam kerja | % tokokan |
|---|---|---|
| Contoso AS | Kerja Lebih Masa | 10% |

*Penggantian tokokan harga peranan*

| Berkuat kuasa dari | Harga | Kesan pada harga untuk transaksi masuk |
|---|---|---|
| Mac 15 | 20% | Peratusan tokokan ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 15 Mac hingga 30 Mac. |
| April 1 | 25% | Tokokan ini akan digunakan pada mana-mana transaksi yang tarikh transaksi adalah antara 1 April hingga 30 Jun. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
