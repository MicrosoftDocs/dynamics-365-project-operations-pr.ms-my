---
title: Konfigurasi kategori projek
description: Artikel ini memberikan maklumat tentang penyediaan kategori projek.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 440fc712750c07e8426d54e3a1f994f506879e3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933595"
---
# <a name="configure-project-categories"></a>Konfigurasi kategori projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Operasi Projek menawarkan keupayaan yang kukuh untuk mengkategorikan perolehan dan perbelanjaan projek. Kategori ini menyediakan keupayaan untuk melaporkan dan menganalisis transaksi projek dan memandu ke lejar umum.

Gambarajah berikut menunjukkan korelasi antara kategori transaksi, kategori dikongsi dan kategori projek. 

Kategori transaksi ialah kumpulan asas untuk transaksi projek. Dalam kumpulan tersebut, terdapat beberapa set kategori dikongsi yang boleh dikongsi merentasi aplikasi dan modul. Lebih lagi ke khusus, kategori projek ialah peringkat paling banyak butiran kategori. Kategori projek khusus untuk entiti, modul dan aplikasi sah.

![Korelasi antara kategori transaksi, kategori dikongsi dan kategori projek.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategori transaksi

Kategori transaksi mewakili kumpulan asas untuk transaksi projek dan bukan khusus syarikat atau transaksi jenis. Sebagai contoh, Contoso Robotics menggunakan kategori Reka bentuk, Perjalanan, Pemasangan dan Transaksi Perkhidmatan kepada transaksi Projek kumpulan.

Kategori transaksi ditakrifkan dalam modul Operasi Projek. 
1. Pergi ke **Tetapan** \> **Kategori Transaksi** untuk membuka borang. 
2. Cipta kategori transaksi baharu sama ada dengan memilih **Baharu** atau dengan memilih **Import dari Excel**.

## <a name="shared-categories"></a>Kategori dikongsi

Dynamics 365 menggunakan konsep kategori dikongsi untuk mengkategorikan perbelanjaan dalam aplikasi yang berbeza, seperti Dynamics 365 Finance, Dynamics 365 Supply Chain dan Dynamics 365 Project Operations. Bagi setiap kategori transaksi yang dicipta, Operasi Projek secara automatik mencipta empat kategori dikongsi yang berkaitan: Jam, Perbelanjaan, Yuran dan Item. Anda boleh menyemak dan melaraskan kategori dikongsi dengan pergi ke kategori **Pengurusan projek dan tetapan perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori Dikongsi**.

## <a name="project-categories"></a>Kategori produk

Kategori projek mewakili paling banyak butiran konfigurasi kategori dan mesti dikonfigurasikan secara berasingan dan untuk setiap syarikat, oleh Akauntan projek.

1. Pergi ke **Pengurusan Projek dan Perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori projek**.
2. Pilih **Baharu**.
3. Pilih **ID kategori** bagi kategori Dikongsi yang anda cipta dalam bahagian sebelumnya. Operasi Projek membenarkan hanya menggunakan kategori dikongsi yang berkaitan dengan kategori transaksi.
4. Pilih kumpulan kategori.

## <a name="category-groups"></a>Kumpulan kategori

Kumpulan kategori digunakan untuk berkongsi sifat, terutamanya menyiarkan profil, antara kategori Projek yang berkaitan. Mesti ada sekurang-kurangnya satu kumpulan kategori untuk setiap jenis transaksi dan setiap kategori projek ditugaskan satu kumpulan.

Spesifikasi dalam Operasi Projek ditakrifkan oleh peraturan profil kos projek dan hasil, kategori projek dan kumpulan kategori. Anda boleh menyediakan kumpulan kategori dengan pergi ke **Pengurusan projek dan perakaunan** \> **Tetapan** \> **Kategori** \> **Kumpulan kategori**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]