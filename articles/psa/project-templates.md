---
title: Templat projek
description: Topik ini memberikan maklumat tentang cara untuk menggunakan templat projek untuk persediaan projek pantas.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123036"
---
# <a name="project-templates"></a>Templat projek 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Templat projek adalah rangka kerja pratakrif yang membantu anda memulakan projek dengan cepat dan mudah. Anda boleh menggunakan templat pratakrif untuk mencipta projek baharu dengan satu klik. Bagi projek, anda mesti mentakrifkan prasyarat untuk templat projek. Anda mesti mentakrifkan kalendar projek untuk setiap templat projek serta senarai peranan dan harga mesti ditetapkan dalam organisasi, supaya komponen templat mempunyai data berguna.

Templat projek terdiri daripada tiga komponen: jadual, anggaran projek dan ahli pasukan projek.

## <a name="schedule"></a>Jadual

Jadual dalam templat projek mempunyai set elemen yang sama dengan jadual dalam projek. Anda boleh mencipta hierarki tugas, mengaitkan peranan dengan tugas, mentakrifkan atribut jadual dan kebergantungan set. Jadual dalam templat projek juga menyokong mod tugas untuk setiap tugas. Oleh itu, ia menyokong enjin penjadualan. Anda mesti mengaitkan kalendar projek dengan projek tersebut. Apabila anda mencipta jadual kerja, tidak ada perbezaan antara template projek dan projek.

## <a name="project-estimates"></a>Anggaran projek

Anggaran projek dalam templat projek berfungsi dengan cara yang sama seperti anggaran projek dalam projek. Walau bagaimanapun, harga kos dan jualan dikeluarkan daripada senarai kos dan harga jualan lalai yang ditakrifkan dalam parameter.

## <a name="creating-a-project-from-a-template"></a>Mencipta projek daripada templat
 
Terdapat beberapa cara untuk mencipta projek daripada templat projek:

- Apabila anda mencipta projek daripada sebut harga, anda boleh memilih templat projek dalam kotak dialog **Cipta Pantas: Projek**.

> ![Kotak dialog Cipta Pantas: Projek](media/project-11.png)

- Apabila anda mencipta projek dengan memilih **Projek Baharu**, halaman **Projek** muncul sebelum rekod disimpan. Dalam medan **Pilih Templat**, pilih salah satu templat projek yang dipratakrif dalam organisasi.
- Gunakan **Cipta Projek daripada Templat** pada halaman **Entiti Templat**.

## <a name="copying-components-of-template-to-project"></a>Menyalin komponen templat kepada projek

Apabila anda menyalin komponen templat projek kepada projek, beberapa gantian boleh berlaku, bergantung pada tetapan dalam projek.

### <a name="copying-the-schedule"></a>Menyalin jadual

Apabila anda menyalin jadual daripada templat projek, jika projek tersebut mempunyai kalendar projek yang berbeza daripada templat, jam kerja daripada kalendar projek akan digunakan pada jadual tugas. Dengan cara ini, jadual diselaraskan supaya sepadan dengan kalendar projek sokongan. Begitu juga, tugas pertama pada jadual mengambil tarikh mula projek, dan jadual bagi hierarki yang selebihnya dikemas kini berdasarkan tempoh dan kebergantungan yang ditakrifkan dalam templat. 

### <a name="copying-project-estimates"></a>Menyalin anggaran projek 

Apabila anda menyalin merentasi baris anggaran projek, senarai harga dikemas kini. Untuk senarai harga kos, kemas kini ini adalah berdasarkan unit pemilikan projek. Untuk senarai harga jualan, ia adalah berdasarkan kepada pelanggan. Bagi projek yang dikaitkan dengan entiti jualan, kos unit dan harga jualan ditentukan berdasarkan pada senarai harga ini.

### <a name="copying-a-project-team"></a>Menyalin pasukan projek

Apabila pasukan projek disalin daripada templat projek kepada projek, sumber generik disalin, bersama-sama dengan kemahiran dan kecekapan yang ditakrifkan dalam template. Tugasan sumber generik juga dikekalkan sebagai mana ia di dalam templat projek. Sumber yang dinamakan tidak disokong dalam templat projek.
