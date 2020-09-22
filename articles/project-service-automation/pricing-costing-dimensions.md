---
title: Halaman utama dimensi penetapan harga dan kos
description: Topik ini memberikan gambaran keseluruhan dimensi penetapan harga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753887"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="7cb9f-103">Halaman utama dimensi penetapan harga dan kos</span><span class="sxs-lookup"><span data-stu-id="7cb9f-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="7cb9f-104">Dimensi yang digunakan dalam sumber manusia untuk menyediakan penetapan harga dan kos terbahagi kepada dua kategori:</span><span class="sxs-lookup"><span data-stu-id="7cb9f-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="7cb9f-105">Orang</span><span class="sxs-lookup"><span data-stu-id="7cb9f-105">People</span></span>
- <span data-ttu-id="7cb9f-106">Kerja dirancang</span><span class="sxs-lookup"><span data-stu-id="7cb9f-106">Planned work</span></span>

<span data-ttu-id="7cb9f-107">Disebabkan ini, terdapat dua jenis nilai dimensi penetapan harga tersedia dalam Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="7cb9f-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="7cb9f-108">**Set pilihan** - Dimensi yang merupakan pengangkaan tetap bagi satu set nilai.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="7cb9f-109">**Nilai berasaskan entiti** - Dimensi yang boleh menjadi satu set nilai yang berbeza-beza.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="7cb9f-110">Dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="7cb9f-110">Pricing dimensions</span></span>

<span data-ttu-id="7cb9f-111">Kapal PSA dengan set dimensi penetapan harga lalai.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="7cb9f-112">Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="7cb9f-113">Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah**, sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="7cb9f-114">Ini akan membolehkan anda menyediakan harga dan kos untuk setiap peranan dan gabungan unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="7cb9f-116">Jika anda telah menggunakan medan peranan siap guna dan unit organisasi sebagai dimensi penetapan harga sebelum versi 3 PSA, tidak akan ada perubahan yang dapat dilihat.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="7cb9f-117">Anda boleh terus menggunakan Project Service seperti biasa.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="7cb9f-118">Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="7cb9f-119">Untuk mendapatkan maklumat lanjut, lihat topik berikut, walau bagaimanapun, sila ambil perhatian bahawa anda mesti melengkapkan prosedur dalam dalam pesanan yang disenaraikan di bawah:</span><span class="sxs-lookup"><span data-stu-id="7cb9f-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="7cb9f-120">Cipta medan dan entiti tersuai</span><span class="sxs-lookup"><span data-stu-id="7cb9f-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="7cb9f-121">Tambah medan tersuai kepada persediaan harga dan entiti transaksi</span><span class="sxs-lookup"><span data-stu-id="7cb9f-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="7cb9f-122">Sediakan medan tersuai sebagai dimensi penetapan harga</span><span class="sxs-lookup"><span data-stu-id="7cb9f-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="7cb9f-123">Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu</span><span class="sxs-lookup"><span data-stu-id="7cb9f-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="7cb9f-124">Masa penetapan harga sumber manusia</span><span class="sxs-lookup"><span data-stu-id="7cb9f-124">Pricing human resource time</span></span>
<span data-ttu-id="7cb9f-125">Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="7cb9f-126">Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="7cb9f-127">Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="7cb9f-128">Medan seperti **Kategori Transaksi** (**msdyn_transactioncategory**) dan **Sumber Boleh Ditempah** (**bookableresource**) ialah contoh dimensi calon.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="7cb9f-129">Anda juga perlu mempertimbangkan sama ada dimensi penetapan harga anda mestilah jadual atau set pilihan.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="7cb9f-130">Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda boleh mencipta entiti dan bukannya set pilihan.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="7cb9f-131">Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru ke jadual boleh dilakukan oleh kebanyakan pengguna.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="7cb9f-132">Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="7cb9f-133">Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="7cb9f-134">Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.</span><span class="sxs-lookup"><span data-stu-id="7cb9f-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="7cb9f-135">**Sampel kadar bil**</span><span class="sxs-lookup"><span data-stu-id="7cb9f-135">**Sample bill rates**</span></span>

