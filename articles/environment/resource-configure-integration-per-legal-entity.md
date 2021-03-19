---
title: Konfigurasikan integrasi Operasi Projek setiap entiti sah
description: Topik ini memberikan maklumat tentang penyediaan integrasi oleh entiti sah dalam Operasi Projek.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276989"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="c6bc9-103">Konfigurasikan integrasi Operasi Projek setiap entiti sah</span><span class="sxs-lookup"><span data-stu-id="c6bc9-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="c6bc9-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="c6bc9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c6bc9-105">Topik ini membimbing anda melalui langkah yang diperlukan untuk mengkonfigurasi Dynamics 365 Project Operations setiap entiti undang-undang.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="c6bc9-106">Dayakan kekunci ciri dalam Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="c6bc9-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="c6bc9-107">Lengkapkan langkah-langkah berikut untuk mendayakan ciri yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="c6bc9-108">Dalam Dynamics 365 Finance, pergi ke ruang kerja **Pengurusan Ciri**.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="c6bc9-109">Dalam **Senarai ciri**, cari dan dayakan ciri berikut:</span><span class="sxs-lookup"><span data-stu-id="c6bc9-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="c6bc9-110">**Dayakan berbilang baris kontrak untuk projek**</span><span class="sxs-lookup"><span data-stu-id="c6bc9-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="c6bc9-111">**Dayakan Operasi Projek pada Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="c6bc9-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="c6bc9-112">Jika anda tidak melihat **Kekunci ciri** yang disenaraikan, sahkan bahawa versi Kewangan anda memenuhi keperluan versi minimum (versi aplikasi 10.0.13 dengan semua kemas kini kualiti digunakan atau lebih tinggi).</span><span class="sxs-lookup"><span data-stu-id="c6bc9-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="c6bc9-113">Pilih **Semak kemas kini** untuk menyegarkan semula senarai ciri.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="c6bc9-114">Takrifkan senario pelaksanaan Operasi Projek untuk entiti sah</span><span class="sxs-lookup"><span data-stu-id="c6bc9-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="c6bc9-115">Anda boleh mendayakan Operasi Projek pada Dynamics 365 Customer Engagement pada peringkat entiti sah.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="c6bc9-116">Anda boleh mempunyai satu entiti sah yang menggunakan Operasi Projek pada Dynamics 365 Customer Engagement untuk senario berasaskan sumber/bukan stok.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="c6bc9-117">Dalam persekitaran yang sama, anda boleh mempunyai entiti sah lain yang menggunakan Operasi Projek untuk senario pesanan stok/pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="c6bc9-118">Dalam Dynamics 365 Finance, pergi ke **Pengurusan projek dan perakaunan** > **Persediaan** > **Parameter pengurusan projek dan perakaunan global**.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="c6bc9-119">Dalam senarai entiti sah yang tersedia, pilih entiti yang berbilang baris kontrak dan Operasi Projek pada ciri Dynamics 365 Customer Engagement akan didayakan.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="c6bc9-120">Biarkan entiti sah yang akan menggunakan Operasi Projek untuk senario pesanan stok/pengeluaran dinyahpilih.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="c6bc9-121">Entiti sah boleh dipilih hanya jika ia tidak mempunyai sebarang projek sedia ada.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="c6bc9-122">Konfigurasikan Parameter pengurusan projek dan perakaunan</span><span class="sxs-lookup"><span data-stu-id="c6bc9-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="c6bc9-123">Setiap entiti sah yang menggunakan Operasi Projek pada Dynamics 365 Customer Engagement memerlukan set parameter lalai.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="c6bc9-124">Parameter ini dikonfigurasikan pada tab **Operasi Projek** pada halaman **Parameter pengurusan projek dan perakaunan**.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="c6bc9-125">Parameter ialah:</span><span class="sxs-lookup"><span data-stu-id="c6bc9-125">The parameters are:</span></span>

  - <span data-ttu-id="c6bc9-126">**Jenis pengebilan lalai**: Operasi Projek menggunakan set tetap jenis pengebilan lalai yang mesti dipetakan kepada sifat baris Kewangan.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="c6bc9-127">Cipta rekod untuk setiap jenis pengebilan: **Tidak ditentukan**, **Boleh caj**, **Tidak boleh caj**, **Percuma** dan **Tidak tersedia**.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="c6bc9-128">**Kategori projek lalai**: Pilih kategori projek lalai yang akan digunakan untuk setiap jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="c6bc9-129">Kategori lalai ini akan digunakan dalam **Jurnal Integrasi Operasi Projek** dan dalam anggaran yang mana tiada kategori transaksi ditentukan untuk projek sebenar.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="c6bc9-130">**Ramalan** : Pilih model ramalan untuk digunakan bagi anggaran masa dan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="c6bc9-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]