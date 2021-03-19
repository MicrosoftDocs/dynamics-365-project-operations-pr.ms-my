---
title: Konfigurasikan pengurusan perbelanjaan
description: Artikel ini menerangkan pertimbangan dan keputusan yang anda mesti lakukan semasa proses perancangan sebelum anda mengkonfigurasi Pengurusan perbelanjaan dalam Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271364"
---
# <a name="configure-expense-management"></a><span data-ttu-id="96afa-103">Konfigurasikan pengurusan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="96afa-103">Configure expense management</span></span>

<span data-ttu-id="96afa-104">Topik ini menerangkan pertimbangan dan keputusan yang anda mesti lakukan semasa proses perancangan sebelum anda mengkonfigurasi Pengurusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="96afa-105">Dalam Pengurusan perbelanjaan, anda boleh menyimpan maklumat tentang kaedah pembayaran, permintaan perjalanan, laporan perbelanjaan, dasar, dan sebagainya.</span><span class="sxs-lookup"><span data-stu-id="96afa-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="96afa-106">Disebabkan oleh kebanyakan keputusan yang anda lakukan apabila anda merancang konfigurasi anda untuk Pengurusan perbelanjaan adalah berdasarkan hierarki dan struktur kewangan organisasi anda, anda mesti merujuk kepada dokumen perancangan untuk kawasan tersebut.</span><span class="sxs-lookup"><span data-stu-id="96afa-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="96afa-107">Perbelanjaan antara syarikat</span><span class="sxs-lookup"><span data-stu-id="96afa-107">Intercompany expenses</span></span>

<span data-ttu-id="96afa-108">Apabila anda mendayakan perbelanjaan antara syarikat, anda membenarkan entiti sah dan pekerja untuk menanggung perbelanjaan bagi pihak entiti sah yang lain, dan mengumpulkan pembayaran daripada entiti sah pekerjaan dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="96afa-109">Contohnya, pekerja dalam entiti sah A melengkapkan projek untuk entiti sah B, dan projek itu menanggung perbelanjaan berkaitan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="96afa-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="96afa-110">Jika perbelanjaan antara syarikat didayakan, pekerja tersebut boleh memfailkan laporan perbelanjaan yang akan menyiarkan perbelanjaan ke entiti sah B, dan perbelanjaan tersebut mesti dibayar oleh entiti sah A. Jika organisasi anda tidak mempunyai berbilang entiti sah, anda tidak perlu mendayakan perbelanjaan antara syarikat.</span><span class="sxs-lookup"><span data-stu-id="96afa-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="96afa-111">**Keputusan:** Adakah anda mahu mendayakan perbelanjaan antara syarikat?</span><span class="sxs-lookup"><span data-stu-id="96afa-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="96afa-112">Pengurusan kewangan</span><span class="sxs-lookup"><span data-stu-id="96afa-112">Financial management</span></span>

<span data-ttu-id="96afa-113">Pengurusan perbelanjaan diintegrasikan kemas dengan pengurusan kewangan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="96afa-114">Banyak konfigurasi anda untuk Pengurusan perbelanjaan akan berdasarkan pada keputusan yang telah anda lakukan tentang kewangan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="96afa-115">Bahagian berikut menerangkan pelbagai bidang yang memerlukan perancangan dan keputusan, berdasarkan keputusan kewangan organisasi anda dan panduan daripada pasukan kepimpinan anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="96afa-116">Harian</span><span class="sxs-lookup"><span data-stu-id="96afa-116">Per diems</span></span>

<span data-ttu-id="96afa-117">Anda mesti mentakrifkan pekerja bagi sehari yang organisasi anda sediakan.</span><span class="sxs-lookup"><span data-stu-id="96afa-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="96afa-118">Oleh kerana bagi sehari biasanya digunakan untuk menampung perbelanjaan seperti makanan, penginapan, dan perbelanjaan sampingan yang lain, anda boleh mencipta peraturan untuk elaun bagi sehari yang ditawarkan oleh organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="96afa-119">kadar bagi sehari boleh didasarkan pada masa dalam tahun, lokasi perjalanan, atau kedua-duanya.</span><span class="sxs-lookup"><span data-stu-id="96afa-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="96afa-120">Apabila anda menakrif peraturan bagi sehari, anda boleh menentukan bahawa peratusan kadar bagi sehari akan ditahan jika pekerja menerima hidangan atau perkhidmatan percuma.</span><span class="sxs-lookup"><span data-stu-id="96afa-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="96afa-121">Anda juga boleh menakrif tahap kadar bagi sehari untuk menetapkan bilangan jam minimum dan maksimum yang kadar bagi sehari boleh digunakan kepada perjalanan pekerja.</span><span class="sxs-lookup"><span data-stu-id="96afa-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="96afa-122">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-122">**Decisions:**</span></span>

