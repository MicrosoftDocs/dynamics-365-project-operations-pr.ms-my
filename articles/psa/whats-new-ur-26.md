---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643274"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="71d54-102">Project Service Automation, Keluaran Kemas kini 26, V3</span><span class="sxs-lookup"><span data-stu-id="71d54-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="71d54-103">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="71d54-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="71d54-104">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="71d54-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="71d54-105">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="71d54-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="71d54-106">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="71d54-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="71d54-107">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="71d54-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="71d54-108">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 26, V3.</span><span class="sxs-lookup"><span data-stu-id="71d54-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="71d54-109">Versi ini mempunyai nombor binaan V3.10.44.59 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Disember 2020.</span><span class="sxs-lookup"><span data-stu-id="71d54-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="71d54-110">Keluaran Kemas kini 26</span><span class="sxs-lookup"><span data-stu-id="71d54-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="71d54-111">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="71d54-111">Bug fixes</span></span>

<span data-ttu-id="71d54-112">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="71d54-112">**Time and Expense**</span></span>

<span data-ttu-id="71d54-113">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="71d54-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="71d54-114">Pengguna boleh mengubah tugas pada entri masa yang telah diluluskan/diserahkan.</span><span class="sxs-lookup"><span data-stu-id="71d54-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="71d54-115">Ralat "Rujukan Objek Tidak Ditetapkan" apabila menyimpan entri masa.</span><span class="sxs-lookup"><span data-stu-id="71d54-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="71d54-116">Import entri masa daripada tugasan sumber menghasilkan entri masa dengan nilai DateTime yang salah.</span><span class="sxs-lookup"><span data-stu-id="71d54-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="71d54-117">Apabila Project Service Automation dan aplikasi Field Service dipasang, butang **Baharu** dipaparkan dua kali pada bar perintah untuk entri masa dalam aplikasi Field Service.</span><span class="sxs-lookup"><span data-stu-id="71d54-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="71d54-118">Kemas kini sel **Benarkan Unit** dan **Kumpulan Unit** kini berfungsi pada grid **Anggaran Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="71d54-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="71d54-119">Borang **Kemas kini Edit Entri Masa** termasuk **Garis masa**.</span><span class="sxs-lookup"><span data-stu-id="71d54-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="71d54-120">Kelulusan masa untuk entri masa bukan projek menyekat sistem ketika mencari peranan pelulus projek.</span><span class="sxs-lookup"><span data-stu-id="71d54-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="71d54-121">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="71d54-121">**Resource Management**</span></span>

<span data-ttu-id="71d54-122">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="71d54-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="71d54-123">Pengesahan yang ditambah dalam pasang masuk **PostProjectCreate** untuk menyemak keperluan utama sebelum mencipta satu.</span><span class="sxs-lookup"><span data-stu-id="71d54-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="71d54-124">Borang cipta cepat **Ahli Pasukan Projek** memberikan pengecualian rujukan nol jika medan dialih keluar daripada borang.</span><span class="sxs-lookup"><span data-stu-id="71d54-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="71d54-125">Menjana keperluan selama 12 jam lebih daripada 1 tahun akan gagal.</span><span class="sxs-lookup"><span data-stu-id="71d54-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="71d54-126">Pengecualian rujukan nol mesej ralat yang dipertingkatkan semasa penciptaan keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="71d54-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="71d54-127">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="71d54-127">**Project Management**</span></span>

<span data-ttu-id="71d54-128">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="71d54-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="71d54-129">Pengesahan yang dipertingkatkan untuk menangani pengecualian rujukan nol yang dijana dalam pasang masuk **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="71d54-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="71d54-130">Projek yang diterbitkan oleh tambahan Microsoft Project memadam tugasan yang tidak ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="71d54-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="71d54-131">Menambah pengesahan baharu apabila rujukan projek tugas tidak sah disebabkan pengecualian rujukan nol dalam pasang masuk **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="71d54-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="71d54-132">Grid ahli pasukan tidak menunjukkan tugasan yang berbeza pada rekod ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="71d54-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="71d54-133">Menambah pengesahan baharu dan mesej ralat disebabkan pengecualian rujukan nol dalam pasang masuk **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="71d54-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="71d54-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="71d54-134">**Sales**</span></span>

<span data-ttu-id="71d54-135">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="71d54-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="71d54-136">Apabila memilih baris berdasarkan projek dalam sebut harga atau kontrak, butang **Cadangan** sepatutnya hanya boleh dilihat apabila memilih baris berdasarkan produk yang dikaitkan dengan produk sedia ada.</span><span class="sxs-lookup"><span data-stu-id="71d54-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="71d54-137">Pisahkan kelayakan **Create_Product** daripada kelayakan **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="71d54-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="71d54-138">Memadamkan baris invois menyebabkan kegagalan rujukan nol pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="71d54-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
