---
title: Jadualkan sumber untuk projek
description: Cara untuk menjadual sumber bagi projek dalam Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753979"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Jadualkan sumber bagi projek (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Anda boleh menyemak ketersediaan sumber untuk mendapatkan pandangan keseluruhan tentang cara sumber anda ditempah atau anda boleh menapis pandang mengikut kemahiran, pasukan, lokasi dan pilihan lain.  
  
Papan jadual menunjukkan senarai sumber dan ketersediaannya. Pilih mod pandangan untuk menunjukkan ketersediaan mengikut **Jam**, **Hari**, **Minggu** atau **Bulan**.  
  
Sebelum anda menggunakan papan jadual, penting untuk menyediakannya. Untuk maklumat lanjut, lihat [Konfigurasikan papan jadual (Field Service atau Project Service Automation)](../field-service/configure-schedule-board.md).
  
Jika anda menggunakan versi lebih lama, untuk ketersediaan sumber, lihat [Lihat ketersediaan sumber.](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  Untuk menggunakan kefungsian penempahan papan jadual, geokod dan perkhidmatan lokasi, anda perlu menghidupkan peta.  
> 
> 1. Pada menu utama, pilih **Penjadualan Sumber** > **Pentadbiran**.  
> 2. Klik **Parameter penjadualan**.  
> 3. Buka rekod dan tatal ke bawah ke bahagian **Resource Scheduling Optimization**.  
> 4. Pada medan **Sambungkan ke Peta**, pilih **Ya**.  
> 5. Terima terma dan simpan rekod.  
> 6. Pada menu utama, pilih **Project Service** > **Papan jadual**. Dari sini, terdapat beberapa cara untuk menjadualkan secara manual keperluan penempahan. Pilih kaedah yang sesuai untuk anda.
  
## <a name="find-available-resources"></a>Cari sumber tersedia

1.  Daripada senarai **Keperluan Penempahan**, klik kanan pada penempahan tidak berjadual dan pilih satu daripada yang berikut:  
  
- Pilih **Cari ketersediaan - Sumber Semasa** untuk mencari sumber yang tersedia daripada senarai pada papan jadual.  
- Pilih **Cari ketersediaan - Semua Sumber**, untuk mencari sumber yang tersedia daripada sumber dalam sistem  
   > [!NOTE]
   >  Apabila anda melakukannya, penapis akan menunjukkan pilihan untuk keperluan penempahan yang dipilih.  
  
2. Apabila anda melihat slot yang tersedia, klik kanan pada slot masa pada papan jadual dan pilih **Tempah Di Sini**. Atau, seret dan lepas keperluan penempahan pada slot masa yang tersedia.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Tempah sumber menggunakan pandangan harian dan cari sumber yang sedang ditempah
  
1.  Pada papan jadual, pilih **Mod Pandangan** dan pilih **Hari**.  
  
    Ini menunjukkan pandangan grid bagi jumlah jam sumber ditempah setiap hari dan hari yang sumber tidak ditempah.  
  
2.  Klik nama sumber yang anda mahu tempah dan kemudian pilih **Tempah**.  
  
3.  Pada kotak dialog **Penempahan sumber (cipta)**, pilih projek yang anda mahu tempah sumbernya bersama dengan kaedah penempahan serta masa mula dan tamat.  
  
4.  Apabila anda telah selesai, pilih **Tempah**.  
  
## <a name="view-to-the-schedule-board"></a>Lihat papan jadual
  
1.  Pilih keperluan penempahan tidak berjadual daripada senarai di bawah.  
  
2.  Seret keperluan penempahan ke sumber/slot masa yang tersedia pada papan jadual.  
  
3.  Apabila anda telah selesai, pilih **Tempah**.  
  
### <a name="additional-resources"></a>Sumber tambahan  
 [Panduan pengurus sumber](../project-service/resource-manager-guide.md)
