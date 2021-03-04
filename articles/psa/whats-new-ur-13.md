---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 13, V3
description: Topik ini memberikan maklumat tentang perkara baharu dalam Keluaran Kemas kini Project Service Automation 13, V3.
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
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147259"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="29654-103">Project Service Automation, Keluaran Kemas kini 13, V3</span><span class="sxs-lookup"><span data-stu-id="29654-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="29654-104">Kami gembira untuk mengumumkan kemas kini terbaharu untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="29654-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="29654-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="29654-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="29654-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="29654-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="29654-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online dan pergi ke halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="29654-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="29654-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="29654-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="29654-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 13.</span><span class="sxs-lookup"><span data-stu-id="29654-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="29654-110">Versi ini mempunyai nombor binaan V3.10.3.18 dan tersedia pada jadual berikut:</span><span class="sxs-lookup"><span data-stu-id="29654-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="29654-111">**Ketersediaan umum (kemas kini kendiri):** November 2019</span><span class="sxs-lookup"><span data-stu-id="29654-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="29654-112">**Kemas kini automatik:** Disember 2019</span><span class="sxs-lookup"><span data-stu-id="29654-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="29654-113">Keluaran Kemas kini 13</span><span class="sxs-lookup"><span data-stu-id="29654-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="29654-114">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="29654-114">Bug fixes</span></span>

- <span data-ttu-id="29654-115">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="29654-115">Time and Expense</span></span>

     - <span data-ttu-id="29654-116">Dibetulkan: Fungsi carian pada halaman **Kelulusan perbelanjaan** tidak berfungsi apabila mencari mengikut tujuan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="29654-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="29654-117">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="29654-117">Resource Management</span></span>

     - <span data-ttu-id="29654-118">Dibetulkan: Nombor dalam penyesuaian telah dikemas kini untuk dijajarkan ke kanan.</span><span class="sxs-lookup"><span data-stu-id="29654-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="29654-119">Dibetulkan: Sumber yang Dinamakan tidak boleh ditugaskan kepada tugas melalui tab **Jadual**.</span><span class="sxs-lookup"><span data-stu-id="29654-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="29654-120">Pengurusan Projek</span><span class="sxs-lookup"><span data-stu-id="29654-120">Project Management</span></span>

     - <span data-ttu-id="29654-121">Dibetulkan: Pengecualian rujukan nol semasa menugaskan ahli pasukan apabila **TransactionType** tidak mempunyai maklumat persediaan untuk **Unit** dan **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="29654-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="29654-122">Sales</span><span class="sxs-lookup"><span data-stu-id="29654-122">Sales</span></span>

     - <span data-ttu-id="29654-123">Dibetulkan: Rekod jenis transaksi duplikasi mengembalikan ralat apabila rekod harga peranan dicipta.</span><span class="sxs-lookup"><span data-stu-id="29654-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="29654-124">Tetap: Butang tambahan untuk **Peluang Baharu**, **Sebut Harga**, **Baris Pesanan** dan **Tambah Produk** boleh dilihat dalam perintah untuk subgrid Peluang, Sebut Harga, Produk Pesanan dan Baris berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="29654-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


