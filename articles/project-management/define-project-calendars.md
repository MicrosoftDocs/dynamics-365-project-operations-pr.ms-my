---
title: Takrifkan kalendar projek
description: Topik ini menyediakan maklumat tentang cara menggunakan templat kalendar ke projek untuk menjejak jadual projek.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981311"
---
# <a name="define-project-calendars"></a>Takrifkan kalendar projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Untuk mencipta dan mengurus projek, anda mesti menggunakan templat kalendar ke projek. Templat kalendar mentakrifkan atribut projek berikut:

- Waktu bekerja termasuk masa mula dan masa tamat
- Hari bekerja
- Pengecualian kalendar seperti hari tidak bekerja

Templat kalendar yang digunakan ke projek ialah salinan templat kalendar yang ditakrifkan dalam tetapan organisasi anda.

> [!NOTE]
> Jika anda menukar templat kalendar, perubahan itu tidak tersebar ke waktu kerja projek. Untuk menukar waktu kerja projek, templat baharu mesti digunakan.

Untuk mencipta templat kalendar bagi organisasi anda, terdapat dua keperluan utama:

- Takrifkan waktu kerja yang dikehendaki bagi templat menggunakan sumber boleh ditempah baharu atau sedia ada.
- Cipta templat kalendar baharu dan kaitkan templat dengan sumber oleh ditempah.

**Takrif waktu bekerja bagi templat**

1. Pergi ke **Sumber** \> **Sumber**.
2. Cipta sumber baharu untuk dirujuk dalam templat kalendar atau pilih sumber sedia ada.
3. Pilih tab **Waktu Kerja** bagi sumber dan lengkapkan arahan dalam [Tetapkan waktu kerja untuk sumber](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) untuk mengkonfigurasikan peraturan kalendar.

**Cipta templat kalendar baharu**

1. Pergi ke **Tetapan** \> **Templat Kalendar**.
2. Pilih **Baharu** dan masukkan nama, perihalan dan sumber templat.

> [!NOTE]
> Apabila sumber dirujuk dalam templat kalendar, salinan kalendar sumber dikaitkan dengan templat kalendar. Jika waktu bekerja bagi templat yang disalin berubah, perubahan itu tidak tersebar ke templat kalendar.

Kini anda boleh mengaitkan templat kerja dengan templat kalendar projek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

