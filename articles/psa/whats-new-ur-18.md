---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 18, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949195"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="402c4-103">Project Service Automation, Keluaran Kemas kini 18, V3</span><span class="sxs-lookup"><span data-stu-id="402c4-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="402c4-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="402c4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="402c4-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="402c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="402c4-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="402c4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="402c4-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="402c4-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="402c4-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="402c4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="402c4-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 18.</span><span class="sxs-lookup"><span data-stu-id="402c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="402c4-110">Versi ini mempunyai nombor binaan V3.10.8.12 dan secara amnya boleh didapati melalui kemas kini sendiri pada April 2020.</span><span class="sxs-lookup"><span data-stu-id="402c4-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="402c4-111">Keluaran Kemas kini 18</span><span class="sxs-lookup"><span data-stu-id="402c4-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="402c4-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="402c4-112">Bug fixes</span></span>

<span data-ttu-id="402c4-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="402c4-113">**Time and Expense**</span></span>

- <span data-ttu-id="402c4-114">Dibaiki: Aliran **Ingat semula**, **Minta** dan **Batalkan Kelulusan** menghasilkan pengecualian dengan mesej ralat tidak jelas.</span><span class="sxs-lookup"><span data-stu-id="402c4-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="402c4-115">Dibaiki: Apabila **Batal Kelulusan** gagal untuk perbelanjaan, ralat pengecualian yang berkaitan tidak dibuang.</span><span class="sxs-lookup"><span data-stu-id="402c4-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="402c4-116">Dibaiki: Grid Entri Masa secara salah mengendalikan hari tidak bekerja di Australia selepas pertukaran waktu penjimatan siang (DST) pada bulan Oktober.</span><span class="sxs-lookup"><span data-stu-id="402c4-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="402c4-117">Dibaiki: Logik lalai yang salah menghalang penghantaran perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="402c4-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="402c4-118">Dibaiki: Apabila kelulusan entri masa gagal, kelulusan masih dalam keadaan **Belum Selesai**.</span><span class="sxs-lookup"><span data-stu-id="402c4-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="402c4-119">Dibaiki: Ralat SQL ke atas kelulusan pukal (kunci mati/tamat tempoh).</span><span class="sxs-lookup"><span data-stu-id="402c4-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="402c4-120">Dibaiki: Isu prestasi penting dalam pengalaman pengguna yang disebabkan oleh mengemas kini ahli pasukan sambil meluluskan entri masa.</span><span class="sxs-lookup"><span data-stu-id="402c4-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="402c4-121">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="402c4-121">**Project Management**</span></span>

- <span data-ttu-id="402c4-122">Dibaiki: Pemberitahuan zon masa dipindahkan daripada pandangan **Penyesuaian** ke borang utama **Projek**.</span><span class="sxs-lookup"><span data-stu-id="402c4-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="402c4-123">Dibaiki: Templat kalendar tidak lalai secara betul apabila borang projek baru dibuka.</span><span class="sxs-lookup"><span data-stu-id="402c4-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="402c4-124">Dibaiki: Untuk pelayar berasaskan chromium, pengguna tidak dapat memilih tugas terdahulu untuk dipadamkan dengan mudah.</span><span class="sxs-lookup"><span data-stu-id="402c4-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="402c4-125">Dibaiki: Mencipta atau menyalin **Projek daripada templat Kosong** menarik tugasan yang tidak berkaitan.</span><span class="sxs-lookup"><span data-stu-id="402c4-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="402c4-126">Dibaiki: Dalam kes-kes edge tertentu, mencipta tugasan baharu daripada keputusan grid tugas dalam rekod pendua yang dicipta.</span><span class="sxs-lookup"><span data-stu-id="402c4-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="402c4-127">Dibaiki: Dalam mod manual, pengguna tidak dapat mengemas kini tarikh mula tugas lebih lewat daripada tarikh semasa yang disimpan.</span><span class="sxs-lookup"><span data-stu-id="402c4-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="402c4-128">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="402c4-128">**Resource Management**</span></span>

- <span data-ttu-id="402c4-129">Dibaiki: Baris subjumlah pandangan **Penyesuaian** salah mengira penempahan varians selepas melanjutkan penempahan.</span><span class="sxs-lookup"><span data-stu-id="402c4-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="402c4-130">Dibaiki: Pandangan **Penyesuaian** yang salah memaparkan tugasan sumber apabila sumber boleh ditempah mempunyai kalendar yang tidak sepadan dengan kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="402c4-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="402c4-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="402c4-131">**Sales**</span></span>

- <span data-ttu-id="402c4-132">Dibaiki: Apabila entri masa telah diluluskan semula (**Lulus > Batal >** lulus semula), pendua sebenar tidak boleh dikenakan bayaran dibuat.</span><span class="sxs-lookup"><span data-stu-id="402c4-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]