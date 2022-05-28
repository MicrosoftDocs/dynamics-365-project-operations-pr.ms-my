---
title: Bekerja dengan model data Project Service Automation
description: Topik ini memberikan maklumat tentang cara untuk bekerja dengan model data.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e0849e5b2ab144814fe5310b11a758475ef56ef5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587551"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Bekerja dengan model data Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Dynamics 365 Project Service Automation melangkaui entiti aplikasi lain dan memperkenalkan entiti sendiri dalam model data Common Data Service. Topik ini menerangkan beberapa entiti yang akan anda hadapi dalam senario pelaporan PSA biasa.

## <a name="reporting-on-opportunities"></a>Pelaporan berkenaan peluang

Project Service Automation melanjutkan entiti **Peluang** Dynamics 365 Sales dengan menambah medan yang mendayakan senario berasaskan projek. Medan ini dikenal pasti oleh nama skema dengan awalan **msdyn.\_**. Satu medan baharu yang penting untuk pelaporan berkenaan peluang PSA ialah **Jenis Pesanan**. Nilai **Berdasarkan Kerja** untuk medan ini menunjukkan yang peluang tersebut ialah peluang PSA. Medan lain yang telah ditambah pada entiti tersebut termasuk **Organisasi Kontrak**, yang merekodkan organisasi yang memegang peluang tersebut dan **Pengurus Akaun**, yang merekodkan nama pengurus akaun yang bertanggungjawab bagi peluang tersebut.

Entiti **Baris Peluang** juga termasuk medan yang berkaitan dengan Project Service. **Kaedah Pengebilan** menunjukkan sama ada baris peluang harus dibilkan berdasarkan masa dan bahan atau berdasarkan harga tetap, dan **Projek** merekodkan nama projek yang menyokong peluang tersebut. Medan lain yang boleh anda laporkan merekodkan jumlah kos dan belanjawan pelanggan untuk item baris.

## <a name="reporting-on-quotes"></a>Pelaporan berkenaan sebut harga

PSA melanjutkan entiti **Sebut Harga** Jualan dengan menambah medan berkaitan projek. **Jenis Pesanan** membezakan sebut harga PSA daripada sebut harga bukan PSA. Nilai **Berdasarkan Kerja** untuk medan ini menunjukkan yang sebut harga tersebut ialah sebut harga PSA. Medan lain yang mungkin berkaitan dengan laporan berkenaan sebut harga PSA termasuk medan jumlah, seperti **Kos Boleh Dituntut**, **Kos Tidak Boleh Dituntut**, **Margin Kasar**, **Anggaran** dan **Belanjawan**. Lain-lain medan berguna menunjukkan sama ada sebut harga menguntungkan, sama ada ia akan diselesaikan mengikut jadual dan sama ada ia memenuhi jangkaan belanjawan pelanggan.

PSA juga melanjutkan entiti **Baris Sebut Harga** Jualan. Satu medan yang PSA tambah ialah **Kaedah Pengebilan**, yang menunjukkan cara baris sebut harga akan dibilkan (masa dan bahan atau harga tetap). Medan lain yang telah ditambah pada entiti merekodkan projek berkaitan yang menyokong baris sebut harga, invois, kos dan bajet.

PSA juga menambah entiti berkaitan sebut harga baharu kepada model data Dynamics 365. Berikut adalah beberapa contoh:

- **Butiran Baris Sebut Harga** – Entiti ini mengandungi butiran anggaran projek bagi baris sebut harga. Ia mempunyai dua rekod bagi setiap baris sebut harga. Salah satu rekod menyimpan kos dan butiran kos baris sebut harga dan rekod lain menyimpan jumlah jualan dan butiran jualan baris sebut harga.
- **Jadual Invois Baris Sebut Harga** – Entiti ini mengandungi jadual pengebilan untuk baris sebut harga. Jadual ini dijana berdasarkan kekerapan penginvoisan yang ditugaskan ke baris sebut harga.
- **Pencapaian Baris Sebut Harga** – Entiti ini mengandungi pencapaian pengebilan untuk baris sebut harga tetap.
- **Pecahan Analisis Baris Sebut Harga** – Entiti ini mengandungi butiran kewangan bagi baris sebut harga. Butiran ini boleh berguna untuk melaporkan jualan sebut harga dan anggaran jumlah kos oleh pelbagai dimensi.

Entiti lain yang PSA tambah kepada sebut harga ialah **Senarai Projek Baris Sebut Harga**, **Kategori Sumber Baris Sebut Harga** dan **Kategori Transaksi Baris Sebut Harga**.

