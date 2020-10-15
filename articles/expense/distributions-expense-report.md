---
title: Pengedaran pada laporan perbelanjaan
description: Apabila anda memasukkan perbelanjaan di dalam laporan perbelanjaan, anda boleh mengagih perbelanjaan merentasi berbilang projek, entiti yang sah atau akaun dalam organisasi anda.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908396"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="b4a51-103">Pengedaran pada laporan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="b4a51-103">Distributions on an expense report</span></span>

<span data-ttu-id="b4a51-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b4a51-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b4a51-105">Apabila anda memasukkan perbelanjaan di dalam laporan perbelanjaan, anda boleh mengagihkan perbelanjaan merentasi berbilang projek, dimensi kewangan atau akaun dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="b4a51-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="b4a51-106">Sebagai contoh, Nancy, wakil jualan Fabrikam, mengembara dari Copenhagen ke Frankfurt.</span><span class="sxs-lookup"><span data-stu-id="b4a51-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="b4a51-107">Di Frankfurt, Nancy bertemu dengan dua organisasi untuk membincangkan projek berasingan untuk setiap organisasi.</span><span class="sxs-lookup"><span data-stu-id="b4a51-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="b4a51-108">Nancy menghabiskan masa tujuh hari perniagaan bekerja dengan organisasi A pada projek A, dan tiga hari perniagaan bekerja dengan organisasi B pada projek B.</span><span class="sxs-lookup"><span data-stu-id="b4a51-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="b4a51-109">Kerana Nancy mengendalikan dua projek berasingan ketika berada di Frankfurt, apabila beliau memasuki Laporan perbelanjaan, Nancy mengagihkan perbelanjaan yang sesuai untuk setiap projek.</span><span class="sxs-lookup"><span data-stu-id="b4a51-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="b4a51-110">Jadual berikut menunjukkan cara Nancy mengagihkan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="b4a51-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="b4a51-111">Jenis perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="b4a51-111">Expense type</span></span> | <span data-ttu-id="b4a51-112">Jumlah amaun perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="b4a51-112">Total expense amount</span></span> | <span data-ttu-id="b4a51-113">Amaun yang diagihkan kepada projek A</span><span class="sxs-lookup"><span data-stu-id="b4a51-113">Amount distributed to project A</span></span> | <span data-ttu-id="b4a51-114">Amaun yang diagihkan kepada projek B</span><span class="sxs-lookup"><span data-stu-id="b4a51-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="b4a51-115">Tambang kereta api</span><span class="sxs-lookup"><span data-stu-id="b4a51-115">Train fare</span></span>   | <span data-ttu-id="b4a51-116">DKK 578</span><span class="sxs-lookup"><span data-stu-id="b4a51-116">DKK 578</span></span>              | <span data-ttu-id="b4a51-117">DKK 405</span><span class="sxs-lookup"><span data-stu-id="b4a51-117">DKK 405</span></span>                         | <span data-ttu-id="b4a51-118">DKK 173</span><span class="sxs-lookup"><span data-stu-id="b4a51-118">DKK 173</span></span>                         |
| <span data-ttu-id="b4a51-119">Hotel</span><span class="sxs-lookup"><span data-stu-id="b4a51-119">Hotel</span></span>        | <span data-ttu-id="b4a51-120">EUR 725</span><span class="sxs-lookup"><span data-stu-id="b4a51-120">EUR 725</span></span>              | <span data-ttu-id="b4a51-121">EUR 557</span><span class="sxs-lookup"><span data-stu-id="b4a51-121">EUR 557</span></span>                         | <span data-ttu-id="b4a51-122">EUR 168</span><span class="sxs-lookup"><span data-stu-id="b4a51-122">EUR 168</span></span>                         |
| <span data-ttu-id="b4a51-123">Hidangan</span><span class="sxs-lookup"><span data-stu-id="b4a51-123">Meals</span></span>        | <span data-ttu-id="b4a51-124">EUR 346</span><span class="sxs-lookup"><span data-stu-id="b4a51-124">EUR 346</span></span>              | <span data-ttu-id="b4a51-125">EUR 284</span><span class="sxs-lookup"><span data-stu-id="b4a51-125">EUR 284</span></span>                         | <span data-ttu-id="b4a51-126">EUR 62</span><span class="sxs-lookup"><span data-stu-id="b4a51-126">EUR 62</span></span>                          |
