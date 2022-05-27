---
title: Takrifkan dasar perbelanjaan
description: Anda boleh menakrifkan dasar perbelanjaan yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ae6de664fc18a00fd6d3d6c8177daa95da5754d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576925"
---
# <a name="define-expense-policies"></a>Takrifkan dasar perbelanjaan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda boleh menakrifkan dasar yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.         
Pelaksanaan dasar perbelanjaan boleh membantu anda mengurus perbelanjaan secara berkesan.         

Contohnya, anda boleh menetapkan dasar untuk perbelanjaan Hotel di New York City yang menyatakan bahawa perbelanjaan bagi setiap malam tidak boleh melebihi USD 250.       
Jika pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan yang kadar bilik melebihi amaun ini, sistem akan memberitahu         
pekerja bahawa amaun dasar untuk perbelanjaan telah melebihi. Anda boleh mengkonfigurasi message yang akan diterima oleh pekerja apabila anda        
menakrifkan dasar.      
        
Anda boleh menakrifkan tiga jenis dasar:         
        
- **Amaran**: Membenarkan pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan tetapi perbelanjaan akan ditandakan untuk semua pelulus dan         
  untuk pelaporan kemudian.        

- **Ralat**: Memerlukan pekerja menyemak semula perbelanjaan untuk mematuhi dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.        
 
 - **Justifikasi**: Memerlukan pekerja atau Pengurus memasukkan justifikasi amaun melebihi jumlah dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.        

## <a name="policy-tips"></a>Tips dasar
Berikut adalah beberapa cadangan yang dapat membantu anda semasa membuat dasar baru untuk pengurusan perbelanjaan: 

- Dasar adalah tarikh berkuatkuasa bermaksud dasar tidak akan berkuatkuasa jika ianya dibuat dengan tarikh selepas tarikh perbelanjaan itu berlaku. Contohnya, anda mencipta dasar baharu hari ini untuk menguatkuasakan perbelanjaan hidangan maksimum sebanyak $50. Sebarang perbelanjaan sedia ada yang dimasukkan pada hari semalam tidak akan disemak berdasarkan dasar ini.
- Apabila mencipta dasar untuk kategori perbelanjaan yang boleh diperincikan, pertimbangkan untuk menambah syarat bagi jenis baris perbelanjaan. Sesetengah dasar seperti yang memerlukan resit mungkin tidak masuk akal untuk baris yang diperincikan. Dalam keadaan ini, dasar hanya digunakan untuk baris pengepala atau baris yang tidak diperincikan. 
- Dasar pengurusan perbelanjaan dinilai berdasarkan entiti sumber secara lalai. Untuk senario antara syarikat, sebaliknya anda boleh menetapkan dasar untuk dinilai berdasarkan entiti destinasi (entiti pinjaman). Untuk menjalankan dasar berdasarkan entiti destinasi, hidupkan ciri **Nilaikan entiti undang-undang peminjaman berdasarkan dasar** dalam ruang kerja **Pengurusan ciri**.

## <a name="when-to-evaluate-policies"></a>Bila untuk menilai dasar

Dalam parameter pengurusan perbelanjaan, anda boleh memilih untuk menilai dasar pengurusan perbelanjaan apabila baris disimpan atau apabila laporan perbelanjaan diserahkan. Jika anda memilih untuk menilai apabila baris disimpan, pengguna akan mempunyai keterlihatan awal kepada apa yang mereka perlu lakukan untuk melengkapkan laporan perbelanjaan mereka sekaligus. Jika tidak, anda boleh melambatkan penilaian dasar dan menjimatkan masa dengan mengesahkan di akhir, semasa penyerahan aliran kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]