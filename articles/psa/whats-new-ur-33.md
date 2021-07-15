---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 33, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334575"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="03baa-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 33, V3</span><span class="sxs-lookup"><span data-stu-id="03baa-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="03baa-104">Kami amat berbesar hati mengumumkan kemas kini terbaharu untuk apl Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="03baa-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="03baa-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="03baa-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="03baa-106">Kemas kini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="03baa-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="03baa-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian dalam talian Pusat Pentadbir untuk Dynamics 365 dan pasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="03baa-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="03baa-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="03baa-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="03baa-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 33.</span><span class="sxs-lookup"><span data-stu-id="03baa-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="03baa-110">Versi ini mempunyai nombor binaan V3.10.54.98 dan secara umumnya tersedia melalui kemas kini kendiri pada Julai 2021.</span><span class="sxs-lookup"><span data-stu-id="03baa-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="03baa-111">Keluaran Kemas kini 33</span><span class="sxs-lookup"><span data-stu-id="03baa-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="03baa-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="03baa-112">Bug fixes</span></span>

<span data-ttu-id="03baa-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="03baa-113">**Time and Expense**</span></span>

<span data-ttu-id="03baa-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="03baa-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="03baa-115">Dua medan terkunci, **msdyn_description** dan **msdyn_externaldescription** boleh diedit selepas penyerahan.</span><span class="sxs-lookup"><span data-stu-id="03baa-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="03baa-116">Mesej ralat berlaku jika perbelanjaan dicipta yang tidak berkaitan dengan projek.</span><span class="sxs-lookup"><span data-stu-id="03baa-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="03baa-117">Apabila entri masa dicipta, peranan sumber ditetapkan secara lalai kepada peranti tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="03baa-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="03baa-118">Baris jurnal yang berkaitan dengan perbelanjaan yang ditarik balik dan dipadamkan tidak dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="03baa-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="03baa-119">Pada **Borang Cipta Cepat Entri masa**, kemas kini pandangan **Senarai Tugas Projek** untuk mengubah tarikh yang dipaparkan secara lalai kepada tarikh mula tugas.</span><span class="sxs-lookup"><span data-stu-id="03baa-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="03baa-120">Apabila anda mencipta entri masa daripada tab **Berkaitan** sumber boleh ditempah, entri masa tidak dicipta dengan betul untuk pengguna didaftar masuk dan bukannya sumber boleh ditempah induk.</span><span class="sxs-lookup"><span data-stu-id="03baa-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="03baa-121">Medan baharu ditambahkan pada kotak dialog **Kelulusan pukal MDD**.</span><span class="sxs-lookup"><span data-stu-id="03baa-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="03baa-122">**Perancangan projek**</span><span class="sxs-lookup"><span data-stu-id="03baa-122">**Project planning**</span></span>

<span data-ttu-id="03baa-123">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="03baa-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="03baa-124">Prestasi penciptaan projek perlahan apabila templat waktu kerja projek digunakan dengan kalendar yang kompleks.</span><span class="sxs-lookup"><span data-stu-id="03baa-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="03baa-125">Apabila tarikh mula lebih besar daripada tarikh tamat, ralat dipaparkan pada templat projek salinan disebabkan perbezaan dalam komponen masa setiap medan.</span><span class="sxs-lookup"><span data-stu-id="03baa-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="03baa-126">**Pengurusan sumber**</span><span class="sxs-lookup"><span data-stu-id="03baa-126">**Resource management**</span></span>

<span data-ttu-id="03baa-127">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="03baa-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="03baa-128">Parameter yang tidak betul digunakan dalam pertanyaan penggunaan  sumber dan XML membawa kepada hasil penapis yang tidak betul pada grid **Penggunaan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="03baa-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="03baa-129">Pengesahan **Tempahan Lanjut** memaparkan tarikh tamat yang tidak betul untuk tempahan.</span><span class="sxs-lookup"><span data-stu-id="03baa-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="03baa-130">**Jualan**</span><span class="sxs-lookup"><span data-stu-id="03baa-130">**Sales**</span></span>

<span data-ttu-id="03baa-131">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="03baa-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="03baa-132">Mesej ralat berlaku jika harga kategori dicipta dengan nilai yang tidak ditemui.</span><span class="sxs-lookup"><span data-stu-id="03baa-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="03baa-133">Mesej ralat berlaku jika pencapaian baris kontrak dicipta tanpa baris pesanan.</span><span class="sxs-lookup"><span data-stu-id="03baa-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
