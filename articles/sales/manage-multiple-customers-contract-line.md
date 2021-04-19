---
title: Urus berbilang pelanggan pada baris kontrak berasaskan projek
description: Topik ini memberikan maklumat tentang bekerja dengan baris kontrak dan kontrak yang mengandungi berbilang pelanggan.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 205363d2ea5f1f5bf5fa8879cedd5b3e857eb772
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278024"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a><span data-ttu-id="09336-103">Urus berbilang pelanggan pada baris kontrak berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="09336-103">Manage multiple customers on project-based contract lines</span></span>

<span data-ttu-id="09336-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="09336-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09336-105">Baris kontrak berasaskan projek boleh memasukkan senarai pelanggan yang bertanggungjawab untuk pembayaran.</span><span class="sxs-lookup"><span data-stu-id="09336-105">Project-based contract lines can include a list of customers that are responsible for payment.</span></span> <span data-ttu-id="09336-106">Senarai pelanggan pada baris kontrak berasaskan projek ini boleh sama dengan senarai pelanggan pada kontrak, tetapi tidak diperlukan.</span><span class="sxs-lookup"><span data-stu-id="09336-106">This list of customers on the project-based contract line can be same as the list of customers on the contract but that isn't required.</span></span> <span data-ttu-id="09336-107">Apabila sebut harga projek dimenangi dan kontrak projek dicipta, senarai pelanggan pada baris sebut harga disalin ke baris kontrak yang sepadan.</span><span class="sxs-lookup"><span data-stu-id="09336-107">When a project quote is won, and a project contract is created, the customer list on the quote line is copied to the corresponding contract line.</span></span> <span data-ttu-id="09336-108">Pelanggan pada sebut harga disalin ke kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-108">Customers on the quote are copied to the contract.</span></span>

<span data-ttu-id="09336-109">Apabila kontrak projek diinvois, senarai pelanggan pada baris kontrak berasaskan projek diutamakan daripada senarai pelanggan pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-109">When the project contract is invoiced, the customer list on project-based contract line takes priority over the customer list on the contract.</span></span> <span data-ttu-id="09336-110">Senarai pelanggan pada kontrak projek hanya digunakan untuk baris kontrak baharu lalai.</span><span class="sxs-lookup"><span data-stu-id="09336-110">The customer list on the project contract is only used to default new contract lines.</span></span>

<span data-ttu-id="09336-111">Semua pelanggan kontrak pada tab **Pelanggan** kontrak projek adalah lalai kerana pelanggan baris kontrak pada mana-mana baris kontrak baharu dicipta untuk kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="09336-111">All contract customers on the **Customers** tab of the project contract default as contract line customers on any new contract lines created for the project contract.</span></span> <span data-ttu-id="09336-112">Mana-mana baris kontrak yang sedia ada tidak akan mewarisi rekod pelanggan kontrak baharu yang dicipta selepas itu.</span><span class="sxs-lookup"><span data-stu-id="09336-112">Any existing contract lines will not inherit the new contract customer records created after them.</span></span>

## <a name="create-update-or-delete-a-contract-line-customer-record"></a><span data-ttu-id="09336-113">Cipta, kemas kini atau padamkan rekod pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="09336-113">Create, update, or delete a contract line customer record</span></span>

