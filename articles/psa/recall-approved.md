---
title: Tarik balik entri masa atau perbelanjaan yang diluluskan
description: Topik ini memberikan maklumat tentang cara untuk menarik balik transaksi masa atau perbelanjaan yang diluluskan sebelumnya.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7bacd70881a6c463cc449a365173da5338a3d3fc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081275"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="447e3-103">Tarik balik entri masa atau perbelanjaan yang diluluskan</span><span class="sxs-lookup"><span data-stu-id="447e3-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="447e3-104">Ahli pasukan projek atau orang lain yang menyerahkan entri masa atau perbelanjaan boleh menarik balik entri masa atau perbelanjaan selepas ia telah diluluskan.</span><span class="sxs-lookup"><span data-stu-id="447e3-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="447e3-105">Proses untuk menarik balik entri masa atau perbelanjaan yang diluluskan mempunyai dua langkah:</span><span class="sxs-lookup"><span data-stu-id="447e3-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="447e3-106">Penyerah meminta tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="447e3-107">Pelulus meluluskan tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="447e3-108">Meminta tarik balik</span><span class="sxs-lookup"><span data-stu-id="447e3-108">Request a recall</span></span>

<span data-ttu-id="447e3-109">Ikut langkah ini untuk meminta tarik balik entri masa atau perbelanjaan yang diluluskan.</span><span class="sxs-lookup"><span data-stu-id="447e3-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="447e3-110">Untuk entri masa, pergi ke **Projek** \> **Kerja Saya** \> **Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="447e3-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="447e3-111">–atau–</span><span class="sxs-lookup"><span data-stu-id="447e3-111">–or–</span></span>

    <span data-ttu-id="447e3-112">Untuk entri perbelanjaan, pergi ke **Projek** \> **Kerja Saya** \> **Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="447e3-113">Untuk entri masa, pilih semua entri masa untuk gabungan projek dan tugas tertentu.</span><span class="sxs-lookup"><span data-stu-id="447e3-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="447e3-114">Secara alternatif, dalam grid, pilih sel individu untuk masa pada tarikh tertentu bagi projek tertentu.</span><span class="sxs-lookup"><span data-stu-id="447e3-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="447e3-115">–atau–</span><span class="sxs-lookup"><span data-stu-id="447e3-115">–or–</span></span>

    <span data-ttu-id="447e3-116">Untuk entri perbelanjaan, pilih baris bagi entri perbelanjaan untuk tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="447e3-117">Pilih **Tarik balik**.</span><span class="sxs-lookup"><span data-stu-id="447e3-117">Select **Recall**.</span></span> <span data-ttu-id="447e3-118">Kotak dialog pengesahan muncul.</span><span class="sxs-lookup"><span data-stu-id="447e3-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="447e3-119">Jika entri masa dan perbelanjaan yang dipilih sudah diluluskan, anda digesa untuk memasukkan sebab untuk tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="447e3-120">Masukkan sebab untuk tarik balik dan kemudian pilih **OK** untuk mengesahkan operasi.</span><span class="sxs-lookup"><span data-stu-id="447e3-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="447e3-121">Sistem menghantar kepada individu yang meluluskan entri tersebut permintaan untuk meluluskan tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="447e3-122">Walaupun entri masa dan perbelanjaan yang diluluskan boleh ditarik balik, jika masa atau perbelanjaan yang diluluskan telah pun diinvoiskan kepada pelanggan, permintaan tarik balik tidak boleh dicipta.</span><span class="sxs-lookup"><span data-stu-id="447e3-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="447e3-123">Pengguna yang cuba mencipta permintaan tarik balik akan menerima mesej yang menyatakan bahawa masa atau perbelanjaan tersebut tidak boleh ditarik balik kerana ia sudah diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="447e3-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="447e3-124">Luluskan atau tolak permintaan tarik balik</span><span class="sxs-lookup"><span data-stu-id="447e3-124">Approve or reject a recall request</span></span>

<span data-ttu-id="447e3-125">Ikuti langkah ini untuk meluluskan atau menolak permintaan tarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="447e3-126">Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="447e3-127">Pada halaman senarai **Kelulusan** , tukar pandangan kepada **Permintaan tarik balik untuk kelulusan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="447e3-128">Senarai permintaan tarik balik yang diserahkan ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="447e3-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="447e3-129">Pilih satu atau lebih entri dan kemudian pilih sama ada **Luluskan** atau **Tolak**.</span><span class="sxs-lookup"><span data-stu-id="447e3-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="447e3-130">Jika anda memilih **Luluskan** , anda menerima mesej amaran yang menerangkan tentang kesan kelulusan tersebut.</span><span class="sxs-lookup"><span data-stu-id="447e3-130">If you selected **Approve** , you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="447e3-131">Pilih **OK** untuk mengesahkan operasi.</span><span class="sxs-lookup"><span data-stu-id="447e3-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="447e3-132">Permintaan tarik balik diluluskan.</span><span class="sxs-lookup"><span data-stu-id="447e3-132">The recall request is approved.</span></span>

    <span data-ttu-id="447e3-133">–atau–</span><span class="sxs-lookup"><span data-stu-id="447e3-133">–or–</span></span>

    <span data-ttu-id="447e3-134">Jika anda memilih **Tolak** , permintaan tarik balik ditolak.</span><span class="sxs-lookup"><span data-stu-id="447e3-134">If you selected **Reject** , the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="447e3-135">Seperti apabila tarik balik diminta, apabila tarik balik diluluskan, sistem menyemak sebarang aktiviti penginvoisan pada entri masa atau perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="447e3-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="447e3-136">Jika entri telah pun diinvoiskan, atau jika ia berada pada invois draf, pelulus akan menerima mesej ralat yang menyatakan bahawa masa atau perbelanjaan tersebut tidak boleh diluluskan untuk tarik balik kerana ia sudah diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="447e3-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="447e3-137">Kesan daripada permintaan tarik balik</span><span class="sxs-lookup"><span data-stu-id="447e3-137">Impact of a recall request</span></span>

