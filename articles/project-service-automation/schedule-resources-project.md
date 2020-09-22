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
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="a3a94-103">Jadualkan sumber bagi projek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a3a94-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a3a94-104">Anda boleh menyemak ketersediaan sumber untuk mendapatkan pandangan keseluruhan tentang cara sumber anda ditempah atau anda boleh menapis pandang mengikut kemahiran, pasukan, lokasi dan pilihan lain.</span><span class="sxs-lookup"><span data-stu-id="a3a94-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="a3a94-105">Papan jadual menunjukkan senarai sumber dan ketersediaannya.</span><span class="sxs-lookup"><span data-stu-id="a3a94-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="a3a94-106">Pilih mod pandangan untuk menunjukkan ketersediaan mengikut **Jam**, **Hari**, **Minggu** atau **Bulan**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="a3a94-107">Sebelum anda menggunakan papan jadual, penting untuk menyediakannya.</span><span class="sxs-lookup"><span data-stu-id="a3a94-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="a3a94-108">Untuk maklumat lanjut, lihat [Konfigurasikan papan jadual (Field Service atau Project Service Automation)](../field-service/configure-schedule-board.md).</span><span class="sxs-lookup"><span data-stu-id="a3a94-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](../field-service/configure-schedule-board.md).</span></span>
  
<span data-ttu-id="a3a94-109">Jika anda menggunakan versi lebih lama, untuk ketersediaan sumber, lihat [Lihat ketersediaan sumber.](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="a3a94-109">If you are using an older version, for resource availability, see [View resource availability](../project-service/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="a3a94-110">Untuk menggunakan kefungsian penempahan papan jadual, geokod dan perkhidmatan lokasi, anda perlu menghidupkan peta.</span><span class="sxs-lookup"><span data-stu-id="a3a94-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="a3a94-111">Pada menu utama, pilih **Penjadualan Sumber** > **Pentadbiran**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="a3a94-112">Klik **Parameter penjadualan**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="a3a94-113">Buka rekod dan tatal ke bawah ke bahagian **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="a3a94-114">Pada medan **Sambungkan ke Peta**, pilih **Ya**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="a3a94-115">Terima terma dan simpan rekod.</span><span class="sxs-lookup"><span data-stu-id="a3a94-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="a3a94-116">Pada menu utama, pilih **Project Service** > **Papan jadual**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="a3a94-117">Dari sini, terdapat beberapa cara untuk menjadualkan secara manual keperluan penempahan.</span><span class="sxs-lookup"><span data-stu-id="a3a94-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="a3a94-118">Pilih kaedah yang sesuai untuk anda.</span><span class="sxs-lookup"><span data-stu-id="a3a94-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="a3a94-119">Cari sumber tersedia</span><span class="sxs-lookup"><span data-stu-id="a3a94-119">Find available resources</span></span>

1.  <span data-ttu-id="a3a94-120">Daripada senarai **Keperluan Penempahan**, klik kanan pada penempahan tidak berjadual dan pilih satu daripada yang berikut:</span><span class="sxs-lookup"><span data-stu-id="a3a94-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="a3a94-121">Pilih **Cari ketersediaan - Sumber Semasa** untuk mencari sumber yang tersedia daripada senarai pada papan jadual.</span><span class="sxs-lookup"><span data-stu-id="a3a94-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="a3a94-122">Pilih **Cari ketersediaan - Semua Sumber**, untuk mencari sumber yang tersedia daripada sumber dalam sistem</span><span class="sxs-lookup"><span data-stu-id="a3a94-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="a3a94-123">Apabila anda melakukannya, penapis akan menunjukkan pilihan untuk keperluan penempahan yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="a3a94-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="a3a94-124">Apabila anda melihat slot yang tersedia, klik kanan pada slot masa pada papan jadual dan pilih **Tempah Di Sini**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="a3a94-125">Atau, seret dan lepas keperluan penempahan pada slot masa yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="a3a94-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="a3a94-126">Tempah sumber menggunakan pandangan harian dan cari sumber yang sedang ditempah</span><span class="sxs-lookup"><span data-stu-id="a3a94-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="a3a94-127">Pada papan jadual, pilih **Mod Pandangan** dan pilih **Hari**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="a3a94-128">Ini menunjukkan pandangan grid bagi jumlah jam sumber ditempah setiap hari dan hari yang sumber tidak ditempah.</span><span class="sxs-lookup"><span data-stu-id="a3a94-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="a3a94-129">Klik nama sumber yang anda mahu tempah dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="a3a94-130">Pada kotak dialog **Penempahan sumber (cipta)**, pilih projek yang anda mahu tempah sumbernya bersama dengan kaedah penempahan serta masa mula dan tamat.</span><span class="sxs-lookup"><span data-stu-id="a3a94-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="a3a94-131">Apabila anda telah selesai, pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="a3a94-132">Lihat papan jadual</span><span class="sxs-lookup"><span data-stu-id="a3a94-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="a3a94-133">Pilih keperluan penempahan tidak berjadual daripada senarai di bawah.</span><span class="sxs-lookup"><span data-stu-id="a3a94-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="a3a94-134">Seret keperluan penempahan ke sumber/slot masa yang tersedia pada papan jadual.</span><span class="sxs-lookup"><span data-stu-id="a3a94-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="a3a94-135">Apabila anda telah selesai, pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="a3a94-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="a3a94-136">Sumber tambahan</span><span class="sxs-lookup"><span data-stu-id="a3a94-136">Additional resources</span></span>  
 [<span data-ttu-id="a3a94-137">Panduan pengurus sumber</span><span class="sxs-lookup"><span data-stu-id="a3a94-137">Resource manager guide</span></span>](../project-service/resource-manager-guide.md)
