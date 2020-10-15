---
title: Tempah ke projek
description: Topik ini memberikan maklumat tentang menempah sumber kepada projek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908415"
---
# <a name="book-to-a-project"></a><span data-ttu-id="a3e46-103">Tempah ke projek</span><span class="sxs-lookup"><span data-stu-id="a3e46-103">Book to a project</span></span>

<span data-ttu-id="a3e46-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="a3e46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3e46-105">Terdapat masa apabila pengurus projek atau pengurus sumber perlu memperuntukkan sumber kepada projek tanpa keperluan khusus yang ditakrifkan daripada ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="a3e46-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="a3e46-106">Ini boleh dicapai dalam salah satu daripada tiga cara.</span><span class="sxs-lookup"><span data-stu-id="a3e46-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="a3e46-107">Tempah daripada grid ahli pasukan</span><span class="sxs-lookup"><span data-stu-id="a3e46-107">Book from the team member grid</span></span>
- <span data-ttu-id="a3e46-108">Tempah daripada papan jadual</span><span class="sxs-lookup"><span data-stu-id="a3e46-108">Book from the schedule board</span></span>
- <span data-ttu-id="a3e46-109">Tempah daripada borang **Projek**</span><span class="sxs-lookup"><span data-stu-id="a3e46-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="a3e46-110">Tempah daripada grid ahli pasukan</span><span class="sxs-lookup"><span data-stu-id="a3e46-110">Book from the team member grid</span></span>

<span data-ttu-id="a3e46-111">Jika organisasi anda beroperasi dalam Mod peruntukan sumber hibrid, Pengurus projek boleh menempah sumber secara langsung kepada projek dengan melengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="a3e46-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="a3e46-112">Daripada projek, pergi ke grid ahli pasukan dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="a3e46-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="a3e46-113">Takrifkan nama jawatan dan peranan sumber.</span><span class="sxs-lookup"><span data-stu-id="a3e46-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="a3e46-114">Pilih sumber yang boleh ditempah daripada carian yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="a3e46-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="a3e46-115">Selepas anda memilih sumber, takrifkan maklumat medan berikut untuk menempah sumber:</span><span class="sxs-lookup"><span data-stu-id="a3e46-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="a3e46-116">Tarikh mula</span><span class="sxs-lookup"><span data-stu-id="a3e46-116">Start date</span></span>
    - <span data-ttu-id="a3e46-117">Tarikh siap</span><span class="sxs-lookup"><span data-stu-id="a3e46-117">Finish date</span></span>
    - <span data-ttu-id="a3e46-118">Kaedah peruntukan</span><span class="sxs-lookup"><span data-stu-id="a3e46-118">Allocation method</span></span>
    - <span data-ttu-id="a3e46-119">Jam, jika berkenaan</span><span class="sxs-lookup"><span data-stu-id="a3e46-119">Hours, if applicable</span></span>
    - <span data-ttu-id="a3e46-120">Pelulus projek</span><span class="sxs-lookup"><span data-stu-id="a3e46-120">Project approver</span></span>

6. <span data-ttu-id="a3e46-121">Pilih **Simpan dan Tutup**</span><span class="sxs-lookup"><span data-stu-id="a3e46-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="a3e46-122">Tempah daripada papan jadual</span><span class="sxs-lookup"><span data-stu-id="a3e46-122">Book from the schedule board</span></span>

<span data-ttu-id="a3e46-123">Apabila Pengurus sumber perlu menempah sumber secara langsung kepada projek, mereka boleh menggunakan papan jadual dan keperluan projek.</span><span class="sxs-lookup"><span data-stu-id="a3e46-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="a3e46-124">Keperluan projek ialah keperluan sumber yang sentiasa tersedia untuk ditempah.</span><span class="sxs-lookup"><span data-stu-id="a3e46-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="a3e46-125">Untuk menempah secara langsung kepada projek daripada papan jadual, lengkapkan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="a3e46-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="a3e46-126">Navigasi ke papan jadual dan pada halaman kiri, tapis untuk sumber yang anda pertimbangkan untuk keperluan.</span><span class="sxs-lookup"><span data-stu-id="a3e46-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="a3e46-127">Dalam anak tetingkap bahagian bawah, pilih tab **Projek** untuk melihat senarai keperluan projek.</span><span class="sxs-lookup"><span data-stu-id="a3e46-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="a3e46-128">Seret keperluan kepada sumber dan tentukan maklumat berikut:</span><span class="sxs-lookup"><span data-stu-id="a3e46-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="a3e46-129">Tarikh mula</span><span class="sxs-lookup"><span data-stu-id="a3e46-129">Start date</span></span>
    - <span data-ttu-id="a3e46-130">Tarikh siap</span><span class="sxs-lookup"><span data-stu-id="a3e46-130">Finish date</span></span>
    - <span data-ttu-id="a3e46-131">Status tempahan</span><span class="sxs-lookup"><span data-stu-id="a3e46-131">Booking status</span></span>
    - <span data-ttu-id="a3e46-132">Kaedah tempahan</span><span class="sxs-lookup"><span data-stu-id="a3e46-132">Booking method</span></span>
    - <span data-ttu-id="a3e46-133">Tempoh</span><span class="sxs-lookup"><span data-stu-id="a3e46-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="a3e46-134">Tempah daripada borang Projek</span><span class="sxs-lookup"><span data-stu-id="a3e46-134">Book from the Project form</span></span>

<span data-ttu-id="a3e46-135">Sebagai Pengurus Projek, anda mungkin perlu menempah sumber kepada projek, tetapi hanya mengetahui kriteria dan bukannya nama sumber.</span><span class="sxs-lookup"><span data-stu-id="a3e46-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="a3e46-136">Lengkapkan langkah berikut untuk menggunakan pembantu jadual bagi mencari sumber berdasarkan sebarang atribut yang tersedia bagi sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="a3e46-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="a3e46-137">Navigasi ke projek dan pilih **Tempah** untuk membuka Pembantu Jadual.</span><span class="sxs-lookup"><span data-stu-id="a3e46-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="a3e46-138">Menggunakan penapis di sebelah kiri Pembantu Jadual, kecilkan kriteria dan pilih **Gelintar.**</span><span class="sxs-lookup"><span data-stu-id="a3e46-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="a3e46-139">Berdasarkan sumber yang dikembalikan dalam hasil, anda boleh menempah sumber.</span><span class="sxs-lookup"><span data-stu-id="a3e46-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="a3e46-140">Kaedah ini tidak mencipta sebarang tempahan untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="a3e46-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="a3e46-141">Sebaliknya, ia menambahkan sumber kepada pasukan.</span><span class="sxs-lookup"><span data-stu-id="a3e46-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="a3e46-142">Selepas ahli pasukan ditambah kepada projek, pengurus projek boleh menggunakan kekalkan tempahan atau lanjutkan tempahan untuk menambah tempahan yang diperlukan kepada sumber.</span><span class="sxs-lookup"><span data-stu-id="a3e46-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
