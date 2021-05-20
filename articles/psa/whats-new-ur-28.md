---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 28, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Project Service Automation Keluaran Kemas kini 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948699"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="8d9dc-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 28, V3</span><span class="sxs-lookup"><span data-stu-id="8d9dc-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8d9dc-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8d9dc-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8d9dc-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8d9dc-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8d9dc-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8d9dc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8d9dc-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas Kini 28. Versi ini mempunyai nombor binaan V3.10.46.32 dan secara umumnya tersedia melalui kemas kini dengan sendiri pada Januari 2021.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="8d9dc-110">Keluaran Kemas kini 28</span><span class="sxs-lookup"><span data-stu-id="8d9dc-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8d9dc-111">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="8d9dc-111">Bug fixes</span></span>

<span data-ttu-id="8d9dc-112">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="8d9dc-112">**Time and Expense**</span></span>

<span data-ttu-id="8d9dc-113">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8d9dc-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d9dc-114">Pengguna boleh menggunakan **Edit Pukal** untuk mengemas kini entri masa yang telah diluluskan dan diserahkan.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="8d9dc-115">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="8d9dc-115">**Project Management**</span></span>

<span data-ttu-id="8d9dc-116">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8d9dc-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d9dc-117">Dalam kes yang tugas GUID ditafsirkan sebagai nombor, tugas tidak boleh dibuka untuk edit menggunakan **Edit Tugas** dalam reben pada halaman **Struktur Pecahan Kerja**.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="8d9dc-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8d9dc-118">**Sales**</span></span>

<span data-ttu-id="8d9dc-119">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="8d9dc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d9dc-120">Pengecualian rujukan nol dijana apabila pasang masuk **GetEstimatesForProject** dipanggil.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="8d9dc-121">**Tandai sebagai bersedia untuk diinvois** pada grid pencapaian hanya sebahagiannya mengemas kini atribut kecuali untuk atribut **InvoiceStatus** yang dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="8d9dc-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]