- <span data-ttu-id="96afa-123">Peraturan bagi sehari lalai untuk hari pertama dan terakhir:</span><span class="sxs-lookup"><span data-stu-id="96afa-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="96afa-124">Berapakah bilangan jam minimum yang boleh dituntut oleh pekerja untuk sehari dan masih menerima bagi sehari?</span><span class="sxs-lookup"><span data-stu-id="96afa-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="96afa-125">Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk hidangan untuk hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="96afa-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="96afa-126">Jika terdapat pengurangan, berapakah peratusan pengurangan?</span><span class="sxs-lookup"><span data-stu-id="96afa-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="96afa-127">Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk hotel untuk hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="96afa-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="96afa-128">Jika terdapat pengurangan, berapakah peratusan pengurangan?</span><span class="sxs-lookup"><span data-stu-id="96afa-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="96afa-129">Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk perbelanjaan lain yang berlaku pada hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="96afa-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="96afa-130">Jika terdapat pengurangan, berapakah peratusan pengurangan?</span><span class="sxs-lookup"><span data-stu-id="96afa-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="96afa-131">Peraturan bagi sehari lalai:</span><span class="sxs-lookup"><span data-stu-id="96afa-131">Default per diem rules:</span></span>

    - <span data-ttu-id="96afa-132">Adakah terdapat pengurangan peratusan bagi elaun bagi sehari untuk setiap hidangan jika, contohnya, hidangan adalah percuma?</span><span class="sxs-lookup"><span data-stu-id="96afa-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="96afa-133">Jika terdapat pengurangan, berapakah peratusan pengurangan untuk setiap hidangan?</span><span class="sxs-lookup"><span data-stu-id="96afa-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="96afa-134">Adakah pengurangan hidangan dikira setiap hari, setiap perjalanan, atau dengan bilangan hidangan setiap hari?</span><span class="sxs-lookup"><span data-stu-id="96afa-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="96afa-135">Perlukah amaun bagi sehari akan dibundarkan mengikut cara biasa atau dibundarkan?</span><span class="sxs-lookup"><span data-stu-id="96afa-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="96afa-136">Adakah bagi sehari dikira pada tempoh 24 jam atau pada hari kalendar?</span><span class="sxs-lookup"><span data-stu-id="96afa-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="96afa-137">Peraturan bagi sehari yang didasarkan pada lokasi:</span><span class="sxs-lookup"><span data-stu-id="96afa-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="96afa-138">Adakah kadar bagi sehari berbeza mengikut lokasi?</span><span class="sxs-lookup"><span data-stu-id="96afa-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="96afa-139">Lokasi apakah yang disertakan?</span><span class="sxs-lookup"><span data-stu-id="96afa-139">What locations are included?</span></span>
    - <span data-ttu-id="96afa-140">Jika kadar bagi sehari berbeza mengikut lokasi, untuk setiap lokasi, apakah amaun peratusan yang disediakan untuk jenis perbelanjaan berikut:</span><span class="sxs-lookup"><span data-stu-id="96afa-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="96afa-141">Hidangan</span><span class="sxs-lookup"><span data-stu-id="96afa-141">Meals</span></span>
        - <span data-ttu-id="96afa-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="96afa-142">Hotel</span></span>
        - <span data-ttu-id="96afa-143">Perbelanjaan lain</span><span class="sxs-lookup"><span data-stu-id="96afa-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="96afa-144">Jurnal pengurusan perbelanjaan dan akaun</span><span class="sxs-lookup"><span data-stu-id="96afa-144">Expense management journals and accounts</span></span>

