---
title: Set kelulusan
description: Topik ini menyediakan maklumat tentang set kelulusan, permintaan dan subset operasi.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116882"
---
# <a name="approval-sets"></a><span data-ttu-id="e19e4-103">Set kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e19e4-104">Set kelulusan mengumpulkan permintaan kelulusan bersama ke dalam subset operasi yang lebih kecil.</span><span class="sxs-lookup"><span data-stu-id="e19e4-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="e19e4-105">Pengumpulan ini membolehkan kelulusan diproses mengikut pelaksanaan Projek dan membolehkan untuk mencuba semula dan penjujukan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="e19e4-106">Pengumpulan meningkatkan kebolehpercayaan dan kebolehkesanan pemprosesan kelulusan untuk jumlah kelulusan yang besar.</span><span class="sxs-lookup"><span data-stu-id="e19e4-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="e19e4-107">Set kelulusan menunjukkan keadaan pemprosesan keseluruhan bagi rekod yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="e19e4-108">Apabila rekod kelulusan diproses dengan menggunakan set kelulusan, rekod bergerak daripada **Diserahkan** kepada **Diluluskan** dan dinyahpautkan daripada set kelulusan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="e19e4-109">Jika rekod gagal apabila ia diserahkan untuk diluluskan, rekod masih dalam status **Diserahkan** dan set kelulusan ditanda sebagai gagal.</span><span class="sxs-lookup"><span data-stu-id="e19e4-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="e19e4-110">Set kelulusan log mesej ralat kegagalan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="e19e4-111">Kelulusan pemprosean dan set kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="e19e4-112">Kelulusan yang dibariskan untuk pemprosesan boleh dilihat dalam pandangan **Kelulusan Pemprosesan**.</span><span class="sxs-lookup"><span data-stu-id="e19e4-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="e19e4-113">Sistem mencuba untuk memproses semua penyertaan beberapa kali secara segerak, termasuk mencuba semula kelulusan jika percubaan sebelumnya gagal.</span><span class="sxs-lookup"><span data-stu-id="e19e4-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="e19e4-114">Medan **Set Kelulusan Seumur Hidup** merekodkan bilangan baki percubaan untuk memproses set sebelum ia ditanda sebagai gagal.</span><span class="sxs-lookup"><span data-stu-id="e19e4-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="e19e4-115">Kelulusan gagal dan set kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="e19e4-116">Pandangan **Kelulusan gagal** menyenaraikan semua kelulusan yang memerlukan campur tangan pengguna.</span><span class="sxs-lookup"><span data-stu-id="e19e4-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="e19e4-117">Buka log set kelulusan berkaitan untuk mengenal pasti punca kegagalan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="e19e4-118">Memilih **Cuba semula** mennambah kepada kiraan jangka hayat set kelulusan, mengalih keluar kelulusan yang ditetapkan kembali ke status **Pemprosesan** dan percubaan untuk memproses baki rekod.</span><span class="sxs-lookup"><span data-stu-id="e19e4-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="e19e4-119">Konfigurasikan set kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="e19e4-120">dayakan ciri set Kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="e19e4-121">Sebelum anda mendayakan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="e19e4-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e19e4-122">Pergi ke halaman **Parameter projek** dan pilih **Kawalan Ciri** > **Dayakan Kelulusan Moden**.</span><span class="sxs-lookup"><span data-stu-id="e19e4-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="e19e4-123">Matikan ciri set Kelulusan</span><span class="sxs-lookup"><span data-stu-id="e19e4-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="e19e4-124">Sebelum anda mematikan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.</span><span class="sxs-lookup"><span data-stu-id="e19e4-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e19e4-125">Pergi ke halaman **Parameter Projek** dan pilih **Kawalan Ciri** > **Nyahdayakan Kelulusan Moden**.</span><span class="sxs-lookup"><span data-stu-id="e19e4-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="e19e4-126">Mengkonfigurasi ambang tidak segerak</span><span class="sxs-lookup"><span data-stu-id="e19e4-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="e19e4-127">Apabila set kelulusan dicipta, pemprosesan bergerak ke latar belakang apabila bilangan rekod yang dipilih untuk diluluskan melebihi ambang yang dinyatakan.</span><span class="sxs-lookup"><span data-stu-id="e19e4-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="e19e4-128">Gunakan medan **Ambang Tidak Segerak** untuk mengkonfigurasikan apabila pemprosesan kelulusan sepatutnya dijalankan secara segerak atau tidak segerak.</span><span class="sxs-lookup"><span data-stu-id="e19e4-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="e19e4-129">Nilai yang sah ialah:</span><span class="sxs-lookup"><span data-stu-id="e19e4-129">Valid values are:</span></span>

  - <span data-ttu-id="e19e4-130">Sifar: Semua permohonan perlu diproses secara tidak segerak.</span><span class="sxs-lookup"><span data-stu-id="e19e4-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="e19e4-131">Bilangan yang lebih besar daripada sifar: Kelulusan diproses secara tidak segerak hanya apabila bilangan kelulusan yang diserahkan melebihi nilai ini.</span><span class="sxs-lookup"><span data-stu-id="e19e4-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
