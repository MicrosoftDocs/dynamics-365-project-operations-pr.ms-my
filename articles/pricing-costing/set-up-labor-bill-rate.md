---
title: Sediakan kadar bil buruh
description: Topik ini memberikan maklumat tentang cara untuk menetapkan kadar pengebilan buruh dalam Operasi Projek.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0fee2c98713f4d1f8da85a0b60fb3fc2a873e5f82a64cf350ebeb68fe65fab35
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003557"
---
# <a name="set-up-labor-bill-rates"></a>Sediakan kadar bil buruh

_ **Gunakan Pada:** Operasi Projek untuk senario berasaskan sumber/bukan stok

Setiap senarai harga mempunyai set harga peranan atau kadar buruh yang efektif untuk konteks dan tarikh kuat kuasa disertakan pada pengepala senarai harga. Kadar bil untuk masa dalam Dynamics 365 Project Operations boleh disediakan dalam hanya satu mata wang, iaitu mata wang pada pengepala senarai Harga.

1. Bagi menyediakan kadar bil buruh untuk senarai harga jualan, pergi ke **Jualan** > **Pelanggan** > **Senarai Harga** dan pilih **Baharu** untuk mencipta senarai harga baharu. 
2. Pada tab **Harga Peranan**, dalam subgrid, pilih **Harga Peranan Baharu**. 
3. Pada anak tetingkap **Cipta Pantas**, masukkan peranan dan gabungan unit organisasi yang anda perlukan untuk menyediakan kadar bil.

   Jadual berikut merangkumi medan pada tab **Umum** dan anak tetingkap **Cipta Pantas** bagi baris harga peranan yang perlu diingati apabila anda mencipta harga peranan pada senarai harga jualan.

    | Medan | Lokasi | Penerangan | Kesan hiliran |
    | --- | --- | --- | --- |
    | Peranan | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Pilih peranan yang anda tetapkan untuk kadar bil. | Peranan pada anggaran atau sebenar yang masuk akan dipadankan dengan baris ini untuk menetapkan kadar bil peranan lalai. |
    | Syarikat Penyumberan | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Pilih syarikat atau entiti sah yang peranan ini berasal. Sebagai contoh, pemaju dari Fabrikam India atau pemaju dari Fabrikam USA. | Syarikat sumber pada anggaran atau sebenar yang masuk akan dipadankan dengan baris ini untuk menetapkan kadar bil peranan lalai. |
    | Unit Sumber | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Pilih unit organisasi atau divisyen syarikat yang peranan ini berasal. Sebagai contoh, pemaju dari bahagian Robotik Fabrikam India atau pemaju dari bahagian Perisian Fabrikam USA. | Unit sumber pada anggaran atau sebenar yang masuk akan dipadankan dengan baris ini untuk menetapkan kadar bil peranan lalai. |
    | Harga | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Sediakan kadar bil untuk peranan, syarikat sumber dan gabungan unit sumber. Contohnya, pemaju daripada Fabrikam India mempunyai kadar bil 100 USD atau pemaju daripada Fabrikam USA mempunyai kadar bil 150 USD. | Harga ini merupakan kadar bil lalai pada harga setiap unit bagi baris anggaran atau sebenar yang masuk untuk kelas transaksi Masa. |
    | Mata wang | Tab **Umum** dan anak tetingkap **Cipta Pantas**| Secara lalai, nilai mata wang diperoleh daripada mata wang pada pengepala senarai harga jualan. Pada senarai harga jualan, mata wang tidak boleh ditulis ganti. | Mata wang ini ialah mata wang lalai pada harga setiap unit bagi baris jualan sebenar yang masuk untuk kelas transaksi Masa. |
    | Jadual Unit | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Jadual unit ini lalai kepada Masa dan tidak boleh ditukar pada entiti harga Peranan kerana ia digunakan untuk menyatakan kadar mengikut unit masa. | Tiada kesan hiliran untuk medan ini. |
    | Unit | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Nilai unit diperoleh daripada medan **Unit Masa** pada pengepala senarai harga jualan. Tetapi nilai boleh ditulis ganti. Contohnya, pemaju daripada Fabrikam India mempunyai kadar bil 1000 USD setiap **Hari India**. Pemaju daripada Fabrikam USA mempunyai kadar bil untuk 1500 USD setiap **Hari AS**. | Apabila harga setiap unit lalai pada baris anggaran atau sebenar yang masuk, sistem ini menggunakan sistem unit dan penukaran dalam unit asas untuk mengira harga setiap unit. Contohnya, anggaran untuk 10 **Hari India**, nilai kerja untuk Pemaju dari India dan unit Hari India ditakrifkan sebagai 10 jam. Semasa penetapan harga garisan anggaran, aplikasi mengira harga unit pada anggaran 1000 USD/10 jam = 100 USD setiap jam. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Pindahkan harga atau sediakan kadar bil untuk sumber daripada unit atau divisyen organisasi yang lain 

Syarikat berasaskan projek sering menggunakan pekerja daripada entiti sah yang berbeza dan divisyen yang berbeza dalam entiti sah untuk bekerja dalam projek. Projek boleh dilaksanakan daripada entiti sah atau divisyen tertentu sementara pekerja atau perunding yang bekerja dalam projek tersebut boleh berasal daripada entiti sah dan divisyen yang sama atau daripada yang lain. Projek ini juga boleh terdiri daripada gabungan individu daripada entiti sah dan divisyen yang berbeza. Dalam Operasi Projek, entiti sah yang memiliki penyerahan projek dipanggil **Syarikat Pemilik** dan divisyen yang memiliki penghantaran dipanggil **Unit Kontrak**. Semua Entiti sah lain yang menyediakan sumber dipanggil **Syarikat Sumber** dan divisyen yang menyediakan sumber dipanggil **Unit Sumber**. Oleh kerana perbezaan dalam kos buruh merentasi pelbagai geografi dan pasaran buruh di seluruh dunia, kadar bil untuk buruh juga ditetapkan secara berbeza bagi geografi yang berbeza.

Contohnya, pemaju daripada divisyen Robotik Fabrikam India yang bekerja untuk projek AS dibilkan pada kadar 100 USD setiap jam. Pemaju daripada divisyen Robotik Fabrikam AS yang bekerja untuk Projek AS dibilkan pada 150 USD setiap sejam. 

### <a name="example-set-up-a-bill-rate"></a>Contoh: sediakan kadar bil 

1. Cipta senarai harga jualan yang dipanggil *Kadar Bil Fabrikam AS* dan tetapkan tarikh kuat kuasa.
2. Dalam senarai harga jualan, masukkan maklumat kadar berikut:

    | Peranan | Syarikat persumberan | Unit persumberan | Kadar bil |
    | --- | --- | --- | --- |
    | Pemaju | Fabrikam India | Fabrikam India - Robotik | $100 |
    | Pemaju | Fabrikam Filipina | Fabrikam Filipina - Robotik | $90 |
    | Pemaju | Fabrikam AS | Fabrikam AS - Robotik | $150 |

3. Lampirkan senarai harga jualan, **Kadar Bil Fabrikam AS** kepada senarai harga projek bagi kontrak projek atau kepada akaun tertentu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
