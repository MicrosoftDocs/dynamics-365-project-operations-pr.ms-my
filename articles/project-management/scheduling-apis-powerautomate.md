---
title: Gunakan API jadual Projek dengan Power Automate
description: Artikel ini menyediakan aliran sampel yang menggunakan antara muka pengaturcaraan aplikasi jadual Projek (API).
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

Artikel ini menerangkan aliran sampel yang menunjukkan cara membuat pelan projek yang lengkap menggunakan Microsoft Power Automate, cara membuat Set Operasi dan cara mengemas kini entiti. Contoh menunjukkan cara mencipta projek, ahli pasukan projek, Set Operasi, tugas projek dan tugasan sumber. Artikel ini juga menerangkan cara mengemas kini entiti dan melaksanakan Set Operasi.

Berikut adalah senarai lengkap langkah-langkah yang didokumenkan dalam aliran sampel dalam artikel ini:

1. [Mencipta PowerApps pencetus](#1)
2. [Cipta projek](#2)
3. [Memulakan pemboleh ubah untuk ahli pasukan](#3)
4. [Buat ahli pasukan generik](#4)
5. [Mencipta Set Operasi](#5)
6. [Buat baldi projek](#6)
7. [Memulakan pemboleh ubah untuk status pautan](#7)
8. [Memulakan pemboleh ubah untuk bilangan tugas](#8)
9. [Memulakan pemboleh ubah untuk ID tugas projek](#9)
10. [Lakukan sehingga](#10)
11. [Mengesetkan tugas projek](#11)
12. [Mencipta tugas projek](#12)
13. [Cipta tugasan sumber](#13)
14. [Decrement pemboleh ubah](#14)
15. [Menamakan semula tugas projek](#15)
16. [Menjalankan Set Operasi](#16)

## <a name="assumptions"></a>Andaian

Artikel ini menganggap bahawa anda mempunyai pengetahuan asas tentang Dataverse platform, aliran awan dan Antara Muka Pengaturcaraan Aplikasi Jadual Projek (API). Untuk maklumat lanjut, lihat seksyen [Rujukan](#references) dalam artikel ini kemudian.

## <a name="create-a-flow"></a>Cipta aliran

### <a name="select-an-environment"></a>Pilih persekitaran

Anda boleh membuat Power Automate aliran di persekitaran anda.

1. Pergi ke <https://flow.microsoft.com>, dan gunakan kelayakan pentadbir anda untuk log masuk.
2. Di penjuru kanan atas, pilih **Persekitaran**.
3. Dalam senarai, pilih persekitaran tempat Dynamics 365 Project Operations dipasang.

### <a name="create-a-solution"></a>Cipta penyelesaian

Ikuti langkah ini untuk mencipta [aliran](/power-automate/overview-solution-flows) kesedaran penyelesaian. Dengan mencipta aliran kesedaran penyelesaian, anda boleh dengan lebih mudah mengeksport aliran untuk menggunakannya kemudian.

1. Dalam anak tetingkap navigasi, pilih **Penyelesaian**.
2. Pada halaman **Penyelesaian**, pilih **Penyelesaian baharu**.
3. Dalam kotak **dialog Penyelesaian** baru, setkan medan yang diperlukan kemudian pilih **Cipta**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Langkah 1: Buat PowerApps pencetus

1. Pada halaman **Penyelesaian**, pilih penyelesaian yang anda cipta, kemudian pilih **Baharu**.
2. Dalam anak tetingkap kiri, pilih **Cloud mengalirkan** \> **Aliran** \> **Awan Automasi** \> **Segera.**
3. Dalam medan **Nama** aliran, masukkan **Jadualkan Aliran** Demo API.
4. Dalam Pilih **cara mencetuskan senarai aliran** ini, pilih **Power Apps**. Apabila anda mencipta Power Apps pencetus, logik terpulang kepada anda sebagai pengarang. Dalam artikel ini, biarkan parameter input kosong untuk tujuan ujian.
5. Pilih **Cipta**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Langkah 2: Cipta projek

Ikuti langkah ini untuk mencipta projek sampel.

1. Dalam aliran yang anda cipta, pilih **Langkah baharu**.

    ![Menambah langkah baharu.](media/newstep.png)

2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.

    ![Memilih pengendalian.](media/chooseactiontab.png)

3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.

![Menamakan semula langkah.](media/renamestep.png)

4. Namakan semula langkah **Cipta Projek**.
5. Dalam medan **Nama** Tindakan, pilih **msdyn\_ CreateProjectV1**.
6. Di bawah medan **subjek msdyn\_, pilih** Tambah kandungan **dinamik**.
7. Pada tab **Ungkapan**, dalam medan fungsi, masukkan **Nama projek - utcNow()**.
8. Pilih **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Langkah 3: Memulakan pemboleh ubah untuk ahli pasukan

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, dalam medan carian, masukkan **mulakan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula ahli **pasukan Init langkah**.
5. Dalam medan **Nama**, masukkan **TeamMemberAction**.
6. Dalam medan **Jenis**, pilih **Rentetan**.
7. Dalam medan **Nilai**, masukkan **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Langkah 4: Buat ahli pasukan generik

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Cipta Ahli** Pasukan.
5. Untuk medan **Nama** Tindakan, pilih **TeamMemberAction** dalam kotak **dialog Kandungan** dinamik.
6. Dalam medan **Parameter** Tindakan, masukkan maklumat parameter berikut.

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

    Berikut adalah penjelasan mengenai parameter:

    - **\@\@ odata.type** – Nama entiti. Contohnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Kunci utama ID pasukan projek. Nilainya ialah ungkapan pengecam unik global (GUID).   ID dijana daripada tab ungkapan.

    - **projek\_ msdyn\@ odata.bind** – ID projek projek yang dimiliki. Nilai akan menjadi kandungan dinamik yang datang daripada tindak balas langkah "Buat Projek". Pastikan anda memasuki laluan penuh dan menambah kandungan dinamik antara tanda kurung. Tanda petikan diperlukan. Contohnya, masukkan **"/projek msdyn\_(ADD DYNAMIC CONTENT)"**.
    - **nama\_ msdyn**– Nama ahli pasukan. Contohnya, masukkan **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Langkah 5: Cipta Set Operasi

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Cipta Set** Operasi.
5. Dalam medan **Nama Tindakan, pilih** tindakan tersuai Msdyn **CreateOperationSetV1\_**.Dataverse
6. Dalam medan **Perihalan**, masukkan **ScheduleAPIDemoOperationSet**.
7. Dalam medan **Projek**, masukkan **/projek msdyn\_(**.
8. Dalam kotak **dialog Kandungan** dinamik, pilih **msdyn\_ CreateProjectV1Response ProjectId**.
9. Dalam medan **Projek**, masukkan **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Langkah 6: Buat baldi projek

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **tambah baris** baru. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Buat Baldi**.
5. Dalam medan **Nama** Jadual, pilih **Baldi** Projek.
6. Dalam medan **Nama**, masukkan **ScheduleAPIDemoBucket1**.
7. Untuk medan **Projek**, pilih **msdyn\_ CreateProjectV1Response ProjectId** dalam kotak **dialog Kandungan** dinamik.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Langkah 7: Memulakan pemboleh ubah untuk status pautan

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, dalam medan carian, masukkan **mulakan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Init linkstatus**.
5. Dalam medan **Nama**, masukkan **linkstatus**.
6. Dalam medan **Jenis**, pilih **Integer**.
7. Dalam medan **Nilai**, masukkan **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Langkah 8: Mulakan pemboleh ubah untuk bilangan tugas

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, dalam medan carian, masukkan **mulakan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Init Bilangan tugas**.
5. Dalam medan **Nama**, masukkan **bilangan tugas**.
6. Dalam medan **Jenis**, pilih **Integer**.
7. Dalam medan **Nilai**, masukkan **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Langkah 9: Memulakan pemboleh ubah untuk ID tugas projek

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih operasi**, dalam medan carian, masukkan **mulakan pemboleh ubah**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Init ProjectTaskID**.
5. Dalam medan **Nama**, masukkan **bilangan tugas**.
6. Dalam medan **Jenis**, pilih **Rentetan**.
7. **Untuk medan Nilai**, masukkan **panduan()** dalam pembina ungkapan.

## <a name="step-10-do-until"></a><a id="10"></a> Langkah 10: Lakukan sehingga

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **lakukan sehingga**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Setkan nilai pertama dalam pernyataan bersyarat kepada **bilangan pemboleh ubah tugas** daripada kotak **dialog Kandungan** dinamik.
4. Tetapkan syarat kepada **kurang daripada sama dengan**.
5. Setkan nilai kedua dalam pernyataan bersyarat kepada **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Langkah 11: Setkan tugas projek

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **pemboleh ubah** set. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah baru, pilih elipsis (**...**), kemudian pilih **Namakan Semula**.
4. Namakan semula langkah **Setkan Tugas** Projek.
5. Dalam medan **Nama**, pilih **msdyn\_ projecttaskid**.
6. **Untuk medan Nilai**, masukkan **panduan()** dalam pembina ungkapan.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Langkah 12: Mencipta tugas projek

Ikuti langkah ini untuk mencipta tugas projek yang mempunyai ID unik yang dimiliki oleh projek semasa dan baldi projek yang anda cipta.

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah itu, pilih elipsis (**...**), kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Tugas** Projek.
5. Dalam medan **Nama** Tindakan, pilih **msdyn\_ PssCreateV1**.
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

    Berikut adalah penjelasan mengenai parameter:

    - **\@\@ odata.type** – Nama entiti. Contohnya, masukkan **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – ID unik tugas itu. Nilai harus ditetapkan kepada pemboleh ubah dinamik daripada **msdyn\_ projecttaskid**.
    - **projek\_ msdyn\@ odata.bind** – ID projek projek yang dimiliki. Nilai akan menjadi kandungan dinamik yang datang daripada tindak balas langkah "Buat Projek". Pastikan anda memasuki laluan penuh dan menambah kandungan dinamik antara tanda kurung. Tanda petikan diperlukan. Contohnya, masukkan **"/projek msdyn\_(ADD DYNAMIC CONTENT)"**.
    - **subjek\_ msdyn**– Sebarang nama tugas.
    - **msdyn\_ projectbucket\@ odata.bind** – Baldi projek yang mengandungi tugas. Nilainya akan menjadi kandungan dinamik yang datang dari tindak balas langkah "Buat Baldi". Pastikan anda memasuki laluan penuh dan menambah kandungan dinamik antara tanda kurung. Tanda petikan diperlukan. Contohnya, masukkan **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ mula** – Kandungan dinamik untuk tarikh mula. Sebagai contoh, esok akan diwakili sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_ dijadual bermula** – Tarikh mula yang dijadualkan. Sebagai contoh, esok akan diwakili sebagai **"addDays(utcNow(), 1)"**.
    - **msdyn\_ dijadualkan** – Tarikh tamat yang dijadualkan. Pilih tarikh pada masa hadapan. Contohnya, tentukan **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Status pautan. Sebagai contoh, masukkan **"192350000"**.

7. **Untuk medan OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** dalam kotak **dialog Kandungan** dinamik.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Langkah 13: Cipta tugasan sumber

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah itu, pilih elipsis (**...**), kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Cipta Tugasan**.
5. Dalam medan **Nama** Tindakan, pilih **msdyn\_ PssCreateV1**.
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

7. **Untuk medan OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** dalam kotak **dialog Kandungan** dinamik.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Langkah 14: Decrement pemboleh ubah

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **pemboleh ubah penyahgaraman**. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam medan **Nama**, pilih **bilangan tugas**.
4. Dalam medan **Nilai**, masukkan **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Langkah 15: Menamakan semula tugas projek

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah itu, pilih elipsis (**...**), kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Namakan Semula Tugas** Projek.
5. Dalam medan **Nama** Tindakan, pilih **msdyn\_ PssUpdateV1**.
6. Dalam medan **Entiti**, masukkan maklumat parameter berikut.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Untuk medan OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response** dalam kotak **dialog Kandungan** dinamik.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Langkah 16: Jalankan Set Operasi

1. Dalam aliran, pilih **Langkah baru**.
2. Dalam kotak **dialog Pilih pengendalian**, dalam medan carian, masukkan **laksanakan tindakan** tidak terikat. Kemudian, pada tab **Tindakan**, pilih operasi dalam senarai keputusan.
3. Dalam langkah itu, pilih elipsis (**...**), kemudian pilih **Namakan semula**.
4. Namakan semula langkah **Laksanakan Set** Operasi.
5. Dalam medan **Nama** Tindakan, pilih **msdyn\_ ExecuteOperationSetV1**.
6. **Untuk medan OperationSetId**, pilih **msdyn\_ CreateOperationSetV1Response OperationSetId** dalam **kotak dialog Kandungan** Dynamid.

## <a name="references"></a>Rujukan

- [Gambaran keseluruhan cara mengintegrasikan aliran dengan Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan](schedule-api-preview.md)
- [Gambaran keseluruhan aliran awan - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Gambaran keseluruhan aliran kesedaran penyelesaian - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
