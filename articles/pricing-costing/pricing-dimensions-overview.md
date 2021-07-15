---
title: Gambaran keseluruhan dimensi penentuan harga
description: Topik ini memberikan maklumat tentang dimensi penetapan harga dalam Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368487"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="51029-103">Gambaran keseluruhan dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="51029-103">Pricing dimensions overview</span></span>

<span data-ttu-id="51029-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="51029-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51029-105">Dimensi yang digunakan dalam sumber manusia untuk menyediakan penetapan harga dan kos terbahagi kepada dua kategori:</span><span class="sxs-lookup"><span data-stu-id="51029-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="51029-106">Orang</span><span class="sxs-lookup"><span data-stu-id="51029-106">People</span></span>
- <span data-ttu-id="51029-107">Kerja dirancang</span><span class="sxs-lookup"><span data-stu-id="51029-107">Planned work</span></span>

<span data-ttu-id="51029-108">Disebabkan ini, terdapat dua jenis nilai dimensi penetapan harga tersedia:</span><span class="sxs-lookup"><span data-stu-id="51029-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="51029-109">**Set pilihan**: Dimensi yang merupakan penghitungan tetap bagi set nilai.</span><span class="sxs-lookup"><span data-stu-id="51029-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="51029-110">**Nilai berasaskan entiti**: Dimensi yang boleh menjadi set nilai yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="51029-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="51029-111">Dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="51029-111">Pricing dimensions</span></span>

<span data-ttu-id="51029-112">Dynamics 365 Project Operations didatangkan dengan set dimensi penetapan harga lalai.</span><span class="sxs-lookup"><span data-stu-id="51029-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="51029-113">Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="51029-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="51029-114">Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah**, sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="51029-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="51029-115">Anda boleh menyediakan harga dan kos untuk setiap peranan dan kombinasi unit organisasi dengan medan ini didayakan.</span><span class="sxs-lookup"><span data-stu-id="51029-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

<span data-ttu-id="51029-117">Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai.</span><span class="sxs-lookup"><span data-stu-id="51029-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="51029-118">Untuk maklumat lanjut, lihat topik yang berikut.</span><span class="sxs-lookup"><span data-stu-id="51029-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="51029-119">Prosedur mesti dilengkapkan mengikut susunan yang disenaraikan.</span><span class="sxs-lookup"><span data-stu-id="51029-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="51029-120">Cipta penyelesaian untuk dimensi penetapan harga tersuai</span><span class="sxs-lookup"><span data-stu-id="51029-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="51029-121">Cipta medan dan entiti tersuai</span><span class="sxs-lookup"><span data-stu-id="51029-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="51029-122">Tambah medan tersuai kepada persediaan harga dan entiti transaksi </span><span class="sxs-lookup"><span data-stu-id="51029-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="51029-123">Sediakan medan tersuai sebagai dimensi penetapan harga </span><span class="sxs-lookup"><span data-stu-id="51029-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="51029-124">Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu</span><span class="sxs-lookup"><span data-stu-id="51029-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="51029-125">Masa penetapan harga sumber manusia</span><span class="sxs-lookup"><span data-stu-id="51029-125">Pricing human resource time</span></span>
<span data-ttu-id="51029-126">Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi.</span><span class="sxs-lookup"><span data-stu-id="51029-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="51029-127">Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.</span><span class="sxs-lookup"><span data-stu-id="51029-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="51029-128">Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="51029-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="51029-129">Medan seperti **Kategori Transaksi** (**msdyn_transactioncategory**) dan **Sumber Boleh Ditempah** (**bookableresource**) ialah contoh dimensi calon.</span><span class="sxs-lookup"><span data-stu-id="51029-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="51029-130">Pertimbangkan sama ada dimensi penetapan harga anda mesti jadual atau set pilihan.</span><span class="sxs-lookup"><span data-stu-id="51029-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="51029-131">Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda boleh mencipta entiti dan bukannya set pilihan.</span><span class="sxs-lookup"><span data-stu-id="51029-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="51029-132">Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru ke jadual boleh dilakukan oleh kebanyakan pengguna.</span><span class="sxs-lookup"><span data-stu-id="51029-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="51029-133">Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki.</span><span class="sxs-lookup"><span data-stu-id="51029-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="51029-134">Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong.</span><span class="sxs-lookup"><span data-stu-id="51029-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="51029-135">Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.</span><span class="sxs-lookup"><span data-stu-id="51029-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="51029-136">**Sampel kadar bil**</span><span class="sxs-lookup"><span data-stu-id="51029-136">**Sample bill rates**</span></span>

