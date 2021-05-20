---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 31, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945546"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="f7042-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 31, V3</span><span class="sxs-lookup"><span data-stu-id="f7042-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f7042-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f7042-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f7042-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="f7042-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f7042-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f7042-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f7042-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="f7042-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f7042-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f7042-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f7042-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 31.</span><span class="sxs-lookup"><span data-stu-id="f7042-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="f7042-110">Versi ini mempunyai nombor binaan V3.10.52.77 dan secara amnya boleh didapati melalui kemas kini sendiri pada Mei 2021.</span><span class="sxs-lookup"><span data-stu-id="f7042-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="f7042-111">Keluaran Kemas kini 31</span><span class="sxs-lookup"><span data-stu-id="f7042-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f7042-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="f7042-112">Bug fixes</span></span>

<span data-ttu-id="f7042-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="f7042-113">**Time and Expense**</span></span>

<span data-ttu-id="f7042-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="f7042-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f7042-115">Butang arahan kawalan entri masa pada halaman **Sumber Boleh Ditempah** adalah mengelirukan.</span><span class="sxs-lookup"><span data-stu-id="f7042-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="f7042-116">Pengecualian rujukan nol dijana dalam **Project.SetTrackingFields** apabila meluluskan entri masa.</span><span class="sxs-lookup"><span data-stu-id="f7042-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="f7042-117">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="f7042-117">**Resource Management**</span></span>

<span data-ttu-id="f7042-118">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="f7042-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f7042-119">**Cipta Ahli Pasukan** tidak memaparkan tetapan metadata persediaan penempahan untuk **Status Penempahan Terikat Lalai** dengan betul.</span><span class="sxs-lookup"><span data-stu-id="f7042-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="f7042-120">Apabila menaik taraf daripada PSA 1.X ke 3.X, proses naik taraf gagal pada **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="f7042-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="f7042-121">**Jualan**</span><span class="sxs-lookup"><span data-stu-id="f7042-121">**Sales**</span></span>

<span data-ttu-id="f7042-122">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="f7042-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="f7042-123">Hasil sebenar menukar jumlah ke mata wang projek dalam grid penjejakan.</span><span class="sxs-lookup"><span data-stu-id="f7042-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="f7042-124">Lalai mata wang lalai tidak jelas apabila mencipta baris jurnal, baris sebut harga dan baris kontrak dalam senario yang mata wang asas organisasi berbeza daripada mata wang projek.</span><span class="sxs-lookup"><span data-stu-id="f7042-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="f7042-125">Pertanyaan **Pengesahan jurnal pembetulan belum selesai** tidak ditapis oleh projek.</span><span class="sxs-lookup"><span data-stu-id="f7042-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="f7042-126">Baki jualan tidak dikira dengan betul pada projek.</span><span class="sxs-lookup"><span data-stu-id="f7042-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="f7042-127">Sebut harga berdasarkan pada kenalan gagal apabila sebut harga dicipta tanpa senarai harga.</span><span class="sxs-lookup"><span data-stu-id="f7042-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="f7042-128">Tiada spinner pemprosesan ditunjukkan apabila anda memilih **Sahkan Invois**.</span><span class="sxs-lookup"><span data-stu-id="f7042-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="f7042-129">Tiada spinner pemprosesan ditunjukkan apabila anda memilih **Cipta Invois**.</span><span class="sxs-lookup"><span data-stu-id="f7042-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="f7042-130">Menutup sebut harga sebagai kehilangan tidak membatalkan tempahan.</span><span class="sxs-lookup"><span data-stu-id="f7042-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







