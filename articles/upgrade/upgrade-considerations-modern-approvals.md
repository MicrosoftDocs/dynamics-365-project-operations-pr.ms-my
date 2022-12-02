---
title: Peningkatan pertimbangan untuk Kelulusan Moden
description: Artikel meliputi mata yang patut dipertimbangkan oleh pentadbir apabila mereka mendayakan fungsi Kelulusan Moden.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931755"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Peningkatan pertimbangan untuk Kelulusan Moden 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Sebagai sebahagian daripada keluaran April 2022 Gelombang 1, fungsi Kelulusan Moden akan didayakan secara lalai. Kefungsian ini meningkatkan kebolehpercayaan logik kelulusan dan memastikan bahawa anda boleh menentukan sebab jika logik kelulusan gagal.

Sebagai sebahagian daripada perubahan ini, perubahan status untuk kelulusan projek dikemas kini. Status kini akan terus daripada **Dihantar** kepada **Diluluskan**. **Belum selesai** bukan lagi status untuk kelulusan. Untuk menentukan sama ada kelulusan adalah belum selesai, mengesahkan bahawa kelulusan merupakan sebahagian daripada set kelulusan dan semak keadaan set kelulusan yang dilampirkan.

## <a name="before-you-upgrade"></a>Sebelum anda tatar

Sebelum anda tatar kepada Kelulusan Moden, pastikan bahawa anda tidak mempunyai kelulusan yang belum selesai. Kelulusan Moden tidak menggunakan status **Belum Selesai**. Oleh itu, sebarang kelulusan yang masih ditandakan sebagai **Belum Selesai** selepas tatar ini tidak akan diproses.

## <a name="after-you-upgrade"></a>Selepas anda tatar

Selepas anda tatar kepada Kelulusan Moden, pentadbir mesti mengesahkan bahawa aliran awan yang memproses kelulusan telah didayakan.

1. Daftar masuk ke [flow.microsoft.com](https://flow.microsoft.com)
2. Di bahagian atas sebelah kanan halaman, tukar persekitaran anda kepada persekitaran yang anda telah tatar.
3. Pilih **Penyelesaian** untuk menyenaraikan penyelesaian yang dipasang dalam persekitaran.
4. Dalam senarai penyelesaian, pilih **Project Operations** atau **Project Service**.
5. Tukar penapis daripada **Semua** kepada **Aliran Awan**.
6. Sahkan bahawa pilihan **Project Service – Jadualkan Set Kelulusan Projek Secara Berulang** ditetapkan kepada **Hidup**. Jika tidak, pilih aliran, kemudian **Hidupkan**.
7. Sahkan bahawa pemprosesan berlaku setiap lima minit dengan menyemak kawasan **Kerja Sistem** dalam **Tetapan**.

## <a name="short-term-rollback"></a>Pengunduran balik jangka pendek

Jika anda tidak dapat mengambil perubahan tersebut atau jika anda menghadapi isu yang teruk dengan ciri ini, anda boleh kembali secara sementara ke aliran kelulusan asal dengan melakukan langkah berikut:
1. Daftar masuk ke persekitaran anda dan sahkan tiada kelulusan yang belum selesai.
2. Pergi ke **Tetapan** > **Parameter Projek**.
3. Pilih **Kawalan Ciri**, kemudian pilih **Kelulusan Moden** untuk memadamkan ciri.

## <a name="removing-the-feature-flag"></a>Mengalih keluar bendera ciri

Dalam kemas kini Oktober 2022 Gelombang 2, keupayaan untuk mematikan ciri ini akan dialih keluar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
