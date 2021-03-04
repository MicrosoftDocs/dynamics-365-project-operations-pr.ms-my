---
title: Gambaran keseluruhan dimensi penentuan harga
description: Topik ini memberikan maklumat tentang dimensi penetapan harga dalam Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650213"
---
# <a name="pricing-dimensions-overview"></a>Gambaran keseluruhan dimensi penentuan harga

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dimensi yang digunakan dalam sumber manusia untuk menyediakan penetapan harga dan kos terbahagi kepada dua kategori:

- Orang
- Kerja dirancang

Disebabkan ini, terdapat dua jenis nilai dimensi penetapan harga tersedia:

- **Set pilihan**: Dimensi yang merupakan penghitungan tetap bagi set nilai.
- **Nilai berasaskan entiti**: Dimensi yang boleh menjadi set nilai yang berbeza.

## <a name="pricing-dimensions"></a>Dimensi penentuan harga

Dynamics 365 Project Operations didatangkan dengan set dimensi penetapan harga lalai. Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**. Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah**, sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**. Anda boleh menyediakan harga dan kos untuk setiap peranan dan kombinasi unit organisasi dengan medan ini didayakan.

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai. Untuk maklumat lanjut, lihat topik yang berikut. 
  
  > [!NOTE]
  > Prosedur mesti dilengkapkan mengikut susunan yang disenaraikan.

1. [Cipta penyelesaian untuk dimensi penetapan harga tersuai](../sales/create-solution-custompd.md)
2. [Cipta medan dan entiti tersuai](create-custom-fields-entities-pricing-dimensions.md)
3. [Tambah medan tersuai kepada persediaan harga dan entiti transaksi ](add-custom-fields-price-setup-transactional-entities.md)
4. [Sediakan medan tersuai sebagai dimensi penetapan harga ](set-up-custom-fields-pricing-dimensions.md)
5. [Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Masa penetapan harga sumber manusia
Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi. Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.

Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda. Medan seperti **Kategori Transaksi** (**msdyn_transactioncategory**) dan **Sumber Boleh Ditempah** (**bookableresource**) ialah contoh dimensi calon. 

Pertimbangkan sama ada dimensi penetapan harga anda mesti jadual atau set pilihan. Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda boleh mencipta entiti dan bukannya set pilihan. Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru ke jadual boleh dilakukan oleh kebanyakan pengguna.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]