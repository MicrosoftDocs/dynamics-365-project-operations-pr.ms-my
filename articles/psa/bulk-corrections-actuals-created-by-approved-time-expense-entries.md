---
title: Pembetulan pukal aktual yang dicipta oleh entri masa dan perbelanjaan yang diluluskan
description: Topik ini menerangkan cara pentadbir boleh membuat pembetulan tunggal atau pukal kepada entri masa atau perbelanjaan yang telah diluluskan jika pengebilan tidak lengkap.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144964"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="f583f-103">Pembetulan pukal aktual yang dicipta oleh entri masa dan perbelanjaan yang diluluskan</span><span class="sxs-lookup"><span data-stu-id="f583f-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f583f-104">Kadangkala entri masa atau perbelanjaan boleh dimasukkan dengan salah.</span><span class="sxs-lookup"><span data-stu-id="f583f-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="f583f-105">Sebagai contoh, seorang perunding mungkin memilih tarikh yang salah apabila mencipta entri masa atau mereka mungkin mengubah nombor apabila memasukkan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="f583f-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="f583f-106">Jika perunding tidak boleh membuat kemas kini kepada entri yang diserahkan, pentadbir boleh secara langsung membetulkan entri untuk projek.</span><span class="sxs-lookup"><span data-stu-id="f583f-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="f583f-107">Untuk melengkapkan prosedur dalam topik ini, anda akan memerlukan keizinan Pentadbir.</span><span class="sxs-lookup"><span data-stu-id="f583f-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="f583f-108">Entri masa yang diluluskan yang betul</span><span class="sxs-lookup"><span data-stu-id="f583f-108">Correct approved time entries</span></span>     

<span data-ttu-id="f583f-109">Lengkapkan langkah berikut untuk membetulkan entri masa tunggal atau berbilang bagi projek.</span><span class="sxs-lookup"><span data-stu-id="f583f-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="f583f-110">Dalam kawasan **Jualan**, pilih **Urus niaga** dan kemudian pilih **Masa yang Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="f583f-111">Dalam senarai **Masa yang Diluluskan**, cari dan pilih satu atau lebih entri masa yang diluluskan untuk dibetulkan.</span><span class="sxs-lookup"><span data-stu-id="f583f-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="f583f-112">Anda boleh menggunakan penapis untuk mengesan entri yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="f583f-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="f583f-113">Contohnya, anda boleh menapis ID Projek dan memilih semua entri masa yang diluluskan dengan ID Projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="f583f-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="f583f-114">Pilih **Entri yang betul**.</span><span class="sxs-lookup"><span data-stu-id="f583f-114">Select **Correct entries**.</span></span> <span data-ttu-id="f583f-115">Jurnal pembetulan baharu dicipta secara automatik, dengan jenis ditugaskan **Pembetulan masa**.</span><span class="sxs-lookup"><span data-stu-id="f583f-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="f583f-116">Entri yang anda pilih ditambah kepada jurnal tersebut.</span><span class="sxs-lookup"><span data-stu-id="f583f-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="f583f-117">Pada halaman **Jurnal Baharu**, masukkan **Perihalan** untuk jurnal pembetulan anda dan kemudian pilih tab **Pembetulan Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="f583f-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="f583f-118">Dalam bahagian **Nilai Baharu untuk Entri Masa**, kemas kini medan dengan maklumat yang betul mengikut keperluan.</span><span class="sxs-lookup"><span data-stu-id="f583f-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="f583f-119">Contohnya, anda boleh mengubah projek yang ditugaskan atau sumber boleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="f583f-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="f583f-120">Pilih **Pratonton**.</span><span class="sxs-lookup"><span data-stu-id="f583f-120">Select **Preview**.</span></span> <span data-ttu-id="f583f-121">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="f583f-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="f583f-122">Pada tab **Garisan jurnal**, anda boleh melihat senarai aktual asal yang berkaitan dengan entri masa terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.</span><span class="sxs-lookup"><span data-stu-id="f583f-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="f583f-123">Jika pembetulan tambahan perlu dibuat, ulangi langkah 5 dan 6.</span><span class="sxs-lookup"><span data-stu-id="f583f-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="f583f-124">Semua aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="f583f-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="f583f-125">Jika pembetulan muncul seperti yang dijangka, pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="f583f-126">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="f583f-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="f583f-127">Kembali ke kawasan **Jualan**, pilih **Projek**, dan kemudian buka projek yang anda baru sahaja kemas kini entri masanya.</span><span class="sxs-lookup"><span data-stu-id="f583f-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="f583f-128">Pada halaman **Projek**, pada tab **Aktual**, lihat perubahan yang anda lakukan.</span><span class="sxs-lookup"><span data-stu-id="f583f-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="f583f-129">Jika tab **Aktual** tidak kelihatan, pilih **Berkaitan** > **Aktual**.</span><span class="sxs-lookup"><span data-stu-id="f583f-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="f583f-130">Dalam senarai **Pandangan Berkaitan Aktual**, anda boleh melihat bahawa entri masa asal yang telah diterbalikkan masih disenaraikan, seperti entri masa dibetulkan yang sepadan.</span><span class="sxs-lookup"><span data-stu-id="f583f-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="f583f-131">Sebagai contoh, dalam grafik berikut, terdapat dua baris item dengan kuantiti 8.00 yang mempunyai debit disenaraikan dalam lajur Amaun.</span><span class="sxs-lookup"><span data-stu-id="f583f-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="f583f-132">Selain itu, terdapat dua baris item dengan kuantiti -8.00 yang menunjukkan amaun yang dikreditkan dalam lajur Amaun.</span><span class="sxs-lookup"><span data-stu-id="f583f-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="f583f-133">Pembetulan ini membawa kuantiti kepada sifar.</span><span class="sxs-lookup"><span data-stu-id="f583f-133">These corrections bring the quantity to zero.</span></span>

