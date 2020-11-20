---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 23, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131129"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="79c9b-103">Project Service Automation, Keluaran Kemas kini 23, V3</span><span class="sxs-lookup"><span data-stu-id="79c9b-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="79c9b-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="79c9b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="79c9b-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="79c9b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="79c9b-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="79c9b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="79c9b-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="79c9b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="79c9b-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="79c9b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="79c9b-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 23.</span><span class="sxs-lookup"><span data-stu-id="79c9b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="79c9b-110">Versi ini mempunyai nombor bina V 3.10.34.30 dan secara amnya boleh didapati melalui kemas kini kendiri pada Ogos 2020.</span><span class="sxs-lookup"><span data-stu-id="79c9b-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="79c9b-111">Keluaran Kemas kini 23</span><span class="sxs-lookup"><span data-stu-id="79c9b-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="79c9b-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="79c9b-112">Bug fixes</span></span>

<span data-ttu-id="79c9b-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="79c9b-113">**Time and Expense**</span></span>

<span data-ttu-id="79c9b-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="79c9b-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="79c9b-115">Kendalikan kes pinggir dalam **Padam Ahli Pasukan Projek** untuk memberikan pengecualian bermakna.</span><span class="sxs-lookup"><span data-stu-id="79c9b-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="79c9b-116">Import tugasan menyebabkan skrin alih keluar kosong.</span><span class="sxs-lookup"><span data-stu-id="79c9b-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="79c9b-117">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="79c9b-117">**Resource Management**</span></span>

<span data-ttu-id="79c9b-118">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="79c9b-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="79c9b-119">**Kad sumber grid penggunaan sumber** menunjukkan data yang salah apabila skala masa lebih daripada lima hari.</span><span class="sxs-lookup"><span data-stu-id="79c9b-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="79c9b-120">Apabila pelanggan mencipta sumber boleh ditempah, pasang masuk sekejap-sekejap gagal menambah sumber secara automatik pada kumpulan Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="79c9b-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="79c9b-121">Pandangan **penyesuaian** memaparkan kontur manual yang salah dalam pandangan **Minggu** atau **Bulan**.</span><span class="sxs-lookup"><span data-stu-id="79c9b-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="79c9b-122">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="79c9b-122">**Project Management**</span></span>

<span data-ttu-id="79c9b-123">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="79c9b-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="79c9b-124">Bilangan berlebihan entiti **RetrieveMultiple for usersettings** telah menyebabkan prestasi diturun taraf untuk kelulusan projek dan operasi lain.</span><span class="sxs-lookup"><span data-stu-id="79c9b-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="79c9b-125">Carian sumber grid **Perancangan Tugas** hanya terhad kepada lima ahli pasukan daripada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="79c9b-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="79c9b-126">Carian sumber grid **Perancangan Tugas** tidak menapis sumber yang tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="79c9b-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="79c9b-127">Mod manual tidak berfungsi seperti yang dijangkakan dalam struktur pecahan kerja perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="79c9b-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="79c9b-128">Grid **Perancangan Tugas** menunjukkan **Kategori Transaksi Tidak Aktif**.</span><span class="sxs-lookup"><span data-stu-id="79c9b-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="79c9b-129">Grid **Tugasan Sumber** dibundarkan dengan tidak betul apabila tugas mempunyai berbilang tugas.</span><span class="sxs-lookup"><span data-stu-id="79c9b-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="79c9b-130">Nilai pembundaran adalah berbeza antara kos yang dirancang dan kos sebenar untuk satu tugas.</span><span class="sxs-lookup"><span data-stu-id="79c9b-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="79c9b-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="79c9b-131">**Sales**</span></span>

<span data-ttu-id="79c9b-132">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="79c9b-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="79c9b-133">Klik dua kali **Kutip Semua Kategori Transaksi** mencipta berbilang baris.</span><span class="sxs-lookup"><span data-stu-id="79c9b-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
