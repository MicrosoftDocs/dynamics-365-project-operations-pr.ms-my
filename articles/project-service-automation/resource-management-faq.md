---
title: Soalan Lazim Pengurusan sumber
description: Topik ini memberikan jawapan kepada soalan lazim mengenai pengurusan sumber.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753957"
---
# <a name="resource-management-faq"></a><span data-ttu-id="3e029-103">Soalan Lazim Pengurusan sumber</span><span class="sxs-lookup"><span data-stu-id="3e029-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="3e029-104">Apakah perbezaan antara ahli pasukan dan keperluan sumber?</span><span class="sxs-lookup"><span data-stu-id="3e029-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="3e029-105">Ahli pasukan projek boleh ditugaskan untuk membuat tugas, menempah atau menempah lebih banyak, dan ditetapkan sebagai pelulus.</span><span class="sxs-lookup"><span data-stu-id="3e029-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="3e029-106">Keperluan sumber boleh wujud tanpa ahli pasukan projek, sebagai draf nota permintaan.</span><span class="sxs-lookup"><span data-stu-id="3e029-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="3e029-107">Apakah perbezaan antara jam yang dicadangkan dan tempahan lembut?</span><span class="sxs-lookup"><span data-stu-id="3e029-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="3e029-108">Jam yang dicadangkan dan waktu yang ditempah lembut berbeza dalam keterlihatan.</span><span class="sxs-lookup"><span data-stu-id="3e029-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="3e029-109">Jam yang dicadangkan hanya boleh dilihat oleh pengurus sumber dan pengurus projek yang memulakan permintaan menggunakan permintaan sumber.</span><span class="sxs-lookup"><span data-stu-id="3e029-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="3e029-110">Jam yang ditempah lembut boleh dilihat oleh sesiapa yang mempunyai akses kepada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="3e029-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="3e029-111">Bagaimanakah saya boleh melihat jam yang ditempah lembut untuk sumber pada pasukan?</span><span class="sxs-lookup"><span data-stu-id="3e029-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="3e029-112">Tempahan lembut boleh dilakukan semasa anda menempah keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="3e029-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="3e029-113">Sumber yang ditempah secara lembut pada pasukan projek muncul sebagai ahli pasukan yang mempunyai jam yang ditempah lembut.</span><span class="sxs-lookup"><span data-stu-id="3e029-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="3e029-114">Ia juga muncul pada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="3e029-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="3e029-115">Bagaimanakah saya boleh mengubah jam yang diperlukan dan tarikh mula dan tamat, bagi sumber (generik atau yang dinamakan) yang saya tempah?</span><span class="sxs-lookup"><span data-stu-id="3e029-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="3e029-116">Selepas sumber ditempah, pilih **Kekalkan Penempahan** untuk membuat sebarang perubahan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="3e029-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="3e029-117">Apakah jenis sumber yang disokong Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="3e029-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="3e029-118">**Pengguna** dan **Kenalan** ialah satu-satunya jenis sumber yang disokong Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3e029-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="3e029-119">Walaupun anda boleh mencipta jenis sumber lain (contohnya **Peralatan** dan **Kumpulan**), tidak menggunakan kes penggunaan hujung ke hujung disokong untuk mereka.</span><span class="sxs-lookup"><span data-stu-id="3e029-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="3e029-120">Apakah perbezaan antara tugasan dengan sesuatu penempahan?</span><span class="sxs-lookup"><span data-stu-id="3e029-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="3e029-121">Tugasan adalah tugasan sumber untuk tugas projek dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="3e029-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="3e029-122">Sumber boleh sama ada sumber sebenar atau generik.</span><span class="sxs-lookup"><span data-stu-id="3e029-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="3e029-123">Penempahan ialah pengagihan sumber yang cetak atau lembut kepada projek.</span><span class="sxs-lookup"><span data-stu-id="3e029-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="3e029-124">Penempahan keras menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="3e029-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="3e029-125">Sebaik-baiknya, untuk sumber sebenar, penempahan dan tugasan harus bersetuju, kerana mereka tidak berbeza.</span><span class="sxs-lookup"><span data-stu-id="3e029-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="3e029-126">Walau bagaimanapun, PSA tidak menguatkuasakan perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="3e029-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="3e029-127">Pandangan penyesuaian menunjukkan pengurus projek tempat penempahan tempahan sumber dan tugasan tidak bersetuju.</span><span class="sxs-lookup"><span data-stu-id="3e029-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
