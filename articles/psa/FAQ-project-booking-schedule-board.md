---
title: Cipta tempahan projek daripada papan Jadual
description: Topik ini memberikan maklumat tentang cara mencipta tempahan projek daripada papan jadual.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286124"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Cipta tempahan projek daripada papan Jadual

[!include [banner](../includes/psa-now-project-operations.md)]

Anda boleh menempah sumber ke dalam projek secara terus dari tab **Pasukan** projek atau dengan menjana keperluan sumber daripada tugasan ahli pasukan generik dan kemudian mengisi keperluan yang dijana dengan ahli pasukan projek.

Anda juga boleh menempah sumber ke dalam projek secara terus dari papan Jadual. Terdapat tiga cara untuk melakukan ini:

- **Tempah dari keperluan sumber yang dijana:** Anda boleh menjana keperluan sumber selepas anda mencipta sumber generik dan menugaskan tugas dalam projek.

- **Tempah daripada keperluan utama:** Keperluan utama muncul pada papan Jadual pada tab **Projek**. 

- **Tempah dari keperluan sumber baharu:** Anda boleh mencipta keperluan sumber dari awal dan mengaitkannya dengan projek. Buka papan Jadual, keperluan sumber muncul pada tab **Buka Keperluan**.

## <a name="book-from-a-generated-resource-requirement"></a>Tempah daripada keperluan sumber yang dijana.

Anda boleh mencipta sumber generik dan menugaskannya satu atau lebih tugas dalam projek. Kemudian anda boleh menjana keperluan sumber daripada ahli pasukan generik. 

1.  Pada papan Jadual, sumber ini akan muncul pada tab **Keperluan Terbuka**. Anda mungkin perlu menggunakan penapis lajur pada grid jika anda ada banya keperluan terbuka. 

    ![Buka tab Keperluan pada papan Jsadual](media/FAQ-Project-Booking-Schedule-Board-1.png "Tangkap layar jadual tempahan dan tugasan")

2. Pilih keperluan. Tab **Cari Ketersediaan** akan muncul di bahagian atas baris dipilih.
 
3. Apabila anda memilih tab, mod Pembantu Jadual bagi papan Jadual dibuka dan kemudian menapis sumber tersedia yang memenuhi keperluan sumber. Selepas itu, anda boleh menempah sumber.

4. Anda juga boleh heret dan jatuhkan baris terpilih dari bawah papan Jadual pada sel sumber dalam grid di atas. Apabila anda lepaskannya, ia membuka panel **Cipta Tempahan Sumber** di sebelah kanan.

    Memilih **Tempah** menempah sumber ke dalam pasukan projek.

![Cipta panel Tempahan Sumber](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Tempah dari Keperluan Utama

Mencipta projek dalam Project Service secara automatik mencipta keperluan sumber yang dipanggil Keperluan Utama. Ini adalah keperluan kosong yang digunakan untuk menempah sumber dengan cepat menggunakan papan Jadual tanpa menjana keperluan atau mencipta dari awal. Disebabkan keperluan kosong, anda perlu menyatakan tarikh serta kaedah peruntukan dan jam, jika berkenaan. 

1. Untuk menempah sumber dengan Keperluan Utama, pada papan Jadual, pilih tab **Projek**. Anda mungkin perlu menggunakan penapis lajur ke atas lajur **Projek** jika anda ada banyak projek.

   ![Penapis lajur pada papan Jadual](media/FAQ-Project-Booking-Schedule-Board-2.png "Tangkap layar jadual tempahan dan tugasan")

2. Pilih keperluan yang hanya mempunyai nama projek sebagai namanya dan mempunyai tempoh sifar (0).

3. Pilih tab **Cari Ketersediaan** yang muncul pada baris. Anda juga boleh heret dan jatuhkan baris terpilih dari bawah papan Jadual pada sel sumber dalam grid di atas.

4. Disebabkan **Keperluan Utama** adalah keperluan kosong dengan tempoh sifar (0), anda perlu menetapkan tempoh pada panel **Cipta Tempahan Sumber** apabila memilih dan menempah sumber.

5. Anda juga boleh memilih **Keperluan Utama Projek** di bahagian bawah papan Jadual dan seret dan jatuhkannya pada sumber untuk menempahnya.
 
    Disebabkan **Keperluan Utama** adalah keperluan kosong yang mempunyai tempoh sifar (0), anda perlu menetapkan tempoh pada panel **Cipta Tempahan Sumber** apabila anda memilih dan menempah sumber.
 
    Apabila anda menempah sumber melalui **Keperluan Utama** pada papan Jadual, anda menambahnya kepada pasukan projek tanpa sebarang tugasan.
 
## <a name="book-from-a-new-resource-requirement"></a>Tempah daripada keperluan sumber baharu.
Lengkapkan langkah-langkah berikut untuk menempah daripada keperluan sumber baharu. 

1. Pergi ke **Keperluan Sumber**, kemudian pilih **Baharu** untuk mencipta keperluan sumber baharu.

2. Pada tab **Projek**, pilih projek untuk mengaitkan keperluan dengan projek.
 
    Pada papan Jadual, keperluan baharu ini ditunjukkan sebagai **Keperluan Terbuka** yang anda boleh isi.

3. Tempah sumber untuk menambahnya pada pasukan projek.

4. Setelah sumber ditempah, anda mesti menugaskan tugas secara manual.



[!INCLUDE[footer-include](../includes/footer-banner.md)]