![Senarai pandangan berkaitan aktual](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="f583f-135">Entri perbelanjaan yang diluluskan yang betul</span><span class="sxs-lookup"><span data-stu-id="f583f-135">Correct approved expense entries</span></span>

<span data-ttu-id="f583f-136">Lengkapkan langkah berikut untuk membetulkan satu atau lebih entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="f583f-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="f583f-137">Dalam kawasan **Jualan**, dalam anak tetingkap navigasi kiri, di bawah **Urus niaga**, pilih **Perbelanjaan Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="f583f-138">Dalam senarai **Perbelanjaan Diluluskan**, pilih projek yang anda mahu betulkan dan kemudian pilih **Entri yang betul**.</span><span class="sxs-lookup"><span data-stu-id="f583f-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="f583f-139">Jurnal pembetulan akan dicipta secara automatik dengan jenis ditugaskan **Pembetulan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="f583f-140">Pada halaman **Jurnal Baharu**, masukkan **Perihalan** untuk pembetulan dan pada tab **Pembetulan Perbelanjaan**, dalam bahagian **Nilai Baharu untuk Perbelanjaan**, pilih medan data yang anda mahu betulkan untuk baris perbelanjaan yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="f583f-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="f583f-141">Contohnya, anda boleh menugaskan perbelanjaan ke **Projek** lain atau membetulkan **Kategori Perbelanjaan**, **Tarikh Perbelanjaan** atau **Sumber Boleh Ditempah**.</span><span class="sxs-lookup"><span data-stu-id="f583f-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="f583f-142">Pilih **Pratonton**.</span><span class="sxs-lookup"><span data-stu-id="f583f-142">Select **Preview**.</span></span> <span data-ttu-id="f583f-143">Dalam kotak dialog, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="f583f-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="f583f-144">Sahkan pembetulan pada tab **Garisan jurnal**. Anda boleh melihat senarai aktual asal yang berkaitan dengan entri perbelanjaan terpilih yang telah diterbalikkan dan baris sepadan yang dibetulkan yang telah dicipta.</span><span class="sxs-lookup"><span data-stu-id="f583f-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="f583f-145">Jika nilai yang dibetulkan adalah seperti yang dijangka, pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="f583f-146">Dalam kotak dialog, pilih **OK.**</span><span class="sxs-lookup"><span data-stu-id="f583f-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="f583f-147">Jika nilai tidak ditunjukkan seperti yang dijangkakan, pilih **Batalkan** untuk kembali ke senarai **Perbelanjaan yang Diluluskan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="f583f-148">Ulangi langkah 2 hingga 5.</span><span class="sxs-lookup"><span data-stu-id="f583f-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="f583f-149">Aktual yang dibetulkan akan mempunyai nilai yang sama yang anda pilih dalam bahagian **Nilai Baharu untuk Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="f583f-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="f583f-150">Selepas anda mengesahkan jurnal pembetulan, navigasi kembali ke projek atau projek yang anda kemas kini, untuk melihat perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="f583f-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="f583f-151">Dalam halaman projek, pada tab **Aktual**, semak **Pandangan Berkaitan Aktual**.</span><span class="sxs-lookup"><span data-stu-id="f583f-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="f583f-152">Entri asal dan entri yang diperbetulkan disenaraikan.</span><span class="sxs-lookup"><span data-stu-id="f583f-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="f583f-153">Grafik berikut menunjukkan jumlah entri perbelanjaan asal dan jumlah entri perbelanjaan dibetulkan yang sepadan.</span><span class="sxs-lookup"><span data-stu-id="f583f-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Aktual perbelanjaan](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
