---
title: Pembetulan invois berdasarkan projek
description: Topik ini menyediakan maklumat tentang cara mencipta dan mengesahkan pembetulan invois berdasarkan projek dalam Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012282"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="813fd-103">Pembetulan invois berdasarkan projek</span><span class="sxs-lookup"><span data-stu-id="813fd-103">Corrective project-based invoices</span></span>

<span data-ttu-id="813fd-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="813fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="813fd-105">Invois projek yang disahkan boleh dibetulkan untuk memproses perubahan atau kredit seperti yang dirundingkan dengan pelanggan dan pengurus projek.</span><span class="sxs-lookup"><span data-stu-id="813fd-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="813fd-106">Untuk mengedit invois yang disahkan, buka invois yang disahkan dan pilih **Betulkan Invois ini**.</span><span class="sxs-lookup"><span data-stu-id="813fd-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="813fd-107">Pemilihan ini tidak tersedia melainkan invois projek disahkan atau invois berdasarkan projek mempunyai pendahuluan atau retainer atau penyesuaian pendahuluan atau retainer.</span><span class="sxs-lookup"><span data-stu-id="813fd-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="813fd-108">Invois draf baharu dicipta daripada invois yang disahkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="813fd-109">Semua butiran baris invois daripada invois yang disahkan sebelum ini disalin ke draf baharu.</span><span class="sxs-lookup"><span data-stu-id="813fd-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="813fd-110">Berikut ialah beberapa perkara utama untuk memahami tentang butiran baris pada invois dibetulkan yang baharu:</span><span class="sxs-lookup"><span data-stu-id="813fd-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="813fd-111">Semua kuantiti dikemas kini ke sifar.</span><span class="sxs-lookup"><span data-stu-id="813fd-111">All quantities are updated to zero.</span></span> <span data-ttu-id="813fd-112">Dynamics 365 Project Operations menganggap bahawa semua item yang diinvois akan dikreditkan sepenuhnya.</span><span class="sxs-lookup"><span data-stu-id="813fd-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="813fd-113">Jika perlu, anda boleh mengemas kini kuantiti ini secara manual untuk menunjukkan kuantiti yang diinvois dan bukan kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="813fd-114">Berdasarkan pada kuantiti yang anda masukkan, aplikasi mengira kuantiti yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="813fd-115">Amaun ini ditunjukkan dalam aktual yang dicipta apabila invois dibetulkan disahkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="813fd-116">Jika anda membuat perubahan pada amaun cukai, anda mesti memasukkan jumlah cukai yang betul dan bukan jumlah cukai yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="813fd-117">Pembetulan pencapaian sentiasa diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="813fd-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="813fd-118">Untuk butiran baris invois yang merupakan pembetulan kepada caj lain yang sudah diinvois, medan **Pembetulan** ditetapkan pada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="813fd-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="813fd-119">Untuk invois yang mempunyai butiran baris invois yang dibetulkan, medan **Memunyai pembetulan** ditetapkan pada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="813fd-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="813fd-120">Aktual dicipta apabila invois pembetulan disahkan</span><span class="sxs-lookup"><span data-stu-id="813fd-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="813fd-121">Jadual berikut menyenaraikan aktual yang dicipta apabila invois pembetulan disahkan.</span><span class="sxs-lookup"><span data-stu-id="813fd-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="813fd-122">
                    <strong>Senario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="813fd-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="813fd-123">
                    <strong>Aktual dicipta pada pengesahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="813fd-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="813fd-124">Penginvoisan kredit penuh bagi transaksi masa invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-125">Pembalikan jualan dibilkan untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="813fd-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-126">Aktual jualan dibilkan baharu untuk jam dan amaun pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="813fd-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="813fd-127">Penginvoisan kredit separa pada transaksi masa.</span><span class="sxs-lookup"><span data-stu-id="813fd-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-128">Pembalikan jualan dibilkan untuk jam dan amaun diinvoiskan pada butiran baris invois asal untuk masa.</span><span class="sxs-lookup"><span data-stu-id="813fd-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-129">Aktual jualan belum dibilkan baharu boleh dicaj untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="813fd-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-130">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki jam dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="813fd-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="813fd-131">Penginvoisan kredit penuh bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-132">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="813fd-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-133">Aktual jualan dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="813fd-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="813fd-134">Penginvoisan kredit separa bagi transaksi perbelanjaan diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-135">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="813fd-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-136">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois yang dibetulkan, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="813fd-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-137">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="813fd-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="813fd-138">Penginvoisan kredit penuh transaksi bahan invois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-139">Pembalikan jualan dibilkan untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="813fd-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-140">Aktual jualan belum dibilkan baharu untuk kuantiti dan jumlah pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="813fd-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="813fd-141">Penginvoisan kredit separa pada transaksi bahan.</span><span class="sxs-lookup"><span data-stu-id="813fd-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-142">Pembalikan jualan dibilkan untuk kuantiti dan jumlah yang diinvois pada butiran baris invois asal untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="813fd-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-143">Aktual jualan baharu belum dibilkan baharu yang boleh dicaj untuk kuantiti dan jumlah pada butiran baris invois yang diedit, pembalikan ini dan aktual jualan dibilkan yang setara.</span><span class="sxs-lookup"><span data-stu-id="813fd-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-144">Aktual jualan belum dibilkan baharu boleh dicaj untuk baki kuantiti dan amaun selepas menolak angka dibetulkan pada butiran baris invois.</span><span class="sxs-lookup"><span data-stu-id="813fd-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="813fd-145">Penginvoisan kredit penuh bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-146">Pembalikan jualan dibilkan untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="813fd-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-147">Aktual jualan belum dibilkan baharu untuk kuantiti dan amaun pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="813fd-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="813fd-148">Penginvoisan kredit separa bagi transaksi yuran diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-149">Pembalikan jualan dibilkan untuk kuantiti dan amaun diinvoiskan pada butiran baris invois asal untuk yuran.</span><span class="sxs-lookup"><span data-stu-id="813fd-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-150">Aktual jualan belum dibilkan baharu boleh dicaj untuk kuantiti dan amaun pada butiran baris invois pembetulan diedit, pembalikan ini dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="813fd-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="813fd-151">Penginvoisan kredit penuh bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-152">Pembalikan jualan dibilkan untuk amaun pada butiran baris invois asal untuk pencapaian.</span><span class="sxs-lookup"><span data-stu-id="813fd-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="813fd-153">Status invois pada pencapaian dikemas kini daripada <b>Invois Pelanggan yang Disiarkan</b> kepada <b>Sedia untuk Diinvois</b>.</span><span class="sxs-lookup"><span data-stu-id="813fd-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="813fd-154">Penginvoisan kredit separa bagi pencapaian diinvois sebelum ini.</span><span class="sxs-lookup"><span data-stu-id="813fd-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="813fd-155">Senario ini tidak disokong.</span><span class="sxs-lookup"><span data-stu-id="813fd-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
