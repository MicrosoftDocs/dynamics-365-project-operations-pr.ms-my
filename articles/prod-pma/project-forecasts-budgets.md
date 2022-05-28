---
title: Ramalan dan belanjawan projek
description: Microsoft Dynamics 365 Kewangan menyediakan ramalan projek dan belanjawan projek untuk mengurus dan mengawal projek anda.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15731010877b5d62329867e878f624149e74f761
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684561"
---
# <a name="project-forecasts-and-budgets"></a>Ramalan dan belanjawan projek

[!include [banner](../includes/banner.md)]

Terdapat dua cara untuk mengurus dan mengawal projek anda: ramalan projek dan belanjawan projek. 

Gunakan ramalan projek jika organisasi anda mempunyai perspektif operasi dan jika ia bertumpu pada hasil dan kos yang diperoleh daripada transaksi tertentu. Gunakan belanjawan projek jika organisasi anda bertumpu lebih banyak pada jumlah kewangan. 

Ramalan projek dan belanjawan projek menggunakan model ramalan untuk menahan jumlah transaksi yang dijangka. 

Setiap kaedah mempunyai kelebihan sendiri. Anda harus mempertimbangkan perkara yang berikut sebelum anda memilih kaedah untuk organisasi anda.

|   Kaedah peruntukan       |           Ramalan projek            |        Belanjawan projek                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Peruntukan tempoh**     | Anda tidak boleh memperuntukkan transaksi secara nyata sepanjang tempoh fiskal. Sebaliknya, ramalan dan kawalan ramalan tersebut, adalah berdasarkan jangka hayat projek. Oleh sebab ramalan adalah berdasarkan tarikh tertentu, anda mesti membuat kesimpulan tempoh daripada tarikh tersebut. | Anda tidak boleh memperuntukkan transaksi pada keseluruhan projek atau sepanjang tempoh fiskal. Jika anda memperuntukkan sepanjang suatu tempoh, anda boleh membawa jumlah yang tidak digunakan kepada tempoh fiskal yang seterusnya. |
| **Melihat transaksi**  | Anda boleh melihat transaksi dalam borang ramalan, yang anda boleh melihat ramalan untuk seluruh syarikat dan untuk semua projek, tanpa mengira hierarki. Untuk berfokus pada projek tertentu, anda mesti menapis data.                                       | Anda boleh melihat transaksi yang diperuntukkan belanjawan untuk hierarki projek tunggal. Oleh itu, anda boleh melihat butiran transaksi untuk projek induk atau subprojek.                 |
| **Pemboleh ubah transaksi** | Apabila anda memasukkan transaksi ramalan, anda boleh menggunakan setiap atribut yang wujud untuk transaksi sebenar. Ini membolehkan anda mendapat butiran lebih tepat dalam ramalan. Sebagai contoh, anda boleh memasukkan butiran untuk kuantiti, pekerja, item atau sifat baris.         | Apabila anda memasukkan butiran belanjawan, anda hanya boleh menggunakan jumlah, kategori dan aktiviti.                    |
| **Keselamatan**              | Ramalan adalah berdasarkan transaksi yang anda masukkan dalam borang ramalan dan tidak melibatkan mekanisme kawalan proses. Mana-mana pekerja yang mempunyai keizinan untuk borang ramalan boleh menyemak semula maklumat tanpa kelulusan.                                        | Belanjawan menggunakan sistem aliran kerja, yang membolehkan pengurusan perubahan dan membolehkan anda menyimpan sejarah semakan semula.         |
| **Jenis entri**           | Entri transaksi ramalan adalah berdasarkan bilangan unit dan pada harga unit kos dan jualan.  | Butiran belanjawan adalah berdasarkan jumlah, yang dibahagikan antara kos dan hasil.                                          |
| **Model ramalan**       | Oleh sebab setiap ramalan mesti dikaitkan dengan model, anda boleh mencipta berbilang model ramalan dan juga menyediakan submodel.           | Belanjawan projek mengehadkan model ramalan yang digunakan untuk belanjawan. Model ramalan yang sedikit boleh membantu anda meningkatkan kekonsistenan dalam unjuran.                           |
| **Limpahan kos**         | Anda hanya boleh membenarkan atau tidak membenarkan entri transaksi yang akan menyebabkan limpahan kos.   | Belanjawan projek menyediakan pilihan kawalan tambahan untuk pengguna. Anda boleh membenarkan amaran dan limpahan.                    |
| **Kawalan**               | Kawalan ramalan dilakukan dengan menggunakan pengurangan ramalan. Jumlah sebenar ditolak daripada baki transaksi ramalan tanpa apa-apa jejak audit. Ini boleh menyukarkan penjejakan titik yang transaksi sebenar berlaku.                   | Dalam kawalan belanjawan projek, jumlah sebenar ditolak daripada jumlah dalam belanjawan yang tinggal. Ini memberikan jejak audit yang lebih jelas.                                   |

## <a name="project-forecasts"></a>Ramalan projek
Apabila anda menggunakan ramalan projek, anda boleh memasukkan transaksi ramalan dalam borang ramalan untuk setiap jenis transaksi. Setiap atribut yang tersedia untuk transaksi sebenar boleh digunakan untuk transaksi ramalan—sebagai contoh, kebolehuntungan baris, atribut baris, pekerja atau perihalan. Anda juga boleh menunjurkan tempoh daripada selepas anda menanggung kos sehingga masa anda akan menghantar invois kepada pelanggan. 

