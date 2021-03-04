---
title: Cipta penyelesaian untuk dimensi penentuan harga tersuai
description: Topik ini memberikan maklumat tentang cara mencipta penyelesaian untuk dimensi penentuan harga tersuai.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514007"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Cipta penyelesaian untuk dimensi penentuan harga tersuai

 _**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_ 

>[!IMPORTANT]
>Semua perubahan dimensi penetapan harga tersuai hendaklah dalam penyelesaian yang berasingan. Amalan terbaik yang penting ini membolehkan fleksibiliti untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, membantu dengan menggunakan semula kerja anda dan dan menjadikan ia lebih mudah untuk port perubahan ini kepada tika lain. Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai penyelesaian **Terurus** dan kemudian import ke dalam tika lain untuk penggunaan semula.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Cipta penyelesaian untuk dimensi penentuan harga tersuai

1.  Pilih **Tetapan** > **Penyelesaian**, dan kemudian pilih **Baharu**.
2.  Namakan penyelesaian, *Dimensi penentuan harga <your organization name>*.
3. Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.

  ![Penciptaan penyelesaian dimensi penentuan harga tersuai](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambah semua entiti yang diperlukan dan dokumen berkaitan pada penyelesaian dimensi Penetapan Harga

Tambah entiti Project Service yang berikut kepada penyelesaian penentuan harga anda untuk membuat perubahan skema yang penting dalam penyelesaian penentuan harga. Selepas anda melengkapkan prosedur ini, entiti akan mengenali dimensi penentuan harga baharu.

1.  Pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **dimensi penentuan harga <*nama organisasi anda*>**.
2.  Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.
3.  Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:
 
   - **Sebenar**
   - **Sumber Boleh Ditempah**
   - **Garisan Anggaran**
   - **Tugas Projek**
   - **Butiran Baris Invois**
   - **Garisan Jurnal**
   - **Butiran Baris Kontrak Projek**
   - **Ahli Pasukan Projek**
   - **Butiran Baris Sebut Harga**
   - **Tokokan Harga Peranan**
   - **Harga Peranan**
   - **Entri Masa**
 
   ![Tambah entiti sedia ada untuk penyelesaian dimensi penentuan harga tersuai](./media/Existing-entities-to-PD-solution.png)
 
 4. Bagi setiap entiti, semak komponen yang ditambah dan senarai akhir aset entiti untuk setiap entiti. 

   >[!NOTE]
   > Sertakan semua borang dan pandangan bagi setiap entiti yang dipilih.

  ![Entiti ditambah](./media/solution-component-selection.png)


5.  Apabila digesa untuk menyertakan sebarang entiti sandaran untuk entiti yang dipilih, pilih **Tidak, jangan sertakan komponen diperlukan.**

    ![Termasuk entiti sandaran](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]