| <span data-ttu-id="7cb9f-136">Peranan</span><span class="sxs-lookup"><span data-stu-id="7cb9f-136">Role</span></span>        | <span data-ttu-id="7cb9f-137">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="7cb9f-137">Org Unit</span></span>    |<span data-ttu-id="7cb9f-138">Unit</span><span class="sxs-lookup"><span data-stu-id="7cb9f-138">Unit</span></span>      |<span data-ttu-id="7cb9f-139">Harga</span><span class="sxs-lookup"><span data-stu-id="7cb9f-139">Price</span></span>      |<span data-ttu-id="7cb9f-140">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="7cb9f-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="7cb9f-141">Pembangun</span><span class="sxs-lookup"><span data-stu-id="7cb9f-141">Developer</span></span>   | <span data-ttu-id="7cb9f-142">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="7cb9f-142">Contoso US</span></span>  |<span data-ttu-id="7cb9f-143">Hour</span><span class="sxs-lookup"><span data-stu-id="7cb9f-143">Hour</span></span> | <span data-ttu-id="7cb9f-144">200</span><span class="sxs-lookup"><span data-stu-id="7cb9f-144">200</span></span>|<span data-ttu-id="7cb9f-145">USD</span><span class="sxs-lookup"><span data-stu-id="7cb9f-145">USD</span></span>     |
| <span data-ttu-id="7cb9f-146">Pembangun</span><span class="sxs-lookup"><span data-stu-id="7cb9f-146">Developer</span></span>   | <span data-ttu-id="7cb9f-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="7cb9f-147">Contoso India</span></span> |<span data-ttu-id="7cb9f-148">Hour</span><span class="sxs-lookup"><span data-stu-id="7cb9f-148">Hour</span></span>|   <span data-ttu-id="7cb9f-149">112</span><span class="sxs-lookup"><span data-stu-id="7cb9f-149">112</span></span>|<span data-ttu-id="7cb9f-150">USD</span><span class="sxs-lookup"><span data-stu-id="7cb9f-150">USD</span></span>     |


<span data-ttu-id="7cb9f-151">**Sampel kadar kos**</span><span class="sxs-lookup"><span data-stu-id="7cb9f-151">**Sample cost rates**</span></span>

| <span data-ttu-id="7cb9f-152">Jalur Gaji</span><span class="sxs-lookup"><span data-stu-id="7cb9f-152">Salary Band</span></span>     | <span data-ttu-id="7cb9f-153">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="7cb9f-153">Org Unit</span></span>    |<span data-ttu-id="7cb9f-154">Unit</span><span class="sxs-lookup"><span data-stu-id="7cb9f-154">Unit</span></span>      |<span data-ttu-id="7cb9f-155">Harga</span><span class="sxs-lookup"><span data-stu-id="7cb9f-155">Price</span></span>      |<span data-ttu-id="7cb9f-156">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="7cb9f-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="7cb9f-157">Syarikat saya_Jalur1</span><span class="sxs-lookup"><span data-stu-id="7cb9f-157">My company_Band1</span></span> | <span data-ttu-id="7cb9f-158">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="7cb9f-158">Contoso US</span></span>  |<span data-ttu-id="7cb9f-159">Hour</span><span class="sxs-lookup"><span data-stu-id="7cb9f-159">Hour</span></span> | <span data-ttu-id="7cb9f-160">145</span><span class="sxs-lookup"><span data-stu-id="7cb9f-160">145</span></span>|<span data-ttu-id="7cb9f-161">USD</span><span class="sxs-lookup"><span data-stu-id="7cb9f-161">USD</span></span>     |
| <span data-ttu-id="7cb9f-162">Syarikat saya_Jalur2</span><span class="sxs-lookup"><span data-stu-id="7cb9f-162">My company_Band2</span></span> | <span data-ttu-id="7cb9f-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="7cb9f-163">Contoso India</span></span> |<span data-ttu-id="7cb9f-164">Hour</span><span class="sxs-lookup"><span data-stu-id="7cb9f-164">Hour</span></span>|   <span data-ttu-id="7cb9f-165">67</span><span class="sxs-lookup"><span data-stu-id="7cb9f-165">67</span></span>|<span data-ttu-id="7cb9f-166">USD</span><span class="sxs-lookup"><span data-stu-id="7cb9f-166">USD</span></span>     |
