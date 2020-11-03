---
title: Perbelanjaan antara syarikat
description: Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama. Dalam situasi ini, anda boleh menggunakan ciri perbelanjaan antara syarikat untuk menugaskan perbelanjaan pekerja kepada entiti sah yang dilaksanakan kerja oleh pekerja tersebut.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081379"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="e5861-104">Perbelanjaan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="e5861-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5861-105">Pekerja yang diupah oleh satu entiti sah dalam organisasi mungkin melaksanakan kerja untuk entiti sah yang lain dalam organisasi yang sama.</span><span class="sxs-lookup"><span data-stu-id="e5861-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="e5861-106">Dalam situasi ini, anda boleh menggunakan ciri perbelanjaan antara syarikat untuk menugaskan perbelanjaan pekerja kepada entiti sah yang dilaksanakan kerja oleh pekerja tersebut.</span><span class="sxs-lookup"><span data-stu-id="e5861-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="e5861-107">Entiti sah yang mengupah pekerja dipanggil sebagai entiti sah peminjaman.</span><span class="sxs-lookup"><span data-stu-id="e5861-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="e5861-108">Entiti sah yang pekerja menanggung perbelanjaan dipanggil entiti sah pinjaman.</span><span class="sxs-lookup"><span data-stu-id="e5861-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="e5861-109">Sebelum pekerja boleh mencipta dan menyerahkan perbelanjaan untuk kerja dilaksanakan untuk entiti sah yang berbeza, dalam entiti sah peminjaman, pada halaman **Parameter pengurusan perbelanjaan** , pilih pilihan **Benarkan baris perbelanjaan antara syarikat**.</span><span class="sxs-lookup"><span data-stu-id="e5861-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="e5861-110">Penyiaran cukai untuk perbelanjaan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="e5861-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5861-111">Jika anda mahu menggunakan kumpulan cukai yang dikaitkan dengan entiti sah peminjaman (sumber) dan bukannya entiti sah pinjaman (destinasi) dalam laporan perbelanjaan anda, anda akan perlu mengkonfigurasikan ciri ini dalam persediaan cukai jualan Lejar am.</span><span class="sxs-lookup"><span data-stu-id="e5861-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="e5861-112">Apabila parameter Lejar am, **Entiti sah untuk penyiaran cukai antara syarikat** ditetapkan kepada **Sumber** dan **Gunakan peraturan pencukaian cukai jualan** ditetapkan kepada **Tidak** , gabungan cukai untuk entiti sah peminjaman akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="e5861-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="e5861-113">Apabila parameter yang sama ditetapkan kepada **Destinasi** , gabungan cukai untuk entiti sah pinjaman akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="e5861-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="e5861-114">Untuk entiti sah di Amerika Syarikat, apabila parameter ditetapkan kepada **Sumber** , medan **Cukai jualan boleh diterima** juga mesti dikonfigurasikan pada halaman  **Kumpulan penyiaran lejar**.</span><span class="sxs-lookup"><span data-stu-id="e5861-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="e5861-115">Enjin perakaunan akan menggunakan maklumat daripada medan ini untuk entri perakaunan berkaitan cukai.</span><span class="sxs-lookup"><span data-stu-id="e5861-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="e5861-116">Tingkah laku ini konsisten untuk baris perbelanjaan yang disiarkan dengan atau tanpa projek.</span><span class="sxs-lookup"><span data-stu-id="e5861-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
