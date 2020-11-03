---
title: Cipta dan sahkan jurnal Pembetulan
description: Topik ini menyediakan maklumat tentang cara mencipta dan mengesahkan jurnal pembetulan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081225"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="44297-103">Cipta dan sahkan jurnal Pembetulan</span><span class="sxs-lookup"><span data-stu-id="44297-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="44297-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="44297-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44297-105">Kadangkala entri masa atau perbelanjaan boleh dimasukkan dengan salah.</span><span class="sxs-lookup"><span data-stu-id="44297-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="44297-106">Sebagai contoh, seorang perunding mungkin memilih tarikh yang salah apabila mencipta entri masa atau mereka mungkin mengubah nombor apabila memasukkan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="44297-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="44297-107">Jika perunding tidak boleh membuat kemas kini kepada entri yang diserahkan, pentadbir boleh secara langsung membetulkan entri untuk projek.</span><span class="sxs-lookup"><span data-stu-id="44297-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="44297-108">Untuk melengkapkan prosedur dalam topik ini, anda akan memerlukan keizinan Pentadbir.</span><span class="sxs-lookup"><span data-stu-id="44297-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="44297-109">Entri masa yang diluluskan yang betul</span><span class="sxs-lookup"><span data-stu-id="44297-109">Correct approved time entries</span></span>     

<span data-ttu-id="44297-110">Lengkapkan langkah berikut untuk membetulkan entri masa tunggal atau berbilang bagi projek.</span><span class="sxs-lookup"><span data-stu-id="44297-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="44297-111">Dalam kawasan **Jualan** , pilih **Urus niaga** dan kemudian pilih **Masa yang Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="44297-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="44297-112">Dalam senarai **Masa yang Diluluskan** , cari dan pilih satu atau lebih entri masa yang diluluskan untuk dibetulkan.</span><span class="sxs-lookup"><span data-stu-id="44297-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="44297-113">Anda boleh menggunakan penapis untuk mengesan entri yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="44297-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="44297-114">Contohnya, anda boleh menapis ID Projek dan memilih semua entri masa yang diluluskan dengan ID Projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="44297-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="44297-115">Pilih **Entri yang betul**.</span><span class="sxs-lookup"><span data-stu-id="44297-115">Select **Correct entries**.</span></span> <span data-ttu-id="44297-116">Jurnal pembetulan baharu dicipta secara automatik, dengan jenis ditugaskan **Pembetulan masa**.</span><span class="sxs-lookup"><span data-stu-id="44297-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="44297-117">Entri yang anda pilih ditambah kepada jurnal tersebut.</span><span class="sxs-lookup"><span data-stu-id="44297-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="44297-118">Pada halaman **Jurnal Baharu** , masukkan **Perihalan** untuk jurnal pembetulan anda dan kemudian pilih tab **Pembetulan Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="44297-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="44297-119">Dalam bahagian **Nilai Baharu untuk Entri Masa** , kemas kini medan dengan maklumat yang betul mengikut keperluan.</span><span class="sxs-lookup"><span data-stu-id="44297-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="44297-120">Contohnya, anda boleh mengubah projek yang ditugaskan atau sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="44297-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="44297-121">Pilih **Pratonton**.</span><span class="sxs-lookup"><span data-stu-id="44297-121">Select **Preview**.</span></span> <span data-ttu-id="44297-122">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="44297-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="44297-123">Pada tab **Garisan jurnal** , anda boleh melihat senarai aktual asal yang berkaitan dengan entri masa terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.</span><span class="sxs-lookup"><span data-stu-id="44297-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="44297-124">Jika pembetulan tambahan perlu dibuat, ulangi langkah 5 dan 6.</span><span class="sxs-lookup"><span data-stu-id="44297-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="44297-125">Semua aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="44297-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="44297-126">Jika pembetulan muncul seperti yang dijangka, pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="44297-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="44297-127">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="44297-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="44297-128">Kembali ke kawasan **Jualan** , pilih **Projek** , dan kemudian buka projek yang anda baru sahaja kemas kini entri masanya.</span><span class="sxs-lookup"><span data-stu-id="44297-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="44297-129">Pada halaman **Projek** , pada tab **Aktual** , lihat perubahan yang anda lakukan.</span><span class="sxs-lookup"><span data-stu-id="44297-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="44297-130">Jika tab **Aktual** tidak kelihatan, pilih **Berkaitan** > **Aktual**.</span><span class="sxs-lookup"><span data-stu-id="44297-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="44297-131">Dalam senarai **Pandangan Berkaitan Aktual** , anda boleh melihat bahawa entri masa asal yang telah diterbalikkan masih disenaraikan, seperti entri masa dibetulkan yang sepadan.</span><span class="sxs-lookup"><span data-stu-id="44297-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="44297-132">Sebagai contoh, dalam grafik berikut, terdapat dua baris item dengan kuantiti 8.00 yang mempunyai debit disenaraikan dalam lajur Amaun.</span><span class="sxs-lookup"><span data-stu-id="44297-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="44297-133">Selain itu, terdapat dua baris item dengan kuantiti -8.00 yang menunjukkan amaun yang dikreditkan dalam lajur Amaun.</span><span class="sxs-lookup"><span data-stu-id="44297-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="44297-134">Pembetulan ini membawa kuantiti kepada sifar.</span><span class="sxs-lookup"><span data-stu-id="44297-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="44297-135">Entri perbelanjaan yang diluluskan yang betul</span><span class="sxs-lookup"><span data-stu-id="44297-135">Correct approved expense entries</span></span>

