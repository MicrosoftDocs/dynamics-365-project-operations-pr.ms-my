---
title: Keperluan item untuk kontrak projek dengan pelbagai sumber pembiayaan
description: Artikel ini memberikan maklumat tentang cara mengkonfigurasi dan menggunakan keperluan item dengan berbilang sumber pembiayaan.
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

Sesetengah perjanjian kontrak untuk serahan berasaskan projek mungkin memerlukan berbilang sumber pembiayaan. Artikel ini menerangkan cara untuk memilih dan mengkonfigurasi sumber pembiayaan yang dikehendaki apabila berbilang sumber diperlukan untuk projek atau kontrak projek.

## <a name="terminology"></a>Istilah

- **Sumber pembiayaan** – Entiti yang membiayai kerja kontrak projek. Entiti ini boleh menjadi organisasi dalaman atau akaun invois luaran (pelanggan atau geran).
- **Pelanggan projek** – Entiti yang diserahkan kerja projek.
- **Akaun invois** – Entiti luaran yang membayar untuk kerja projek.

## <a name="example"></a>Contoh

Contoso telah memenangi kontrak pembaharuan peralatan dengan dua pelanggannya: Adatum AS dan Adatum Corporate. Kontrak termasuk perkhidmatan perkakasan dan pemasangan yang akan dihantar kepada Adatum AS (pelanggan projek). Perkakasan akan dibiayai oleh Adatum Corporate (akaun invois 1) dan kerja pemasangan akan dibiayai oleh Adatum AS (akaun invois 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Sediakan peraturan lalai akaun invois untuk keperluan item

### <a name="prerequisites"></a>Prasyarat

- Microsoft Dynamics 365 Finance **versi 10.0.27 atau lebih baharu** diperlukan untuk menggunakan keperluan item yang mempunyai berbilang akaun invois.
- Pentadbir sistem anda mesti mendayakan ciri **Benarkan keperluan Item dengan berbilang sumber pembiayaan untuk senario dalam stok/berdasarkan pengeluaran Project Operations** dalam ruang kerja **Pengurusan ciri**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Sediakan peraturan lalai akaun invois

Untuk menyediakan peraturan lalai bagi akaun invois, ikut langkah ini.

1. Pergi ke **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Pengurusan dan parameter perakaunan projek**.
1. Pada tab **Umum**, dalam bahagian **Pesanan jualan dan Keperluan item**, tetapkan pilihan **Benarkan projek dengan berbilang sumber pembiayaan** kepada **Ya**.
1. Dalam medan **Pelanggan lalai**, tentukan tempat pelanggan penghantaran projek pada keperluan item berasal secara lalai:

    - **Dari sumber pembiayaan** – Pelanggan penghantaran projek lalai datang dari sumber pembiayaan. Jika berbilang sumber pembiayaan dikaitkan dengan kontrak projek, sumber pembiayaan pertama dalam senarai akan digunakan.
    - **Dari projek** – Pelanggan penghantaran projek lalai datang dari pelanggan yang dipilih dalam medan **Akaun rekod projek**.

1. Pilihan: Tetapkan atau ubah akaun invois lalai pada rekod projek:

    1. Pergi ke **Pengurusan dan perakaunan projek** \> **Projek** \> **Semua projek** dan buka butiran rekod projek.
    2. Pada tab **Umum**, tetapkan atau kemas kini medan **Akaun invois lalai**. Akaun yang anda tentukan akan digunakan sebagai akaun invois lalai untuk keperluan item baharu yang dicipta untuk projek tersebut. Jika anda membiarkan medan kosong, akaun invois sumber pembiayaan kontrak projek pertama akan digunakan secara lalai. Walau bagaimanapun, pengguna akan dapat mengubah akaun apabila mereka menyimpan rekod.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pilih akaun invois untuk digunakan apabila anda mencipta keperluan item

Untuk memilih akaun invois untuk digunakan apabila anda mencipta keperluan item, ikut langkah ini.

1. Pergi ke **Pengurusan projek dan perakaunan** \> **Projek** \> **Semua projek** dan pilih rekod projek.
1. Pada tab **Pelan**, pilih **Keperluan item**.
1. Cipta rekod keperluan item baharu.

    - Secara lalai, medan **Akaun invois** dalam rekod ditetapkan kepada akaun invois yang ditetapkan untuk projek tersebut. Anda boleh mengubah nilai medan **Akaun invois** dan kemudian menyimpan rekod. Selepas rekod disimpan, anda tidak boleh mengemas kini nilai **Akaun invois** lagi. Jika anda mesti mengemas kini nilai **Akaun invois** untuk keperluan item, padamkan keperluan item sedia ada dan kemudian cipta yang baharu yang mempunyai nilai yang diingini.
    - Secara lalai, medan **Pelanggan** untuk keperluan item ditetapkan berdasarkan nilai **Pelanggan lalai** yang ditetapkan pada halaman **Parameter pengurusan projek dan perakaunan**.

    Apabila rekod keperluan item disimpan, sistem mengaitkannya dengan rekod pengepala **Pesanan jualan keperluan item**. Jika tiada pengepala pesanan jualan terbuka mempunyai akaun invois yang dipilih, sistem akan mencipta satu pengepala dan mengaitkan baris keperluan item dengannya.

> [!NOTE]
> Keperluan item sentiasa diinvois sepenuhnya ke akaun invois yang ditetapkan dalam rekod. Sistem tidak menyokong peraturan peruntukan pembiayaan yang mempunyai keperluan item pada masa ini dan tidak akan membahagikan siaran berdasarkan persediaan peraturan peruntukan pembiayaan.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Cipta keperluan item daripada rekod ramalan item

Untuk mencipta keperluan item daripada rekod ramalan item, ikut langkah ini.

1. Pergi ke **Pengurusan projek dan perakaunan** \> **Projek** \> **Semua projek** dan pilih rekod projek.
1. Pada tab **Pelan**, pilih **Ramalan item**.
1. Cipta rekod ramalan item baharu.
1. Pilihan: Pada tab **Projek**, dalam medan **Sumber pembiayaan**, pilih akaun invois yang dikehendaki.
1. Pilih **Cipta keperluan item** dan sahkan mesej yang anda terima.

    > [!NOTE]
    > Sistem menyalin nilai **Sumber pembiayaan** daripada rekod ramalan item kepada rekod keperluan item yang baru dicipta.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Akaun invois lalai apabila sistem mencipta keperluan item secara automatik daripada baris pesanan pembelian

Jika pilihan **Cipta keperluan item** ditetapkan kepada **Ya** pada halaman **Parameter pengurusan projek dan perakaunan**, sistem mencipta keperluan item secara automatik apabila baris pesanan pembelian projek baharu disimpan. Secara lalai, medan **Akaun invois** dan **Keperluan item** ditetapkan kepada nilai medan **Akaun invois lalai** dalam rekod projek. Sistem tidak menyokong pengemaskinian atau perubahan akaun invois untuk rekod jenis ini.
