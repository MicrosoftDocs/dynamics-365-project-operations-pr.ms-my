---
title: Gunakan API jadual Projek dengan Power Automate
description: Artikel ini memberikan aliran sampel yang menggunakan antara muka pengaturcaraan aplikasi (API) jadual Projek.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404461"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Gunakan API jadual Projek dengan Power Automate

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini menerangkan aliran sampel yang menunjukkan cara mencipta pelan projek lengkap dengan menggunakan Microsoft Power Automate, cara untuk mencipta Set Operasi dan cara mengemas kini entiti. Contoh menunjukkan cara mencipta projek, ahli pasukan projek, Set Operasi, tugas projek dan penugasan sumber. Artikel ini juga menjelaskan cara mengemas kini entiti dan melaksanakan Set Operasi.

Berikut ialah senarai lengkap langkah yang didokumenkan dalam aliran sampel dalam artikel ini:

1. [Cipta pencetus PowerApps](#1)
2. [Cipta projek](#2)
3. [Asalkan pemboleh ubah untuk ahli pasukan](#3)
4. [Cipta ahli pasukan generik](#4)
5. [Cipta Set Operasi](#5)
6. [Cipta baldi projek](#6)
7. [Asalkan pemboleh ubah untuk status pautan](#7)
8. [Asalkan pemboleh ubah untuk bilangan tugas](#8)
9. [Asalkan pemboleh ubah untuk ID tugas projek](#9)
10. [Lakukan sehingga](#10)
11. [Tetapkan tugas projek](#11)
12. [Cipta tugas projek](#12)
13. [Cipta penugasan sumber](#13)
14. [Kurangkan pemboleh ubah](#14)
15. [Namakan semula tugas projek](#15)
16. [Jalankan Set Operasi](#16)

## <a name="assumptions"></a>Anggapan

Artikel ini menganggap bahawa anda mempunyai pengetahuan asas tentang platform, aliran awan dan Antara Muka Pengaturcaraan Aplikasi (API) Jadual Projek Dataverse. Untuk maklumat lanjut, lihat bahagian [Rujukan](#references) kemudian dalam artikel ini.

## <a name="create-a-flow"></a>Cipta aliran

### <a name="select-an-environment"></a>Pilih persekitaran

Anda boleh mencipta aliran Power Automate dalam persekitaran anda.

1. Pergi ke <https://flow.microsoft.com> dan gunakan kelayakan pentadbir anda untuk mendaftar masuk.
2. Di sudut kanan atas, pilih **Persekitaran**.
3. Dalam senarai, pilih persekitaran tempat Dynamics 365 Project Operations dipasang.

### <a name="create-a-solution"></a>Cipta penyelesaian

Ikut langkah ini untuk mencipta [aliran sedar penyelesaian](/power-automate/overview-solution-flows). Dengan mencipta aliran sedar penyelesaian, anda boleh mengeksport aliran dengan lebih mudah untuk menggunakannya kemudian.

1. Dalam anak tetingkap navigasi, pilih **Penyelesaian**.
2. Pada halaman **Penyelesaian**, pilih **Penyelesaian baharu**.
3. Dalam kotak dialog **Penyelesaian baharu**, tetapkan medan yang diperlukan dan kemudian pilih **Cipta**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Langkah 1: Cipta pencetus PowerApps

1. Pada halaman **Penyelesaian**, pilih penyelesaian yang anda cipta dan kemudian pilih **Baharu**.
2. Dalam anak tetingkap sebelah kiri, pilih **Aliran awan** \> **Automasi** \> **Aliran awan** \> **Segera**.
3. Dalam medan **Nama aliran**, masukkan **Jadualkan Aliran Demo API**.
4. Dalam senarai **Pilih cara mencetuskan aliran ini**, pilih **Power Apps**. Apabila anda mencipta pencetus Power Apps, logik adalah mengikut kehendak anda sebagai penulis. Dalam artikel ini, biarkan parameter input kosong untuk tujuan ujian.
5. Pilih **Cipta**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Langkah 2: Cipta projek

Ikut langkah ini untuk mencipta projek sampel.

1. Dalam aliran yang anda cipta, pilih **Langkah baharu**.

    ![Menambah langkah baharu.](media/newstep.png)

2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.

    ![Memilih operasi.](media/chooseactiontab.png)

3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.

![Menamakan semula langkah.](media/renamestep.png)

4. Namakan semula langkah **Cipta Projek**.
5. Dalam medan **Nama Tindakan**, pilih **msdyn\_CreateProjectV1**.
6. Di bawah medan **msdyn\_subject**, pilih **Tambahkan kandungan dinamik**.
7. Pada tab **Ekspresi**, dalam medan fungsi, masukkan **Nama projek - utcNow()**.
8. Pilih **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Langkah 3: Asalkan pemboleh ubah untuk ahli pasukan

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **asalkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Asalkan ahli pasukan**.
5. Dalam medan **Nama**, masukkan **TeamMemberAction**.
6. Dalam medan **Jenis**, pilih **Rentetan**.
7. Dalam medan **Nilai**, masukkan **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Langkah 4: Cipta ahli pasukan generik

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Ahli Pasukan**.
5. Untuk medan **Nama Tindakan**, pilih **TeamMemberAction** dalam kotak dialog **Kandungan dinamik**.
6. Dalam medan **Parameter Tindakan**, masukkan maklumat parameter berikut.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Berikut ialah penjelasan tentang parameter:

    - **\@\@odata.type** – Nama entiti. Contohnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Kunci primer ID pasukan projek. Nilai ialah ungkapan pengecam unik sejagat (GUID).   ID dijana daripada tab ungkapan.

    - **msdyn\_project\@odata.bind** – ID projek bagi projek pemilikan. Nilai merupakan kandungan dinamik yang datang daripada respons langkah "Cipta projek". Pastikan anda memasukkan laluan penuh dan menambah kandungan dinamik antara kurungan. Tanda petikan diperlukan. Contohnya, masukkan **"/msdyn\_project(TAMBAH KANDUNGAN DINAMIK)"**.
    - **msdyn\_name** – Nama ahli pasukan. Contohnya, masukkan **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Langkah 5: Cipta Set Operasi

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Set Operasi**.
5. Dalam medan **Nama Tindakan**, pililh **msdyn\_CreateOperationSetV1** tindakan tersuai Dataverse.
6. Dalam medan **Perihalan**, masukkan **ScheduleAPIDemoOperationSet**.
7. Dalam medan **Projek**, masukkan **/msdyn\_projects(**.
8. Dalam kotak dialog **Kandungan dinamik**, pilih **msdyn\_CreateProjectV1Response ProjectId**.
9. Dalam medan **Projek**, masukkan **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Langkah 6: Cipta baldi projek

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **tambahkan baris baharu**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Baldi**.
5. Dalam medan **Nama Jadual**, pilih **Baldi Projek**.
6. Dalam medan **Nama**, masukkan **ScheduleAPIDemoBucket1**.
7. Untuk medan **Projek**, pilih **msdyn\_CreateProjectV1Response ProjectId** dalam kotak dialog **Kandungan dinamik**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Langkah 7: Asalkan pemboleh ubah untuk status pautan

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **asalkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Asalkan linkstatus**.
5. Dalam medan **Nama**, masukkan **linkstatus**.
6. Dalam medan **Jenis**, pilih **Integer**.
7. Dalam medan **Nilai**, masukkan **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Langkah 8: Asalkan pemboleh ubah untuk bilangan tugas

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **asalkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Asalkan Bilangan tugas**.
5. Dalam medan **Nama**, masukkan **bilangan tugas**.
6. Dalam medan **Jenis**, pilih **Integer**.
7. Dalam medan **Nilai**, masukkan **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Langkah 9: Asalkan pemboleh ubah untuk ID tugas projek

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **asalkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Asalkan ProjectTaskID**.
5. Dalam medan **Nama**, masukkan **bilangan tugas**.
6. Dalam medan **Jenis**, pilih **Rentetan**.
7. Untuk medan **Nilai**, masukkan **guid()** dalam pembina ungkapan.

## <a name="step-10-do-until"></a><a id="10"></a>Langkah 10: Lakukan sehingga

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan sehingga**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Tetapkan nilai pertama dalam pernyataan bersyarat kepada pemboleh ubah **bilangan tugas** daripada kotak dialog **Kandungan dinamik**.
4. Tetapkan syarat kepada **kurang daripada atau sama dengan**.
5. Tetapkan nilai kedua dalam pernyataan bersyarat kepada **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Langkah 11: Tetapkan tugas projek

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **tetapkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baharu, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Tetapkan Tugas Projek**.
5. Dalam medan **Nama**, pilih **msdyn\_projecttaskid**.
6. Untuk medan **Nilai**, masukkan **guid()** dalam pembina ungkapan.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Langkah 12: Cipta tugas projek

Ikut langkah ini untuk mencipta tugas projek yang mempunyai ID unik yang tergolong dalam projek semasa dan baldi projek yang anda cipta.

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Tugas Projek**.
5. Dalam medan **Nama Tindakan**, pilih **msdyn\_PssCreateV1**.
6. Dalam medan **Entiti**, masukkan maklumat parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Berikut ialah penjelasan tentang parameter:

    - **\@\@odata.type** – Nama entiti. Contohnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID unik tugas. Nilai sepatutnya ditetapkan kepada pemboleh ubah dinamik daripada **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projek bagi projek pemilikan. Nilai merupakan kandungan dinamik yang datang daripada respons langkah "Cipta projek". Pastikan anda memasukkan laluan penuh dan menambah kandungan dinamik antara kurungan. Tanda petikan diperlukan. Contohnya, masukkan **"/msdyn\_project(TAMBAH KANDUNGAN DINAMIK)"**.
    - **msdyn\_subject** – Apa-apa nama tugas.
    - **msdyn\_projectbucket\@odata.bind** – Baldi projek yang mengandungi tugas. Nilai merupakan kandungan dinamik yang datang daripada respons langkah "Cipta Baldi". Pastikan anda memasukkan laluan penuh dan menambah kandungan dinamik antara kurungan. Tanda petikan diperlukan. Contohnya, masukkan **"/msdyn\_projectbuckets(TAMBAH KANDUNGAN DINAMIK)"**.
    - **msdyn\_start** – Kandungan dinamik untuk tarikh mula. Sebagai contoh, esok akan diwakili sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Tarikh mula dijadualkan. Sebagai contoh, esok akan diwakili sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Tarikh akhir yang dijadualkan. Pilih tarikh pada masa hadapan. Contohnya, tentukan **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Status pautan. Sebagai contoh, masukkan **"192350000"**.

7. Untuk medan **OperationSetId**, pilih **msdyn\_CreateOperationSetV1Response** dalam kotak dialog **Kandungan dinamik**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Langkah 13: Cipta penugasan sumber

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Penugasan**.
5. Dalam medan **Nama Tindakan**, pilih **msdyn\_PssCreateV1**.
6. Dalam medan **Entiti**, masukkan maklumat parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Untuk medan **OperationSetId**, pilih **msdyn\_CreateOperationSetV1Response** dalam kotak dialog **Kandungan dinamik**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Langkah 14: Kurangkan pemboleh ubah

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **kurangkan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam medan **Nama**, pilih **bilangan tugas**.
4. Dalam medan **Nilai**, masukkan **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Langkah 15: Namakan semula tugas projek

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Namakan Semula Tugas Projek**.
5. Dalam medan **Nama Tindakan**, pilih **msdyn\_PssUpdateV1**.
6. Dalam medan **Entiti**, masukkan maklumat parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Untuk medan **OperationSetId**, pilih **msdyn\_CreateOperationSetV1Response** dalam kotak dialog **Kandungan dinamik**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Langkah 16: Jalankan Set Operasi

1. Dalam aliran, pilih **Langkah baharu**.
2. Dalam kotak dialog **Pilih operasi**, dalam medan carian, masukkan **lakukan tindakan yang tidak terikat**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah, pilih elipsis (**…**) dan kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Laksanakan Set Operasi**.
5. Dalam medan **Nama Tindakan**, pilih **msdyn\_ExecuteOperationSetV1**.
6. Untuk medan **OperationSetId**, pilih **msdyn\_CreateOperationSetV1Response OperationSetId** dalam kotak dialog **Kandungan dinamik**.

## <a name="references"></a>Rujukan

- [Gambaran keseluruhan cara menyepadukan aliran dengan Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](schedule-api-preview.md)
- [Gambaran keseluruhan aliran awan - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Gambaran keseluruhan aliran sedar penyelesaian - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