![Rajah menunjukkan sebut harga, baris sebut harga dan perhubungan projek.](media/PS-Reporting-image2.png "Gambarajah menunjukkan sebut harga, baris sebut harga dan perhubungan projek")

## <a name="reporting-on-project-contracts"></a>Pelaporan berkenaan kontrak projek

PSA melanjutkan entiti **Pesanan** Jualan yang digunakan apabila kontrak projek direkodkan. Ia menambah medan baharu yang penting, **Jenis Pesanan**, yang mengenal pasti kontrak sebagai kontrak projek PSA bukan pesanan jualan. Nilai **Berdasarkan Kerja** untuk medan ini menunjukkan yang pesanan tersebut ialah kontrak projek PSA. Medan baharu lain yang ditambahkan pada entiti **Pesanan** merekodkan butiran tentang kos, status kontrak PSA dan organisasi yang memiliki kontrak tersebut.

PSA juga melanjutkan entiti **Baris Pesanan Jualan**. Antara medan yang ditambah ialah medan yang merekodkan kaedah pengebilan (masa dan bahan atau harga tetap), jumlah belanjawan pelanggan, dan projek dasar.

PSA juga menambah entiti baharu yang direka bentuk untuk kontrak projek. Berikut adalah beberapa contoh:

- **Butiran Baris Kontrak Projek** – Entiti ini mengandungi butiran peringkat baris yang dikumpulkan pada jumlah baris kontrak. Ini boleh jadi begitu terperinci seperti item baris yang dijana daripada jadual projek pada peringkat tugas.
- **Jadual Invois Baris Kontrak** – Entiti ini mengandungi jadual pengebilan yang dijana berdasarkan kekerapan invois yang ditugaskan kepada baris kontrak.
- **Pencapaian Kontrak** – Entiti ini mengandungi pencapaian pengebilan untuk baris kontrak yang mempunyai tempoh pengebilan harga tetap.

Entiti lain yang PSA tambah kepada kontrak ialah **Senarai Harga Projek Baris Kontrak Projek**, **Kategori Sumber Baris Kontrak Projek** dan **Kategori Transaksi Baris Kontrak Projek**.

![Rajah menunjukkan pesanan, baris pesanan dan perhubungan projek.](media/PS-Reporting-image3.png "Gambarajah menunjukkan pesanan, baris pesanan dan perhubungan projek")

## <a name="reporting-on-projects"></a>Pelaporan berkenaan projek

Entiti **Projek** dan entiti berkaitannya adalah eksklusif untuk PSA. **Projek** ialah entiti peringkat tinggi yang digunakan untuk merekodkan kerja dan bahagian kos operasi. Berikut ialah senarai entiti berkaitan:

- **Ahli pasukan projek** – Entiti ini mengandungi butiran tentang sumber boleh ditempah yang ditugaskan kepada projek tersebut. Sumber tersebut boleh menjadi sumber boleh ditempah yang generik atau ia boleh menjadi sumber boleh ditempah yang dinamakan yang dimasukkan oleh pengurus projek atau dijana daripada jadual projek.
- **Tugas Projek** – Entiti ini mengandungi tugas yang membentuk pelan atau jadual projek.
- **Penugasan Sumber** – Entiti ini mengandungi penugasan tugas untuk sumber boleh ditempah.
- **Keperluan Sumber** – Entiti ini mengandungi keperluan untuk sebarang ahli pasukan sumber generik.
- **Anggaran** dan **Baris anggaran** – Entiti ini mempunyai perhubungan pengepala/baris dan mengandungi anggaran perbelanjaan untuk projek. Anggaran tugas disimpan pada entiti **Anggaran Sumber**.

![Rajah menunjukkan keperluan sumber dan perhubungan projek.](media/PS-Reporting-image4.png "Gambarajah menunjukkan keperluan sumber dan perhubungan projek")

## <a name="reporting-on-resources"></a>Pelaporan berkenaan sumber

Sumber projek menggunakan entiti **Sumber Boleh Ditempah** daripada Universal Resource Scheduling (URS) yang dikongsi dengan aplikasi lain, seperti Microsoft Dynamics 365 Field Service. Berikut ialah senarai entiti yang anda mungkin perlu gunakan apabila anda melaporkan tentang sumber projek:

