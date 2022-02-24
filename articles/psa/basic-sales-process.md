---
title: Proses jualan
description: Topik ini menyediakan maklumat mengenai proses jualan asas.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145189"
---
# <a name="sales-processes"></a>Proses jualan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proses jualan yang digunakan dalam organisasi berasaskan projek berbeza daripada proses jualan yang digunakan dalam organisasi berasaskan produk. Perbezaan ini berlaku kerana kitaran jualan untuk organisasi berasaskan projek lebih lama dan memerlukan teknik anggaran tersuai untuk menganalisis dan mencipta sebut harga untuk setiap urusan. Dynamics 365 Project Service Automation menggunakan beberapa fungsi sama yang digunakan dalam proses jualan untuk Dynamics 365 Sales. Berikut adalah beberapa contoh:

- Sebuah entiti Bakal Pelanggan digunakan untuk menjejaki proses jualan.
- Bakal pelanggan yang layak dijejak sebagai peluang. Proses jualan juga boleh bermula dengan peluang.
- Semua artifak berkaitan untuk peluang dicapai. Artifak ini termasuk pasukan jualan, pemegang kepentingan, kebarangkalian, penarafan, peringkat jualan dan proses perniagaan.
- Sebut harga berbilang dicipta untuk peluang.
- Sebut harga ditanda **Tutup sebagai Menang** untuk mencipta pesanan jualan. Dalam PSA, pesanan jualan disesuaikan dan dipanggil kontrak projek.

Ilustrasi berikut menunjukkan proses jualan biasa dalam organisasi berasaskan projek.

