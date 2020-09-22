---
title: Naik taraf laman utama
description: Topik ini menunjukkan di mana untuk mencari maklumat penting mengenai ciri baharu dan diubah dalam Dynamics 365 Project Service Automation dan proses untuk menaik taraf kepada versi terbaharu.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753941"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="1db42-103">Naik taraf laman utama</span><span class="sxs-lookup"><span data-stu-id="1db42-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="1db42-104">Naik taraf daripada versi PSA 2.x atau 1.x kepada versi 3.x</span><span class="sxs-lookup"><span data-stu-id="1db42-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="1db42-105">Tika baharu</span><span class="sxs-lookup"><span data-stu-id="1db42-105">New instances</span></span>

<span data-ttu-id="1db42-106">Pada 17 Mei 2019, apabila Project Service Automation dipilih semasa peruntukan tika baharu, versi 3.x dipasang secara lalai.</span><span class="sxs-lookup"><span data-stu-id="1db42-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="1db42-107">Tika sedia ada</span><span class="sxs-lookup"><span data-stu-id="1db42-107">Existing instances</span></span>

<span data-ttu-id="1db42-108">Sebelum ini, pelanggan yang mempunyai tika PSA versi 2. x dan perlu menaik taraf kepada versi 3.x, yang merupakan versi Berasaskan antara muka klien disatukan (UCI) bagi PSA, mesti menghubungi Sokongan Microsoft dan menyediakan butiran tika mereka, supaya sokongan boleh mendayakan tika bagi naik taraf kepada versi 3.x.</span><span class="sxs-lookup"><span data-stu-id="1db42-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="1db42-109">Pada 1 Mac 2020, pelanggan yang mempunyai tika PSA versi 2.x dan perlu menaik taraf kepada versi 3.x, akan dapat menaik taraf tika mereka secara terus daripada portal Pentadbir tanpa perlu menghubungi Sokongan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1db42-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="1db42-110">PSA versi 3.x termasuk perubahan ketara.</span><span class="sxs-lookup"><span data-stu-id="1db42-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="1db42-111">Ia telah dibina pada rangka kerja Antara Muka Disatukan untuk membantu menyediakan pengalaman pengguna yang lebih baik.</span><span class="sxs-lookup"><span data-stu-id="1db42-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="1db42-112">Aplikasi direka bentuk semula menghantar yang konsisten dan seragam (UI) dan ia mengikut prinsip reka bentuk responsif untuk pandangan optimum pada sebarang saiz skrin atau peranti.</span><span class="sxs-lookup"><span data-stu-id="1db42-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="1db42-113">Telah ada perubahan lain di seluruh aplikasi.</span><span class="sxs-lookup"><span data-stu-id="1db42-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="1db42-114">Antara kawasan yang telah ditukar termasuk penetapan harga, penempahan dan pemberian sumber, masa, perbelanjaan dan kelulusan.</span><span class="sxs-lookup"><span data-stu-id="1db42-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="1db42-115">Sebelum anda memulakan proses peningkatan, kami mengesyorkan anda melengkapkan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="1db42-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="1db42-116">Tentu sahkan sama Dynamics 365 Field Service dan Project Service Automation telah dipasang pada tika yang dikenal pasti.</span><span class="sxs-lookup"><span data-stu-id="1db42-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="1db42-117">Jika kedua-dua penyelesaian dipasang, anda perlu merancang untuk menaik taraf sebelum anda menyambung semula kegunaan biasa tika.</span><span class="sxs-lookup"><span data-stu-id="1db42-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="1db42-118">Semak semula dengan teliti topik berikut.</span><span class="sxs-lookup"><span data-stu-id="1db42-118">Carefully review the following topics.</span></span> <span data-ttu-id="1db42-119">Kesedaran dan pemahaman tentang perubahan antara versi akan membantu anda dengan proses peningkatan.</span><span class="sxs-lookup"><span data-stu-id="1db42-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="1db42-120">Topik ini memberikan maklumat tentang perubahan besar dalam PSA, bersama dengan pertimbangan dan pengesyoran untuk merancang naik taraf anda kepada versi 3.x.</span><span class="sxs-lookup"><span data-stu-id="1db42-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="1db42-121">Perkara baharu atau berubah dalam Project Service Automation versi 3</span><span class="sxs-lookup"><span data-stu-id="1db42-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="1db42-122">Pertimbangan naik taraf - Project Service Automation versi 2.x atau 1.x kepada versi 3</span><span class="sxs-lookup"><span data-stu-id="1db42-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="1db42-123">Naik taraf tika kotak pasir anda untuk menilai perubahan dalam pelaksanaan anda sebelum anda menaik taraf tika pengeluaran anda.</span><span class="sxs-lookup"><span data-stu-id="1db42-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="1db42-124">Selepas anda menyemak topik yang disebutkan sebelum ini dan bersedia untuk menaik taraf kepada PSA versi 3.x atau versi UCI, serahkan permintaan kepada sokongan Microsoft untuk membuat peningkatan tersedia daripada Pusat pentadbir.</span><span class="sxs-lookup"><span data-stu-id="1db42-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="1db42-125">Dalam permintaan anda, berikan butiran tika anda.</span><span class="sxs-lookup"><span data-stu-id="1db42-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="1db42-126">Versi lebih lama PSA (PSA versi 2.x) dalam tika yang baharu dicipta</span><span class="sxs-lookup"><span data-stu-id="1db42-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="1db42-127">Pada 17 Mei, 2019, semua tika baru akan mempunyai UCI sebagai klien lalai.</span><span class="sxs-lookup"><span data-stu-id="1db42-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="1db42-128">Untuk penjajaran dengan perubahan ini, PSA versi 3.x dan Field Service Version 8.x akan diperuntukkan secara lalai, kerana versi ini direka untuk berfungsi dengan klien UCI.</span><span class="sxs-lookup"><span data-stu-id="1db42-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="1db42-129">Mulai 1 Mac 2020, pelanggan Dynamics PSA tidak lagi akan dapat mencipta persekitaran baharu dengan versi PSA yang lebih lama, contohnya PSA versi 2.x atau lebih rendah.</span><span class="sxs-lookup"><span data-stu-id="1db42-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="1db42-130">Sebarang persekitaran baharu akan hanya mendapat versi 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="1db42-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="1db42-131">Untuk pengalaman terbaik apabila anda menggunakan versi lebih lama daripada Field Service dan aplikasi PSA, pergi ke halaman **Tetapan sistem** dan untuk medan **Gunakan medan baru Antara Muka Disatukan hanya (disyorkan)**, pilih **Tidak** sebagai versi ini tidak direka untuk dimuatkan dengan betul dalam UCI.</span><span class="sxs-lookup"><span data-stu-id="1db42-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="1db42-132">Selepas anda memadamkan UCI, anda boleh buka dan jalankan versi Field Service ini dan PSA dengan menggunakan klien web lama.</span><span class="sxs-lookup"><span data-stu-id="1db42-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="1db42-133">Untuk arahan mengenai cara untuk mematikan klien UCI, lihat [Dayakan antara muka disatukan sahaja](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="1db42-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
