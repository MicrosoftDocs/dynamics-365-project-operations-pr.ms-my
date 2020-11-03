---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 13, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 13, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081188"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="75419-103">Project Service Automation, Keluaran Kemas kini 13, V3</span><span class="sxs-lookup"><span data-stu-id="75419-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="75419-104">Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="75419-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="75419-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="75419-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="75419-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="75419-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="75419-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="75419-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="75419-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="75419-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="75419-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 13.</span><span class="sxs-lookup"><span data-stu-id="75419-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="75419-110">Versi ini mempunyai nombor binaan V3.10.3.18 dan tersedia pada jadual berikut:</span><span class="sxs-lookup"><span data-stu-id="75419-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="75419-111">**Ketersediaan umum (kemas kini kendiri):** November 2019</span><span class="sxs-lookup"><span data-stu-id="75419-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="75419-112">**Kemas kini automatik:** Disember 2019</span><span class="sxs-lookup"><span data-stu-id="75419-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="75419-113">Keluaran Kemas kini 13</span><span class="sxs-lookup"><span data-stu-id="75419-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="75419-114">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="75419-114">Bug fixes</span></span>

- <span data-ttu-id="75419-115">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="75419-115">Time and Expense</span></span>

     - <span data-ttu-id="75419-116">Dibetulkan: Fungsi carian pada halaman **Kelulusan perbelanjaan** tidak berfungsi apabila mencari mengikut tujuan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="75419-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="75419-117">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="75419-117">Resource Management</span></span>

     - <span data-ttu-id="75419-118">Dibetulkan: Nombor dalam penyesuaian telah dikemas kini untuk dijajarkan ke kanan.</span><span class="sxs-lookup"><span data-stu-id="75419-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="75419-119">Dibetulkan: Sumber yang Dinamakan tidak boleh ditugaskan kepada tugas melalui tab **Jadual**.</span><span class="sxs-lookup"><span data-stu-id="75419-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="75419-120">Pengurusan Projek</span><span class="sxs-lookup"><span data-stu-id="75419-120">Project Management</span></span>

     - <span data-ttu-id="75419-121">Dibetulkan: Pengecualian rujukan nol semasa menugaskan ahli pasukan apabila **TransactionType** tidak mempunyai maklumat persediaan untuk **Unit** dan **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="75419-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="75419-122">Sales</span><span class="sxs-lookup"><span data-stu-id="75419-122">Sales</span></span>

     - <span data-ttu-id="75419-123">Dibetulkan: Rekod jenis transaksi duplikasi mengembalikan ralat apabila rekod harga peranan dicipta.</span><span class="sxs-lookup"><span data-stu-id="75419-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="75419-124">Dibetulkan: Butang tambahan untuk **Peluang Baharu** , **Sebut Harga** , **Baris Pesanan** dan **Tambah produk** boleh dilihat dalam perintah untuk Peluang, Sebut Harga, Produk Pesanan dan sub grid Baris berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="75419-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


