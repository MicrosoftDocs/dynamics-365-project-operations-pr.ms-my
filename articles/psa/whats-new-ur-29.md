---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 29, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas Kini Project Service Automation 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664654"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="c9609-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 29, V3</span><span class="sxs-lookup"><span data-stu-id="c9609-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c9609-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c9609-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c9609-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="c9609-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c9609-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c9609-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c9609-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="c9609-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c9609-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c9609-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c9609-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 29.</span><span class="sxs-lookup"><span data-stu-id="c9609-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="c9609-110">Versi ini mempunyai nombor binaan V3.10.47.7 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Februari 2021.</span><span class="sxs-lookup"><span data-stu-id="c9609-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="c9609-111">Keluaran Kemas kini 29</span><span class="sxs-lookup"><span data-stu-id="c9609-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c9609-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="c9609-112">Bug fixes</span></span>

<span data-ttu-id="c9609-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="c9609-113">**Time and Expense**</span></span>

<span data-ttu-id="c9609-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="c9609-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c9609-115">Pengguna tidak dapat melihat waktu bekerja yang dilog pada hari tidak bekerja dalam grid entri masa.</span><span class="sxs-lookup"><span data-stu-id="c9609-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="c9609-116">Entri perbelanjaan yang diluluskan boleh diedit pada grid.</span><span class="sxs-lookup"><span data-stu-id="c9609-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="c9609-117">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="c9609-117">**Project Management**</span></span>

<span data-ttu-id="c9609-118">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="c9609-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="c9609-119">Logik pengesahan tiada untuk memastikan waktu usaha tugasan sumber tidak boleh negatif.</span><span class="sxs-lookup"><span data-stu-id="c9609-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="c9609-120">Tindakan tersuai, **AssignResourcesForTask** mengemas kini semua medan dan bukannya hanya medan yang berubah.</span><span class="sxs-lookup"><span data-stu-id="c9609-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="c9609-121">Apabila menyalin projek dalam persekitaran dengan pasang masuk atau aliran kerja yang didaftarkan pada peristiwa **CreateProject**, atribut **msdyn_bulkgenerationstatus** tidak dikemas kini jika **CopyWBSToProject** gagal.</span><span class="sxs-lookup"><span data-stu-id="c9609-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="c9609-122">Apabila anda mengembangkan kalendar projek, hari bekerja tidak diisih dalam susunan naik menyebabkan beberapa kemas kini tugas projek gagal.</span><span class="sxs-lookup"><span data-stu-id="c9609-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="c9609-123">Mengubah Pengurus Projek pada projek sedia ada mencetuskan logik lalai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="c9609-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="c9609-124">**Jualan**</span><span class="sxs-lookup"><span data-stu-id="c9609-124">**Sales**</span></span>

<span data-ttu-id="c9609-125">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="c9609-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="c9609-126">Tab **Prestasi Kontrak** pada halaman **Kontrak** gagal secara senyap semasa pengawalan apabila tiada baris kontrak wujud.</span><span class="sxs-lookup"><span data-stu-id="c9609-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
