---
title: Gambaran keseluruhan penggunaan sumber
description: Topik ini memberikan maklumat tentang penggunaan sumber dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279329"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="8ede1-103">Gambaran keseluruhan penggunaan sumber</span><span class="sxs-lookup"><span data-stu-id="8ede1-103">Resource utilization overview</span></span>

<span data-ttu-id="8ede1-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="8ede1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8ede1-105">Sumber boleh mempunyai sasaran penggunaan boleh dibilkan.</span><span class="sxs-lookup"><span data-stu-id="8ede1-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="8ede1-106">Penggunaan sasaran ini ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu.</span><span class="sxs-lookup"><span data-stu-id="8ede1-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="8ede1-107">Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.</span><span class="sxs-lookup"><span data-stu-id="8ede1-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="8ede1-108">Formula berikut digunakan untuk mengira penggunaan:</span><span class="sxs-lookup"><span data-stu-id="8ede1-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="8ede1-109">Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="8ede1-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="8ede1-110">Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="8ede1-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="8ede1-111">Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="8ede1-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="8ede1-112">Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="8ede1-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="8ede1-113">Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="8ede1-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="8ede1-114">Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan.</span><span class="sxs-lookup"><span data-stu-id="8ede1-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="8ede1-115">Formula berikut digunakan untuk mewarnakan sel:</span><span class="sxs-lookup"><span data-stu-id="8ede1-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="8ede1-116">**Hijau**: Penggunaan boleh dibilkan >= Penggunaan sasaran sumber</span><span class="sxs-lookup"><span data-stu-id="8ede1-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="8ede1-117">**Kuning**: Penggunaan sasaran – 20 <= Penggunaan boleh dibilkan < Penggunaan sasaran</span><span class="sxs-lookup"><span data-stu-id="8ede1-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="8ede1-118">**Merah**: Penggunaan boleh dibilkan < Penggunaan sasaran – 20</span><span class="sxs-lookup"><span data-stu-id="8ede1-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="8ede1-119">Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.</span><span class="sxs-lookup"><span data-stu-id="8ede1-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="8ede1-120">Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu.</span><span class="sxs-lookup"><span data-stu-id="8ede1-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="8ede1-121">Untuk melakukan persediaan ini, pergi ke **Sumber** > **Peranan sumber**.</span><span class="sxs-lookup"><span data-stu-id="8ede1-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="8ede1-122">Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="8ede1-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="8ede1-123">Pergi ke **Sumber** > **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="8ede1-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="8ede1-124">Pada tab **Perkhidmatan Projek**, sahkan peranan sumber yang ditakrifkan dan medan **Ialah Lalai** ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="8ede1-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="8ede1-125">Anda boleh menambah peranan tambahan iaitu **Ialah Lalai** = **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="8ede1-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="8ede1-126">Peranan iaitu **Ialah Lalai** = **Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.</span><span class="sxs-lookup"><span data-stu-id="8ede1-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="8ede1-127">Pada tab **Project Service**, anda juga boleh menetapkan penggunaan sasaran individu untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="8ede1-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="8ede1-128">Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.</span><span class="sxs-lookup"><span data-stu-id="8ede1-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="8ede1-129">Penggunaan ditunjukkan untuk sumber sahaja jika sumber tersebut telah diluluskan dan masa boleh dituntut dalam tempoh yang ditunjukkan dalam grid.</span><span class="sxs-lookup"><span data-stu-id="8ede1-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]