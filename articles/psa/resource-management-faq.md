---
title: Soalan Lazim Pengurusan sumber
description: Topik ini memberikan jawapan kepada soalan lazim mengenai pengurusan sumber.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008772"
---
# <a name="resource-management-faq"></a><span data-ttu-id="366de-103">Soalan Lazim Pengurusan sumber</span><span class="sxs-lookup"><span data-stu-id="366de-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="366de-104">Apakah perbezaan antara ahli pasukan dan keperluan sumber?</span><span class="sxs-lookup"><span data-stu-id="366de-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="366de-105">Ahli pasukan projek boleh ditugaskan untuk membuat tugas, menempah atau menempah lebih banyak, dan ditetapkan sebagai pelulus.</span><span class="sxs-lookup"><span data-stu-id="366de-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="366de-106">Keperluan sumber boleh wujud tanpa ahli pasukan projek, sebagai draf nota permintaan.</span><span class="sxs-lookup"><span data-stu-id="366de-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="366de-107">Apakah perbezaan antara jam yang dicadangkan dan tempahan lembut?</span><span class="sxs-lookup"><span data-stu-id="366de-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="366de-108">Jam yang dicadangkan dan waktu yang ditempah lembut berbeza dalam keterlihatan.</span><span class="sxs-lookup"><span data-stu-id="366de-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="366de-109">Jam yang dicadangkan hanya boleh dilihat oleh pengurus sumber dan pengurus projek yang memulakan permintaan menggunakan permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="366de-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="366de-110">Jam yang ditempah lembut boleh dilihat oleh sesiapa yang mempunyai akses kepada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="366de-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="366de-111">Bagaimanakah saya boleh melihat jam yang ditempah lembut untuk sumber pada pasukan?</span><span class="sxs-lookup"><span data-stu-id="366de-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="366de-112">Tempahan lembut boleh dilakukan semasa anda menempah keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="366de-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="366de-113">Sumber yang ditempah secara lembut pada pasukan projek muncul sebagai ahli pasukan yang mempunyai jam yang ditempah lembut.</span><span class="sxs-lookup"><span data-stu-id="366de-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="366de-114">Ia juga muncul pada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="366de-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="366de-115">Bagaimanakah saya boleh mengubah jam yang diperlukan dan tarikh mula dan tamat, bagi sumber (generik atau yang dinamakan) yang saya tempah?</span><span class="sxs-lookup"><span data-stu-id="366de-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="366de-116">Selepas sumber ditempah, pilih **Kekalkan Penempahan** untuk membuat sebarang perubahan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="366de-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="366de-117">Apakah jenis sumber yang disokong Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="366de-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="366de-118">**Pengguna** dan **Kenalan** ialah satu-satunya jenis sumber yang disokong Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="366de-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="366de-119">Walaupun anda boleh mencipta jenis sumber lain (contohnya **Peralatan** dan **Kumpulan**), tidak menggunakan kes penggunaan hujung ke hujung disokong untuk mereka.</span><span class="sxs-lookup"><span data-stu-id="366de-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="366de-120">Apakah perbezaan antara tugasan dengan sesuatu penempahan?</span><span class="sxs-lookup"><span data-stu-id="366de-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="366de-121">Tugasan adalah tugasan sumber untuk tugas projek dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="366de-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="366de-122">Sumber boleh sama ada sumber sebenar atau generik.</span><span class="sxs-lookup"><span data-stu-id="366de-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="366de-123">Penempahan ialah pengagihan sumber yang cetak atau lembut kepada projek.</span><span class="sxs-lookup"><span data-stu-id="366de-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="366de-124">Penempahan keras menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="366de-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="366de-125">Sebaik-baiknya, untuk sumber sebenar, penempahan dan tugasan harus bersetuju, kerana mereka tidak berbeza.</span><span class="sxs-lookup"><span data-stu-id="366de-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="366de-126">Walau bagaimanapun, PSA tidak menguatkuasakan perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="366de-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="366de-127">Pandangan penyesuaian menunjukkan pengurus projek tempat penempahan tempahan sumber dan tugasan tidak bersetuju.</span><span class="sxs-lookup"><span data-stu-id="366de-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]