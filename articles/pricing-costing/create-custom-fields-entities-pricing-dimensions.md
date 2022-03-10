---
title: Cipta medan dan entiti tersuai sebagai dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang cara mencipta set pilihan atau entiti tersuai.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 40a6a4173cb0e4d7ea5bcf24c8954fe9d7e079d1e9ecf4aac252b5133f12d3ff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003647"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Cipta medan dan entiti tersuai sebagai dimensi penentuan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Lengkapkan langkah berikut apabila anda mahu mencipta set pilihan atau entiti tersuai untuk menggunakan sebagai dimensi penentuan harga. Untuk mendapatkan maklumat lanjut, lihat [Gambaran keseluruhan dimensi penentuan harga](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Kami mengesyorkan agar anda membuat semua perubahan dimensi penentuan harga dalam penyelesaian berasingan. Amalan terbaik yang penting ini memberikan fleksibiliti pada masa depan untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan. Ini juga akan membantu dengan penggunaan semula kerja anda dan menjadikan ia lebih mudah untuk port perubahan ini kepada tika lain. Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan mengimport ke dalam tika lain untuk menggunakan semula persediaan penentuan harga anda.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Cipta medan tersuai dan seti pilihan dalam penyelesaian dimensi penentuan harga

Dimensi penentuan harga boleh menjadi set pilihan atau entiti. Kedua-duanya mesti dicipta dalam penyelesaian penentuan harga anda. Langkah-langkah dalam prosedur ini menerangkan cara mencipta dimensi berasaskan entiti dan dimensi berasaskan set pilihan.

### <a name="entity-based-dimensions"></a>Dimensi berasaskan entiti
Untuk mencipta dimensi berasaskan entiti, ikuti langkah ini:

1. Pergi ke **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti**.
3. Pilih **Baharu** untuk mencipta entiti baharu dipanggil **Tajuk Standard**. 
4. Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.

> ![Definisi entiti tajuk standard.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensi berasaskan set pilihan 
Anda boleh mencipta dua dimensi berasaskan set pilihan. 

- Gunakan **Lokasi Kerja Sumber** untuk menjejaki harga kerja lokasi **Rumah** dan kerja **Di Tapak**. 
- Gunakan **jam Kerja Sumber** dengan nilai **Biasa** dan **Kerja Lebih Masa** untuk menggunakan tokokan apabila kerja selesai.

Grafik berikut menyediakan pandangan dimensi **Lokasi Kerja Sumber**. 

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Lokasi Kerja Sumber.](media/Option-set-PD-called-Resource-Work-Location.png)

Grafik berikut menyediakan pandangan dimensi **Waktu Kerja Sumber**. 

> ![Dimensi penentuan harga berasaskan set pilihan dipanggil Jam Kerja Sumber.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Pergi ke **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Set Pilihan**. 
3. Pilih **Baharu** untuk mencipta set pilihan baharu, masukkan baki maklumat yang diperlukan, kemudian pilih **Simpan**.

## <a name="create-data-for-entity-based-dimensions"></a>Cipta data untuk dimensi berasaskan entiti

Anda boleh mencipta data untuk dimensi berasaskan entiti secara manual, atau menggunakan panggilan import atau perkhidmatan Microsoft Excel. Guna langkah-langkah dalam prosedur ini untuk mencipta dua jawatan standard **Jurutera Sistem** dan **Jurutera Sistem Kanan** daripada dimensi berasaskan entiti, **Jawatan Standard**. Jika data yang anda mahu cipta adalah kecil, seperti dalam contoh berikut, anda boleh menggunakan borang standard.

1. Pilih **Carian Lanjutan**.
2. Pilih entiti **Jawatan Standard** dan kemudian pilih **Hasil**. Semua baris dalam entiti **Jawatan Standard** akan ditunjukkan.
3. Pilih **Baharu** dan dalam medan **Nama**, masukkan "Jurutera Sistem" dan kemudian pilih **Simpan**.
4. Tutup halaman. 
5. Ulangi langkah 1 - 3 untuk mencipta jawatan lain untuk "Jurutera Sistem Kanan".

> ![Data Sampel untuk entiti Jawatan Standard.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]