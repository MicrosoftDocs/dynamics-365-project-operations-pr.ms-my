---
title: Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek
description: Topik ini memberikan maklumat tentang cara untuk menambah komponen boleh dituntut kepada baris kontrak dalam Operasi Projek.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003732"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="1a219-103">Konfigurasi komponen boleh dicaj bagi baris kontrak berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="1a219-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="1a219-104">_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="1a219-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1a219-105">Baris kontrak berasaskan projek mempunyai komponen *disertakan* dan komponen *boleh dituntut*.</span><span class="sxs-lookup"><span data-stu-id="1a219-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="1a219-106">Komponen yang disertakan ialah komponen yang tertakluk kepada:</span><span class="sxs-lookup"><span data-stu-id="1a219-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="1a219-107">Kaedah pengebilan dan pecahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="1a219-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="1a219-108">Had yang tidak melebihi</span><span class="sxs-lookup"><span data-stu-id="1a219-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="1a219-109">Tetapan kekerapan invois ditakrifkan pada baris kontrak berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="1a219-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="1a219-110">Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**.</span><span class="sxs-lookup"><span data-stu-id="1a219-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="1a219-111">Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris kontrak:</span><span class="sxs-lookup"><span data-stu-id="1a219-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="1a219-112">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-112">Chargeable</span></span>
  - <span data-ttu-id="1a219-113">Tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-113">Non-chargeable</span></span>

<span data-ttu-id="1a219-114">Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="1a219-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="1a219-115">Boleh dituntut ditakrifkan pada tugas untuk baris kontrak projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian.</span><span class="sxs-lookup"><span data-stu-id="1a219-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="1a219-116">Jika medan **Tugas Termasuk** pada baris kontrak adalah kosong atau ditetapkan kepada **Keseluruhan projek**, tab **Tugas boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="1a219-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="1a219-117">Boleh dituntut ditakrifkan pada peranan untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Masa**.</span><span class="sxs-lookup"><span data-stu-id="1a219-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="1a219-118">Jika medan **Sertakan Masa** pada baris kontrak ditetapkan kepada **Tidak**, tab **Peranan boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="1a219-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="1a219-119">Boleh dituntut ditakrifkan pada kategori transaksi untuk baris kontrak projek hanya terpakai untuk kelas transaksi **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="1a219-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="1a219-120">Jika medan **Sertakan Perbelanjaan** ditetapkan kepada **Tidak**, tab **Kategori boleh dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="1a219-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1a219-121">Kemas kini tugas projek sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="1a219-122">Tugas projek boleh dituntut atau tidak boleh dituntut pada baris kontrak khusus, yang memungkinkan persediaan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="1a219-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="1a219-123">Jika baris kontrak berasaskan projek termasuk **Masa** dan tugas tertentu, **T1** dikaitkan dengannya sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="1a219-124">Jika terdapat baris kontrak kedua yang termasuk **Perbelanjaan**, anda boleh mengaitkan tugas T1 pada baris kontrak sebagai tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="1a219-125">Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="1a219-126">Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada tugas baris kontrak sub.</span><span class="sxs-lookup"><span data-stu-id="1a219-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="1a219-127">Sebagai alternatif, anda boleh mengemas kini medan **Jenis Pengebilan** pada sub persediaan Pengebilan tugas bagi projek yang menunjukkan baris kontrak yang berkaitan dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="1a219-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1a219-128">Kemas kini peranan sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="1a219-129">Peranan boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="1a219-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="1a219-130">Jenis pengebilan peranan boleh dikonfigurasikan pada tab **Peranan Boleh Dituntut** bagi baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="1a219-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="1a219-131">Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="1a219-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="1a219-132">Kemas kini kategori transaksi sebagai boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="1a219-133">Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="1a219-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="1a219-134">Jenis pengebilan transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** bagi baris kontrak berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="1a219-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="1a219-135">Untuk berbuat demikian, kemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="1a219-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="1a219-136">Menyelesaikan kebolehtuntutan</span><span class="sxs-lookup"><span data-stu-id="1a219-136">Resolve chargeability</span></span>

<span data-ttu-id="1a219-137">Anggaran atau aktual yang dicipta untuk masa hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="1a219-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="1a219-138">**Masa** disertakan pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="1a219-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="1a219-139">**Peranan** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak.</span><span class="sxs-lookup"><span data-stu-id="1a219-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="1a219-140">**Tugas Disertakan** ditetapkan untuk **Tugas yang Dipilih** pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="1a219-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="1a219-141">Jika ketiga-tiga perkara ini benar, tugas itu dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="1a219-142">Anggaran atau aktual yang dicipta untuk perbelanjaan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="1a219-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="1a219-143">**Perbelanjaan** disertakan pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="1a219-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="1a219-144">**Kategori transaksi** dikonfigurasikan sebagai boleh dituntut pada barisan kontrak</span><span class="sxs-lookup"><span data-stu-id="1a219-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="1a219-145">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="1a219-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="1a219-146">Jika ketiga-tiga perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="1a219-147">Anggaran atau aktual yang dicipta untuk bahan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="1a219-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="1a219-148">**Bahan** disertakan pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="1a219-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="1a219-149">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="1a219-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="1a219-150">Jika kedua-dua perkara ini benar, **Tugas** dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="1a219-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-151">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1a219-152">
                    <strong>Termasuk Perbelanjaan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1a219-153">
                    <strong>Termasuk Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="1a219-154">
                    <strong>Tugas yang Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-155">
                    <strong>Peranan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-157">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="1a219-158">
                    <strong>Kesan Kebolehtuntutan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-159">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-160">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-161">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-162">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-163">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-164">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-165">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-166">Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-167">Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-168">Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-169">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-170">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-171">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-172">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="1a219-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-173">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-174">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-175">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-176">Pengebilan pada aktual masa: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-177">Jenis pengebilan pada aktual perbelanjaan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-178">Jenis pengebilan pada aktual bahan: <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-179">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-180">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-181">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-182">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="1a219-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-183">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-184">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-185">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-186">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-187">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1a219-188">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-189">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-190">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-191">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-192">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="1a219-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-193">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-194">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-195">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-196">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-197">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-198">Jenis pengebilan pada aktual bahan: <strong>Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-199">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-200">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-201">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-202">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="1a219-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-203">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-204">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-205">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-206">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-207">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-208">Jenis pengebilan pada aktual bahan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-209">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-210">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-211">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-212">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="1a219-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-213">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-214">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-215">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-216">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-217">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-218">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-219">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-220">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-221">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-222">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-223">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-224">
                    <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-225">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-226">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-227">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1a219-228">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-229">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-230">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-231">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-232">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-233">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-234">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-235">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-236">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-237">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-238">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-239">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1a219-240">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-241">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-242">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-243">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-244">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-245">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-246">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1a219-247">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-248">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-249">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1a219-250">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1a219-251">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-252">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-253">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-254">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-255">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-256">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-257">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-258">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-259">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-260">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1a219-261">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-262">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-263">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-264">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-265">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-266">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1a219-267">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="1a219-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1a219-268">Jenis pengebilan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1a219-269">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1a219-270">Ya</span><span class="sxs-lookup"><span data-stu-id="1a219-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1a219-271">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1a219-272">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="1a219-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1a219-273">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1a219-274">
                    <strong>Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1a219-275">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="1a219-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1a219-276">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-277">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1a219-278">Jenis pengebilan pada aktual bahan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1a219-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
