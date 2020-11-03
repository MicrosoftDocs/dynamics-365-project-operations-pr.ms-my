---
title: Menyalin kontrak projek
description: Topik ini menyediakan maklumat tentang menyalin kontrak projek dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081133"
---
# <a name="copying-project-contracts"></a>Menyalin kontrak projek

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Anda boleh secara mudah mencipta kontrak projek baharu dengan membuat salinan kontrak sedia ada dalam salah satu daripada dua cara: 

  - Pada halaman senarai **Kontrak Projek** , pilih kontrak projek dan kemudian pilih **Salin**.
  - Pada halaman butiran **Kontrak projek** , pilih **Salin**.

Halaman dialog akan membuka lokasi yang anda boleh pilih parameter bagi kontrak yang disalinkan. Medan berikut disertakan pada dialog. Bergantung pada nilai yang anda pilih dalam dialog ini, proses penyalinan mungkin berubah.

| **Medan** | **Keterkaitan, tujuan dan panduan** | **Kesan hiliran** |
| --- | --- | --- |
| Topik | Masukkan topik kontrak sasaran. Apabila halaman dialog dibuka, sistem akan menetapkan medan ini ke nama kontrak sumber dengan **-salin** ditambahkan kepadanya. | Tiada kesan hiliran untuk medan ini. |
| Pelanggan | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila dialog dibuka, sistem akan menetapkan medan ini ke akaun pada kontrak sumber. | Medan ini adalah pelanggan utama pada kontrak. |
| Unit Pengkontrakan | Unit Organisasi yang bertanggungjawab untuk penghantaran projek berkaitan dengan urusan ini. Apabila halaman dialog dibuka, sistem akan menetapkannya ke unit kontrak bagi kontrak sumber. | Unit kontrak adalah bahagian syarikat yang akan melaksanakan projek selepas urusan ditutup. Setiap unit kontrak mempunyai mata wang. Mata wang ini digunakan untuk melaporkan kos anggaran dan aktual yang dikenakan semasa projek. |
| Mata wang | Mata wang dalam urusan yang ditransaksikan. Apabila halaman dialog dibuka, sistem akan menetapkan medan ke mata wang bagi kontrak sumber. Mata wang tidak boleh ditukar. Jika ya, medan **Salin Penetapan Harga** sentiasa ditetapkan ke **Tidak** kerana senarai harga pada kontrak sumber tidak lagi relevan. | Mata wang digunakan untuk senarai harga lalai, untuk membina anggaran kewangan pada kontrak dan untuk penginvoisan pelanggan apabila urusan menang. |
| Tarikh Penghantaran Diminta | Tarikh penghantaran diminta oleh pelanggan. | Tarikh digunakan sebagai tarikh akhir apabila anda mencipta tarikh penginvoisan sepanjang kekerapan tertentu. |
| Salin penetapan harga | Menunjukkan sama ada penetapan harga pada kontrak hendaklah disalin daripada kontrak sumber. | Jika medan ditetapkan ke **Ya** , rujukan senarai harga projek dan produk disalin daripada sumber ke kontrak sasaran. Jika **Tidak** dipilih, senarai harga lalai berdasarkan pada senarai harga terkini pada parameter akaun atau projek. |

Apabila anda memilih **OK** pada halaman dialog, sistem mencipta salinan kontrak berasaskan pada parameter yang dipilih. Kontrak baharu akan dibuka.

Maklumat berikut tidak disalin daripada **Sumber** ke **Kontrak Sasaran** :

  - Jadual invois
  - Pelanggan kontrak dan baris kontrak
  - Rujukan projek pada baris kontrak berasaskan projek
  - Maklumat belanjawan pelanggan

Oleh kerana maklumat ini sangat khusus untuk setiap kontrak, medan dan rekod ini tidak disalin. Baris kontrak untuk projek dan produk, anggaran pada butiran baris kontrak dan nilai tidak boleh melebihi pada peringkat kontrak disalin. Kadar harga dan kos lalai bergantung pada pilihan dalam medan **Salin penetapan harga** pada halaman dialog **Salin parameter**.
