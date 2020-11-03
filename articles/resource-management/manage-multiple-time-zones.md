---
title: Urus zon waktu
description: Apabila projek dicipta, zon masa adalah berdasarkan zon waktu yang ditakrifkan dalam templat jam kerja yang digunakan.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081166"
---
# <a name="manage-time-zones"></a><span data-ttu-id="23b25-103">Urus zon waktu</span><span class="sxs-lookup"><span data-stu-id="23b25-103">Manage time zones</span></span>

<span data-ttu-id="23b25-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="23b25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="23b25-105">Projek</span><span class="sxs-lookup"><span data-stu-id="23b25-105">Projects</span></span>

<span data-ttu-id="23b25-106">Apabila projek dicipta, zon masa adalah berdasarkan pada zon waktu yang ditakrifkan dalam templat jam kerja yang digunakan.</span><span class="sxs-lookup"><span data-stu-id="23b25-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="23b25-107">Pada **Projek** itu, tarikh sentiasa relatif kepada zon masa pengguna yang dilog masuk pada setiap tab, kecuali tab **Tugas**. Apabila anda melihat struktur pecahan kerja, tarikh akan sentiasa dipaparkan dalam zon waktu projek.</span><span class="sxs-lookup"><span data-stu-id="23b25-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="23b25-108">Tugas</span><span class="sxs-lookup"><span data-stu-id="23b25-108">Tasks</span></span>

<span data-ttu-id="23b25-109">Apabila tugas dicipta, masa mula, masa tamat dan jam/hari dikawal oleh waktu kerja projek.</span><span class="sxs-lookup"><span data-stu-id="23b25-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="23b25-110">Contohnya, jika tugas dicipta dengan projek yang zon masa adalah -8 PST dan mempunyai waktu kerja berikut: 9:00 PAGI hingga 5:00 PETANG Isnin hingga Jumaat, sebarang tugas yang dicipta tanpa sebarang penugasan akan mengikut masa mula dan masa akhir kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="23b25-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="23b25-111">Urus sumber dengan zon masa</span><span class="sxs-lookup"><span data-stu-id="23b25-111">Manage resources with time zones</span></span>

<span data-ttu-id="23b25-112">Untuk keputusan yang tepat dan boleh diramal apabila menggunakan **Penempahan Lanjutan** , terdapat dua syarat utama yang mesti dipatuhi:</span><span class="sxs-lookup"><span data-stu-id="23b25-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="23b25-113">Pengguna mesti mengkonfigurasi zon masa peranti mereka untuk dipadankan dengan zon waktu yang ditakrifkan dalam **Tetapan Peribadi** sistem.</span><span class="sxs-lookup"><span data-stu-id="23b25-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Tetapan zon waktu dalam Windows 10](media/reconcile-assignments-03.png)

  ![Tetapan zon waktu dalam tetapan pemperibadian](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="23b25-116">Sumber boleh ditempah mesti mempunyai sekurang-kurangnya satu minit daripada masa kerja yang bertindih dengan kontur yang digunakan untuk mentakrifkan sambungan yang diminta.</span><span class="sxs-lookup"><span data-stu-id="23b25-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="23b25-117">Contohnya, sumber yang berikut dengan waktu bekerja yang jatuh antara 9:00 PAGI dan 7:00 MALAM.</span><span class="sxs-lookup"><span data-stu-id="23b25-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Perbandingan sumber kontur](media/reconcile-assignments-05.png)

<span data-ttu-id="23b25-119">Jadual berikut menunjukkan:</span><span class="sxs-lookup"><span data-stu-id="23b25-119">The following table shows:</span></span>

- <span data-ttu-id="23b25-120">Templat kalendar projek</span><span class="sxs-lookup"><span data-stu-id="23b25-120">A project calendar template</span></span>
- <span data-ttu-id="23b25-121">Sumber A: Sumber ini mempunyai kalendar yang sama dan berada dalam zon waktu yang sama seperti projek.</span><span class="sxs-lookup"><span data-stu-id="23b25-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="23b25-122">Masa mula tempahan ialah 9:00 PG.</span><span class="sxs-lookup"><span data-stu-id="23b25-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="23b25-123">Sumber B: Sumber ini terletak dalam zon waktu yang berbeza daripada projek dan bermula pada 7:00 PAGI dalam zon waktu mereka.</span><span class="sxs-lookup"><span data-stu-id="23b25-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="23b25-124">Walau bagaimanapun, tempahan akan bermula pada 9:00 PG kerana itu adalah masa mula paling awal kontur tugasan.</span><span class="sxs-lookup"><span data-stu-id="23b25-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="23b25-125">Sumber C dan D: Sumber yang terletak dalam zon masa berbeza, kedua-duanya berbeza antara satu sama lain dan projek, dan penempahan mereka bermula tidak lebih awal daripada masa tersedia mereka.</span><span class="sxs-lookup"><span data-stu-id="23b25-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="23b25-126">Entiti</span><span class="sxs-lookup"><span data-stu-id="23b25-126">Entity</span></span>  |<span data-ttu-id="23b25-127">Kalendar</span><span class="sxs-lookup"><span data-stu-id="23b25-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="23b25-128">Templat kalendar projek</span><span class="sxs-lookup"><span data-stu-id="23b25-128">Project calendar template</span></span>   | ![kalendar projek](media/reconcile-assignments-06.png) |
|<span data-ttu-id="23b25-130">Sumber A</span><span class="sxs-lookup"><span data-stu-id="23b25-130">Resource A</span></span>  | ![Kalendar Sumber A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="23b25-132">Sumber B</span><span class="sxs-lookup"><span data-stu-id="23b25-132">Resource B</span></span>  |  ![Kalendar Sumber B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="23b25-134">Sumber C</span><span class="sxs-lookup"><span data-stu-id="23b25-134">Resource C</span></span>  |  ![Kalendar Sumber C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="23b25-136">Sumber D</span><span class="sxs-lookup"><span data-stu-id="23b25-136">Resource D</span></span>  | ![Kalendar Sumber D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="23b25-138">Apabila anda menavigasi ke pandangan **Penyelarasan** , tugasan sumber dan kekurangan penempahan yang berkaitan dipaparkan.</span><span class="sxs-lookup"><span data-stu-id="23b25-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Pandangan penyesuaian sebelum lanjutan](media/reconcile-assignments-10.png)

<span data-ttu-id="23b25-140">Selepas fungsi penempahan lanjutan telah digunakan untuk setiap sumber, penempahan berjaya dilanjutkan untuk setiap sumber kerana setiap jam kerja yang bertindih dengan kekurangan kontur.</span><span class="sxs-lookup"><span data-stu-id="23b25-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Pandangan penyesuaian selepas lanjutan tempahan](media/reconcile-assignments-11.png) 

<span data-ttu-id="23b25-142">Perhatikan bahawa pandangan lebih dekat pada butiran daripada penempahan Tempahan menunjukkan perbezaan dalam masa mula penempahan.</span><span class="sxs-lookup"><span data-stu-id="23b25-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="23b25-143">Penempahan mula tidak lebih awal daripada masa mula penugasan kontur dan tidak akan lebih awal daripada masa mula sumber yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="23b25-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Tempahan baharu sumber dalam papan jadual](media/reconcile-assignments-12.png)
