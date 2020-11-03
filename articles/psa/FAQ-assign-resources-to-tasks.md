---
title: Tugaskan sumber kepada tugas
description: Topik ini memberikan maklumat tentang cara menugaskan sumber kepada tugas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081417"
---
# <a name="assign-a-resource-to-a-task"></a>Tugaskan sumber kepada tugas

Terdapat tiga cara untuk menugaskan sumber kepada tugas dalam Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Tempah sumber sebagai ahli pasukan, kemudian tugaskan sumber kepada tugas

Anda boleh menambah sumber kepada pasukan projek, kemudian tugaskan sumber kepada tugas dalam jadual projek.

1. Pada tab **Ahli Pasukan**. tambah ahli pasukan baharu dengan memilih **Baharu**. 

2. Panel **Cipta Pantas Ahli Pasukan** dibuka, di mana anda boleh memilih nama sumber boleh ditempah dan menetapkan peranan. 

    Pilih salah satu daripada kaedah peruntukan berikut untuk tempahan sumber?

    - **Kapasiti Penuh** menempah kapasiti penuh sumber untuk tarikh dari dan sehingga yang dinyatakan.
    - **Kapasiti Peratusan** menempah sumber untuk peratusan kapasiti sumber bagi tarikh dari dan sehingga yang dinyatakan.
    - **Mengikut Jam Mengagih Sama Rata** menempah sumber untuk jumlah jam tertentu, mengagihkan masa tersebut secara sama rata setiap hari selama tempoh tarikh dari dan tarikh hingga khusus.
    - **Mengikut Jam Muatan Depan** menempah sumber untuk bilangan jam yang dinyatakan, memuatkan depan masa setiap hari selama tarikh dari dan sehingga.
    - **Tiada** menambah sumber kepada pasukan tetapi tidak mencipta sebarang tempahan yang menyerap kapasiti mereka.

3. Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber, kemudian di bawah **Ahli Pasukan** , pilih ahli pasukan yang anda baharu tambah. 

> [!NOTE]
> Pada tab **Ahli Pasukan** dan **Penyesuaian** , sumber menunjukkan jam ditempah dan ditugaskan. Jam hendaklah sama, tetapi tidak diperlukan memandangkan tempahan dan tugasan tidaklah terlalu bergandingan. Tab **Penyesuaian** memberikan butiran kepada anda apabila ia berbeza, seperti apabila anda menugaskan sumber lebih jam berbanding yang anda telah tempah. Jika perlu, anda boleh membetulkan maklumat dengan melanjutkan tempahan sumber atau menukar tugasan.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Cipta ahli pasukan generik melalui tugasan tugas

Apabila anda mencipta ahli pasukan generik melalui tugasan tugas, anda mencipta pemegang ruang atau sumber generik yang menggambarkan sifat sumber bernama yang anda mahu menguruskan tugas tersebut. Kemudian, anda boleh menjana keperluan (atau menyerahkan permintaan menggunakan keperluan) yang digunakan untuk mencari dan menempah sumber bernama.

1. Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber.

2. Taipkan nama untuk berfungsi sebagai nama sumber pemegang ruang. Contohnya, Pengurus Program.

3. Pilih **Cipta** , dan dalam medan **Cipta Pantas Ahli Pasukan Projek** , tetapkan peranan untuk sumber generik.

4. Anda boleh teruskan menugaskan tugas kepada sumber pemegang ruang ini dengan memilih sumber pada **Pemilih Sumber** untuk tugas tersebut. Ia tersenarai di bawah **Ahli Pasukan**.

5. Apabila anda selesai menugaskan sumber generik, pilih sumber generik pada tab **Pasukan** , kemudian pilih **Jana Keperluan** untuk mencipta keperluan sumber untuk sumber generik.

6. Pilih **Tempah** untuk sumber generik. Kemudian, anda boleh menggunakan papan Jadual untuk mencari dan menempah sumber sebenar. Anda juga boleh menghantar keperluan untuk pemenuhan oleh pengurus sumber.

7. Apabila sumber generik dipenuhkan dengan sumber dinamakan, sumber generik dialih keluar daripada pasukan dan tugasan tugas untuk sumber generik ditugaskan kepada sumber dinamakan yang telah memenuhi keperluan sumber bagi sumber generik.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tugaskan sumber bernama dari senarai semua sumber boleh dtitempah

Anda boleh menggunakan kotak carian dalam **Pemilih Sumber** untuk mencari semua sumber boleh ditempah dan menugaskannya kepada tugas.

Sumber yang ditugaskan dengan cara ini ditambah kepada pasukan tanpa sebarang tempahan. Ini serupa dengan menambah ahli pasukan dan memilih Tiada sebagai kaedah peruntukan. Sumber dipaparkan dalam tab **Pasukan** dan **Penyesuaian** sebagai sumber yang mempunyai hanya tugasan dan defisit tempahan. Tempah mereka jika anda ingin menggunakan ketersediaan mereka.

1. Pada grid **Jadual** untuk tugas, pilih ikon **Sumber** dalam sel sumber.

2. Mula menaip nama. Hasil carian untuk nama dipaparkan dalam **Pemilih Sumber** di bawah **Sumber Lain**.

3. Pilih sumber yang anda mahu tugaskan kepada tugas.