> ![Proses jualan dalam organisasi berasaskan projek](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Menganggarkan jualan
Nilai jualan boleh dianggarkan berdasarkan projek yang sebelum ini diserahkan dan kerumitan projek. Untuk projek yang melibatkan sambungan kepada projek sebelumnya, atau projek di mana kepakaran penjual adalah template kerja yang tinggi dan terkenal digunakan, anda boleh menggunakan proses anggaran yang lebih mudah. Projek yang lebih rumit biasanya mempunyai proses pembelian yang lebih panjang. Oleh itu, terdapat lebih banyak peringkat dalam proses anggaran jualan. Pada awal proses, pasukan jualan menggunakan input pengurus akaun dan pakar perkara subjek (PKS) untuk mula mewujudkan anggaran tahap tinggi bagi setiap komponen kerja yang jelas yang dipetik. Komponen kerja ini diwakili oleh baris sebut harga. 

Anda boleh mencipta anggaran tahap tinggi sebut harga. Akhirnya, anggaran tahap tinggi akan digantikan dengan anggaran yang lebih terperinci berdasarkan pelan projek yang anda cipta dengan menggunakan templat projek yang diseragamkan. Templat ini membantu anda membina jadual dan menentukan nilai kewangan pada sebut harga dan komponennya (baris sebut harga). 

Anda boleh mencipta sebut harga berbilang untuk projek dan kumpulkan mereka di bawah jenis entiti peluang. Akhirnya, salah satu daripada sebut harga ditanda **Ditutup sebagai Menang** dan kontrak projek atau pernyataan kerja (SOW) dicipta. Kontrak projek memegang nilai kontrak untuk setiap komponen (baris kontrak) yang diterima oleh pelanggan untuk penghantaran. SOW biasanya dicipta sebagai dokumen Microsoft Word. Semua invois yang dihantar kepada pelanggan melalui rujukan penghantaran projek kontrak projek atau SOW.

Anda juga boleh mencipta sebut harga alternatif di bawah satu jenis entiti peluang atau menyediakan sistem supaya kontrak projek dicipta apabila sebut harga dimenangi. Dalam kes ini, anda boleh melampirkan dokumen Word yang mewakili SOW kepada rekod kontrak projek.

![Menutup sebut harga untuk mencipta kontrak projek](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Mengkonfigurasikan proses jualan
Anda boleh menggunakan aliran proses perniagaan (BPFs) pada Microsoft Dynamics 365 untuk mengkonfigurasi proses jualan anda. BPFs memberikan pekerja jualan anda antara muka visual dipandu yang mereka boleh gunakan untuk menggerakkan transaksi ke hadapan melalui peringkat yang tipikal untuk syarikat anda.

Sebagai contoh, syarikat anda mungkin mempunyai enam peringkat berikut dalam proses jualan:

1. Layakkan
2. Anggarkan
3. Semakan dalama
4. Kontrak
5. Hantar
6. Tutup

Enam peringkat ini diwakili oleh chevrons (\>) yang anda pilih untuk mengembangkan dalam setiap jenis entiti peluang yang anda cipta.

![Konfigurasi proses perniagaan dalam Dynamics 365](media/basic-guide-3.png)
 
Organisasi anda mungkin menggunakan entiti berbeza untuk mewakili urusan yang sama semasa ia berkembang. Pada awal proses jualan, urusan diwakili oleh entiti Peluang. Apabila masa berlalu dan butiran lanjut muncul, anda mungkin menggunakan anggaran peringkat tinggi untuk mencipta satu atau lebih sebut harga. Jika salah satu daripada sebut harga ini disemak oleh pemegang amanah pelanggan dan dalaman, entiti Sebut Harga mewakili urusan. Selepas pelanggan menerima sebut harga, kontrak projek atau SOW mewakili perjanjian tersebut. Untuk menyokong tingkah laku ini, BPFs berstruktur supaya setiap peringkat dalam proses dihubungkan kepada jadual pangkalan data yang berbeza.

Peringkat **Kelayakan** dalam proses jualan boleh disokong oleh entiti Peluang. Peringkat **Anggaran** dan **Semakan Dalaman** boleh disokong oleh entiti Sebut Harga. Peringkat **Kontrak**, **Penghantaran** dan **Tutup** boleh disokong oleh entiti Kontrak Projek.

Apabila anda memindahkan transaksi melalui peringkat, anda akan digesa untuk mencipta rekod entiti yang sesuai untuk membantu dan membimbing anda melalui proses. Peringkat boleh bersyarat. Contohnya, jika anda memerlukan semakan dalaman sebut harga hanya jika sebut harga menggunakan senarai harga tersuai, anda boleh mengkonfigurasi keadaan tersebut dalam peringkat proses perniagaan yang sesuai. Peringkat **Semakan Dalaman** kemudian ditunjukkan hanya untuk sebut harga yang menggunakan senarai harga tersuai. Untuk semua tawaran dan sebut harga lain, peringkat **Anggaran** diikuti oleh peringkat **Kontrak**.

> [!NOTE]
> PSA mempunyai halaman khusus untuk entiti Peluang, Sebut Harga, Pesanan dan Invois. Anda mesti mencipta peluang perkhidmatan projek, sebut harga, pesanan dan invois menggunakan halaman maklumat projek untuk entiti tersebut. Jika anda menggunakan halaman lain untuk mencipta rekod, anda tidak akan dapat membuka rekod daripada halaman **Maklumat Projek**. Jika anda mahu membuka rekod daripada halaman **Maklumat Projek**, anda mesti memadamkan rekod dan menciptanya semula menggunakan halaman **Maklumat Projek**. Pada halaman **Maklumat Projek**, logik perniagaan untuk setiap jenis entiti ini memastikan medan **Jenis** rekod ditetapkan dengan betul, dan semua konsep mandatori telah dimulakan dengan betul.

> ![Maklumat projek untuk arahan baharu](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Perbezaan antara Project Service Automation dan Jualan
Walaupun proses jualan dalam PSA menggunakan keupayaan asas untuk proses jualan dalam Jualan, ia mempunyai beberapa perbezaan utama kerana variasi dalam amalan perniagaan organisasi berasaskan projek. Berikut adalah beberapa contoh:

- **Sebut harga projek** – dalam Project Service Automation, sebut harga ditutup selepas kontrak projek dicipta daripada sebut harga. Dalam Jualan, anda boleh menyimpan sebut harga terbuka selepas anda memenanginya. Sebab perbezaan ini ialah padanan antara sebut harga dan kontrak projek adalah lebih baik untuk organisasi berasaskan projek. 
- **Pengaktifan dan semakan** – Dalam PSA, pengaktifan dan semakan tidak disokong untuk sebut harga projek. Dalam Jualan, sebut harga boleh dikunci untuk mengelakkan edit tambahan.
- **Menutup sebut harga sebagai kalah atau menang** – Dalam PSA, apabila projek sebut harga ditutup sebagai menang atau kalah, peluang kekal terbuka. Semua sebut harga lain pada peluang ditutup sebagai kalah. Dalam Jualan, apabila sebut harga ditutup sebagai menang atau kalah, pengguna digesa untuk mengambil tindakan ke atas peluang tersebut. Bergantung pada input pengguna, peluang asas mungkin ditutup atau dibiarkan terbuka.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Menjejaki semakan kepada sebut harga dan rancangan projek dalam kitaran jualan
Dalam PSA, anda tidak boleh menjejaki semakan yang dibuat kepada sebut harga. Sebaliknya, anda mesti menandakan sebut harga **Tutup sebagai Kalah** dan kemudian mencipta sebut harga baharu. Anda boleh menyalin sebut harga atau klon sebut harga berasaskan projek dengan menggunakan PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Menjejaki komen dan kelulusan daripada sebut harga dan kontrak projek
Anda boleh mengurus semakan dan kelulusan sebut harga dan kontrak projek dengan menggunakan dinding rekod dan siaran. Organisasi anda boleh mencipta aliran kerja tersuai dan pasang masuk untuk menugaskan, mengubah hala, memuncak dan mengurus pemberitahuan semakan dan item kerja kelulusan.
