---
title: Cipta invois berdasarkan projek pembetulan
description: Topik ini menyediakan maklumat tentang invois pembetulan dalam Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001634"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="61ad2-103">Cipta invois berdasarkan projek pembetulan</span><span class="sxs-lookup"><span data-stu-id="61ad2-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="61ad2-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="61ad2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="61ad2-105">Invois projek yang disahkan boleh dibetulkan untuk memproses perubahan atau kredit seperti yang dirundingkan dengan pelanggan dan pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="61ad2-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="61ad2-106">Untuk mengedit invois yang disahkan, buka invois yang disahkan dan pilih **Betulkan Invois ini**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="61ad2-107">Pemilihan ini tidak tersedia kecuali invois projek disahkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="61ad2-108">Invois draf baharu dicipta daripada invois yang disahkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="61ad2-109">Semua butiran baris invois daripada invois yang disahkan sebelum ini disalin ke draf baharu.</span><span class="sxs-lookup"><span data-stu-id="61ad2-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="61ad2-110">Berikut ialah beberapa isi utama untuk membantu anda memahami lebih lanjut tentang butiran baris pada invois baharu yang dibetulkan:</span><span class="sxs-lookup"><span data-stu-id="61ad2-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="61ad2-111">Semua kuantiti dikemas kini ke sifar.</span><span class="sxs-lookup"><span data-stu-id="61ad2-111">All quantities are updated to zero.</span></span> <span data-ttu-id="61ad2-112">Ini menganggap bahawa semua item yang diinvois akan dikreditkan sepenuhnya.</span><span class="sxs-lookup"><span data-stu-id="61ad2-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="61ad2-113">Jika perlu, anda boleh mengemas kini kuantiti ini secara manual untuk menunjukkan kuantiti yang diinvois dan bukan kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="61ad2-114">Berdasarkan pada kuantiti yang anda masukkan, aplikasi mengira kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="61ad2-115">Amaun ini ditunjukkan dalam aktual yang dicipta apabila invois dibetulkan disahkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="61ad2-116">Jika anda membuat perubahan pada amaun cukai, anda mesti memasukkan jumlah cukai yang betul dan bukan jumlah cukai yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="61ad2-117">Pembetulan pencapaian sentiasa diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="61ad2-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="61ad2-118">Amaun retainer atau pendahuluan boleh dibetulkan jika pelanggan telah diinvoiskan dengan jumlah yang salah.</span><span class="sxs-lookup"><span data-stu-id="61ad2-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="61ad2-119">Penyesuaian retainer dan pendahuluan boleh dibetulkan jika amaun yang salah digunakan untuk menyesuaikan terhadap caj ke atas invois yang disahkan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="61ad2-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61ad2-120">Butiran baris invois yang merupakan pembetulan kepada caj lain yang sudah diinvois mempunyai medan **Pembetulan** yang ditetapkan pada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="61ad2-121">Invois yang mempunyai butiran baris invois dibetulkan mempunyai medan yang dipanggil **Mempunyai pembetulan** yang juga ditetapkan ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="61ad2-122">Aktual yang dicipta pada pengesahan invois pembetulan</span><span class="sxs-lookup"><span data-stu-id="61ad2-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="61ad2-123">Jadual berikut menyenaraikan aktual yang dicipta apabila invois pembetulan disahkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="61ad2-124">
                    <strong>Senario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="61ad2-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="61ad2-125">
                    <strong>Aktual dicipta pada pengesahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="61ad2-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="61ad2-126">Sahkan pembetulan pendahuluan atau retainer diinvois.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="61ad2-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-127">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="61ad2-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="61ad2-128">Amaun ini adalah positif kerana ia bertujuan untuk membatalkan negatif yang dicipta apabila retainer atau pendahuluan diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-129">Aktual pembalikan jualan dibilkan dicipta untuk amaun pada retainer atau pendahuluan bagi membalikkan jualan dibilkan yang asal.</span><span class="sxs-lookup"><span data-stu-id="61ad2-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-130">Aktual jualan dibilkan baharu dicipta untuk amaun dibetulkan pada retainer atau baris invois dibetulkan berasaskan pendahuluan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-131">Aktual jualan dibilkan bagi amaun negatif retainer atau baris invois dibetulkan berasaskan pendahuluan yang akan digunakan untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="61ad2-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="61ad2-132">Pengesahan pembetulan retainer atau pendahuluan sebelum ini yang disesuaikan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-133">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="61ad2-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="61ad2-134">Amaun adalah positif dan bertujuan untuk membatalkan negatif yang dicipta apabila penyesuaian sebelum ini berlaku.</span><span class="sxs-lookup"><span data-stu-id="61ad2-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-135">Aktual pembalikan jualan dibilkan untuk amaun pada invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-136">Aktual jualan dibilkan baharu dicipta untuk amaun retainer dibetulkan yang digunakan pada invois dibetulkan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-137">Aktual jualan dibilkan dengan amaun negatif daripada retainer atau pendahuluan sisa dibetulkan yang akan digunakan untuk penyesuaian dalam invois kemudian.</span><span class="sxs-lookup"><span data-stu-id="61ad2-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="61ad2-138">Penginvoisan kredit penuh bagi transaksi masa invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-139">Pembalikan jualan dibilkan untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="61ad2-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-140">Aktual jualan dibilkan baharu untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="61ad2-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="61ad2-141">Penginvoisan kredit separa pada transaksi masa.</span><span class="sxs-lookup"><span data-stu-id="61ad2-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-142">Pembalikan jualan dibilkan untuk jam dan amaun diinvoiskan pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="61ad2-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-143">Aktual jualan belum dibilkan baharu boleh dicaj untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="61ad2-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-144">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki jam dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="61ad2-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="61ad2-145">Penginvoisan kredit penuh bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-146">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-147">Aktual jualan dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="61ad2-148">Penginvoisan kredit separa bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-149">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="61ad2-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-150">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois yang dibetulkan, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="61ad2-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-151">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="61ad2-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="61ad2-152">Penginvoisan kredit penuh bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-153">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="61ad2-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-154">Aktual jualan belum dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="61ad2-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="61ad2-155">Penginvoisan kredit separa bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-156">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="61ad2-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-157">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois pembetulan diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="61ad2-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="61ad2-158">Penginvoisan kredit penuh bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-159">Pembalikan jualan dibilkan untuk amaun pada butiran baris invois asal untuk pencapaian.</span><span class="sxs-lookup"><span data-stu-id="61ad2-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="61ad2-160">Status invois pada pencapaian dikemas kini daripada <b>Invois pelanggan yang disiarkan</b> kepada <b>Sedia untuk Diinvois</b>.</span><span class="sxs-lookup"><span data-stu-id="61ad2-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="61ad2-161">Penginvoisan kredit separa bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="61ad2-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="61ad2-162">Tidak Disokong</span><span class="sxs-lookup"><span data-stu-id="61ad2-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