<span data-ttu-id="09336-114">Anda boleh mencipta, mengemas kini atau memadamkan pelanggan baris kontrak daripada tab **Pelanggan Baris Kontrak** pada halaman **Baris Kontrak berasaskan Projek**.</span><span class="sxs-lookup"><span data-stu-id="09336-114">You can create, update, or delete a contract line customer from the **Contract Line Customers** tab on the **Project-based Contract Line** page.</span></span> <span data-ttu-id="09336-115">Apabila pelanggan baharu ditambah pada baris kontrak berasaskan projek, mereka juga ditambah pada keseluruhan kontrak sebagai pelanggan kontrak dengan peratusan pecahan bil lalai sebanyak kosong peratus.</span><span class="sxs-lookup"><span data-stu-id="09336-115">When a new customer is added on the project-based contract line, they are also added on the overall contract as a contract customer with a default billing split percentage of zero percent.</span></span> <span data-ttu-id="09336-116">Peratusan pecahan bil pada keseluruhan kontrak disalin ke baris kontrak baharu dan ke kontrak projek akhir.</span><span class="sxs-lookup"><span data-stu-id="09336-116">The billing split percentage on the overall contract is copied to new contract lines and to the eventual project contract.</span></span> <span data-ttu-id="09336-117">Walau bagaimanapun, apabila invois daripada kontrak, invois itu ialah peratusan pecahan bil pada peringkat baris kontrak yang digunakan dan bukan peratusan pecahan bil pada peringkat keseluruhan kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-117">However, when invoicing from the contract, it's the billing split percentage at the contract line level that is used and not the billing split percentage at the overall contract level.</span></span> 

<span data-ttu-id="09336-118">Berikut ialah medan pada rekod pelanggan baris Kontrak bagi baris Kontrak berasaskan projek yang perlu diingat ketika anda bekerja dengan baris tersebut:</span><span class="sxs-lookup"><span data-stu-id="09336-118">Below are the fields on the Contract line customer record of a project-based Contract line to keep in mind as you are working with it:</span></span>

