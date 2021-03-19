---
title: Cipta penyelesaian tersuai untuk dimensi penentuan harga
description: Topik ini menerangkan cara untuk mencipta penyelesaian tersuai apabila membuat dimensi penetapan harga tersuai.
author: Rumant
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284999"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="1ee17-103">Cipta penyelesaian tersuai untuk dimensi penentuan harga</span><span class="sxs-lookup"><span data-stu-id="1ee17-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="1ee17-104">Semua perubahan dimensi penetapan harga tersuai hendaklah dalam penyelesaian yang berasingan.</span><span class="sxs-lookup"><span data-stu-id="1ee17-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="1ee17-105">Amalan terbaik penting ini memberikan kefleksibelan pada masa akan datang untuk mengemas kini atau mengalih keluar perubahan seperti yang diperlukan, akan membantu menggunakan semula kerja anda, dan memudahkan untuk port perubahan ini kepada tika lain.</span><span class="sxs-lookup"><span data-stu-id="1ee17-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="1ee17-106">Selepas anda membuat perubahan yang diperlukan, eksport penyelesaian ini sebagai **Penyelesaian terurus** dan import ini ke dalam tika lain untuk guna semula persediaan penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="1ee17-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="1ee17-107">Pilih **Tetapan** > **Penyelesaian**, dan kemudian pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="1ee17-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="1ee17-108">Namakan penyelesaian, **\<your organization name> dimensi penetapan harga**, masukkan baki maklumat yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="1ee17-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Mencipta penyelesaian tersuai untuk dimensi penentuan harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="1ee17-110">Tambah semua entiti yang diperlukan dan dokumen berkaitan pada penyelesaian dimensi Penetapan Harga</span><span class="sxs-lookup"><span data-stu-id="1ee17-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="1ee17-111">Anda perlu menambah entiti Project Service berikut pada penyelesaian penentuan harga anda.</span><span class="sxs-lookup"><span data-stu-id="1ee17-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="1ee17-112">Lengkapkan langkah-langkah dalam prosedur ini untuk membuat perubahan penting dalam penyelesaian penentuan harga agar entiti maklum dengan dimensi penentuan harga baharu.</span><span class="sxs-lookup"><span data-stu-id="1ee17-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="1ee17-113">Pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.</span><span class="sxs-lookup"><span data-stu-id="1ee17-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="1ee17-114">Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Tambah Sedia Ada** > **Entiti**.</span><span class="sxs-lookup"><span data-stu-id="1ee17-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="1ee17-115">Dalam kotak dialog **Komponen Penyelesaian**, pilih entiti berikut:</span><span class="sxs-lookup"><span data-stu-id="1ee17-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="1ee17-116">Sebenar</span><span class="sxs-lookup"><span data-stu-id="1ee17-116">Actual</span></span>
- <span data-ttu-id="1ee17-117">Sumber Boleh Ditempah</span><span class="sxs-lookup"><span data-stu-id="1ee17-117">Bookable Resource</span></span>
- <span data-ttu-id="1ee17-118">Garisan Anggaran</span><span class="sxs-lookup"><span data-stu-id="1ee17-118">Estimate Line</span></span>
- <span data-ttu-id="1ee17-119">Tugas Projek</span><span class="sxs-lookup"><span data-stu-id="1ee17-119">Project Task</span></span>
- <span data-ttu-id="1ee17-120">Butiran Baris Invois</span><span class="sxs-lookup"><span data-stu-id="1ee17-120">Invoice Line Detail</span></span>
- <span data-ttu-id="1ee17-121">Garisan Jurnal</span><span class="sxs-lookup"><span data-stu-id="1ee17-121">Journal Line</span></span>
- <span data-ttu-id="1ee17-122">Butiran Baris Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="1ee17-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="1ee17-123">Ahli Pasukan Projek</span><span class="sxs-lookup"><span data-stu-id="1ee17-123">Project Team Member</span></span>
- <span data-ttu-id="1ee17-124">Butiran Baris Sebut Harga</span><span class="sxs-lookup"><span data-stu-id="1ee17-124">Quote Line Detail</span></span>
- <span data-ttu-id="1ee17-125">Tokokan Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="1ee17-125">Role Price Markup</span></span>
- <span data-ttu-id="1ee17-126">Harga Peranan</span><span class="sxs-lookup"><span data-stu-id="1ee17-126">Role Price</span></span> 
- <span data-ttu-id="1ee17-127">Entri Masa</span><span class="sxs-lookup"><span data-stu-id="1ee17-127">Time Entry</span></span> 

> ![Tambah entiti sedia ada untuk penyelesaian dimensi penentuan harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen penyelesaian](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="1ee17-130">Pastikan anda memasukkan semua borang dan pandangan bagi setiap entiti yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="1ee17-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="1ee17-131">Apabila digesa untuk memasukkan sebarang entiti bersandar bagi entiti yang dipilih, pilih **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="1ee17-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Jangan masukkan semua komponen berkaitan](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]