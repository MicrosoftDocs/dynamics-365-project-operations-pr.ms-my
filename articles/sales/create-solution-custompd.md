---
title: Cipta penyelesaian untuk dimensi penentuan harga tersuai
description: Topik ini memberikan maklumat tentang cara mencipta penyelesaian untuk dimensi penentuan harga tersuai.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010347"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6c8f7-103">Cipta penyelesaian untuk dimensi penentuan harga tersuai</span><span class="sxs-lookup"><span data-stu-id="6c8f7-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="6c8f7-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="6c8f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="6c8f7-105">Semua perubahan dimensi penetapan harga tersuai hendaklah dalam penyelesaian yang berasingan.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="6c8f7-106">Amalan terbaik yang penting ini membolehkan fleksibiliti untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, membantu dengan menggunakan semula kerja anda dan dan menjadikan ia lebih mudah untuk port perubahan ini kepada tika lain.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="6c8f7-107">Selepas anda membuat semua perubahan yang diperlukan, eksport penyelesaian ini sebagai penyelesaian **Terurus** dan kemudian import ke dalam tika lain untuk penggunaan semula.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6c8f7-108">Cipta penyelesaian untuk dimensi penentuan harga tersuai</span><span class="sxs-lookup"><span data-stu-id="6c8f7-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="6c8f7-109">Pilih **Tetapan** > **Penyelesaian**, dan kemudian pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="6c8f7-110">Namakan penyelesaian, *Dimensi penentuan harga <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="6c8f7-111">Masukkan baki maklumat diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Penciptaan penyelesaian dimensi penentuan harga tersuai](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="6c8f7-113">Tambah semua entiti yang diperlukan dan dokumen berkaitan pada penyelesaian dimensi Penetapan Harga</span><span class="sxs-lookup"><span data-stu-id="6c8f7-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="6c8f7-114">Tambah entiti Project Service yang berikut kepada penyelesaian penentuan harga anda untuk membuat perubahan skema yang penting dalam penyelesaian penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="6c8f7-115">Selepas anda melengkapkan prosedur ini, entiti akan mengenali dimensi penentuan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="6c8f7-116">Pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **dimensi penentuan harga <*nama organisasi anda*>**.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="6c8f7-117">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="6c8f7-118">Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="6c8f7-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="6c8f7-119">**Sebenar**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-119">**Actual**</span></span>
   - <span data-ttu-id="6c8f7-120">**Sumber Boleh Ditempah**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="6c8f7-121">**Garisan Anggaran**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-121">**Estimate Line**</span></span>
   - <span data-ttu-id="6c8f7-122">**Tugas Projek**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-122">**Project Task**</span></span>
   - <span data-ttu-id="6c8f7-123">**Butiran Baris Invois**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="6c8f7-124">**Garisan Jurnal**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-124">**Journal Line**</span></span>
   - <span data-ttu-id="6c8f7-125">**Butiran Baris Kontrak Projek**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="6c8f7-126">**Ahli Pasukan Projek**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-126">**Project Team Member**</span></span>
   - <span data-ttu-id="6c8f7-127">**Butiran Baris Sebut Harga**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="6c8f7-128">**Tokokan Harga Peranan**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="6c8f7-129">**Harga Peranan**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-129">**Role Price**</span></span>
   - <span data-ttu-id="6c8f7-130">**Entri Masa**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-130">**Time Entry**</span></span>
 
   ![Tambah entiti sedia ada untuk penyelesaian dimensi penentuan harga tersuai](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="6c8f7-132">Bagi setiap entiti, semak komponen yang ditambah dan senarai akhir aset entiti untuk setiap entiti.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="6c8f7-133">Sertakan semua borang dan pandangan bagi setiap entiti yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="6c8f7-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entiti ditambah](./media/solution-component-selection.png)


5.  <span data-ttu-id="6c8f7-135">Apabila digesa untuk menyertakan sebarang entiti sandaran untuk entiti yang dipilih, pilih **Tidak, jangan sertakan komponen diperlukan.**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Termasuk entiti sandaran](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]