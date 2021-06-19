---
title: Naik taraf laman utama
description: Topik ini menunjukkan di mana untuk mencari maklumat penting mengenai ciri baharu dan diubah dalam Dynamics 365 Project Service Automation dan proses untuk menaik taraf kepada versi terbaharu.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012372"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="ab62a-103">Naik taraf laman utama</span><span class="sxs-lookup"><span data-stu-id="ab62a-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="ab62a-104">Naik taraf daripada versi PSA 2.x atau 1.x kepada versi 3.x</span><span class="sxs-lookup"><span data-stu-id="ab62a-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="ab62a-105">Tika baharu</span><span class="sxs-lookup"><span data-stu-id="ab62a-105">New instances</span></span>

<span data-ttu-id="ab62a-106">Pada 17 Mei 2019, apabila Project Service Automation dipilih semasa peruntukan tika baharu, versi 3.x dipasang secara lalai.</span><span class="sxs-lookup"><span data-stu-id="ab62a-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="ab62a-107">Tika sedia ada</span><span class="sxs-lookup"><span data-stu-id="ab62a-107">Existing instances</span></span>

<span data-ttu-id="ab62a-108">Sebelum ini, pelanggan yang mempunyai tika versi PSA 2.x dan perlu menaik taraf kepada versi 3.x, yang berasaskan antara muka klien Disatukan (UCI) versi PSA, mesti menghubungi Sokongan Microsoft dan menyediakan butiran tika mereka, supaya sokongan boleh mendayakan tika untuk naik taraf kepada versi 3.x.</span><span class="sxs-lookup"><span data-stu-id="ab62a-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="ab62a-109">Bermula 1 Mac 2020, pelanggan yang mempunyai tika PSA versi 2.x dan perlu menaik taraf kepada versi 3.x akan dapat menaik taraf tika mereka secara terus daripada portal Pentadbir tanpa perlu menghubungi Sokongan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ab62a-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="ab62a-110">PSA versi 3.x termasuk perubahan ketara.</span><span class="sxs-lookup"><span data-stu-id="ab62a-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="ab62a-111">Ia telah dibina pada rangka kerja Antara Muka Disatukan untuk membantu menyediakan pengalaman pengguna yang lebih baik.</span><span class="sxs-lookup"><span data-stu-id="ab62a-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="ab62a-112">Aplikasi direka bentuk semula menghantar yang konsisten dan seragam (UI) dan ia mengikut prinsip reka bentuk responsif untuk pandangan optimum pada sebarang saiz skrin atau peranti.</span><span class="sxs-lookup"><span data-stu-id="ab62a-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="ab62a-113">Telah ada perubahan lain di seluruh aplikasi.</span><span class="sxs-lookup"><span data-stu-id="ab62a-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="ab62a-114">Antara kawasan yang telah ditukar termasuk penetapan harga, penempahan dan pemberian sumber, masa, perbelanjaan dan kelulusan.</span><span class="sxs-lookup"><span data-stu-id="ab62a-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="ab62a-115">Sebelum anda memulakan proses peningkatan, kami mengesyorkan anda melengkapkan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="ab62a-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="ab62a-116">Tentu sahkan sama Dynamics 365 Field Service dan Project Service Automation telah dipasang pada tika yang dikenal pasti.</span><span class="sxs-lookup"><span data-stu-id="ab62a-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="ab62a-117">Jika kedua-dua penyelesaian dipasang, anda perlu merancang untuk menaik taraf sebelum anda menyambung semula kegunaan biasa tika.</span><span class="sxs-lookup"><span data-stu-id="ab62a-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="ab62a-118">Semak semula dengan teliti topik berikut.</span><span class="sxs-lookup"><span data-stu-id="ab62a-118">Carefully review the following topics.</span></span> <span data-ttu-id="ab62a-119">Kesedaran dan pemahaman tentang perubahan antara versi akan membantu anda dengan proses peningkatan.</span><span class="sxs-lookup"><span data-stu-id="ab62a-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="ab62a-120">Topik ini memberikan maklumat tentang perubahan besar dalam PSA, bersama dengan pertimbangan dan pengesyoran untuk merancang naik taraf anda kepada versi 3.x.</span><span class="sxs-lookup"><span data-stu-id="ab62a-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="ab62a-121">Perkara baharu atau berubah dalam Project Service Automation versi 3</span><span class="sxs-lookup"><span data-stu-id="ab62a-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="ab62a-122">Pertimbangan naik taraf - Project Service Automation versi 2.x atau 1.x kepada versi 3</span><span class="sxs-lookup"><span data-stu-id="ab62a-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="ab62a-123">Naik taraf tika kotak pasir anda untuk menilai perubahan dalam pelaksanaan anda sebelum anda menaik taraf tika pengeluaran anda.</span><span class="sxs-lookup"><span data-stu-id="ab62a-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="ab62a-124">Selepas anda menyemak topik yang disebutkan sebelum ini dan bersedia untuk menaik taraf kepada PSA versi 3.x atau versi UCI, serahkan permintaan kepada sokongan Microsoft untuk membuat peningkatan tersedia daripada Pusat pentadbir.</span><span class="sxs-lookup"><span data-stu-id="ab62a-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="ab62a-125">Dalam permintaan anda, berikan butiran tika anda.</span><span class="sxs-lookup"><span data-stu-id="ab62a-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="ab62a-126">Versi lebih lama PSA (PSA versi 2.x) dalam tika yang baharu dicipta</span><span class="sxs-lookup"><span data-stu-id="ab62a-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="ab62a-127">Pada 17 Mei, 2019, semua tika baru akan mempunyai UCI sebagai klien lalai.</span><span class="sxs-lookup"><span data-stu-id="ab62a-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="ab62a-128">Untuk penjajaran dengan perubahan ini, PSA versi 3.x dan Field Service Version 8.x akan diperuntukkan secara lalai, kerana versi ini direka untuk berfungsi dengan klien UCI.</span><span class="sxs-lookup"><span data-stu-id="ab62a-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="ab62a-129">Bermula 1 Mac 2020, pelanggan Dynamics PSA tidak lagi perlu mencipta persekitaran baharu dengan versi PSA yang lama, contohnya PSA versi 2.x atau ke bawah.</span><span class="sxs-lookup"><span data-stu-id="ab62a-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="ab62a-130">Sebarang persekitaran baharu akan hanya mendapat versi 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="ab62a-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="ab62a-131">Untuk pengalaman terbaik apabila anda menggunakan versi lebih lama daripada Field Service dan aplikasi PSA, pergi ke halaman **Tetapan sistem** dan untuk medan **Gunakan medan baru Antara Muka Disatukan hanya (disyorkan)**, pilih **Tidak** sebagai versi ini tidak direka untuk dimuatkan dengan betul dalam UCI.</span><span class="sxs-lookup"><span data-stu-id="ab62a-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="ab62a-132">Selepas anda memadamkan UCI, anda boleh buka dan jalankan versi Field Service ini dan PSA dengan menggunakan klien web lama.</span><span class="sxs-lookup"><span data-stu-id="ab62a-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]