| <span data-ttu-id="09336-119">Medan</span><span class="sxs-lookup"><span data-stu-id="09336-119">Field</span></span> | <span data-ttu-id="09336-120">Lokasi</span><span class="sxs-lookup"><span data-stu-id="09336-120">Location</span></span> | <span data-ttu-id="09336-121">Penerangan </span><span class="sxs-lookup"><span data-stu-id="09336-121">Description</span></span> | <span data-ttu-id="09336-122">Kesan hiliran</span><span class="sxs-lookup"><span data-stu-id="09336-122">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="09336-123">Akaun</span><span class="sxs-lookup"><span data-stu-id="09336-123">Account</span></span> | <span data-ttu-id="09336-124">Grid boleh diedit pada tab **Pelanggan Baris Kontrak** dan borang Utama dan Cipta Cepat untuk pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="09336-124">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="09336-125">Semua akaun aktif.</span><span class="sxs-lookup"><span data-stu-id="09336-125">All active accounts.</span></span> <span data-ttu-id="09336-126">Medan ini dikunci selepas rekod dicipta.</span><span class="sxs-lookup"><span data-stu-id="09336-126">This field is locked after the record is created.</span></span> <span data-ttu-id="09336-127">Untuk mengemas kini medan, padamkan rekod dan cipta rekod baharu.</span><span class="sxs-lookup"><span data-stu-id="09336-127">To update the field, delete the record, and create a new record.</span></span> <span data-ttu-id="09336-128">Jika anda telah merekodkan sebarang aktual, anda tidak boleh memadamkan rekod tersebut.</span><span class="sxs-lookup"><span data-stu-id="09336-128">If you have recorded any actuals, you can't delete the record.</span></span> <span data-ttu-id="09336-129">Walau bagaimanapun, anda boleh menandakan peratusan pecahan bil sebagai sifar untuk akaun tersebut.</span><span class="sxs-lookup"><span data-stu-id="09336-129">However, you can mark the billing split percentage as zero for that account.</span></span> <span data-ttu-id="09336-130">Apabila rekod ditandakan sebagai sifar, mana-mana kos masa depan dan aktual hasil yang diatribut atau dipecahkan kepada pelanggan ini akan terjejas.</span><span class="sxs-lookup"><span data-stu-id="09336-130">When the record is marked as zero, any future cost and revenue actuals that are attributed or split to this customer are impacted.</span></span> | <span data-ttu-id="09336-131">Apabila anda memilih akaun daripada senarai induk akaun untuk menambah dan menyimpan akaun tersebut, pelanggan baris kontrak juga ditambah sebagai pelanggan kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-131">When you pick an account from the master list of accounts to add and save them, the contract line customer is also added as a contract customer.</span></span> <span data-ttu-id="09336-132">Pelanggan baris kontrak digunakan apabila invois dijana.</span><span class="sxs-lookup"><span data-stu-id="09336-132">Contract line customers are used when invoices are generated.</span></span> |
| <span data-ttu-id="09336-133">Peratusan Pecahan Pengebilan</span><span class="sxs-lookup"><span data-stu-id="09336-133">Billing split percent</span></span> | <span data-ttu-id="09336-134">Grid boleh diedit pada tab **Pelanggan Baris Kontrak** dan borang Utama dan Cipta Cepat untuk pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="09336-134">Editable grid on **Contract Line Customers** tab and the Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="09336-135">Medan ini mewakili peratusan setiap transaksi jualan belum dibilkan yang akan diatribut kepada pelanggan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="09336-135">This field represents the percentage of each unbilled sales transaction that will be attributed to this contract line customer.</span></span> | <span data-ttu-id="09336-136">Pelanggan baris kontrak dan peratusan pecahan bil digunakan apabila aktual dicipta selepas mendapat kelulusan dan apabila invois dijana.</span><span class="sxs-lookup"><span data-stu-id="09336-136">Contract line customers and billing split percentages are used when actuals are created after approval and when the invoice is generated.</span></span> |
| <span data-ttu-id="09336-137">Had yang tidak boleh melebihi</span><span class="sxs-lookup"><span data-stu-id="09336-137">Not-to-exceed limit</span></span> | <span data-ttu-id="09336-138">Grid boleh diedit pada tab **Pelanggan Baris Kontrak** dan borang Utama dan Cipta Cepat untuk pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="09336-138">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="09336-139">Menunjukkan jika terdapat had yang dirundingkan atau had kepada jumlah keseluruhan yang akan diinvoiskan kepada pelanggan ini untuk baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-139">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for the contract line.</span></span> | <span data-ttu-id="09336-140">Had tidak-boleh dilebihi untuk pelanggan baris kontrak digunakan apabila aktual dicipta dan invois dijana.</span><span class="sxs-lookup"><span data-stu-id="09336-140">The not-to-exceed limit for the contract line customer is used when actuals are created and the invoices are generated.</span></span> |
| <span data-ttu-id="09336-141">Syarikat Pemilikan</span><span class="sxs-lookup"><span data-stu-id="09336-141">Owning Company</span></span> | <span data-ttu-id="09336-142">Grid boleh diedit pada tab **Pelanggan Baris Sebut Harga** dan borang Utama dan Cipta Cepat untuk pelanggan baris sebut harga</span><span class="sxs-lookup"><span data-stu-id="09336-142">Editable grid on the **Quote Line Customers** tab and the Main and Quick Create forms for a quote line customer</span></span> | <span data-ttu-id="09336-143">Entiti sah yang pelanggan ini sediakan.</span><span class="sxs-lookup"><span data-stu-id="09336-143">The legal entity that this customer is set up in.</span></span> <span data-ttu-id="09336-144">Medan ini adalah baca sahaja dan ditetapkan kepada syarikat pemilikan sebut harga.</span><span class="sxs-lookup"><span data-stu-id="09336-144">This field is read-only and is set to the owning company of the quote.</span></span> <span data-ttu-id="09336-145">Senarai pelanggan untuk ditambah dalam medan **Akaun** telah ditapis kepada senarai daripada syarikat pemilikan ini.</span><span class="sxs-lookup"><span data-stu-id="09336-145">The list of customers to add in the **Account** field is already filtered to the list from this owning company.</span></span> | <span data-ttu-id="09336-146">Konsep syarikat pemilikan adalah sama dengan konsep entiti sah.</span><span class="sxs-lookup"><span data-stu-id="09336-146">The concept of an owning company equates to the concept of a legal entity.</span></span> <span data-ttu-id="09336-147">Semua kos dan hasil yang terakru daripada projek ini diambil kira dalam Lejar umum syarikat pemilikan.</span><span class="sxs-lookup"><span data-stu-id="09336-147">All costs and revenue accruing from this project are accounted for in the General ledger of the owning company.</span></span> |
| <span data-ttu-id="09336-148">Adakah Pembundaran</span><span class="sxs-lookup"><span data-stu-id="09336-148">Is Rounding</span></span> | <span data-ttu-id="09336-149">Grid boleh diedit pada tab **Pelanggan Baris Kontrak** dan borang Utama dan Cipta Cepat untuk pelanggan baris kontrak</span><span class="sxs-lookup"><span data-stu-id="09336-149">Editable grid on **Contract Line Customers** tab and Main and Quick Create forms for a contract line customer</span></span> | <span data-ttu-id="09336-150">Medan ini menunjukkan jika pelanggan ini ialah pelanggan pembundaran lalai untuk baris kontrak berasaskan projek ini.</span><span class="sxs-lookup"><span data-stu-id="09336-150">This field indicates if this customer is a default rounding customer for this project-based contract line.</span></span> | <span data-ttu-id="09336-151">Apabila anda menjana aktual mengikut peratusan pecahan bil, mungkin terdapat beberapa perbezaan pembundaran.</span><span class="sxs-lookup"><span data-stu-id="09336-151">When you generate an actual according to the billing split percentage, there may be some rounding differences.</span></span> <span data-ttu-id="09336-152">Pelanggan ini diatribut dengan perbezaan pembundaran dalam situasi ini.</span><span class="sxs-lookup"><span data-stu-id="09336-152">This customer is attributed the rounding differences in this case.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="09336-153">Edit peratusan pecahan pengebilan</span><span class="sxs-lookup"><span data-stu-id="09336-153">Edit billing split percentages</span></span>

