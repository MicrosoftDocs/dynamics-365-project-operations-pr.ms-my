---
title: Sahkan invois proforma - ringan
description: Topik ini menyediakan maklumat tentang mengesahkan invois proforma dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176532"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="0b624-103">Sahkan invois proforma - ringan</span><span class="sxs-lookup"><span data-stu-id="0b624-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="0b624-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="0b624-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0b624-105">Selepas invois proforma disahkan, status invois projek dikemas kini kepada **Disahkan**.</span><span class="sxs-lookup"><span data-stu-id="0b624-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="0b624-106">Apabila invois disahkan, ia menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="0b624-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="0b624-107">Melangkah ke hadapan, invois hanya boleh diperbetulkan jika terdapat sebarang pembetulan atau kredit yang yang dimulakan oleh pelanggan, jika invois tersebut ditanda sebagai berbayar.</span><span class="sxs-lookup"><span data-stu-id="0b624-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="0b624-108">Jadual berikut menyenaraikan aktual yang dicipta oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="0b624-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="0b624-109">Aktual ini dicipta apabila operasi tertentu dilaksanakan pada draf invois projek sebelum disahkan.</span><span class="sxs-lookup"><span data-stu-id="0b624-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0b624-110">
                    <strong>Senario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b624-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0b624-111">
                    <strong>Aktual dicipta pada pengesahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0b624-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-112">Menginvoiskan retainer atau pendahuluan</span><span class="sxs-lookup"><span data-stu-id="0b624-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-113">Aktual jualan dibilkan bagi jenis, <strong>Retainer</strong> dibuat untuk jumlah dalam pendahuluan atau retainer.</span><span class="sxs-lookup"><span data-stu-id="0b624-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-114">Aktual jualan dibilkan bagi amaun negatif untuk retainer atau pendahuluan yang akan digunakan untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="0b624-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-115">Selepas disesuaikan sepenuhnya retainer atau pendahuluan pada invois.</span><span class="sxs-lookup"><span data-stu-id="0b624-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-116">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="0b624-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0b624-117">Amaun ini adalah positif kerana ia bertujuan untuk membatalkan negatif yang dicipta apabila retainer atau pendahuluan diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="0b624-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-118">Aktual jualan dibilkan untuk amaun pada invois ini.</span><span class="sxs-lookup"><span data-stu-id="0b624-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0b624-119">Selepas disesuaikan separuh retainer atau pendahuluan pada invois.</span><span class="sxs-lookup"><span data-stu-id="0b624-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-120">Balikan jualan yang belum dibilkan daripada retainer atau pendahuluan yang dicipta untuk penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="0b624-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0b624-121">Amaun ini adalah positif kerana ia bertujuan untuk membatalkan negatif yang dicipta apabila retainer atau pendahuluan diinvoiskan.</span><span class="sxs-lookup"><span data-stu-id="0b624-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-122">Aktual jualan dibilkan untuk amaun pada invois ini.</span><span class="sxs-lookup"><span data-stu-id="0b624-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-123">Aktual jualan belum dibilkan negatif untuk baki amaun retainer atau pendahuluan akan digunakan untuk penyesuaian pada invois akan datang.</span><span class="sxs-lookup"><span data-stu-id="0b624-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-124">Menginvoiskan transaksi masa tanpa sebarang pengeditan pada invois draf.</span><span class="sxs-lookup"><span data-stu-id="0b624-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-125">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="0b624-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-126">Aktual jualan dibilkan untuk jam dan amaun pada kelulusan masa asal.</span><span class="sxs-lookup"><span data-stu-id="0b624-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0b624-127">Menginvoiskan transaksi masa yang diedit untuk mengurangkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="0b624-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-128">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="0b624-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-129">Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-130">Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki jam dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-131">Menginvoiskan transaksi masa yang diedit untuk meningkatkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="0b624-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-132">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="0b624-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-133">Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-134">Penginvoisan transaksi perbelanjaan tanpa sebarang pengeditan pada invois draf.</span><span class="sxs-lookup"><span data-stu-id="0b624-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-135">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="0b624-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-136">Aktual jualan dibilkan sebenar bagi kuantiti dan amaun pada kelulusan perbelanjaan asal</span><span class="sxs-lookup"><span data-stu-id="0b624-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0b624-137">Menginvoiskan transaksi perbelanjaan yang diedit untuk mengurangkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="0b624-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-138">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="0b624-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-139">Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-140">Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki kuantiti dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-141">Menginvoiskan transaksi perbelanjaan yang diedit untuk meningkatkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="0b624-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-142">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="0b624-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-143">Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="0b624-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0b624-144">Menginvoiskan bayaran.</span><span class="sxs-lookup"><span data-stu-id="0b624-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-145">Pembalikan jualan belum dibilkan untuk amaun bayaran pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="0b624-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-146">Aktual jualan dibilkan bagi kuantiti dan amaun pada garisan jurnal bayaran sebenar.</span><span class="sxs-lookup"><span data-stu-id="0b624-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0b624-147">Menginvoiskan pencapaian.</span><span class="sxs-lookup"><span data-stu-id="0b624-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-148">Aktual jualan dibilkan untuk amaun pencapaian pada pencapaian asal pada baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="0b624-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0b624-149">Penginvoisan baris kontrak berdasarkan produk.</span><span class="sxs-lookup"><span data-stu-id="0b624-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0b624-150">Aktual jualan dibilkan untuk baris produk dengan kuantiti dan amaun yang datang daripada baris kontrak berdasarkan produk.</span><span class="sxs-lookup"><span data-stu-id="0b624-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
