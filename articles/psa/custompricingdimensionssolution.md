---
title: Cipta penyelesaian tersuai untuk dimensi penentuan harga
description: Topik ini menerangkan cara untuk mencipta penyelesaian tersuai apabila membuat dimensi penetapan harga tersuai.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081237"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Cipta penyelesaian tersuai untuk dimensi penentuan harga

> [!IMPORTANT]
> Semua perubahan dimensi penetapan harga tersuai hendaklah dalam penyelesaian yang berasingan. Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain. Selepas anda membuat perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.

1. Pilih **Tetapan** > **Penyelesaian** , dan kemudian pilih **Baharu**. 
2. Namakan penyelesaian, **\<your organization name> dimensi penetapan harga** , masukkan baki maklumat yang diperlukan dan kemudian pilih **Simpan**.

> ![Mencipta penyelesaian tersuai untuk dimensi penentuan harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambah semua entiti yang diperlukan dan dokumen berkaitan pada penyelesaian dimensi Penetapan Harga
Anda perlu menambah entiti Project Service berikut pada penyelesaian penentuan harga anda. Lengkapkan langkah-langkah dalam prosedur ini untuk membuat perubahan penting dalam penyelesaian penentuan harga agar entiti maklum dengan dimensi penentuan harga baharu.

1. Pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.
3. Dalam kotak dialog **Komponen Penyelesaian** , pilih entiti berikut:

- Sebenar
- Sumber Boleh Ditempah
- Garisan Anggaran
- Tugas Projek
- Butiran Baris Invois
- Garisan Jurnal
- Butiran Baris Kontrak Projek
- Ahli Pasukan Projek
- Butiran Baris Sebut Harga
- Tokokan Harga Peranan
- Harga Peranan 
- Entri Masa 

> ![Tambah entiti sedia ada untuk penyelesaian dimensi penentuan harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen penyelesaian](media/Dimension-Components.png)

> [!NOTE]
> Pastikan anda memasukkan semua borang dan pandangan bagi setiap entiti yang dipilih.

4. Apabila digesa untuk memasukkan sebarang entiti bersandar bagi entiti yang dipilih, pilih **Tidak**.

> ![Jangan masukkan semua komponen berkaitan](media/Do-not-include-required.png)

