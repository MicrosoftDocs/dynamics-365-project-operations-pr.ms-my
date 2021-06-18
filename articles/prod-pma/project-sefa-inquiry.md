---
title: Jadual Perbelanjaan pertanyaan Anugerah Persekutuan
description: Topik ini menyediakan maklumat mengenai Jadual Perbelanjaan pertanyaan Anugerah Persekutuan.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010077"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="80f0f-103">Jadual Perbelanjaan pertanyaan Anugerah Persekutuan</span><span class="sxs-lookup"><span data-stu-id="80f0f-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80f0f-104">Menurut pejabat Pengurusan dan Pekeliling Belanjawan A-133, agensi yang menerima dana persekutuan adalah tertakluk kepada keperluan audit, yang juga dikenali sebagai audit tunggal.</span><span class="sxs-lookup"><span data-stu-id="80f0f-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="80f0f-105">Proses audit digunakan untuk melaporkan hasil dan perbelanjaan pemberian persekutuan pada asas yang berulang.</span><span class="sxs-lookup"><span data-stu-id="80f0f-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="80f0f-106">Sebahagian daripada laporan audit tunggal termasuk Jadual Perbelanjaan Anugerah Persekutuan (SEFA).</span><span class="sxs-lookup"><span data-stu-id="80f0f-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="80f0f-107">Jadual Perbelanjaan pertanyaan Anugerah Persekutuan termasuk tajuk dan nombor Katalog Bantuan Domestik Persekutuan (CFDA), nombor pemberian, tahun pemberian, nama agensi persekutuan yang menyediakan dana dan nama entiti serah semua.</span><span class="sxs-lookup"><span data-stu-id="80f0f-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="80f0f-108">Pertanyaan adalah untuk tempoh tertentu.</span><span class="sxs-lookup"><span data-stu-id="80f0f-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="80f0f-109">Lazimnya, tempoh tersebut adalah sama dengan tempoh penyata kewangan yang merupakan tahun fiskal.</span><span class="sxs-lookup"><span data-stu-id="80f0f-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="80f0f-110">Pertanyaan termasuk pemberian yang mempunyai tarikh unjuran dalam julat tarikh yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="80f0f-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="80f0f-111">Lajur **Agensi penerima** bagi pertanyaan menunjukkan pelanggan pemberian atau, untuk pemberian serah semua, agensi penerima.</span><span class="sxs-lookup"><span data-stu-id="80f0f-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="80f0f-112">Untuk pemberian serah semua, lajur **Agensi serah semua** menunjukkan pelanggan pemberian.</span><span class="sxs-lookup"><span data-stu-id="80f0f-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="80f0f-113">Jika pemberian bukan pemberian serah semua, lajur **Agensi serah semua** adalah kosong.</span><span class="sxs-lookup"><span data-stu-id="80f0f-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="80f0f-114">Sediakan kelompok CFDA</span><span class="sxs-lookup"><span data-stu-id="80f0f-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="80f0f-115">Anda mesti sediakan kelompok CFDA yang boleh dikaitkan dengan nombor CFDA dalam Jadual Perbelanjaan pertanyaan Anugerah Persekutuan.</span><span class="sxs-lookup"><span data-stu-id="80f0f-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="80f0f-116">Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Pemberian \> Katalog kelompok Bantuan Domestik Persekutuan**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="80f0f-117">Pilih **Baharu** untuk mencipta kelompok CFDA.</span><span class="sxs-lookup"><span data-stu-id="80f0f-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="80f0f-118">Masukkan nama kelompok.</span><span class="sxs-lookup"><span data-stu-id="80f0f-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="80f0f-119">Pilih **Simpan** untuk menyimpan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="80f0f-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="80f0f-120">Sediakan nombor CFDA</span><span class="sxs-lookup"><span data-stu-id="80f0f-120">Set up CFDA numbers</span></span>

