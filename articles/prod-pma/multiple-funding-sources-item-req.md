---
title: Keperluan item untuk kontrak projek dengan pelbagai sumber pembiayaan
description: Artikel ini memberikan maklumat tentang cara mengkonfigurasi dan menggunakan keperluan item dengan pelbagai sumber pembiayaan.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028499"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Keperluan item untuk kontrak projek dengan pelbagai sumber pembiayaan

_**Digunakan Pada:** Project Operations untuk senario berasaskan stok/pengeluaran_

Sesetengah perjanjian kontrak untuk penghantaran berasaskan projek mungkin memerlukan pelbagai sumber pembiayaan. Artikel ini menerangkan cara memilih dan mengkonfigurasi sumber pembiayaan yang dikehendaki apabila pelbagai sumber diperlukan untuk projek atau kontrak projek.

## <a name="terminology"></a>Istilah

- **Sumber pembiayaan** - Entiti yang membiayai kerja kontrak projek. Entiti ini boleh menjadi organisasi dalaman atau akaun invois luaran (pelanggan atau geran).
- **Pelanggan projek** - Entiti yang dihantar oleh kerja projek.
- **Akaun invois** - Entiti luaran yang membayar untuk kerja projek.

## <a name="example"></a>Contoh

Contoso telah memenangi kontrak pembaharuan peralatan dengan dua pelanggannya: Adatum US dan Adatum Corporate. Kontrak ini termasuk perkhidmatan perkakasan dan pemasangan yang akan dihantar ke Adatum AS (pelanggan projek). Perkakasan akan dibiayai oleh Adatum Corporate (akaun invois 1), dan kerja pemasangan akan dibiayai oleh Adatum US (akaun invois 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Sediakan peraturan lalai akaun invois untuk keperluan item

### <a name="prerequisites"></a>Prasyarat

- Microsoft Dynamics 365 Kewangan **versi 10.0.27 atau lebih** baru diperlukan untuk menggunakan keperluan item yang mempunyai berbilang akaun invois.
- Pentadbir sistem anda mesti mendayakan **keperluan Benarkan Item dengan berbilang sumber pembiayaan untuk ciri senario** berasaskan stok/pengeluaran Operasi Projek dalam **ruang kerja pengurusan** Ciri.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Sediakan peraturan lalai akaun invois

Untuk menyediakan peraturan lalai bagi akaun invois, ikut langkah ini.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Pengurusan dan parameter perakaunan projek**.
1. **Pada tab Umum**, dalam **bahagian Pesanan Jualan dan Keperluan** Item, tetapkan **pilihan Benarkan projek dengan berbilang sumber** pembiayaan kepada **Ya**.
1. Dalam medan **Pelanggan** lalai, tentukan dari mana pelanggan penghantaran projek pada keperluan item berasal secara lalai:

    - **Dari sumber** pembiayaan - Pelanggan penghantaran projek lalai berasal dari sumber pembiayaan. Sekiranya pelbagai sumber pembiayaan dikaitkan dengan kontrak projek, sumber pembiayaan pertama dalam senarai akan digunakan.
    - **Dari projek** - Pelanggan penghantaran projek lalai berasal dari pelanggan yang dipilih dalam **medan akaun** rekod Projek.

1. Pilihan: Setkan atau ubah akaun invois lalai pada rekod projek:

    1. Pergi ke **Projek pengurusan dan projek** \> **perakaunan** \> **Semua projek**, dan buka butiran rekod projek.
    2. **Pada tab Umum**, tetapkan atau kemas kini **medan Akaun** invois lalai. Akaun yang anda tentukan akan digunakan sebagai akaun invois lalai untuk keperluan item baru yang dibuat untuk projek tersebut. Jika anda meninggalkan medan kosong, akaun invois sumber pembiayaan kontrak projek pertama akan digunakan secara lalai. Walau bagaimanapun, pengguna akan dapat menukar akaun apabila mereka menyimpan rekod.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pilih akaun invois untuk digunakan apabila anda mencipta keperluan item

Untuk memilih akaun invois untuk digunakan apabila anda mencipta keperluan item, ikuti langkah ini.

1. Pergi ke **Projek pengurusan dan projek perakaunan** \> **Semua** \> **projek**, dan pilih rekod projek.
1. **Pada tab Pelan**, pilih **Keperluan item**.
1. Cipta rekod keperluan item baru.

    - Secara lalai, **medan akaun** Invois dalam rekod ditetapkan kepada akaun invois yang ditetapkan untuk projek. Anda boleh menukar nilai **medan akaun** Invois dan kemudian menyimpan rekod. Selepas rekod disimpan, anda tidak lagi boleh mengemas kini **nilai akaun** Invois. Jika anda mesti mengemas kini **nilai akaun** Invois untuk keperluan item, padamkan keperluan item sedia ada, kemudian cipta yang baharu yang mempunyai nilai yang dikehendaki.
    - Secara lalai, **medan Pelanggan** untuk keperluan item ditetapkan berdasarkan **nilai pelanggan** Lalai yang ditetapkan pada **halaman pengurusan Projek dan parameter** perakaunan.

    Apabila rekod keperluan item disimpan, sistem mengaitkannya dengan **rekod pengepala pesanan** jualan keperluan Item. Sekiranya tidak ada tajuk pesanan penjualan terbuka yang mempunyai akaun invois yang dipilih, sistem akan membuatnya dan mengaitkan garis keperluan item dengannya.

> [!NOTE]
> Keperluan item sentiasa diinvois sepenuhnya ke akaun invois yang ditetapkan dalam rekod. Sistem ini pada masa ini tidak menyokong peraturan peruntukan pembiayaan yang mempunyai keperluan item, dan ia tidak akan membahagikan siaran berdasarkan penyediaan peraturan peruntukan pembiayaan.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Mencipta keperluan item daripada rekod ramalan item

Untuk mencipta keperluan item daripada rekod ramalan item, ikuti langkah ini.

1. Pergi ke **Projek pengurusan dan Projek perakaunan** \> **Semua** \> **projek** dan pilih rekod projek.
1. **Pada tab Pelan**, pilih **Ramalan item**.
1. Buat rekod ramalan item baru.
1. Pilihan: Pada **tab Projek**, dalam **medan Sumber** pembiayaan, pilih akaun invois yang dikehendaki.
1. Pilih **Cipta keperluan** item dan sahkan mesej yang anda terima.

    > [!NOTE]
    > Sistem ini menyalin **nilai sumber** Pembiayaan dari rekod ramalan item ke rekod keperluan item yang baru dibuat.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Akaun invois lalai apabila sistem secara automatik mencipta keperluan item daripada baris pesanan pembelian

**Jika pilihan Buat keperluan** item ditetapkan kepada **Ya** pada **halaman Pengurusan Projek dan parameter** perakaunan, sistem secara automatik mencipta keperluan item apabila baris pesanan pembelian projek baru disimpan. Secara lalai, **medan keperluan** akaun **Invois dan** Item disetkan kepada nilai **medan Akaun** invois lalai dalam rekod projek. Sistem ini tidak menyokong pengemaskinian atau perubahan akaun invois untuk rekod jenis ini buat masa ini.
