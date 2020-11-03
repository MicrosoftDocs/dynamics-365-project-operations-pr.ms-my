---
title: Kontrak projek
description: Topik ini menyediakan contoh kontrak projek yang boleh anda cipta untuk pelbagai jenis produk dan sumber pembiayaan serta cara anda boleh mengurus kontrak dan menginvois pelanggan projek.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081359"
---
# <a name="project-contracts"></a><span data-ttu-id="8deb6-103">Kontrak projek</span><span class="sxs-lookup"><span data-stu-id="8deb6-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8deb6-104">Artikel ini menyediakan contoh kontrak projek yang boleh anda cipta untuk pelbagai jenis produk dan sumber pembiayaan serta cara anda boleh mengurus kontrak dan menginvois pelanggan projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="8deb6-105">Jenis projek yang anda cipta untuk kontrak projek menentukan kaedah yang digunakan untuk menginvois pelanggan projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="8deb6-106">Anda boleh mengubah kontrak projek dan projek yang berkaitan tetapi anda tidak boleh mengubah jenis projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="8deb6-107">Dengan menggunakan kontrak projek, anda boleh menginvois satu atau lebih projek pada masa yang sama.</span><span class="sxs-lookup"><span data-stu-id="8deb6-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="8deb6-108">Kontrak projek juga membantu menjamin prosedur penginvoisan yang konsisten untuk setiap subprojek dalam struktur projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="8deb6-109">Setiap projek yang akan diinvoiskan mesti berkaitan dengan kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="8deb6-110">Tetapan untuk kontrak projek terpakai kepada semua projek dan subprojek yang berkaitan dengan kontrak projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="8deb6-111">Kontrak projek boleh menentukan satu atau lebih sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="8deb6-112">Oleh itu, anda boleh memisahkan pengebilan antara berbilang pembiaya, menyediakan had pembiayaan supaya sumber pembiayaan tidak dibilkan lebih daripada amaun yang ditentukan dan mengkonfigurasikan peraturan pembiayaan untuk mengecaj perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="8deb6-113">Pembiayaan untuk kontrak projek</span><span class="sxs-lookup"><span data-stu-id="8deb6-113">Funding for project contracts</span></span>
<span data-ttu-id="8deb6-114">Beberapa kontrak projek menentukan bahawa berbilang pihak mempunyai tanggungjawab bersama untuk membiayai kos projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="8deb6-115">Berikut adalah beberapa contoh:</span><span class="sxs-lookup"><span data-stu-id="8deb6-115">Here are some examples:</span></span>

