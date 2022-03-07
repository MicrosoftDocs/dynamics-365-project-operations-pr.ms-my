---
title: Nyahaktifkan senarai harga
description: Topik ini menerangkan cara menyahaktifkan atau mengalih keluar senarai harga yang tidak digunakan atau lama.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aca58eed2a0ee5e108d40636529802a7feec5b8dd060ba6c0eabc6d0b92b2e2f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997662"
---
# <a name="deactivate-price-lists"></a>Nyahaktifkan senarai harga 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Untuk mengalih keluar senarai harga yang lama atau tidak digunakan daripada Dynamics 365 Project Operations, terdapat dua langkah yang mesti anda lengkapkan. 

1. Alih keluar atau padamkan senarai harga daripada halaman tertentu.
2. Nyahaktifkan atau padamkan senarai harga daripada Senarai harga aktif pada halaman **Senarai Harga**.

>[!IMPORTANT]
> Anda mesti melengkapkan kedua-dua langkah untuk mengalih keluar senarai harga sepenuhnya. Hanya melakukan langkah 2, iaitu memadam atau menyahaktifkan senarai harga secara terus daripada pandangan Senarai Harga Aktif, tidak mencukupi. Anda juga mesti memadamkan perkaitan senarai harga ini daripada semua tempat yang dinyatakan dalam langkah 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Padamkan senarai harga daripada halaman tertentu
1. Untuk memadamkan senarai harga daripada Project Operations, pergi ke halaman berikut:  

      - Halaman **Parameter projek** > tab **Senarai Harga**
      - Halaman **Unit Organisasi** > grid **Senarai Harga**
      - Halaman **Akaun** > grid **Senarai Harga Projek**
      - Halaman **Sebut Harga Projek** > grid **Senarai Harga Projek**: Ini digunakan pada semua sebut harga projek aktif.
      - Halaman **Kontrak Projek** > grid **Senarai Harga Projek**: Ini digunakan pada semua kontrak projek aktif.

 2. Untuk setiap halaman, anda perlu memilih senarai harga yang anda mahu padamkan, dan kemudian pilih **Padam**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Padamkan atau nyahaktifkan senarai harga daripada halaman Senarai Harga
 
1. Untuk memadamkan senarai harga daripada senarai harga aktif, pergi ke **Jualan** > **Pelanggan** > **Senarai Harga**. 
2. Pilih senarai harga yang anda mahu padamkan untuk memadamkan dan kemudian pilih **Padam**. Jika senarai harga dirujuk pada sebarang transaksi sedia ada, anda tidak akan dapat memadamkannya. Jika ini berlaku, anda boleh menyahaktifkan senarai harga supaya ia tidak muncul dalam sebarang pandangan. 
3. Untuk menyahaktifkan senarai harga, pilih senarai harga sekali lagi, dan kemudian pilih **Nyahaktifkan**.   