<span data-ttu-id="09336-154">Peratusan pecahan bil boleh diedit dalam grid.</span><span class="sxs-lookup"><span data-stu-id="09336-154">Billing split percentages can be edited in the grid.</span></span> <span data-ttu-id="09336-155">Apabila peratusan pecahan bil tidak berjumlah 100 peratus, ralat akan berlaku.</span><span class="sxs-lookup"><span data-stu-id="09336-155">When the billing split percentages don't total 100 percent, an error will occur.</span></span> <span data-ttu-id="09336-156">Selepas anda mengedit peratusan pecahan bil, segar semula halaman untuk mengeluarkan ralat.</span><span class="sxs-lookup"><span data-stu-id="09336-156">After you edit the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="09336-157">Anda juga boleh cuba memilih **Agihkan Secara Sekata** pada subgrid pelanggan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="09336-157">You can also try selecting **Evenly Distribute** on the contract line customer subgrid.</span></span> <span data-ttu-id="09336-158">Tindakan ini menguntukkan pecahan bil kepada semua pelanggan baris kontrak secara sekata.</span><span class="sxs-lookup"><span data-stu-id="09336-158">This action evenly allocates billing splits to all contract line customers.</span></span> <span data-ttu-id="09336-159">Jika terdapat mana-mana faktor pembundaran, faktor itu akan ditambah kepada pelanggan pembundaran.</span><span class="sxs-lookup"><span data-stu-id="09336-159">If there is any rounding factor, it will be added to the rounding customer.</span></span> <span data-ttu-id="09336-160">Seorang pelanggan baris kontrak sentiasa ditandakan sebagai pelanggan **Pembundaran** dengan bendera **Pembundaran** ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="09336-160">One contract line customer is always tagged as the **Rounding** customer with the **Rounding** flag set to **Yes**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]