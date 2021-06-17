---
title: Konfigurasikan komponen boleh dituntut bagi baris sebut harga
description: Topik ini menyediakan maklumat tentang menyediakan komponen boleh dituntut dan tidak boleh dituntut pada baris sebut harga berasaskan projek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003777"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="2b259-103">Konfigurasikan komponen boleh dikenakan bagi baris sebut harga</span><span class="sxs-lookup"><span data-stu-id="2b259-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="2b259-104">_**Gunakan Pada:** Pelaksanaan ringan - urusan untuk penginvoisan proforma, Project Operations untuk senario berdasarkan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="2b259-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b259-105">Baris sebut harga berasaskan projek mempunyai konsep komponen *disertakan* dan komponen *boleh dituntut*.</span><span class="sxs-lookup"><span data-stu-id="2b259-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="2b259-106">Komponen yang disertakan adalah tertakluk kepada:</span><span class="sxs-lookup"><span data-stu-id="2b259-106">Included components are subject to:</span></span>

  - <span data-ttu-id="2b259-107">Kaedah pengebilan dan pecahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="2b259-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="2b259-108">Had yang tidak melebihi</span><span class="sxs-lookup"><span data-stu-id="2b259-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="2b259-109">Tetapan kekerapan invois ditakrifkan pada baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="2b259-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="2b259-110">Subset komponen yang termasuk boleh ditandakan sebagai boleh dituntut menggunakan medan **Jenis Pengebilan**.</span><span class="sxs-lookup"><span data-stu-id="2b259-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="2b259-111">Medan **Jenis Pengebilan** ialah set pilihan yang membenarkan nilai berikut dalam konteks baris sebut harga:</span><span class="sxs-lookup"><span data-stu-id="2b259-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="2b259-112">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-112">Chargeable</span></span>
  - <span data-ttu-id="2b259-113">Tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-113">Non-chargeable</span></span>

