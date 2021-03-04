---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 12, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143839"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="dc056-103">Project Service Automation, Keluaran Kemas kini 12, V3</span><span class="sxs-lookup"><span data-stu-id="dc056-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dc056-104">Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="dc056-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="dc056-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="dc056-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dc056-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dc056-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dc056-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="dc056-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="dc056-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dc056-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dc056-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 12.</span><span class="sxs-lookup"><span data-stu-id="dc056-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="dc056-110">Versi ini mempunyai nombor binaan V3.10.2.34 dan secara amnya boleh didapati melalui kemas kini kendiri pada Oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="dc056-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="dc056-111">Keluaran Kemas kini 12</span><span class="sxs-lookup"><span data-stu-id="dc056-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dc056-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="dc056-112">Bug fixes</span></span>

- <span data-ttu-id="dc056-113">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="dc056-113">Time and Expense</span></span>

    - <span data-ttu-id="dc056-114">Dibetulkan: Mesej ralat entri masa telah dikemas kini dengan konteks yang lebih berkaitan.</span><span class="sxs-lookup"><span data-stu-id="dc056-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="dc056-115">Dibetulkan: Grid entri masa dan jadual memaparkan bar skrol menegak dengan betul apabila diperlukan.</span><span class="sxs-lookup"><span data-stu-id="dc056-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="dc056-116">Dibetulkan: Perbelanjaan dan entri masa yang telah diserahkan boleh diluluskan.</span><span class="sxs-lookup"><span data-stu-id="dc056-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="dc056-117">Dibetulkan: Mesej dialog batalkan pengesahan kelulusan telah dibetulkan untuk menggambarkan status kelulusan apabila diubah daripada **Diluluskan** kepada **Diserahkan**.</span><span class="sxs-lookup"><span data-stu-id="dc056-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="dc056-118">Dibetulkan: Medan **Harga**, **Unit** dan **Kuantiti** kini dikunci pada rekod Perbelanjaan selepas ia telah diluluskan.</span><span class="sxs-lookup"><span data-stu-id="dc056-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="dc056-119">Pengurusan Projek</span><span class="sxs-lookup"><span data-stu-id="dc056-119">Project Management</span></span>

    - <span data-ttu-id="dc056-120">Dibetulkan: Tindakan **Baharu** pada borang utama **Ahli pasukan** telah dialih keluar.</span><span class="sxs-lookup"><span data-stu-id="dc056-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="dc056-121">Dibetulkan: Penugasan sumber telah dikemas kini pada akaun untuk ralat pembundaran tidak tepat, yang membawa kepada anjakan dalam tarikh akhir tugas.</span><span class="sxs-lookup"><span data-stu-id="dc056-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="dc056-122">Dibetulkan: Dalam grid tugas, ralat bahagian pelayan yang berkaitan akan ditunjukkan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="dc056-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="dc056-123">Dibetulkan: Nama ahli pasukan kini dipaparkan pada pemilih orang tugas dan bukannya nama kedudukan.</span><span class="sxs-lookup"><span data-stu-id="dc056-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="dc056-124">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="dc056-124">Resource Management</span></span>

    - <span data-ttu-id="dc056-125">Dibetulkan: Butiran keperluan sumber untuk projek yang dicipta daripada templat kini menggunakan kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="dc056-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="dc056-126">Dibetulkan: Kemahiran dan kecekapan kini lalai daripada data induk peranan kepada keperluan sumber yang dicipta untuk peranan tersebut.</span><span class="sxs-lookup"><span data-stu-id="dc056-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="dc056-127">Sales</span><span class="sxs-lookup"><span data-stu-id="dc056-127">Sales</span></span>

    - <span data-ttu-id="dc056-128">Dibetulkan: ID objek duplikasi ditemui pada borang utama **Kontrak**.</span><span class="sxs-lookup"><span data-stu-id="dc056-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="dc056-129">Dibetulkan: Logik telah dikemas kini untuk menjadikan tab **Analisis Sebut Harga** boleh dilihat supaya ia memaparkan persediaan metadata tab.</span><span class="sxs-lookup"><span data-stu-id="dc056-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="dc056-130">Dibetulkan: Tarikh perakaunan pada rekod sebenar kini datang daripada tarikh bagi tarikh entri masa/perbelanjaan dan bukan tarikh kelulusan.</span><span class="sxs-lookup"><span data-stu-id="dc056-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
