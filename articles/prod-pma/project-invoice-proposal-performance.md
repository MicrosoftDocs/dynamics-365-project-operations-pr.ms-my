---
title: Prestasi cadangan invois projek
description: Topik ini menyediakan maklumat tentang peningkatan prestasi untuk cadangan invois projek.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269801"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="82883-103">Prestasi cadangan invois projek</span><span class="sxs-lookup"><span data-stu-id="82883-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82883-104">Apabila anda mencipta cadangan invois baharu, anda mungkin menghadapi masalah prestasi apabila bilangan projek dan subprojek meningkat.</span><span class="sxs-lookup"><span data-stu-id="82883-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="82883-105">Untuk meningkatkan prestasi, ciri tersedia yang mengurangkan masa yang diperlukan untuk mencipta cadangan invois baharu bagi transaksi projek yang disiarkan.</span><span class="sxs-lookup"><span data-stu-id="82883-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="82883-106">Dayakan peningkatan prestasi cadangan invois projek</span><span class="sxs-lookup"><span data-stu-id="82883-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="82883-107">Untuk mendayakan ciri peningkatan prestasi cadangan invois projek, lengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="82883-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="82883-108">Pergi ke **Pengurusan ciri** > **Semua**.</span><span class="sxs-lookup"><span data-stu-id="82883-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="82883-109">Dalam senarai ciri, cari **Peningkatan prestasi cadangan invois projek**.</span><span class="sxs-lookup"><span data-stu-id="82883-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="82883-110">Pilih **Dayakan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="82883-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="82883-111">Segarkan semula pelayar anda, dan kemudian cipta cadangan invois baharu.</span><span class="sxs-lookup"><span data-stu-id="82883-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="82883-112">Matikan peningkatan prestasi cadangan invois projek</span><span class="sxs-lookup"><span data-stu-id="82883-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="82883-113">Lengkapkan langkah berikut untuk mematikan ciri peningkatan prestasi cadangan invois projek.</span><span class="sxs-lookup"><span data-stu-id="82883-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="82883-114">Pergi ke **Pengurusan ciri** > **Semua**.</span><span class="sxs-lookup"><span data-stu-id="82883-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="82883-115">Dalam senarai ciri, cari **Peningkatan prestasi cadangan invois projek**.</span><span class="sxs-lookup"><span data-stu-id="82883-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="82883-116">Pilih **Nyahdayakan**.</span><span class="sxs-lookup"><span data-stu-id="82883-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="82883-117">Segar semula pelayar anda.</span><span class="sxs-lookup"><span data-stu-id="82883-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="82883-118">Prestasi cadangan invois tidak boleh digunakan apabila peraturan pengebilan didayakan.</span><span class="sxs-lookup"><span data-stu-id="82883-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="82883-119">Semasa proses kelompok untuk mencipta cadangan invois, bilangan subtugas akan membahagikan tugas kepada bilangan maksimum berdasarkan bilang kontrak dengan transaksi boleh diinvois tanpa mengira nombor yang telah anda masukkan.</span><span class="sxs-lookup"><span data-stu-id="82883-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="82883-120">Contohnya, jika anda memasukkan **3** untuk bilangan subtugas untuk penciptaan cadangan invois dalam kelompok dan hanya terdapat dua kontrak dengan transaksi boleh diinvois, hanya dua subtugas dicipta.</span><span class="sxs-lookup"><span data-stu-id="82883-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
