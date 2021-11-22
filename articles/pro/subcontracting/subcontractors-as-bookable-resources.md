---
title: Sediakan subkontraktor sebagai sumber yang boleh ditempah
description: Topik ini menerangkan cara untuk menyediakan dan menyenggara sumber subkontraktor yang dicipta daripada pengguna dan kenalan dalam sistem, supaya ia boleh dikaitkan dengan subkontrak dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994197"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Sediakan subkontraktor sebagai sumber yang boleh ditempah

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Ikut langkah-langkah ini untuk menyediakan subkontraktor sebagai sumber yang boleh ditempah dalam Microsoft Dynamics 365 Project Operations.

1. Pergi ke **Projek** \> **Sumber**, dan pilih **Baharu**.
2. Pada halaman **Sumber Boleh Ditempah Baharu**, dalam medan **Jenis Sumber**, pilih salah satu pilihan berikut:

    - **Pengguna** – Pilih jenis sumber ini jika subkontraktor mesti mengakses Project Operations untuk memasukkan masa atau perbelanjaan. Jika anda memilih **Pengguna**, subkontraktor memerlukan lesen yang sah untuk mengakses sistem.
    - **Kenalan** atau **Akaun** – Pilih salah satu jenis sumber ini jika subkontraktor tidak memerlukan akses kepada Project Operations, tetapi mesti tersedia untuk penugasan tugas atau tempahan pada projek. Kedua-dua jenis sumber ini tidak menyediakan akses kepada sistem. Pilih **Akaun** untuk mewakili syarikat vendor sebagai sumber yang boleh ditempah. Pilih **Kenalan** untuk mewakili pekerja individu vendor.

3. Bergantung pada jenis sumber yang anda pilih, anda diminta untuk memilih pengguna, akaun, atau rekod kenalan yang sesuai.
4. Dalam medan **Jenis Pekerja**, pilih "Pekerja kontrak" untuk menetapkan subkontraktor sebagai sumber yang boleh ditempah.

    > [!NOTE]
    > Jika anda biarkan medan **Jenis Pekerja** kosong, sumber yang boleh ditempah akan dianggap sebagai pekerja.

5. Jika anda pilih **Pekerja Kontrak** sebagai jenis pekerja, pilih vendor yang sumber tersebut bekerja untuknya.
6. Pilih zon waktu sumber, dan kemudian pilih **Simpan**. Untuk menugaskan templat waktu kerja kepada sumber yang boleh ditempah, anda boleh memilih **Tetapkan kalendar** pada halaman senarai **Sumber Boleh Ditempah**.

Untuk dikaitkan dengan baris subkontrak, sumber yang boleh ditempah mesti memenuhi syarat-syarat berikut:

- Sumber yang boleh ditempah mestilah pekerja kontrak.
- Sumber yang boleh ditempah bagi jenis sumber **Kenalan** mesti dikaitkan dengan akaun vendor sebagai kenalan. Sumber yang boleh ditempah bagi jenis sumber **Pengguna** tidak perlu dikaitkan dengan akaun vendor sebagai kenalan.
- Nilai bagi medan **Vendor** untuk sumber yang boleh ditempah mesti sepadan dengan nilai medan **Vendor** untuk subkontrak.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Kemas kini jenis pekerja dan pemetaan vendor untuk sumber yang boleh ditempah

Medan **Jenis pekerja** untuk sumber yang boleh ditempah menentukan sama ada sumber yang boleh ditempah ialah pekerja kontrak atau pekerja. Medan **Vendor** mentakrifkan akaun vendor yang dikaitkan dengan sumber yang boleh ditempah. Dengan mengaitkan sumber yang boleh ditempah dengan vendor sebagai kenalan, anda menunjukkan bahawa kenalan tersebut ialah pekerja syarikat vendor.

Jika medan **Jenis Pekerja** dan **Vendor** untuk sumber yang boleh ditempah diubah, perubahan tersebut mempengaruhi sebarang pengesahan masa depan pada rekod baru yang dicipta oleh sumber yang boleh ditempah itu, seperti entri masa. Walau bagaimanapun, perubahan tersebut tidak membatalkan rekod yang sedia ada.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]