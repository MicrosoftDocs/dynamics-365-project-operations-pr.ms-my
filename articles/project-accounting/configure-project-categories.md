---
title: Konfigurasi kategori projek
description: Topik ini memberikan maklumat tentang menyediakan kategori projek.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131939"
---
# <a name="configure-project-categories"></a><span data-ttu-id="3d83b-103">Konfigurasi kategori projek</span><span class="sxs-lookup"><span data-stu-id="3d83b-103">Configure project categories</span></span>

<span data-ttu-id="3d83b-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="3d83b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d83b-105">Operasi Projek menawarkan keupayaan yang kukuh untuk mengkategorikan perolehan dan perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="3d83b-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="3d83b-106">Kategori ini menyediakan keupayaan untuk melaporkan dan menganalisis transaksi projek dan memandu ke lejar umum.</span><span class="sxs-lookup"><span data-stu-id="3d83b-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="3d83b-107">Gambarajah berikut menunjukkan korelasi antara kategori transaksi, kategori dikongsi dan kategori projek.</span><span class="sxs-lookup"><span data-stu-id="3d83b-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="3d83b-108">Kategori transaksi ialah kumpulan asas untuk transaksi projek.</span><span class="sxs-lookup"><span data-stu-id="3d83b-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="3d83b-109">Dalam kumpulan tersebut, terdapat beberapa set kategori dikongsi yang boleh dikongsi merentasi aplikasi dan modul.</span><span class="sxs-lookup"><span data-stu-id="3d83b-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="3d83b-110">Lebih lagi ke khusus, kategori projek ialah peringkat paling banyak butiran kategori.</span><span class="sxs-lookup"><span data-stu-id="3d83b-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="3d83b-111">Kategori projek khusus untuk entiti, modul dan aplikasi sah.</span><span class="sxs-lookup"><span data-stu-id="3d83b-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelasi antara kategori transaksi, kategori dikongsi dan kategori projek](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="3d83b-113">Kategori transaksi</span><span class="sxs-lookup"><span data-stu-id="3d83b-113">Transaction categories</span></span>

<span data-ttu-id="3d83b-114">Kategori transaksi mewakili kumpulan asas untuk transaksi projek dan bukan khusus syarikat atau transaksi jenis.</span><span class="sxs-lookup"><span data-stu-id="3d83b-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="3d83b-115">Sebagai contoh, Contoso Robotics menggunakan kategori Reka bentuk, Perjalanan, Pemasangan dan Transaksi Perkhidmatan kepada transaksi Projek kumpulan.</span><span class="sxs-lookup"><span data-stu-id="3d83b-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="3d83b-116">Kategori transaksi ditakrifkan dalam modul Operasi Projek.</span><span class="sxs-lookup"><span data-stu-id="3d83b-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="3d83b-117">Pergi ke **Tetapan** \> **Kategori Transaksi** untuk membuka borang.</span><span class="sxs-lookup"><span data-stu-id="3d83b-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="3d83b-118">Cipta kategori transaksi baharu sama ada dengan memilih **Baharu** atau dengan memilih **Import dari Excel**.</span><span class="sxs-lookup"><span data-stu-id="3d83b-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="3d83b-119">Kategori dikongsi</span><span class="sxs-lookup"><span data-stu-id="3d83b-119">Shared categories</span></span>

<span data-ttu-id="3d83b-120">Dynamics 365 menggunakan konsep kategori dikongsi untuk categorize perbelanjaan dalam aplikasi yang berbeza, seperti Dynamics 365 Finance, rantaian bekalan Dynamics 365 dan Operasi Projek Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3d83b-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="3d83b-121">Bagi setiap kategori transaksi yang dicipta, Operasi Projek secara automatik mencipta empat kategori dikongsi yang berkaitan: Jam, Perbelanjaan, Yuran dan Item.</span><span class="sxs-lookup"><span data-stu-id="3d83b-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="3d83b-122">Anda boleh menyemak dan melaraskan kategori dikongsi dengan pergi ke kategori **Pengurusan projek dan tetapan perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori Dikongsi**.</span><span class="sxs-lookup"><span data-stu-id="3d83b-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="3d83b-123">Kategori produk</span><span class="sxs-lookup"><span data-stu-id="3d83b-123">Project categories</span></span>

<span data-ttu-id="3d83b-124">Kategori projek mewakili paling banyak butiran konfigurasi kategori dan mesti dikonfigurasikan secara berasingan dan untuk setiap syarikat, oleh Akauntan projek.</span><span class="sxs-lookup"><span data-stu-id="3d83b-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="3d83b-125">Pergi ke **Pengurusan Projek dan Perakaunan** \> **Tetapan** \> **Kategori** \> **Kategori projek**.</span><span class="sxs-lookup"><span data-stu-id="3d83b-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="3d83b-126">Pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="3d83b-126">Select **New**.</span></span>
3. <span data-ttu-id="3d83b-127">Pilih **ID kategori** bagi kategori Dikongsi yang anda cipta dalam bahagian sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="3d83b-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="3d83b-128">Operasi Projek membenarkan hanya menggunakan kategori dikongsi yang berkaitan dengan kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="3d83b-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="3d83b-129">Pilih kumpulan kategori.</span><span class="sxs-lookup"><span data-stu-id="3d83b-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="3d83b-130">Kumpulan kategori</span><span class="sxs-lookup"><span data-stu-id="3d83b-130">Category groups</span></span>

<span data-ttu-id="3d83b-131">Kumpulan kategori digunakan untuk berkongsi sifat, terutamanya menyiarkan profil, antara kategori Projek yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="3d83b-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="3d83b-132">Mesti ada sekurang-kurangnya satu kumpulan kategori untuk setiap jenis transaksi dan setiap kategori projek ditugaskan satu kumpulan.</span><span class="sxs-lookup"><span data-stu-id="3d83b-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="3d83b-133">Spesifikasi dalam Operasi Projek ditakrifkan oleh peraturan profil kos projek dan hasil, kategori projek dan kumpulan kategori.</span><span class="sxs-lookup"><span data-stu-id="3d83b-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="3d83b-134">Anda boleh menyediakan kumpulan kategori dengan pergi ke **Pengurusan projek dan perakaunan** \> **Tetapan** \> **Kategori** \> **Kumpulan kategori**.</span><span class="sxs-lookup"><span data-stu-id="3d83b-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
