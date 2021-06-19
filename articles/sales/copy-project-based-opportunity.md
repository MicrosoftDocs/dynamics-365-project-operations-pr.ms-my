---
title: Salin peluang berasaskan projek
description: Topik ini menyediakan maklumat tentang penyalinan peluang berasaskan projek dalam Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae724d18e768b838f388b6fd089bfa657c937da1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013452"
---
# <a name="copy-project-based-opportunities"></a>Salin peluang berasaskan projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Peluang projek boleh disalin dengan mudah untuk mencipta peluang projek baharu. 

1. Pergi ke halaman senarai **Peluang Projek** dan pilih peluang daripada senarai. Atau buka halaman butiran peluang tertentu. 
2. Daripada mana-mana halaman, pilih **Salin**. Halaman dialog akan membuka yang mengandungi maklumat medan berikut. Bergantung pada nilai yang dipilih dalam dialog ini, proses penyalinan mungkin berubah.

    | **Medan** | **Perihalan** | **Kesan hiliran** |
    | --- | --- | --- |
    | Topik | Masukkan topik yang berkaitan peluang sasaran. Apabila dialog dibuka, sistem akan menetapkannya ke topik peluang sumber dengan **-salin** ditambahkan kepadanya. | Tiada kesan hiliran untuk medan ini. |
    | Akaun | Merujuk syarikat atau rekod akaun pelanggan. Apabila dialog dibuka, sistem akan menetapkannya ke akaun pada peluang sumber. | Medan ini adalah pelanggan utama pada peluang. |
    | Unit Pengkontrakan | Unit organisasi yang bertanggungjawab untuk penghantaran projek berkaitan dengan urusan ini. Apabila dialog dibuka, sistem akan menetapkannya kepada unit kontrak peluang sumber. | Unit kontrak adalah divisyen syarikat yang melaksanakan projek selepas urusan ditutup. Setiap unit pengkontrakan mempunyai mata wang dan mata wang ini digunakan untuk melaporkan kos anggaran dan sebenar yang berlaku semasa projek. |
    | Mata wang | Mata wang dalam urusan yang ditransaksikan. Apabila dialog dibuka, sistem akan menetapkannya ke mata wang peluang sumber. | Mata wang digunakan untuk melalaikan senarai harga dan membina anggaran kewangan pada sebut harga. Akhirnya mata wang digunakan untuk menginvois pelanggan apabila perjanjian itu menang. |
    | Salin penetapan harga | Nilai Ya/Tidak yang menunjukkan jika penetapan harga pada peluang sepatutnya disalin daripada peluang sumber. | Jika **Ya** dipilih, senarai harga disalin daripada sumber ke peluang sasaran. Jika **Tidak** dipilih, senarai harga akan dilalaikan berdasarkan pada senarai harga terkini yang ditetapkan. |

3. Pilih **OK**. Sistem mencipta salinan peluang projek berasaskan parameter yang dipilih dan peluang projek baharu dibuka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]