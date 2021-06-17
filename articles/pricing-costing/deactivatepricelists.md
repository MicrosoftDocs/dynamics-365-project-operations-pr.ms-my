---
title: Nyahaktifkan senarai harga
description: Topik ini menerangkan cara menyahaktifkan atau mengalih keluar senarai harga yang tidak digunakan atau lama.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001347"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="658d4-103">Nyahaktifkan senarai harga</span><span class="sxs-lookup"><span data-stu-id="658d4-103">Deactivate price lists</span></span> 

<span data-ttu-id="658d4-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="658d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="658d4-105">Untuk mengalih keluar senarai harga yang lama atau tidak digunakan daripada Dynamics 365 Project Operations, terdapat dua langkah yang mesti anda lengkapkan.</span><span class="sxs-lookup"><span data-stu-id="658d4-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="658d4-106">Alih keluar atau padamkan senarai harga daripada halaman tertentu.</span><span class="sxs-lookup"><span data-stu-id="658d4-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="658d4-107">Nyahaktifkan atau padamkan senarai harga daripada Senarai harga aktif pada halaman **Senarai Harga**.</span><span class="sxs-lookup"><span data-stu-id="658d4-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="658d4-108">Anda mesti melengkapkan kedua-dua langkah untuk mengalih keluar senarai harga sepenuhnya.</span><span class="sxs-lookup"><span data-stu-id="658d4-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="658d4-109">Hanya melakukan langkah 2, iaitu memadam atau menyahaktifkan senarai harga secara terus daripada pandangan Senarai Harga Aktif, tidak mencukupi.</span><span class="sxs-lookup"><span data-stu-id="658d4-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="658d4-110">Anda juga mesti memadamkan perkaitan senarai harga ini daripada semua tempat yang dinyatakan dalam langkah 1.</span><span class="sxs-lookup"><span data-stu-id="658d4-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="658d4-111">Padamkan senarai harga daripada halaman tertentu</span><span class="sxs-lookup"><span data-stu-id="658d4-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="658d4-112">Untuk memadamkan senarai harga daripada Project Operations, pergi ke halaman berikut:</span><span class="sxs-lookup"><span data-stu-id="658d4-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="658d4-113">Halaman **Parameter projek** > tab **Senarai Harga**</span><span class="sxs-lookup"><span data-stu-id="658d4-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="658d4-114">Halaman **Unit Organisasi** > grid **Senarai Harga**</span><span class="sxs-lookup"><span data-stu-id="658d4-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="658d4-115">Halaman **Akaun** > grid **Senarai Harga Projek**</span><span class="sxs-lookup"><span data-stu-id="658d4-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="658d4-116">Halaman **Sebut Harga Projek** > grid **Senarai Harga Projek**: Ini digunakan pada semua sebut harga projek aktif.</span><span class="sxs-lookup"><span data-stu-id="658d4-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="658d4-117">Halaman **Kontrak Projek** > grid **Senarai Harga Projek**: Ini digunakan pada semua kontrak projek aktif.</span><span class="sxs-lookup"><span data-stu-id="658d4-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="658d4-118">Untuk setiap halaman, anda perlu memilih senarai harga yang anda mahu padamkan, dan kemudian pilih **Padam**.</span><span class="sxs-lookup"><span data-stu-id="658d4-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="658d4-119">Padamkan atau nyahaktifkan senarai harga daripada halaman Senarai Harga</span><span class="sxs-lookup"><span data-stu-id="658d4-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="658d4-120">Untuk memadamkan senarai harga daripada senarai harga aktif, pergi ke **Jualan** > **Pelanggan** > **Senarai Harga**.</span><span class="sxs-lookup"><span data-stu-id="658d4-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="658d4-121">Pilih senarai harga yang anda mahu padamkan untuk memadamkan dan kemudian pilih **Padam**.</span><span class="sxs-lookup"><span data-stu-id="658d4-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="658d4-122">Jika senarai harga dirujuk pada sebarang transaksi sedia ada, anda tidak akan dapat memadamkannya.</span><span class="sxs-lookup"><span data-stu-id="658d4-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="658d4-123">Jika ini berlaku, anda boleh menyahaktifkan senarai harga supaya ia tidak muncul dalam sebarang pandangan.</span><span class="sxs-lookup"><span data-stu-id="658d4-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="658d4-124">Untuk menyahaktifkan senarai harga, pilih senarai harga sekali lagi, dan kemudian pilih **Nyahaktifkan**.</span><span class="sxs-lookup"><span data-stu-id="658d4-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
