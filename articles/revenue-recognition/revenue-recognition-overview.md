---
title: Gambaran keseluruhan pengiktirafan hasil
description: Topik ini memberikan maklumat tentang pengiktirafan hasil dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278879"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="45a9f-103">Gambaran keseluruhan pengiktirafan hasil</span><span class="sxs-lookup"><span data-stu-id="45a9f-103">Revenue recognition overview</span></span>

<span data-ttu-id="45a9f-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="45a9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="45a9f-105">Dalam Dynamics 365 Project Operations, prinsip pengiktirafan hasil berbeza-beza berdasarkan pada kaedah pengebilan terpilih untuk projek atau bahagian projek.</span><span class="sxs-lookup"><span data-stu-id="45a9f-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="45a9f-106">Topik ini memberikan maklumat tentang pengiktirafan hasil dalam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="45a9f-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="45a9f-107">Transaksi dikira menggunakan kaedah pengebilan masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="45a9f-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="45a9f-108">Kos dan pengiktirafan hasil disambungkan.</span><span class="sxs-lookup"><span data-stu-id="45a9f-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="45a9f-109">Kos transaksi dan jualan yang belum dibilkan diposkan menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="45a9f-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="45a9f-110">Kos projek dan profil hasil menentukan sama ada transaksi jualan yang belum dibilkan disiarkan kepada lejar umum.</span><span class="sxs-lookup"><span data-stu-id="45a9f-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="45a9f-111">Jika **Hasil akruan** dipilih, sistem menggunakan akaun **Nilai jualan WIP** dan **Nilai jualan hasi terakru** semasa penyiaran.</span><span class="sxs-lookup"><span data-stu-id="45a9f-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="45a9f-112">Berikut ialah sebuah contoh bagi kaedah ini.</span><span class="sxs-lookup"><span data-stu-id="45a9f-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="45a9f-113">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="45a9f-113">Transaction type</span></span> | <span data-ttu-id="45a9f-114">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-114">Debit/Credit</span></span> | <span data-ttu-id="45a9f-115">Amaun</span><span class="sxs-lookup"><span data-stu-id="45a9f-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="45a9f-116">Nilai Jualan WIP</span><span class="sxs-lookup"><span data-stu-id="45a9f-116">WIP Sales value</span></span> | <span data-ttu-id="45a9f-117">Debit</span><span class="sxs-lookup"><span data-stu-id="45a9f-117">Debit</span></span> | <span data-ttu-id="45a9f-118">100</span><span class="sxs-lookup"><span data-stu-id="45a9f-118">100</span></span> |
  | <span data-ttu-id="45a9f-119">Hasil jualan hasi terakru</span><span class="sxs-lookup"><span data-stu-id="45a9f-119">Accrued revenue sales value</span></span> | <span data-ttu-id="45a9f-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-120">Credit</span></span> | <span data-ttu-id="45a9f-121">100</span><span class="sxs-lookup"><span data-stu-id="45a9f-121">100</span></span> |

- <span data-ttu-id="45a9f-122">Hasil diktiraf semasa penginvoisan.</span><span class="sxs-lookup"><span data-stu-id="45a9f-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="45a9f-123">Sistem ini menggunakan akaun **Hasil Invois** semasa penyiaran.</span><span class="sxs-lookup"><span data-stu-id="45a9f-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="45a9f-124">Berikut ialah sebuah contoh bagi kaedah ini.</span><span class="sxs-lookup"><span data-stu-id="45a9f-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="45a9f-125">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="45a9f-125">Transaction type</span></span> | <span data-ttu-id="45a9f-126">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-126">Debit/Credit</span></span> | <span data-ttu-id="45a9f-127">Amaun</span><span class="sxs-lookup"><span data-stu-id="45a9f-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="45a9f-128">Baki pelanggan</span><span class="sxs-lookup"><span data-stu-id="45a9f-128">Customer balance</span></span> | <span data-ttu-id="45a9f-129">Debit</span><span class="sxs-lookup"><span data-stu-id="45a9f-129">Debit</span></span> | <span data-ttu-id="45a9f-130">120</span><span class="sxs-lookup"><span data-stu-id="45a9f-130">120</span></span> |
  | <span data-ttu-id="45a9f-131">Cukai jualan boleh bayar</span><span class="sxs-lookup"><span data-stu-id="45a9f-131">Sales tax payable</span></span> | <span data-ttu-id="45a9f-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-132">Credit</span></span> | <span data-ttu-id="45a9f-133">20</span><span class="sxs-lookup"><span data-stu-id="45a9f-133">20</span></span> |
  | <span data-ttu-id="45a9f-134">Hasil Diinvois</span><span class="sxs-lookup"><span data-stu-id="45a9f-134">Invoiced Revenue</span></span> | <span data-ttu-id="45a9f-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-135">Credit</span></span> | <span data-ttu-id="45a9f-136">100</span><span class="sxs-lookup"><span data-stu-id="45a9f-136">100</span></span> |

