---
title: Bagaimanakah saya menyesuaikan aliran proses perniagaan Project Stages?
description: Gambaran keseluruhan tentang cara menyesuaikan aliran proses perniagaan Peringkat Projek.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 7efbb19161878e13a1b0d33bc1bc4e06521445c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596981"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Bagaimanakah saya menyesuaikan aliran proses perniagaan Project Stages?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Terdapat pengehadan yang diketahui dalam versi awal aplikasi Project Service yang nama peringkat dalam aliran proses perniagaan Project Stages mesti betul-betul sepadan dengan nama Bahasa Inggeris yang dijangka (**Quote**, **Plan**, **Close**). Jika tidak, logik perniagaan, yang bergantung pada nama peringkat bahasa Inggeris, tidak berfungsi seperti yang diharapkan. Itulah sebabnya anda tidak melihat tindakan biasa seperti **Tukar Proses** atau **Edit Proses** tersedia pada borang projek dan menyesuaikan aliran proses perniagaan adalah tidak digalakkan. 

Had ini telah ditangani dalam versi 2.4.5.48 dan kemudian. Artikel ini menyediakan penyelesaian sementara yang dicadangkan jika anda perlu menyesuaikan aliran proses perniagaan lalai untuk versi terdahulu.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Logik perniagaan memerlukan padanan yang tepat dengan nama Bahasa Inggeris peringkat.

Aliran proses perniagaan Project Stages termasuk logik perniagaan yang mendorong tingkah laku yang berikut dalam aplikasi:
- Apabila projek dikaitkan dengan sebut harga, kod ini menetapkan aliran proses perniagaan kepada peringkat **Quote**.
- Apabila projek dikaitkan dengan kontrak, kod ini menetapkan aliran proses perniagaan kepada peringkat **Plan**.
- Apabila aliran proses perniagaan maju ke peringkat **Close**, rekod projek dinyahaktifkan. Apabila projek dinyahaktifkan, borang projek dan struktur pecahan kerja (WBS) ditetapkan kepada baca sahaja, tempahan sumber yang dinamakan dikeluarkan dan sebarang senarai harga yang berkaitan dinyahaktifkan.

Logik perniagaan ini bergantung pada nama Bahasa Inggeris untuk peringkat projek. Pergantungan pada nama Bahasa Inggeris peringkat ini adalah sebab utama penyesuaian aliran proses perniagaan Project Stages tidak digalakkan, serta sebab anda tidak dapat melihat tindakan aliran proses perniagaan biasa seperti **Tukar Proses** atau **Edit Proses** pada entiti projek.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Apakah yang akan berlaku jika nama peringkat tidak sepadan dengan nama Bahasa Inggeris?

Dalam aplikasi Project Service versi 1.x pada platform 8.2, apabila nama peringkat dalam aliran proses perniagaan tidak sepadan dengan tepat dengan nama Bahasa Inggeris, logik perniagaan yang menetapkan peringkat yang betul untuk sebut harga atau kontrak atau yang menutup projek itu telah dilangkau. Tiada mesej ralat dipaparkan. Oleh itu, nampaknya anda dapat menyesuaikan aliran proses perniagaan Project Stages. Walau bagaimanapun, anda tidak akan melihat sebarang proses automatik berfungsi untuk sebut harga, kontrak dan tutup projek.

Dalam versi aplikasi Project Service 2.4.4.30 atau lebih awal pada platform 9.0, terdapat perubahan seni bina yang ketara kepada aliran proses perniagaan yang memerlukan logik perniagaan aliran proses perniagaan ditulis semula. Akibatnya, jika nama peringkat proses tidak sepadan dengan nama Bahasa Inggeris yang dijangkakan, anda akan menerima mesej ralat. 

Oleh itu, jika anda mahu untuk menyesuaikan aliran proses perniagaan Project Stages bagi entiti projek, anda hanya boleh menambah peringkat baru kepada aliran proses perniagaan lalai bagi entiti projek, sambil mengekalkan peringkat **Quote**, **Plan** dan **Close** seadanya. Pengehadan ini memastikan yang anda tidak mendapat ralat daripada logik perniagaan yang menjangkakan nama Bahasa Inggeris peringkat dalam aliran proses perniagaan.

Dalam versi 2.4.5.48 atau kemudian, logik perniagaan yang diterangkan dalam artikel ini telah dikeluarkan dari aliran proses perniagaan lalai bagi entiti projek. Menaik taraf kepada versi itu atau kemudian akan membolehkan anda menyesuaikan atau menggantikan aliran proses perniagaan lalai dengan salah satu daripada aliran proses perniagaan anda sendiri. 

