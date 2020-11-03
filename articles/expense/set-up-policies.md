---
title: Takrifkan dasar perbelanjaan
description: Anda boleh menakrifkan dasar perbelanjaan yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081298"
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
        
- **Amaran** : Membenarkan pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan tetapi perbelanjaan akan ditandakan untuk semua pelulus dan         
  untuk pelaporan kemudian.        

- **Ralat** : Memerlukan pekerja menyemak semula perbelanjaan untuk mematuhi dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.        
 
 - **Justifikasi** : Memerlukan pekerja atau Pengurus memasukkan justifikasi amaun melebihi jumlah dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.        

## <a name="policy-tips"></a>Tips dasar
Berikut adalah beberapa cadangan yang dapat membantu anda semasa membuat dasar baru untuk pengurusan perbelanjaan: 

- Dasar adalah tarikh berkuatkuasa bermaksud dasar tidak akan berkuatkuasa jika ianya dibuat dengan tarikh selepas tarikh perbelanjaan itu berlaku. Contohnya, anda mencipta dasar baharu hari ini untuk menguatkuasakan perbelanjaan hidangan maksimum sebanyak $50. Sebarang perbelanjaan sedia ada yang dimasukkan pada hari semalam tidak akan disemak berdasarkan dasar ini.
- Apabila mencipta dasar untuk kategori perbelanjaan yang boleh diperincikan, pertimbangkan untuk menambah syarat bagi jenis baris perbelanjaan. Sesetengah dasar seperti yang memerlukan resit mungkin tidak masuk akal untuk baris yang diperincikan. Dalam keadaan ini, dasar hanya digunakan untuk baris pengepala atau baris yang tidak diperincikan. 
- Dasar pengurusan perbelanjaan dinilai berdasarkan entiti sumber secara lalai. Untuk senario antara syarikat, sebaliknya anda boleh menetapkan dasar untuk dinilai berdasarkan entiti destinasi (entiti pinjaman). Untuk menjalankan dasar berdasarkan entiti destinasi, hidupkan ciri **Nilaikan entiti undang-undang peminjaman berdasarkan dasar** dalam ruang kerja **Pengurusan ciri**.

## <a name="when-to-evaluate-policies"></a>Bila untuk menilai dasar

Dalam parameter pengurusan perbelanjaan, anda boleh memilih untuk menilai dasar pengurusan perbelanjaan apabila baris disimpan atau apabila laporan perbelanjaan diserahkan. Jika anda memilih untuk menilai apabila baris disimpan, pengguna akan mempunyai keterlihatan awal kepada apa yang mereka perlu lakukan untuk melengkapkan laporan perbelanjaan mereka sekaligus. Jika tidak, anda boleh melambatkan penilaian dasar dan menjimatkan masa dengan mengesahkan di akhir, semasa penyerahan aliran kerja.
