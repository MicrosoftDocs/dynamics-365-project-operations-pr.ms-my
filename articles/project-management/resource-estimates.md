---
title: Anggaran kewangan untuk masa sumber pada projek
description: Topik ini menyediakan maklumat tentang cara anggaran kewangan untuk masa dikira.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010797"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Anggaran kewangan untuk masa sumber pada projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anggaran kewangan untuk masa dikira berdasarkan tiga faktor: 

- Jenis ahli pasukan generik atau bernama yang ditugaskan kepada setiap tugas nod daun pada pelan projek. 
- Jenis atau kerumitan kerja.
- Penyebaran usaha untuk tugasan sumber pada tugas. 

Dua faktor pertama mempengaruhi kos unit atau kadar bil tugasan sumber. Kos unit atau kadar bil tugasan sumber ditentukan oleh atribut sumber yang ditugaskan. Atribut ini termasuk unit organisasi yang dimiliki oleh sumber dan peranan standard sumber. Anda juga boleh menambah atribut tersuai yang berkaitan dengan perniagaan anda untuk sumber, seperti tajuk standard atau tahap pengalaman serta mempengaruhi kos unit atau kadar bil tugasan.
Sebagai tambahan kepada atribut sumber, atribut kerja, seperti tugas, juga boleh mempengaruhi kadar bil unit atau kadar kos tugasan. Contohnya, apabila tugasan tertentu lebih kompleks, tugasan sumber kepada tugas tertentu tersebut menyebabkan kos unit atau kadar bil lebih tinggi daripada tugas yang kurang kompleks.   

Faktor ketiga menyediakan kuantiti jam pada kadar tersebut. Dalam keadaan yang mana tugasan meliputi dua tempoh harga, kemungkinan bahagian pertama tugasan sumber untuk tugas itu mempunyai kos dan harga yang berbeza daripada bahagian kedua tugas. Anggaran usaha ke atas setiap tugasan sumber ialah nilai kompleks yang disimpan dengan pengagihan harian bagi usaha setiap hari.

Untuk arahan terperinci tentang cara menyediakan atribut tersuai kerja dan sumber sebagai dimensi penetapan harga dan kos, lihat [Gambaran keseluruhan Dimensi Penetapan Harga](../pricing-costing/pricing-dimensions-overview.md).

Anggaran kewangan bagi setiap tugasan sumber dikira sebagai **kadar/j untuk tugasan didarabkan dengan bilangan jam.**  Sama seperti anggaran usaha, anggaran kewangan untuk kos dan hasil bagi setiap tugasan sumber ialah nilai kompleks yang disimpan dengan pengagihan harian amaun kewangan setiap hari. 

## <a name="summarizing-financial-estimates-for-time"></a>Meringkaskan anggaran kewangan untuk masa
Anggaran kewangan untuk masa pada tugas nod daun ialah jumlah anggaran kewangan pada semua tugasan sumber untuk tugas itu.

Anggaran kewangan untuk masa pada tugas ringkasan atau induk ialah jumlah anggaran kewangan pada semua tugas anaknya. Ini ialah kos buruh yang dianggarkan pada projek. 

![Anggaran Sumber](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Harga kos dan mata wang kos lalai

Harga kos lalai diambil daripada senarai harga yang dilampirkan pada unit kontrak projek. Mata wang kos projek sentiasa mata wang unit kontrak projek. Pada tugasan sumber, anggaran kewangan untuk kos disimpan dalam mata wang kos projek. Kadangkala, mata wang kadar kos yang ditetapkan dalam senarai harga berbeza daripada mata wang kos projek. Dalam keadaan ini, aplikasi menukar mata wang harga kos yang ditetapkan untuk mata wang projek. Pada grid **Anggaran**, semua anggaran kos dipaparkan dan diringkaskan dalam mata wang kos projek. 

## <a name="default-bill-rate-and-sales-currency"></a>Kadar bil dan mata wang jualan lalai

Harga jualan lalai diambil daripada senarai harga projek yang dilampirkan pada kontrak projek yang berkaitan jika urusan itu dimenangi, atau daripada sebut harga projek yang berkaitan jika urusan itu masih dalam peringkat prajualan. Mata wang jualan projek sentiasa mata wang bagi sebut harga projek atau kontrak projek. Pada tugasan sumber, anggaran kewangan untuk jualan disimpan dalam mata wang jualan projek. Tidak seperti kos, harga jualan yang ditetapkan dalam senarai harga tidak boleh berbeza daripada mata wang jualan projek. Tiada senario yang penukaran mata wang diperlukan. Pada grid **Anggaran**, semua anggaran jualan dipaparkan dan diringkaskan dalam mata wang jualan projek. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
