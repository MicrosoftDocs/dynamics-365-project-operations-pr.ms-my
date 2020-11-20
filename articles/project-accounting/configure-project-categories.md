---
title: Konfigurasi kategori projek
description: Topik ini memberikan maklumat tentang menyediakan kategori projek.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131939"
---
# <a name="configure-project-categories"></a>Konfigurasi kategori projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Operasi Projek menawarkan keupayaan yang kukuh untuk mengkategorikan perolehan dan perbelanjaan projek. Kategori ini menyediakan keupayaan untuk melaporkan dan menganalisis transaksi projek dan memandu ke lejar umum.

Gambarajah berikut menunjukkan korelasi antara kategori transaksi, kategori dikongsi dan kategori projek. 

Kategori transaksi ialah kumpulan asas untuk transaksi projek. Dalam kumpulan tersebut, terdapat beberapa set kategori dikongsi yang boleh dikongsi merentasi aplikasi dan modul. Lebih lagi ke khusus, kategori projek ialah peringkat paling banyak butiran kategori. Kategori projek khusus untuk entiti, modul dan aplikasi sah.

![Korelasi antara kategori transaksi, kategori dikongsi dan kategori projek](media/project-categories.png)

## <a name="transaction-categories"></a>Kategori transaksi

Kategori transaksi mewakili kumpulan asas untuk transaksi projek dan bukan khusus syarikat atau transaksi jenis. Sebagai contoh, Contoso Robotics menggunakan kategori Reka bentuk, Perjalanan, Pemasangan dan Transaksi Perkhidmatan kepada transaksi Projek kumpulan.

Kategori transaksi ditakrifkan dalam modul Operasi Projek. 
1. Pergi ke **Tetapan** \> **Kategori Transaksi** untuk membuka borang. 
2. Cipta kategori transaksi baharu sama ada dengan memilih **Baharu** atau dengan memilih **Import dari Excel**.

## <a name="shared-categories"></a>Kategori dikongsi

Dynamics 365 menggunakan konsep kategori dikongsi untuk categorize perbelanjaan dalam aplikasi yang berbeza, seperti Dynamics 365 Finance, rantaian bekalan Dynamics 365 dan Operasi Projek Dynamics 365. Bagi setiap kategori transaksi yang dicipta, Operasi Projek secara automatik mencipta empat kategori dikongsi yang berkaitan: Jam, Perbelanjaan, Yuran dan Item. Anda boleh menyemak dan melaraskan kategori dikongsi dengan pergi ke kategori **Pengurusan projek dan tetapan perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori Dikongsi**.

## <a name="project-categories"></a>Kategori produk

Kategori projek mewakili paling banyak butiran konfigurasi kategori dan mesti dikonfigurasikan secara berasingan dan untuk setiap syarikat, oleh Akauntan projek.

1. Pergi ke **Pengurusan Projek dan Perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori projek**.
2. Pilih **Baharu**.
3. Pilih **ID kategori** bagi kategori Dikongsi yang anda cipta dalam bahagian sebelumnya. Operasi Projek membenarkan hanya menggunakan kategori dikongsi yang berkaitan dengan kategori transaksi.
4. Pilih kumpulan kategori.

## <a name="category-groups"></a>Kumpulan kategori

Kumpulan kategori digunakan untuk berkongsi sifat, terutamanya menyiarkan profil, antara kategori Projek yang berkaitan. Mesti ada sekurang-kurangnya satu kumpulan kategori untuk setiap jenis transaksi dan setiap kategori projek ditugaskan satu kumpulan.

Spesifikasi dalam Operasi Projek ditakrifkan oleh peraturan profil kos projek dan hasil, kategori projek dan kumpulan kategori. Anda boleh menyediakan kumpulan kategori dengan pergi ke **Pengurusan projek dan perakaunan** \> **Tetapan** \> **Kategori** \> **Kumpulan kategori**.
