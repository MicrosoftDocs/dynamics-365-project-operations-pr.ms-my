---
title: Harian
description: Artikel ini memberikan maklumat tentang peraturan saraan harian yang digunakan dalam pengurusan Perbelanjaan.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930191"
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