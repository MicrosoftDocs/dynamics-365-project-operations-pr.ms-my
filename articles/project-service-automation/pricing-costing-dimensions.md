---
title: Halaman utama dimensi penetapan harga dan kos
description: Topik ini memberikan gambaran keseluruhan dimensi penetapan harga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753887"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Halaman utama dimensi penetapan harga dan kos

Dimensi yang digunakan dalam sumber manusia untuk menyediakan penetapan harga dan kos terbahagi kepada dua kategori:

- Orang
- Kerja dirancang

Disebabkan ini, terdapat dua jenis nilai dimensi penetapan harga tersedia dalam Project Service Automation (PSA): 

- **Set pilihan** - Dimensi yang merupakan pengangkaan tetap bagi satu set nilai.
- **Nilai berasaskan entiti** - Dimensi yang boleh menjadi satu set nilai yang berbeza-beza.

## <a name="pricing-dimensions"></a>Dimensi penentuan harga

Kapal PSA dengan set dimensi penetapan harga lalai. Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**. Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah**, sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**. Ini akan membolehkan anda menyediakan harga dan kos untuk setiap peranan dan gabungan unit organisasi.

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jika anda telah menggunakan medan peranan siap guna dan unit organisasi sebagai dimensi penetapan harga sebelum versi 3 PSA, tidak akan ada perubahan yang dapat dilihat. Anda boleh terus menggunakan Project Service seperti biasa. 

Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai. Untuk mendapatkan maklumat lanjut, lihat topik berikut, walau bagaimanapun, sila ambil perhatian bahawa anda mesti melengkapkan prosedur dalam dalam pesanan yang disenaraikan di bawah:

- [Cipta medan dan entiti tersuai](create-custom-fields-entities.md)
- [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md)
- [Sediakan medan tersuai sebagai dimensi penetapan harga](set-up-pricing-dimensions.md)
- [Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Masa penetapan harga sumber manusia
Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi. Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.

Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda. Medan seperti **Kategori Transaksi** (**msdyn_transactioncategory**) dan **Sumber Boleh Ditempah** (**bookableresource**) ialah contoh dimensi calon. 

Anda juga perlu mempertimbangkan sama ada dimensi penetapan harga anda mestilah jadual atau set pilihan. Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda boleh mencipta entiti dan bukannya set pilihan. Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru ke jadual boleh dilakukan oleh kebanyakan pengguna.

Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki. Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong. Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.

**Sampel kadar bil**

| Peranan        | Unit Organisasi    |Unit      |Harga      |Mata Wang  |
| ------------|-------------|----------|----------:|----------|
| Pembangun   | Contoso AS  |Hour | 200|USD     |
| Pembangun   | Contoso India |Hour|   112|USD     |


**Sampel kadar kos**

| Jalur Gaji     | Unit Organisasi    |Unit      |Harga      |Mata Wang  |
| ----------------|-------------|----------|----------:|----------|
| Syarikat saya_Jalur1 | Contoso AS  |Hour | 145|USD     |
| Syarikat saya_Jalur2 | Contoso India |Hour|   67|USD     |
