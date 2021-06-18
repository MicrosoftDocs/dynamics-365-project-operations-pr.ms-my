---
title: Halaman utama dimensi penetapan harga dan kos
description: Topik ini memberikan gambaran keseluruhan dimensi penetapan harga.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009267"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Halaman utama dimensi penetapan harga dan kos

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensi yang digunakan untuk menetapkan harga buruh dan kos dalam organisasi berasaskan projek dipengaruhi oleh atribut berikut:

- Orang yang melakukan kerja sama seperti pengalaman, peranan atau
- Kerja yang perlu dilakukan sama dengan kerumitan atau masa siang

Memandangkan sifat tipikal ini atribut kerja dan orang yang diperlukan untuk melaksanakan kerja, terdapat dua jenis nilai dimensi penetapan harga yang tersedia dalam Project Service Automation: 

- **Set pilihan**: Atribut yang merupakan penghitungan tetap bagi set nilai.
- **Nilai berasaskan entiti** - Atribut yang boleh mempunyai pelbagai set nilai yang terhad tetapi boleh berubah dari semasa ke semasa.

## <a name="pricing-dimensions"></a>Dimensi penentuan harga

Kapal PSA dengan set dimensi penetapan harga lalai. Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**. Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah**, sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**. Ini akan membolehkan anda menyediakan harga dan kos untuk setiap peranan dan gabungan unit organisasi.

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jika anda telah menggunakan medan peranan siap guna dan unit organisasi sebagai dimensi penetapan harga sebelum versi 3 PSA, tidak akan ada perubahan yang dapat dilihat. Anda boleh terus menggunakan Project Service seperti biasa. 

Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai. Untuk mendapatkan maklumat lanjut, lihat topik berikut, walau bagaimanapun, sila ambil perhatian bahawa anda mesti melengkapkan prosedur dalam dalam pesanan yang disenaraikan di bawah:

- [Cipta medan dan entiti tersuai](create-custom-fields-entities.md)
- [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md)
- [Sediakan medan tersuai sebagai dimensi penetapan harga ](set-up-pricing-dimensions.md)
- [Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Masa penetapan harga sumber manusia
Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi. Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.

Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda. Medan seperti **Kategori Transaksi** (**msdyn_transactioncategory**) dan **Sumber Boleh Ditempah** (**bookableresource**) ialah contoh dimensi calon. 

Pertimbangkan sama ada dimensi penetapan harga anda mesti jadual atau set pilihan. Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan ke atas nilai ini, cipta entiti dan bukannya set pilihan. Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru pada jadual boleh dilakukan oleh kebanyakan pengguna perniagaan.

Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki. Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong. Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.

**Sampel kadar bil**

| Peranan        | Unit Organisasi    |Unit      |Harga      |Mata wang  |
| ------------|-------------|----------|----------:|----------|
| Pemaju   | Contoso AS  |Jam | 200|USD     |
| Pemaju   | Contoso India |Jam|   112|USD     |


**Sampel kadar kos**

| Jalur Gaji     | Unit Organisasi    |Unit      |Harga      |Mata wang  |
| ----------------|-------------|----------|----------:|----------|
| Syarikat saya_Jalur1 | Contoso AS  |Jam | 145|USD     |
| Syarikat saya_Jalur2 | Contoso India |Jam|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]