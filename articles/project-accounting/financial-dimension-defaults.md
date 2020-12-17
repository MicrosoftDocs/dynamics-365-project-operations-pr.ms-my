---
title: Dimensi perakaunan lalai
description: Topik ini memberikan maklumat mengenai cara untuk menyediakan lalai dimensi kewangan.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642374"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="14991-103">Dimensi perakaunan lalai</span><span class="sxs-lookup"><span data-stu-id="14991-103">Financial dimension defaults</span></span>

<span data-ttu-id="14991-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="14991-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="14991-105">Dynamics 365 Project Operations menggunakan rangka kerja [Dimensi kewangan](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) dalam Dynamics 365 Finance untuk menyediakan cerapan tambahan tentang sublejar projek dan transaksi lejar umum.</span><span class="sxs-lookup"><span data-stu-id="14991-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="14991-106">Dimensi kewangan lalai boleh ditetapkan pada pelanggan, sumber pembiayaan projek, pencapaian, baris kontrak projek, atau projek.</span><span class="sxs-lookup"><span data-stu-id="14991-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="14991-107">Takrifkan dimensi kewangan lalai untuk pelanggan</span><span class="sxs-lookup"><span data-stu-id="14991-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="14991-108">Lalai dimensi pelanggan ditentukan dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="14991-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="14991-109">Lengkapkan langkah berikut untuk menetapkan lalai dimensi.</span><span class="sxs-lookup"><span data-stu-id="14991-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="14991-110">Pergi ke **Akaun belum terima** > **Pelanggan** > **Semua pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="14991-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="14991-111">Pada halaman **Pelanggan**, pada tab **Dimensi kewangan**, tetapkan nilai dimensi kewangan untuk pelanggan khusus.</span><span class="sxs-lookup"><span data-stu-id="14991-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="14991-112">Takrifkan dimensi kewangan lalai untuk kontrak projek</span><span class="sxs-lookup"><span data-stu-id="14991-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="14991-113">Kontrak projek dicipta dan dikekalkan dalam Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="14991-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="14991-114">Sifat perakaunan bagi kontrak projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="14991-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="14991-115">Tetapkan dimensi kewangan untuk sumber pembiayaan projek</span><span class="sxs-lookup"><span data-stu-id="14991-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="14991-116">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="14991-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="14991-117">Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="14991-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="14991-118">Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.</span><span class="sxs-lookup"><span data-stu-id="14991-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="14991-119">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="14991-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="14991-120">Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="14991-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="14991-121">Tetapkan dimensi kewangan untuk baris kontrak</span><span class="sxs-lookup"><span data-stu-id="14991-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="14991-122">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="14991-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="14991-123">Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="14991-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="14991-124">Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.</span><span class="sxs-lookup"><span data-stu-id="14991-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="14991-125">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="14991-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="14991-126">Lalai dimensi kewangan boleh terpakai dan boleh digunakan hanya dengan baris kontrak Harga tetap (pencapaian).</span><span class="sxs-lookup"><span data-stu-id="14991-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="14991-127">Lalai ini digunakan pada transaksi akaun berkaitan dan baris invois.</span><span class="sxs-lookup"><span data-stu-id="14991-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="14991-128">Takrifkan dimensi kewangan lalai untuk projek</span><span class="sxs-lookup"><span data-stu-id="14991-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="14991-129">Projek dicipta dan dikekalkan dalam (CDS).</span><span class="sxs-lookup"><span data-stu-id="14991-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="14991-130">Atribut perakaunan bagi projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="14991-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="14991-131">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Semua projek**.</span><span class="sxs-lookup"><span data-stu-id="14991-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="14991-132">Pilih rekod yang anda mahu kemas kini dan pada tab **Projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="14991-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="14991-133">Kembangkan **Maklumat berkaitan** dan pilih tab **Penyediaan**.</span><span class="sxs-lookup"><span data-stu-id="14991-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="14991-134">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="14991-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="14991-135">Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="14991-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="14991-136">Jika projek berkaitan dengan baris kontrak dengan pelanggan kontrak berbilang projek, pelanggan utama digunakan untuk dimensi kewangan lalai.</span><span class="sxs-lookup"><span data-stu-id="14991-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="14991-137">Projek dimensi kewangan lalai digunakan untuk menetapkan garisan jurnal lalai untuk masa, perbelanjaan dan yuran transaksi dalam **Jurnal Integrasi Project Operations** dan pada baris invois projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="14991-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
