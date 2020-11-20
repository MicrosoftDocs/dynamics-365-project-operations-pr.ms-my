---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 14, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124829"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="a65b9-103">Project Service Automation, Keluaran Kemas kini 14, V3</span><span class="sxs-lookup"><span data-stu-id="a65b9-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="a65b9-104">Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a65b9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a65b9-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="a65b9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a65b9-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a65b9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a65b9-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="a65b9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a65b9-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a65b9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a65b9-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 14.</span><span class="sxs-lookup"><span data-stu-id="a65b9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="a65b9-110">Versi ini mempunyai nombor binaan V3.10.4.21 dan tersedia pada jadual berikut:</span><span class="sxs-lookup"><span data-stu-id="a65b9-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="a65b9-111">**Ketersediaan umum (kemas kini kendiri):** Januari 2020</span><span class="sxs-lookup"><span data-stu-id="a65b9-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="a65b9-112">**Kemas kini automatik:** Februari 2020</span><span class="sxs-lookup"><span data-stu-id="a65b9-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="a65b9-113">Keluaran Kemas kini 14</span><span class="sxs-lookup"><span data-stu-id="a65b9-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="a65b9-114">Peningkatan</span><span class="sxs-lookup"><span data-stu-id="a65b9-114">Enhancements</span></span>

- <span data-ttu-id="a65b9-115">Sales</span><span class="sxs-lookup"><span data-stu-id="a65b9-115">Sales</span></span>

     - <span data-ttu-id="a65b9-116">Nilai medan tersuai daripada **Butiran Baris Sebut Harga** disalin kepada **Butiran Baris Kontrak Projek** apabila sebut harga dikemas kini kepada **Ditutup sebagai menang**.</span><span class="sxs-lookup"><span data-stu-id="a65b9-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="a65b9-117">Projek yang telah disahkan boleh **Ditutup sebagai kalah**.</span><span class="sxs-lookup"><span data-stu-id="a65b9-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="a65b9-118">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="a65b9-118">Resource Management</span></span>

     - <span data-ttu-id="a65b9-119">Apabila melanjutkan tempahan, pengguna akan digesa dengan kotak dialog pengesahan untuk meringkaskan hasil tempahan dan menyediakan pautan untuk Kekalkan Tempahan.</span><span class="sxs-lookup"><span data-stu-id="a65b9-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="a65b9-120">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="a65b9-120">Bug fixes</span></span>

- <span data-ttu-id="a65b9-121">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="a65b9-121">Time and Expense</span></span>

     - <span data-ttu-id="a65b9-122">Dibetulkan: Memperbaik pengalaman pengguna apabila pengguna tidak memilih sebarang entri untuk dibetulkan.</span><span class="sxs-lookup"><span data-stu-id="a65b9-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="a65b9-123">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="a65b9-123">Resource Management</span></span>

     - <span data-ttu-id="a65b9-124">Dibetulkan: Menempah sumber beberapa kali memenuhkan nama sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="a65b9-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="a65b9-125">Sales</span><span class="sxs-lookup"><span data-stu-id="a65b9-125">Sales</span></span>

     - <span data-ttu-id="a65b9-126">Dibetulkan: Jumlah harga jualan tidak dikira sehingga pengguna juga menginput harga kos untuk anggaran perbelanjaan pada projek.</span><span class="sxs-lookup"><span data-stu-id="a65b9-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="a65b9-127">Dibetulkan: Tutup sebut harga sebagai **Menang** gagal jika kontrak projek yang berkaitan bukan dalam keadaan **Draf**.</span><span class="sxs-lookup"><span data-stu-id="a65b9-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

