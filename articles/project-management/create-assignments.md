---
title: Cipta tugas sumber
description: Artikel ini memberikan maklumat tentang penciptaan penugasan tugas generik dan dinamakan.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812005"
---
# <a name="create-resource-assignments"></a>Cipta tugas sumber

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


Peruntukkan sumber ialah persatuan langsung ahli pasukan projek kepada tugas nod daun. Artikel ini memberikan maklumat tentang cara berbeza untuk menugaskan sumber.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Cipta ahli pasukan generik melalui tugasan tugas


Apabila anda mencipta ahli pasukan generik melalui tugasan tugas, anda mencipta pemegang tempat atau sumber generik. Sumber generik ini menerangkan ciri-ciri sumber yang dinamakan yang akhirnya anda mahu bekerja pada tugas. Anda kemudian menjana keperluan, atau anda mengemukakan permintaan dengan menggunakan keperluan yang digunakan untuk mencari dan menempah sumber yang dinamakan.

1. Pada grid Jadual untuk tugas, pilih ikon Sumber dalam sel **Sumber**.
2. Taipkan nama untuk berfungsi sebagai nama sumber ruang letak. Contohnya, Pengurus Program.
3. Pilih **Cipta**, dan dalam medan **Cipta Pantas Ahli Pasukan Projek**, tetapkan peranan untuk sumber generik.
4. Tugaskan tugas seperti yang diperlukan kepada sumber pemegang ruang ini dengan memilih sumber pada **Pemilih Sumber** untuk tugas tersebut. Sumber tersenarai di bawah **Ahli Pasukan**.
5. Apabila anda selesai menugaskan sumber generik, pada **tab Pasukan**, pilih sumber generik, kemudian pilih **Jana Keperluan** untuk mencipta keperluan sumber untuk sumber generik.
6. Pilih **Tempah** untuk sumber generik, dan kemudian anda boleh menggunakan papan Jadual untuk mencari dan menempah sumber sebenar. Anda juga boleh menghantar keperluan untuk pemenuhan oleh pengurus sumber.
7. Apabila sumber generik dipenuhi sepenuhnya dengan sumber yang dinamakan, sumber generik dikeluarkan dari pasukan. (Pemenuhan keperluan sumber separa tidak akan menghasilkan tugasan sumber.) Tugasan tugas untuk sumber generik diberikan kepada sumber yang dinamakan yang memenuhi keperluan sumber sumber generik.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tugaskan sumber bernama dari senarai semua sumber boleh dtitempah

Anda boleh menggunakan kotak carian dalam **Pemilih Sumber** untuk mencari semua sumber boleh ditempah aktif dan menugaskannya kepada tugas nod daun. Sumber yang ditugaskan dengan cara ini ditambah kepada pasukan tanpa sebarang tempahan. Ini serupa dengan menambah ahli pasukan dan memilih **Tiada** sebagai kaedah peruntukan. Sumber dipaparkan dalam tab **Pasukan** dan **Tugasan Sumber** dan **Penyesuaian** sebagai sumber yang mempunyai hanya tugasan dan defisit tempahan. Tempah mereka jika anda ingin menggunakan ketersediaan mereka.

1. Daripada grid tugas, papan atau garis masa, navigasi ke sel **Ditugaskan Ke**.
2. Dalam kotak carian, mula menaip nama. Hasil carian untuk nama dipaparkan dalam **Pemilih Sumber** di bawah **Sumber Lain**.
3. Pilih sumber yang anda mahu peruntukkan kepada tugas atau pilih nama sumber di bawah **Sumber Pasukan Lain**.

## <a name="editing-resource-assignment-contours"></a>Mengedit kontur tugasan sumber

Secara lalai, apabila sumber ditugaskan kepada tugas dalam jadual, usaha mereka diagihkan secara linear kepada setiap sumber, berdasarkan waktu kerja sumber tersebut dan mod jadual projek. Pengurus projek boleh menggunakan grid tugasan sumber untuk memperhalusi anggaran usaha setiap sumber yang ditugaskan kepada satu atau banyak tugas merentasi skala masa yang berbeza. Ciri ini membantu pengurus projek menghasilkan anggaran kos dan jualan yang lebih tepat, yang didorong oleh kontur tugasan sumber yang dijana apabila sumber ditugaskan untuk tugas. Di samping itu, pengurus projek dapat dengan lebih mudah mencerminkan permintaan sumber yang diperlukan untuk membina permintaan dalam keperluan sumber.

### <a name="navigation"></a>Navigasi

Untuk mencapai grid pengeditan kontur, pengurus projek terlebih dahulu memilih tab Tugas pada halaman utama projek kemudian memilih **tab** Tugasan **.** 

![Tab Tugasan pada tab Tugas halaman utama projek.](media/AssignmentGrid.png)

Grid menyokong dua kaedah untuk pengumpulan: **kumpulan mengikut sumber** dan **kumpulan mengikut tugas**. Tidak seperti dalam pandangan grid, lajur tidak boleh dikonfigurasikan. Satu-satunya lajur yang kelihatan ialah **Diuntukkan Kepada,Nama** **Tugas,Mula Tugasan,Selesai** **·** **Tugasan** dan **Usaha** Tugasan.

Apabila grid pada mulanya diberikan, ia bermula pada kontur tugasan terawal. Jika jadual anda tidak mengandungi sebarang tugasan yang mempunyai usaha, grid akan kosong dan tidak akan memberikan apa-apa.

![Grid tugasan kosong.](media/emptyassignmentgrid.png)

Jika anda ingin melihat kontur anda dan skala masa yang berbeza, grid tugasan sumber baca sahaja dan grid perdamaian sumber juga tersedia.

### <a name="resource-calendars"></a>Kalendar sumber

Keupayaan untuk mengedit kontur untuk hari tertentu ditadbir oleh hari kerja sumber, seperti yang ditunjukkan dalam kalendar mereka. Jika sel dinyahdayakan untuk sumber tertentu, sumber tersebut tidak mempunyai hari bekerja dalam tempoh tersebut.

Kontur sumber boleh melangkaui tarikh mula dan tamat tugas semasa yang ditetapkan. Jika kontur dikemas kini supaya ia selepas tarikh tamat tugas yang terkini atau tarikh mula terawal tugas, tarikh tamat atau tarikh mula tugas tugas akan diubah mengikut kesesuaian. Walau bagaimanapun, jika kontur dikemas kini supaya ia lebih awal daripada tarikh permulaan tugas yang dipautkan kepada pendahulu, kemas kini akan gagal kerana tugasan akan mencetuskan tugas untuk bermula sebelum pendahulunya selesai, dan tingkah laku itu tidak disokong pada masa ini.

### <a name="co-authoring"></a>Pengarangan bersama

Perubahan pada grid tugasan sumber digambarkan secara automatik dalam sebarang pandangan yang berkaitan, termasuk carta, garis masa, papan dan pandangan grid. Jika berbilang pengguna menyemak semula projek pada masa yang sama, sebarang perubahan yang dibuat oleh seorang pengguna akan ditunjukkan dalam grid. Sebaliknya, sebarang perubahan yang dibuat dalam grid tugasan sumber akan ditunjukkan kepada semua pengguna lain yang melihat projek dalam sesi yang sama.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
