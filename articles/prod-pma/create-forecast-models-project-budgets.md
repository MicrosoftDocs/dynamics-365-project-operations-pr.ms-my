---
title: Cipta model ramalan untuk belanjawan projek
description: Topik ini menerangkan cara untuk mencipta model ramalan untuk belanjawan selebihnya.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081364"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="0ffec-103">Cipta model ramalan untuk belanjawan projek</span><span class="sxs-lookup"><span data-stu-id="0ffec-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ffec-104">Topik ini menerangkan cara untuk mencipta model ramalan untuk belanjawan selebihnya.</span><span class="sxs-lookup"><span data-stu-id="0ffec-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="0ffec-105">Projek yang tertakluk kepada kawalan belanjawan menggunakan dua jenis belanjawan: asal dan selebihnya.</span><span class="sxs-lookup"><span data-stu-id="0ffec-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="0ffec-106">Apabila anda mencipta belanjawan projek, anda mesti menentukan model ramalan belanjawan asal dan selebihnya yang dicipta dalam halaman **Model ramalan**.</span><span class="sxs-lookup"><span data-stu-id="0ffec-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="0ffec-107">Belanjawan projek berdasarkan model yang ditentukan dicipta apabila anda melaksanakan belanjawan projek.</span><span class="sxs-lookup"><span data-stu-id="0ffec-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="0ffec-108">Model ramalan yang digunakan untuk kawalan belanjawan tidak boleh mempunyai submodel atau digunakan sebagai submodel.</span><span class="sxs-lookup"><span data-stu-id="0ffec-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="0ffec-109">Pilih **Pengurusan dan perakaunan projek** > **Penyediaan** > **Ramalan**  > **Model ramalan**.</span><span class="sxs-lookup"><span data-stu-id="0ffec-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="0ffec-110">Pilih **Baharu** untuk mencipta model ramalan baharu dan kemudian masukkan nombor ID model dan nama untuk model baharu itu.</span><span class="sxs-lookup"><span data-stu-id="0ffec-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="0ffec-111">Tetapkan pilihan **Berhenti** kepada **Ya** untuk mengelakkan sebarang perubahan pada baris ramalan untuk model ramalan.</span><span class="sxs-lookup"><span data-stu-id="0ffec-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="0ffec-112">Jika baris ramalan yang dikaitkan dengan model tersebut sepatutnya menjana ramalan aliran tunai dalam lejar umum, tetapkan **Sertakan dalam Ramalan aliran tunai** kepada **Ya.**</span><span class="sxs-lookup"><span data-stu-id="0ffec-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="0ffec-113">Untuk menggunakan tarikh projek sebagai tarikh invois, tetapkan **Tarikh Invoice Ramalan** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="0ffec-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="0ffec-114">Dalam medan **Jenis belanjawan** , pilih salah satu daripada jenis model berikut:</span><span class="sxs-lookup"><span data-stu-id="0ffec-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="0ffec-115">**Belanjawan asal** : Gunakan jumlah belanjawan asal yang dilaksanakan apabila belanjawan awal dicipta dan diluluskan.</span><span class="sxs-lookup"><span data-stu-id="0ffec-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="0ffec-116">**Belanjawan selebihnya** : Gunakan jumlah belanjawan selebihnya semasa hayat projek.</span><span class="sxs-lookup"><span data-stu-id="0ffec-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="0ffec-117">Baki dalam model ramalan ini dikurangkan dengan transaksi sebenar dan ditambah atau dikurangkan mengikut semakan belanjawan.</span><span class="sxs-lookup"><span data-stu-id="0ffec-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="0ffec-118">**Bawa ke hadapan** : Gunakan jumlah belanjawan dibawa ke hadapan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="0ffec-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="0ffec-119">Bawa ke hadapan ialah satu proses pilihan yang boleh dijalankan untuk memindahkan jumlah belanjawan yang tidak digunakan daripada satu tahun fiskal kepada tahun fiskal yang lain.</span><span class="sxs-lookup"><span data-stu-id="0ffec-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="0ffec-120">Tetapkan pilihan berikut mengikut keperluan:</span><span class="sxs-lookup"><span data-stu-id="0ffec-120">Set the following options as required:</span></span>

   - <span data-ttu-id="0ffec-121">Dayakan **Tarikh invois ramalan** untuk menggunakan tarikh projek sebagai tarikh invois.</span><span class="sxs-lookup"><span data-stu-id="0ffec-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="0ffec-122">Dayakan **Ramalan dengan WIP** untuk meramal berdasarkan kerja yang sedang berjalan (WIP) dan kemudian, pilih jenis WIP.</span><span class="sxs-lookup"><span data-stu-id="0ffec-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="0ffec-123">Anda boleh mengekalkan **Jenis belanjawan** lalai sebagai **Tiada** atau masukkan jenis baharu.</span><span class="sxs-lookup"><span data-stu-id="0ffec-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="0ffec-124">Jenis belanjawan tidak boleh ditukar selepas anda menukar rekod.</span><span class="sxs-lookup"><span data-stu-id="0ffec-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="0ffec-125">Jika anda menukar jenis belanjawan lalai, semua pilihan lain tidak akan tersedia untuk kemas kini dan anda tidak boleh menggunakan semula model ramalan ini.</span><span class="sxs-lookup"><span data-stu-id="0ffec-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

