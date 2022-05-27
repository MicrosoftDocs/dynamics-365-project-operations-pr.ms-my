---
title: Bagaimanakah cara saya menugaskan sumber boleh ditempah kepada tugas dalam aplikasi web?
description: Satu gambaran keseluruhan cara anda boleh menugaskan sumber boleh ditempah.
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
ms.openlocfilehash: 0aaf7f69fa8ae081a74fbc4f18014686f625661c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578857"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Bagaimanakah saya menugaskan sumber boleh tempah kepada tugas dalam aplikasi web (aplikasi Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Terdapat dua cara untuk menugaskan sumber kepada tugas dalam Project Service. Anda boleh menempah sumber sebagai ahli pasukan dan kemudian menugaskannya kepada tugas Atau anda boleh mencipta ahli pasukan generik melalui tugasan peranan pada tugas, menjana pasukan dan kemudian memnuhi keperluan sandaran dengan sumber yang dinamakan.

Perhatian bahawa jika anda ingin menugaskan sumber boleh tempah kepada tugas, ahli pasukan sumber boleh tempah mesti mempunyai tempahan tersedia yang secukupnya. Status tempahan mesti Buku Keras Jenis Ikat dan Komited Status. Jika tempahan tidak mencukupi untuk sumber, Project Service mengalih keluar tugasan dan memaparkan mesej ralat berikut:

*Tidak dapat menugaskan sumber ke tugas - Sumber berikut tidak mempunyai jam ditempah yang mencukupi terhadap projek*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Tempah sumber sebagai ahli pasukan dan kemudian tugaskan sumber kepada tugas

Dengan kaedah ini, anda menambah sumber kepada pasukan projek dan kemudian tugaskan tugas kepada sumber dalam jadual projek. Berikut adalah cara untuk melakukan ini:
1.  Pada grid ahli pasukan, tambah ahli pasukan baharu dengan memlih **Baharu**.
2.  Pada skrin Cipta Pantas Ahli Pasukan, pilih nama sumber boleh tempah dan tetapkan peranan.
3.  Pilih tarikh **Dari** dan **Sehingga**.

    > [!div class="mx-imgBorder"] 
    > ![Tangkapan skrin menambah ahli pasukan.](media/FAQ-Resources-to-Tasks2-1.png "Tangkapan skrin menambah ahli pasukan")
 
4.  Pilih satu daripada kaedah peruntukan berikut untuk tempahan sumber:
    - **Kapasiti Penuh** menempah kapasiti penuh sumber untuk tarikh dari dan sehingga yang dinyatakan.
    - **Kapasiti Peratusan** menempah sumber untuk peratusan kapasiti sumber bagi tarikh dari dan sehingga yang dinyatakan.
    - **Mengikut Jam Agihan Secara Rata** menempah sumber untuk bilangan jam yang dinyatakan, mengagihkan masa dengan sekata setiap hari selama tarikh dari dan sehingga.
    - **Mengikut Jam Muatan Depan** menempah sumber untuk bilangan jam yang dinyatakan, memuatkan depan masa setiap hari selama tarikh dari dan sehingga.

    Jangan pilih **Tiada** kerana ia menambah sumber kepada pasukan tetapi tidak mencipta sebarang tempahan yang menyerap kapasiti sumber.
5.  Pilih **Simpan**.

    Perhatian bahawa jam tempahan mesti cukup untuk meliputi jam usaha dan julat tarikh tugas yang anda tugaskan kepada sumber. Jika ia tidak sejajar, anda tidak boleh menugaskan sumber kepada tugas ini.

6.  Pada struktir pecahan kerja (WBS) untuk tugas, klik sel ke bawah sumber. Kemudian: 

    1. Pilih **Tambah**.
    2. Pilih ke bawah di bawah **Sumber** dan kemudian pilih ahli pasukan yang telah tambah di atas.
    3. Pilih **OK**. Ahli pasukan kini ditugaskan kepada kerja.

    > [!div class="mx-imgBorder"] 
    > ![Tangkapan skrin menambah sumber dengan WBS.](media/FAQ-Resources-to-Tasks2-2.png "Tangkapan skrin menambah sumber dengan WBS")
 
Pada grid ahli pasukan, anda akan lihat agregat jam ditugaskan sumber di bawah Jam Ditugaskan. Ia akan kurang daripada atau sama dengan jam ditempah untuk sumber. 

> [!div class="mx-imgBorder"] 
> ![Tangkapan skrin masa yang ditugaskan untuk sumber.](media/FAQ-Resources-to-Tasks2-3.png "Tangkapan skrin masa yang ditugaskan untuk sumber")
 
