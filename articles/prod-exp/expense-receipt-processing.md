---
title: Pemprosesan resit perbelanjaan
description: Topik ini menyediakan maklumat tentang pemprosesan pengecaman aksara optik (OCR) untuk resit. Ciri ini direka untuk menambah baik pengalamanan pengguna apabila laporan perbelanjaan dicipta dalam Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081386"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="2edd9-104">Pemprosesan resit perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="2edd9-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2edd9-105">Entri perbelanjaan telah dipertingkatkan melalui pengenalan pemprosesan pengecaman aksara optik (OCR) untuk resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="2edd9-106">Ciri ini direka untuk menambah baik pengalamanan pengguna apabila laporan perbelanjaan dicipta.</span><span class="sxs-lookup"><span data-stu-id="2edd9-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="2edd9-107">Ciri utama</span><span class="sxs-lookup"><span data-stu-id="2edd9-107">Key features</span></span>

- <span data-ttu-id="2edd9-108">Nama peniaga, tarikh dan jumlah amaun diekstrak daripada resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="2edd9-109">Ciri ini akan cuba memadankan resit yang tidak dilampirkan kepada transaksi perbelanjaan yang tidak dilampirkan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="2edd9-110">Pengguna boleh mencipta transaksi perbelanjaan yang dimasukkan secara manual daripada resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="2edd9-111">Contoh penggunaan</span><span class="sxs-lookup"><span data-stu-id="2edd9-111">Usage examples</span></span>

<span data-ttu-id="2edd9-112">Untuk melampirkan resit secara automatik termasuk transaksi kad kredit apabila laporan perbelanjaan dicipta, lakukan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="2edd9-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="2edd9-113">Buka ruang kerja **Pengurusan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="2edd9-114">Pada tab **Resit** , sahkan resit tidak dilampirkan wujud.</span><span class="sxs-lookup"><span data-stu-id="2edd9-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="2edd9-115">Anda juga boleh muat naik resit pada tab **Resit**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="2edd9-116">Pada tab **Perbelanjaan** , sahkan perbelanjaan tidak dilampirkan wujud.</span><span class="sxs-lookup"><span data-stu-id="2edd9-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="2edd9-117">Kebiasaannya, pentadbir perbelanjaan mengimport perbelanjaan ini daripada pembekal kad kredit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="2edd9-118">Pilih **Laporan perbelanjaan baharu**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-118">Select **New expense report**.</span></span> <span data-ttu-id="2edd9-119">Perhatikan bahawa anda boleh memasukkan perbelanjaan dan resit, kini juga, apabila anda mencipta laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="2edd9-120">Jika anda menambah kedua-dua perbelanjaan dan resit, pemadanan automatik bagi resit berbanding perbelanjaan dicetuskan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="2edd9-121">Untuk mencipta perbelanjaan atau memadankan perbelanjaan daripada resit, lakukan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="2edd9-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="2edd9-122">Pada laporan perbelanjaan, pada tab **Resit** , lampirkan resit dengan memilih **Tambah resit**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="2edd9-123">Di bawah imej yang dimuat naik resit, perhatikan pilihan **Cipta** dan **Padan**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="2edd9-124">Pilih **Cipta** untuk mencipta transaksi perbelanjaan yang dimasukkan secara manual dan isikan nilai yang diekstrak daripada resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="2edd9-125">Jika anda memilih **Padan** , sistem cuba memadankan perbelanjaan sedia ada kepada resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="2edd9-126">Pemasangan</span><span class="sxs-lookup"><span data-stu-id="2edd9-126">Installation</span></span>

<span data-ttu-id="2edd9-127">Ciri ini berfungsi bersama dengan ciri **Laporan perbelanjaan dibentuk semula** untuk membantu meringkaskan pengalaman perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="2edd9-128">Ciri ini hanya tersedia untuk persekitaran Peringkat 2+, yang merupakan Kotak pasir dan Pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="2edd9-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="2edd9-129">Untuk menggunakan keupayaan perbelanjaan lanjutan ini, pasang tambahan Perkhidmatan Pengurusan Perbelanjaan for Microsoft Dynamics 365 Finance dan hidupkan ciri dalam tika anda.</span><span class="sxs-lookup"><span data-stu-id="2edd9-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="2edd9-130">Anda boleh mengakses tambahan daripada projek anda dalam Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2edd9-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2edd9-131">Log masuk ke dalam LCS dan buka persekitaran yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="2edd9-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="2edd9-132">Pergi ke **Butiran penuh**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="2edd9-133">Pilih **Kekalkan** atau tatal ke bawah ke FastTab **Tambahan persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="2edd9-134">Pilih **Pasangkan tambahan baharu**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="2edd9-135">Pilih **Perkhidmatan Pengurusan Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="2edd9-136">Ikuti panduan pemasangan dan bersetuju dengan terma dan syarat.</span><span class="sxs-lookup"><span data-stu-id="2edd9-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="2edd9-137">Pilih **Pasang**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-137">Select **Install**.</span></span>

