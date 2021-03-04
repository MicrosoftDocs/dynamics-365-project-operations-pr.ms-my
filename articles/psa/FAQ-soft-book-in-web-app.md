---
title: Bagaimanakah saya "menempah sementara" sumber dalam versi aplikasi 2.x?
description: Artikel ini menghuraikan cara menempah sementara ahli pasukan projek dengan Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 6bd13c448f4ce16fb93843df54f26cdd9bb884f4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146494"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="bf12a-103">Bagaimanakah saya "menempah sementara" sumber dalam aplikasi web (aplikasi Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="bf12a-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bf12a-104">Anda boleh secara sementara menjadualkan atau "menempah sementara" sumber ke atas pasukan projek untuk menunjukkan yang anda merancang untuk menugaskan sumber kepada projek.</span><span class="sxs-lookup"><span data-stu-id="bf12a-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="bf12a-105">Tempahan sementara tidak menggunakan kapasiti tersedia sumber.</span><span class="sxs-lookup"><span data-stu-id="bf12a-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="bf12a-106">Ahli pasukan ditempah sementara tidak boleh ditugaskan kepada tugas projek.</span><span class="sxs-lookup"><span data-stu-id="bf12a-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="bf12a-107">Hanya sumber yang mempunyai Status Ditempah Tetap dan Jenis Perlakuan Terikat boleh ditugaskan kepada tugas (dengan anggapan yang ia mempunyai jam tempahan tetap yang mencukupi meliputi usaha tugasan).</span><span class="sxs-lookup"><span data-stu-id="bf12a-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="bf12a-108">Ahli pasukan projek ditempah sementara muncul dalam grid Ahli Pasukan dengan jam ditempah sementara mereka ditunjukkan dalam lajur Tempah Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="bf12a-109">Mereka juga muncul pada papan jadual.</span><span class="sxs-lookup"><span data-stu-id="bf12a-109">They also show up on the schedule board.</span></span> <span data-ttu-id="bf12a-110">Tambahan pula, mereka tidak menunjukkan penggunaan kapasiti kerana tempahan sementara tidak menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="bf12a-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="bf12a-111">Terdapat tiga cara untuk menempah sementara ahli pasukan ke atas projek dengan Project Service versi 2.x.</span><span class="sxs-lookup"><span data-stu-id="bf12a-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="bf12a-112">Anda boleh menempah sementara dengan papan jadual, gunakan ciri Kekalkan Tempahan atau dengan mencipta sumber generik.</span><span class="sxs-lookup"><span data-stu-id="bf12a-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="bf12a-113">Kaedah ini dihuraikan seperti di bawah.</span><span class="sxs-lookup"><span data-stu-id="bf12a-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="bf12a-114">Tempah sementara dengan papan jadual</span><span class="sxs-lookup"><span data-stu-id="bf12a-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="bf12a-115">Untuk menempah sementara dengan papan jadual, ikuti prosedur ini:</span><span class="sxs-lookup"><span data-stu-id="bf12a-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="bf12a-116">Buka papan jadual.</span><span class="sxs-lookup"><span data-stu-id="bf12a-116">Open the schedule board.</span></span>
2. <span data-ttu-id="bf12a-117">Pilih tab Projek di bahagian bawah panel Keperluan Tempahan papan jadual.</span><span class="sxs-lookup"><span data-stu-id="bf12a-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="bf12a-118">Cari projek yang anda ingin menempah sementara sumber ke atasnya.</span><span class="sxs-lookup"><span data-stu-id="bf12a-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="bf12a-119">Jika anda mempunyai banyak projek, klik pengepala lajur Projek dan kemudian gunakan penapis untuk mencari projek anda.</span><span class="sxs-lookup"><span data-stu-id="bf12a-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="bf12a-120">Klik pada projek, kemudian seret dan lepaskannya pada grid masa sumber.</span><span class="sxs-lookup"><span data-stu-id="bf12a-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="bf12a-121">Ini membuka panel Cipta Tempahan Sumber di sebelah kanan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="bf12a-122">Laraskan tarikh mula dan akhir, pilih Status Tempahan sebagai Sementara dan tetapkan jam.</span><span class="sxs-lookup"><span data-stu-id="bf12a-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="bf12a-123">Klik Tempah.</span><span class="sxs-lookup"><span data-stu-id="bf12a-123">Click Book.</span></span>
7. <span data-ttu-id="bf12a-124">Kembali ke projek, sumber kini akan ditunjukkan sebagai ahli pasukan dengan jam ditempah sementara dalam lajur Tempah Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="bf12a-125">Perhatian bahawa anda tidak boleh menugaskan mereka dengan tugas pada struktur pecahan kerja (WBS) kerana sumber haruslah ditempah tetap pada pasukan yang akan ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="bf12a-126">Tempah sementara menggunakan ciri Kekalkan Tempahan</span><span class="sxs-lookup"><span data-stu-id="bf12a-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="bf12a-127">Untuk menempah sementara dengan Kekalkan Tempahan, ikuti prosedur ini:</span><span class="sxs-lookup"><span data-stu-id="bf12a-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="bf12a-128">Dari grid ahli pasukan, Klik Baharu.</span><span class="sxs-lookup"><span data-stu-id="bf12a-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="bf12a-129">Pilih sumber, peranan, dari/ke yang boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="bf12a-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="bf12a-130">Pilih kaedah peruntukan selain daripada Tiada:</span><span class="sxs-lookup"><span data-stu-id="bf12a-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="bf12a-131">Kapasiti Penuh</span><span class="sxs-lookup"><span data-stu-id="bf12a-131">Full Capacity</span></span>
- <span data-ttu-id="bf12a-132">Kapasiti Peratusan</span><span class="sxs-lookup"><span data-stu-id="bf12a-132">Percentage Capacity</span></span>
- <span data-ttu-id="bf12a-133">Edarkan Dengan Sekata Mengikut Jam</span><span class="sxs-lookup"><span data-stu-id="bf12a-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="bf12a-134">Caj Muka Mengikut Jam</span><span class="sxs-lookup"><span data-stu-id="bf12a-134">By Hours Front Load</span></span>
4. <span data-ttu-id="bf12a-135">Klik Simpan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-135">Click Save.</span></span> <span data-ttu-id="bf12a-136">Anda akan melihat sumber pada grid pasukan dan jam mereka ditunjukkan sebagai Tetap.</span><span class="sxs-lookup"><span data-stu-id="bf12a-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="bf12a-137">Kekalkan tempahan sumber dengan mengklik Kekalkan Tempahan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="bf12a-138">Apabila papan jadual dibuka, kembangkan sumber untuk menunjukkan tempahan mereka.</span><span class="sxs-lookup"><span data-stu-id="bf12a-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="bf12a-139">Anda akan melihat tempahan yang ditunjukkan sebagai Tetap.</span><span class="sxs-lookup"><span data-stu-id="bf12a-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="bf12a-140">Klik kanan tempahan, di bawah bahagian Tukar Status, pilih Tempah Sementara dan kemudian Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="bf12a-141">Status tempahan kini Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="bf12a-142">Selepas menutup papan jadual, anda akan melihat bahawa jam untuk sumber telah bertukar daripada Tetap kepada Sementara pada grid ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="bf12a-143">Perhatian bahawa jika anda menempah tetap sumber ke atas pasukan dan kemudian menugaskan mereka dengan tugas dalam WBS, apabila anda menggunakan kekalkan tempahan untuk menukar status Tetap kepada Sementara, ia akan mengeluarkan tugasan daripada tugas untuk sumber itu kerana hanya sumber ditempah tetap boleh ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="bf12a-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="bf12a-144">Tempah sementara dengan mencipta sumber generik</span><span class="sxs-lookup"><span data-stu-id="bf12a-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="bf12a-145">Anda boleh mencipta tempahan sementara dengan menjana ahli pasukan sumber generik, memenuhi papan jadual atau Permintaan Sumber dan menukar jenis semasa tempahan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="bf12a-146">Untuk melakukan ini, gunakan prosedur berikut:</span><span class="sxs-lookup"><span data-stu-id="bf12a-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="bf12a-147">Pada projek WBS, tugaskan peranan kepada tugas yang anda ingin janakan untuk ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="bf12a-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="bf12a-148">Klik Jana Pasukan Projek.</span><span class="sxs-lookup"><span data-stu-id="bf12a-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="bf12a-149">Pada grid ahli pasukan projek, pilih sumber generik dan klik Tempah.</span><span class="sxs-lookup"><span data-stu-id="bf12a-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="bf12a-150">Pada papan jadual, pilih sumber yang anda ingin menempah.</span><span class="sxs-lookup"><span data-stu-id="bf12a-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="bf12a-151">Pada papan jadual panel Cipta Tempahan Sumber, tukar Status Tempahan kepada Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="bf12a-152">Klik Tempah atau Tempah dan Keluar.</span><span class="sxs-lookup"><span data-stu-id="bf12a-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="bf12a-153">Selepas menutup papan jadual, anda akan melihat sumber terpilih ditambah kepada pasukan dengan jam ditempah Sementara serta jam ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="bf12a-154">Anda juga akan melihat bahawa sumber generik kekal berada dalam pasukan sebagai penunjuk yang tugas diberikan kepada ahli pasukan ditempah sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="bf12a-155">Apabila anda sudah bersedia untuk menukar sumber ahli pasukan ditempah sementara kepada ahli pasukan ditempah tetap supaya anda boleh menugaskan mereka kepada tugas, lakukan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="bf12a-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="bf12a-156">Pilih sumber dan klik Kekalkan Tempahan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="bf12a-157">Apabila papan jadual dibuka, kembangkan sumber untuk menunjukkan tempahan mereka.</span><span class="sxs-lookup"><span data-stu-id="bf12a-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="bf12a-158">Anda akan melihat tempahan ditanda sebagai Sementara.</span><span class="sxs-lookup"><span data-stu-id="bf12a-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="bf12a-159">Klik kanan tempahan, di bawah bahagian Tukar Status, pilih Tempah Tetap dan kemudian Tetap.</span><span class="sxs-lookup"><span data-stu-id="bf12a-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="bf12a-160">Status tempahan kini Tetap.</span><span class="sxs-lookup"><span data-stu-id="bf12a-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="bf12a-161">Selepas menutup papan jadual, anda akan melihat bahawa jam untuk sumber telah bertukar daripada Sementara kepada Tetap pada grid ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="bf12a-162">Anda kini boleh menugaskan sumber kepada tugas (dengan syarat terdapat penjajaran antara jam ditempah tetap dan jam usaha tugas untuk tugasan).</span><span class="sxs-lookup"><span data-stu-id="bf12a-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="bf12a-163">Perhatian bahawa jika anda mengikuti langkah pemenuhan sumber generik dalam item #3 di atas, apabila anda menukar status sumber boleh ditempah untuk ditempah sementara kepada tetap, ahli pasukan generik akan dikeluarkan dari pasukan.</span><span class="sxs-lookup"><span data-stu-id="bf12a-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
