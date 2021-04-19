---
title: Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek
description: Topik ini memberikan maklumat tentang cara untuk menambah komponen boleh dituntut kepada baris kontrak dalam Operasi Projek.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858484"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="b36c8-103">Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="b36c8-104">_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b36c8-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b36c8-105">Baris kontrak berasaskan projek mempunyai komponen *disertakan* dan komponen *boleh dituntut*.</span><span class="sxs-lookup"><span data-stu-id="b36c8-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="b36c8-106">Komponen yang disertakan ialah komponen yang tertakluk kepada:</span><span class="sxs-lookup"><span data-stu-id="b36c8-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="b36c8-107">Kaedah pengebilan dan pecahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="b36c8-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="b36c8-108">Had yang tidak melebihi</span><span class="sxs-lookup"><span data-stu-id="b36c8-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="b36c8-109">Tetapan kekerapan invois ditakrifkan pada baris kontrak berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="b36c8-110">Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**.</span><span class="sxs-lookup"><span data-stu-id="b36c8-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="b36c8-111">Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris kontrak:</span><span class="sxs-lookup"><span data-stu-id="b36c8-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="b36c8-112">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-112">Chargeable</span></span>
  - <span data-ttu-id="b36c8-113">Tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-113">Non-chargeable</span></span>

<span data-ttu-id="b36c8-114">Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="b36c8-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="b36c8-115">Boleh dituntut ditakrifkan pada tugas untuk baris kontrak projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian.</span><span class="sxs-lookup"><span data-stu-id="b36c8-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="b36c8-116">Jika medan **Tugas Termasuk** pada baris kontrak adalah kosong atau ditetapkan kepada **Keseluruhan projek**, tab **Tugas boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="b36c8-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="b36c8-117">Boleh dituntut ditakrifkan pada peranan untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Masa**.</span><span class="sxs-lookup"><span data-stu-id="b36c8-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="b36c8-118">Jika medan **Sertakan Masa** pada baris kontrak ditetapkan kepada **Tidak**, tab **Peranan boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="b36c8-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="b36c8-119">Boleh dituntut ditakrifkan pada kategori transaksi untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="b36c8-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="b36c8-120">Jika medan **Sertakan Perbelanjaan** ditetapkan kepada **Tidak**, tab **Kategori boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="b36c8-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b36c8-121">Kemas kini tugas projek sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="b36c8-122">Tugas projek boleh dituntut atau tidak boleh dituntut pada baris kontrak khusus, yang memungkinkan persediaan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="b36c8-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="b36c8-123">Jika baris kontrak berasaskan projek termasuk **Masa** dan tugas tertentu, **T1** dikaitkan dengannya sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="b36c8-124">Jika terdapat baris kontrak kedua yang termasuk **Perbelanjaan**, anda boleh mengaitkan tugas T1 pada baris kontrak sebagai tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="b36c8-125">Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="b36c8-126">Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada tugas baris kontrak sub.</span><span class="sxs-lookup"><span data-stu-id="b36c8-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="b36c8-127">Sebagai alternatif, anda boleh mengemas kini medan **Jenis Pengebilan** pada sub persediaan Pengebilan tugas bagi projek yang menunjukkan baris kontrak yang berkaitan dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="b36c8-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b36c8-128">Kemas kini peranan sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="b36c8-129">Peranan boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="b36c8-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="b36c8-130">Jenis pengebilan peranan boleh dikonfigurasikan pada tab **Peranan Boleh Dituntut** bagi baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b36c8-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="b36c8-131">Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="b36c8-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="b36c8-132">Kemas kini kategori transaksi sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="b36c8-133">Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="b36c8-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="b36c8-134">Jenis pengebilan transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** bagi baris kontrak berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="b36c8-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="b36c8-135">Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="b36c8-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="b36c8-136">Menyelesaikan kebolehtuntutan</span><span class="sxs-lookup"><span data-stu-id="b36c8-136">Resolve chargeability</span></span>

<span data-ttu-id="b36c8-137">Anggaran atau aktual yang dicipta untuk masa hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="b36c8-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="b36c8-138">**Masa** disertakan pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b36c8-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="b36c8-139">**Peranan** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak.</span><span class="sxs-lookup"><span data-stu-id="b36c8-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="b36c8-140">**Tugas Disertakan** ditetapkan untuk **Tugas yang Dipilih** pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b36c8-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="b36c8-141">Jika ketiga-tiga perkara ini benar, tugas itu dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="b36c8-142">Anggaran atau aktual yang dicipta untuk perbelanjaan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="b36c8-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="b36c8-143">**Perbelanjaan** disertakan pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="b36c8-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="b36c8-144">**Kategori transaksi** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak</span><span class="sxs-lookup"><span data-stu-id="b36c8-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="b36c8-145">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="b36c8-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="b36c8-146">Jika ketiga-tiga perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="b36c8-147">Anggaran atau aktual yang dicipta untuk bahan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="b36c8-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="b36c8-148">**Bahan** disertakan pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="b36c8-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="b36c8-149">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="b36c8-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="b36c8-150">Jika kedua-dua perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="b36c8-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-151">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b36c8-152">
                    <strong>Termasuk Perbelanjaan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b36c8-153">
                    <strong>Termasuk Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="b36c8-154">
                    <strong>Tugas yang Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-155">
                    <strong>Peranan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-157">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="b36c8-158">
                    <strong>Kesan Kebolehtuntutan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-159">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-160">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-161">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-162">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-163">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-164">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-165">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-166">Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-167">Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-168">Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-169">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-170">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-171">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-172">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="b36c8-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-173">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-174">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-175">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-176">Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-177">Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-178">Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-179">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-180">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-181">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-182">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="b36c8-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-183">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-184">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-185">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-186">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-187">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b36c8-188">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-189">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-190">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-191">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-192">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="b36c8-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-193">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-194">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-195">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-196">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-197">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-198">Jenis pengebilan pada aktual bahan: <strong>Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-199">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-200">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-201">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-202">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="b36c8-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-203">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-204">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-205">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-206">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-207">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-208">Jenis pengebilan pada aktual bahan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-209">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-210">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-211">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-212">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="b36c8-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-213">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-214">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-215">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-216">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-217">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-218">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-219">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-220">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-221">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-222">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-223">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-224">
                    <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-225">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-226">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-227">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b36c8-228">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-229">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-230">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-231">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-232">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-233">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-234">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-235">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-236">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-237">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-238">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-239">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b36c8-240">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-241">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-242">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-243">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-244">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-245">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-246">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b36c8-247">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-248">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-249">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b36c8-250">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b36c8-251">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-252">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-253">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-254">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-255">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-256">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-257">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-258">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-259">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-260">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b36c8-261">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-262">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-263">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-264">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-265">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-266">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b36c8-267">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="b36c8-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b36c8-268">Jenis pengebilan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b36c8-269">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b36c8-270">Ya</span><span class="sxs-lookup"><span data-stu-id="b36c8-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b36c8-271">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b36c8-272">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="b36c8-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b36c8-273">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b36c8-274">
                    <strong>Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b36c8-275">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="b36c8-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b36c8-276">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-277">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b36c8-278">Jenis pengebilan pada aktual bahan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b36c8-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
