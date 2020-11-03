---
title: Cipta medan tersuai dan entiti
description: Topik ini menerangkan cara mencipta set pilihan dan entiti dalam penyelesaian anda sendiri dalam platform Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081297"
---
# <a name="create-custom-fields-and-entities"></a>Cipta medan tersuai dan entiti 

Lengkapkan langkah-langkah berikut pada bila-bila masa anda mahu mencipta set pilihan atau entiti tersuai pada platform Power Apps.  
Prosedur dalam topik ini hendaklah diselesaikan menggunakan antara muka web Project Service Automation (PSA).

> [!IMPORTANT]
> Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan. Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain. Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga

Dimensi penentuan harga boleh menjadi set pilihan atau entiti. Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda. Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berasaskan entiti

1. Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**.
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.
3. Klik **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**. Masukkan baki maklumat diperlukan, kemudian klik **Simpan**.

> ![Definisi entiti tajuk standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensi berasaskan set pilihan 
Anda boleh mencipta dua dimensi berasaskan set pilihan. Guna **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak** dan menggunakan **Jam Bekerja Sumber** dengan nilai **Biasa** dan **Lebih Masa** untuk mengenakan tokokan apabila kerja selesai.


1. Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**. 
3. Klik **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian klik **Simpan**.

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Lokasi Kerja Sumber ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Waktu Kerja Sumber ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Cipta data untuk dimensi berasaskan entiti

Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel. Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**. Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.

1. Dalam PSA, klik **Carian Lanjutan**. Pilih entiti **Jawatan Standard** dan kemudian klik **Hasil**. Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.
2. Klik **Baharu**. Dalam medan **Nama** , masukkan "Jurutera Sistem" dan kemudian klik **Simpan**.
3. Tutup borang. 
4. Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".

> ![Data Sampel untuk entiti Jawatan Standard ](media/ST-data.png)

