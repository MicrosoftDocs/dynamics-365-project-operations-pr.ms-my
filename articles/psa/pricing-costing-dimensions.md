---
title: Halaman utama dimensi penetapan harga dan kos
description: Topik ini memberikan gambaran keseluruhan dimensi penetapan harga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081269"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="099e4-103">Halaman utama dimensi penetapan harga dan kos</span><span class="sxs-lookup"><span data-stu-id="099e4-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="099e4-104">Dimensi yang digunakan untuk menetapkan harga buruh dan kos dalam organisasi berasaskan projek dipengaruhi oleh atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="099e4-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="099e4-105">Orang yang melakukan kerja sama seperti pengalaman, peranan atau</span><span class="sxs-lookup"><span data-stu-id="099e4-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="099e4-106">Kerja yang perlu dilakukan sama dengan kerumitan atau masa siang</span><span class="sxs-lookup"><span data-stu-id="099e4-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="099e4-107">Memandangkan sifat tipikal ini atribut kerja dan orang yang diperlukan untuk melaksanakan kerja, terdapat dua jenis nilai dimensi penetapan harga yang tersedia dalam Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="099e4-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="099e4-108">**Set pilihan** : Atribut yang merupakan penghitungan tetap bagi set nilai.</span><span class="sxs-lookup"><span data-stu-id="099e4-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="099e4-109">**Nilai berasaskan entiti** - Atribut yang boleh mempunyai pelbagai set nilai yang terhad tetapi boleh berubah dari semasa ke semasa.</span><span class="sxs-lookup"><span data-stu-id="099e4-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="099e4-110">Dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="099e4-110">Pricing dimensions</span></span>

