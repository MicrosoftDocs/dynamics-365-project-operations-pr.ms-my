---
title: Unit dan kumpulan unit
description: Topik ini menyediakan maklumat tentang cara mencipta unit dan kumpulan unit dalam Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277349"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="53943-103">Unit dan kumpulan unit</span><span class="sxs-lookup"><span data-stu-id="53943-103">Units and unit groups</span></span>

<span data-ttu-id="53943-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="53943-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53943-105">Unit ialah kuantiti atau ukuran yang anda gunakan untuk menjual produk atau perkhidmatan anda.</span><span class="sxs-lookup"><span data-stu-id="53943-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="53943-106">Sebagai contoh, jika anda menjual bekalan berkebun, anda mungkin menjual benih dalam unit paket, kotak dan palet.</span><span class="sxs-lookup"><span data-stu-id="53943-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="53943-107">Kumpulan unit ini ialah koleksi unit yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="53943-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="53943-108">Untuk melengkapkan langkah dalam topik ini, pastikan anda ditugaskan kepada Pentadbir Sistem atau peranan Pengurus Sales Professional atau mempunyai keizinan setara.</span><span class="sxs-lookup"><span data-stu-id="53943-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="53943-109">Cipta kumpulan unit</span><span class="sxs-lookup"><span data-stu-id="53943-109">Create a unit group</span></span>

1. <span data-ttu-id="53943-110">Dalam peta tapak, pilih **Unit**.</span><span class="sxs-lookup"><span data-stu-id="53943-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="53943-111">Pilih **Baharu** dan dalam kotak dialog **Cipta Kumpulan Unit**, masukkan nama unit.</span><span class="sxs-lookup"><span data-stu-id="53943-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="53943-112">Medan **Unit utama**, masukkan unit ukuran lazim terendah yang akan digunakan dalam jualan produk.</span><span class="sxs-lookup"><span data-stu-id="53943-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="53943-113">Contohnya, anda mungkin memasukkan "potongan" atau "auns".</span><span class="sxs-lookup"><span data-stu-id="53943-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="53943-114">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="53943-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="53943-115">Tambah unit ke kumpulan unit</span><span class="sxs-lookup"><span data-stu-id="53943-115">Add units to a unit group</span></span>

1. <span data-ttu-id="53943-116">Buka kumpulan unit dan pada tab **Berkaitan**, pilih **Unit**.</span><span class="sxs-lookup"><span data-stu-id="53943-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="53943-117">Anda akan melihat unit utama telah ditambah.</span><span class="sxs-lookup"><span data-stu-id="53943-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="53943-118">Pilih **Tambah Unit Baharu** dan pada halaman **Cipta Pantas: Unit**, dalam medan **Nama**, masukkan nama unit.</span><span class="sxs-lookup"><span data-stu-id="53943-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="53943-119">Dalam medan **Kuantiti**, masukkan kuantiti bagi unit.</span><span class="sxs-lookup"><span data-stu-id="53943-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="53943-120">Contohnya, jika kotak mengandungi dua bahagian, masukkan "2".</span><span class="sxs-lookup"><span data-stu-id="53943-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="53943-121">Dalam medan **Unit Asas**, pilih unit asas untuk mewujudkan unit terendah bagi ukuran unit.</span><span class="sxs-lookup"><span data-stu-id="53943-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="53943-122">Contohnya, anda mungkin memilih "Bahagian".</span><span class="sxs-lookup"><span data-stu-id="53943-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="53943-123">Pilih **Simpan**:</span><span class="sxs-lookup"><span data-stu-id="53943-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]