<span data-ttu-id="44297-136">Lengkapkan langkah berikut untuk membetulkan satu atau lebih entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="44297-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="44297-137">Dalam kawasan **Jualan** , dalam anak tetingkap navigasi kiri, di bawah **Urus niaga** , pilih **Perbelanjaan Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="44297-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="44297-138">Dalam senarai **Perbelanjaan Diluluskan** , pilih projek yang anda mahu betulkan dan kemudian pilih **Entri yang betul**.</span><span class="sxs-lookup"><span data-stu-id="44297-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="44297-139">Jurnal pembetulan akan dicipta secara automatik dengan jenis ditugaskan **Pembetulan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="44297-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="44297-140">Pada halaman **Jurnal Baharu** , masukkan **Perihalan** untuk pembetulan dan pada tab **Pembetulan Perbelanjaan** , dalam bahagian **Nilai Baharu untuk Perbelanjaan** , pilih medan data yang anda mahu betulkan untuk baris perbelanjaan yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="44297-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="44297-141">Contohnya, anda boleh menugaskan perbelanjaan ke **Projek** lain atau membetulkan **Kategori Perbelanjaan** , **Tarikh Perbelanjaan** atau **Sumber Boleh Ditempah**.</span><span class="sxs-lookup"><span data-stu-id="44297-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="44297-142">Pilih **Pratonton**.</span><span class="sxs-lookup"><span data-stu-id="44297-142">Select **Preview**.</span></span> <span data-ttu-id="44297-143">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="44297-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="44297-144">Sahkan pembetulan pada tab **Garisan jurnal**. Anda boleh melihat senarai aktual asal yang berkaitan dengan entri perbelanjaan terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.</span><span class="sxs-lookup"><span data-stu-id="44297-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="44297-145">Jika nilai yang dibetulkan adalah seperti yang dijangka, pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="44297-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="44297-146">Dalam kotak dialog, pilih **OK.**</span><span class="sxs-lookup"><span data-stu-id="44297-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="44297-147">Jika nilai tidak ditunjukkan seperti yang dijangkakan, pilih **Batalkan** untuk kembali ke senarai **Perbelanjaan yang Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="44297-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="44297-148">Ulangi langkah 2 hingga 5.</span><span class="sxs-lookup"><span data-stu-id="44297-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="44297-149">Aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="44297-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="44297-150">Selepas anda mengesahkan jurnal pembetulan, navigasi kembali ke projek atau projek yang anda kemas kini, untuk melihat perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="44297-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="44297-151">Dalam halaman projek, pada tab **Aktual** , semak **Pandangan Berkaitan Aktual**.</span><span class="sxs-lookup"><span data-stu-id="44297-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="44297-152">Entri asal dan entri yang diperbetulkan disenaraikan.</span><span class="sxs-lookup"><span data-stu-id="44297-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="44297-153">Grafik berikut menunjukkan jumlah entri perbelanjaan asal dan jumlah entri perbelanjaan dibetulkan yang sepadan.</span><span class="sxs-lookup"><span data-stu-id="44297-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