Jika tugas yang anda cuba untuk tugaskan kepada sumber bermula selepas tarikh akhir tempahan sumber, sumber tidak akan muncul dalam ke bawah.

Perhatian bahawa anda boleh menugaskans umber kepada lebih banyak jam berbanding jam ditempah mereka jika sumber mempunyai beberapa baki kapasiti tidak ditugaskan. Dalam kes ini, sumber hanya akan ditugaskan sebahagian kepada tempahan mereka. Anda boleh lihat baki jam tugas tidak ditugaskan dengan menambah Jam Tidak Bertugas kepada struktur pecahan kerja.

Jika sumber ditugaskan kepada jam ditempah mereka (jam ditempah mereka sama dengan jam ditugaskan mereka), anda akan nampak mesej ralat berikut semasa anda mencuba untuk menugaskan mereka tugas seterusnya:

*Tidak dapat menugaskan sumber ke tugas - Sumber berikut tidak mempunyai jam ditempah yang mencukupi terhadap projek.*

Tambahan, ahli pasukan projek lalai yang ditambah ke pasukan semasa anda mencipta projek ditambah tanpa sebarang tempahan dan tidak boleh ditugaskan kepada mana-mana tugas. Ia tidak akan muncul dalam ke bawah sumber untuk tugas.

Jika anda ingin menugaskan sumber ini, anda perlu mengalih keluar mereka daripada pasukan dan kemudian tambah semula mereka dengan kaedah peruntukan selain daripada Tiada. Sebab mereka ditambah ke pasukan di mana projek dicipta adalah supaya projek mempunyai sekurang-kurangnya satu pelulus projek secara lalai.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Cipta ahli pasukan generik melalui tugasan peranan pada tugas

Kaedah ini memastikan bahawa sumber mempunyai tempahan yang mencukupi untuk tugas. Pertama sekali, anda mencipta tempat atau sumber generik yang menerangkan perwatakan sumber yang dinamakan sehingga akhirnya anda ingin mengerjakan tugas dengan menjana pasukan selepas menugaskan peranan ke tugas. Berikut adalah cara untuk melakukan ini:

1. Pada struktur pecahan kerja, pilih tugas.
2. Pilih ikon ke bawah **Peranan Ditugaskan** dalam sel sumber.
3. Pilih ke bawah **Peranan** dan pilih peranan untuk sumber generik.
4. Pilih **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Tangkapan skrin menggunakan WBS untuk menambah sumber.](media/FAQ-Resources-to-Tasks2-4.png "Tangkapan skrin menggunakan WBS untuk menambah sumber")
 
Sebaik sahaja anda telah selesai menugaskan peranan kepada tugas dalam WBS, pilih **Jana Pasukan Projek**. Project Service mencipta bilangan minimum ahli pasukan generik berdasarkan pada peranan, sumber unit organisasi dan kalendar projek dengan mengagregat tugasan tugas.

> [!div class="mx-imgBorder"] 
> ![Tangkapan skrin menjana pasukan projek.](media/FAQ-Resources-to-Tasks2-5.png "Tangkapan skrin menjana pasukan projek")
 
Pada grid Ahli Pasukan, anda akan lihat sumber jenis Sumber Generik dengan nama peranan dan jawatan. Jika dua sumber diperlukan untuk peranan melengkapkan kerja, ciri Jana Pasukan mencipta dua ahli pasukan dan menggunakan nama jawatan untuk membezakannya.

> [!div class="mx-imgBorder"] 
> ![Tangkapan skrin menambah dua sumber generik.](media/FAQ-Resources-to-Tasks2-6.png "Tangkapan skrin menambah dua sumber generik")
 
Anda boleh membuka keperluan sumber sandaran untuk ahli pasukan generik dengan memilih pautan di bawah Keperluan sumber.

> [!div class="mx-imgBorder"] 
> ![Tangkapan skrin membuka keperluan sumber sokongan.](media/FAQ-Resources-to-Tasks2-7.png "Tangkapan skrin membuka keperluan sumber sokongan")

Pilih **Tempah** untuk sumber generik, dan kemudian anda boleh menggunakan papan jadual untuk mencari dan menempah sumber sebenar. Anda juga boleh menghantar keperluan untuk pemenuhan oleh pengurus sumber dengan memilih **Serah Permintaan**.

Apabila sumber generik dipenuhkan dengan sumber dinamakan, sumber generik dialih keluar daripada pasukan dan tugasan tugas untuk sumber generik ditugaskan kepada sumber dinamakan yang telah memenuhi keperluan sumber bagi sumber generik.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
