---
title: Sediakan kadar kos buruh - ringan
description: Topik ini menyediakan maklumat mengenai cara untuk menetapkan kadar kos untuk dalam buruh Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6b1265e5e4d29ccc3f620da364fc9554285a176
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274379"
---
# <a name="set-up-labor-cost-rates---lite"></a>Sediakan kadar kos buruh - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Setiap senarai harga mempunyai set kadar buruh (harga peranan) yang selaras dengan kandungan dan tarikh keberkesanan untuk senarai harga.

1. Cipta senarai harga dan pada tab **Harga Peranan**, dalam subgrid, pilih **Peranan Baharu**.
2. Pada halaman **Cipta Pantas**, pilih peranan dan unit organisasi.
3. Masukkan maklumat medan lain yang diperlukan.

Jadual berikut termasuk beberapa medan yang penting apabila mencipta kadar buruh pada senarai harga kos.

| Medan | Lokasi | Penerangan  | Kesan hiliran |
| --- | --- | --- | --- |
| Peranan | Tab **Umum** dan halaman **Cipta Pantas** | Pilih peranan yang tertakluk kepada kadar kos tersebut. | Peranan pada anggaran masuk atau sebenar akan dipadankan dengan baris ini untuk memberi nilai lalai kos peranan. |
| Unit Sumber | Tab **Umum** dan halaman **Cipta Pantas** | Pilih unit organisasi atau bahagian syarikat yang peranan ini akan digunakan. Sebagai contoh, pemaju dari bahagian Robotik Fabrikam India atau pemaju dari bahagian Perisian Fabrikam USA. | Unit penyumberan pada anggaran masuk atau sebenar akan dipadankan dengan baris ini untuk memberi nilai lalai kos peranan. |
| Harga | Tab **Umum** dan halaman **Cipta Pantas** | Sediakan kadar kos untuk peranan, syarikat penyumberan dan kombinasi unit penyumberan. Sebagai contoh, kos pemaju dari Fabrikam India adalah INR 1000 atau kos pemaju dari Fabrikam USA adalah USD 150. | Harganya adalah kadar kos lalai pada kos setiap unit bagi anggaran masuk atau baris sebenar untuk kelas transaksi **Masa**. |
| Mata wang | Tab **Umum** dan halaman **Cipta Pantas** | Secara lalai, nilai mata wang datang dari mata wang pada pengepala senarai harga kos tetapi boleh diganti. Sebagai contoh, kos pemaju daripada Fabrikam India berharga adalah INR 1000. Kos pemaju daripada Fabrikam USA adalah USD 150. | Mata wang ini lalai pada setiap unit kos bagi anggaran masuk baris sebenar untuk kelas transaksi **Masa**. Pada anggaran projek, nilai mata wang ditukar kepada mata wang projek dan ditunjukkan pada pandangan fasa Masa untuk anggaran tersebut. |
| Jadual Unit | Tab **Umum** dan halaman **Cipta Pantas** | Unit jadual lalai ke Masa dan tidak boleh ditukar pada entiti harga Peranan kerana kadar ekspres mengikut unit masa digunakan. | Tiada kesan kepada fungsi hiliran. |
| Unit | Tab **Umum** dan halaman **Cipta Pantas** | Secara lalai, nilai datang dari medan **Unit Masa** pada pengepala senarai harga kos. Nilai boleh diganti. Sebagai contoh, kos pemaju daripada Fabrikam India adalah INR 1000 setiap **Hari India**. Kos pemaju daripada Fabrikam USA adalah USD 150 setiap **Hari India**. | Sistem ini menggunakan sistem unit dan penukaran unit asas untuk mengira kos seunit untuk mengira harga lalai setiap unit pada anggaran masuk atau baris sebenar. Sebagai contoh, anggaran adalah untuk 10 **Hari India** bekerja untuk pemaju dari India dan unit, **Hari India** ditakrifkan sebagai 10 jam. Apabila pengiraan yang menganggar baris, aplikasi mengira kos unit pada anggaran sebagai: INR 1000/10 jam = INR 100 sejam yang ditukar kepada USD dan ditunjukkan sebagai kos unit pada halaman **Anggaran Projek**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Pindahan penetapan harga dan kos untuk sumber di luar bahagian anda atau entiti sah

