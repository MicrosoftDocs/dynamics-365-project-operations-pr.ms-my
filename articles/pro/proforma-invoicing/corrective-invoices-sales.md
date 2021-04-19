---
title: Invois projek pembetulan
description: Topik ini menyediakan maklumat tentang cara mencipta dan mengesahkan invois pembetulan dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866602"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="36d94-103">Invois projek pembetulan</span><span class="sxs-lookup"><span data-stu-id="36d94-103">Corrective project invoices</span></span>

<span data-ttu-id="36d94-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="36d94-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36d94-105">Invois projek yang disahkan boleh dibetulkan untuk memproses perubahan atau kredit seperti yang dirundingkan dengan pelanggan dan pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="36d94-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="36d94-106">Untuk mengedit invois yang disahkan, buka invois yang disahkan dan pilih **Betulkan Invois ini**.</span><span class="sxs-lookup"><span data-stu-id="36d94-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="36d94-107">Pemilihan ini tidak tersedia kecuali invois projek disahkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="36d94-108">Invois draf baharu dicipta daripada invois yang disahkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="36d94-109">Semua butiran baris invois daripada invois yang disahkan sebelum ini disalin ke draf baharu.</span><span class="sxs-lookup"><span data-stu-id="36d94-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="36d94-110">Berikut ialah beberapa perkara utama untuk memahami tentang butiran baris pada invois dibetulkan yang baharu:</span><span class="sxs-lookup"><span data-stu-id="36d94-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="36d94-111">Semua kuantiti dikemas kini ke sifar.</span><span class="sxs-lookup"><span data-stu-id="36d94-111">All quantities are updated to zero.</span></span> <span data-ttu-id="36d94-112">Aplikasi ini menganggap semua item diinvois dikreditkan sepenuhnya.</span><span class="sxs-lookup"><span data-stu-id="36d94-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="36d94-113">Jika perlu, anda boleh mengemas kini kuantiti ini secara manual untuk menunjukkan kuantiti yang diinvois dan bukan kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="36d94-114">Berdasarkan pada kuantiti yang anda masukkan, aplikasi mengira kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="36d94-115">Amaun ini ditunjukkan dalam aktual yang dicipta apabila invois dibetulkan disahkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="36d94-116">Jika anda membuat perubahan pada amaun cukai, anda mesti memasukkan jumlah cukai yang betul dan bukan jumlah cukai yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="36d94-117">Baris kontrak berasaskan produk yang disahkan sebelum ini tidak disalin.</span><span class="sxs-lookup"><span data-stu-id="36d94-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="36d94-118">Memproses pembetulan pada invois projek berasaskan produk tidak disokong.</span><span class="sxs-lookup"><span data-stu-id="36d94-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="36d94-119">Pembetulan pencapaian sentiasa diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="36d94-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="36d94-120">Amaun retainer atau pendahuluan boleh dibetulkan jika pelanggan telah diinvoiskan dengan jumlah yang salah.</span><span class="sxs-lookup"><span data-stu-id="36d94-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="36d94-121">Penyesuaian retainer dan pendahuluan boleh dibetulkan jika amaun yang salah digunakan untuk menyesuaikan terhadap caj ke atas invois yang disahkan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="36d94-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36d94-122">Butiran baris invois yang merupakan pembetulan kepada caj diinvois yang lain mempunyai medan **Pembetulan** ditetapkan ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="36d94-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="36d94-123">Invois yang mempunyai butiran baris invois dibetulkan mempunyai medan yang dipanggil **Mempunyai pembetulan** yang juga ditetapkan ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="36d94-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="36d94-124">Aktual dicipta apabila invois pembetulan disahkan</span><span class="sxs-lookup"><span data-stu-id="36d94-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="36d94-125">Jadual berikut menyenaraikan aktual yang dicipta apabila invois pembetulan disahkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="36d94-126">
                    <strong>Senario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36d94-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="36d94-127">
                    <strong>Aktual dicipta pada pengesahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="36d94-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="36d94-128">Sahkan pembetulan pendahuluan atau retainer diinvois.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="36d94-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-129">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="36d94-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="36d94-130">Amaun ini adalah positif kerana ia bertujuan untuk membatalkan negatif yang dicipta apabila retainer atau pendahuluan diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="36d94-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-131">Aktual pembalikan jualan dibilkan dicipta untuk amaun pada retainer atau pendahuluan bagi membalikkan jualan dibilkan yang asal.</span><span class="sxs-lookup"><span data-stu-id="36d94-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-132">Aktual jualan dibilkan baharu dicipta untuk amaun dibetulkan pada retainer atau baris invois dibetulkan berasaskan pendahuluan.</span><span class="sxs-lookup"><span data-stu-id="36d94-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-133">Aktual jualan dibilkan bagi amaun negatif retainer atau baris invois dibetulkan berasaskan pendahuluan yang akan digunakan untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="36d94-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="36d94-134">Pengesahan pembetulan retainer atau pendahuluan sebelum ini yang disesuaikan.</span><span class="sxs-lookup"><span data-stu-id="36d94-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-135">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="36d94-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="36d94-136">Amaun adalah positif dan bertujuan untuk membatalkan negatif yang dicipta apabila penyesuaian sebelum ini berlaku.</span><span class="sxs-lookup"><span data-stu-id="36d94-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-137">Aktual pembalikan jualan dibilkan untuk amaun pada invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-138">Aktual jualan dibilkan baharu dicipta untuk amaun retainer dibetulkan yang digunakan pada invois dibetulkan.</span><span class="sxs-lookup"><span data-stu-id="36d94-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-139">Aktual jualan dibilkan dengan amaun negatif daripada retainer atau pendahuluan sisa dibetulkan yang akan digunakan untuk penyesuaian dalam invois kemudian.</span><span class="sxs-lookup"><span data-stu-id="36d94-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36d94-140">Penginvoisan kredit penuh bagi transaksi masa invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-141">Pembalikan jualan dibilkan untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="36d94-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-142">Aktual jualan dibilkan baharu untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="36d94-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="36d94-143">Penginvoisan kredit separa pada transaksi masa.</span><span class="sxs-lookup"><span data-stu-id="36d94-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-144">Pembalikan jualan dibilkan untuk jam dan amaun diinvoiskan pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="36d94-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-145">Aktual jualan belum dibilkan baharu boleh dicaj untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="36d94-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-146">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki jam dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="36d94-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36d94-147">Penginvoisan kredit penuh bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-148">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="36d94-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-149">Aktual jualan dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="36d94-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="36d94-150">Penginvoisan kredit separa bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-151">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="36d94-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-152">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois yang dibetulkan, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="36d94-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-153">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="36d94-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36d94-154">Penginvoisan kredit penuh transaksi bahan invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-155">Pembalikan jualan dibilkan untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="36d94-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-156">Aktual jualan belum dibilkan baharu untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="36d94-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="36d94-157">Penginvoisan kredit separa pada transaksi bahan.</span><span class="sxs-lookup"><span data-stu-id="36d94-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-158">Pembalikan jualan dibilkan untuk kuantiti dan jumlah yang diinvois pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="36d94-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-159">Aktual jualan baharu belum dibilkan baharu yang boleh dicaj untuk kuantiti dan jumlah pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang setara.</span><span class="sxs-lookup"><span data-stu-id="36d94-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-160">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="36d94-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36d94-161">Penginvoisan kredit penuh bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-162">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="36d94-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-163">Aktual jualan belum dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="36d94-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="36d94-164">Penginvoisan kredit separa bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-165">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="36d94-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-166">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois pembetulan diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="36d94-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="36d94-167">Penginvoisan kredit penuh bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-168">Pembalikan jualan dibilkan untuk amaun pada butiran baris invois asal untuk pencapaian.</span><span class="sxs-lookup"><span data-stu-id="36d94-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="36d94-169">Status invois pada pencapaian dikemas kini daripada <b>Invois Pelanggan yang Disiarkan</b> kepada <b>Sedia untuk Diinvois</b>.</span><span class="sxs-lookup"><span data-stu-id="36d94-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="36d94-170">Penginvoisan kredit separa bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-171">Tidak Disokong</span><span class="sxs-lookup"><span data-stu-id="36d94-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="36d94-172">Kredit dan pembetulan bagi baris kontrak berasaskan produk diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="36d94-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="36d94-173">Tidak Disokong</span><span class="sxs-lookup"><span data-stu-id="36d94-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
