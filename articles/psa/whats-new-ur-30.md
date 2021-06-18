---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 30, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Kemas kini Project Service Automation Keluaran 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010437"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="ffd0f-103">Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 30, V3</span><span class="sxs-lookup"><span data-stu-id="ffd0f-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ffd0f-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ffd0f-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ffd0f-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ffd0f-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ffd0f-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="ffd0f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="ffd0f-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 30.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="ffd0f-110">Versi ini mempunyai nombor binaan V3.10.51.61 dan secara amnya boleh didapati melalui kemas kini sendiri pada April 2021.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="ffd0f-111">Keluaran Kemas kini 30</span><span class="sxs-lookup"><span data-stu-id="ffd0f-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ffd0f-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="ffd0f-112">Bug fixes</span></span>

<span data-ttu-id="ffd0f-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="ffd0f-113">**Time and Expense**</span></span>

<span data-ttu-id="ffd0f-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="ffd0f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ffd0f-115">Ralat berlaku apabila anda mencipta dan menyimpan entri masa pada halaman **Cipta Pantas** jika medan **Peranan** dialih keluar.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="ffd0f-116">Penapis Entri Masa menggunakan operator penapis yang salah.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="ffd0f-117">Lembaran masa yang disalin tidak dipaparkan secara automatik apabila anda memilih **Salin Minggu** pada kawalan entri masa.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="ffd0f-118">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="ffd0f-118">**Resource Management**</span></span>

<span data-ttu-id="ffd0f-119">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="ffd0f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="ffd0f-120">Apabila anda melanjutkan tempahan, status tempahan ditugaskan kepada tempahan tetap adalah salah.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="ffd0f-121">Melanjutkan tempahan berkaitan status tempahan yang ditakrifkan sebagai **Terikat** dalam metadata persediaan tempahan.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="ffd0f-122">Apabila status tempahan yang sah tidak ditentukan, mesej ralat tidak disetempatkan dengan betul.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="ffd0f-123">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="ffd0f-123">**Project Management**</span></span>

<span data-ttu-id="ffd0f-124">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="ffd0f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ffd0f-125">Projek tidak boleh dicipta dalam satu mata wang dan termasuk tugas berkaitan dalam mata wang lain.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="ffd0f-126">**Jualan**</span><span class="sxs-lookup"><span data-stu-id="ffd0f-126">**Sales**</span></span>

<span data-ttu-id="ffd0f-127">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="ffd0f-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="ffd0f-128">Apabila senarai harga disalin, harga tidak dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="ffd0f-129">Menutup sebut harga sebagai gagal dimenangi apabila butiran kos mempunyai nilai untuk asal.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="ffd0f-130">Pada entiti **Tugas Projek**, **Kos yang Dianggarkan** telah dinamakan semula kepada **Kos yang Dirancang (Asas)**.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="ffd0f-131">Pengecualian rujukan nol dijana apabila invois dicipta atau dipadamkan.</span><span class="sxs-lookup"><span data-stu-id="ffd0f-131">A null reference exception is generated when invoices are created or deleted.</span></span>
