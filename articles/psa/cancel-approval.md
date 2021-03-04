---
title: Batalkan entri masa dan perbelanjaan yang diluluskan sebelumnya
description: Topik ini memberikan maklumat tentang cara membatalkan masa projek diluluskan dan transaksi perbelanjaan.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150589"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="b500b-103">Batalkan entri masa atau perbelanjaan yang diluluskan sebelumnya</span><span class="sxs-lookup"><span data-stu-id="b500b-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b500b-104">Dalam versi terkini Dynamics 365 Project Service Automation, pelulus boleh membatalkan entri masa atau perbelanjaan yang mereka luluskan sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="b500b-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="b500b-105">Batalkan entri masa atau perbelanjaan yang diluluskan sebelumnya</span><span class="sxs-lookup"><span data-stu-id="b500b-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="b500b-106">Ikuti langkah-langkah ini untuk membatalkan entri masa atau perbelanjaan yang anda luluskan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="b500b-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="b500b-107">Pergi ke **Projek** \> **Kerja Saya** \> **Kelulusan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="b500b-108">Pada halaman senarai **Kelulusan**, ubah pandangan kepada **Kelulusan lalu saya**.</span><span class="sxs-lookup"><span data-stu-id="b500b-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="b500b-109">Senarai entri masa dan perbelanjaan yang anda luluskan sebelum ini ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="b500b-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="b500b-110">Pilih satu atau lebih entri, kemudian pilih **Batalkan kelulusan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="b500b-111">Anda menerima satu mesej amaran.</span><span class="sxs-lookup"><span data-stu-id="b500b-111">You receive a warning message.</span></span>
4. <span data-ttu-id="b500b-112">Pilih **OK** untuk membatalkan kelulusan.</span><span class="sxs-lookup"><span data-stu-id="b500b-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="b500b-113">Fahami impak pembatalan kelulusan entri masa atau perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="b500b-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="b500b-114">Apabila kelulusan dibatalkan, terdapat impak operasi dan impak kewangan.</span><span class="sxs-lookup"><span data-stu-id="b500b-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="b500b-115">Impak operasi</span><span class="sxs-lookup"><span data-stu-id="b500b-115">Operational impact</span></span>

<span data-ttu-id="b500b-116">Pada bahagian operasi, apabila kelulusan dibatalkan, status rekod ditetapkan kepada **Draf**, dan kelulusan tidak lagi muncul dalam pandangan **Kelulusan lalu saya**.</span><span class="sxs-lookup"><span data-stu-id="b500b-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="b500b-117">Sebaliknya, kelulusan yang dibatalkan muncul dalam sama ada pandangan **Entri masa untuk kelulusan** atau pandangan **Entri perbelanjaan untuk kelulusan**, bergantung pada sama ada ia adalah entri masa atau entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="b500b-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="b500b-118">Selain itu, status entri masa atau perbelanjaan berkaitan diubah kepada **Diserahkan**, agar entri berkaitan konsisten dengan kelulusan yang mempunyai status **Draf**.</span><span class="sxs-lookup"><span data-stu-id="b500b-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="b500b-119">Sebagai pelulus, anda boleh mengedit beberapa medan kelulusan yang mempunyai status **Draf**.</span><span class="sxs-lookup"><span data-stu-id="b500b-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="b500b-120">Medan ini termasuk **Jenis Pengebilan** dan **Jam Boleh Dibilkan untuk Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="b500b-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="b500b-121">Selepas anda membuat perubahan, anda boleh meluluskan rekod semula.</span><span class="sxs-lookup"><span data-stu-id="b500b-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="b500b-122">Secara alternatif, anda boleh menolak entri.</span><span class="sxs-lookup"><span data-stu-id="b500b-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="b500b-123">Jika anda menolak kelulusan entri masa, status entri diubah kepada **Dipulangkan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="b500b-124">Jika anda menolak kelulusan entri perbelanjaan, status entri diubah kepada **Ditolak**.</span><span class="sxs-lookup"><span data-stu-id="b500b-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="b500b-125">Dari segi fungsi, entri yang dipulangkan dan ditolak bertindak sama seperti entri yang mempunyai status **Draf**.</span><span class="sxs-lookup"><span data-stu-id="b500b-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="b500b-126">Ahli pasukan projek boleh sama ada membuat sebarang perubahan yang diperlukan ke atas entri, dan kemudian menyerahkan semula untuk kelulusan, atau memadam entri secara keseluruhannya.</span><span class="sxs-lookup"><span data-stu-id="b500b-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="b500b-127">Impak kewangan</span><span class="sxs-lookup"><span data-stu-id="b500b-127">Financial impact</span></span>

<span data-ttu-id="b500b-128">Projek juga terjejas dari segi kewangan apabila kelulusan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="b500b-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="b500b-129">Pertama, aktual serupa untuk kos dan jualan dikemas kini dalam cara berikut:</span><span class="sxs-lookup"><span data-stu-id="b500b-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="b500b-130">Status pelarasan ditetapkan kepada **Dilaraskan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="b500b-131">Status pengebilan ditetapkan kepada **Dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="b500b-132">Seterusnya, entri balikan dicipta dalam jadual Aktual.</span><span class="sxs-lookup"><span data-stu-id="b500b-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="b500b-133">Untuk mencipta entri balikan, sistem menyalin nilai medan daripada aktual sebenar.</span><span class="sxs-lookup"><span data-stu-id="b500b-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="b500b-134">Satu-satunya nilai yang tidak disalin adalah nilai kuantiti.</span><span class="sxs-lookup"><span data-stu-id="b500b-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="b500b-135">Sebaliknya, nilai ini dibalikkan.</span><span class="sxs-lookup"><span data-stu-id="b500b-135">These values are reversed instead.</span></span> <span data-ttu-id="b500b-136">Aktual balikan dicipta untuk **Kos** dan aktual **Jualan Tidak Dibilkan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="b500b-137">Medan **Status Pelarasan** pada aktual balikan ditetapkan kepada **Tidak dilaraskan**, dan status pengebilan ditetapkan kepada **Dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="b500b-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="b500b-138">Selepas semua perubahan ini dibuat, amaun yang direkod sebagai dibelanja ke atas projek dan tunggakan hasil ke atas projek tidak lagi dikira untuk amaun yang diwakili aktual ini.</span><span class="sxs-lookup"><span data-stu-id="b500b-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
