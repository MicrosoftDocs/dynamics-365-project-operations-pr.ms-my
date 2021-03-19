---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 26, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Project Service Automation Keluaran Kemas kini 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280409"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="80bf4-103">Project Service Automation, Keluaran Kemas kini 26, V3</span><span class="sxs-lookup"><span data-stu-id="80bf4-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="80bf4-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="80bf4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="80bf4-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="80bf4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="80bf4-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="80bf4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="80bf4-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="80bf4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="80bf4-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="80bf4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="80bf4-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 26, V3.</span><span class="sxs-lookup"><span data-stu-id="80bf4-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="80bf4-110">Versi ini mempunyai nombor binaan V3.10.44.59 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Disember 2020.</span><span class="sxs-lookup"><span data-stu-id="80bf4-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="80bf4-111">Keluaran Kemas kini 26</span><span class="sxs-lookup"><span data-stu-id="80bf4-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="80bf4-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="80bf4-112">Bug fixes</span></span>

<span data-ttu-id="80bf4-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="80bf4-113">**Time and Expense**</span></span>

<span data-ttu-id="80bf4-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="80bf4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="80bf4-115">Pengguna boleh mengubah tugas pada entri masa yang telah diluluskan/diserahkan.</span><span class="sxs-lookup"><span data-stu-id="80bf4-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="80bf4-116">Ralat "Rujukan Objek Tidak Ditetapkan" apabila menyimpan entri masa.</span><span class="sxs-lookup"><span data-stu-id="80bf4-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="80bf4-117">Import entri masa daripada tugasan sumber menghasilkan entri masa dengan nilai DateTime yang salah.</span><span class="sxs-lookup"><span data-stu-id="80bf4-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="80bf4-118">Apabila Project Service Automation dan aplikasi Field Service dipasang, butang **Baharu** dipaparkan dua kali pada bar perintah untuk entri masa dalam aplikasi Field Service.</span><span class="sxs-lookup"><span data-stu-id="80bf4-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="80bf4-119">Kemas kini sel **Benarkan Unit** dan **Kumpulan Unit** kini berfungsi pada grid **Anggaran Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="80bf4-120">Borang **Kemas kini Edit Entri Masa** termasuk **Garis masa**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="80bf4-121">Kelulusan masa untuk entri masa bukan projek menyekat sistem ketika mencari peranan pelulus projek.</span><span class="sxs-lookup"><span data-stu-id="80bf4-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="80bf4-122">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="80bf4-122">**Resource Management**</span></span>

<span data-ttu-id="80bf4-123">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="80bf4-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="80bf4-124">Pengesahan yang ditambah dalam pasang masuk **PostProjectCreate** untuk menyemak keperluan utama sebelum mencipta satu.</span><span class="sxs-lookup"><span data-stu-id="80bf4-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="80bf4-125">Borang cipta cepat **Ahli Pasukan Projek** memberikan pengecualian rujukan nol jika medan dialih keluar daripada borang.</span><span class="sxs-lookup"><span data-stu-id="80bf4-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="80bf4-126">Menjana keperluan selama 12 jam lebih daripada 1 tahun akan gagal.</span><span class="sxs-lookup"><span data-stu-id="80bf4-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="80bf4-127">Pengecualian rujukan nol mesej ralat yang dipertingkatkan semasa penciptaan keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="80bf4-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="80bf4-128">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="80bf4-128">**Project Management**</span></span>

<span data-ttu-id="80bf4-129">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="80bf4-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="80bf4-130">Pengesahan yang dipertingkatkan untuk menangani pengecualian rujukan nol yang dijana dalam pasang masuk **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="80bf4-131">Projek yang diterbitkan oleh tambahan Microsoft Project memadam tugasan yang tidak ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="80bf4-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="80bf4-132">Menambah pengesahan baharu apabila rujukan projek tugas tidak sah disebabkan pengecualian rujukan nol dalam pasang masuk **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="80bf4-133">Grid ahli pasukan tidak menunjukkan tugasan yang berbeza pada rekod ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="80bf4-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="80bf4-134">Menambah pengesahan baharu dan mesej ralat disebabkan pengecualian rujukan nol dalam pasang masuk **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="80bf4-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="80bf4-135">**Sales**</span></span>

<span data-ttu-id="80bf4-136">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="80bf4-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="80bf4-137">Apabila memilih baris berdasarkan projek dalam sebut harga atau kontrak, butang **Cadangan** sepatutnya hanya boleh dilihat apabila memilih baris berdasarkan produk yang dikaitkan dengan produk sedia ada.</span><span class="sxs-lookup"><span data-stu-id="80bf4-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="80bf4-138">Pisahkan kelayakan **Create_Product** daripada kelayakan **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="80bf4-139">Memadamkan baris invois menyebabkan kegagalan rujukan nol pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="80bf4-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]