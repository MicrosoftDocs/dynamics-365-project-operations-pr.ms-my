---
title: Sediakan peranan pada templat Struktur pecahan kerja
description: Topik ini memberikan maklumat tentang menyediakan maklumat peranan pada templat Struktur pecahan kerja.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c84015c46f0a8c9d3d48be1b995d4bdd7fd8ee25b240f455bbe2031f42adc0f5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008912"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Sediakan peranan pada templat Struktur pecahan kerja

[!include [banner](../includes/banner.md)]

Pengurus projek boleh menyediakan templat Struktur pecahan kerja yang boleh mereka gunakan apabila mereka mencipta WBS untuk projek baharu. Pengurus projek boleh menambah peranan apabila mereka mencipta templat. Gunakan prosedur berikut untuk tugaskan peranan kepada templat WBS.

1. Pilih **Pengurusan projek dan perakaunan** > **Persediaan** > **Projek** > **Templat struktur pecahan kerja**.
2. Pilih **Butiran** untuk templat WBS yang dipilih.
3. Pilih tugas dalam senarai, dan kemudian, dalam medan **Peranan**, pilih peranan untuk tugaskan kepada tugas tersebut.

## <a name="work-with-a-wbs"></a>Bekerja dengan WBS

Anda boleh mencipta WBS baharu, atau anda boleh menyalin WBS daripada templat WBS sedia ada. Pengurus projek boleh mengurus sumber dengan mudah dengan menugaskan peranan kepada tugas baharu dalam WBS. Peranan boleh digantikan sama ada selepas sumber diperolehi atau selepas sumber yang disahkan untuk kerja pada tugas adalah dikenal pasti. Fleksibiliti ini membolehkan pengurus projek melaksanakan tugas berikut:

- Kenal pasti bilangan sumber yang diperlukan untuk pakej kerja WBS.
- Anggarkan kos projek.
- Tentukan belanjawan awal.
- Anggarkan tempoh aktiviti, berdasarkan peranan dan sumber.
- Bangunkan beberapa pelan pengurusan projek, berdasarkan maklumat projek yang tersedia.

Pilihan tambahan telah ditambah dalam WBS untuk menggunakan kefungsian penyumberan dengan lebih baik.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pilihan</th>
<th>Penerangan</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Penugasan sumber</td>
<td>Lihat sumber, tarikh, bilangan jam, dan jenis tempahan yang diberikan untuk tugas pada WBS.</td>
</tr>
<tr class="even">
<td>Menjana pasukan secara automatik</td>
<td>Tambah sumber yang dirancang secara automatik dengan menggunakan peranan yang berkaitan dengan tugas. Kewangan secara automatik mencadangkan sumber yang dirancang dengan menggunakan analisis keputusan berbilang kriteria berdasarkan peranan. Selepas peranan dan usaha (jam) telah ditetapkan untuk tugas dalam WBS, dan selepas struktur telah dikeluarkan, pilih <strong>Menjana pasukan secara automatik</strong>. Bilangan sumber yang dirancang yang diperlukan akan ditambahkan ke WBS dan tab <strong>Penjadualan projek dan pasukan</strong>.</td>
</tr>
<tr class="odd">
<td>Sumber (senarai juntai bawah)</td>
<td>Pada halaman <strong>Lancarkan tugasan sumber</strong>, anda boleh memilih sumber untuk menempah tetap atau menempah sementara, berdasarkan tempoh yang ditentukan. Anda boleh melaraskan tetapan pandangan untuk melihat dan menetapkan tempoh aktiviti sumber. Anda boleh memilih dan tugaskan sumber pada tahap pakej kerja dengan menggunakan pilihan berikut:
<ul>
<li><strong>Terima</strong> – Sahkan perubahan kepada sumber yang ditugaskan kepada tugas.</li>
<li><strong>Batalkan</strong> – Batalkan perubahan kepada sumber yang ditugaskan kepada tugas.</li>
<li><strong>Tugaskan secara automatik</strong> – Sumber diperlukan tersedia yang mempunyai peranan sepadan yang dipilih secara automatik dan ditugaskan kepada tugas yang dipilih.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Pada halaman **Semua projek**, pilih projek **Naik taraf XYZ Fasa 2**.
2. Pilih **Rancang** > **Aktiviti** > **Struktur pecahan kerja**.
3. Pilih **Baharu** untuk menambah aktiviti tahap satu yang berikut kepada WBS:

    - Memulakan
    - Perancangan
    - Melaksanakan
    - Pemantauan dan Kawalan
    - Tutup

4. Tetapkan tarikh dan usaha (jam), seperti yang ditunjukkan dalam ilustrasi berikut.

    [![Tetapan tarikh dan usaha.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pilih baris tugas **Memulakan**, dan kemudian, dalam medan **Peranan**, pilih **Pengurus Projek Kanan**.
6. Pilih **Terbitkan**.
7. Pada baris yang sama, dalam medan **Sumber**, pilih **Daniel Goldschmidt**, dan kemudian pilih **Terima**.
8. Pilih baris tugas **Perancangan**, dan kemudian, dalam medan **Peranan**, pilih **Penganalisis perniagaan**.
9. Pilih **Terbitkan**, dan kemudian pilih **Menjana pasukan secara automatik**.
10. Dalam kotak mesej yang muncul, pilih **Ya**.
11. Dalam medan **Sumber**, sahkan bahawa nilai adalah **Penganalisis perniagaan 1**.
12. Untuk sumber **Penganalisis perniagaan 1**, buka carian, dan pilih **Lancarkan tugasan sumber**. Kemudian pilih pekerja untuk tugas itu.
13. Pilih **Tugaskan sementara** &gt; **Kapasiti penuh**.

    > [!NOTE] 
    > Anda tidak menerima amaran bahawa sumber yang ditentukan adalah kini 2, kerana bilangan sumber kekal 1.

14. Pada halaman **Struktur pecahan kerja**, mengesahkan tugasan sumber pada WBS, dan kemudian pilih **Simpan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]