<span data-ttu-id="96afa-145">Pengurusan perbelanjaan memerlukan anda menggunakan berbilang jurnal dan akaun.</span><span class="sxs-lookup"><span data-stu-id="96afa-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="96afa-146">Anda mesti memutuskan, contohnya, sama ada akaun yang sama digunakan untuk pendahuluan tunai dan pertikaian kad kredit.</span><span class="sxs-lookup"><span data-stu-id="96afa-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="96afa-147">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-147">**Decisions:**</span></span>

- <span data-ttu-id="96afa-148">Jurnal lejar manakah adalah laporan perbelanjaan diluluskan yang disiarkan?</span><span class="sxs-lookup"><span data-stu-id="96afa-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="96afa-149">Akaun manakah yang digunakan untuk pendahuluan tunai?</span><span class="sxs-lookup"><span data-stu-id="96afa-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="96afa-150">Perlukah pendahuluan tunai disiarkan dengan segera?</span><span class="sxs-lookup"><span data-stu-id="96afa-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="96afa-151">Kaedah pembayaran</span><span class="sxs-lookup"><span data-stu-id="96afa-151">Payment methods</span></span>

<span data-ttu-id="96afa-152">Apabila anda membenarkan pekerja menanggung perbelanjaan bagi pihak perniagaan anda, anda mesti mentakrifkan kaedah pembayaran yang pekerja dibenarkan untuk menggunakan.</span><span class="sxs-lookup"><span data-stu-id="96afa-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="96afa-153">Contohnya, anda mungkin membenarkan pekerja menggunakan wang tunai atau kad kredit korporat.</span><span class="sxs-lookup"><span data-stu-id="96afa-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="96afa-154">Anda juga boleh membenarkan pekerja untuk menggunakan kad kredit peribadi, dan kemudian membayar balik pekerja.</span><span class="sxs-lookup"><span data-stu-id="96afa-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="96afa-155">Anda mesti membuat keputusan berikut untuk setiap kaedah pembayaran yang anda benarkan.</span><span class="sxs-lookup"><span data-stu-id="96afa-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="96afa-156">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-156">**Decisions:**</span></span>

- <span data-ttu-id="96afa-157">Apakah kaedah pembayaran yang dibenarkan?</span><span class="sxs-lookup"><span data-stu-id="96afa-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="96afa-158">Siapakah memiliki perbelanjaan kaedah pembayaran?</span><span class="sxs-lookup"><span data-stu-id="96afa-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="96afa-159">Adakah terdapat jenis akaun ofset?</span><span class="sxs-lookup"><span data-stu-id="96afa-159">Is there an offset account type?</span></span> <span data-ttu-id="96afa-160">Jika terdapat jenis akaun ofset, apakah ia?</span><span class="sxs-lookup"><span data-stu-id="96afa-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="96afa-161">Jika terdapat akaun ofset, apakah akaun tersebut?</span><span class="sxs-lookup"><span data-stu-id="96afa-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="96afa-162">Jika kaedah pembayaran adalah kad kredit, perlukah kaedah pembayaran digunakan hanya dengan transaksi yang diimport?</span><span class="sxs-lookup"><span data-stu-id="96afa-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="96afa-163">Kategori perbelanjaan dan kategori dikongsi</span><span class="sxs-lookup"><span data-stu-id="96afa-163">Expense categories and shared categories</span></span>

<span data-ttu-id="96afa-164">Apabila pekerja mencipta laporan perbelanjaan, setiap perbelanjaan yang mereka rekod mesti dikaitkan dengan kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="96afa-165">Kategori perbelanjaan diperoleh daripada kategori dikongsi yang boleh dikongsi merentasi entiti yang sah dalam organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="96afa-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="96afa-166">Kategori ini juga boleh dikongsi dalam Pengurusan projek dan perakaunan, bergantung kepada cara organisasi anda ditakrifkan.</span><span class="sxs-lookup"><span data-stu-id="96afa-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="96afa-167">Berdasarkan definisi organisasi dan panduan anda daripada pasukan pelaksanaan, menentukan sama ada kategori yang digunakan dalam Pengurusan perbelanjaan akan digunakan hanya dalam Pengurusan perbelanjaan, atau sama ada mereka hendaklah dikongsi di antara Pengurusan projek dan perakaunan dan Pengurusan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="96afa-168">Ambil perhatian kategori ini boleh dikongsi di antara Projek dan Perbelanjaan atau Projek dan Pengeluaran, tetapi tidak di antara Perbelanjaan dan Pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="96afa-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="96afa-169">Anda mesti membuat keputusan berikut untuk setiap kategori perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="96afa-170">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-170">**Decisions:**</span></span>

