---
title: Pertimbangan naik taraf - Microsoft Dynamics 365 Project Service Automation versi 2.x atau 1.x kepada versi 3
description: Topik ini menyediakan maklumat tentang pertimbangan yang perlu anda lakukan apabila anda menaik taraf daripada Project Service Automation versi 2.x atau 1.x kepada versi 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b29ef5d6d2c1c97658d79bbbe82e5893adeafe4d20354e90058dde79b67cb716
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000092"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Pertimbangan naik taraf - PSA versi 2.x atau 1.x kepada versi 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation dan Field service
Dynamics 365 Project Service Automation dan Dynamics 365 Field Service menggunakan penyelesaian Universal Resourcing Scheduling (URS) untuk penjadualan sumber. Jika anda mempunyai Project Service Automation dan Field Service dalam tika anda, naik taraf kedua-dua penyelesaian kepada versi terkini. Untuk Project Service Automation, iaitu versi 3.x. Untuk Field Service, iaitu versi 8.x. Menaik taraf Project Service Automation atau Field Service akan memasang versi URS yang terkini. Jika kedua-dua penyelesaian Project Service Automation dan Field Service berada dalam tika sama yang tidak dinaik taraf kepada versi terkini, mungkin akan terdapat sedikit tingkah laku yang tidak konsisten.

## <a name="resource-assignments"></a>Penugasan sumber
Dalam Project Service Automation versi 2 dan versi 1, penugasan tugasan disimpan sebagai tugas anak (juga dipanggil tugas baris) dalam **Entiti tugas** dan berkaitan secara tidak langsung dengan entiti **Penugasan Sumber**. Tugas baris kelihatan pada tetingkap timbul tugasan pada Struktur Pecahan Kerja (WBS).

![Tugas baris pada WBS dalam Project Service Automation versi 2 dan versi 1.](media/upgrade-line-task-01.png)

Dalam versi 3 Project Service Automation, skema dasar yang menugaskan sumber boleh ditempah kepada tugas telah berubah. Tugas baris ditamatkan dan terdapat perhubungan 1:1 yang langsung antara tugas dalam **Entiti tugas** dan ahli pasukan dalam entiti **Tugasan Sumber**. Tugas yang ditugaskan kepada ahli pasukan projek kini disimpan secara langsung dalam entiti Tugasan Sumber.  

Perubahan ini memberi kesan kepada naik taraf mana-mana projek yang mempunyai tugasan sumber untuk sumber boleh ditempah yang telah dinamakan dan sumber generik pada pasukan projek. Topik ini menyediakan pertimbangan bahawa anda perlu mengambil kira projek anda apabila anda menaik taraf ke versi 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tugas ditugaskan kepada sumber yang dinamakan
Menggunakan entiti tugas dasar, tugas dalam versi 2 dan versi 1 membenarkan ahli pasukan untuk menggambarkan peranan selain daripada peranan tertakrif lalai mereka. Contohnya, Farziah Fairuz yang secara lalai ditugaskan peranan Pengurus Program, boleh ditugaskan untuk tugas dengan peranan Pembangun. Dalam versi 3, peranan ahli pasukan yang dinamakan sentiasa menjadi lalai, maka apa-apa tugas yang ditugaskan kepada Farziah Fairuz menggunakan peranan lalainya sebagai Pengurus Program.

Jika anda telah menugaskan sumber kepada tugas di luar peranan lalai mereka dalam versi 2 dan versi 1, apabila anda menaik taraf, sumber yang dinamakan akan ditugaskan dengan peranan lalai untuk semua tugasan tugas tanpa mengira tugasan peranan dalam versi 2. Tugasan ini menghasilkan perbezaan dalam anggaran yang dikira daripada versi 2 atau versi 1 hingga versi 3 kerana anggaran dikira berdasarkan pada peranan sumber dan bukan tugasan tugas baris. Contohnya, dalam versi 2, dua tugas telah ditugaskan kepada Rokiah Awang. Peranan pada tugas baris untuk tugas 1 ialah Pembangun dan untuk tugas 2, Pengurus Program. Rokiah Awang mempunyai peranan lalai Pengurus Program.

![Berbilang peranan ditugaskan kepada satu sumber.](media/upgrade-multiple-roles-02.png)

Oleh sebab peranan Pembangun dan Pengurus Program berbeza, anggaran kos dan jualan adalah seperti berikut:

![Anggaran kos untuk peranan sumber.](media/upggrade-cost-estimates-03.png)

![Anggaran jualan untuk peranan sumber.](media/upgrade-sales-estimates-04.png)

Apabila anda menaik taraf kepada versi 3, tugas baris digantikan dengan tugasan sumber pada tugas ahli pasukan sumber boleh ditempah. Tugasan akan menggunakan peranan lalai daripada sumber boleh ditempah. Dalam grafik berikut, Rokiah Awang yang mempunyai peranan sebagai Pengurus Program Manager adalah sumber.

![Penugasan sumber.](media/resource-assignment-v2-05.png)

Oleh sebab anggaran adalah berdasarkan pada peranan lalai untuk sumber, anggaran jualan dan kos mungkin berubah. Dalam grafik berikut, anda tidak lagi melihat peranan **Pembangun** kerana peranan kini diambil daripada peranan lalai sumber boleh ditempah.

![Anggaran kos untuk peranan lalai.](media/resource-assignment-cost-estimate-06.png)
![Anggaran jualan untuk peranan lalai.](media/resource-assignment-sales-estimate-07.png)

Selepas naik taraf selesai, anda boleh mengedit peranan ahli pasukan menjadi sesuatu selain daripada lalai yang ditugaskan. Walau bagaimanapun, jika anda mengubah peranan ahli pasukan, ia akan diubah kepada semua tugas yang ditetapkan kerana ahli pasukan tidak lagi boleh ditugaskan dengan berbilang peranan dalam versi 3.

