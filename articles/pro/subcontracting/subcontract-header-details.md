---
title: Butiran pengepala untuk subkontrak
description: Topik ini menerangkan fungsian yang diberikan pada pengepala subkontrak dalam Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323652"
---
# <a name="header-details-for-subcontracts"></a>Butiran pengepala untuk subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini menerangkan fungsian yang diberikan pada pengepala subkontrak dalam Dynamics 365 Project Operations.

Disebabkan Pengurus Projek merancang dan melaksanakan projek, mereka boleh menggunakan subkontraktor dan membeli produk dan perkhidmatan daripada vendor. Apabila Pengurus Projek perlu membeli produk atau perkhidmatan, mereka boleh mencipta subkontrak dalam Project Operations.

Untuk mencipta subkontrak, lengkapkan langkah berikut.

1. Dalam anak tetingkap navigasi, pilih **Subkontrak** dan pada halaman **Subkontrak**, pilih **Baharu**.
2. Masukkan maklumat diperlukan dan kemudian pilih **Simpan**.

    Jadual berikut memberikan maklumat tentang medan pada halaman pengepala Subkontrak.

    | **Medan** | **Perihalan** |
    | --- | --- | 
    | Nama | Nama subkontrak. |
    | Penerangan | Penerangan ringkas tentang perkhidmatan dan produk yang dibeli pada subkontrak. |
    | Vendor | Nama syarikat yang produk dan perkhidmatan dibeli. Rekod akaun ini mempunyai jenis perhubungan **Vendor** atau **Pembekal**. |
    | Tarikh Subkontrak | Tarikh subkontrak dicipta. |
    | Sebab Status | Status subkontrak. |
    | Mata wang | Mata wang yang produk dan perkhidmatan dibeli. Nilai dalam medan ini terlalai daripada akaun vendor tetapi boleh diubah. Senarai harga projek yang digunakan untuk produk dan perkhidmatan penetapan harga pada subkontrak hendaklah dalam mata wang ini. Senarai harga dalam mana-mana mata wang lain tidak boleh dikaitkan dengan subkontrak. Kos produk dan perkhidmatan yang dikenakan pada subkontrak ini akan direkodkan pada projek dalam mata wang ini. |
    | Unit Pengkontrakan | Bahagian syarikat yang mengikat kontrak pembelian atau subkontrak dengan vendor. |
    | Terma pembayaran | Terma pembayaran pada invois vendor yang dikeluarkan pada subkontrak ini. Nilai dalam medan ini terlalai daripada rekod akaun vendor. |
    | Alamat Pembayaran | Alamat yang pembayaran pada invois vendor akan dihantar. Nilai dalam medan ini terlalai daripada rekod akaun vendor. |
    | Nama Bil Kepada | Nama individu atau bahagian dalam syarikat vendor yang akan menghantar invois. Nilai dalam medan ini terlalai daripada rekod akaun vendor dan akan digunakan sebagai nama kenalan utama pada invois vendor yang dicipta untuk subkontrak ini. |
    | Alamat Bil kepada | Alamat yang digunakan pada invois daripada vendor ini. Nilai dalam medan ini terlalai daripada rekod akaun vendor. Alamat ini juga digunakan sebagai invois daripada alamat pada invois vendor yang dicipta untuk subkontrak ini. |
    | Jumlah kecil | Jika subkontrak tidak mempunyai baris, masukkan nilai dalam medan ini yang menandakan jumlah kecil pesanan sebelum cukai. Jika subkontrak mempunyai baris, medan ini adalah baca sahaja. Amaun yang dipaparkan ialah amaun jumlah kecil daripada semua baris pada subkontrak. |
    | Jumlah Cukai | Jika subkontrak tidak mempunyai baris, masukkan nilai dalam medan ini yang menandakan cukai pada subkontrak ini. Jika subkontrak mempunyai baris, medan ini adalah baca sahaja. Amaun yang dipaparkan ialah jumlah amaun cukai daripada semua baris pada subkontrak. |
    | Jumlah Amaun |  Medan dikira ini menunjukkan jumlah amaun subkontrak selepas cukai dimasukkan.  |
    | Tarikh Disahkan | Tarikh yang subkontrak telah disahkan.  |
    | Diminta Oleh | Nilai dalam medan ini terlalai kepada nama pengguna yang mencipta subkontrak. Nilai ini boleh diubah oleh pencipta subkontrak untuk menunjukkan orang itu bagi pihak orang yang mencipta subkontrak.  |
    | Pengurus Akaun Vendor | Nama kenalan utama akaun vendor. Nilai dalam medan ini terlalai daripada rekod akaun vendor. Nilai medan ini boleh diubah oleh pengguna untuk memilih kenalan yang berbeza sebagai pengurus akaun vendor subkontrak. Isyarat e-mel dan rundingan harga boleh dikonfigurasikan dan dihantar oleh kenalan ini. |


