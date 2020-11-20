---
title: Dimensi perakaunan lalai
description: Topik ini memberikan maklumat mengenai cara untuk menyediakan lalai dimensi kewangan.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131894"
---
# <a name="financial-dimension-defaults"></a>Dimensi perakaunan lalai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Dynamics 365 Project Operations rangka kerja [Dimensi kewangan](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) dalam Dynamics 365 Finance untuk menyediakan wawasan tambahan mengenai sub Lejar projek dan transaksi lejar umum.

Dimensi kewangan lalai boleh ditetapkan pada pelanggan, sumber pembiayaan projek, pencapaian, baris kontrak projek, atau projek.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Takrifkan dimensi kewangan lalai untuk pelanggan

Lalai dimensi pelanggan ditentukan dalam Kewangan. Lengkapkan langkah berikut untuk menetapkan lalai dimensi.

1. Pergi ke **Akaun belum terima** > **Pelanggan** > **Semua pelanggan**.
2. Pada halaman **Pelanggan**, pada tab **Dimensi kewangan**, tetapkan nilai dimensi kewangan untuk pelanggan khusus.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Takrifkan dimensi kewangan lalai untuk kontrak projek

Kontrak projek dicipta dan dikekalkan dalam Common Data Service (CDS). Sifat perakaunan bagi kontrak projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Tetapkan dimensi kewangan untuk sumber pembiayaan projek

1. Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.
2. Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.
3. Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.
4. Tetapkan dimensi perakaunan lalai. Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Tetapkan dimensi kewangan untuk baris kontrak

1. Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.
2. Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.
3. Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.
4. Tetapkan dimensi perakaunan lalai. Lalai dimensi kewangan boleh terpakai dan boleh digunakan hanya dengan baris kontrak Harga tetap (pencapaian).

Lalai ini digunakan pada transaksi akaun berkaitan dan baris invois.

## <a name="define-default-financial-dimensions-for-projects"></a>Takrifkan dimensi kewangan lalai untuk projek

Projek dicipta dan dikekalkan dalam (CDS). Atribut perakaunan bagi projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.

1. Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Semua projek**.
2. Pilih rekod yang anda mahu kemas kini dan pada tab **Projek**, pilih **Tunjuk perakaunan lalai**.
3. Kembangkan **Maklumat berkaitan** dan pilih tab **Penyediaan**.
4. Tetapkan dimensi perakaunan lalai. Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan. Jika projek berkaitan dengan baris kontrak dengan pelanggan kontrak berbilang projek, pelanggan utama digunakan untuk dimensi kewangan lalai.

Projek dimensi kewangan lalai digunakan untuk menetapkan garisan jurnal lalai untuk masa, perbelanjaan dan yuran transaksi dalam **Jurnal Integrasi Project Operations** dan pada baris invois projek berkaitan.
