---
title: Penyenaraian perbelanjaan
description: Topik ini menerangkan cara memperincikan perbelanjaan menggunakan ruang kerja Perbelanjaan yang dibayangkan semula.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574533"
---
# <a name="expense-itemization"></a>Penyenaraian perbelanjaan

[!include [banner](../includes/banner.md)]

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Organisasi sering memerlukan pekerja untuk memberikan pecahan terperinci perbelanjaan yang ditanggung semasa perjalanan. Sebagai contoh, folio hotel mungkin mengandungi beberapa garisan terperinci untuk harga bilik, cukai, tempat letak kereta, dan perbelanjaan pelbagai lain yang ditanggung setiap hari sepanjang tempoh penginapan. Atau perbelanjaan makan mungkin memerlukan anda menyediakan pecahan yang lebih terperinci untuk sarapan, makan tengah hari, atau makan malam. Walau apa pun keperluan organisasi, setiap kategori perbelanjaan boleh disediakan untuk mencerminkan subkategori atau item baris yang membentuk perbelanjaan. Walaupun pengetinan sentiasa disokong dalam **pengurusan Perbelanjaan,** ruang kerja perbelanjaan **yang dibayangkan semula membolehkan perincian yang lebih cekap apabila ciri tersebut,** Keupayaan untuk memperincikan perbelanjaan berulang dengan cepat **didayakan**.  

## <a name="enable-quick-itemization"></a>Mendayakan pengetinan pantas 

Anda boleh menggunakan **Keupayaan untuk memperincikan perbelanjaan berulang dengan cepat** untuk memperincikan perbelanjaan berulang dengan cepat sambil mengelakkan keperluan untuk memasukkan perbelanjaan harian setiap kali untuk tempoh penginapan. Lengkapkan langkah berikut untuk mendayakan pemantasan pantas.

1. Pergi ke **ruang kerja Pengurusan** Ciri dan dalam senarai ciri, cari dan pilih, **Laporan Perbelanjaan Dibayangkan Semula**. 
2. Pilih **Dayakan sekarang**. 
3. Dalam senarai ciri, cari dan pilih, **Keupayaan untuk memperincikan perbelanjaan berulang dengan cepat**.
4. Pilih **Dayakan sekarang**. 

## <a name="itemization-grid"></a>Grid itemisasi 

Jika kategori perbelanjaan mempunyai subkategori atau komponen yang berbeza yang membentuk perbelanjaan itu, maka ia boleh diperincikan. Untuk memperincikan perbelanjaan, pilih baris perbelanjaan dalam laporan perbelanjaan dan dalam **anak tetingkap Butiran** perbelanjaan, pilih **Saiz** > **Item Tindakan**. Slaid **Itemisasi** mendedahkan grid dengan medan. Jadual berikut menyediakan contoh setiap medan dalam grid dan cara medan diterap dalam laporan perbelanjaan. 

|     Medan          |     Description                                                                                  |     Contoh              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subkategori    |     Senarai subkategori yang dikonfigurasikan di bawah jenis kategori perbelanjaan, **Hotel**.             |     Harga bilik harian      |
|     Tarikh mula     |     Tarikh item perbelanjaan pertama kali ditanggung.                                           |     09/13/2021           |
|     Kadar Harian     |     Amaun yang ditanggung untuk item perbelanjaan.                                                    |     200                  |
|     Kuantiti       |     Bilangan kali caj diulang dalam tempoh yang berterusan.                       |     3                    |

![Memperincikan perbelanjaan.](media/Itemization%20screen%201.png)

Apabila anda menyimpan item, anda akan melihat baris terperinci individu untuk kuantiti yang ditentukan dalam grid Itemisasi. Setiap baris bermula pada tarikh yang ditentukan dalam grid.

![Laporan terperinci.](media/Itemization%20screen%202.png)

