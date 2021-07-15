---
title: Integrasi Microsoft Project Client
description: Merancang dan menyelenggara jadual projek boleh menjadi proses yang rumit, oleh itu, pengurus projek perlu menggunakan alat yang membantu mereka menguruskan tugas ini. Integrasi dengan Microsoft Project Client menyediakan sokongan untuk membuka dan menguruskan struktur pecahan kerja projek.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269846"
---
# <a name="microsoft-project-client-integration"></a>Integrasi Microsoft Project Client

[!include [banner](../includes/banner.md)]

Merancang dan menyelenggara jadual projek boleh menjadi proses yang rumit, oleh itu, pengurus projek perlu menggunakan alat yang membantu mereka menguruskan tugas ini. Integrasi dengan Microsoft Project Client menyediakan sokongan untuk membuka dan menguruskan struktur pecahan kerja projek. Pengurus projek boleh menerbitkan apa-apa perubahan kembali kepada struktur pecahan kerja projek Dynamics 365 Finance.

> [!NOTE]
> Jika anda menggunakan versi kemas kini Julai (versi 10.0.4), anda mesti memasang KB 4054797 dan 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurasikan tambahan Microsoft Project Client
Untuk mendayakan integrasi dengan Microsoft Project Client, tambahan Microsoft Dynamics 365 diperlukan untuk dipasang dalam aplikasi Microsoft Project klien pengguna. Ini boleh dilakukan dengan membuka **Ruang kerja pengurusan projek**.

•   Klik **Konfigurasikan tambahan klien projek** daripada **Pautan** > **bahagian Persediaan** ruang kerja.

•   Klik **Buka**, kemudian klik **Jalankan** apabila digesa.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Buka dan edit struktur pecahan kerja draf yang sedia ada dalam Microsoft Project Client
Jika projek dalam Dynamics 365 Finance sudah pun mempunyai struktur pecahan kerja yang dicipta, struktur pecahan kerja boleh dibuka dalam aplikasi Microsoft Project Client jika struktur pecahan kerja berada dalam status draf. Untuk membuka daripada halaman **Projek**, klik pautan **Buka dalam Microsoft Project** daripada tab **Pelan**. Halaman ini juga boleh dibuka dari dalam aplikasi Microsoft Project Client dengan mengklik **Buka** dalam tab **Microsoft Dynamics 365**. Pilih **Entiti undang-undang** dan **Projek** daripada senarai.

> [!NOTE]
> Jika anda menggunakan Internet Explorer sebagai pelayar anda, anda akan perlu klik **Simpan** untuk membuka secara manual dari lokasi yang fail itu dimuat turun. Atau, klik **Simpan dan buka** untuk membuka fail dalam Microsoft Project Client. Jangan namakan semula nama fail semasa menyimpan.

Sebelum membuat apa-apa pengeditan pada fail dengan menggunakan Microsoft Project Client, anda perlu mendaftar keluar fail. Klik **Daftar keluar** dalam tab **Microsoft Dynamics 365**. Ini akan mengelakkan pengguna lain daripada mengedit struktur pecahan kerja dari dalam Kewangan pada masa yang sama. Untuk menerbitkan struktur pecahan kerja selepas menyelesaikan apa-apa pengeditan, klik **Daftar masuk** pada tab **Microsoft Dynamics 365**.

Jika pasukan projek sudah ditambah pada projek dalam Kewangan, senarai sumber akan diisi dengan ahli pasukan. Jika pasukan projek belum lagi ditambah pada projek, anda boleh memilih sumber dan membina pasukan dalam Microsoft Project Client dengan mengklik butang **Sumber** pada tab **Microsoft Dynamics 365**. 

Data berikut akan disegerakkan kembali kepada Kewangan sebagai sebahagian daripada proses daftar masuk:

•   Nama tugas

•   Tarikh mula

•   Tarikh siap

•   Terdahulu

•   Nama sumber

•   Kategori

•   Kategori sumber

•   Jam kerja

•   Nota

•   Keutamaan

> [!NOTE]
> Jika anda menambah apa-apa lajur lain pada fail Microsoft Project Client anda, lajur tersebut tidak akan disimpan pada fail dan tidak akan dipaparkan apabila fail dibuka semula.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Cipta struktur pecahan kerja untuk projek yang sedia ada menggunakan Microsoft Project Client
Untuk mencipta struktur pecahan kerja baharu dengan menggunakan Microsoft Project Client, ikut langkah ini:


1.  Buka Microsoft Project Client.

2.  Pada tab **Microsoft Dynamics 365**, klik **Buka**.

3.  Pilih **Entiti undang-undang** untuk projek.

4.  Pilih **Projek**.

5.  Klik **Daftar keluar** pada tab **Microsoft Dynamics 365**.

6.  Apabila anda sedia untuk menerbitkan kepada Kewangan, klik **Daftar masuk** pada tab **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Gantikan struktur pecahan kerja yang sedia ada untuk projek sedia ada menggunakan Microsoft Project Client
Untuk mencipta struktur pecahan kerja baharu dengan menggunakan Microsoft Project Client dan menggantikan struktur pecahan kerja yang sedia ada untuk projek sedia ada, ikut langkah ini:

1.  Buka Microsoft Project Client.

2.  CIpta jadual dalam Microsoft Project Client.

3.  Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Gantikan projek sedia ada**.

4.  Pilih **Entiti undang-undang** untuk projek.

5.  Pilih **Projek**.

6.  Klik **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Cipta projek baharu dari dalam Microsoft Project Client


1.  Buka Microsoft Project Client.

2.  CIpta jadual dalam Microsoft Project Client.

3.  Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Simpan pada Projek baharu**.

4.  Pilih **Entiti undang-undang** untuk projek.

5.  Masukkan **ID projek**, jika perlu.

6.  Masukkan **Nama projek**.

7.  Pilih **Jenis projek**, **Kumpulan projek** dan **ID kontrak projek**. Sebagai alternatif, anda boleh mencipta kontrak projek baharu dengan mengklik **Baharu**.

8.  Pilih **Kalendar** untuk digunakan untuk penyumberan.

11. Klik **OK**.

> [!NOTE]
> Tambahan Klien Projek tidak menyokong aksara berikut dalam format ID projek:
> 
>   - Garis bawah
>   - Noktah
>   - Ruang
>   - Garis Miring

[!INCLUDE[footer-include](../includes/footer-banner.md)]
