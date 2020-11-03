---
title: Kontrak berasaskan pendahuluan dan retainer
description: Topik ini memberikan maklumat tentang model kontrak berasaskan retainer dan pendahuluan dalam Operasi Projek.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088024"
---
# <a name="advances-and-retainer-based-contracts"></a>Kontrak berasaskan pendahuluan dan retainer 


_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dynamics 365 Project Operations menyokong kontrak berasaskan retainer. Kontrak berasaskan retainer merupakan set rundingan pembayaran yang diagihkan sama rata yang mana pelanggan akan diinvoiskan untuk sepanjang tempoh projek. Jenis kontrak ini biasanya digunakan untuk model pengebilan berasaskan masa dan material atau penggunaan yang mana terdapat keperluan untuk memberi pelanggan invois dan jadual pembayaran yang boleh diramal. Hasil sebenar terakru setiap tempoh akan diselaraskan dengan pembayaran yang diterima daripada pelanggan pada awal tempoh tersebut. Menurut konsep model pengebilan Masa dan Bahan, nilai hasil terakru dalam setiap tempoh mungkin berbeza dengan kos yang ditanggung. Jika hasil terakru lebih daripada jumlah yang diterima pada awal tempoh tersebut, syarikat penghantaran projek boleh:

- Hanya invois pelanggan untuk lebihan 
- Tangguhkan penyelarasan hasil kepada tempoh penginvoisan yang seterusnya dan buat satu bil akhir pada penghujung projek untuk sebarang hasil berbaki yang tidak diselaraskan

Perbezaan utama antara model kontrak berasaskan retainer dan model kontrak harga tetap dalam Operasi Projek ialah dalam model kontrak harga tetap, jumlah invois tidak dikaitkan atau terikat dengan kos yang ditanggung. Penginvoisan mengikut pendekatan berasaskan pencapaian yang disejajarkan dengan kos yang ditanggung untuk tempoh tersebut. Dalam kontrak berasaskan retainer, hasil yang boleh diinvoiskan akan direkodkan berdasarkan kaedah pengebilan pada baris kontrak. Apabila kaedah pengebilan ialah masa dan bahan, hasil yang boleh diinvois terikat dengan kos yang ditanggung dalam mana-mana sesuatu tempoh dan mungkin berbeza dari tempoh ke tempoh. Walau bagaimanapun, pelanggan hanya diinvois untuk jumlah pada retainer berkala. Sistem menggunakan invois lain pada akhir tempoh untuk menyelaraskan hasil boleh diinvois yang direkodkan dalam tempoh itu dengan jumlah yang pelanggan telah diinvois untuk permulaan tempoh tersebut.

Kelebihan kaedah ini ialah kos pelanggan dapat diramalkan dalam jadual retainer tidak seperti dalam model masa dan bahan yang biasa. Organisasi yang menghantar projek juga mempunyai sedikit ruang untuk menampung risiko bagi memulihkan kos yang ditanggung disebabkan oleh sebarang peningkatan dalam skop yang mana model harga tetap tidak akan benarkan mereka berbuat demikian.

Sebagai tambahan kepada jadual berasaskan retainer berkala, Operasi Projek boleh merekodkan lebih awal sekali daripada pelanggan dan menyelaraskannya dengan perbezaan komponen kos projek.

Retainer dalam Operasi Projek tidak tersedia untuk digunakan sehingga ia diinvoiskan kepada pelanggan. Ini ditunjukkan oleh medan berikut pada subgrid untuk pendahuluan dan retainer.

| Medan | Keterkaitan, tujuan dan panduan | Kesan hiliran |
| --- | --- | --- |
| Amaun Tersedia | Jumlah yang tersedia untuk digunakan pada rekod retainer atau pendahuluan. | Sehingga pendahuluan atau retainer diinvoiskan, ia tidak tersedia untuk digunakan yang bermaksud jumlah yang tersedia adalah sifar. |
| Amaun Digunakan | Jumlah yang sudah digunakan pada rekod retainer atau pendahuluan. | Pendahuluan atau retainer boleh diselaraskan sebahagian pada invois dengan kos sebenar yang akan mempunyai beberapa bahagian yang ditanda sebagai sudah digunakan atau habis. Jumlah baki pendahuluan atau retainer tersedia untuk diselaraskan pada invois masa hadapan dengan kos sebenar. |
