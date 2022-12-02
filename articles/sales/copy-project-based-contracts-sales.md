---
title: Salin kontrak berasaskan projek
description: Artikel ini memberikan maklumat tentang penyalinan kontrak projek dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410375"
---
# <a name="copy-project-based-contracts"></a>Salin kontrak berasaskan projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Anda boleh mencipta kontrak projek baharu secara mudah dengan menyalin kontrak sedia ada dalam salah satu daripada dua cara:

- Pada halaman senarai **Kontrak Projek**, pilih kontrak projek dan kemudian pilih **Salin**.
- Pada halaman butiran **Kontrak projek**, pilih **Salin**.

Dalam kedua-dua kes, kotak dialog akan muncul dan anda boleh menetapkan parameter bagi kontrak yang disalin. Kotak dialog merangkumi medan berikut. Bergantung pada nilai yang anda pilih, proses salin mungkin berubah.

| Medan | Description | Kesan hiliran |
| --- | --- | --- |
| Topik | Masukkan topik kontrak sasaran. Apabila kotak dialog dibuka, sistem menetapkan medan kepada nama kontrak sumber, tetapi perkataan "salin" ditambahkan kepadanya. | Tiada kesan hiliran untuk medan ini. |
| Dihormati | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila kotak dialog dibuka, sistem menetapkan medan kepada akaun pada kontrak sumber. | Medan ini adalah pelanggan utama pada kontrak. |
| Syarikat Pemilikan | Syarikat yang bertanggungjawab untuk penghantaran projek yang berkaitan dengan urusan ini. Apabila kotak dialog dibuka, sistem menetapkan medan kepada syarikat pemilikan kontrak sumber. | Syarikat pemilikan ialah entiti sah yang akan melaksanakan projek selepas urusan ditutup. Mata wang syarikat pemilikan mestilah sepadan dengan mata wang unit kontrak. |
| Unit Pengkontrakan | Unit organisasi yang bertanggungjawab untuk penghantaran projek yang berkaitan dengan urusan ini. Apabila kotak dialog dibuka, sistem menetapkan medan kepada unit kontrak bagi kontrak sumber. | Unit kontrak adalah bahagian syarikat yang akan melaksanakan projek selepas urusan ditutup. Setiap unit kontrak mempunyai mata wang. Mata wang ini digunakan untuk melaporkan kos anggaran dan aktual yang dikenakan semasa projek. |
| Mata Wang | Mata wang dalam urusan yang ditransaksikan. Apabila kotak dialog dibuka, sistem menetapkan medan kepada mata wang bagi kontrak sumber. Mata wang tidak boleh ditukar. Jika ya, medan **Salin Harga** sentiasa ditetapkan kepada **Tidak** kerana senarai harga pada kontrak sumber tidak lagi relevan. | Mata wang ini digunakan untuk senarai harga lalai, untuk menjana anggaran kewangan pada kontrak dan untuk menginvois pelanggan apabila urusan dimenangi. |
| Tarikh Penyampaian Diminta | Tarikh penghantaran yang diminta oleh pelanggan. | Tarikh digunakan sebagai tarikh akhir apabila anda mencipta tarikh penginvoisan pada kekerapan tertentu. |
| Salin penetapan harga | Nilai yang menunjukkan sama ada harga pada kontrak harus disalin daripada kontrak sumber. | Jika medan ditetapkan kepada **Ya**, rujukan senarai harga projek dan produk disalin daripada kontrak sumber kepada kontrak sasaran. Jika ditetapkan kepada **Tidak**, senarai harga lalai digunakan, berdasarkan pada senarai harga terkini dalam parameter akaun atau projek. |

Apabila anda memilih **OK** dalam kotak dialog, sistem mencipta salinan kontrak, berdasarkan nilai parameter yang anda tetapkan. Kemudian kontrak baharu akan dibuka.

Maklumat berikut **tidak** disalin daripada kontrak sumber kepada kontrak sasaran kerana ia khusus untuk setiap kontrak:

- Jadual invois
- Pelanggan kontrak dan baris kontrak
- Rujukan projek pada baris kontrak berasaskan projek
- Maklumat belanjawan pelanggan

Baris kontrak untuk projek dan produk, anggaran dalam butiran baris kontrak dan nilai tidak boleh dilebihi pada peringkat kontrak disalin. Entri kadar harga dan kos lalai bergantung pada pilihan dalam medan **Salin harga** dalam kotak dialog **Salin Parameter**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