- <span data-ttu-id="96afa-171">Apakah itu kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-171">What is the expense category?</span></span> <span data-ttu-id="96afa-172">Contohnya termasuk kategori untuk penerbangan, hotel, atau perbatuan.</span><span class="sxs-lookup"><span data-stu-id="96afa-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="96afa-173">Bolehkah kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan?</span><span class="sxs-lookup"><span data-stu-id="96afa-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="96afa-174">Apakah itu jenis perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-174">What is the expense type?</span></span>
- <span data-ttu-id="96afa-175">Apakah itu kaedah pembayaran lalai untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="96afa-176">Adakah perbelanjaan dalam kategori perbelanjaan perlu diperincikan?</span><span class="sxs-lookup"><span data-stu-id="96afa-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="96afa-177">Apakah itu akaun lalai utama untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="96afa-178">Apakah itu kumpulan cukai jualan item lalai untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="96afa-179">Adakah kaedah pembayaran tambahan dibenarkan untuk kategori perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="96afa-180">Jika kaedah pembayaran tambahan dibenarkan, apakah itu?</span><span class="sxs-lookup"><span data-stu-id="96afa-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="96afa-181">Adakah terdapat subkategori dalam kategori perbelanjaan ini?</span><span class="sxs-lookup"><span data-stu-id="96afa-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="96afa-182">Jika terdapat subkategori, anda juga mesti membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="96afa-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="96afa-183">Adakah sebarang subkategori dikecualikan daripada pemulihan cukai?</span><span class="sxs-lookup"><span data-stu-id="96afa-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="96afa-184">Apakah itu kumpulan cukai jualan item subkategori?</span><span class="sxs-lookup"><span data-stu-id="96afa-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="96afa-185">Jika kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan, jawab soalan yang tinggal.</span><span class="sxs-lookup"><span data-stu-id="96afa-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="96afa-186">Jika tidak, alihkan ke bahagian seterusnya.</span><span class="sxs-lookup"><span data-stu-id="96afa-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="96afa-187">Akaun kos manakah akan digunakan untuk perbelanjaan yang berikut?</span><span class="sxs-lookup"><span data-stu-id="96afa-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="96afa-188">Kos</span><span class="sxs-lookup"><span data-stu-id="96afa-188">Cost</span></span>
    - <span data-ttu-id="96afa-189">Peruntukan gaji</span><span class="sxs-lookup"><span data-stu-id="96afa-189">Payroll allocation</span></span>
    - <span data-ttu-id="96afa-190">WIP-nilai kos</span><span class="sxs-lookup"><span data-stu-id="96afa-190">WIP-cost value</span></span>
    - <span data-ttu-id="96afa-191">Kos-item</span><span class="sxs-lookup"><span data-stu-id="96afa-191">Cost-item</span></span>
    - <span data-ttu-id="96afa-192">WIP-nilai kos-item</span><span class="sxs-lookup"><span data-stu-id="96afa-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="96afa-193">Kerugian terakru</span><span class="sxs-lookup"><span data-stu-id="96afa-193">Accrued loss</span></span>
    - <span data-ttu-id="96afa-194">WIP-kerugian terakru</span><span class="sxs-lookup"><span data-stu-id="96afa-194">WIP-accrued loss</span></span>

