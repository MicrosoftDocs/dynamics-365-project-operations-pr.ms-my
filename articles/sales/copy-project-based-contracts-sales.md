---
title: Salin kontrak berasaskan projek
description: Artikel ini menyediakan maklumat tentang menyalin kontrak projek dalam Microsoft Dynamics 365 Project Operations.
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

Anda boleh membuat kontrak projek baru dengan mudah dengan menyalin kontrak sedia ada dengan salah satu daripada dua cara:

- **Pada halaman senarai Kontrak** Projek, pilih kontrak projek, kemudian pilih **Salin**.
- Pada halaman butiran **Kontrak projek**, pilih **Salin**.

Dalam kedua-dua kes, kotak dialog muncul, di mana anda boleh menetapkan parameter kontrak yang disalin. Kotak dialog termasuk medan berikut. Bergantung pada nilai yang anda pilih, proses salin mungkin berubah.

| Medan | Description | Kesan hiliran |
| --- | --- | --- |
| Topik | Masukkan topik kontrak sasaran. Apabila kotak dialog dibuka, sistem menetapkan medan kepada nama kontrak sumber, tetapi perkataan "salin" ditambah kepadanya. | Tiada kesan hiliran untuk medan ini. |
| Dihormati | Rujukan kepada syarikat atau rekod akaun pelanggan. Apabila kotak dialog dibuka, sistem mengesetkan medan kepada akaun pada kontrak sumber. | Medan ini adalah pelanggan utama pada kontrak. |
| Syarikat Pemilikan | Syarikat yang bertanggungjawab untuk menyampaikan projek-projek yang berkaitan dengan perjanjian ini. Apabila kotak dialog dibuka, sistem menetapkan medan kepada syarikat pemilik kontrak sumber. | Syarikat milik adalah entiti undang-undang yang akan melaksanakan projek itu selepas perjanjian ditutup. Mata wang syarikat yang memiliki mesti sepadan dengan mata wang unit kontrak. |
| Unit Pengkontrakan | Unit organisasi yang bertanggungjawab untuk menyampaikan projek-projek yang berkaitan dengan perjanjian ini. Apabila kotak dialog dibuka, sistem mengesetkan medan kepada unit kontrak kontrak sumber. | Unit kontrak adalah bahagian syarikat yang akan melaksanakan projek selepas urusan ditutup. Setiap unit kontrak mempunyai mata wang. Mata wang ini digunakan untuk melaporkan anggaran dan kos sebenar yang ditanggung semasa projek. |
| Mata Wang | Mata wang dalam urusan yang ditransaksikan. Apabila kotak dialog dibuka, sistem mengesetkan medan kepada mata wang kontrak sumber. Mata wang tidak boleh ditukar. Sekiranya demikian, **medan Salin Harga** sentiasa ditetapkan kepada **Tidak**, kerana senarai harga pada kontrak sumber tidak lagi relevan. | Mata wang ini digunakan untuk senarai harga lalai, untuk menjana anggaran kewangan pada kontrak, dan untuk menginvois pelanggan apabila perjanjian itu dimenangi. |
| Tarikh Penyampaian Diminta | Tarikh penghantaran yang diminta oleh pelanggan. | Tarikh ini digunakan sebagai tarikh tamat apabila anda mencipta tarikh invois pada kekerapan tertentu. |
| Salin penetapan harga | Nilai yang menunjukkan sama ada harga pada kontrak harus disalin dari kontrak sumber. | Jika medan disetkan kepada **Ya**, rujukan senarai harga projek dan produk disalin daripada kontrak sumber kepada kontrak sasaran. Jika ia ditetapkan kepada **Tidak**, senarai harga lalai digunakan, berdasarkan senarai harga terkini dalam akaun atau parameter projek. |

Apabila anda memilih **OK** dalam kotak dialog, sistem mencipta salinan kontrak, berdasarkan nilai parameter yang anda setkan. Kemudian kontrak baru dibuka.

Maklumat berikut tidak **disalin** dari kontrak sumber ke kontrak sasaran, kerana ia khusus untuk setiap kontrak:

- Jadual invois
- Pelanggan kontrak dan baris kontrak
- Rujukan projek pada baris kontrak berasaskan projek
- Maklumat belanjawan pelanggan

Talian kontrak untuk projek dan produk, anggaran dalam butiran baris kontrak, dan nilai tidak melebihi di peringkat kontrak disalin. Kemasukan harga lalai dan kadar kos bergantung pada pemilihan dalam **medan Salin harga** dalam kotak **dialog Salin Parameter**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