<span data-ttu-id="447e3-138">Apabila kelulusan ditarik balik, terdapat kesan operasi dan kesan kewangan.</span><span class="sxs-lookup"><span data-stu-id="447e3-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="447e3-139">Kesan operasi</span><span class="sxs-lookup"><span data-stu-id="447e3-139">Operational impact</span></span>

<span data-ttu-id="447e3-140">Jika permintaan tarik balik diluluskan, rekod kelulusan akan ditandakan sebagai **Ditolak.**</span><span class="sxs-lookup"><span data-stu-id="447e3-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="447e3-141">Status entri ditukar kepada sama ada **Dikembalikan** atau **Ditolak** , bergantung pada sama ada ia ialah entri masa atau entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="447e3-141">The status of the entry is changed to either **Returned** or **Rejected** , depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="447e3-142">Ahli pasukan projek boleh melihat entri, mengedit dan kemudian menghantar semula entri atau memadamkan entri sepenuhnya.</span><span class="sxs-lookup"><span data-stu-id="447e3-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="447e3-143">Jika permintaan tarik balik ditolak, status entri masih **Diluluskan** dan entri tersebut tidak boleh diedit oleh ahli pasukan projek atau pelulus bagi projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="447e3-143">If a recall request is rejected, the status of the entry remains **Approved** , and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="447e3-144">Kesan kewangan</span><span class="sxs-lookup"><span data-stu-id="447e3-144">Financial impact</span></span>

<span data-ttu-id="447e3-145">Jika permintaan tarik balik diluluskan, aktual yang berkaitan dengan kos dan jualan dikemas kini dengan cara berikut:</span><span class="sxs-lookup"><span data-stu-id="447e3-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="447e3-146">Medan **Status Pelarasan** dikemas kini kepada **Dilaraskan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="447e3-147">Medan **Status Pengebilan** dikemas kini kepada **Dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="447e3-148">Seterusnya, entri balikan dicipta dalam jadual Aktual.</span><span class="sxs-lookup"><span data-stu-id="447e3-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="447e3-149">Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar.</span><span class="sxs-lookup"><span data-stu-id="447e3-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="447e3-150">Satu-satunya nilai yang tidak disalin adalah nilai kuantiti.</span><span class="sxs-lookup"><span data-stu-id="447e3-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="447e3-151">Sebaliknya, nilai ini dibalikkan.</span><span class="sxs-lookup"><span data-stu-id="447e3-151">These values are reversed instead.</span></span> <span data-ttu-id="447e3-152">Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="447e3-153">Medan **Status Pelarasan** pada aktual yang diterbalikkan ditetapkan kepada **Tidak boleh diselaraskan** dan medan **Status pengebilan** ditetapkan kepada **Dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="447e3-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable** , and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="447e3-154">Disebabkan perubahan ini, perbelanjaan yang direkodkan dan tunggakan hasil pada projek tidak lagi menjelaskan jumlah yang diwakili oleh aktual ini.</span><span class="sxs-lookup"><span data-stu-id="447e3-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="447e3-155">Jika permintaan tarik balik ditolak, tiada kesan kewangan pada projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="447e3-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="447e3-156">Perubahan pada rekod entri masa</span><span class="sxs-lookup"><span data-stu-id="447e3-156">Changes to time entry records</span></span>

<span data-ttu-id="447e3-157">Ilustrasi berikut menunjukkan perubahan yang berlaku bagi entri masa yang diluluskan apabila ia ditarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Peralihan keadaan Entri Masa](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="447e3-159">Perubahan pada rekod entri perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="447e3-159">Changes to expense entry records</span></span>

<span data-ttu-id="447e3-160">Ilustrasi berikut menunjukkan perubahan yang berlaku bagi entri perbelanjaan yang diluluskan apabila ia ditarik balik.</span><span class="sxs-lookup"><span data-stu-id="447e3-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Peralihan keadaan Entri Perbelanjaan](media/ExpenseEntryStateTransitions.png)