- <span data-ttu-id="96afa-195">Akaun hasil manakah akan digunakan untuk yang berikut?</span><span class="sxs-lookup"><span data-stu-id="96afa-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="96afa-196">Hasil diinvois</span><span class="sxs-lookup"><span data-stu-id="96afa-196">Invoiced revenue</span></span>
    - <span data-ttu-id="96afa-197">Hasil terakru-nilai jualan</span><span class="sxs-lookup"><span data-stu-id="96afa-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="96afa-198">WIP-nilai jualan</span><span class="sxs-lookup"><span data-stu-id="96afa-198">WIP-sales value</span></span>
    - <span data-ttu-id="96afa-199">Hasil terakru-pengeluaran</span><span class="sxs-lookup"><span data-stu-id="96afa-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="96afa-200">WIP-pengeluaran</span><span class="sxs-lookup"><span data-stu-id="96afa-200">WIP-production</span></span>
    - <span data-ttu-id="96afa-201">Hasil terakru-keuntungan</span><span class="sxs-lookup"><span data-stu-id="96afa-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="96afa-202">WIP-keuntungan</span><span class="sxs-lookup"><span data-stu-id="96afa-202">WIP-profit</span></span>
    - <span data-ttu-id="96afa-203">Hasil terakru-langganan</span><span class="sxs-lookup"><span data-stu-id="96afa-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="96afa-204">WIP-langganan</span><span class="sxs-lookup"><span data-stu-id="96afa-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="96afa-205">Cukai</span><span class="sxs-lookup"><span data-stu-id="96afa-205">Taxes</span></span>

<span data-ttu-id="96afa-206">Untuk cukai berkaitan perbelanjaan, anda mesti menentukan apa yang disertakan atau didayakan pada laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="96afa-207">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-207">**Decisions:**</span></span>

- <span data-ttu-id="96afa-208">Adakah cukai jualan dimasukkan ke dalam amaun perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="96afa-209">Perlukah pemulihan cukai didayakan pada perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="96afa-210">Apabila anda merancang lejar umum, jika anda memutuskan untuk menggunakan cukai jualan AS dan menggunakan peraturan cukai, anda tidak boleh mendayakan pemulihan cukai pada perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="96afa-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="96afa-211">(Untuk menggunakan cukai jualan AS dan menggunakan peraturan cukai, tetapkan pilihan **Gunakan peraturan percukaian cukai jualan** kepada **Ya**.)</span><span class="sxs-lookup"><span data-stu-id="96afa-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="96afa-212">Dasar</span><span class="sxs-lookup"><span data-stu-id="96afa-212">Policies</span></span>

<span data-ttu-id="96afa-213">Dengan mencipta dasar laporan perbelanjaan, anda boleh membantu organisasi anda menjimatkan masa dan wang apabila pekerja menanggung perbelanjaan bagi pihaknya.</span><span class="sxs-lookup"><span data-stu-id="96afa-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="96afa-214">Dasar membantu menjamin pekerja kekal dalam belanjawan, memberikan semua maklumat yang diperlukan, dan membelanjakan wang hanya apabila mereka memerlukannya.</span><span class="sxs-lookup"><span data-stu-id="96afa-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="96afa-215">Anda mesti membuat keputusan berikut untuk setiap dasar laporan perbelanjaan dan setiap dasar kelulusan laporan perbelanjaan yang anda cipta.</span><span class="sxs-lookup"><span data-stu-id="96afa-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="96afa-216">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="96afa-216">**Decisions:**</span></span>

- <span data-ttu-id="96afa-217">Apakah nama dasar itu?</span><span class="sxs-lookup"><span data-stu-id="96afa-217">What is the name of the policy?</span></span>
- <span data-ttu-id="96afa-218">Untuk apakah dasar perbelanjaan?</span><span class="sxs-lookup"><span data-stu-id="96afa-218">What is the expense policy for?</span></span>
- <span data-ttu-id="96afa-219">Jika anda sebelum ini memutuskan untuk mendayakan perbelanjaan antara syarikat, syarikat mana dalam organisasi anda akan menggunakan dasar ini?</span><span class="sxs-lookup"><span data-stu-id="96afa-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="96afa-220">Bilakah dasar ini berkuat kuasa?</span><span class="sxs-lookup"><span data-stu-id="96afa-220">When does the policy become effective?</span></span>
- <span data-ttu-id="96afa-221">Bilakah dasar ini tamat tempoh?</span><span class="sxs-lookup"><span data-stu-id="96afa-221">When does the policy expire?</span></span>
- <span data-ttu-id="96afa-222">Apakah itu peraturan dasar?</span><span class="sxs-lookup"><span data-stu-id="96afa-222">What is the policy rule?</span></span>
- <span data-ttu-id="96afa-223">Apakah hasil peraturan dasar itu?</span><span class="sxs-lookup"><span data-stu-id="96afa-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]