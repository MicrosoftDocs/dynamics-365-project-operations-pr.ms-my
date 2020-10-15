---
title: Tambah langganan Azure untuk projek LCS
description: Topik ini memberikan maklumat mengenai cara untuk menyambungkan langganan Azure anda ke projek LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948991"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="dd774-103">Tambah langganan Azure untuk projek LCS</span><span class="sxs-lookup"><span data-stu-id="dd774-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="dd774-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="dd774-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dd774-105">Persekitaran berhos awan mesti dilaksanakan dengan menggunakan langganan Azure yang sedia ada.</span><span class="sxs-lookup"><span data-stu-id="dd774-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="dd774-106">Topik ini menjelaskan cara untuk menyambungkan langganan Azure sedia ada anda ke projek LCS.</span><span class="sxs-lookup"><span data-stu-id="dd774-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="dd774-107">Berikan persetujuan pentadbir</span><span class="sxs-lookup"><span data-stu-id="dd774-107">Grant admin consent</span></span>

1. <span data-ttu-id="dd774-108">Dalam projek LCS anda, dalam bahagian **persekitaran**, pilih tetapan **Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="dd774-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Tetapan Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="dd774-110">Pada halaman **tetapan projek**, pada tab **penyambung Azure**, pilih **Benarkan**.</span><span class="sxs-lookup"><span data-stu-id="dd774-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="dd774-111">Ini membolehkan persekitaran digunakan untuk projek ini.</span><span class="sxs-lookup"><span data-stu-id="dd774-111">This allows environments to be deployed to this project.</span></span>

![Penyambung Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="dd774-113">Pilih semula **Benarkan** untuk memberikan kebenaran pentadbir.</span><span class="sxs-lookup"><span data-stu-id="dd774-113">Select **Authorize** again to provide admin consent.</span></span>

![Berikan Persetujuan Pentadbir](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="dd774-115">Menerima permintaan keizinan.</span><span class="sxs-lookup"><span data-stu-id="dd774-115">Accept the permissions request.</span></span>

![Menerima Permintaan Keizinan](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="dd774-117">Pengesahan kini selesai.</span><span class="sxs-lookup"><span data-stu-id="dd774-117">The authorization is now complete.</span></span> 

![Pengesahan Berjaya](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="dd774-119">Berikan akses Perkhidmatan Pelaksanaan Dynamics kepada langganan Azure anda</span><span class="sxs-lookup"><span data-stu-id="dd774-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="dd774-120">Pergi ke pengebilan [Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) dan pilih langganan anda.</span><span class="sxs-lookup"><span data-stu-id="dd774-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="dd774-121">Perkhidmatan Pelaksanaan Dynamics perlu mengakses langganan ini untuk dapat menggunakan persekitaran.</span><span class="sxs-lookup"><span data-stu-id="dd774-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Butiran Langganan Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="dd774-123">Pilih **kawalan capaian (IAM)** dalam anak tetingkap navigasi dan kemudian pilih **Tambah tugasan peranan**.</span><span class="sxs-lookup"><span data-stu-id="dd774-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="dd774-124">Dalam gelangsar di sebelah kanan, pilih **Peranan penyumbang** dan dalam senarai yang disediakan, cari dan pilih **Perkhidmatan Pelaksanaan Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="dd774-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="dd774-125">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="dd774-125">Select **Save**.</span></span>

![Akses Langganan](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="dd774-127">Tambah penyambung langganan ke projek LCS</span><span class="sxs-lookup"><span data-stu-id="dd774-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="dd774-128">Dalam projek LCS anda, pada halaman tetapan **Microsoft Azure**, pilih **Tambah** untuk menambah penyambung baharu.</span><span class="sxs-lookup"><span data-stu-id="dd774-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="dd774-129">Masukkan ID langganan Azure anda.</span><span class="sxs-lookup"><span data-stu-id="dd774-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="dd774-130">Anda boleh mencari ID langganan Azure anda dalam [Portal Azure](https://ms.portal.azure.com/), di bawah  **Tetapan**  di sebelah kiri bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="dd774-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="dd774-131">Dalam **Konfigurasi untuk menggunakan medan Pengurus Sumber Azure**, pilih **Ya**.</span><span class="sxs-lookup"><span data-stu-id="dd774-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="dd774-132">Pastikan Langganan Azure AAD Domain Penyewa yang sepadan dengan domain-memiliki langganan Azure yang anda gunakan dan pilih **Seterusnya**.</span><span class="sxs-lookup"><span data-stu-id="dd774-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="dd774-133">Pada skrin **Persediaan Microsoft Azure**, pilih **Seterusnya** untuk mengesahkannya.</span><span class="sxs-lookup"><span data-stu-id="dd774-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="dd774-134">Jika anda menerima ralat pada skrin ini, kembali ke bahagian [Berikan akses kepada Perkhidmatan Pelaksanaan Dynamics kepada Langganan Azure](#provide) dalam topik ini dan pastikan anda telah melengkapkan semua langkah tersebut.</span><span class="sxs-lookup"><span data-stu-id="dd774-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="dd774-135">Muat turun Sijil Pengurusan Azure ke folder tempatan pada komputer anda dan kemudian muat naik fail tersebut ke Portal Pengurusan Azure dengan pergi ke **Tetapan** > **Sijil Pengurusan**.</span><span class="sxs-lookup"><span data-stu-id="dd774-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="dd774-136">Sijil ini akan mendayakan LCS untuk berhubung dengan Azure bagi pihak anda.</span><span class="sxs-lookup"><span data-stu-id="dd774-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="dd774-137">Anda boleh melangkau langkah ini jika pengguna anda mempunyai akses kepada langganan.</span><span class="sxs-lookup"><span data-stu-id="dd774-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="dd774-138">Pilih  **Seterusnya**.</span><span class="sxs-lookup"><span data-stu-id="dd774-138">Select  **Next**.</span></span>
8. <span data-ttu-id="dd774-139">Pilih rantau Azure untuk menggunakan dan pilih pusat data yang berdekatan dengan tempat anda merancang untuk menggunakan sistem ini.</span><span class="sxs-lookup"><span data-stu-id="dd774-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="dd774-140">Pilih  **Connect**.</span><span class="sxs-lookup"><span data-stu-id="dd774-140">Select  **Connect**.</span></span>

<span data-ttu-id="dd774-141">Anda telah berjaya menyambungkan langganan Azure anda.</span><span class="sxs-lookup"><span data-stu-id="dd774-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="dd774-142">Anda kini boleh menggunakan Dynamics 365 Finance persekitaran berhos awan.</span><span class="sxs-lookup"><span data-stu-id="dd774-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


