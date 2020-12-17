---
title: Kemas kini atribut pasang masuk dengan dimensi penentuan harga baharu
description: Topik ini memberikan maklumat tentang cara mengemas kini atribut pasang masuk untuk dimensi penentuan harga.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643229"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="3e1c4-103">Kemas kini atribut pasang masuk dengan dimensi penentuan harga baharu</span><span class="sxs-lookup"><span data-stu-id="3e1c4-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="3e1c4-104">Topik ini memberikan maklumat tentang cara mengemas kini atribut pasang masuk untuk dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3e1c4-105">Topik ini hanya digunakan untuk sebut harga dan ciri kontrak dalam Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e1c4-106">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="3e1c4-106">Prerequisites</span></span>
<span data-ttu-id="3e1c4-107">Sebelum anda melengkapkan langkah dalam topik ini, anda mesti melengkapkan prosedur dalam topik berikut:</span><span class="sxs-lookup"><span data-stu-id="3e1c4-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="3e1c4-108">Cipta medan dan entiti tersuai</span><span class="sxs-lookup"><span data-stu-id="3e1c4-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="3e1c4-109">Tambah medan tersuai kepada persediaan harga dan entiti transaksi </span><span class="sxs-lookup"><span data-stu-id="3e1c4-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="3e1c4-110">[Sediakan medan tersuai sebagai dimensi penentuan harga](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3e1c4-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="3e1c4-111">Jika anda belum melengkapkan prosedur tersebut, lengkapkannya dan kemudian kembali ke topik ini.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="3e1c4-112">Daftarkan pasang masuk</span><span class="sxs-lookup"><span data-stu-id="3e1c4-112">Register a plug-in</span></span>
<span data-ttu-id="3e1c4-113">Apabila butiran baris sebut harga dicipta pada halaman **Baris Sebut Harga** untuk baris sebut harga projek, sistem mencipta dua baris anggaran.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="3e1c4-114">Satu baris adalah untuk bahagian kos anggaran dan baris lain untuk bahagian jualan.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="3e1c4-115">Ini adalah sama untuk baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3e1c4-116">Apabila anda membuat perubahan pada kuantiti atau medan pada bahagian kos, perubahan tersebut juga dibuat pada bahagian jualan.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="3e1c4-117">Ini berlaku kerana pasang masuk PreOperation pada Quotelinedetail dan entiti butiran baris kontrak menghubungkan atribut tertentu pada bahagian kos kepada bahagian jualan transaksi.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="3e1c4-118">Jika anda memerlukan perubahan yang dibuat pada nilai dimensi penentuan harga pada bahagian jualan juga dibuat pada bahagian kos, pasang masuk berikut mesti didaftarkan semula selepas membuat perubahan pada dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="3e1c4-119">Ini ialah pasang masuk untuk dikemas kini dan didaftar semula:</span><span class="sxs-lookup"><span data-stu-id="3e1c4-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="3e1c4-120">PreOperationContractLineDetailUpdate - **Kemas kini msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3e1c4-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="3e1c4-121">PreOperationQuoteLineDetailUpdate - **Kemas kini msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="3e1c4-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="3e1c4-122">Lengkapkan langkah berikut untuk mengemas kini dan mendaftar semula pasang masuk.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="3e1c4-123">Buka **PluginRegistrationTool** dan sambung ke persekitaran Project Operations Dataverse anda.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="3e1c4-124">Pilih **Cari** dan taip beberapa huruf pertama bagi pasang masuk yang akan dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="3e1c4-125">Selepas pasang masuk ditemui, pilihnya dan pilih **Pilih pada Borang Utama**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="3e1c4-126">Pilih langkah **Kemas kini msdyn_orderlinetransaction**, klik kanan dan kemudian pilih **Kemas kini**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="3e1c4-127">Dalam halaman dialog **Kemas kini**, pilih elipsis (**...**) dalam atribut penapisan.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="3e1c4-128">Tetingkap atribut penapisan dibuka dan menyediakan senarai semua atribut dalam entiti dan dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="3e1c4-129">Pilih kotak semak untuk atribut dimensi penentuan harga.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="3e1c4-130">Pilih **OK** untuk menutup halaman dan kemudian pilih **Kemas Kini Langkah**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="3e1c4-131">Ulangan langkah 2-7 untuk pasang masuk kedua, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="3e1c4-132">Untuk pasang masuk ini, anda perlu mengemas kini langkah **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="3e1c4-133">Tutup **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="3e1c4-133">Close **PluginRegistrationTool**.</span></span>
