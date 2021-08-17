---
title: Cipta projek baharu
description: Topik ini memberikan maklumat tentang cara untuk mencipta projek baharu.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5aa5e00252697f91a585eaaa83a0c8a39b315cc1b25fcbf6343fdf2ce31a824e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985962"
---
# <a name="create-a-new-project"></a>Cipta projek baharu

[!include [banner](../includes/banner.md)]

Lengkapkan langkah berikut untuk mencipta projek baharu.

1. Pada halaman **Pengurusan projek**, pilih **Projek baharu**, dan masukkan nilai berikut:

    - **Jenis projek:** Masa dan bahan
    - **Nama projek:** Naik taraf XYZ Fasa 2
    - **Kumpulan projek:** TM\_WIP
    - **ID kontrak projek:** 00000002

2. Pilih **Cipta projek**.

## <a name="assign-a-resource-to-a-project"></a>Tugaskan sumber kepada projek

1. Pada halaman **Pekerja**, dalam senarai **Pekerja**, pilih rekod untuk pekerja yang sebelum ini anda sediakan kecekapan, dan buka rekod pekerja.
2. Pada Anak Tetingkap Tindakan, pada tab **Projek**, dalam kumpulan **Persediaan**, pilih **Tugaskan projek**.
3. Pada halaman **Tugasan projek pengesahan sumber**, pada tab **Projek**, dalam medan **Tambah projek ke projek dipilih**, tapis pada projek **Naik taraf XYZ Fasa 2**.
4. Dalam anak tetingkap **Baki projek**, pilih projek, dan kemudian pilih butang anak panah untuk menambahnya ke anak tetingkap **Projek dipilih**.

Anda juga boleh tugaskan kategori untuk sumber yang anda perlukan. Jenis kategori ialah sama ada **Kos** atau **Hasil**. Jenis kategori adalah ditentukan oleh organisasi anda. Jika tiada kategori ditugaskan untuk sumber, Kewangan mencari kategori lalai pada harga jam bagi kos dan hasil.

## <a name="set-up-project-resource-and-role-characteristics"></a>Sediakan sumber projek dan ciri peranan

Pengurus projek boleh menggunakan kefungsian penyumberan projek untuk mencipta peranan yang diperlukan untuk projek. Peranan boleh digunakan jika sumber yang disahkan masih tidak diketahui apabila sumber diperuntukkan. Peranan boleh diperuntukkan sementara sebagai sumber yang dirancang, supaya anda boleh meneruskan peringkat perancangan projek.

[![Contoh peranan.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senario:** Contoso diupah untuk melengkapkan projek Masa dan bahan yang mempunyai piagam projek yang diluluskan. Pengurus projek muda masih melengkapkan skop projek. Resource manager pada masa ini sedang mengenal pasti sumber tertentu yang akan diperuntukkan untuk bekerja pada projek baharu. Oleh kerana sifat kritikal projek itu, penaja projek meminta Pengurus projek kanan sebagai salah satu peranan. Resource manager mesti mendapatkan sumber baharu dan mentakrifkan peranan dalam sistem sekiranya pengurus projek muda memerlukan maklumat sumber semasa perancangan projek.

Langkah berikut menunjukkan cara resource manager boleh menyediakan peranan Pengurus projek kanan dan kaitkan ciri sumber dengannya. Kemudian, peranan boleh digunakan untuk carian sumber tersedia yang sepadan dengan kecekapan sumber yang diperlukan.

1. Pada halaman **Peranan persediaan**, pilih **Baharu**, dan masukkan nilai berikut:

    - **ID peranan:** Pengurus Projek Kanan
    - **Perihalan** Pengurus Projek Kanan

2. Pilih **Cipta**.
3. Pilih peranan **Pengurus Projek Kanan**, dan kemudian pilih **Ciri konfigurasi**.
4. Dalam medan **Jenis ciri**, pilih **Kemahiran**.
5. Dalam medan **Ciri tersedia**, masukkan kemahiran untuk carian.
6. Dalam medan **Jenis ciri**, pilih **Sijil**.
7. Dalam medan **Ciri tersedia**, masukkan jenis sijil untuk carian.

## <a name="assign-a-project-resource-to-a-project"></a>Tugaskan sumber projek kepada projek

1. Pada halaman **Semua projek**, pilih projek **Naik taraf XYZ Fasa 2**.
2. Pada tab **Pasukan projek dan penjadualan**, pilih **Tambah**.
3. Dalam medan **Peranan**, pilih **Ahli pasukan**.
4. Pilih **Tempah daripada kalendar**.
5. Pada halaman **Ketersediaan sumber**, pilih **Pandangan tetapan**.
6. Pada halaman **Laraskan pandangan tetapan**, masukkan nilai berikut:

    - **Format untuk tarikh pandangan julat:** Hari
    - **Paparan perihalan ketersediaan:** Ya
    - **Paparan kapasiti baki:** Ya

7. Dalam senarai sumber, pilih sumber.
8. Pilih **Tempah Keras** dan **Kapasiti penuh**.

## <a name="assign-a-resource-to-a-default-role"></a>Tugaskan sumber kepada peranan lalai

Untuk membantu projek atau pengurus projek boleh gerudi bawah lebih lanjut tentang sumber yang boleh diperuntukkan untuk projek. Anda boleh kaitkan peranan lalai dengan sumber sedia ada atau sumber yang baharu diperolehi. Contohnya, apabila Daniel diupah, beliau mempunyai pengalaman dan kemahiran untuk mengisi peranan Penganalisis perniagaan. Resource manager ditugaskan peranan ini sebagai peranan lalai Daniel. Oleh itu, resource manager menambah Daniel kepada himpunan penganalisa perniagaan yang bersedia untuk mengerjakan projek.

Semasa tempahan sumber, pengurus projek boleh menapis sumber peranan yang tersedia untuk mengerjakan projek. Mereka boleh menggunakan maklumat ini sebagai satu kriteria apabila mereka melaksanakan analisis keputusan berbilang kriteria semasa pemenuhan sumber. Mereka juga boleh menambah ciri sumber lain kepada penapis untuk carian sumber yang mempunyai kemahiran, pendidikan, dan pengalaman khusus untuk projek yang diberikan.

**Senario:** Projek yang diluluskan telah dimulakan, dan peranan Pengurus projek kanan telah diperuntukkan sebagai sumber yang dirancang semasa peringkat perancangan projek. Resource manager kini telah memperolehi sumber untuk memenuhi peranan Pengurus projek kanan.

1. Pada halaman **Senarai sumber**, pilih **Daniel Goldschmidt**.
2. Pada halaman **Peranan sumber**, pilih **Baharu**, dan masukkan nilai berikut:

    - **Berkuat kuasa:** Masukkan tarikh semasa.
    - **Tamat tempoh:** Masukkan **Jangan sekali-kali**.
    - **Peranan:** Masukkan **Pengurus Projek Kanan**.

3. Pilih **Simpan**, dan kemudian tutup halaman.
4. Pada tab **Kecekapan**, tambah kemahiran **ProjectMgmt** dan sijil **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]