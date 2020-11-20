---
title: Sahkan invois proforma
description: Topik ini memberikan maklumat tentang mengesahkan invois proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128114"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="a0e50-103">Sahkan invois proforma</span><span class="sxs-lookup"><span data-stu-id="a0e50-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="a0e50-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="a0e50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a0e50-105">Selepas invois proforma disahkan, status invois projek dikemas kini kepada **Disahkan**.</span><span class="sxs-lookup"><span data-stu-id="a0e50-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="a0e50-106">Apabila invois disahkan, ia menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="a0e50-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="a0e50-107">Melangkah ke hadapan, invois hanya boleh diperbetulkan jika terdapat sebarang pembetulan atau kredit yang yang dimulakan oleh pelanggan, atau apabila invois tersebut ditanda sebagai berbayar.</span><span class="sxs-lookup"><span data-stu-id="a0e50-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="a0e50-108">Jadual berikut menyenaraikan aktual yang dicipta oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="a0e50-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="a0e50-109">Aktual ini dicipta apabila operasi tertentu dilaksanakan pada draf invois projek sebelum disahkan.</span><span class="sxs-lookup"><span data-stu-id="a0e50-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="a0e50-110">
                    <strong>Senario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a0e50-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="a0e50-111">
                    <strong>Aktual dicipta pada pengesahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a0e50-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a0e50-112">Menginvoiskan transaksi masa tanpa sebarang pengeditan pada invois draf.</span><span class="sxs-lookup"><span data-stu-id="a0e50-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-113">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="a0e50-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-114">Aktual jualan dibilkan untuk jam dan amaun pada kelulusan masa asal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a0e50-115">Menginvoiskan transaksi masa yang diedit untuk mengurangkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="a0e50-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-116">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="a0e50-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-117">Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-118">Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki jam dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a0e50-119">Menginvoiskan transaksi masa yang diedit untuk meningkatkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="a0e50-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-120">Pembalikan jualan belum dibilkan untuk jam dan amaun pada kelulusan masa sebenar.</span><span class="sxs-lookup"><span data-stu-id="a0e50-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-121">Aktual jualan belum dibilkan baharu boleh dituntut untuk jam dan amaun pada butiran baris invois yang diedit, pembalikan aktual jualan belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a0e50-122">Menginvoiskan transaksi perbelanjaan tanpa sebarang pengeditan pada invois draf.</span><span class="sxs-lookup"><span data-stu-id="a0e50-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-123">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-124">Aktual jualan dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a0e50-125">Menginvoiskan transaksi perbelanjaan yang diedit untuk mengurangkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="a0e50-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-126">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-127">Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-128">Aktual jualan belum dibilkan baharu yang tidak boleh dituntut untuk baki kuantiti dan amaun selepas mengurangkan angka yang dibetulkan pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibilkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a0e50-129">Menginvoiskan transaksi perbelanjaan yang diedit untuk meningkatkan kuantiti.</span><span class="sxs-lookup"><span data-stu-id="a0e50-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-130">Balikan jualan belum dibilkan bagi kuantiti dan amaun pada kelulusan perbelanjaan asal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-131">Aktual jualan belum dibilkan baharu boleh dituntut untuk kuantiti dan amaun pada butiran baris invois yang diedit, balikan aktual jualan yang belum dibillkan, dan aktual jualan dibilkan yang sama.</span><span class="sxs-lookup"><span data-stu-id="a0e50-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a0e50-132">Menginvoiskan bayaran.</span><span class="sxs-lookup"><span data-stu-id="a0e50-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-133">Pembalikan jualan belum dibilkan untuk amaun bayaran pada garisan jurnal.</span><span class="sxs-lookup"><span data-stu-id="a0e50-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-134">Aktual jualan dibilkan bagi kuantiti dan amaun pada garisan jurnal bayaran sebenar.</span><span class="sxs-lookup"><span data-stu-id="a0e50-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a0e50-135">Menginvoiskan pencapaian.</span><span class="sxs-lookup"><span data-stu-id="a0e50-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a0e50-136">Aktual jualan dibilkan untuk amaun pencapaian pada pencapaian asal pada baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="a0e50-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
