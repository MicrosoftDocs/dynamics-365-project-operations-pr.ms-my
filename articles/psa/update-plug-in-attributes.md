---
title: Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu
description: Topik ini memberikan maklumat mengenai mengemas kini atribut pasang masuk untuk dimensi penetapan.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281804"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="253b5-103">Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu</span><span class="sxs-lookup"><span data-stu-id="253b5-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="253b5-104">Jika anda tidak menggunakan ciri Pesanan Harga Project Service Automation (PSA) dan Pengkontrakan, anda boleh melangkau topik ini.</span><span class="sxs-lookup"><span data-stu-id="253b5-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="253b5-105">Topik ini menganggap bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai](create-custom-fields-entities.md), [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md) dan [Sediakan medan tersuai sebagai dimensi penetapan harga](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="253b5-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="253b5-106">Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini.</span><span class="sxs-lookup"><span data-stu-id="253b5-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="253b5-107">Apabila butiran baris sebut harga dicipta pada halaman baris **Baris Sebut Harga** untuk baris sebut harga projek, sistem mencipta dua baris anggaran dalam latar belakang -- satu baris untuk bahagian kos anggaran dan satu untuk jualan pihak.</span><span class="sxs-lookup"><span data-stu-id="253b5-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="253b5-108">Ini adalah sama untuk baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="253b5-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="253b5-109">Apabila anda membuat perubahan pada kuantiti atau medan pada bahagian kos, perubahan tersebut akan disebarkan ke bahagian jualan.</span><span class="sxs-lookup"><span data-stu-id="253b5-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="253b5-110">Ini mungkin kerana pasang berikut yang mesti didaftarkan semula selepas perubahan dimensi penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="253b5-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="253b5-111">PreOperationContractLineDetailUpdate- Kemas Kini **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="253b5-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="253b5-112">PreOperationQuoteLineDetailUpdate - Kemas Kini **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="253b5-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="253b5-113">Langkah berikut menerangkan tentang proses pendaftaran pasang masuk.</span><span class="sxs-lookup"><span data-stu-id="253b5-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="253b5-114">Buka **PluginRegistrationTool** dan sambung kepada tika dalam talian anda.</span><span class="sxs-lookup"><span data-stu-id="253b5-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="253b5-115">Klik **Cari** dan cari untuk pasang masuk dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="253b5-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Tangkapan skrin pepohon carian](media/PRT-1.png)

3. <span data-ttu-id="253b5-117">Selepas pasang masuk ditemui, pilihnya dan klik **Pilih pada Borang Utama**.</span><span class="sxs-lookup"><span data-stu-id="253b5-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="253b5-118">Pilih langkah pasang masuk untuk dikemas kini, klik kanan dan kemudian pilih **Kemas Kini**.</span><span class="sxs-lookup"><span data-stu-id="253b5-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Tangkapan skrin bagi pasang masuk yang akan dikemas kini](media/PRT-2.png)
 
5. <span data-ttu-id="253b5-120">Dalam tetingkap kemas kini, klik elsis (**...**) dalam atribut penapisan.</span><span class="sxs-lookup"><span data-stu-id="253b5-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Tangkapan skrin kemas kini langkah sedia ada maklumat konfigurasi](media/PRT-3.png)
 
6. <span data-ttu-id="253b5-122">Pilih kotak semak atribut penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="253b5-122">Select the pricing attribute check boxes.</span></span>

 ![Tangkapan skrin yang ditunjukkan pilihan kotak semak untuk atribut penetapan](media/PRT-4.png)

7. <span data-ttu-id="253b5-124">Klik **OK** untuk menutup halaman dan kemudian pilih **Kemas Kini Langkah**.</span><span class="sxs-lookup"><span data-stu-id="253b5-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Skrin menunjukkan butang “Langkah Kemas Kini”](media/PRT-5.png)
 
8. <span data-ttu-id="253b5-126">Ulang proses ini untuk pasang masuk kedua, **PreOperationQuoteLineDetail - Kemas Kini msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="253b5-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="253b5-127">Tutup alat pendaftaran pasang masuk.</span><span class="sxs-lookup"><span data-stu-id="253b5-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]