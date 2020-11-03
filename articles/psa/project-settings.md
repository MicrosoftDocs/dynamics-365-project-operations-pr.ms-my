---
title: Tetapan projek
description: Topik ini memberikan maklumat tentang tetapan pengurusan projek.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081391"
---
# <a name="project-settings"></a><span data-ttu-id="45b32-103">Tetapan projek</span><span class="sxs-lookup"><span data-stu-id="45b32-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45b32-104">Gunakan tetapan berikut untuk mengakses ciri perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="45b32-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="45b32-105">Templat kerja</span><span class="sxs-lookup"><span data-stu-id="45b32-105">Work template</span></span>

<span data-ttu-id="45b32-106">Untuk mencipta jadual projek, anda cipta templat kalendar projek yang mentakrifkan bilangan jam kerja setiap hari dan sebarang penutupan perniagaan.</span><span class="sxs-lookup"><span data-stu-id="45b32-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="45b32-107">Untuk mencipta templat kalendar projek, anda kaitkan templat kerja dengan medan **Templat kalendar** untuk projek.</span><span class="sxs-lookup"><span data-stu-id="45b32-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="45b32-108">Ikuti langkah ini untuk mencipta templat kerja.</span><span class="sxs-lookup"><span data-stu-id="45b32-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="45b32-109">Dalam PSA, dalam anak tetingkap navigasi kiri, klik **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="45b32-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="45b32-110">Pada halaman senarai **Sumber** , buka rekod pengguna dan kemudian pilih **Tunjuk Jam Kerja**.</span><span class="sxs-lookup"><span data-stu-id="45b32-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="45b32-111">Pastikan anda membenarkan tetimbul pada halaman pelayar.</span><span class="sxs-lookup"><span data-stu-id="45b32-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="45b32-112">Ini membenarkan anda melihat jam kerja yang ditetapkan untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="45b32-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="45b32-113">Pada tab **Pandangan Bulanan** , klik **Sediakan**.</span><span class="sxs-lookup"><span data-stu-id="45b32-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="45b32-114">Satu senarai tiga pilihan muncul:</span><span class="sxs-lookup"><span data-stu-id="45b32-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="45b32-115">Jadual Mingguan Baharu</span><span class="sxs-lookup"><span data-stu-id="45b32-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="45b32-116">Jadual Kerja untuk Satu Hari</span><span class="sxs-lookup"><span data-stu-id="45b32-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="45b32-117">Masa Rehat</span><span class="sxs-lookup"><span data-stu-id="45b32-117">Time Off</span></span>

> ![Sediakan pilihan](media/project-13.png)

4. <span data-ttu-id="45b32-119">Pilih **Jadual Mingguan Baharu** dan kemudian tetapkan pilihan untuk jadual sumber ini.</span><span class="sxs-lookup"><span data-stu-id="45b32-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="45b32-120">Anda boleh menetapkan jadual mingguan berulang, parameter jam harian, penutupan perniagaan dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="45b32-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="45b32-121">Tetapkan julat tarikh, pilih **Simpan** dan kemudian klik **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="45b32-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="45b32-122">Kembali ke halaman senarai **Sumber** dan pilih sumber yang anda tetapkan jam kerja.</span><span class="sxs-lookup"><span data-stu-id="45b32-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="45b32-123">Pilih **Tetapkan Kalendar Sebagai** untuk menetapkan templat kerja.</span><span class="sxs-lookup"><span data-stu-id="45b32-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="45b32-124">Dalam kotak dialog **Templat Kerja** , masukkan nama untuk templat kerja dan kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="45b32-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="45b32-125">Kini anda boleh mengaitkan templat kerja dengan templat kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="45b32-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="45b32-126">Peranan sumber</span><span class="sxs-lookup"><span data-stu-id="45b32-126">Resource roles</span></span>

<span data-ttu-id="45b32-127">Istilah *peranan sumber* merujuk kepada set kemahiran, kecekapan dan pensijilan yang seseorang mesti ada untuk melakukan satu set tugas tertentu pada projek.</span><span class="sxs-lookup"><span data-stu-id="45b32-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="45b32-128">PSA membolehkan anda menetapkan kos dan mengebilkan masa sumber berdasarkan peranan yang dikaitkan dengan sumber tersebut.</span><span class="sxs-lookup"><span data-stu-id="45b32-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="45b32-129">Setiap organisasi mesti menyediakan peranan ini dengan menggunakan navigasi kiri pada menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="45b32-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="45b32-130">Setiap organisasi mesti menyediakan peranan ini pada halaman **Kategori Sumber Aktif**.</span><span class="sxs-lookup"><span data-stu-id="45b32-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="45b32-131">Untuk membuka halaman ini, dalam anak tetingkap navigasi kiri, pilih **Peranan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="45b32-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="45b32-132">Senarai harga</span><span class="sxs-lookup"><span data-stu-id="45b32-132">Price lists</span></span>

<span data-ttu-id="45b32-133">Senarai harga membolehkan anda menetapkan kos dan harga jualan untuk peranan sumber, kategori perbelanjaan, produk dan elemen lain dalam organisasi.</span><span class="sxs-lookup"><span data-stu-id="45b32-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="45b32-134">Sebelum anda menetapkan anggaran kewangan untuk kerja yang mesti dihantar bagi sesuatu projek, anda harus mencipta senarai kos sokongan dan harga jualan.</span><span class="sxs-lookup"><span data-stu-id="45b32-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="45b32-135">Dalam bahagian parameter, anda juga perlu menyediakan senarai kos dan harga jualan lalai yang digunakan pada semua projek yang dicipta dalam organisasi.</span><span class="sxs-lookup"><span data-stu-id="45b32-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="45b32-136">Pada halaman **Parameter Projek Aktif** , pastikan anda menyediakan senarai kos dan harga jualan lalai.</span><span class="sxs-lookup"><span data-stu-id="45b32-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
