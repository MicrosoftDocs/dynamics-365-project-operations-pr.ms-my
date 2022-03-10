---
title: Konfigurasikan integrasi Operasi Projek setiap entiti sah
description: Topik ini memberikan maklumat tentang penyediaan integrasi oleh entiti sah dalam Operasi Projek.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999417"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurasikan integrasi Operasi Projek setiap entiti sah 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini membimbing anda melalui langkah yang diperlukan untuk mengkonfigurasi Dynamics 365 Project Operations setiap entiti undang-undang.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dayakan kekunci ciri dalam Dynamics 365 Finance

Lengkapkan langkah-langkah berikut untuk mendayakan ciri yang diperlukan.

1. Dalam Dynamics 365 Finance, pergi ke ruang kerja **Pengurusan Ciri**.
2. Dalam **Senarai ciri**, cari dan dayakan ciri berikut:
  
    - **Dayakan berbilang baris kontrak untuk projek**
    - **Dayakan Operasi Projek pada Dynamics 365 Customer Engagement**

> [!NOTE]
> Jika anda tidak melihat **Kekunci ciri** yang disenaraikan, sahkan bahawa versi Kewangan anda memenuhi keperluan versi minimum (versi aplikasi 10.0.13 dengan semua kemas kini kualiti digunakan atau lebih tinggi). Pilih **Semak kemas kini** untuk menyegarkan semula senarai ciri.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Takrifkan senario pelaksanaan Operasi Projek untuk entiti sah

Anda boleh mendayakan Operasi Projek pada Dynamics 365 Customer Engagement pada peringkat entiti sah. Anda boleh mempunyai satu entiti sah yang menggunakan Operasi Projek pada Dynamics 365 Customer Engagement untuk senario berasaskan sumber/bukan stok. Dalam persekitaran yang sama, anda boleh mempunyai entiti sah lain yang menggunakan Operasi Projek untuk senario pesanan stok/pengeluaran.

1. Dalam Dynamics 365 Finance, pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Parameter pengurusan projek dan perakaunan global**.
2. Dalam senarai entiti sah yang tersedia, pilih entiti yang berbilang baris kontrak dan Operasi Projek pada ciri Dynamics 365 Customer Engagement akan didayakan. Biarkan entiti sah yang akan menggunakan Operasi Projek untuk senario pesanan stok/pengeluaran dinyahpilih.

> [!NOTE]
> Entiti sah boleh dipilih hanya jika ia tidak mempunyai sebarang projek sedia ada.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurasikan Parameter pengurusan projek dan perakaunan

Setiap entiti sah yang menggunakan Operasi Projek pada Dynamics 365 Customer Engagement memerlukan set parameter lalai. Parameter ini dikonfigurasikan pada tab **Operasi Projek** pada halaman **Parameter pengurusan projek dan perakaunan**. Parameter ialah:

  - **Jenis pengebilan lalai**: Operasi Projek menggunakan set tetap jenis pengebilan lalai yang mesti dipetakan kepada sifat baris Kewangan. Cipta rekod untuk setiap jenis pengebilan: **Tidak ditentukan**, **Boleh caj**, **Tidak boleh caj**, **Percuma** dan **Tidak tersedia**.
  - **Kategori projek lalai**: Pilih kategori projek lalai yang akan digunakan untuk setiap jenis transaksi. Kategori lalai ini akan digunakan dalam **Jurnal Integrasi Operasi Projek** dan dalam anggaran yang mana tiada kategori transaksi ditentukan untuk projek sebenar.
  - **Ramalan** : Pilih model ramalan untuk digunakan bagi anggaran masa dan perbelanjaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]