-   <span data-ttu-id="8deb6-116">Pelanggan besar yang mempunyai berbilang bahagian meminta agar pembiayaan projek dipisahkan mengikut bahagian.</span><span class="sxs-lookup"><span data-stu-id="8deb6-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="8deb6-117">Syarikat anda berkongsi kod projek besar dengan organisasi luar.</span><span class="sxs-lookup"><span data-stu-id="8deb6-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="8deb6-118">Projek jalan dibiayai bersama oleh dua majlis perbandaran.</span><span class="sxs-lookup"><span data-stu-id="8deb6-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="8deb6-119">Projek jambatan dibiayai oleh geran kerajaan dan syarikat swasta.</span><span class="sxs-lookup"><span data-stu-id="8deb6-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="8deb6-120">Dalam Dynamics 365 Finance, anda boleh memisahkan pengebilan untuk transaksi tunggal atau keseluruhan projek antara berbilang pelanggan, geran atau organisasi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="8deb6-121">Dalam projek yang mempunyai berbilang pembiaya, semua pihak yang menyumbang kepada pembiayaan projek pembiayaan awal dipanggil sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="8deb6-122">Selepas pelanggan, organisasi atau pelan ditakrifkan sebagai sumber pembiayaan, ia boleh diperuntukkan kepada satu atau lebih peraturan pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="8deb6-123">Peraturan pembiayaan mengandungi kriteria yang menentukan cara caj diperuntukkan kepada pelbagai sumber pembiayaan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="8deb6-124">Disebabkan item stok, seperti yang muncul pada pemerolehan pembelian dan pesanan pembelian, tidak boleh dipisahkan, amaun kos tidak boleh dipisahkan antara berbilang sumber pembiayaan pada waktu pengagihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="8deb6-125">Oleh itu, nilai sumber pembiayaan kekal 0 (sifar) sehingga isu inventori disiarkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="8deb6-126">Apabila isu inventori disiarkan, amaun kos diagihkan mengikut peraturan pengagihan akaun untuk projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="8deb6-127">Berikut beberapa langkah yang boleh anda ambil untuk menjadikannya lebih mudah untuk memisahkan pengebilan antara berbilang sumber pembiayaan:</span><span class="sxs-lookup"><span data-stu-id="8deb6-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="8deb6-128">Tentukan bahawa semua transaksi yang dimasukkan untuk projek menggunakan mata wang jualan yang sama seperti kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="8deb6-129">Sediakan had pembiayaan, supaya sumber pembiayaan tidak diinvoiskan lebih daripada amaun yang ditentukan terhadap projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="8deb6-130">Konfigurasikan peraturan pembiayaan dan had pembiayaan untuk setiap pekerja, item, kategori, kumpulan kategori dan jenis transaksi (atau untuk semua jenis transaksi).</span><span class="sxs-lookup"><span data-stu-id="8deb6-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="8deb6-131">Pilih tarikh mula dan tamat pilihan untuk mentakrifkan tempoh apabila setiap peraturan pembiayaan adalah sah.</span><span class="sxs-lookup"><span data-stu-id="8deb6-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="8deb6-132">Tentukan peratusan yang menjadi tanggungjawab setiap sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="8deb6-133">Tentukan sumber pembiayaan yang bertanggungjawab terhadap perbezaan pembundaran yang disebabkan oleh pengiraan peruntukan pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="8deb6-134">Sediakan peraturan yang menentukan cara kos projek diinvoiskan kepada pelanggan luar dan dicaj kepada organisasi luar.</span><span class="sxs-lookup"><span data-stu-id="8deb6-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="8deb6-135">Rekodkan transaksi dalam akaun pembiayaan yang ditahan sehingga pembiayaan tambahan boleh diperoleh atau sehingga anda memutuskan untuk menanggung kos secara dalaman.</span><span class="sxs-lookup"><span data-stu-id="8deb6-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="8deb6-136">Untuk menentukan kumpulan cukai yang akan dikaitkan dengan transaksi, projek dicari untuk tugasan kumpulan cukai.</span><span class="sxs-lookup"><span data-stu-id="8deb6-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="8deb6-137">Jika tiada tugasan kumpulan cukai telah dibuat pada peringkat projek, kontrak projek dicari.</span><span class="sxs-lookup"><span data-stu-id="8deb6-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="8deb6-138">Contoh: Berbilang sumber pembiayaan (ringkas)</span><span class="sxs-lookup"><span data-stu-id="8deb6-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="8deb6-139">Jadual yang berikut memberikan senario untuk menguruskan peruntukan pembiayaan antara berbilang sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="8deb6-140">Senario ini berdasarkan anggapan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="8deb6-141">Tetapan keutamaan difaktorkan ke dalam peruntukan dana sebelum kriteria peraturan pembiayaan lain dikenakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="8deb6-142">Tiada julat tarikh telah ditentukan untuk mentakrifkan tempoh d apabila peraturan pembiayaan adalah sah.</span><span class="sxs-lookup"><span data-stu-id="8deb6-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8deb6-143"><strong>Senario</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="8deb6-144"><strong>Sumber pembiayaan</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="8deb6-145"><strong>Peratusan peruntukan</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="8deb6-146"><strong>Keutamaan peruntukan</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8deb6-147">Anda mahu menguntukkan kos kepada sumber pembiayaan pertama sehingga dananya habis, menguntukkan kos kepada sumber pembiayaan kedua sehingga dananya habis dan akhir sekali menguntukkan kos yang tinggal kepada sumber pembiayaan ketiga.</span><span class="sxs-lookup"><span data-stu-id="8deb6-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-148">Sumber pembiayaan 1</span><span class="sxs-lookup"><span data-stu-id="8deb6-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="8deb6-149">Sumber pembiayaan 2</span><span class="sxs-lookup"><span data-stu-id="8deb6-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="8deb6-150">Sumber pembiayaan 3</span><span class="sxs-lookup"><span data-stu-id="8deb6-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-151">100%</span><span class="sxs-lookup"><span data-stu-id="8deb6-151">100%</span></span></li>
<li><span data-ttu-id="8deb6-152">100%</span><span class="sxs-lookup"><span data-stu-id="8deb6-152">100%</span></span></li>
<li><span data-ttu-id="8deb6-153">100%</span><span class="sxs-lookup"><span data-stu-id="8deb6-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-154">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-154">1</span></span></li>
<li><span data-ttu-id="8deb6-155">2</span><span class="sxs-lookup"><span data-stu-id="8deb6-155">2</span></span></li>
<li><span data-ttu-id="8deb6-156">3</span><span class="sxs-lookup"><span data-stu-id="8deb6-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8deb6-157">Anda mahu menguntukkan 75 peratus kos kepada sumber pembiayaan pertama dan 25 peratus kepada sumber pembiayaan kedua.</span><span class="sxs-lookup"><span data-stu-id="8deb6-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8deb6-158">Apabila sama ada sumber pembiayaan tersebut habis, anda mahu membayar kos yang tinggal daripada sumber pembiayaan ketiga.</span><span class="sxs-lookup"><span data-stu-id="8deb6-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-159">Sumber pembiayaan 1</span><span class="sxs-lookup"><span data-stu-id="8deb6-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="8deb6-160">Sumber pembiayaan 2</span><span class="sxs-lookup"><span data-stu-id="8deb6-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="8deb6-161">Sumber pembiayaan 3</span><span class="sxs-lookup"><span data-stu-id="8deb6-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-162">75%</span><span class="sxs-lookup"><span data-stu-id="8deb6-162">75%</span></span></li>
<li><span data-ttu-id="8deb6-163">25%</span><span class="sxs-lookup"><span data-stu-id="8deb6-163">25%</span></span></li>
<li><span data-ttu-id="8deb6-164">100%</span><span class="sxs-lookup"><span data-stu-id="8deb6-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-165">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-165">1</span></span></li>
<li><span data-ttu-id="8deb6-166">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-166">1</span></span></li>
<li><span data-ttu-id="8deb6-167">2</span><span class="sxs-lookup"><span data-stu-id="8deb6-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8deb6-168">Anda mahu menguntukkan 75 peratus kos kepada sumber pembiayaan pertama dan 25 peratus kepada sumber pembiayaan kedua.</span><span class="sxs-lookup"><span data-stu-id="8deb6-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8deb6-169">Apabila sama ada sumber pembiayaan tersebut habis, anda mahu memisahkan kos yang tinggal antara sumber pembiayaan ketiga dan sumber pembiayaan keempat.</span><span class="sxs-lookup"><span data-stu-id="8deb6-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-170">Sumber pembiayaan 1</span><span class="sxs-lookup"><span data-stu-id="8deb6-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="8deb6-171">Sumber pembiayaan 2</span><span class="sxs-lookup"><span data-stu-id="8deb6-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="8deb6-172">Sumber pembiayaan 3</span><span class="sxs-lookup"><span data-stu-id="8deb6-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="8deb6-173">Sumber pembiayaan 4</span><span class="sxs-lookup"><span data-stu-id="8deb6-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-174">75%</span><span class="sxs-lookup"><span data-stu-id="8deb6-174">75%</span></span></li>
<li><span data-ttu-id="8deb6-175">25%</span><span class="sxs-lookup"><span data-stu-id="8deb6-175">25%</span></span></li>
<li><span data-ttu-id="8deb6-176">50%</span><span class="sxs-lookup"><span data-stu-id="8deb6-176">50%</span></span></li>
<li><span data-ttu-id="8deb6-177">50%</span><span class="sxs-lookup"><span data-stu-id="8deb6-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-178">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-178">1</span></span></li>
<li><span data-ttu-id="8deb6-179">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-179">1</span></span></li>
<li><span data-ttu-id="8deb6-180">2</span><span class="sxs-lookup"><span data-stu-id="8deb6-180">2</span></span></li>
<li><span data-ttu-id="8deb6-181">2</span><span class="sxs-lookup"><span data-stu-id="8deb6-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8deb6-182">Anda mahu menguntukkan 25 peratus kos pertama kepada sumber pembiayaan pertama dan selebihnya kepada sumber pembiayaan kedua.</span><span class="sxs-lookup"><span data-stu-id="8deb6-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-183">Sumber pembiayaan 1</span><span class="sxs-lookup"><span data-stu-id="8deb6-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="8deb6-184">Sumber pembiayaan 2</span><span class="sxs-lookup"><span data-stu-id="8deb6-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-185">25%</span><span class="sxs-lookup"><span data-stu-id="8deb6-185">25%</span></span></li>
<li><span data-ttu-id="8deb6-186">100%</span><span class="sxs-lookup"><span data-stu-id="8deb6-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8deb6-187">1</span><span class="sxs-lookup"><span data-stu-id="8deb6-187">1</span></span></li>
<li><span data-ttu-id="8deb6-188">2</span><span class="sxs-lookup"><span data-stu-id="8deb6-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="8deb6-189">Contoh: Berbilang sumber pembiayaan (rumit)</span><span class="sxs-lookup"><span data-stu-id="8deb6-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="8deb6-190">Anda mempunyai tiga sumber pembiayaan yang anda mahu gunakan dalam terbit yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="8deb6-191">Gunakan sumber pembiayaan 2 dan sumber pembiayaan 3 secara sama rata sehingga sumber pembiayaan 2 habis.</span><span class="sxs-lookup"><span data-stu-id="8deb6-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="8deb6-192">Terus menggunakan sumber pembiayaan 3 sehingga ia habis.</span><span class="sxs-lookup"><span data-stu-id="8deb6-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="8deb6-193">Gunakan sumber pembiayaan 1 selepas sumber pembiayaan 3 habis.</span><span class="sxs-lookup"><span data-stu-id="8deb6-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="8deb6-194">Untuk mencapai matlamat ini, anda mesti melakukan perkara berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="8deb6-195">Sediakan had pembiayaan untuk sumber pembiayaan 2 dan sumber pembiayaan 3 bagi amaun mereka masing-masing.</span><span class="sxs-lookup"><span data-stu-id="8deb6-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="8deb6-196">Cipta peraturan pembiayaan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="8deb6-197">Peraturan 1 (Keutamaan 1): Peruntukkan 50 peratus transaksi kepada sumber pembiayaan 2 dan 50 peratus kepada sumber pembiayaan 3.</span><span class="sxs-lookup"><span data-stu-id="8deb6-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="8deb6-198">Peraturan 2 (Keutamaan 2): Peruntukkan 100 peratus transaksi kepada sumber pembiayaan 3.</span><span class="sxs-lookup"><span data-stu-id="8deb6-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="8deb6-199">Peraturan 3 (Keutamaan 3): Peruntukkan 100 peratus transaksi kepada sumber pembiayaan 1.</span><span class="sxs-lookup"><span data-stu-id="8deb6-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="8deb6-200">Persediaan ini berfungsi kerana transaksi disemak terhadap peraturan dan had untuk menentukan sama ada mana-mana daripadanya dikenakan kepada transaksi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="8deb6-201">Jika tiada peraturan atau had khusus dikenakan kepada transaksi, Semua peraturan transaksi dikenakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="8deb6-202">Semua peraturan transaksi sepadan dengan semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="8deb6-203">Jika peraturan didapati sepadan dengan transaksi, peratusan yang telah diperuntukkan dalam peraturan tersebut dikenakan dahulu tetapi hanya selepas padanan disemak terhadap sebarang had yang telah disediakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="8deb6-204">Jika had telah dicapai dan dana sumber pembiayaan habis, peraturan pembiayaan yang berkaitan dengan had pembiayaan tersebut diabaikan dan semakan program untuk peraturan seterusnya dikenakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="8deb6-205">Dalam sesetengah kes, hanya sebahagian transaksi boleh diperuntukkan di bawah peraturan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="8deb6-206">Ini mungkin berlaku disebabkan had dicapai apabila transaksi diperuntukkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="8deb6-207">Dalam kes ini, hanya amaun tertentu diperuntukkan mengikut peraturan tersebut, seperti 50 peratus untuk setiap sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="8deb6-208">Ini ialah kes dalam peraturan 1, yang dihuraikan lebih awal dalam bahagian ini.</span><span class="sxs-lookup"><span data-stu-id="8deb6-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="8deb6-209">Selebihnya diperuntukkan mengikut peraturan seterusnya dalam jujukan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="8deb6-210">Jadual yang berikut memeriksa senario ini dengan lebih terperinci.</span><span class="sxs-lookup"><span data-stu-id="8deb6-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8deb6-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="8deb6-212"><strong>Butiran</strong></span><span class="sxs-lookup"><span data-stu-id="8deb6-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8deb6-213">Peraturan pembiayaan</span><span class="sxs-lookup"><span data-stu-id="8deb6-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-214">Peraturan 1 (Keutamaan 1): Semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="8deb6-215">Peruntukkan sumber pembiayaan 2 pada 50% dan sumber pembiayaan 3 pada 50%.</span><span class="sxs-lookup"><span data-stu-id="8deb6-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="8deb6-216">Peraturan 2 (Keutamaan 2): Semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="8deb6-217">Peruntukkan sumber pembiayaan 3 pada 100%.</span><span class="sxs-lookup"><span data-stu-id="8deb6-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="8deb6-218">Peraturan 3 (Keutamaan 2): Semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="8deb6-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="8deb6-219">Peruntukkan sumber pembiayaan 1 pada 100%.</span><span class="sxs-lookup"><span data-stu-id="8deb6-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8deb6-220">Had pembiayaan</span><span class="sxs-lookup"><span data-stu-id="8deb6-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-221">Had sumber pembiayaan 1 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="8deb6-222">Had sumber pembiayaan 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="8deb6-223">Had sumber pembiayaan 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8deb6-224">Transaksi 1</span><span class="sxs-lookup"><span data-stu-id="8deb6-224">Transaction 1</span></span></td>
<td><span data-ttu-id="8deb6-225"><strong>Amaun transaksi:</strong> Pembiayaan<strong>100.00:</strong> Transaksi dibayar mengikut peraturan 1 sahaja, kerana transaksi dibayar penuh selepas peraturan 1 dikenakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="8deb6-226">Transaksi dibiayai sama rata antara sumber pembiayaan 2 dan sumber pembiayaan 3.</span><span class="sxs-lookup"><span data-stu-id="8deb6-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="8deb6-227">Sumber pembiayaan 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="8deb6-228">Sumber pembiayaan 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8deb6-229">Transaksi 2</span><span class="sxs-lookup"><span data-stu-id="8deb6-229">Transaction 2</span></span></td>
<td><span data-ttu-id="8deb6-230"><strong>Amaun transaksi:</strong> Pembiayaan<strong>5,000.00:</strong> Transaksi dibayar mengikut kesemua tiga peraturan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="8deb6-231"><strong>Peraturan 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="8deb6-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="8deb6-232">Sumber pembiayaan 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="8deb6-233">Sumber pembiayaan 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="8deb6-234">
<strong>Peraturan 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="8deb6-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="8deb6-235">Sumber pembiayaan 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="8deb6-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="8deb6-236">
<strong>Peraturan 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="8deb6-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="8deb6-237">Sumber pembiayaan 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="8deb6-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8deb6-238">Jumlah dana yang diagihkan untuk setiap sumber pembiayaan</span><span class="sxs-lookup"><span data-stu-id="8deb6-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="8deb6-239">Sumber pembiayaan 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="8deb6-240">Sumber pembiayaan 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="8deb6-241">Sumber pembiayaan 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="8deb6-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="8deb6-242">Peraturan pengebilan</span><span class="sxs-lookup"><span data-stu-id="8deb6-242">Billing rules</span></span>
<span data-ttu-id="8deb6-243">Apabila anda berunding tentang kontrak projek dengan pelanggan, anda mentakrifkan cara dan masa anda boleh menginvois pelanggan untuk kerja bagi satu projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="8deb6-244">Selepas anda menyediakan kontrak projek dan projek, anda boleh menyediakan peraturan pengebilan untuk projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="8deb6-245">Peraturan pengebilan adalah berdasarkan terma projek yang ditentukan dalam kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="8deb6-246">Peraturan pengebilan yang boleh anda cipta bergantung pada terma kontrak projek dan jenis projek, seperti Masa dan bahan atau Harga Tetap, yang anda kaitkan dengan peraturan pengebilan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="8deb6-247">Anda boleh mencipta lebih daripada satu peraturan pengebilan untuk kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="8deb6-248">Anda juga boleh menetapkan peraturan pengebilan kepada berbilang projek yang dikaitkan dengan kontrak projek yang sama dan mempunyai terma pengebilan yang serupa.</span><span class="sxs-lookup"><span data-stu-id="8deb6-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="8deb6-249">Anda boleh menyediakan jenis peraturan pengebilan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="8deb6-250">**Unit penghantaran** – Invois pelanggan apabila anda melengkapkan unit penghantaran.</span><span class="sxs-lookup"><span data-stu-id="8deb6-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="8deb6-251">Anda mentakrifkan unit penghantaran dalam kontrak.</span><span class="sxs-lookup"><span data-stu-id="8deb6-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="8deb6-252">**Kemajuan** – Invois pelanggan apabila anda melengkapkan peraturan projek yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="8deb6-253">Anda boleh menyediakan peraturan pengebilan untuk mengira secara automatik peratusan kerja yang dilengkapkan atau anda boleh mengira secara manual peratusan kerja yang dilengkapkan dan amaun untuk menginvois pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="8deb6-254">**Pencapaian** – Invois pelanggan untuk amaun penuh pencapaian projek apabila pencapaian dicapai.</span><span class="sxs-lookup"><span data-stu-id="8deb6-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="8deb6-255">**Yuran** – Invois pelanggan untuk perkhidmatan anda serta yuran pengurusan, yang pada lazimnya peratusan kos perkhidmatan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="8deb6-256">**Masa dan bahan** – Invois pelanggan untuk nilai masa dan bahan yang digunakan dalam projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="8deb6-257">Untuk semua jenis peraturan pengebilan, anda boleh menentukan peratusan penahanan yang dipotong daripada invois pelanggan sehingga projek mencapai peringkat yang telah dipersetujui.</span><span class="sxs-lookup"><span data-stu-id="8deb6-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="8deb6-258">Peratusan penahanan bayaran ditentukan dalam kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="8deb6-259">Amaun dikira berdasarkan dan ditolak daripada, jumlah nilai barisan dalam invois pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="8deb6-260">Untuk peraturan pengebilan **Masa dan bahan** dan **Kemajuan** , anda boleh menetapkan kategori boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="8deb6-261">Kategori boleh dituntut menunjukkan transaksi yang perlu disertakan dalam invois pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="8deb6-262">Apabila anda bersedia untuk menginvois pelanggan, amaun untuk menginvois bagi projek dikira berdasarkan peraturan pengebilan dan cadangan invois projek dijanakan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="8deb6-263">Bahagian berikut memberikan contoh yang menunjukkan cara menyediakan dan menguruskan peraturan pengebilan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="8deb6-264">Contoh: Cipta peraturan pengebilan yang berdasarkan bilangan unit yang dihantar</span><span class="sxs-lookup"><span data-stu-id="8deb6-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="8deb6-265">Organisasi anda membuat perjanjian untuk menyediakan sejumlah lima sesi latihan kepada pekerja pelanggan pada kos 10,000 setiap sesi latihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="8deb6-266">Anda menginvois pelanggan selepas setiap sesi latihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="8deb6-267">Apabila anda menyediakan peraturan pengebilan untuk kontrak tersebut, anda menggunakan nilai yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="8deb6-268">Unit penghantaran ialah satu sesi latihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="8deb6-269">Harga unit ialah 10,000 setiap sesi latihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="8deb6-270">Jumlah bilangan unit ialah lima sesi latihan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="8deb6-271">Apabila anda telah melengkapkan satu sesi latihan, anda boleh mencipta invois untuk 10,000 bagi unit pertama yang telah dihantar dan menghantar invois kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="8deb6-272">Contoh: Cipta peraturan pengebilan yang berdasarkan peratusan pelengkapan projek yang ditentukan (pengiraan manual)</span><span class="sxs-lookup"><span data-stu-id="8deb6-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="8deb6-273">Organisasi anda, sebuah firma perunding perisian, membuat perjanjian dengan pelanggan untuk membangunkan sebahagian produk yang sedang dibangunkan oleh pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="8deb6-274">Organisasi anda bersetuju untuk menghantar kod perisian dalam tempoh enam bulan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="8deb6-275">Pelanggan bersetuju untuk membayar organisasi anda sejumlah 100,000 untuk kerja tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="8deb6-276">Anda mencipta peraturan pengebilan untuk menginvois pelanggan berdasarkan peratusan kerja yang dilengkapkan bagi projek tersebut, seperti yang ditentukan dalam kontrak.</span><span class="sxs-lookup"><span data-stu-id="8deb6-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="8deb6-277">Pada penghujung bulan pertama, anda bertemu dengan pelanggan untuk menentukan peratusan kerja dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="8deb6-278">Selepas anda dan pelanggan menyemak semula projek, anda membuat keputusan bahawa projek tersebut 15 peratusan dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="8deb6-279">Anda mencipta invois untuk 15,000 (15 peratus daripada 100,000) dan menghantarnya kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="8deb6-280">Contoh: Cipta peraturan pengebilan yang berdasarkan peratusan pelengkapan projek yang ditentukan (pengiraan automatik)</span><span class="sxs-lookup"><span data-stu-id="8deb6-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="8deb6-281">Organisasi anda, sebuah firma pembangunan perisian, bersetuju untuk membangunkan pakej perakaunan gaji untuk pelanggan pada harga 30,000.</span><span class="sxs-lookup"><span data-stu-id="8deb6-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="8deb6-282">Pelanggan bersetuju untuk membayar organisasi anda berdasarkan peratusan kerja dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="8deb6-283">Anda menganggarkan bahawa kos projek ialah 20,000.</span><span class="sxs-lookup"><span data-stu-id="8deb6-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="8deb6-284">Kontrak projek menentukan kategori kerja yang anda gunakan dalam proses pengebilan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="8deb6-285">Anda menyediakan peraturan pengebilan yang mengira secara automatik amaun invois untuk peratusan kerja yang dilengkapkan untuk setiap kategori.</span><span class="sxs-lookup"><span data-stu-id="8deb6-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="8deb6-286">Anda menyediakan belanjawan untuk setiap kategori:</span><span class="sxs-lookup"><span data-stu-id="8deb6-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="8deb6-287">**Pembangunan** – Kos 15,000 dan hasil 20,000</span><span class="sxs-lookup"><span data-stu-id="8deb6-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="8deb6-288">**Pemasangan** – Kos 5,000 dan hasil 10,000</span><span class="sxs-lookup"><span data-stu-id="8deb6-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="8deb6-289">Apabila anda mencipta invois pelanggan buat pertama kali, amaun invois tersebut dikira secara automatik berdasarkan maklumat yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="8deb6-290">Selepas sebulan, pekerja bagi projek tersebut menyerahkan lembaran masa untuk projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="8deb6-291">Kos jam pekerja ialah 5,000 untuk pembangunan dan 1,000 untuk pemasangan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="8deb6-292">Kerja pembangunan adalah 33 peratus dilengkapkan (5,000 kos sebenar/15,000 kos belanjawan) dan kerja pemasangan adalah 20 peratus dilengkapkan (1,000 kos sebenar/5,000 kos belanjawan).</span><span class="sxs-lookup"><span data-stu-id="8deb6-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="8deb6-293">Amaun invois 8,667 dikira secara automatik (33 peratus daripada 20,000 + 20 peratus daripada 10,000).</span><span class="sxs-lookup"><span data-stu-id="8deb6-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="8deb6-294">Anda mencipta invois untuk 8,667 dan menghantarnya kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="8deb6-295">Contoh: Cipta peraturan pengebilan yang berdasarkan pencapaian yang telah dipersetujui</span><span class="sxs-lookup"><span data-stu-id="8deb6-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="8deb6-296">Organisasi anda, sebuah firma perunding pengurusan, bersetuju untuk melakukan penyelidikan pasaran untuk produk pelanggan yang dirancang oleh pelanggan untuk dijual.</span><span class="sxs-lookup"><span data-stu-id="8deb6-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="8deb6-297">Pelanggan bersetuju untuk menggunakan perkhidmatan anda untuk tempoh tiga bulan, bermula pada bulan Mac dan bersetuju untuk membayar organisasi anda sebanyak 50,000.</span><span class="sxs-lookup"><span data-stu-id="8deb6-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="8deb6-298">Projek ini mempunyai tiga pencapaian:</span><span class="sxs-lookup"><span data-stu-id="8deb6-298">The project has three milestones:</span></span>