<span data-ttu-id="2edd9-138">Dalam ruang kerja **Pengurusan ciri** , hidupkan ciri berikut:</span><span class="sxs-lookup"><span data-stu-id="2edd9-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="2edd9-139">Laporan perbelanjaan digambarkan semula</span><span class="sxs-lookup"><span data-stu-id="2edd9-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="2edd9-140">Padankan secara automatik dan cipta perbelanjaan daripada resit</span><span class="sxs-lookup"><span data-stu-id="2edd9-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="2edd9-141">Apabila anda menghidupkan ciri ini, tindakan berikut berlaku:</span><span class="sxs-lookup"><span data-stu-id="2edd9-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="2edd9-142">Ruang kerja **Pengurusan perbelanjaan** sedia ada diganti dengan ruang kerja baharu.</span><span class="sxs-lookup"><span data-stu-id="2edd9-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2edd9-143">Item menu baharu untuk keterlihatan medan perbelanjaan ditambah.</span><span class="sxs-lookup"><span data-stu-id="2edd9-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2edd9-144">Anda masih boleh membuka halaman **Laporan perbelanjaan** dengan pergi ke **Pengurusan perbelanjaan > Perbelanjaan saya > Laporan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="2edd9-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="2edd9-145">Aliran kerja dan sebarang kelulusan masih akan membawa anda ke halaman laporan perbelanjaan sedia ada.</span><span class="sxs-lookup"><span data-stu-id="2edd9-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="2edd9-146">Resit akan diproses melalui Microsoft Azure Cognitive Services dan metadata akan diekstrak dan ditambah.</span><span class="sxs-lookup"><span data-stu-id="2edd9-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="2edd9-147">Pilihan ditambah membolehkan anda mencipta laporan perbelanjaan yang merangkumi resit yang tidak dilampirkan dipadankan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="2edd9-148">Pilihan yang ditambahkan ke laporan perbelanjaan membolehkan anda mencipta baris perbelanjaan daripada resit atau cuba untuk memadankan resit sedia ada ke baris perbelanjaan sedia ada.</span><span class="sxs-lookup"><span data-stu-id="2edd9-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="2edd9-149">Untuk mendapatkan maklumat lanjut tentang ciri Laporan perbelanjaan dibentuk semula, lihat [Laporan perbelanjaan dibentuk semula](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="2edd9-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2edd9-150">Soalan lazim</span><span class="sxs-lookup"><span data-stu-id="2edd9-150">Frequently asked questions</span></span>

<span data-ttu-id="2edd9-151">**Adakah Microsoft menggunakan data saya untuk modelnya?**</span><span class="sxs-lookup"><span data-stu-id="2edd9-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="2edd9-152">Tidak, Microsoft telah membina model pembelajaran mesin umum untuk perkhidmatan pemprosesan penerimaannya.</span><span class="sxs-lookup"><span data-stu-id="2edd9-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="2edd9-153">Model ini tidak berasaskan pada resit yang anda muat naik.</span><span class="sxs-lookup"><span data-stu-id="2edd9-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="2edd9-154">**Di manakah ciri ini tersedia dan diproses?**</span><span class="sxs-lookup"><span data-stu-id="2edd9-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="2edd9-155">Pada masa ini, Amerika Syarikat disokong.</span><span class="sxs-lookup"><span data-stu-id="2edd9-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="2edd9-156">**Di manakah resit saya pergi?**</span><span class="sxs-lookup"><span data-stu-id="2edd9-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="2edd9-157">Kewangan akan menghubungi Perkhidmatan Kognitif untuk mengekstrak data medan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="2edd9-158">Perkhidmatan Kognitif akan menyimpan salinan resit anda untuk tempoh masa hingga 24 jam selepas pemprosesan berlaku.</span><span class="sxs-lookup"><span data-stu-id="2edd9-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="2edd9-159">Selepas pemprosesan selesai, Perkhidmatan Kognitif akan mengalih keluar resit.</span><span class="sxs-lookup"><span data-stu-id="2edd9-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="2edd9-160">Resit masih disimpan dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="2edd9-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="2edd9-161">Untuk maklumat lanjut, lihat [Dayakan pemahaman resit dengan keupayaan baharu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="2edd9-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
