---
title: Perbelanjaan antara syarikat
description: Topik ini menyediakan maklumat tentang cara untuk menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960843"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c751a-103">Perbelanjaan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="c751a-103">Intercompany expenses</span></span>

<span data-ttu-id="c751a-104">Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama.</span><span class="sxs-lookup"><span data-stu-id="c751a-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c751a-105">Anda boleh menggunakan perbelanjaan antara syarikat untuk menguntukkan perbelanjaan pekerja kepada entiti undang-undang yang mana kerja tersebut dilaksanakan.</span><span class="sxs-lookup"><span data-stu-id="c751a-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="c751a-106">Entiti sah yang mengupah pekerja dipanggil sebagai entiti sah peminjaman.</span><span class="sxs-lookup"><span data-stu-id="c751a-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c751a-107">Entiti sah yang pekerja menanggung perbelanjaan dipanggil entiti sah pinjaman.</span><span class="sxs-lookup"><span data-stu-id="c751a-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c751a-108">Sebelum pekerja boleh mencipta dan menyerahkan perbelanjaan antara syarikat, anda mestilah mendayakan baris perbelanjaan antara syarikat.</span><span class="sxs-lookup"><span data-stu-id="c751a-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="c751a-109">Dalam entiti undang-undang peminjaman, pada halaman **Parameter pengurusan perbelanjaan**, pilih **Benarkan baris perbelanjaan antara syarikat**.</span><span class="sxs-lookup"><span data-stu-id="c751a-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c751a-110">Penyiaran cukai untuk perbelanjaan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="c751a-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c751a-111">Sebelum anda boleh menggunakan kumpulan cukai yang dikaitkan dengan entiti undang-undang (sumber) peminjaman dan bukannya entiti undang-undang (destinasi) pinjaman dalam laporan perbelanjaan anda, anda mestilah mendayakan kefungsian dalam persediaan cukai jualan lejar Am.</span><span class="sxs-lookup"><span data-stu-id="c751a-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="c751a-112">Apabila parameter **Entiti undang-undang untuk penyiaran cukai antara syarikat** ditetapkan kepada **Sumber** dan **Gunakan peraturan pencukaian cukai jualan** ditetapkan kepada **Tidak**, gabungan cukai untuk entiti undang-undang peminjaman digunakan.</span><span class="sxs-lookup"><span data-stu-id="c751a-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="c751a-113">Apabila parameter yang sama ditetapkan kepada **Destinasi**, gabungan cukai untuk entiti sah pinjaman akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="c751a-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c751a-114">Untuk entiti sah di Amerika Syarikat, apabila parameter ditetapkan kepada **Sumber**, medan **Cukai jualan boleh diterima** juga mesti dikonfigurasikan pada halaman  **Kumpulan penyiaran lejar**.</span><span class="sxs-lookup"><span data-stu-id="c751a-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c751a-115">Enjin perakaunan akan menggunakan maklumat daripada medan ini untuk entri perakaunan berkaitan cukai.</span><span class="sxs-lookup"><span data-stu-id="c751a-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="c751a-116">Tingkah laku ini konsisten untuk baris perbelanjaan yang disiarkan dengan atau tanpa projek.</span><span class="sxs-lookup"><span data-stu-id="c751a-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
