---
title: Harian
description: Topik ini memberikan maklumat tentang peraturan harian yang digunakan dalam pengurusan Perbelanjaan.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995272"
---
# <a name="per-diems"></a>Harian

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_


Harian ialah elaun yang dibayar kepada pekerja yang membuat perjalanan untuk kerja. Dalam pengurusan Perbelanjaan, anda boleh mencipta peraturan harian untuk pelbagai situasi perjalanan. Kadar harian boleh berdasarkan masa dalam tahun, lokasi perjalanan atau kedua-duanya. Apabila anda mencipta peraturan harian, anda boleh menentukan bahawa peratusan kadar harian akan ditahan jika pekerja menerima hidangan atau perkhidmatan percuma. Anda juga boleh menetapkan bilangan jam minimum dan maksimum yang kadar harian boleh gunakan kepada perjalanan pekerja.

## <a name="configuration"></a>Konfigurasi 

1. Untuk menambahkan lokasi harian, pergi ke **Sediakan** > **Pengiraan dan kod** > **Lokasi harian**.
2. Untuk setiap lokasi yang ditambahkan di atas, pilih kadar harian dan mata wang yang sah antara tarikh mula dan tamat tertentu untuk hotel, hidangan dan perbelanjaan lain. Kadar harian dan mata wang dikonfigurasikan di bawah **Sediakan** > **Pengiraan dan kod** > **Harian**.
3. Pada halaman **Lokasi harian**, konfigurasikan tahap kadar harian. Tahap kadar harian membolehkan anda mentakrifkan pecahan peratusan elaun harian untuk hotel, hidangan dan perbelanjaan lain. 
4. Untuk menentukan pengurangan peratusan hidangan untuk sarapan, makan tengah hari atau makan malam, kemas kini medan pada halaman **Parameter pengurusan perbelanjaan** pada tab **Harian**. 
    
## <a name="submit-expenses-using-per-diem"></a>Serahkan perbelanjaan menggunakan harian
Untuk menyerahkan perbelanjaan menggunakan harian, gunakan kategori perbelanjaan **Harian** apabila anda mencipta laporan perbelanjaan. Masukkan **Harian daripada tarikh**, **Harian daripada tarikh** dan **Lokasi harian**. Amaun akan dikira berdasarkan kadar harian untuk lokasi yang dipilih dan pengurangan hidangan akan dikira berdasarkan tahap kadar harian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]