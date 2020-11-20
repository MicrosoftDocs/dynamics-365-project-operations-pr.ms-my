---
title: Cipta entri masa
description: Topik ini memberikan maklumat tentang cara untuk mencipta entri masa.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
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
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131294"
---
# <a name="create-time-entries"></a>Cipta entri masa

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dalam versi sebelumnya Dynamics 365 Project Service Automation, entri masa penyertaan telah dimasukkan pada setiap minggu. Dalam versi 3 Project Service Automation, penyertaan masa akan dimasukkan pada setiap hari. Namun, selepas beberapa penyertaan masa telah dicipta, anda boleh membuat atau menyalinnya secara pukal.

## <a name="create-a-time-entry"></a>Cipta entri masa

Ikuti langkah ini untuk mencipta entri masa.

1. Pada halaman **Entri Masa** , pilih **Baharu**.
2. Dalam kotak dialog **Cipta Pantas: Entri Masa**, masukkan tempoh masa penyertaan dalam minit, jam, atau hari. Tempoh mesti di masukkan dalam format berikut: *x* minit , *x* jam atau *x* hari. Jam dan hari boleh juga dimasukkan menggunakan nilai perpuluhan, seperti *x.x* jam atau *x.x* hari.
3. Pilih jenis kemasukan masa dan projek yang anda masukkan entri masa untuk anda.
4. Dalam medan **Tugas Projek**, cari tugas untuk entri masa ini.

    > [!NOTE]
    > Jika anda mencipta entri masa untuk tugas yang tidak ditugaskan kepada pengguna, dalam medan **Tugas Projek**, pilih butang **Carian**, pilih **Ubah Pandangan** dan kemudian pilih **Semua Tugas Projek Aktif** ke senarai semua tugas.

5. Masukkan perihalan, jika perihalan diperlukan dan kemudian pilih **Simpan dan Tutup.**

Selepas kemasukan masa dicipta dan disimpan, anda boleh mengeditnya dalam grid kemasukan masa. Grid entri masa menyokong dua format:

- Anda boleh masukkan penyertaan masa dalam **format hh:mm**. Format ini kemudian ditukar kepada jam dan fractions.
- Anda boleh masukkan jam dan pecahan secara langsung.

Perhatikan bahawa pecahan sejam tidak minit. Oleh itu, 1.5 jam mewakili 1 jam dan 30 minit. Peraturan yang sama diguna pakai untuk pecahan hari. Satu hari adalah 24 jam, dan 0.5 hari mewakili 12 jam.

## <a name="bulk-create-time-entries"></a>Cipta entri masa pukal

Selepas beberapa kali entri telah dicipta, anda boleh salin ia untuk mencipta entri masa tambahan dalam pukal.

1. Pada halaman **Entri Masa** , pilih **Salin Minggu**.
2. Dalam kumpulan medan **Dari Tempoh** dalam **Tarikh Mula** dan **Tarikh Akhir** tentukan julat tarikh untuk menyalin entri masa.
3. Dalam kumpulan medan **Ke Tempoh** dalam medan **Tarikh Mula**. tentukan tarikh untuk mencipta penyertaan masa.
4. Pilih **Salin** untuk mencipta salinan penyertaan masa yang sesuai dengan hari minggu yang ditentukan dalam kumpulan medan **Ke Tempoh**. Sebagai contoh, kemasukan masa untuk Isnin minggu lepas disalin ke hari Isnin minggu yang ditetapkan dalam kumpulan medan **Ke Tempoh**.

## <a name="import-data-for-time-entries"></a>Import data untuk entri masa

Anda boleh mengimport data daripada penempahan projek dan tugasan. Apabila anda mengimport data, anda boleh menentukan julat tarikh bagi penempahan untuk diimport dan kemudian secara eksplisit memilih penempahan yang sepatutnya dicipta sebagai **Draf** entiti masa.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Kumpul mengikut, isih, cari dan keupayaan menapis

Anda boleh mengumpulkan dan menapis entri masa dengan dimensi yang ditetapkan dalam lajur. Dalam medan **Kumpulkan dengan**, pilih dimensi yang akan digunakan untuk menapis entri masa. Anda juga boleh mengisih rekod kemasukan masa dalam urutan menaik atau menurun dengan menggunakan anak panah isih pada pengepala lajur. Selain itu, anda boleh menunjukkan atau menyembunyikan entri dengan memilih butang **Tapis** pada tajuk lajur dan kemudian, dalam kotak **Carian**, memasukkan teks yang sepatutnya digunakan untuk mencari penyertaan masa dengan nama projek, tugas projek, masa entri atau sumber.
