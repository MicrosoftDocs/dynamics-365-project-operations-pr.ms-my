---
title: Pertimbangan naik taraf untuk Kelulusan Moden
description: Topik ini merangkumi perkara yang harus dipertimbangkan oleh pentadbir apabila mereka mendayakan fungsi Kelulusan Moden.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578397"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Pertimbangan naik taraf untuk Kelulusan Moden 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Sebagai sebahagian daripada Keluaran Gelombang 1 April 2022, fungsi Kelulusan Moden akan didayakan secara lalai. Fungsi ini meningkatkan kebolehpercayaan logik kelulusan dan memastikan bahawa anda boleh menentukan sebab jika logik kelulusan gagal.

Sebagai sebahagian daripada perubahan ini, perubahan status untuk kelulusan projek dikemas kini. Status kini pergi terus dari **Dihantar** ke **Diluluskan**. **Belum selesai** bukan lagi status untuk kelulusan. Untuk menentukan sama ada kelulusan belum selesai, sahkan bahawa kelulusan adalah sebahagian daripada set kelulusan, dan semak keadaan set kelulusan yang dilampirkan.

## <a name="before-you-upgrade"></a>Sebelum anda menaik taraf

Sebelum anda menaik taraf kepada Kelulusan Moden, pastikan anda tidak mempunyai kelulusan yang belum selesai. Kelulusan Moden tidak menggunakan **status Menunggu**. Oleh itu, sebarang kelulusan yang masih ditandakan sebagai **Menunggu** selepas naik taraf tidak akan diproses.

## <a name="after-you-upgrade"></a>Selepas anda menaik taraf

Selepas anda menaik taraf kepada Kelulusan Moden, pentadbir mesti mengesahkan bahawa aliran awan yang memproses kelulusan telah didayakan.

1. Log masuk ke [flow.microsoft.com](https://flow.microsoft.com)
2. Di bahagian atas sebelah kanan halaman, tukar persekitaran anda kepada persekitaran yang telah anda naik taraf.
3. Pilih **Penyelesaian** untuk menyenaraikan penyelesaian yang dipasang dalam persekitaran.
4. Dalam senarai penyelesaian, pilih **Operasi** Projek atau **Perkhidmatan** Projek.
5. Tukar penapis daripada **Semua** kepada **Aliran** Awan.
6. Sahkan bahawa **Perkhidmatan Projek - Pilihan Set** Kelulusan Projek Jadual Berulang disetkan kepada **Hidup**. Jika tidak, pilih aliran, kemudian pilih **Hidupkan**.
7. Sahkan bahawa pemprosesan berlaku setiap lima minit dengan **menyemak senarai Kerja** Sistem di **kawasan Tetapan**.

## <a name="short-term-rollback"></a>Gulung balik jangka pendek

Jika anda tidak dapat menerima perubahan atau jika anda menghadapi masalah yang teruk dengan ciri ini, anda boleh kembali ke aliran kelulusan asal buat sementara waktu dengan melaksanakan langkah berikut:
1. Daftar masuk ke persekitaran anda dan sahkan bahawa tiada kelulusan yang belum selesai.
2. Pergi ke **Tetapan** > **Parameter** Projek.
3. Pilih **Kawalan** Ciri dan kemudian pilih **Kelulusan** Moden untuk mematikan ciri.

## <a name="removing-the-feature-flag"></a>Mengalih keluar bendera ciri

Dalam kemas kini Gelombang 2 Oktober 2022, keupayaan untuk mematikan ciri ini akan dialih keluar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