<span data-ttu-id="099e4-111">Kapal PSA dengan set dimensi penetapan harga lalai.</span><span class="sxs-lookup"><span data-stu-id="099e4-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="099e4-112">Anda boleh melihat ini dengan pergi ke **Project Service** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="099e4-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="099e4-113">Dalam rekod parameter, pada tab **Dimensi penetapan harga berdasarkan jumlah** , sahkan bahawa peranan, **msdyn_resourcecategory** dan unit organisasi sumber, **msdyn_organizationalunit** mempunyai medan **Digunakan pada jualan** dan **Digunakan pada kos** yang ditetapkan kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="099e4-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="099e4-114">Ini akan membolehkan anda menyediakan harga dan kos untuk setiap peranan dan gabungan unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="099e4-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Petikan skrin parameter Project Service dengan "Digunakan pada Jualan" diserlahkan](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="099e4-116">Jika anda telah menggunakan medan peranan siap guna dan unit organisasi sebagai dimensi penetapan harga sebelum versi 3 PSA, tidak akan ada perubahan yang dapat dilihat.</span><span class="sxs-lookup"><span data-stu-id="099e4-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="099e4-117">Anda boleh terus menggunakan Project Service seperti biasa.</span><span class="sxs-lookup"><span data-stu-id="099e4-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="099e4-118">Jika anda perlukan harga atau kos untuk sumber anda menggunakan atribut tambahan, anda boleh mencipta medan, entiti dan dimensi tersuai.</span><span class="sxs-lookup"><span data-stu-id="099e4-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="099e4-119">Untuk mendapatkan maklumat lanjut, lihat topik berikut, walau bagaimanapun, sila ambil perhatian bahawa anda mesti melengkapkan prosedur dalam dalam pesanan yang disenaraikan di bawah:</span><span class="sxs-lookup"><span data-stu-id="099e4-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="099e4-120">Cipta medan dan entiti tersuai</span><span class="sxs-lookup"><span data-stu-id="099e4-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="099e4-121">Tambah medan tersuai kepada persediaan harga dan entiti transaksi</span><span class="sxs-lookup"><span data-stu-id="099e4-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="099e4-122">Sediakan medan tersuai sebagai dimensi penetapan harga </span><span class="sxs-lookup"><span data-stu-id="099e4-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="099e4-123">Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu</span><span class="sxs-lookup"><span data-stu-id="099e4-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="099e4-124">Masa penetapan harga sumber manusia</span><span class="sxs-lookup"><span data-stu-id="099e4-124">Pricing human resource time</span></span>
<span data-ttu-id="099e4-125">Cara sebuah organisasi menilai masa sumber manusia sering menjadi pertimbangan strategik yang penting yang secara langsung mempengaruhi keuntungan organisasi.</span><span class="sxs-lookup"><span data-stu-id="099e4-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="099e4-126">Bekerja dengan pasukan kewangan dan ketua latihan apabila organisasi anda bersedia untuk mengenal pasti cara ia mahu menyediakan kadar bil dan kos untuk masa sumber manusia.</span><span class="sxs-lookup"><span data-stu-id="099e4-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="099e4-127">Pertimbangan lain untuk penetapan harga termasuk sama ada untuk menggunakan semula medan atau entiti yang bukan pada masa ini dimensi penetapan harga tetapi digunakan sebagai dimensi penetapan harga untuk organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="099e4-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="099e4-128">Medan seperti **Kategori Transaksi** ( **msdyn_transactioncategory** ) dan **Sumber Boleh Ditempah** ( **bookableresource** ) ialah contoh dimensi calon.</span><span class="sxs-lookup"><span data-stu-id="099e4-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="099e4-129">Pertimbangkan sama ada dimensi penetapan harga anda mesti jadual atau set pilihan.</span><span class="sxs-lookup"><span data-stu-id="099e4-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="099e4-130">Jika anda meramalkan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan ke atas nilai ini, cipta entiti dan bukannya set pilihan.</span><span class="sxs-lookup"><span data-stu-id="099e4-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="099e4-131">Mengekalkan set pilihan, seperti menambah atau mengalih keluar nilai, memerlukan pentadbir atau pembangun, manakala menambah baris baru pada jadual boleh dilakukan oleh kebanyakan pengguna perniagaan.</span><span class="sxs-lookup"><span data-stu-id="099e4-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="099e4-132">Contoh berikut menunjukkan kadar bil yang ditetapkan berdasarkan peranan dan unit organisasi sumber yang sumbernya dimiliki.</span><span class="sxs-lookup"><span data-stu-id="099e4-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="099e4-133">Kadar kos biasanya berdasarkan pada jalur gaji pekerja dan unit organisasi yang mereka tergolong.</span><span class="sxs-lookup"><span data-stu-id="099e4-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="099e4-134">Dalam contoh ini, jadual kadar bil dan kadar kos akan kelihatan seperti berikut.</span><span class="sxs-lookup"><span data-stu-id="099e4-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="099e4-135">**Sampel kadar bil**</span><span class="sxs-lookup"><span data-stu-id="099e4-135">**Sample bill rates**</span></span>

| <span data-ttu-id="099e4-136">Peranan</span><span class="sxs-lookup"><span data-stu-id="099e4-136">Role</span></span>        | <span data-ttu-id="099e4-137">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="099e4-137">Org Unit</span></span>    |<span data-ttu-id="099e4-138">Unit</span><span class="sxs-lookup"><span data-stu-id="099e4-138">Unit</span></span>      |<span data-ttu-id="099e4-139">Harga</span><span class="sxs-lookup"><span data-stu-id="099e4-139">Price</span></span>      |<span data-ttu-id="099e4-140">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="099e4-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="099e4-141">Pembangun</span><span class="sxs-lookup"><span data-stu-id="099e4-141">Developer</span></span>   | <span data-ttu-id="099e4-142">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="099e4-142">Contoso US</span></span>  |<span data-ttu-id="099e4-143">Hour</span><span class="sxs-lookup"><span data-stu-id="099e4-143">Hour</span></span> | <span data-ttu-id="099e4-144">200</span><span class="sxs-lookup"><span data-stu-id="099e4-144">200</span></span>|<span data-ttu-id="099e4-145">USD</span><span class="sxs-lookup"><span data-stu-id="099e4-145">USD</span></span>     |
| <span data-ttu-id="099e4-146">Pembangun</span><span class="sxs-lookup"><span data-stu-id="099e4-146">Developer</span></span>   | <span data-ttu-id="099e4-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="099e4-147">Contoso India</span></span> |<span data-ttu-id="099e4-148">Hour</span><span class="sxs-lookup"><span data-stu-id="099e4-148">Hour</span></span>|   <span data-ttu-id="099e4-149">112</span><span class="sxs-lookup"><span data-stu-id="099e4-149">112</span></span>|<span data-ttu-id="099e4-150">USD</span><span class="sxs-lookup"><span data-stu-id="099e4-150">USD</span></span>     |


<span data-ttu-id="099e4-151">**Sampel kadar kos**</span><span class="sxs-lookup"><span data-stu-id="099e4-151">**Sample cost rates**</span></span>

| <span data-ttu-id="099e4-152">Jalur Gaji</span><span class="sxs-lookup"><span data-stu-id="099e4-152">Salary Band</span></span>     | <span data-ttu-id="099e4-153">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="099e4-153">Org Unit</span></span>    |<span data-ttu-id="099e4-154">Unit</span><span class="sxs-lookup"><span data-stu-id="099e4-154">Unit</span></span>      |<span data-ttu-id="099e4-155">Harga</span><span class="sxs-lookup"><span data-stu-id="099e4-155">Price</span></span>      |<span data-ttu-id="099e4-156">Mata Wang</span><span class="sxs-lookup"><span data-stu-id="099e4-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="099e4-157">Syarikat saya_Jalur1</span><span class="sxs-lookup"><span data-stu-id="099e4-157">My company_Band1</span></span> | <span data-ttu-id="099e4-158">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="099e4-158">Contoso US</span></span>  |<span data-ttu-id="099e4-159">Hour</span><span class="sxs-lookup"><span data-stu-id="099e4-159">Hour</span></span> | <span data-ttu-id="099e4-160">145</span><span class="sxs-lookup"><span data-stu-id="099e4-160">145</span></span>|<span data-ttu-id="099e4-161">USD</span><span class="sxs-lookup"><span data-stu-id="099e4-161">USD</span></span>     |
| <span data-ttu-id="099e4-162">Syarikat saya_Jalur2</span><span class="sxs-lookup"><span data-stu-id="099e4-162">My company_Band2</span></span> | <span data-ttu-id="099e4-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="099e4-163">Contoso India</span></span> |<span data-ttu-id="099e4-164">Hour</span><span class="sxs-lookup"><span data-stu-id="099e4-164">Hour</span></span>|   <span data-ttu-id="099e4-165">67</span><span class="sxs-lookup"><span data-stu-id="099e4-165">67</span></span>|<span data-ttu-id="099e4-166">USD</span><span class="sxs-lookup"><span data-stu-id="099e4-166">USD</span></span>     |
