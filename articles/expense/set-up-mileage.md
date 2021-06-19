---
title: Sediakan perbatuan menggunakan peringkat kadar perbatuan
description: Topik ini menyediakan maklumat tentang kadar perbatuan dan peringkat kadar perbatuan.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083682"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a><span data-ttu-id="a299f-103">Sediakan perbatuan menggunakan peringkat kadar perbatuan</span><span class="sxs-lookup"><span data-stu-id="a299f-103">Set up mileage using mileage rate tiers</span></span>

<span data-ttu-id="a299f-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="a299f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a299f-105">Apabila perbelanjaan dilaporkan dan kategori perbelanjaan dipilih ialah **Perbatuan**, jumlah untuk baris perbelanjaan dikira mengikut jumlah *kadar setiap perbatuan*.</span><span class="sxs-lookup"><span data-stu-id="a299f-105">When an expense is reported and the selected expense category is **Mileage**, the amount for that expense line is calculated according to the *rate per mileage* amount.</span></span> <span data-ttu-id="a299f-106">Jumlah ini ditentukan dengan menggunakan peringkat perbatuan yang ditakrifkan atau jika tiada peringkat kadar perbatuan disediakan, dengan mengikut kadar standard perbatuan.</span><span class="sxs-lookup"><span data-stu-id="a299f-106">This amount is determined by using defined mileage tiers or, if no mileage rate tiers are set up, by following a standard rate of mileage.</span></span> 

<span data-ttu-id="a299f-107">Peringkat kadar perbatuan boleh ditetapkan dengan pergi ke **Pengurusan Perbelanjaan** > **Persediaan** > **Umum** > **Kategori perbelanjaan** > **Perbatuan** > **Persediaan kategori**.</span><span class="sxs-lookup"><span data-stu-id="a299f-107">Mileage rate tiers can be set up by going to **Expense Management** > **Setup** > **General** > **Expense categories** > **Mileage** > **Category setup**.</span></span>

<span data-ttu-id="a299f-108">Selepas anda menaik taraf kepada 10.0.18, jika organisasi anda menggunakan kategori perbelanjaan perbatuan, pertimbangkan mendayakan ciri perbatuan selepas menyemak perubahan reka bentuk di bawah.</span><span class="sxs-lookup"><span data-stu-id="a299f-108">After you upgrade to 10.0.18, if your organization uses the mileage expense category, consider enabling the mileage feature after reviewing the design changes below.</span></span> 

<span data-ttu-id="a299f-109">Reka bentuk baharu peringkat kadar perbatuan memberi kesan kepada cara nilai dalam medan **Kuantiti** diproses.</span><span class="sxs-lookup"><span data-stu-id="a299f-109">The new design of mileage rate tiers impacts how the value in the **Quantity** field is processed.</span></span> <span data-ttu-id="a299f-110">Sebelum keluaran 10.0.18, nilai dalam medan **Kuantiti** dianggap sebagai had yang lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="a299f-110">Prior to the release of 10.0.18, the value in the **Quantity** field was considered to be the lower limit.</span></span> <span data-ttu-id="a299f-111">Apabila pengumpulan melepasi nilai tersebut, kadar yang berkaitan digunakan.</span><span class="sxs-lookup"><span data-stu-id="a299f-111">When accumulation crossed that value, the corresponding rate was used.</span></span>  <span data-ttu-id="a299f-112">Mengikut10.0.18, nilai dalam medan **Kuantiti** dianggap had lebih atas.</span><span class="sxs-lookup"><span data-stu-id="a299f-112">As of 10.0.18, the value in the **Quantity** field is considered the upper limit.</span></span> <span data-ttu-id="a299f-113">Kadar yang sepadan digunakan apabila pengumpulan perbatuan kurang daripada nilai dalam medan **Kuantiti**.</span><span class="sxs-lookup"><span data-stu-id="a299f-113">The corresponding rate is used when mileage accumulation is less than the value in the **Quantity** field.</span></span>  <span data-ttu-id="a299f-114">Model baharu untuk peringkat perbatuan membantu dengan konsistensi merentasi peringkat perbatuan dan kebolehgunaan yang lebih baik.</span><span class="sxs-lookup"><span data-stu-id="a299f-114">The new model for mileage tiers helps with consistency across mileage tiers and better usability.</span></span>   

