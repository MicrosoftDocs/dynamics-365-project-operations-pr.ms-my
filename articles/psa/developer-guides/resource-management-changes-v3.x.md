---
title: Perubahan pengurusan sumber (Project Service Automation 3.x)
description: Artikel ini memberikan maklumat tentang perubahan pada kawasan pengurusan Sumber.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916023"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Perubahan pengurusan sumber (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Bahagian artikel ini memberikan maklumat mengenai perubahan yang telah dibuat kepada kawasan Dynamics 365 Project Service Automation pengurusan Sumber versi 3.x.

## <a name="project-estimates"></a>Anggaran projek

Selain daripada yang berasaskan entiti **msdyn\_projecttask** (**Tugas Projek**), anggaran projek adalah berdasarkan kepada entiti **msdyn\_resourceassignment** (**Tugasan sumber**). Tugasan sumber telah menjadi "sumber kebenaran" untuk penjadualan tugas dan penetapan harga.

## <a name="line-tasks"></a>Tugas talian

Dalam PSA 3. x, tugas talian adalah usang (ditamatkan). Tugasan sekarang menunjuk ke tugas keseluruhan bukan tugas talian.

Contoh berikut menunjukkan cara tugas yang dinamakan "Tugas Ujian" ditugaskan kepada ahli pasukan A dan B dalam versi awal PSA dan dalam PSA 3. x.

- **Sebelum PSA 3.x:**

    - Tugas ujian

        - Tugas ujian – Tugas talian 1

            - Tugasan ke A

        - Tugas ujian – Tugas talian 2

            - Tugasan ke B

- **PSA 3.x:**

    - Tugas ujian

        - Tugasan ke A
        - Tugasan ke B

## <a name="unassigned-assignment"></a>Tugasan yang tidak ditugaskan

Dalam PSA 3.x, tugasan yang tidak ditugaskan ialah tugasan yang ditugaskan kepada ahli pasukan yang **TIDAK** batal dan sumber **TIDAK**. Tugasan yang tidak ditugaskan boleh berlaku dalam beberapa senario:

- Jika tugas telah dicipta tetapi belum ditugaskan kepada mana-mana ahli pasukan, penyerahan tugas yang tidak ditugaskan sentiasa dicipta. 
- Jika semua penugas pada tugas dikeluarkan, tugasan yang tidak ditugaskan telah dicipta semula untuk tugas tersebut.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Medan penjadualan pada entiti Tugas Projek

Medan pada **entiti msdyn\_projecttask** telah ditamatkan atau dipindahkan ke entiti **msdyn\_resourceassignment** atau ia kini dirujuk daripada entiti **msdyn\_projectteam**(**Ahli Pasukan Projek**).

| Medan ditamatkan pada msdyn\_projecttask (Tugas projek) | Medan baharu tentang msdyn\_resourceassignment (Tugasan Sumber) | Komen |
|---|---|---|
| msdyn\_assignedresources | Tiada | |
| msdyn\_assignedteammembers | Tiada | |
| msdyn\_numberofresources | Tiada | |
| msdyn\_scheduledhours | Tiada | |
| msdyn\_effortcontour | msdyn\_plannedwork | Format struktur data Nota Objek JavaScript (JSON) yang disimpan dalam medan telah ditukar. |

## <a name="schedule-contour"></a>Jadual kontur

Kontur jadual tersebut disimpan dalam medan **Kerja Terancang** (**msdyn\_plannedwork**) bagi setiap entiti **Tugasan Sumber**(**msdyn\_sumber**).

### <a name="structure"></a>Struktur

Struktur baharu jadual kontur terdiri daripada hirisan masa fleksibel yang ditakrifkan untuk setiap hari jadual. Setiap hirisan masa mempunyai sifat berikut:

- **Mulakan** – Bermulanya waktu kerja untuk hari tersebut, mengikut kalendar projek.
- **Akhir** – Berakhirnya waktu kerja untuk hari tersebut, mengikut kalendar projek.
- **Jam** – Bilangan jam yang ditugaskan pada hari tersebut.

**Contoh**

Contoh ini menggunakan kalendar projek di mana hari kerja adalah dari jam 9 pagi hingga 5 petang dalam zon waktu UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Penjadualan automatik dan penjadualan manual

Jika tugas dijadualkan secara automatik, waktu yang dimuatkan depan dan tempoh tugas mungkin dikurangkan.

**Contoh**

Tugas berikut adalah dijadualkan secara automatik selama 18 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Jika sesuatu tugas dijadualkan secara manual, waktu secara sekata diedarkan kepada semua tarikh.

**Contoh**

Tugas berikut adalah dijadualkan secara manual selama 18 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unit tugasan

Unit tugasan telah ditamatkan dalam PSA 3.x. Masa kerja kerja kini juga dibahagikan sama rata, setiap hari, antara semua sumber yang ditugaskan.

**Contoh**

Dalam contoh ini, tugas itu ditugaskan kepada dua sumber dan dijadualkan automatik untuk 36 jam untuk tiga hari (3 Disember, 2018, hingga 5 Disember, 2018).

- Tugasan 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Tugasan 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensi penentuan harga

Dalam PSA 3.x, medan dimensi penetapan harga khusus (seperti **Peranan** dan **Unit Organisasi**) telah dialih keluar daripada entiti **msdyn\_projecttask**. Medan ini kini boleh diambil daripada ahli pasukan projek yang berkaitan (**msdyn\_projectteam**) daripada tugasan sumber (**msdyn\_resourceassignment**) apabila anggaran projek dijana. Medan baharu, **msdyn\_organizationalunit**, telah ditambah kepada entiti **msdyn\_projectteam**.

| Medan ditamatkan pada msdyn\_projecttask (Tugas projek) | Medan daripada msdyn\_projectteam (Ahli Pasukan Projek) yang digunakan sebagai ganti |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontur

Penetapan harga dan penganggaran medan kontur telah ditamatkan pada entiti **msdyn\_projecttask**. Mereka telah dipindahkan ke entiti **msdyn\_resourceassignment**.

| Medan ditamatkan pada msdyn\_projecttask (Tugas projek) | Medan baharu tentang msdyn\_resourceassignment (Tugasan Sumber) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Medan berikut ditambah ke entiti **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Medan berikut untuk dirancang, sebenar dan baki kos dan jualan tidak berubah pada entiti **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