Dalam syarikat berasaskan projek, adalah perkara biasa untuk menggunakan pekerja daripada entiti atau bahagian yang berbeza pada projek. Projek boleh dilaksanakan oleh satu entiti sah, tetapi pekerja atau perunding yang bekerja pada projek boleh datang daripada entiti sah yang sama atau daripada yang lain atau kemungkinan kombinasi kedua-duanya. Dalam Dynamics 365 Project Operations, entiti undang-undang yang memiliki penyampaian projek ialag **Syarikat Pemilik** dan bahagian yang memiliki penghantaran ialah **Unit Kontrak**. Entiti sah lain yang menyediakan sumber adalah **Syarikat penyumberan** dan bahagian yang menyediakan sumber ialah **Unit Penyumberan**. Di kebanyakan negara, syarikat dikehendaki memastikan bahawa sumber entiti atau bahagian sah, mengecaj syarikat pemilikan dan unit kontrak untuk penggunaan sumber.

Sebagai contoh, perbadanan Fabrikam mesti memastikan Fabrikam India-Robotics telah berunding kos kad kadar dengan Fabrikam US-Robotics atau Fabrikam UK-Robotics.

Pemaju daripada Fabrikam India-Robotic mengenakan caj $100 apabila dipinjamkan kepada Fabrikam US-Robotics dan $150 apabila dipinjamkan kepada Fabrikam UK-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Sediakan kos untuk sumber luar

1. Cipta senarai harga kos yang dipanggil, *kadar kos Fabrikam US-Robotics* dan menetapkan julat efektif tarikh.
2. Dalam senarai harga kos, tetapkan kadar dengan menggunakan maklumat daripada jadual berikut. 

| Peranan | Syarikat Penyumberan | Unit Sumber | Kadar kos |
| --- | --- | --- | --- |
| Pemaju | Fabrikam India | Fabrikam India-Robotics | $100 |
| Pemaju | Fabrikam Filipina | Fabrikam Philippines-Robotics | $90 |
| Pemaju | Fabrikam US | Fabrikam US-Robotics | $150 |

3. Lampirkan senarai harga kos ini kepada unit organisasi Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Sediakan pemindahan penetapan harga untuk sumber dalam mata wang yang sesuai 

Dalam Project Operations, penetapan harga sumber boleh ditetapkan dalam sebarang mata wang. Mata wang lalai kepada nilai yang ada pada pengepala senarai harga, tetapi boleh ditukar.

Menggunakan contoh untuk persediaan harga pemindahan, maklumat boleh ditukar kepada:

Perbadanan Fabrikam mesti memastikan Fabrikam India-Robotics telah berunding kos kadar dengan Fabrikam US-Robotics atau Fabrikam UK-Robotics.

Pemaju daripada Fabrikam India-Robotics mengenakan caj INR 5000 apabila dipinjamkan kepada Fabrikam US-Robotics dan INR 5500 apabila dipinjamkan kepada Fabrikam UK-Robotics.

Dalam senarai harga kos untuk Fabrikam US-Robotics, kadar kos boleh dinyatakan sebagai:

| Peranan | Syarikat Penyumberan | Kos |
| --- | --- | --- |
| Pemaju | Fabrikam India | INR 5000 |
| Pemaju | Fabrikam US | 115 USD |

Dalam senarai harga kos untuk Fabrikam UK-Robotics, kadar kos boleh dinyatakan berikut:

| Peranan | Syarikat persumberan | Kos |
| --- | --- | --- |
| Pemaju | Fabrikam India | INR 5500 |
| Pemaju | Fabrikam UK | 115 GBP |

Senarai harga kos boleh memberikan kadar buruh dalam berbilang mata wang. Apabila menjana anggaran kos pada projek, Project Operations akan menukar kadar kos ini ke dalam mata wang projek dan memaparkannya kepada pengguna. Apabila kemasukan masa telah diluluskan dan kos sebenar dicipta, kos sebenar dinilai dalam mata wang bagi peranan sepadan baris harga pada senarai harga kos. Kos sebenar untuk masa pada satu projek boleh direkodkan dalam berbilang mata wang. Walau bagaimanapun, apabila mengira atau meringkaskan kos buruh sebenar pada peringkat projek, Project Operations akan menukar semua kos buruh ke dalam mata wang projek yang pengguna boleh lihat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]