| <span data-ttu-id="51029-137">Peranan</span><span class="sxs-lookup"><span data-stu-id="51029-137">Role</span></span>        | <span data-ttu-id="51029-138">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="51029-138">Org Unit</span></span>    |<span data-ttu-id="51029-139">Unit</span><span class="sxs-lookup"><span data-stu-id="51029-139">Unit</span></span>      |<span data-ttu-id="51029-140">Harga</span><span class="sxs-lookup"><span data-stu-id="51029-140">Price</span></span>      |<span data-ttu-id="51029-141">Mata wang</span><span class="sxs-lookup"><span data-stu-id="51029-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="51029-142">Pemaju</span><span class="sxs-lookup"><span data-stu-id="51029-142">Developer</span></span>   | <span data-ttu-id="51029-143">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="51029-143">Contoso US</span></span>  |<span data-ttu-id="51029-144">Jam</span><span class="sxs-lookup"><span data-stu-id="51029-144">Hour</span></span> | <span data-ttu-id="51029-145">200</span><span class="sxs-lookup"><span data-stu-id="51029-145">200</span></span>|<span data-ttu-id="51029-146">USD</span><span class="sxs-lookup"><span data-stu-id="51029-146">USD</span></span>     |
| <span data-ttu-id="51029-147">Pemaju</span><span class="sxs-lookup"><span data-stu-id="51029-147">Developer</span></span>   | <span data-ttu-id="51029-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="51029-148">Contoso India</span></span> |<span data-ttu-id="51029-149">Jam</span><span class="sxs-lookup"><span data-stu-id="51029-149">Hour</span></span>|   <span data-ttu-id="51029-150">112</span><span class="sxs-lookup"><span data-stu-id="51029-150">112</span></span>|<span data-ttu-id="51029-151">USD</span><span class="sxs-lookup"><span data-stu-id="51029-151">USD</span></span>     |


<span data-ttu-id="51029-152">**Sampel kadar kos**</span><span class="sxs-lookup"><span data-stu-id="51029-152">**Sample cost rates**</span></span>

| <span data-ttu-id="51029-153">Jalur Gaji</span><span class="sxs-lookup"><span data-stu-id="51029-153">Salary Band</span></span>     | <span data-ttu-id="51029-154">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="51029-154">Org Unit</span></span>    |<span data-ttu-id="51029-155">Unit</span><span class="sxs-lookup"><span data-stu-id="51029-155">Unit</span></span>      |<span data-ttu-id="51029-156">Harga</span><span class="sxs-lookup"><span data-stu-id="51029-156">Price</span></span>      |<span data-ttu-id="51029-157">Mata wang</span><span class="sxs-lookup"><span data-stu-id="51029-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="51029-158">Syarikat saya_Jalur1</span><span class="sxs-lookup"><span data-stu-id="51029-158">My company_Band1</span></span> | <span data-ttu-id="51029-159">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="51029-159">Contoso US</span></span>  |<span data-ttu-id="51029-160">Jam</span><span class="sxs-lookup"><span data-stu-id="51029-160">Hour</span></span> | <span data-ttu-id="51029-161">145</span><span class="sxs-lookup"><span data-stu-id="51029-161">145</span></span>|<span data-ttu-id="51029-162">USD</span><span class="sxs-lookup"><span data-stu-id="51029-162">USD</span></span>     |
| <span data-ttu-id="51029-163">Syarikat saya_Jalur2</span><span class="sxs-lookup"><span data-stu-id="51029-163">My company_Band2</span></span> | <span data-ttu-id="51029-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="51029-164">Contoso India</span></span> |<span data-ttu-id="51029-165">Jam</span><span class="sxs-lookup"><span data-stu-id="51029-165">Hour</span></span>|   <span data-ttu-id="51029-166">67</span><span class="sxs-lookup"><span data-stu-id="51029-166">67</span></span>|<span data-ttu-id="51029-167">USD</span><span class="sxs-lookup"><span data-stu-id="51029-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]