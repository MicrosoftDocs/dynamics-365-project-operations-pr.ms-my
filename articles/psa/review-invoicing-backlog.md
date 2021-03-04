---
title: Semak invois yang tertunggak pada projek dan kontrak projek
description: Topik ini memberikan maklumat mengenai cara untuk mengkaji masa, perbelanjaan dan tunggakan produk, dan cara menandanya sebagai bersedia untuk penginvoisan.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150499"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="b5eef-103">Semak invois yang tertunggak pada projek dan kontrak projek</span><span class="sxs-lookup"><span data-stu-id="b5eef-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b5eef-104">Apabila transaksi bersedia untuk mempunyai invois yang dicipta dan diproses, transaksi sepatutnya ditanda **Bersedia untuk dinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="b5eef-105">Topik ini menghuraikan jenis transaksi yang boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="b5eef-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="b5eef-106">Semak semula tunggakan pengebilan masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="b5eef-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="b5eef-107">Apabila masa kemasukan atau perbelanjaan diserahkan dan diluluskan untuk projek, PSA mewujudkan projek sebenar.</span><span class="sxs-lookup"><span data-stu-id="b5eef-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="b5eef-108">Jika kombinasi projek dan kelas transaksi dipetakan ke satu baris kontrak untuk projek masa dan bahan, dua aktual dicipta apabila kemasukan diluluskan:</span><span class="sxs-lookup"><span data-stu-id="b5eef-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="b5eef-109">Kos sebenar</span><span class="sxs-lookup"><span data-stu-id="b5eef-109">Cost actual</span></span> 
- <span data-ttu-id="b5eef-110">Jualan sebenar belum dibilkan</span><span class="sxs-lookup"><span data-stu-id="b5eef-110">Unbilled sales actual</span></span>

<span data-ttu-id="b5eef-111">Jualan sebenar yang belum dibilkan mewakili log pengebilan dan status pengebilan mereka mesti ditetapkan kepada **Bersedia untuk Diinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="b5eef-112">Apabila invois projek dicipta, jualan sebenar yang tidak dibilkan yang ditandakan **Bersedia untuk Diinvois** disalin sebagai butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="b5eef-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="b5eef-113">Untuk menyemak tunggakan pengebilan untuk masa dan bahan, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Masa dan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="b5eef-114">Pilih semua aplikasi jualan yang tidak dibilkan yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.**</span><span class="sxs-lookup"><span data-stu-id="b5eef-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="b5eef-115">Status pengebilan bagi aktual ini ditukar kepada **Bersedia untuk Diinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Tunggakan pengebilan masa dan bahan](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="b5eef-117">Semak semula tunggakan pengebilan produk</span><span class="sxs-lookup"><span data-stu-id="b5eef-117">Review the product billing backlog</span></span>

<span data-ttu-id="b5eef-118">Dalam PSA, apabila kontrak projek mempunyai talian kontrak berasaskan produk, baris tersebut dipertimbangkan untuk penginvoisan apabila invois dicipta untuk kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="b5eef-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="b5eef-119">Sebarang produk yang mempunyai baris kontrak yang ditanda **Bersedia untuk Diinvois** disalin ke invois projek sebagai baris invois projek.</span><span class="sxs-lookup"><span data-stu-id="b5eef-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="b5eef-120">Untuk menyemak tunggakan pengebilan untuk produk, pergi ke **Jualan** \> **Pengebilan** \> **Tunggakan Pengebilan Produk**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="b5eef-121">Pilih semua baris kontrak berdasarkan produk yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk Diinvois.**</span><span class="sxs-lookup"><span data-stu-id="b5eef-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="b5eef-122">Status pengebilan baris ini ditukar kepada **Bersedia untuk Diinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Tunggakan pengebilan produk](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="b5eef-124">Tinjauan pencapaian pengebilan pada kontrak harga tetap</span><span class="sxs-lookup"><span data-stu-id="b5eef-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="b5eef-125">Setiap baris kontrak projek yang mempunyai kaedah pengebilan harga tetap mesti mentakrifkan pencapaian kontrak.</span><span class="sxs-lookup"><span data-stu-id="b5eef-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="b5eef-126">Pencapaian kontrak ini hanya boleh diinvois hanya jika ia ditandakan **Bersedia untuk Diinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="b5eef-127">Untuk menyemak semula pencapaian pengebilan, pergi ke **Jualan** \> **Pengebilan** \> **Pencapaian Harga Tetap**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="b5eef-128">Pilih semua pencapaian yang bersedia untuk diinvois dan kemudian pilih **Bersedia untuk diinvois.**</span><span class="sxs-lookup"><span data-stu-id="b5eef-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="b5eef-129">Status pengebilan pencapaian ini ditukar kepada **Bersedia untuk Diinvois**.</span><span class="sxs-lookup"><span data-stu-id="b5eef-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Pencapaian harga tetap](media/FPBacklog.png)