## <a name="workarounds-for-earlier-versions"></a>Penyelesaian untuk versi lebih awal

Jika menaik taraf bukan satu pilihan, anda boleh menyesuaikan aliran proses perniagaan Project Stages bagi entiti projek dalam satu daripada dua cara ini:

1. Tambah peringkat tambahan kepada konfigurasi lalai, sementara mengekalkan nama Bahasa Inggeris peringkat untuk **Quote**, **Plan** dan **Close**.


![Tangkapan skrin penambahan peringkat kepada konfigurasi lalai.](media/FAQ-Customize-BPF-1.png)
 
2. Cipta aliran proses perniagaan anda sendiri dan jadikannya aliran proses perniagaan utama bagi entiti projek yang membolehkan anda mempunyai sebarang nama peringkat yang anda inginkan. Walau bagaimanapun, jika anda mahu menggunakan standard peringkat projek **Quote**, **Plan** dan **Close** yang sama, anda perlu melakukan beberapa penyesuaian yang memaksa keluar nama peringkat tersuai anda. Logik yang lebih kompleks adalah dalam penutupan projek, yang anda masih boleh cetuskan dengan hanya menyahaktifkan rekod projek.

![Penyesuaian BPF.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Pertimbangan tambahan bagi aplikasi Project Service versi 2.4.4.30 atau lebih awal pada platform 9.0

Dalam Project Service 2.4.4.30 atau lebih awal pada platform 9.0, dengan aliran proses perniagaan tersuai, medan **Nama Peringkat** pada entiti projek yang digunakan dalam carta **Projek Mengikut Peringkat** dan pandangan senarai projek tidak akan kemas kini, kerana ia digandingkan kepada aliran proses perniagaan Project Stages lalai. Anda boleh mengemukakan isu ini dengan langkah-langkah berikut:

- Tambah medan tersuai untuk merekodkan peringkat aliran proses perniagaan semasa yang dikemas kini apabila pengguna maju menerusi aliran proses perniagaan tersuai.

- Ubah suai carta **Projek Mengikut Peringkat** untuk berfungsi dengan medan tersuai anda dan bukannya konfigurasi lalai.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Langkah-langkah untuk mencipta aliran proses perniagaan anda sendiri bagi entiti projek

Untuk mencipta aliran proses perniagaan anda sendiri bagi entiti projek, lakukan yang berikut:

1. Pergi ke **Tetapan** > **Pusat Proses**. Jangan menyalin aliran proses perniagaan Project Stages kerana itu turut menyalin logik perniagaan Project Service.

  ![Cipta proses.](media/FAQ-Customize-BPF-3.png)

2. Gunakan Pereka Proses untuk mencipta nama peringkat yang anda inginkan. Jika anda mahu fungsi yang sama sebagai peringkat lalai untuk **Quote**, **Plan** dan **Close**, anda perlu mencipta fungsi itu berdasarkan nama peringkat aliran proses perniagaan tersuai anda.

   ![Tangkapan skrin Pereka Proses yang digunakan untuk menyesuaikan BPF.](media/FAQ-Customize-BPF-4.png) 

3. Dalam Pereka Proses, klik **Aliran Proses Pesanan** untuk menjadikan aliran proses perniagaan tersuai sebagai aliran proses perniagaan utama bagi entiti projek dengan memindahkannya di atas aliran proses perniagaan Project Stages ke bahagian atas senarai.


   [Tangkap layar penggunaan Aliran Proses Pesanan](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Langkah-langkah berikut digunakan pada aplikasi Project Service 2.4.4.30 atau lebih awal pada platform 9.0

4. Tambah medan tersuai baru kepada entiti projek untuk merekodkan peringkat tersuai dalam aliran proses perniagaan tersuai anda. Anda perlu menambah logik perniagaan (plugin/aliran kerja) untuk mengemas kini medan ini apabila peringkat pada aliran proses perniagaan tersuai dikemas kini.

   ![Tangkapan skrin penyesuaian entiti Projek.](media/FAQ-Customize-BPF-6-720.png)

5. Ubah suai carta **Projek Mengikut Peringkat** untuk menggunakan medan tersuai baru anda bagi peringkat.

   ![Tangkapan skrin penggunaan carta Projek Mengikut Peringkat.](media/FAQ-Customize-BPF-7-720.png)

6. Ubah suai sebarang pandangan bagi entiti projek untuk memasukkan medan tersuai baru anda bagi peringkat.

   ![Tangkapan skrin pengubahsuaian pandangan pada entiti Projek.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
