---
title: Atur letak aplikasi Project Operations Dataverse secara manual dengan sokongan dwi tulis
description: Topik ini menerangkan cara untuk mengatur letak aplikasi Project Operations Dataverse secara manual supaya ia menyokong dwi tulis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274019"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="b38f2-103">Atur letak aplikasi Project Operations Dataverse secara manual dengan sokongan dwi tulis</span><span class="sxs-lookup"><span data-stu-id="b38f2-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="b38f2-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b38f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b38f2-105">Topik ini menerangkan cara untuk mengatur letak Microsoft Dynamics 365 Project Operations dalam Microsoft Dataverse secara manual supaya ia menyokong dwi tulis.</span><span class="sxs-lookup"><span data-stu-id="b38f2-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="b38f2-106">Project Operations mengesan konfigurasi persekitaran dan menambahkan sokongan tambahan untuk dwi tulis jika prasyarat dipenuhi.</span><span class="sxs-lookup"><span data-stu-id="b38f2-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="b38f2-107">Semasa pelaksanaan melalui Microsoft Dynamics Lifecycle Services (LCS), jika anda telah mengikuti arahan dalam topik ini, anda boleh melangkau pelaksanaan integrasi Microsoft Power Platform (sebelum ini dikenali sebagai persekitaran Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="b38f2-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="b38f2-108">Proses pelaksanaan Project Operations dalam Dataverse supaya ia menyokong dwi tulis mempunyai empat langkah utama:</span><span class="sxs-lookup"><span data-stu-id="b38f2-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="b38f2-109">[Cipta persekitaran baharu dalam Dataverse yang menyokong dwi tulis](#create).</span><span class="sxs-lookup"><span data-stu-id="b38f2-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="b38f2-110">[Tambah prasyarat dwi tulis pada persekitaran](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="b38f2-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="b38f2-111">[Tambah aplikasi Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="b38f2-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="b38f2-112">[Pautkan persekitaran anda](#link).</span><span class="sxs-lookup"><span data-stu-id="b38f2-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="b38f2-113">Cipta persekitaran baharu dalam Dataverse yang menyokong dwi tulis</span><span class="sxs-lookup"><span data-stu-id="b38f2-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="b38f2-114">Untuk melengkapkan prosedur ini, anda mesti mendaftar masuk sebagai pentadbir.</span><span class="sxs-lookup"><span data-stu-id="b38f2-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="b38f2-115">Buka [Pusat pentadbir Power Platform](https://admin.powerplatform.com) dan daftar masuk sebagai pentadbir.</span><span class="sxs-lookup"><span data-stu-id="b38f2-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="b38f2-116">Cipta persekitaran baharu dan namakannya.</span><span class="sxs-lookup"><span data-stu-id="b38f2-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="b38f2-117">Pilih jenis persekitaran.</span><span class="sxs-lookup"><span data-stu-id="b38f2-117">Select the environment type.</span></span> <span data-ttu-id="b38f2-118">Jika anda telah mendaftar untuk tawaran percubaan, pilih **Percubaan (berdasarkan langganan)**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="b38f2-119">Sahkan rantau pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="b38f2-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="b38f2-120">Dayakan opsyen **Cipta pangkalan data untuk persekitaran ini**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="b38f2-121">Sahkan bahasa dan kemudian sahkan bahawa mata wang sepadan dengan mata wang untuk aplikasi Finance and Operations anda.</span><span class="sxs-lookup"><span data-stu-id="b38f2-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="b38f2-122">Dayakan opsyen **Aplikasi Dynamics 365** dan sahkan bahawa medan **Laksanakan secara automatik aplikasi ini** ditetapkan kepada **Tiada**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="b38f2-123">Tambah kumpulan keselamatan, jika kumpulan keselamatan ini diperlukan.</span><span class="sxs-lookup"><span data-stu-id="b38f2-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="b38f2-124">Pilih **Simpan** untuk mencipta persekitaran.</span><span class="sxs-lookup"><span data-stu-id="b38f2-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="b38f2-125">Tunggu sehingga pelaksanaan selesai dan persekitaran mencapai keadaan **Sedia**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="b38f2-126">Tambah prasyarat dwi tulis pada persekitaran</span><span class="sxs-lookup"><span data-stu-id="b38f2-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="b38f2-127">Sokongan dwi tulis termasuk medan tambahan yang ditambahkan pada entiti utama seperti entiti **Syarikat**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="b38f2-128">Jika anda menambahkan sokongan dwi tulis pada persekitaran sedia ada, anda mungkin perlu mengemas kini data untuk mendayakan sokongan tersebut.</span><span class="sxs-lookup"><span data-stu-id="b38f2-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="b38f2-129">Untuk maklumat mengenai cara untuk butstrap data, lihat [Butstrap data syarikat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="b38f2-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="b38f2-130">Untuk maklumat lanjut mengenai dwi tulis, lihat [Keperluan sistem dwi tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="b38f2-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="b38f2-131">Lengkapkan prosedur ini untuk menambahkan prasyarat dwi tulis pada persekitaran anda.</span><span class="sxs-lookup"><span data-stu-id="b38f2-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="b38f2-132">Buka persekitaran yang baharu anda cipta dan kemudian pergi ke **Sumber** \> **Aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="b38f2-133">Pilih **Penyelesaian teras dwi tulis** dalam senarai aplikasi dan memasangnya.</span><span class="sxs-lookup"><span data-stu-id="b38f2-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="b38f2-134">Tunggu sehingga pemasangan selesai.</span><span class="sxs-lookup"><span data-stu-id="b38f2-134">Wait until the installation is completed.</span></span> <span data-ttu-id="b38f2-135">Kemudian pilih **Penyelesaian pengorkestraan aplikasi dwi tulis** dalam senarai aplikasi dan memasangnya.</span><span class="sxs-lookup"><span data-stu-id="b38f2-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="b38f2-136">Tambah aplikasi Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="b38f2-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="b38f2-137">Anda boleh melengkapkan prosedur ini hanya jika anda melengkapkan prosedur sebelumnya sebelum anda memasang Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b38f2-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="b38f2-138">Semasa pemasangan, sistem menganalisis konfigurasi persekitaran dan menambahkan sokongan untuk dwi tulis jika ia diperlukan.</span><span class="sxs-lookup"><span data-stu-id="b38f2-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="b38f2-139">Buka persekitaran yang anda cipta lebih awal dan kemudian pergi ke **Sumber** \> **Aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b38f2-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="b38f2-140">Pilih **Microsoft Dynamics 365 Project Operations** dalam senarai aplikasi dan memasangnya.</span><span class="sxs-lookup"><span data-stu-id="b38f2-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="b38f2-141">Pautkan persekitaran anda</span><span class="sxs-lookup"><span data-stu-id="b38f2-141">Link your environments</span></span>

<span data-ttu-id="b38f2-142">Selepas persekitaran Dataverse diatur letak, anda boleh menyediakan pautan dalam aplikasi Finance and Operations anda.</span><span class="sxs-lookup"><span data-stu-id="b38f2-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="b38f2-143">Ikut langkah dalam [Gunakan wizard dwi tulis untuk memautkan persekitaran anda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="b38f2-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