<span data-ttu-id="80f0f-121">Anda mesti sediakan nombor CFDA yang boleh ditambah untuk memberikan dan termasuk dalam pertanyaan Jadual Perbelanjaan Anugerah Persekutuan.</span><span class="sxs-lookup"><span data-stu-id="80f0f-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="80f0f-122">Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Geran \> Katalog nombor Bantuan Domestik Persekutuan**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="80f0f-123">Pilih **Baharu** untuk mencipta nombor CFDA.</span><span class="sxs-lookup"><span data-stu-id="80f0f-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="80f0f-124">Dalam lajur **Nombor**, masukkan nombor CFDA.</span><span class="sxs-lookup"><span data-stu-id="80f0f-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="80f0f-125">Tekan kekunci **Tab**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="80f0f-126">Dalam lajur **Description**, masukkan tajuk CFDA.</span><span class="sxs-lookup"><span data-stu-id="80f0f-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="80f0f-127">Tekan kekunci **Tab**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="80f0f-128">Pilihan: Dalam medan **Kelompok program**, tambah kelompok CFDA yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="80f0f-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="80f0f-129">Pilih **Simpan** untuk menyimpan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="80f0f-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="80f0f-130">Menyediakan geran untuk melapor untuk Jadual Perbelanjaan pertanyaan Anugerah Persekutuan</span><span class="sxs-lookup"><span data-stu-id="80f0f-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="80f0f-131">Pergi ke **Pengurusan dan perakaunan projek \> Geran \> Geran**, dan pilih geran sedia ada.</span><span class="sxs-lookup"><span data-stu-id="80f0f-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="80f0f-132">Pada FastTab **Persediaan**, dalam medan **Katalog Bantuan Domestik Persekutuan**, tugaskan nombor CFDA.</span><span class="sxs-lookup"><span data-stu-id="80f0f-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="80f0f-133">Nombor CFDA pada geran menentukan kelompok CFDA untuk pelaporan.</span><span class="sxs-lookup"><span data-stu-id="80f0f-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="80f0f-134">Pada FastTab **Maklumat kenalan**, masukkan maklumat pemberi dengan mengikut langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="80f0f-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="80f0f-135">Dalam medan **Berikan pelanggan**, masukkan pelanggan yang bertanggungjawab untuk geran tersebut.</span><span class="sxs-lookup"><span data-stu-id="80f0f-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="80f0f-136">Untuk geran sedia ada, maklumat ini mungkin telah dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="80f0f-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="80f0f-137">Menunjukkan sama ada pemberian pelanggan adalah pemberi dana.</span><span class="sxs-lookup"><span data-stu-id="80f0f-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="80f0f-138">Jika pemberian pelanggan adalah pemberi dana, biarkan kotak semak **Serah semua** kosong.</span><span class="sxs-lookup"><span data-stu-id="80f0f-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="80f0f-139">Jika pelanggan lain adalah pemberi dana, dan pelanggan pemberian bertanggungjawab untuk berbelanja dan menjejaki wang, pilih kotak semak **Serah semua**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="80f0f-140">Jika anda memilih kotak semak **Serah semua** dalam langkah sebelumnya, dalam medan **Agensi pemberi**, masukkan pelanggan yang menyediakan pemberian tersebut.</span><span class="sxs-lookup"><span data-stu-id="80f0f-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="80f0f-141">Agensi penerima dan pelanggan pemberian tidak boleh menjadi pelanggan yang sama.</span><span class="sxs-lookup"><span data-stu-id="80f0f-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="80f0f-142">Berikut ialah contoh pemberian serah semua:</span><span class="sxs-lookup"><span data-stu-id="80f0f-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="80f0f-143">Kerajaan persekutuan telah membiayai projek infrastruktur untuk keadaan.</span><span class="sxs-lookup"><span data-stu-id="80f0f-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="80f0f-144">Kerajaan persekutuan memberikan wang kepada keadaan untuk berbelanja.</span><span class="sxs-lookup"><span data-stu-id="80f0f-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="80f0f-145">Dalam hal ini, kerajaan persekutuan ialah agensi penerima, dan keadaan ini ialah pelanggan pemberian.</span><span class="sxs-lookup"><span data-stu-id="80f0f-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="80f0f-146">Apabila anda terlebih dahulu menghidupkan ciri, nombor CFDA awal akan dimasukkan dengan menggunakan nombor sedia ada pada pemberian.</span><span class="sxs-lookup"><span data-stu-id="80f0f-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="80f0f-147">Kecualikan pemberian daripada pelaporan SEFA berdasarkan jenis pemberian</span><span class="sxs-lookup"><span data-stu-id="80f0f-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="80f0f-148">Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Pemberian \> Jenis pemberian**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="80f0f-149">Pada FastTab **Maklumat lalai**, pilih kotak semak **Kecualikan daripada Jadual Perbelanjaan Anugerah Persekutuan**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="80f0f-150">Pilih **Simpan** untuk menyimpan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="80f0f-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="80f0f-151">Jalankan Jadual Perbelanjaan pertanyaan Anugerah Persekutuan</span><span class="sxs-lookup"><span data-stu-id="80f0f-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="80f0f-152">Pergi ke **Pengurusan dan perakaunan projek \> Pertanyaan dan laporan \> Pertanyaan pemberian \> Jadual Perbelanjaan Anugerah Persekutuan**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="80f0f-153">Dalam bahagian **Parameter**, ikuti langkah ini:</span><span class="sxs-lookup"><span data-stu-id="80f0f-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="80f0f-154">Dalam medan **Selang tarikh**, pilih kod untuk selang tarikh.</span><span class="sxs-lookup"><span data-stu-id="80f0f-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="80f0f-155">Sebagai alternatif, pada medan **Daripada tarikh** dan **Hingga Tarikh**, takrifkan selang tarikh.</span><span class="sxs-lookup"><span data-stu-id="80f0f-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="80f0f-156">Pilihan: Untuk memasukkan hanya transaksi yang dibilkan sebagai pendapatan dalam pertanyaan, tetapkan pilihan **Termasuk hasil dibilkan sahaja** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="80f0f-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="80f0f-157">Lajur</span><span class="sxs-lookup"><span data-stu-id="80f0f-157">Columns</span></span>