![Mengemas kini peranan sumber.](media/resource-role-assignment-08.png)

Hal ini turut benar untuk tugas baris yang ditugaskan kepada sumber dinamakan apabila anda mengubah unit organisasi sumber daripada lalai kepada unit organisasi lain. Selepas naik taraf versi 3 selesai, tugasan akan menggunakan unit organisasi lalai sumber dan bukannya yang ditetapkan pada tugas baris.

### <a name="tasks-assigned-to-generic-resources"></a>Tugas ditugaskan kepada sumber generik
Dalam versi 2 dan versi 1, anda boleh menetapkan peranan dan unit organisasi pada tugas dan kemudian gunakan ciri **Jana pasukan** untuk menjana sumber generik berdasarkan pada atribut yang ditetapkan pada tugas. Dalam versi 3, anda mencipta ahli pasukan generik dengan peranan dan unit organisasi dan kemudian menugaskan ahli pasukan kepada tugas.

Dalam versi 2 dan versi 1, projek dengan sumber generik boleh berada dalam dua keadaan atau gabungan kedua-duanya di peringkat tugas. Contohnya, anda boleh mempunyai senario berikut:

- Tugas dengan peranan dan unit organisasi yang ditetapkan tetapi tiada tugasan sumber gabungan yang dijana.
- Tugas dengan tugasan sumber ahli pasukan generik yang ditugaskan dengan mencipta sumber generik menggunakan ciri **Jana pasukan**.

Sebelum anda mula menaik taraf, kami mengesyorkan agar anda menjana semula pasukan untuk setiap projek yang mempunyai tugas yang ditetapkan kepada sumber generik atau masih belum menjana proses pasukan dijalankan pada mereka.

Untuk tugas yang ditugaskan kepada ahli pasukan generik yang dijana dengan **Jana Pasukan**, naik taraf ini akan meninggalkan sumber generik dalam pasukan dan meninggalkan tugasan kepada ahli pasukan generik itu. Kami mengesyorkan agar anda menjana keperluan sumber untuk ahli pasukan generik selepas naik taraf tetapi sebelum anda menempah atau menyerahkan permintaan sumber. Ini akan mengekalkan mana-mana tugasan unit organisasi pada ahli pasukan generik yang berbeza daripada unit organisasi kontrak projek.

Contohnya, dalam Projek Z, unit organisasi kontrak ialah Contoso AS. Dalam pelan projek, tugas ujian dalam Fasa Pelaksanaan telah ditugaskan dengan peranan Perunding Teknikal dan unit organisasi yang ditugaskan ialah Contoso India.

![Tugasan organisasi fasa pelaksanaan.](media/org-unit-assignment-09.png)

Selepas fasa pelaksanaan, tugas ujian integrasi ditugaskan kepada peranan Perunding teknikal tetapi organisasi ditetapkan kepada Contoso AS.  

![Tugasan organisasi tugas ujian integrasi.](media/org-unit-generate-team-10.png)

Apabila anda menjana pasukan untuk projek, dua ahli pasukan generik dicipta kerana unit organisasi yang berlainan pada tugas. Perunding teknikal 1 akan ditugaskan dengan tugas Contoso India dan Perunding teknikal 2 akan mempunyai tugas Contoso AS.  

![Ahli pasukan generik yang dijanakan.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Dalam Project Service Automation versi 2 dan versi 1, ahli pasukan tidak memegang unit organisasi yang dikekalkan dalam tugas baris.

![Tugas baris versi 2 dan versi 1 dalam Project Service Automation.](media/line-tasks-12.png)

Anda boleh melihat unit organisasi pada pandangan anggaran. 

![Anggaran unit organisasi.](media/org-unit-estimates-view-13.png)
 
Apabila naik taraf selesai, unit organisasi pada tugas baris yang sepadan dengan ahli pasukan generik ditambah kepada ahli pasukan generik dan tugas baris dialih keluar. Oleh sebab ini, kami mengesyorkan agar sebelum anda menaik taraf, anda menjana atau menjana semula pasukan pada setiap projek yang mengandungi sumber generik.

Bagi tugas yang ditugaskan untuk peranan dengan unit organisasi yang berbeza daripada unit organisasi projek kontrak, dan pasukan yang masih belum dijana, naik taraf akan mencipta ahli pasukan generik untuk peranan, tetapi akan menggunakan unit kontrak daripada projek untuk unit organisasi ahli pasukan. Merujuk kembali kepada contoh dengan Projek Z, unit organisasi kontrak Contoso AS dan tugas ujian pelan projek dalam Fasa implementasi telah ditugaskan peranan Perunding Teknikal dengan unit organisasi yang ditugaskan kepada Contoso India. Tugas ujian Integrasi yang diselesaikan selepas Fasa pelaksanaan telah ditugaskan untuk peranan Perunding teknikal. Unit organisasi ialah Contoso AS dan pasukan masih belum dijana. Naik taraf akan mencipta satu ahli pasukan generik, Perunding teknikal yang mempunyai jam yang ditugaskan bagi ketiga-tiga tugas dan unit organisasi Contoso AS, unit organisasi kontrak projek.   
 
Mengubah lalai unit organisasi yang berbeza pada ahli pasukan yang tidak dijana adalah sebab kami mengesyorkan supaya anda menjana atau menjana semula pasukan pada setiap projek yang mengandungi sumber generik sebelum naik taraf supaya tugasan unit organisasi tidak hilang.



[!INCLUDE[footer-include](../includes/footer-banner.md)]