- **Sumber Boleh Ditempah** – Entiti ini mewakili pengguna, kenalan, sumber generik, akaun, kumpulan atau peralatan yang digunakan pada pasukan projek.
- **Ciri Sumber Boleh Ditempah** – Entiti ini termasuk kemahiran, persijilan atau pendidikan sumber. Ciri boleh mempunyai nilai penarafan yang ditakrifkan oleh model penarafan.
- **Kategori Sumber Boleh Ditempah** – Entiti ini mewakili peranan sumber boleh ditempah.
- **Penempahan sumber boleh ditempah** – Entiti ini mewakili masa yang ditempah pada projek untuk sumber tersebut. Setiap tempahan mempunyai entiti pengepala dan entiti baris, dan setiap baris mempunyai status yang mewakili status tempahan.

![Rajah menunjukkan perhubungan ciri sumber boleh ditempah.](media/PS-Reporting-image5.png "Gambarajah menunjukkan perhubungan ciri sumber boleh ditempah")

## <a name="reporting-on-actual-transactions"></a>Pelaporan berkenaan transaksi sebenar

Apabila anda meluluskan satu lembar masa atau perbelanjaan, atau menginvoiskan kontrak dalam PSA, transaksi perniagaan direkodkan dalam entiti **Aktual**. Entiti ini boleh berfungsi sebagai asas bagi hampir semua laporan berkaitan kewangan dalam PSA. Entiti **Aktual** merekodkan transaksi kos dan jualan bagi peristiwa perniagaan. Ia juga merekodkan banyak atribut yang berkaitan.

Apabila anda bekerja dengan entiti **Aktual**, adalah penting anda untuk memahami transaksi atau transaksi-transaksi yang direkodkan dalam entiti dan masa transaksi direkodkan. Berikut ialah aliran biasa apabila anda bekerja dengan entri masa (aliran untuk entri perbelanjaan adalah serupa):

1. Apabila entri masa disimpan, tiada rekod dicipta dalam entiti **Aktual**.
2. Apabila entri masa diserahkan, tiada rekod dicipta dalam entiti **Aktual**.
3. Apabila entri diluluskan, satu rekod akan dicipta dalam entiti **Aktual** dan rekod kedua juga boleh dicipta. Rekod pertama menyimpan kos bagi entri masa. Rekod kedua menyimpan jumlah jualan belum dibilkan bagi entri masa. Rekod kedua bergantung pada projek sama ada mempunyai pelanggan, sebut harga atau baris kontrak yang ditugaskan padanya.

    | Tarikh dokumen | Jenis transaksi | Kelas transaksi | Pelanggan         | Kontrak   | Sumber     | Peranan sumber | Jenis pengebilan | Kuantiti | Harga unit | Amaun |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Kos             | Time              | Alpine Ski House | Alpine CRM | Rokiah Awang | Pengurus Projek   | Boleh dituntut   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Jualan belum dibilkan   | Time              | Alpine Ski House | Alpine CRM | Rokiah Awang | Pengurus Projek   | Boleh dituntut   | 8.0      | 100.00     | 800.00 |

    Kedua-dua rekod ini berasingan tetapi rekod yang berkaitan. Ia bukan debit mahupun kredit.

4. Jika satu kontrak dikaitkan dengan projek, apabila entri masa diinvoiskan, dua lagi rekod dicipta dalam entiti **Aktual**. Pertama, jumlah negatif untuk rekod jualan belum dibilkan dicipta. Rekod ini secara dasarnya menterbalikkan jualan yang belum dibilkan. Kedua, satu transaksi untuk jualan yang dibilkan dicipta. Sekali lagi, rekod ini berasingan tetapi rekod yang berkaitan, bukan debit dan kredit.

    | Tarikh dokumen | Jenis transaksi | Kelas transaksi | Pelanggan         | Kontrak   | Sumber     | Peranan sumber | Jenis pengebilan | Kuantiti | Harga unit | Amaun   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Jualan belum dibilkan   | Time              | Alpine Ski House | Alpine CRM | Rokiah Awang | Pengurus Projek   | Boleh dituntut   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Jualan dibilkan     | Time              | Alpine Ski House | Alpine CRM | Rokiah Awang | Pengurus Projek   | Boleh dituntut   | 8.0      | 100.00     | 800.00   |

Entiti **Asal Transaksi** merekodkan asal rekod **Aktual** dan entiti **Sambungan Transaksi** merekodkan rekod yang berkaitan bagi rekod **Aktual**. Selain itu, rekod **Aktual** mengandungi rujukan projek, kontrak projek (pesanan), sumber boleh ditempah dan pelanggan.

![Rajah menunjukkan sambungan transaksi, asal dan perhubungan aktual.](media/PS-Reporting-image6.png "Gambarajah menunjukkan sambungan transaksi, asal dan perhubungan sebenar")


[!INCLUDE[footer-include](../includes/footer-banner.md)]