<span data-ttu-id="80f0f-158">Jadual Perbelanjaan pertanyaan Anugerah Persekutuan termasuk lajur berikut:</span><span class="sxs-lookup"><span data-stu-id="80f0f-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="80f0f-159">Katalog nama kelompok Bantuan Domestik Persekutuan</span><span class="sxs-lookup"><span data-stu-id="80f0f-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="80f0f-160">Agensi pemberi</span><span class="sxs-lookup"><span data-stu-id="80f0f-160">Grantor agency</span></span>
- <span data-ttu-id="80f0f-161">Agensi serah semua</span><span class="sxs-lookup"><span data-stu-id="80f0f-161">Pass-through agency</span></span>
- <span data-ttu-id="80f0f-162">Nama pemberian</span><span class="sxs-lookup"><span data-stu-id="80f0f-162">Grant name</span></span>
- <span data-ttu-id="80f0f-163">ID pemberian</span><span class="sxs-lookup"><span data-stu-id="80f0f-163">Grant ID</span></span>
- <span data-ttu-id="80f0f-164">ID aplikasi pemberian</span><span class="sxs-lookup"><span data-stu-id="80f0f-164">Grant application ID</span></span>
- <span data-ttu-id="80f0f-165">Katalog Bantuan Domestik Persekutuan</span><span class="sxs-lookup"><span data-stu-id="80f0f-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="80f0f-166">Resit</span><span class="sxs-lookup"><span data-stu-id="80f0f-166">Receipts</span></span>
- <span data-ttu-id="80f0f-167">Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="80f0f-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]