Transaksi ramalan projek adalah berdasarkan unit dan jumlah. 

Anda mesti mengaitkan setiap ramalan projek dengan model ramalan. Apabila anda memasukkan transaksi ramalan, model ramalan akan dicadangkan secara automatik. Model ramalan bertindak sebagai bekas untuk transaksi ramalan. 

Anda boleh menetapkan model ramalan sebagai submodel untuk model. Ini membolehkan anda membuat ramalan mengikut rantau, tempoh masa atau bahagian. Anda boleh menyalin transaksi ramalan dalam model untuk mencipta model baharu, dan anda juga boleh memindahkan transaksi kepada lejar am. Oleh sebab terdapat hubungan satu ke satu antara ramalan dan model, setiap model ramalan membentuk belanjawan yang berasingan untuk projek. 

Model ramalan boleh menggunakan pengurangan ramalan sebagai mekanisme kawalan untuk projek. Dalam pengurangan ramalan, transaksi sebenar akan mengurangkan baki transaksi ramalan. Namun, oleh sebab pengurangan ramalan digunakan untuk projek tertinggi dalam hierarki, ia menyediakan pandangan terhad terhadap perubahan dalam ramalan. Sebagai contoh, jika pekerja dikaitkan dengan subprojek, transaksi sebenar untuk pekerja dihantar kepada projek induk. Ini boleh menyukarkan penjejakan perubahan, kerana anda tidak boleh menentukan transaksi yang subprojeknya menyebabkan pengurangan pada jumlah ramalan dengan mudah. Oleh itu, idea yang terbaik adalah untuk mencipta salinan model ramalan untuk digunakan oleh pengurangan ramalan. Anda kemudian boleh menggunakan laporan untuk melihat perkara yang diramalkan pada asalnya. 

Anda boleh menyemak semula, menyalin, memadamkan atau memindahkan ramalan projek kepada belanjawan lejar am. Walau bagaimanapun, tiada kawalan proses. Mana-mana pekerja yang mempunyai keizinan untuk borang ramalan boleh membuat semakan semula tanpa ulasan.

-   **Semak semula**– Anda boleh menyemak semula transaksi ramalan dalam borang yang sama yang entri asal telah dibuat.
-   **Salin atau padam** – Apabila anda menyalin ramalan transaksi, anda menyalin baris transaksi satu model ramalan kepada model ramalan yang lain. Apabila anda memadamkan ramalan, anda memadamkan transaksi ramalan daripada model ramalan. Untuk mengehadkan transaksi ramalan yang disalin atau dipadamkan, pilih jenis transaksi dan tarikh tertentu. Ini membolehkan anda hanya menyalin atau memadamkan bahagian ramalan yang khusus.
-   **Pindahkan** – Apabila anda memindahkan ramalan projek kepada belanjawan lejar am, anda memindahkan transaksi ramalan dalam model ramalan kepada belanjawan lejar am. Anda boleh menulis ganti mana-mana transaksi yang sebelumnya dipindahkan dalam belanjawan lejar am yang anda pindahkan ramalan projek anda.

## <a name="project-budgets"></a>Belanjawan projek
Belanjawan projek merupakan cara yang lebih mudah daripada ramalan, walaupun ia berintegrasi dengan model ramalan. Ia menggunakan borang entri tunggal untuk butiran belanjawan asal dan semakan semula, dan menyediakan unjuran yang hanya berdasarkan jumlah, kategori atau aktiviti. 

Dalam belanjawan projek, semua belanjawan asal dan semakan semula mesti dihantar kepada aliran kerja projek untuk diluluskan. Aliran kerja memberi anda kawalan yang lebih banyak terhadap proses dan mencipta rekod sejarah perubahan. 

Belanjawan projek menyerupai belanjawan lejar am, tetapi lebih cepat dan lebih mudah untuk disediakan. Kebanyakan pilihan dalam belanjawan lejar am, seperti nombor urutan atau mata wang, tidak perlu disediakan secara berasingan untuk projek.

Belanjawan projek dikaitkan secara automatik dengan dua model ramalan, satu untuk belanjawan asal dan satu untuk belanjawan yang tinggal. Oleh itu, laporan yang berdasarkan model ramalan boleh menggunakan data belanjawan. Apabila belanjawan projek diserahkan, sistem mencipta transaksi ramalan berdasarkan model yang dikaitkan, yang digunakan untuk tujuan laporan dan kawalan.

## <a name="forecast-models"></a>Model ramalan
Model ramalan mempunyai hierarki lapisan tunggal. Ini bermaksud satu ramalan projek mesti dikaitkan dengan satu model ramalan.

Jika anda menggunakan ramalan projek, anda boleh mengenal pasti model sebagai submodel. Anda kemudian boleh mencipta ramalan mengikut bahagian, tempoh masa atau rantau. Sebagai contoh, anda boleh mencipta model ramalan untuk setahun dan kemudian cipta submodel untuk ramalan serantau Timur Laut, Tenggara, Barat Laut dan Barat Daya yang diserahkan oleh ketua serantau. Dengan memilih pilihan yang berbeza dalam laporan yang tersedia, anda boleh melihat maklumat mengikut jumlah ramalan atau mengikut submodel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]