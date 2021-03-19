---
title: Sediakan sumber projek
description: Topik ini memberikan maklumat tentang menyediakan atau memohon sumber projek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288750"
---
# <a name="set-up-project-resources"></a>Sediakan sumber projek

[!include [banner](../includes/banner.md)]

Anda mesti menyediakan kalendar dan kaitkannya dengan pekerja atau pekerja. Kalendar digunakan untuk menjadualkan projek dan masa kerja sumber yang diperuntukkan untuk projek. Semasa persediaan kalendar, pengurus projek boleh lakukan pelarasan sumber sebagai sebahagian daripada pengoptimuman sumber. Berdasarkan jadual kalendar, sekatan boleh diletakkan pada sumber. Anda boleh menyediakan kalendar pada halaman **Kalendar**.

Apabila anda menyediakan pekerja sebagai sumber projek, anda boleh memilih daripada pekerja yang bekerja dalam syarikat tempat anda menyediakan sumber. Secara alternatif, anda boleh memilih pekerja daripada syarikat lain dalam organisasi anda. Pekerja ini dikenali sebagai sumber antara syarikat.

Prosedur berikut menerangkan cara untuk menyediakan pekerja sebagai sumber projek dalam syarikat anda dan cara untuk menyediakan sumber projek antara syarikat.

## <a name="set-up-a-worker-as-a-project-resource"></a>Sediakan pekerja sebagai sumber projek

1. Pada halaman **Pekerja**, dalam senarai **Pekerja**, pilih pekerja yang anda tambah sebagai sumber projek dan buka rekod pekerja.
2. Pada Anak Tetingkap Tindakan, pilih **Projek** &gt; **Persediaan** &gt; **Persediaan projek**.
3. Pilih kalendar, dan kemudian tutup halaman.

Anda juga boleh menentukan projek lalai untuk sumber sebagai jenis pra-tugasan. Pra-tugasan boleh digunakan apabila pengurus sumber atau pengurus projek mengetahui projek sumber yang mana akan berjalan terlebih dahulu. Pra-tugasan juga boleh berdasarkan kepada permintaan penaja projek atau pelanggan. Untuk membuat pra-tugaskan projek, pada halaman **Tugaskan projek**, pada tab **Projek**, dalam senarai **Baki projek**, pilih projek yang sesuai.

## <a name="set-up-an-intercompany-resource"></a>Sediakan sumber antara syarikat

Apabila anda menyediakan pekerja sebagai sumber antara syarikat, anda mesti melengkapkan persediaan dalam kedua-dua syarikat pinjaman dan syarikat peminjaman.

### <a name="in-the-lending-company"></a>Dalam syarikat pinjaman

1. Dalam Kewangan, sahkan bahawa syarikat pinjaman dipilih, dan kemudian lengkapkan prosedur dalam bahagian sebelumnya, "Sediakan pekerja sebagai sumber projek."
2. Pada halaman **Perakaunan antara syarikat**, pilih **Baharu**.
3. Dalam medan **ID entiti undang-undang**, pilih syarikat pinjaman. Isikan medan yang selebihnya mengikut kesesuaian, dan kemudian pilih **Simpan**.
4. Pada halaman **Pemindahan harga**, pilih **Baharu**.
5. Dalam medan **Entiti undang-undang peminjaman**, pilih syarikat yang sesuai.
6. Untuk meminjamkan syarikat peminjaman hanya sumber yang anda cipta pada permulaan bahagian ini, dalam medan **Sumber**, pilih nama sumber yang anda cipta. Untuk menjadikan semua sumber dalam syarikat pinjaman tersedia kepada syarikat peminjaman, sila tinggalkan medan **Sumber** kosong.
7. Pada halaman **Pengurusan projek dan parameter perakaunan**, pada tab **Antara Syarikat**, tetapkan pilihan **Dayakan penjadualan sumber antara syarikat dan lembaran masa** kepada **Ya**.

### <a name="in-the-borrowing-company"></a>Dalam syarikat peminjaman

- Pada halaman **Senarai sumber**, dalam penapis carian, masukkan nama sumber yang anda cipta untuk syarikat pinjaman, untuk mengesahkan bahawa nama tersebut disertakan dalam senarai sumber untuk syarikat peminjaman.

## <a name="request-project-resources"></a>Permohonan sumber projek
Kefungsian untuk penjadualan sumber projek hanya membolehkan pengurus sumber edarkan sumber yang diperlukan dalam penglibatan atau projek. Untuk mendayakan kefungsian ini, lengkapkan tugas berikut, atau sahkan yang telah dilengkapkan:

- Sediakan jujukan nombor.
- Sediakan aliran kerja pengurusan projek dan perakaunan.
- Dayakan aliran kerja permintaan sumber.

Selepas tugas sebelum ini dilengkapkan, anda boleh melengkapkan tugas berikut seperti yang anda perlukan:

- Cipta permintaan sumber daripada sumber diperlukan yang ditempah sementara.
- Pantau permintaan sumber.
- Penuhi permintaan sumber.
- Minta sumber yang diperlukan daripada WBS.
- Tempah sumber untuk projek tanpa mempunyai permintaan untuk sumber yang diperlukan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]