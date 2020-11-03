---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 23, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081175"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="d1ee3-103">Project Service Automation, Keluaran Kemas kini 23, V3</span><span class="sxs-lookup"><span data-stu-id="d1ee3-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="d1ee3-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d1ee3-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d1ee3-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d1ee3-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d1ee3-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d1ee3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d1ee3-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 23.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="d1ee3-110">Versi ini mempunyai nombor bina V 3.10.34.30 dan secara amnya boleh didapati melalui kemas kini kendiri pada Ogos 2020.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="d1ee3-111">Keluaran Kemas kini 23</span><span class="sxs-lookup"><span data-stu-id="d1ee3-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d1ee3-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="d1ee3-112">Bug fixes</span></span>

<span data-ttu-id="d1ee3-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="d1ee3-113">**Time and Expense**</span></span>

<span data-ttu-id="d1ee3-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="d1ee3-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="d1ee3-115">Kendalikan kes pinggir dalam **Padam Ahli Pasukan Projek** untuk memberikan pengecualian bermakna.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="d1ee3-116">Import tugasan menyebabkan skrin alih keluar kosong.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="d1ee3-117">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="d1ee3-117">**Resource Management**</span></span>

<span data-ttu-id="d1ee3-118">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="d1ee3-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1ee3-119">**Kad sumber grid penggunaan sumber** menunjukkan data yang salah apabila skala masa lebih daripada lima hari.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="d1ee3-120">Apabila pelanggan mencipta sumber boleh ditempah, pasang masuk sekejap-sekejap gagal menambah sumber secara automatik pada kumpulan Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="d1ee3-121">Pandangan **penyesuaian** memaparkan kontur manual yang salah dalam pandangan **Minggu** atau **Bulan**.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="d1ee3-122">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="d1ee3-122">**Project Management**</span></span>

<span data-ttu-id="d1ee3-123">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="d1ee3-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1ee3-124">Bilangan berlebihan entiti **RetrieveMultiple for usersettings** telah menyebabkan prestasi diturun taraf untuk kelulusan projek dan operasi lain.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="d1ee3-125">Carian sumber grid **Perancangan Tugas** hanya terhad kepada lima ahli pasukan daripada pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="d1ee3-126">Carian sumber grid **Perancangan Tugas** tidak menapis sumber yang tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="d1ee3-127">Mod manual tidak berfungsi seperti yang dijangkakan dalam struktur pecahan kerja perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="d1ee3-128">Grid **Perancangan Tugas** menunjukkan **Kategori Transaksi Tidak Aktif**.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="d1ee3-129">Grid **Tugasan Sumber** dibundarkan dengan tidak betul apabila tugas mempunyai berbilang tugas.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="d1ee3-130">Nilai pembundaran adalah berbeza antara kos yang dirancang dan kos sebenar untuk satu tugas.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="d1ee3-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d1ee3-131">**Sales**</span></span>

<span data-ttu-id="d1ee3-132">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="d1ee3-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1ee3-133">Klik dua kali **Kutip Semua Kategori Transaksi** mencipta berbilang baris.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
