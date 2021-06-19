---
title: Gunakan perbelanjaan peribadi pada laporan perbelanjaan
description: Topik ini menyediakan maklumat tentang cara untuk menggunakan perbelanjaan peribadi yang ditanggung oleh pekerja semasa melakukan perjalanan bagi tujuan perniagaan.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025695"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="5021a-103">Gunakan perbelanjaan peribadi pada laporan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="5021a-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="5021a-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="5021a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5021a-105">Semasa perjalanan perniagaan, pekerja mungkin dikenakan caj perbelanjaan peribadi pada kad kredit korporat mereka.</span><span class="sxs-lookup"><span data-stu-id="5021a-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="5021a-106">Jika proses belum ditakrifkan untuk pengendalian perbelanjaan peribadi, proses kelulusan laporan perbelanjaan mungkin terganggu apabila pekerja menyerahkan laporan perbelanjaan butiran mereka.</span><span class="sxs-lookup"><span data-stu-id="5021a-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="5021a-107">Terdapat dua kaedah yang anda boleh gunakan untuk menggunakan perbelanjaan peribadi pekerja:</span><span class="sxs-lookup"><span data-stu-id="5021a-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="5021a-108">**Dibayar oleh pekerja**: Organisasi anda tidak membayar perbelanjaan peribadi yang tertera pada bil untuk kad kredit korporat.</span><span class="sxs-lookup"><span data-stu-id="5021a-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="5021a-109">Sebaliknya, pekerja membayar vendor kad kredit secara terus untuk perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="5021a-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="5021a-110">**Dibayar oleh syarikat**: Organisasi anda membayar bil penuh untuk kad kredit korporat, dan kemudian mendebitkan akaun pekerja untuk perbelanjaan peribadi.</span><span class="sxs-lookup"><span data-stu-id="5021a-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="5021a-111">Anda boleh memilih kaedah yang organisasi anda gunakan pada halaman **Parameter pengurusan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="5021a-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="5021a-112">Dayakan fungsi perbelanjaan pisah apabila medan jumlah peribadi mempunyai nilai ditakrifkan</span><span class="sxs-lookup"><span data-stu-id="5021a-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="5021a-113">Ciri ini, **Dayakan fungsi perbelanjaan pisah apabila medan jumlah peribadi mempunyai nilai ditakrifkan** hanya diguna pakai pada laporan perbelanjaan yang diluluskan menggunakan aliran kerja peringkat baris.</span><span class="sxs-lookup"><span data-stu-id="5021a-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="5021a-114">Laporan diluluskan dengan pergi ke **Laporan perbelanjaan proses** > **Laporan perbelanjaan ditugaskan kepada saya** > **Buka laporan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="5021a-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="5021a-115">Untuk mendayakan ciri ini, pergi ke **Ruang kerja** > **Pengurusan Ciri**, pilih **Dayakan fungsi perbelanjaan pisah apabila medan jumlah peribadi mempunyai nilai yang ditakrifkan** dan kemudian pilih **Dayakan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="5021a-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="5021a-116">Apabila ciri didayakan, baris perbelanjaan yang menggunakan fungsi ini menjana dua baris apabila laporan diserahkan.</span><span class="sxs-lookup"><span data-stu-id="5021a-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="5021a-117">Dua baris dijana supaya pelulus boleh meluluskan setiap baris secara berasingan.</span><span class="sxs-lookup"><span data-stu-id="5021a-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