<span data-ttu-id="2b259-114">Komponen boleh dituntut boleh ditakrifkan pada tugas, peranan dan kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="2b259-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="2b259-115">Boleh dituntut ditakrifkan pada tugas untuk baris sebut harga projek dan terpakai untuk semua kelas transaksi yang dimasukkan ke dalam talian tersebut.</span><span class="sxs-lookup"><span data-stu-id="2b259-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="2b259-116">Jika medan **Sertakan Tugas** ditetapkan kepada **Seluruh projek** atau dibiarkan kosong, tab **Tugas Boleh Dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="2b259-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="2b259-117">Boleh dituntut ditakrifkan pada peranan untuk baris sebut harga dan hanay terpakai untuk kelas transaksi **Masa**.</span><span class="sxs-lookup"><span data-stu-id="2b259-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="2b259-118">Jika medan, **Sertakan Masa** ditetapkan kepada **Tidak** pada baris projek, tab **Peranan Boleh Dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="2b259-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="2b259-119">Boleh dituntut ditakrifkan pada kategori transaksi untuk baris sebut harga dan hanya terpakai untuk kelas transaksi **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="2b259-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="2b259-120">Jika medan, **Sertakan Perbelanjaan** ditetapkan kepada **Tidak** pada baris projek, tab **Kategori Boleh Dituntut** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="2b259-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="2b259-121">Kemas kini tugas projek untuk menjadi boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="2b259-122">Tugas projek boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berdasarkan projek khusus, yang memungkinkan persediaan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="2b259-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="2b259-123">Jika baris sebut harga berasaskan projek termasuk **Masa** dan tugas **T1**, tugas itu dikaitkan dengan baris sebut harga sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="2b259-124">Jika terdapat baris sebut harga kedua yang menyertakan **Perbelanjaan**, anda boleh mengaitkan tugas **T1** pada baris ssebut harga sebagai tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="2b259-125">Hasilnya adalah semua masa yang direkodkan pada tugas boleh dituntut dan semua perbelanjaan yang direkodkan pada tugas adalah tidak boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="2b259-126">Jenis pengebilan tugas boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Tugas Baris Sebut Harga**.</span><span class="sxs-lookup"><span data-stu-id="2b259-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="2b259-127">Sebagai alternatif, anda boleh mengemas kini jenis pengebilan untuk tugas projek dalam medan **Jenis Pengebilan** pada subgrid pada penyediaan pengebilan tugas bagi projek yang menunjukkan baris sebut harga yang berkaitan dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="2b259-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="2b259-128">Kemas kini peranan menjadi boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="2b259-129">Peranan boleh jadi boleh dituntut atau tidak boleh dituntut dalam konteks baris sebut harga berasaskan projek tertentu.</span><span class="sxs-lookup"><span data-stu-id="2b259-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="2b259-130">Jenis pengebilan tugas peranan boleh dikonfigurasikan pada tab **Tugas Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Peranan Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="2b259-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="2b259-131">Kemas kini kategori transaksi menjadi boleh dituntut atau tidak boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="2b259-132">Kategori transaksi boleh jadi boleh dituntut atau tidak boleh dituntut ke atas baris sebut harga tertentu.</span><span class="sxs-lookup"><span data-stu-id="2b259-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="2b259-133">Jenis pengebilan tugas transaksi boleh dikonfigurasikan pada tab **Kategori Boleh Dituntut** baris kontrak dengan mengemas kini medan **Jenis Pengebilan** pada subgrid **Kategori Boleh Dituntut**.</span><span class="sxs-lookup"><span data-stu-id="2b259-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="2b259-134">Menyelesaikan kebolehtuntutan</span><span class="sxs-lookup"><span data-stu-id="2b259-134">Resolve chargeability</span></span>
<span data-ttu-id="2b259-135">Anggaran atau aktual yang dicipta untuk masa akan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="2b259-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="2b259-136">**Masa** disertakan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="2b259-137">**Peranan** dikonfigurasikan sebagai boleh dituntut pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="2b259-138">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="2b259-139">Jika ketiga-tiga perkara ini benar, **Tugas** juga dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="2b259-140">Anggaran atau aktual yang dicipta untuk perbelanjaan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="2b259-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="2b259-141">**Perbelanjaan** disertakan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="2b259-142">**Kategori transaksi** dikonfigurasikan sebagai boleh dituntut pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="2b259-143">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="2b259-144">Jika ketiga-tiga perkara ini benar, **Tugas** juga dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="2b259-145">Anggaran atau aktual yang dicipta untuk bahan akan hanya dianggap boleh dituntut jika:</span><span class="sxs-lookup"><span data-stu-id="2b259-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="2b259-146">**Bahan** disertakan pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="2b259-147">**Tugas Disertakan** ditetapkan untuk **Tugas yang dipilih** pada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="2b259-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="2b259-148">Jika kedua-dua perkara ini benar, **Tugas** juga harus dikonfigurasikan sebagai boleh dituntut.</span><span class="sxs-lookup"><span data-stu-id="2b259-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-149">
                    <strong>Termasuk Masa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2b259-150">
                    <strong>Termasuk Perbelanjaan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2b259-151">
                    <strong>Termasuk Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="2b259-152">
                    <strong>Tugas yang Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-153">
                    <strong>Peranan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-155">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="2b259-156">
                    <strong>Kesan kebolehtuntutan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-157">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-158">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-159">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-160">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-161">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-162">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-163">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-164">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-165">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-166">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-167">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-168">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-169">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-170">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="2b259-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-171">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-172">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-173">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-174">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-175">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-176">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-177">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-178">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-179">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-180">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="2b259-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-181">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-182">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-183">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-184">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-185">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-186">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-187">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-188">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-189">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-190">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="2b259-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-191">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-192">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-193">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-194">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-195">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-196">Jenis pengebilan pada aktual bahan: <strong>Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-197">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-198">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-199">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-200">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="2b259-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-201">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-202">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-203">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-204">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-205">Jenis pengebilan pada aktual perbelanjaan: <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-206">Jenis pengebilan pada aktual bahan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-207">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-208">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-209">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-210">Tugas terpilih sahaja</span><span class="sxs-lookup"><span data-stu-id="2b259-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-211">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-212">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-213">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-214">Pengebilan pada aktual masa: <strong>Tidak Boleh DItuntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-215">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-216">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-217">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-218">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-219">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-220">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-221">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-222">
                    <strong>Boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-223">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-224">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-225">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-226">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-227">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-228">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-229">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-230">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-231">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-232">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-233">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-234">Pengebilan pada aktual masa: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-235">Jenis pengebilan pada aktual perbelanjaan: <strong> Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-236">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-237">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2b259-238">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-239">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-240">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-241">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-242">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-243">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-244">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-245">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-246">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-247">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="2b259-248">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="2b259-249">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-250">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-251">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-252">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-253">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-254">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-255">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-256">Jenis pengebilan pada aktual bahan: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-257">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-258">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2b259-259">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-260">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-261">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-262">Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-263">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-264">Pengebilan pada masa sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-265">Jenis pengebilan pada perbelanjaan sebenar: Boleh dituntut</span><span class="sxs-lookup"><span data-stu-id="2b259-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="2b259-266">Jenis pengebilan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="2b259-267">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="2b259-268">Ya</span><span class="sxs-lookup"><span data-stu-id="2b259-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="2b259-269">
                    <strong>Tidak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="2b259-270">Keseluruhan Projek</span><span class="sxs-lookup"><span data-stu-id="2b259-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2b259-271">
                    <strong>Tidak Boleh Dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="2b259-272">
                    <strong>Tidak boleh dituntut</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2b259-273">Tidak boleh ditetapkan</span><span class="sxs-lookup"><span data-stu-id="2b259-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="2b259-274">Pengebilan pada aktual masa: <strong>Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-275">Jenis pengebilan pada aktual perbelanjaan:<strong> Tidak boleh dituntut </strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="2b259-276">Jenis pengebilan pada aktual bahan:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2b259-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
