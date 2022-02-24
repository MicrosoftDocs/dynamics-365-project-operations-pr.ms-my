---
title: Sediakan dasar perbelanjaan
description: Anda boleh menyediakan dasar perbelanjaan yang mesti dipatuhi oleh pekerja anda apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan dalam Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271274"
---
# <a name="set-up-expense-policies"></a>Sediakan dasar perbelanjaan

Anda boleh menakrifkan dasar yang mesti dipatuhi oleh pekerja apabila memasukkan dan menyerahkan laporan perbelanjaan dan permintaan perjalanan.         
Pelaksanaan dasar perbelanjaan boleh membantu anda mengurus perbelanjaan secara berkesan.         

Contohnya, anda boleh menetapkan dasar untuk perbelanjaan Hotel di New York City yang menyatakan bahawa perbelanjaan bagi setiap malam tidak boleh melebihi USD 250.       
Jika pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan yang kadar bilik melebihi amaun ini, sistem akan memberitahu        
pekerja bahawa amaun dasar untuk perbelanjaan telah melebihi. Anda boleh mengkonfigurasi message yang akan diterima oleh pekerja apabila anda        
menakrifkan dasar.      
        
Anda boleh menakrifkan tiga jenis dasar:         
        
- Amaran – Membenarkan pekerja menyerahkan laporan perbelanjaan atau permintaan perjalanan tetapi perbelanjaan akan ditandakan untuk semua pelulus dan        
  untuk pelaporan kemudian.        

- Ralat – Memerlukan pekerja menyemak semula perbelanjaan untuk mematuhi dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.       
 
 - Justifikasi – Memerlukan pekerja atau pengurus memasukkan justifikasi amaun melebihi jumlah dasar sebelum menyerahkan laporan perbelanjaan atau permintaan perjalanan.        

## <a name="policy-tips"></a>Tips dasar
Berikut adalah beberapa cadangan yang dapat membantu anda semasa mencipta dasar baharu untuk pengurusan perbelanjaan. 
* Dasar adalah tarikh kuat kuasa dan tidak akan berkuat kuasa jika dasar dicipta dengan tarikh selepas tarikh perbelanjaan itu berlaku. Sebagai contoh, jika anda mencipta dasar baharu hari ini untuk menguatkuasakan perbelanjaan makan maksimum sebanyak $50 berbanding sebarang perbelanjaan sedia ada yang dimasukkan semalam tidak akan disemak terhadap dasar ini.
* Apabila mencipta dasar untuk kategori perbelanjaan yang boleh diperincikan, pertimbangkan untuk menambah syarat bagi jenis baris perbelanjaan. Sesetengah dasar seperti yang memerlukan resit mungkin tidak masuk akal untuk baris yang diperincikan dan sepatutnya digunakan untuk baris pengepala atau baris yang tidak diperincikan. 
* Dasar pengurusan perbelanjaan dinilai berdasarkan entiti sumber secara lalai. Untuk senario antara syarikat, sebaliknya anda boleh menetapkan dasar untuk dinilai berdasarkan entiti destinasi (entiti pinjaman). Untuk menjalankan dasar terhadap entiti destinasi, hidupkan ciri "Nilaikan dasar Perbelanjaan terhadap peminjaman entiti undang-undang" dalam ruang kerja **Pengurusan Ciri**.

## <a name="when-to-evaluate-policies"></a>Bila untuk menilai dasar

Dalam parameter pengurusan perbelanjaan, terdapat pilihan untuk sama ada menilai dasar pengurusan perbelanjaan apabila baris disimpan atau apabila laporan perbelanjaan diserahkan. Jika anda memilih untuk menilai apabila baris disimpan ini memastikan pengguna mempunyai keterlihatan awal kepada perkara yang mereka perlu lakukan untuk melengkapkan laporan perbelanjaan mereka sekaligus. Jika tidak, anda boleh melambatkan penilaian dasar dan menjimatkan masa jika anda mempunyai pengesahan terjadi di akhir, semasa penyerahan aliran kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]