<span data-ttu-id="a299f-115">Semua laporan perbelanjaan yang diluluskan akan dikira semula semasa penyiaran mengikut reka bentuk baharu.</span><span class="sxs-lookup"><span data-stu-id="a299f-115">All approved expense reports will be recalculated during posting according to the new design.</span></span>

## <a name="example"></a><span data-ttu-id="a299f-116">Contoh</span><span class="sxs-lookup"><span data-stu-id="a299f-116">Example</span></span>
 
### <a name="before-version-10018"></a><span data-ttu-id="a299f-117">Sebelum versi 10.0.18</span><span class="sxs-lookup"><span data-stu-id="a299f-117">Before version 10.0.18</span></span>
<span data-ttu-id="a299f-118">Dengan dua peringkat kadar perbatuan, medan **Kuantiti** dalam setiap peringkat mewakili had perbatuan yang lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="a299f-118">With two mileage rate tiers, the **Quantity** field in each tier represents the lower mileage limit.</span></span> <span data-ttu-id="a299f-119">Pada masa ini, peringkat satu mempunyai nilai sifar (0) dan kadar 0.45 dan periingkat dua mempunyai nilai 1000 dan kadar 0.25.</span><span class="sxs-lookup"><span data-stu-id="a299f-119">Currently, tier one has a value of zero (0) and a rate of 0.45, and tier two has a value of 1000 and a rate of 0.25.</span></span> <span data-ttu-id="a299f-120">Jika perbatuan atau kilometer yang terkumpul melepasi nilai dalam medan, kadar berkaitan digunakan.</span><span class="sxs-lookup"><span data-stu-id="a299f-120">If the accumulated miles or kilometers crosses the value in the field, the related rate is used.</span></span> <span data-ttu-id="a299f-121">Jika tiada baris dengan kuantiti sifar, sistem menggunakan kadar perbatuan yang ditakrifkan dalam pengurusan Perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="a299f-121">If there's no line with zero quantity, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="a299f-122">Jika pekerja menyerahkan laporan perbelanjaan dengan 1,500 batu, dua baris perbatuan pada laporan perbelanjaan yang disiarkan akan menjadi: 1000 (kadar 0.45) + 500 (kadar 0.25) = 575.00.</span><span class="sxs-lookup"><span data-stu-id="a299f-122">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575.00.</span></span>

### <a name="after-version-10018"></a><span data-ttu-id="a299f-123">Selepas versi 10.0.18</span><span class="sxs-lookup"><span data-stu-id="a299f-123">After version 10.0.18</span></span>
<span data-ttu-id="a299f-124">Dalam 10.0.18, medan **Kuantiti** dalam setiap peringkat mewakili had lebih atas peringkat.</span><span class="sxs-lookup"><span data-stu-id="a299f-124">In 10.0.18, the **Quantity** field in each tier represents the upper limit of the tier.</span></span> <span data-ttu-id="a299f-125">Pada masa ini, peringkat satu mempunyai nilai sifar 999 dan kadar 0.45 dan periingkat dua mempunyai nilai 999,999,999.00 dan kadar 0.25.</span><span class="sxs-lookup"><span data-stu-id="a299f-125">Currently, tier one has a value of 999 and a rate of 0.45, and tier two has a value of 999,999,999.00 and a rate of 0.25.</span></span> <span data-ttu-id="a299f-126">Jika perbatuan atau kilometer yang terkumpul melepasi nilai dalam medan **Kuantiti**, kadar berkaitan digunakan.</span><span class="sxs-lookup"><span data-stu-id="a299f-126">If the accumulated miles or kilometers crosses the value in the **Quantity** field, the related rate is used.</span></span> <span data-ttu-id="a299f-127">Jika melebihi semua had lebih atas, sistem menggunakan kadar perbatuan yang ditakrifkan dalam pengurusan Perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="a299f-127">If all upper limits are exceeded, the system uses the rate of mileage that is defined in Expense management.</span></span> 
 
