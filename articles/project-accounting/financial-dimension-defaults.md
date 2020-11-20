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
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131894"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="15a3e-103">Dimensi perakaunan lalai</span><span class="sxs-lookup"><span data-stu-id="15a3e-103">Financial dimension defaults</span></span>

<span data-ttu-id="15a3e-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="15a3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="15a3e-105">Dynamics 365 Project Operations rangka kerja [Dimensi kewangan](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) dalam Dynamics 365 Finance untuk menyediakan wawasan tambahan mengenai sub Lejar projek dan transaksi lejar umum.</span><span class="sxs-lookup"><span data-stu-id="15a3e-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="15a3e-106">Dimensi kewangan lalai boleh ditetapkan pada pelanggan, sumber pembiayaan projek, pencapaian, baris kontrak projek, atau projek.</span><span class="sxs-lookup"><span data-stu-id="15a3e-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="15a3e-107">Takrifkan dimensi kewangan lalai untuk pelanggan</span><span class="sxs-lookup"><span data-stu-id="15a3e-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="15a3e-108">Lalai dimensi pelanggan ditentukan dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="15a3e-109">Lengkapkan langkah berikut untuk menetapkan lalai dimensi.</span><span class="sxs-lookup"><span data-stu-id="15a3e-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="15a3e-110">Pergi ke **Akaun belum terima** > **Pelanggan** > **Semua pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="15a3e-111">Pada halaman **Pelanggan**, pada tab **Dimensi kewangan**, tetapkan nilai dimensi kewangan untuk pelanggan khusus.</span><span class="sxs-lookup"><span data-stu-id="15a3e-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="15a3e-112">Takrifkan dimensi kewangan lalai untuk kontrak projek</span><span class="sxs-lookup"><span data-stu-id="15a3e-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="15a3e-113">Kontrak projek dicipta dan dikekalkan dalam Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="15a3e-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="15a3e-114">Sifat perakaunan bagi kontrak projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="15a3e-115">Tetapkan dimensi kewangan untuk sumber pembiayaan projek</span><span class="sxs-lookup"><span data-stu-id="15a3e-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="15a3e-116">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="15a3e-117">Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15a3e-118">Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="15a3e-119">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="15a3e-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="15a3e-120">Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="15a3e-121">Tetapkan dimensi kewangan untuk baris kontrak</span><span class="sxs-lookup"><span data-stu-id="15a3e-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="15a3e-122">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="15a3e-123">Pilih rekod yang anda mahu kemas kini dan pada tab **Kontrak projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15a3e-124">Kembangkan **Maklumat berkaitan** dan pilih tab **Sumber pembiayaan**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="15a3e-125">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="15a3e-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="15a3e-126">Lalai dimensi kewangan boleh terpakai dan boleh digunakan hanya dengan baris kontrak Harga tetap (pencapaian).</span><span class="sxs-lookup"><span data-stu-id="15a3e-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="15a3e-127">Lalai ini digunakan pada transaksi akaun berkaitan dan baris invois.</span><span class="sxs-lookup"><span data-stu-id="15a3e-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="15a3e-128">Takrifkan dimensi kewangan lalai untuk projek</span><span class="sxs-lookup"><span data-stu-id="15a3e-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="15a3e-129">Projek dicipta dan dikekalkan dalam (CDS).</span><span class="sxs-lookup"><span data-stu-id="15a3e-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="15a3e-130">Atribut perakaunan bagi projek ditetapkan dalam modul **Pengurusan projek dan perakaunan** dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="15a3e-131">Pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Semua projek**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="15a3e-132">Pilih rekod yang anda mahu kemas kini dan pada tab **Projek**, pilih **Tunjuk perakaunan lalai**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="15a3e-133">Kembangkan **Maklumat berkaitan** dan pilih tab **Penyediaan**.</span><span class="sxs-lookup"><span data-stu-id="15a3e-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="15a3e-134">Tetapkan dimensi perakaunan lalai.</span><span class="sxs-lookup"><span data-stu-id="15a3e-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="15a3e-135">Perhatikan bahawa dimensi kewangan lalai daripada akaun pelanggan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="15a3e-136">Jika projek berkaitan dengan baris kontrak dengan pelanggan kontrak berbilang projek, pelanggan utama digunakan untuk dimensi kewangan lalai.</span><span class="sxs-lookup"><span data-stu-id="15a3e-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="15a3e-137">Projek dimensi kewangan lalai digunakan untuk menetapkan garisan jurnal lalai untuk masa, perbelanjaan dan yuran transaksi dalam **Jurnal Integrasi Project Operations** dan pada baris invois projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="15a3e-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
