---
title: Cipta medan dan entiti tersuai sebagai dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang cara mencipta set pilihan atau entiti tersuai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898272"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Cipta medan dan entiti tersuai sebagai dimensi penentuan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Lengkapkan langkah berikut pada bila-bila masa anda mahu mencipta set pilihan atau entiti tersuai.

> [!IMPORTANT]
> Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan. Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain. Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Cipta penyelesaian tersuai untuk dimensi penentuan harga
1. Pergi ke **Tetapan** > **Penyelesaian** dan, kemudian pilih **Baharu** untuk mencipta penyelesaian baharu. 
2. Namakan penyelesaian, **\<your organization name> dimensi penetapan harga**, masukkan baki maklumat yang diperlukan dan kemudian pilih **Simpan**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga

Dimensi penentuan harga boleh menjadi set pilihan atau entiti. Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda. Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berasaskan entiti

1. Pergi ke **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.
3. Pilih **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**. 
4. Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.


### <a name="option-set-based-dimensions"></a>Dimensi berasaskan set pilihan 
Anda boleh mencipta dua dimensi berasaskan set pilihan. Guna **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak** dan menggunakan **Jam Bekerja Sumber** dengan nilai **Biasa** dan **Lebih Masa** untuk mengenakan tokokan apabila kerja selesai.


1. Pergi ke **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**. 
3. Pilih **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian pilih **Simpan**.

## <a name="create-data-for-entity-based-dimensions"></a>Cipta data untuk dimensi berasaskan entiti

Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel. Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**. Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.

1. Pilih **Carian Lanjutan**, pilih entiti **Tajuk Standard** dan kemudian pilih **Keputusan**. Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.
2. Pilih **Baharu** dan dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian pilih **Simpan**.
3. Tutup borang. 
4. Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tambah semua entiti yang diperlukan dan dokumen berkaitan ke Penyelesaian Dimensi Penetapan Harga
Anda perlu menambah entiti berikut ke penyelesaian penetapan harga anda. Guna langkah-langkah dalam prosedur untuk membuat perubahan penting dalam penyelesaian penentuan harga agar entiti maklum dengan dimensi penentuan harga baharu.

1. Pilih **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.
3. Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:

  - Sebenar
  - Sumber Boleh Ditempah
  - Garisan Anggaran
  - Butiran Baris Invois
  - Garisan Jurnal
  - Butiran Baris Kontrak Projek
  - Ahli Pasukan Projek
  - Butiran Baris Sebut Harga
  - Tokokan Harga Peranan
  - Harga Peranan 
  - Entri Masa 


> [!NOTE]
> Pastikan anda memasukkan semua borang dan pandangan bagi setiap entiti yang dipilih.

4. Apabila digesa untuk memasukkan sebarang entiti bersandar bagi entiti yang dipilih di atas, pilih **Tidak**.

