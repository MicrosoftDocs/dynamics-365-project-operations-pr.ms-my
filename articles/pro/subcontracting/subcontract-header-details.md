---
title: Butiran pengepala untuk subkontrak
description: Topik ini menerangkan fungsian yang diberikan pada pengepala subkontrak dalam Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501337"
---
# <a name="header-details-for-subcontracts"></a>Butiran pengepala untuk subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini menerangkan fungsian yang diberikan pada pengepala subkontrak dalam Dynamics 365 Project Operations.

Disebabkan Pengurus Projek merancang dan melaksanakan projek, mereka boleh menggunakan subkontraktor dan membeli produk dan perkhidmatan daripada vendor. Apabila Pengurus Projek perlu membeli produk atau perkhidmatan, mereka boleh mencipta subkontrak dalam Project Operations.

Untuk mencipta subkontrak, lengkapkan langkah berikut.

1. Dalam anak tetingkap navigasi, pilih **Subkontrak** dan pada halaman **Subkontrak**, pilih **Baharu**.
2. Masukkan maklumat diperlukan dan kemudian pilih **Simpan**.

    Jadual berikut memberikan maklumat tentang medan pada halaman **Pengepala subkontrak**.

    | Medan | Penerangan |Kesan Kefungsian |
    |---|------|---| 
    | Nama | Nama subkontrak. | Dalam semua senarai juntai bawah subkontrak, nama subkontrak disenaraikan dalam lajur pertama untuk membantu anda mengenal pasti subkontrak. | 
    | Penerangan | Penerangan ringkas tentang perkhidmatan dan produk yang dibeli pada subkontrak. | Tiada |
    | Vendor | Nama syarikat yang produk dan perkhidmatan dibeli. Rekod akaun ini mempunyai jenis perhubungan **Vendor** atau **Pembekal**. | Berdasarkan pada vendor yang dipilih, nilai lalai akan dimasukkan secara automatik untuk medan berikut:<br/> **• Mata Wang** </br> **• Senarai Harga** </br> **• Terma Pembayaran**</br> **• Alamat Pembayaran**</br> **• Alamat Bil Kepada**</br> **• Nama Bil Kepada** </br>**• Pengurus Akaun Vendor**|
    | Tarikh Subkontrak | Tarikh subkontrak dicipta. | Tarikh subkontrak digunakan untuk memilih senarai harga pembelian yang betul sama ada daripada senarai harga yang dilampirkan ke vendor berkaitan atau daripada parameter projek. |
    | Sebab Status | Status subkontrak. | Status menentukan tempat subkontrak dalam proses perniagaan dan sama ada ia boleh diedit. <br/>Nilai termasuk:<br>• **Draf**: Subkontrak boleh diedit. Anda hanya boleh mengedit subkontrak dengan status **Draf**.<br/>• **Disahkan**: Rundingan dengan vendor adalah lengkap dan subkontrak diluluskan untuk penghantaran. <br/>• **Ditutup**: Penghantaran ke atas subkontrak selesai.<br/>• **Dibatalkan**: Subkontrak telah dibatalkan dan tiada penghantaran dirancang.  | 
    | Mata wang | Mata wang bagi produk dan perkhidmatan yang dibeli. Nilai lalai akan dimasukkan secara automatik daripada akaun vendor tetapi ia boleh ditukar. | Mata wang subkontrak digunakan untuk memilih senarai harga pembelian sama ada daripada senarai harga yang dilampirkan ke vendor berkaitan atau daripada parameter projek. Senarai harga dalam mata wang lain tidak boleh dikaitkan dengan subkontrak. Kos masa, perbelanjaan dan bahan yang dihantar oleh sumber vendor daripada subkontrak ini akan direkodkan dalam mata wang ini pada projek. Selepas rekod subkontrak disimpan, mata wang pada subkontrak tidak boleh ditukar.|
    | Unit Pengkontrakan | Bahagian syarikat yang mengikat kontrak pembelian atau subkontrak dengan vendor. | Tiada |
    | Terma pembayaran | Terma pembayaran invois vendor yang dikeluarkan pada subkontrak ini. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Terma pembayaran daripada subkontrak akan disalin ke semua invois vendor yang berkaitan dengan subkontrak ini. Terma pembayaran boleh dikemaskini jika subkontrak mempunyai status **Draf**. | 
    | Alamat Pembayaran | Alamat vendor untuk penghantaran pembayaran. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Alamat pembayaran daripada subkontrak disalin sebagai alamat pembayaran ke semua invois vendor yang dicipta untuk subkontrak ini. Alamat pembayaran boleh dikemaskini jika subkontrak mempunyai status **Draf**.|
    | Nama Bil Kepada | Nama individu atau bahagian dalam syarikat vendor yang akan menghantar invois. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Nilai **Nama Bil Kepada** daripada subkontrak disalin ke semua invois vendor yang berkaitan dengan subkontrak ini. Medan ini boleh dikemaskini jika subkontrak mempunyai status **Draf**.|
    | Alamat Bil Kepada | Alamat yang digunakan pada invois daripada vendor. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. | Alamat ini adalah alamat "invois daripada" pada invois vendor yang dicipta untuk subkontrak ini. |
    | Jumlah kecil | Jika subkontrak tidak mempunyai baris, masukkan subjumlah pesanan sebelum cukai. Jika subkontrak mempunyai baris, medan ini adalah baca sahaja. Jumlah yang ditunjukkan ialah amaun subjumlah daripada semua baris pada subkontrak. | Tiada |
    | Jumlah Cukai | Jika subkontrak tidak mempunyai baris, masukkan jumlah cukai pada subkontrak ini. Jika subkontrak mempunyai baris, medan ini adalah baca sahaja. Jumlah yang ditunjukkan ialah jumlah amaun cukai daripada semua baris pada subkontrak. | Tiada |
    | Jumlah Amaun | Medan dikira ini menunjukkan jumlah amaun subkontrak selepas cukai dimasukkan. | Tiada |
    | Tarikh Disahkan | Tarikh subkontrak disahkan. | Tiada |
    | Diminta Oleh | Secara lalai, medan ini ditetapkan kepada nama pengguna yang mencipta subkontrak. Walau bagaimanapun pencipta subkontrak boleh mengubah nilai untuk menunjukkan individu yang mereka ciptakan subkontrak. | Tiada |
    | Pengurus Akaun Vendor | Nama kenalan utama akaun vendor. Nilai lalai akan dimasukkan secara automatik daripada rekod akaun vendor. Anda boleh memilih kenalan yang berbeza sebagai pengurus akaun vendor bagi subkontrak. | Anda boleh menyediakan isyarat e-mel untuk memberitahu kenalan apabila perubahan dibuat kepada subkontrak sebagai hasil daripada rundingan harga. |
