---
title: Gambaran keseluruhan dimensi penentuan harga
description: Topik ini menyediakan maklumat tentang dimensi penetapan harga dalam Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081335"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="fb0ee-103">Gambaran keseluruhan dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="fb0ee-103">Pricing dimensions overview</span></span>

<span data-ttu-id="fb0ee-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="fb0ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb0ee-105">Dimensi yang digunakan dalam sumber manusia untuk menyediakan penetapan harga dan kos terbahagi kepada dua kategori:</span><span class="sxs-lookup"><span data-stu-id="fb0ee-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="fb0ee-106">Orang</span><span class="sxs-lookup"><span data-stu-id="fb0ee-106">People</span></span>
- <span data-ttu-id="fb0ee-107">Kerja dirancang</span><span class="sxs-lookup"><span data-stu-id="fb0ee-107">Planned work</span></span>

<span data-ttu-id="fb0ee-108">Disebabkan ini, terdapat dua jenis nilai dimensi penetapan harga tersedia:</span><span class="sxs-lookup"><span data-stu-id="fb0ee-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="fb0ee-109">**Set pilihan** : Dimensi yang merupakan penghitungan tetap bagi set nilai.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="fb0ee-110">**Nilai berasaskan entiti** : Dimensi yang boleh menjadi set nilai yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="fb0ee-111">Dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="fb0ee-111">Pricing dimensions</span></span>

<span data-ttu-id="fb0ee-112">Operasi Projek Dynamics 365 dihantar dengan set dimensi penetapan harga lalai.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="fb0ee-113">Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="fb0ee-114">Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah** , sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="fb0ee-115">Anda boleh menyediakan harga dan kos untuk setiap peranan dan kombinasi unit organisasi dengan medan ini didayakan.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="fb0ee-116">Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="fb0ee-117">Masa penetapan harga sumber manusia</span><span class="sxs-lookup"><span data-stu-id="fb0ee-117">Pricing human resource time</span></span>
<span data-ttu-id="fb0ee-118">Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="fb0ee-119">Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="fb0ee-120">Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="fb0ee-121">Medan seperti **Kategori Transaksi** ( **msdyn_transactioncategory** ) dan **Sumber Boleh Ditempah** ( **bookableresource** ) ialah contoh dimensi calon.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="fb0ee-122">Pertimbangkan sama ada dimensi penetapan harga anda mesti jadual atau set pilihan.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="fb0ee-123">Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda boleh mencipta entiti dan bukannya set pilihan.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="fb0ee-124">Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru ke jadual boleh dilakukan oleh kebanyakan pengguna.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="fb0ee-125">Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="fb0ee-126">Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="fb0ee-127">Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.</span><span class="sxs-lookup"><span data-stu-id="fb0ee-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="fb0ee-128">**Sampel kadar bil**</span><span class="sxs-lookup"><span data-stu-id="fb0ee-128">**Sample bill rates**</span></span>

| <span data-ttu-id="fb0ee-129">Peranan</span><span class="sxs-lookup"><span data-stu-id="fb0ee-129">Role</span></span>        | <span data-ttu-id="fb0ee-130">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="fb0ee-130">Org Unit</span></span>    |<span data-ttu-id="fb0ee-131">Unit</span><span class="sxs-lookup"><span data-stu-id="fb0ee-131">Unit</span></span>      |<span data-ttu-id="fb0ee-132">Harga</span><span class="sxs-lookup"><span data-stu-id="fb0ee-132">Price</span></span>      |<span data-ttu-id="fb0ee-133">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="fb0ee-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="fb0ee-134">Pembangun</span><span class="sxs-lookup"><span data-stu-id="fb0ee-134">Developer</span></span>   | <span data-ttu-id="fb0ee-135">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="fb0ee-135">Contoso US</span></span>  |<span data-ttu-id="fb0ee-136">Hour</span><span class="sxs-lookup"><span data-stu-id="fb0ee-136">Hour</span></span> | <span data-ttu-id="fb0ee-137">200</span><span class="sxs-lookup"><span data-stu-id="fb0ee-137">200</span></span>|<span data-ttu-id="fb0ee-138">USD</span><span class="sxs-lookup"><span data-stu-id="fb0ee-138">USD</span></span>     |
| <span data-ttu-id="fb0ee-139">Pembangun</span><span class="sxs-lookup"><span data-stu-id="fb0ee-139">Developer</span></span>   | <span data-ttu-id="fb0ee-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="fb0ee-140">Contoso India</span></span> |<span data-ttu-id="fb0ee-141">Hour</span><span class="sxs-lookup"><span data-stu-id="fb0ee-141">Hour</span></span>|   <span data-ttu-id="fb0ee-142">112</span><span class="sxs-lookup"><span data-stu-id="fb0ee-142">112</span></span>|<span data-ttu-id="fb0ee-143">USD</span><span class="sxs-lookup"><span data-stu-id="fb0ee-143">USD</span></span>     |


<span data-ttu-id="fb0ee-144">**Sampel kadar kos**</span><span class="sxs-lookup"><span data-stu-id="fb0ee-144">**Sample cost rates**</span></span>

| <span data-ttu-id="fb0ee-145">Jalur Gaji</span><span class="sxs-lookup"><span data-stu-id="fb0ee-145">Salary Band</span></span>     | <span data-ttu-id="fb0ee-146">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="fb0ee-146">Org Unit</span></span>    |<span data-ttu-id="fb0ee-147">Unit</span><span class="sxs-lookup"><span data-stu-id="fb0ee-147">Unit</span></span>      |<span data-ttu-id="fb0ee-148">Harga</span><span class="sxs-lookup"><span data-stu-id="fb0ee-148">Price</span></span>      |<span data-ttu-id="fb0ee-149">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="fb0ee-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="fb0ee-150">Syarikat saya_Jalur1</span><span class="sxs-lookup"><span data-stu-id="fb0ee-150">My company_Band1</span></span> | <span data-ttu-id="fb0ee-151">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="fb0ee-151">Contoso US</span></span>  |<span data-ttu-id="fb0ee-152">Hour</span><span class="sxs-lookup"><span data-stu-id="fb0ee-152">Hour</span></span> | <span data-ttu-id="fb0ee-153">145</span><span class="sxs-lookup"><span data-stu-id="fb0ee-153">145</span></span>|<span data-ttu-id="fb0ee-154">USD</span><span class="sxs-lookup"><span data-stu-id="fb0ee-154">USD</span></span>     |
| <span data-ttu-id="fb0ee-155">Syarikat saya_Jalur2</span><span class="sxs-lookup"><span data-stu-id="fb0ee-155">My company_Band2</span></span> | <span data-ttu-id="fb0ee-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="fb0ee-156">Contoso India</span></span> |<span data-ttu-id="fb0ee-157">Hour</span><span class="sxs-lookup"><span data-stu-id="fb0ee-157">Hour</span></span>|   <span data-ttu-id="fb0ee-158">67</span><span class="sxs-lookup"><span data-stu-id="fb0ee-158">67</span></span>|<span data-ttu-id="fb0ee-159">USD</span><span class="sxs-lookup"><span data-stu-id="fb0ee-159">USD</span></span>     |