<span data-ttu-id="a299f-128">Untuk mengira dengan betul senario yang sama, peringkat yang ditetapkan mesti ditukar.</span><span class="sxs-lookup"><span data-stu-id="a299f-128">To correctly calculate the same scenario, the tier set up must be changed.</span></span> <span data-ttu-id="a299f-129">Medan **Kuantiti** dalam peringkat satu mempunyai nilai 999.00 dan nilai 999,999,999.00 dalam peringkat dua.</span><span class="sxs-lookup"><span data-stu-id="a299f-129">The **Quantity** field in tier one has a value of 999.00 and a value of 999,999,999.00 in tier two.</span></span> <span data-ttu-id="a299f-130">Jika pekerja melebihi jumlah kuantiti batu atau kilometer dalam satu peringkat, sistem menggunakan kadar Perbatuan yang ditakrifkan dalam pengurusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="a299f-130">If an employee exceeds the total quantity of miles or kilometers in tier one, the system uses the rate of mileage that is defined in Expense management.</span></span> 
  
<span data-ttu-id="a299f-131">Jika pekerja menyerahkan laporan perbelanjaan dengan 1,500 batu, dua baris perbatuan pada laporan perbelanjaan yang disiarkan akan menjadi: 1000 (kadar 0.45) + 500 (kadar 0.25) = 575</span><span class="sxs-lookup"><span data-stu-id="a299f-131">If an employee submits an expense report with 1,500 miles, the two mileage lines on the posted expense report would be: 1000 (rate 0.45) +  500 (rate 0.25) = 575</span></span>

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a><span data-ttu-id="a299f-132">Dayakan pengiraan jumlah Perbatuan untuk berbilang peringkat perbatuan dengan ciri kadar yang sama</span><span class="sxs-lookup"><span data-stu-id="a299f-132">Enable the Mileage amount calculation for multiple mileage tiers with same rate feature</span></span>

<span data-ttu-id="a299f-133">Ciri **Pengiraan jumlah Perbatuan untuk berbilang peringkat perbatuan dengan kadar yang sama** menambah baik pengiraan kadar perbatuan.</span><span class="sxs-lookup"><span data-stu-id="a299f-133">The **Mileage amount calculation for multiple mileage tiers with same rate** feature improves mileage rate calculation.</span></span> <span data-ttu-id="a299f-134">Lengkapkan langkah berikut untuk mendayakan ciri ini.</span><span class="sxs-lookup"><span data-stu-id="a299f-134">Complete the following steps to enable this feature.</span></span>

1. <span data-ttu-id="a299f-135">Pergi ke **Tetapan** > **Pengurusan Ciri**.</span><span class="sxs-lookup"><span data-stu-id="a299f-135">Go to **Workspaces** > **Feature Management**.</span></span> 
2. <span data-ttu-id="a299f-136">Dalam senarai, cari dan pilih **Pengiraan jumlah perbatuan untuk berbilang peringkat perbatuan dengan kadar yang sama** dan kemudian pilih **dayakan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="a299f-136">In the list, locate and select **Mileage amount calculation for multiple mileage tiers with same rate**, and then select **Enable now**.</span></span>

<span data-ttu-id="a299f-137">Selepas anda mendayakan ciri tersebut, tetapkan semula peringkat perbatuan untuk menunjukkan nilai medan kuantiti medan **Kuantiti**.</span><span class="sxs-lookup"><span data-stu-id="a299f-137">After you enable the feature, reset the mileage tiers to correctly reflect the value of the **Quantity** field.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]