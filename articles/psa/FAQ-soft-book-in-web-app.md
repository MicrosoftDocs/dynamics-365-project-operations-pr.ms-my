---
title: Bagaimanakah saya "menempah sementara" sumber dalam versi aplikasi 2.x?
description: Artikel ini menghuraikan cara menempah sementara ahli pasukan projek dengan Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585205"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Bagaimanakah saya "menempah sementara" sumber dalam aplikasi web (aplikasi Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Anda boleh secara sementara menjadualkan atau "menempah sementara" sumber ke atas pasukan projek untuk menunjukkan yang anda merancang untuk menugaskan sumber kepada projek. Tempahan sementara tidak menggunakan kapasiti tersedia sumber. Ahli pasukan ditempah sementara tidak boleh ditugaskan kepada tugas projek. Hanya sumber yang mempunyai Status Ditempah Tetap dan Jenis Perlakuan Terikat boleh ditugaskan kepada tugas (dengan anggapan yang ia mempunyai jam tempahan tetap yang mencukupi meliputi usaha tugasan).

Ahli pasukan projek ditempah sementara muncul dalam grid Ahli Pasukan dengan jam ditempah sementara mereka ditunjukkan dalam lajur Tempah Sementara. Mereka juga muncul pada papan jadual. Tambahan pula, mereka tidak menunjukkan penggunaan kapasiti kerana tempahan sementara tidak menggunakan kapasiti sumber.

Terdapat tiga cara untuk menempah sementara ahli pasukan ke atas projek dengan Project Service versi 2.x. Anda boleh menempah sementara dengan papan jadual, gunakan ciri Kekalkan Tempahan atau dengan mencipta sumber generik. Kaedah ini dihuraikan seperti di bawah.

## <a name="soft-book-with-the-schedule-board"></a>Tempah sementara dengan papan jadual

Untuk menempah sementara dengan papan jadual, ikuti prosedur ini: 
1. Buka papan jadual.
2. Pilih tab Projek di bahagian bawah panel Keperluan Tempahan papan jadual.
3. Cari projek yang anda ingin menempah sementara sumber ke atasnya. Jika anda mempunyai banyak projek, klik pengepala lajur Projek dan kemudian gunakan penapis untuk mencari projek anda.
4. Klik pada projek, kemudian seret dan lepaskannya pada grid masa sumber.
5. Ini membuka panel Cipta Tempahan Sumber di sebelah kanan. Laraskan tarikh mula dan akhir, pilih Status Tempahan sebagai Sementara dan tetapkan jam. 
6. Klik Tempah.
7. Kembali ke projek, sumber kini akan ditunjukkan sebagai ahli pasukan dengan jam ditempah sementara dalam lajur Tempah Sementara.

Perhatian bahawa anda tidak boleh menugaskan mereka dengan tugas pada struktur pecahan kerja (WBS) kerana sumber haruslah ditempah tetap pada pasukan yang akan ditugaskan.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Tempah sementara menggunakan ciri Kekalkan Tempahan

Untuk menempah sementara dengan Kekalkan Tempahan, ikuti prosedur ini:
1. Dari grid ahli pasukan, Klik Baharu.
2. Pilih sumber, peranan, dari/ke yang boleh ditempah.
3. Pilih kaedah peruntukan selain daripada Tiada:
- Kapasiti Penuh
- Kapasiti Peratusan
- Edarkan Dengan Sekata Mengikut Jam
- Caj Muka Mengikut Jam
4. Klik Simpan. Anda akan melihat sumber pada grid pasukan dan jam mereka ditunjukkan sebagai Tetap.
5. Kekalkan tempahan sumber dengan mengklik Kekalkan Tempahan.
6. Apabila papan jadual dibuka, kembangkan sumber untuk menunjukkan tempahan mereka. Anda akan melihat tempahan yang ditunjukkan sebagai Tetap.
7. Klik kanan tempahan, di bawah bahagian Tukar Status, pilih Tempah Sementara dan kemudian Sementara. Status tempahan kini Sementara.
8. Selepas menutup papan jadual, anda akan melihat bahawa jam untuk sumber telah bertukar daripada Tetap kepada Sementara pada grid ahli pasukan.
Perhatian bahawa jika anda menempah tetap sumber ke atas pasukan dan kemudian menugaskan mereka dengan tugas dalam WBS, apabila anda menggunakan kekalkan tempahan untuk menukar status Tetap kepada Sementara, ia akan mengeluarkan tugasan daripada tugas untuk sumber itu kerana hanya sumber ditempah tetap boleh ditugaskan kepada tugas.

## <a name="soft-book-by-creating-a-generic-resource"></a>Tempah sementara dengan mencipta sumber generik

Anda boleh mencipta tempahan sementara dengan menjana ahli pasukan sumber generik, memenuhi papan jadual atau Permintaan Sumber dan menukar jenis semasa tempahan.
Untuk melakukan ini, gunakan prosedur berikut:

1. Pada projek WBS, tugaskan peranan kepada tugas yang anda ingin janakan untuk ahli pasukan generik.
2. Klik Jana Pasukan Projek.
3. Pada grid ahli pasukan projek, pilih sumber generik dan klik Tempah.
4. Pada papan jadual, pilih sumber yang anda ingin menempah.
5. Pada papan jadual panel Cipta Tempahan Sumber, tukar Status Tempahan kepada Sementara.
6. Klik Tempah atau Tempah dan Keluar.

Selepas menutup papan jadual, anda akan melihat sumber terpilih ditambah kepada pasukan dengan jam ditempah Sementara serta jam ditugaskan. Anda juga akan melihat bahawa sumber generik kekal berada dalam pasukan sebagai penunjuk yang tugas diberikan kepada ahli pasukan ditempah sementara.

Apabila anda sudah bersedia untuk menukar sumber ahli pasukan ditempah sementara kepada ahli pasukan ditempah tetap supaya anda boleh menugaskan mereka kepada tugas, lakukan yang berikut:

1. Pilih sumber dan klik Kekalkan Tempahan.
2. Apabila papan jadual dibuka, kembangkan sumber untuk menunjukkan tempahan mereka. Anda akan melihat tempahan ditanda sebagai Sementara.
3. Klik kanan tempahan, di bawah bahagian Tukar Status, pilih Tempah Tetap dan kemudian Tetap. Status tempahan kini Tetap.
4. Selepas menutup papan jadual, anda akan melihat bahawa jam untuk sumber telah bertukar daripada Sementara kepada Tetap pada grid ahli pasukan. Anda kini boleh menugaskan sumber kepada tugas (dengan syarat terdapat penjajaran antara jam ditempah tetap dan jam usaha tugas untuk tugasan). Perhatian bahawa jika anda mengikuti langkah pemenuhan sumber generik dalam item #3 di atas, apabila anda menukar status sumber boleh ditempah untuk ditempah sementara kepada tetap, ahli pasukan generik akan dikeluarkan dari pasukan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
