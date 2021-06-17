---
title: Harian
description: Topik ini memberikan maklumat tentang peraturan harian yang digunakan dalam pengurusan Perbelanjaan.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995272"
---
# <a name="per-diems"></a><span data-ttu-id="b83cd-103">Harian</span><span class="sxs-lookup"><span data-stu-id="b83cd-103">Per diems</span></span>

<span data-ttu-id="b83cd-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b83cd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="b83cd-105">Harian ialah elaun yang dibayar kepada pekerja yang membuat perjalanan untuk kerja.</span><span class="sxs-lookup"><span data-stu-id="b83cd-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="b83cd-106">Dalam pengurusan Perbelanjaan, anda boleh mencipta peraturan harian untuk pelbagai situasi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="b83cd-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="b83cd-107">Kadar harian boleh berdasarkan masa dalam tahun, lokasi perjalanan atau kedua-duanya.</span><span class="sxs-lookup"><span data-stu-id="b83cd-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b83cd-108">Apabila anda mencipta peraturan harian, anda boleh menentukan bahawa peratusan kadar harian akan ditahan jika pekerja menerima hidangan atau perkhidmatan percuma.</span><span class="sxs-lookup"><span data-stu-id="b83cd-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b83cd-109">Anda juga boleh menetapkan bilangan jam minimum dan maksimum yang kadar harian boleh gunakan kepada perjalanan pekerja.</span><span class="sxs-lookup"><span data-stu-id="b83cd-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="b83cd-110">Konfigurasi</span><span class="sxs-lookup"><span data-stu-id="b83cd-110">Configuration</span></span> 

1. <span data-ttu-id="b83cd-111">Untuk menambahkan lokasi harian, pergi ke **Sediakan** > **Pengiraan dan kod** > **Lokasi harian**.</span><span class="sxs-lookup"><span data-stu-id="b83cd-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="b83cd-112">Untuk setiap lokasi yang ditambahkan di atas, pilih kadar harian dan mata wang yang sah antara tarikh mula dan tamat tertentu untuk hotel, hidangan dan perbelanjaan lain.</span><span class="sxs-lookup"><span data-stu-id="b83cd-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="b83cd-113">Kadar harian dan mata wang dikonfigurasikan di bawah **Sediakan** > **Pengiraan dan kod** > **Harian**.</span><span class="sxs-lookup"><span data-stu-id="b83cd-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="b83cd-114">Pada halaman **Lokasi harian**, konfigurasikan tahap kadar harian.</span><span class="sxs-lookup"><span data-stu-id="b83cd-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="b83cd-115">Tahap kadar harian membolehkan anda mentakrifkan pecahan peratusan elaun harian untuk hotel, hidangan dan perbelanjaan lain.</span><span class="sxs-lookup"><span data-stu-id="b83cd-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="b83cd-116">Untuk menentukan pengurangan peratusan hidangan untuk sarapan, makan tengah hari atau makan malam, kemas kini medan pada halaman **Parameter pengurusan perbelanjaan** pada tab **Harian**.</span><span class="sxs-lookup"><span data-stu-id="b83cd-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="b83cd-117">Serahkan perbelanjaan menggunakan harian</span><span class="sxs-lookup"><span data-stu-id="b83cd-117">Submit expenses using per diem</span></span>
<span data-ttu-id="b83cd-118">Untuk menyerahkan perbelanjaan menggunakan harian, gunakan kategori perbelanjaan **Harian** apabila anda mencipta laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="b83cd-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="b83cd-119">Masukkan **Harian daripada tarikh**, **Harian daripada tarikh** dan **Lokasi harian**.</span><span class="sxs-lookup"><span data-stu-id="b83cd-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="b83cd-120">Amaun akan dikira berdasarkan kadar harian untuk lokasi yang dipilih dan pengurangan hidangan akan dikira berdasarkan tahap kadar harian.</span><span class="sxs-lookup"><span data-stu-id="b83cd-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]