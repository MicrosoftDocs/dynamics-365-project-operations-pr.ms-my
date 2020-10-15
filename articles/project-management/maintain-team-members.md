---
title: Mengekalkan ahli pasukan
description: Topik ini memberikan maklumat tentang tempahan sumber dinamakan kepada pasukan projek dan menugaskannya kepada tugasan.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961913"
---
# <a name="maintain-team-members"></a><span data-ttu-id="ba4c5-103">Mengekalkan ahli pasukan</span><span class="sxs-lookup"><span data-stu-id="ba4c5-103">Maintain team members</span></span>

<span data-ttu-id="ba4c5-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="ba4c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba4c5-105">Anda boleh menambahkan sumber yang dinamakan kepada pasukan projek anda dengan menempahnya secara langsung ke pasukan.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="ba4c5-106">Dalam Dynamics 365 Project Operations, pergi ke **Projek** dan pilih buka projek yang ditempah untuk anda.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="ba4c5-107">Pada halaman **Projek**, pada tab **Pasukan**, pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="ba4c5-108">Dalam kotak dialog **Ahli Pasukan Projek Cipta Pantas**, pilih sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="ba4c5-109">Medan **Peranan** akan mengisi peranan lalai sumber jika mereka mempunyai satu yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="ba4c5-110">Anda boleh mengubah peranan.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-110">You can change the role.</span></span> 
4. <span data-ttu-id="ba4c5-111">Pilih tarikh dari dan hingga yang diperlukan oleh sumber dan pilih kaedah peruntukan bagi kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="ba4c5-112">Dalam medan **Pelulus Projek**, pilih **Ya** jika anda mahu menjadikan ahli pasukan sebagai pelulus projek.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="ba4c5-113">Ahli pasukan boleh meluluskan masa diserah dan kemasukan perbelanjaan untuk projek ini.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="ba4c5-114">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-114">Select **Save**.</span></span>

<span data-ttu-id="ba4c5-115">Anda kini boleh menugaskan sumber boleh ditempah kepada tugasan pada projek.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="ba4c5-116">Pada halaman **Projek**, pada tab **Jadual**, tugaskan tugas ke sumber baharu.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="ba4c5-117">Pemilih sumber yang dilancarkan daripada medan **Sumber** dalam grid tugas akan menunjukkan ahli pasukan yang anda boleh pilih.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="ba4c5-118">Dalam Project Operations, penempahan sumber dan tugasan tugas tidak terlalu bergandingan.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="ba4c5-119">Apabila anda menggunakan pemilih sumber dalam jadual, anda boleh menugaskan tugas ke ahli pasukan untuk lebih jam daripada liputan penempahan mereka pada projek.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="ba4c5-120">Perbezaan antara penempahan ahli pasukan dan tugasan ditunjukkan pada tab **Pasukan** dan **Penyelarasan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="ba4c5-121">Anda juga boleh menyelaraskan perbezaan antara penempahan dan tugasan untuk sumber pada tahap yang lebih terperinci.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="ba4c5-122">Gunakan pemilih sumber pada tab **Jadual** untuk mencari dan memilih sumber boleh ditempah yang bukan lagi sebahagian daripada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="ba4c5-123">Sumber ini ditunjukkan dalam pemilih sumber sebagai **Sumber Lain**.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="ba4c5-124">Apabila anda melakukan pemilihan, sumber ditambah kepada pasukan projek dan ditugaskan ke tugas tetapi tiada tempahan dijana.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="ba4c5-125">Anda boleh menggunakan keupayaan tempahan lanjutan tab **Penyelarasan** atau **Papan Jadual** untuk menempah kapasiti sumber untuk projek.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="ba4c5-126">Selepas ahli pasukan ditempah pada projek anda, anda boleh menggunakan **Kekalkan tempahan** atau **Papan Jadual** secara langsung untuk mengurus penempahan mereka.</span><span class="sxs-lookup"><span data-stu-id="ba4c5-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
