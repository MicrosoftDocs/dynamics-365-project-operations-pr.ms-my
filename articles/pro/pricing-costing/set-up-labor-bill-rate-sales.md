---
title: Sediakan kadar bil buruh - ringan
description: Artikel ini menyediakan maklumat mengenai cara untuk menetapkan kadar pengebilan buruh dalam Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 443132797f20c961b42ed20340e74f420965526f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917449"
---
# <a name="set-up-labor-bill-rates---lite"></a>Sediakan kadar bil buruh - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Setiap senarai harga mempunyai set harga peranan atau kadar buruh yang efektif untuk konteks dan tarikh kuat kuasa disertakan pada pengepala senarai harga. Kadar bil untuk masa dalam Dynamics 365 Project Operations boleh disediakan dalam hanya satu mata wang, iaitu mata wang pada pengepala senarai Harga.

1. Untuk menyediakan kadar bil buruh bagi senarai harga jualan, cipta senarai harga berdasarkan pengepala senarai harga. 
2. Pada tab **Harga Peranan**, dalam sub grid, pilih **+ Harga Peranan Baharu**. 
3. Pada anak tetingkap **Cipta Pantas**, masukkan peranan dan gabungan unit organisasi yang anda perlukan untuk menyediakan kadar bil.

  Jadual berikut merangkumi medan pada tab **Umum** dan anak tetingkap **Cipta Pantas** bagi baris harga peranan yang perlu diingati apabila anda mencipta harga peranan pada senarai harga jualan.

  | Medan | Lokasi | Penerangan | Kesan hiliran |
  | --- | --- | --- | --- |
  | Peranan | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Pilih peranan yang anda tetapkan untuk kadar bil. | Peranan pada anggaran atau sebenar yang masuk akan dipadankan dengan baris ini untuk menetapkan kadar bil peranan lalai. |
  | Unit Sumber | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Pilih unit organisasi atau divisyen syarikat yang peranan ini berasal. Sebagai contoh, pemaju dari bahagian Robotik Fabrikam India atau pemaju dari bahagian Perisian Fabrikam USA. | Unit sumber pada anggaran atau sebenar yang masuk akan dipadankan dengan baris ini untuk menetapkan kadar bil peranan lalai. |
  | Harga | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Sediakan kadar bil untuk peranan, syarikat sumber dan gabungan unit sumber. Contohnya, pemaju daripada Fabrikam India mempunyai kadar bil 100 USD atau pemaju daripada Fabrikam USA mempunyai kadar bil 150 USD. | Harga ini merupakan kadar bil lalai pada harga setiap unit bagi baris anggaran atau sebenar yang masuk untuk kelas transaksi Masa. |
  | Mata wang | Tab **Umum** dan anak tetingkap **Cipta Pantas**| Secara lalai, nilai mata wang diperoleh daripada mata wang pada pengepala senarai harga jualan. Pada senarai harga jualan, mata wang tidak boleh ditulis ganti. | Mata wang ini ialah mata wang lalai pada harga setiap unit bagi baris jualan sebenar yang masuk untuk kelas transaksi Masa. |
  | Jadual Unit | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Jadual unit ini lalai kepada Masa dan tidak boleh ditukar pada entiti harga Peranan kerana ia digunakan untuk menyatakan kadar mengikut unit masa. | Tiada kesan hiliran untuk medan ini. |
  | Unit | Tab **Umum** dan anak tetingkap **Cipta Pantas** | Nilai unit diperoleh daripada medan **Unit Masa** pada pengepala senarai harga jualan. Tetapi nilai boleh ditulis ganti. Contohnya, pemaju daripada Fabrikam India mempunyai kadar bil 1000 USD setiap **Hari India**. Pemaju daripada Fabrikam USA mempunyai kadar bil untuk 1500 USD setiap **Hari AS**. | Apabila harga setiap unit lalai pada baris anggaran atau sebenar yang masuk, sistem ini menggunakan sistem unit dan penukaran dalam unit asas untuk mengira harga setiap unit. Contohnya, anggaran untuk 10 **Hari India**, nilai kerja untuk Pemaju dari India dan unit Hari India ditakrifkan sebagai 10 jam. Semasa penetapan harga garisan anggaran, aplikasi mengira harga unit pada anggaran 1000 USD/10 jam = 100 USD setiap jam. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Pindahkan harga atau sediakan kadar bil untuk sumber daripada unit atau divisyen organisasi yang lain 

Syarikat berasaskan projek menggunakan pekerja daripada divisyen yang berbeza untuk bekerja pada projek. Projek boleh dilaksanakan dari satu divisyen semasa pekerja atau perunding datang dari divisyen berbeza bagi syarikat yang sama. Projek ini juga boleh terdiri daripada gabungan orang dari divisyen yang berbeza. Dalam Project Operations, syarikat yang memiliki penyerahan projek tersebut dipanggil **Unit Kontrak**. Semua divisyen lain yang menyediakan sumber dipanggil **Unit Penyumberan**. Oleh kerana perbezaan dalam kos buruh merentasi pelbagai geografi dan pasaran buruh di seluruh dunia, kadar bil untuk buruh juga ditetapkan secara berbeza bagi geografi yang berbeza.

Sebagai contoh, pemaju daripada Fabrikam India yang bekerja pada projek AS dibilkan pada kadar USD 100 sejam. Pemaju daripada Fabrikam US bekerja pada Projek AS dibilkan pada USD 150 sejam.

### <a name="example-set-up-a-bill-rate"></a>Contoh: sediakan kadar bil

1. Cipta senarai harga jualan yang dipanggil *Kadar Bil Fabrikam US* dan tetapkan penguatkuasaan tarikh.
2. Dalam senarai harga jualan, masukkan maklumat kadar berikut:

    | Peranan | Unit organisasi | Kadar bil |
    | --- | --- | --- |
    | Pemaju | Fabrikam India | $100 |
    | Pemaju | Fabrikam Philippines | $90 |
    | Pemaju | Fabrikam US | $150 |

3. Lampirkan senarai harga jualan, **Kadar Bil Fabrikam US** kepada senarai harga projek kontrak projek atau kepada akaun tertentu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]