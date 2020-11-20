---
title: Menyelesaikan harga kos untuk anggaran dan aktual
description: Topik ini menyediakan maklumat tentang cara harga kos untuk anggaran dan aktual diselesaikan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119700"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Menyelesaikan harga kos untuk anggaran dan aktual

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menyelesaikan harga kos dan senarai harga kos bagi anggaran dan aktual, sistem ini menggunakan maklumat dalam medan **Tarikh**, **Mata Wang** dan **Unit Kontrak** untuk projek berkaitan. Selepas senarai harga kos diselesaikan, aplikasi ini menyelesaikan kadar kos.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Masa

Baris anggaran untuk Masa merujuk kepada butiran sebut harga dan baris kontrak bagi tugasan masa dan sumber pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan medan **Peranan**, **Syarikat Sumber** dan **Unit Sumber** pada baris anggaran untuk Masa bagi pemadanan terhadap baris harga peranan dalam senarai harga. Pemadanan ini menganggap anda menggunakan dimensi penetapan harga luar kotak untuk kos buruh. Sebaliknya jika anda mengkonfigurasikan sistem untuk memadankan medan atau sebagai tambahan kepada **Peranan**, **Syarikat Sumber** dan **Unit Sumber** maka kombinasi berbeza akan digunakan untuk mendapatkan baris harga peranan pemadanan. Jika aplikasi mencari baris harga peranan yang mempunyai kadar kos untuk kombinasi **Peranan**, **Syarikat Sumber** dan **Unit Sumber** iaitu kadar kos lalai. Jika aplikasi tidak boleh memadankan nilai **Peranan**, **Syarikat Sumber** dan **Unit Sumber** maka aplikasi mendapatkan baris harga peranan dengan peranan padanan tetapi nilai nol **Unit Sumber**. Selepas aplikasi mendapat rekod harga peranan yang sepadan, kadar kos lalai daripada rekod itu. 

> [!NOTE]
> Jika anda mengkonfigurasikan keutamaan yang berbeza **Peranan**, **Syarikat Sumber** dan **Unit Sumber** atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku ini akan berubah sewajarnya. Sistem akan mendapatkan rekod harga peranan dengan nilai yang sepadan dengan setiap nilai dimensi penetapan harga mengikut urutan keutamaan dengan baris yang mempunyai nilai nol bagi dimensi yang terakhir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Perbelanjaan

Baris anggaran untuk Perbelanjaan merujuk kepada butiran sebut harga dan baris kontrak bagi perbelanjaan dan baris anggaran perbelanjaan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan kombinasi medan **Kategori** dan **Unit** pada baris anggaran untuk Perbelanjaan bagi pemadanan terhadap baris **Harga Kategori** pada senarai harga diselesaikan. Jika sistem mencari baris harga kategori yang mempunyai kadar kos untuk kombinasi **Kategori** dan **Unit**, kadar kos dilalaikan. Jika sistem tidak boleh memadankan nilai **Kategori** dan **Unit**, atau jika sistem berupaya mencari baris harga kategori yang berpadanan tetapi kaedah penetapan harga bukan **Unit Setiap Harga**, kadar kos dilalaikan ke kosong(0).
