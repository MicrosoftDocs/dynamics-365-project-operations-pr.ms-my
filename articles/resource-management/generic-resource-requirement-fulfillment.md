---
title: Pemenuhan keperluan sumber generik
description: Topik ini memberikan maklumat tentang menempah sumber bernama untuk keperluan sumber generik.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897597"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="e3b6f-103">Pemenuhan keperluan sumber generik</span><span class="sxs-lookup"><span data-stu-id="e3b6f-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="e3b6f-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="e3b6f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3b6f-105">Anda boleh menempah sumber bernama untuk menggantikan sumber generik yang mempunyai keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="e3b6f-106">Pada halaman **Projek**, pilih tab **Pasukan**.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="e3b6f-107">Pilih sumber generik yang mempunyai keperluan sumber daripada senarai dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="e3b6f-108">Atau buka keperluan sumber dan kemudian pilih **Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="e3b6f-109">Pada halaman **Pembantu Jadual**, pilih sumber dinamakan untuk menempah ke dalam pasukan projek anda dan kemudian pilih**Tempah**.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="e3b6f-110">Apabila tempahan selesai dan diisi dengan sumber bernama, sumber generik digantikan dengan sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="e3b6f-111">Tugasan ke atas jadual dikemas kini dengan sumber bernama juga.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="e3b6f-112">Isi sumber generik dengan berbilang sumber bernama</span><span class="sxs-lookup"><span data-stu-id="e3b6f-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="e3b6f-113">Mengisi keperluan untuk sumber generik dengan berbilang sumber bernama adalah serupa dengan menugaskan sumber bernama tunggal.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="e3b6f-114">Contohnya, terdapat tugas yang mempunyai tempoh lima hari dan 120 jam usaha.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="e3b6f-115">Tugas ini tidak boleh diselesaikan oleh satu sumber yang bekerja 8 jam sehari selama lima hari seminggu yang biasa.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="e3b6f-116">Keperluan adalah untuk 120 jam bagi kejuruteraan robotik selama lima hari, yang mana 24 jam sehari.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="e3b6f-117">Ini adalah contoh ketika sumber berbilang diperlukan untuk mengisi permintaan sumber generik.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="e3b6f-118">Anda perlu menempah berbilang sumber untuk mengisi keperluan.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="e3b6f-119">Perbezaan utama dalam senario ini ialah bahawa sumber generik kekal dalam pasukan yang ditugaskan kepada tugas, dan ahli pasukan sumber bernama yang ditempah tidak ditugaskan sebagai sebahagian daripada kedudukan tersebut.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="e3b6f-120">Pengurus projek boleh menugaskan kerja sebagai sesuai kepada sumber bernama.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="e3b6f-121">Pandangan **Penyesuaian** boleh membantu pengurus projek dalam memecahkan tempahan di semua berbilang sumber untuk menugaskan tugasan.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="e3b6f-122">Ini tidak dilakukan secara automatik kerana dalam mana-mana senario yang lebih rumit daripada contoh mudah di atas seperti di mana anda mempunyai tugas yang memenuhi keperluan atau tujuan cara pengurus projek mahu menugaskan, perlu diandaikan oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="e3b6f-123">Oleh kerana sistem tidak boleh memahami tujuan, andaian mungkin akan berbeza daripada yang ditujukan dan hasil yang salah atau tidak dapat diramalkan akan berlaku.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="e3b6f-124">Hasil yang boleh dijangka ialah sumber generik kekal ditugaskan sehingga pengurus projek secara sengaja mencipta tugasan, dengan bantuan pandangan **Penyesuaian**.</span><span class="sxs-lookup"><span data-stu-id="e3b6f-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

