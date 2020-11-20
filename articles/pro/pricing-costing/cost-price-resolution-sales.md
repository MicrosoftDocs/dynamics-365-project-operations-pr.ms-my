---
title: Selesaikan harga kos berkaitan anggaran dan aktual - ringan
description: Topik ini menyediakan maklumat tentang cara harga kos pada anggaran dan aktual diselesaikan.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176802"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Selesaikan harga kos berkaitan anggaran dan aktual - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Untuk menyelesaikan harga kos dan senarai harga kos bagi anggaran dan aktual, sistem ini menggunakan maklumat dalam medan **Tarikh**, **Mata Wang** dan **Unit Kontrak** untuk projek berkaitan. Selepas senarai harga kos diselesaikan, aplikasi ini menyelesaikan kadar kos.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Masa

Baris anggaran untuk Masa merujuk kepada butiran sebut harga dan baris kontrak bagi tugasan masa dan sumber pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan medan **Peranan** dan **Unit Sumber** pada baris anggaran untuk Masa bersaing dengan baris harga peranan dalam senarai harga. Pemadanan ini menganggap anda menggunakan dimensi penetapan harga luar kotak untuk kos buruh. Jika anda mengkonfigurasi sistem untuk sepadan dengan bidang bukan atau sebagai tambahan **Peranan** dan **Unit Sumber** kemudian kombinasi berbeza akan digunakan untuk mendapatkan baris harga peranan yang berpadanan. Jika aplikasi mencari baris harga peranan yang mempunyai kadar kos untuk kombinasi **Peranan** dan **Unit Sumber** yang merupakan kadar kos lalai. Jika aplikasi tidak boleh memadankan nilai **Peranan** dan **Unit Sumber** kemudian ia akan mendapatkan baris harga peranan dengan peranan yang berpadan tetapi nilai nol **Unit Sumber**. Selepas aplikasi mendapat rekod harga peranan yang sepadan, kadar kos lalai daripada rekod itu. 

> [!NOTE]
> Jika anda mengkonfigurasi keutamaan **Peranan** dan **Unit Sumber** yang berbeza atau jika anda mempunyai dimensi lain yang mempunyai keutamaan lebih tinggi, tingkah laku ini akan berubah sewajarnya. Sistem akan mendapatkan rekod harga peranan dengan nilai yang sepadan dengan setiap nilai dimensi penetapan harga mengikut urutan keutamaan dengan baris yang mempunyai nilai nol bagi dimensi yang terakhir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menyelesaikan kadar kos pada baris aktual dan anggaran untuk Perbelanjaan

Baris anggaran untuk Perbelanjaan merujuk kepada butiran sebut harga dan baris kontrak bagi perbelanjaan dan baris anggaran perbelanjaan pada projek.

Selepas senarai harga kos diselesaikan, sistem menggunakan kombinasi medan **Kategori** dan **Unit** pada baris anggaran untuk Perbelanjaan bagi pemadanan terhadap baris **Harga Kategori** pada senarai harga diselesaikan. Jika sistem mencari baris harga kategori yang mempunyai kadar kos untuk kombinasi **Kategori** dan **Unit**, kadar kos dilalaikan. Jika sistem tidak boleh memadankan nilai **Kategori** dan **Unit**, atau jika sistem berupaya mencari baris harga kategori yang berpadanan tetapi kaedah penetapan harga bukan **Unit Setiap Harga**, kadar kos dilalaikan ke kosong(0).