-   <span data-ttu-id="8deb6-299">Pencapaian 1: Kumpul data pelanggan – 31 Mac</span><span class="sxs-lookup"><span data-stu-id="8deb6-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="8deb6-300">Pencapaian 2: Analisis data pelanggan – 30 April</span><span class="sxs-lookup"><span data-stu-id="8deb6-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="8deb6-301">Pencapaian 3: Bentangkan cadangan kebolehjayaan produk – 31 Mei</span><span class="sxs-lookup"><span data-stu-id="8deb6-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="8deb6-302">Pelanggan bersetuju untuk membayar organisasi anda sebanyak 10,000 untuk pencapaian pertama, 20,000 untuk pencapaian kedua dan 20,000 untuk pencapaian ketiga.</span><span class="sxs-lookup"><span data-stu-id="8deb6-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="8deb6-303">Apabila anda menyediakan kontrak projek, anda bersetuju untuk mengebil pelanggan berdasarkan pencapaian yang telah dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="8deb6-304">Persediaan peraturan pengebilan termasuk langkah yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="8deb6-305">Takrifkan pencapaian projek.</span><span class="sxs-lookup"><span data-stu-id="8deb6-305">Define the project milestones.</span></span>
-   <span data-ttu-id="8deb6-306">Takrifkan amaun untuk menginvois pelanggan apabila setiap pencapaian dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="8deb6-307">Apabila pencapaian pertama dilengkapkan pada 31 Mac, anda menandakan pencapaian tersebut sebagai dilengkapkan dan kemudian mencipta invois untuk 10,000 dan menghantarnya kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="8deb6-308">Anda tidak boleh mencipta invois untuk satu pencapaian sehingga anda telah menandakan pencapaian tersebut sebagai dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="8deb6-309">Contoh: Cipta peraturan pengebilan yang berdasarkan perkhidmatan serta yuran pengurusan</span><span class="sxs-lookup"><span data-stu-id="8deb6-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="8deb6-310">Organisasi anda, sebuah firma perunding pengurusan, bersetuju untuk melakukan penyelidikan pasaran bagi menilai kebolehjayaan produk yang sedang dibangunkan oleh pelanggan, sebuah syarikat runcit.</span><span class="sxs-lookup"><span data-stu-id="8deb6-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="8deb6-311">Terma perjanjian menentukan bahawa anda akan menyediakan perkhidmatan bagi tiga perunding pengurusan terbaik anda yang akan melakukan penyelidikan mengikut masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="8deb6-312">Pelanggan bersetuju untuk membayar sebanyak 100 setiap jam, serta 10 peratus yuran pengurusan untuk waktu perundingan yang dikenakan kepada projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8deb6-313">Apabila anda menyediakan kontrak projek, cipta peraturan pengebilan untuk menambahkan 10 peratus yuran pengurusan untuk waktu perundingan yang dikenakan kepada projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8deb6-314">Apabila anda mencipta invois untuk pelanggan, pelanggan dibilkan 10 peratus yuran pengurusan serta kos jam rundingan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="8deb6-315">Contohnya, jika tiga perunding telah bekerja sejumlah 200 jam dalam projek, invois untuk 22,000 dicipta berdasarkan pengiraan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="8deb6-316">200 jam dengan bayaran 100 setiap jam = 20,000</span><span class="sxs-lookup"><span data-stu-id="8deb6-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="8deb6-317">10 peratus yuran pengurusan = 2,000</span><span class="sxs-lookup"><span data-stu-id="8deb6-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="8deb6-318">Jumlah amaun invois = 22,000</span><span class="sxs-lookup"><span data-stu-id="8deb6-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="8deb6-319">Jika yuran boleh dikenakan cukai kepada pelanggan dan anda memilih kumpulan cukai jualan dalam kontrak projek, kumpulan cukai jualan dimasukkan secara automatik dalam peraturan pengebilan untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="8deb6-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="8deb6-320">Contoh: Cipta peraturan pengebilan untuk nilai bagi masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="8deb6-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="8deb6-321">Organisasi anda, sebuah firma perunding perisian, bersetuju untuk menyediakan lima perunding teknikal bagi mengusahakan projek pembangunan perisian untuk pelanggan selama enam bulan berikutnya.</span><span class="sxs-lookup"><span data-stu-id="8deb6-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="8deb6-322">Pelanggan bersetuju untuk membayar 150 untuk setiap jam rundingan serta kos bekalan pejabat.</span><span class="sxs-lookup"><span data-stu-id="8deb6-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="8deb6-323">Organisasi anda menghantar invois kepada pelanggan pada hujung setiap bulan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="8deb6-324">Apabila anda menyediakan kontrak projek, anda bersetuju untuk mengebil pelanggan setiap bulan untuk masa dan bahan bagi projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="8deb6-325">Anda mencipta peraturan pengebilan yang mengandungi maklumat yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8deb6-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="8deb6-326">Tempoh kontrak ialah enam bulan.</span><span class="sxs-lookup"><span data-stu-id="8deb6-326">The contract period is six months.</span></span>
-   <span data-ttu-id="8deb6-327">Masa rundingan dikira pada kadar 150 setiap jam.</span><span class="sxs-lookup"><span data-stu-id="8deb6-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="8deb6-328">Bekalan pejabat diinvoiskan pada kos dan jumlah kos untuk projek tidak boleh melebihi 10,000.</span><span class="sxs-lookup"><span data-stu-id="8deb6-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="8deb6-329">Anda mencipta invois pelanggan pada hujung setiap bulan kalendar sepanjang projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="8deb6-330">Sepanjang bulan pertama, sejumlah 800 jam direkodkan oleh perunding bagi projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="8deb6-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="8deb6-331">Kos bekalan pejabat. yang dicaj kepada projek ialah 2,000.</span><span class="sxs-lookup"><span data-stu-id="8deb6-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="8deb6-332">Oleh itu, pada hujung bulan, anda mencipta invois untuk 122,000, yang dikira sebagai 800 jam pada harga 150 setiap jam, serta 2,000 untuk bekalan pejabat.</span><span class="sxs-lookup"><span data-stu-id="8deb6-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



