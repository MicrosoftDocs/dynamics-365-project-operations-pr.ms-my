---
title: Salin sebut harga berasaskan projek
description: Topik ini menyediakan maklumat tentang cara menyalin sebut harga berasaskan projek dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081105"
---
# <a name="copy-project-based-quotes"></a>Salin sebut harga berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Anda dengan mudah boleh mencipta sebut harga Projek baharu dengan menyalin yang sedia ada. 

- Untuk menyalin sebut harga Projek, pada halaman senarai **Sebut Harga Projek** atau halaman butiran **Sebut Harga Projek** , pilih sebut harga Projek yang anda mahu salin dan kemudian pilih **Salin**.

Ini akan membuka halaman dialog yang anda boleh memasukkan parameter bagi salinan. Jadual berikut menyenaraikan medan yang disertakan dalam halaman dialog. Bergantung pada nilai yang anda pilih, proses penyalinan mungkin berubah.

| **Medan** | **Keterkaitan, tujuan dan panduan** | **Kesan hiliran** |
| --- | --- | --- |
| Topik | Masukkan topik atau nama yang berkaitan dengan sebut harga sasaran. Apabila dialog dibuka, sistem akan menetapkannya kepada topik sebut harga sumber dengan **-salin** ditambahkan padanya. | |
| Pelanggan Berpotensi | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila dialog dibuka, sistem akan menetapkannya kepada akaun pada sebut harga sumber. | Medan ini ialah pelanggan utama pada sebut harga. |
| Unit Pengkontrakan | Unit organisasi yang bertanggungjawab untuk penghantaran projek yang berkaitan dengan urusan ini.
Apabila dialog dibuka, sistem akan menetapkannya kepada unit kontrak sebut harga sumber. | Unit kontrak adalah divisyen syarikat yang akan melaksanakan projek selepas urusan ditutup. Setiap unit kontrak mempunyai mata wang. Mata wang digunakan untuk melaporkan kos dianggar dan sebenar yang ditanggung semasa pelaksanaan projek. |
| Mata wang | Ini adalah mata wang urusan yang ditransaksikan . Apabila dialog dibuka, sistem akan menetapkannya kepada mata wang sebut harga sumber. Ini boleh diubah suai dan jika ianya berubah, medan **Salin Penetapan Harga** sentiasa ditetapkan ke **Tidak**. Ini adalah kerana senarai harga pada sebut harga sumber tidak lagi relevan. | Mata wang digunakan untuk melalaikan senarai harga bagi membina anggaran kewangan pada sebut harga dan akhirnya kepada invois pelanggan apabila perjanjian dimenangi. |
| Tarikh Penghantaran Diminta | Ini adalah tarikh penghantaran yang diminta oleh pelanggan. | Ini digunakan sebagai tarikh akhir apabila mencipta tarikh penginvoisan sepanjang kekerapan tertentu. |
| Salin penetapan harga | Nilai Ya/Tidak menunjukkan sama ada penetapan harga pada sebut harga perlu disalin daripada sebut harga sumber. | Jika **Ya** dipilih, rujukan senarai harga projek dan senarai harga produk disalin daripada sebut harga sumber kepada sebut harga sasaran. Jika **Tidak** dipilih, senarai harga akan dilalaikan semula berdasarkan pada senarai harga terkini yang ditetapkan pada parameter akaun atau projek. |

Apabila anda memilih **OK** pada halaman dialog, sistem mencipta salinan sebut harga projek berasaskan pada parameter yang dipilih dalam dialog. Sebut harga projek baharu dibuka. 

> [!NOTE]
> Maklumat berikut tidak disalin daripada sebut harga Sumber ke Sasaran:
>
> - Jadual invois
> - Sebut harga dan sebut harga baris pelanggan
> - Rujukan projek dalam projek – berasaskan maklumat belanjawan baris sebut harga -Pelanggan
>
>Oleh kerana maklumat ini sangat khusus untuk setiap sebut harga, medan dan rekod ini tidak disalin. Baris sebut harga untuk projek dan produk, anggaran butiran baris sebut harga dan nilai tidak melebihi pada peringkat sebut harga disalin. Kadar harga dan kos lalai bergantung pada pilihan **Salin penetapan harga** yang dipilih pada halaman dialog **Salin parameter**.