- <span data-ttu-id="45a9f-137">Jika hasil terakru apabila jualan belum dibilkan disiarkan, sistem akan mengundurkan hasil terakru pada invois.</span><span class="sxs-lookup"><span data-stu-id="45a9f-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="45a9f-138">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="45a9f-138">Transaction type</span></span> | <span data-ttu-id="45a9f-139">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-139">Debit/Credit</span></span> | <span data-ttu-id="45a9f-140">Amaun</span><span class="sxs-lookup"><span data-stu-id="45a9f-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="45a9f-141">Nilai Jualan WIP</span><span class="sxs-lookup"><span data-stu-id="45a9f-141">WIP Sales value</span></span> | <span data-ttu-id="45a9f-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="45a9f-142">Credit</span></span> | <span data-ttu-id="45a9f-143">100</span><span class="sxs-lookup"><span data-stu-id="45a9f-143">100</span></span> |
  | <span data-ttu-id="45a9f-144">Hasil jualan hasi terakru</span><span class="sxs-lookup"><span data-stu-id="45a9f-144">Accrued revenue sales value</span></span> | <span data-ttu-id="45a9f-145">Debit</span><span class="sxs-lookup"><span data-stu-id="45a9f-145">Debit</span></span> | <span data-ttu-id="45a9f-146">100</span><span class="sxs-lookup"><span data-stu-id="45a9f-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="45a9f-147">Transaksi dikira menggunakan kaedah pengebilan harga tetap</span><span class="sxs-lookup"><span data-stu-id="45a9f-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="45a9f-148">Kos dan pengiktirafan hasil diasingkan.</span><span class="sxs-lookup"><span data-stu-id="45a9f-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="45a9f-149">Kos transaksi diposkan menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="45a9f-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="45a9f-150">Transaksi jualan belum dibilkan tidak dicipta.</span><span class="sxs-lookup"><span data-stu-id="45a9f-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="45a9f-151">Hasil boleh diiktiraf semasa penginvoisan jika kos projek dan profil hasil telah menetapkan **Prinsip digunakan untuk pengiraan penyiapan projek** kepada **Tiada WIP**.</span><span class="sxs-lookup"><span data-stu-id="45a9f-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="45a9f-152">Hanya gunakan kaedah ini untuk projek jangka pendek yang mudah.</span><span class="sxs-lookup"><span data-stu-id="45a9f-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="45a9f-153">Hasil boleh diiktiraf menggunakan anggaran hasil harga tetap, dengan sama ada kaedah **Kontrak siap** atau **Pengiktirafan hasil siap peratus**.</span><span class="sxs-lookup"><span data-stu-id="45a9f-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45a9f-154">Sumber tambahan</span><span class="sxs-lookup"><span data-stu-id="45a9f-154">Additional resources</span></span>
[<span data-ttu-id="45a9f-155">Konfigurasi perakaunan untuk artikel projek boleh dibil</span><span class="sxs-lookup"><span data-stu-id="45a9f-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="45a9f-156">Projek anggaran hasil harga tetap</span><span class="sxs-lookup"><span data-stu-id="45a9f-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="45a9f-157">Uruskan anggaran hasil</span><span class="sxs-lookup"><span data-stu-id="45a9f-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="45a9f-158">Kos untuk melengkapkan kaedah</span><span class="sxs-lookup"><span data-stu-id="45a9f-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]