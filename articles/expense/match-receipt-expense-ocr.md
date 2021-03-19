---
title: Rekodkan resit menggunakan OCR
description: Topik ini menyediakan maklumat tentang pemprosesan pengecaman aksara optik (OCR) untuk resit.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499862"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="53091-103">Rekodkan resit menggunakan OCR</span><span class="sxs-lookup"><span data-stu-id="53091-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="53091-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="53091-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="53091-105">Entri perbelanjaan telah dipertingkatkan melalui pengenalan pemprosesan pengecaman aksara optik (OCR) untuk resit.</span><span class="sxs-lookup"><span data-stu-id="53091-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="53091-106">Fungsian ini direka bentuk untuk meningkatkan pengalaman pengguna semasa mencipta laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="53091-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="53091-107">Ciri utama</span><span class="sxs-lookup"><span data-stu-id="53091-107">Key features</span></span>

- <span data-ttu-id="53091-108">Sistem mengekstrak nama saudagar, tarikh dan amaun jumlah daripada resit.</span><span class="sxs-lookup"><span data-stu-id="53091-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="53091-109">Sistem akan cuba memadankan resit yang tidak dilampirkan untuk transaksi perbelanjaan tidak dilampirkan.</span><span class="sxs-lookup"><span data-stu-id="53091-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="53091-110">Anda boleh mencipta transaksi perbelanjaan secara manual daripada resit.</span><span class="sxs-lookup"><span data-stu-id="53091-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="53091-111">Lampirkan resit ke laporan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="53091-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="53091-112">Untuk melampirkan resit secara automatik termasuk transaksi kad kredit apabila laporan perbelanjaan dicipta, lengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="53091-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="53091-113">Buka ruang kerja **Pengurusan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="53091-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="53091-114">Pada tab **Resit**, sahkan resit tidak dilampirkan wujud.</span><span class="sxs-lookup"><span data-stu-id="53091-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="53091-115">Anda juga boleh muat naik resit pada tab **Resit**.</span><span class="sxs-lookup"><span data-stu-id="53091-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="53091-116">Pada tab **Perbelanjaan**, sahkan perbelanjaan tidak dilampirkan wujud.</span><span class="sxs-lookup"><span data-stu-id="53091-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="53091-117">Kebiasaannya, pentadbir perbelanjaan mengimport perbelanjaan ini daripada pembekal kad kredit.</span><span class="sxs-lookup"><span data-stu-id="53091-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="53091-118">Pilih **Laporan perbelanjaan baharu**.</span><span class="sxs-lookup"><span data-stu-id="53091-118">Select **New expense report**.</span></span> <span data-ttu-id="53091-119">Perhatikan bahawa anda boleh memasukkan perbelanjaan dan resit, kini juga, apabila anda mencipta laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="53091-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="53091-120">Jika anda menambah kedua-dua perbelanjaan dan resit, pemadanan automatik bagi resit berbanding perbelanjaan dicetuskan.</span><span class="sxs-lookup"><span data-stu-id="53091-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="53091-121">Cipta dan padan resit ke laporan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="53091-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="53091-122">Untuk mencipta perbelanjaan atau memadankan perbelanjaan daripada resit, lengkapkan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="53091-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="53091-123">Pada laporan perbelanjaan, pada tab **Resit**, lampirkan resit dengan memilih **Tambah resit**.</span><span class="sxs-lookup"><span data-stu-id="53091-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="53091-124">Di bawah imej yang dimuat naik resit, perhatikan pilihan **Cipta** dan **Padan**.</span><span class="sxs-lookup"><span data-stu-id="53091-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="53091-125">Pilih **Cipta** untuk mencipta transaksi perbelanjaan yang dimasukkan secara manual dan isikan nilai yang diekstrak daripada resit.</span><span class="sxs-lookup"><span data-stu-id="53091-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="53091-126">Jika anda memilih **Padan**, sistem cuba memadankan perbelanjaan sedia ada kepada resit.</span><span class="sxs-lookup"><span data-stu-id="53091-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="53091-127">Pemasangan</span><span class="sxs-lookup"><span data-stu-id="53091-127">Installation</span></span>

<span data-ttu-id="53091-128">Untuk menggunakan keupayaan perbelanjaan lanjutan ini, pasang tambahan Perkhidmatan Pengurusan Perbelanjaan for Microsoft Dynamics 365 Finance dan hidupkan ciri dalam tika anda.</span><span class="sxs-lookup"><span data-stu-id="53091-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="53091-129">Anda boleh mengakses tambahan daripada projek anda dalam Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="53091-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="53091-130">Log masuk ke dalam LCS dan buka persekitaran yang dikehendaki.</span><span class="sxs-lookup"><span data-stu-id="53091-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="53091-131">Pergi ke **Butiran penuh**.</span><span class="sxs-lookup"><span data-stu-id="53091-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="53091-132">Pilih **Kekalkan** atau tatal ke bawah ke FastTab **Tambahan persekitaran**.</span><span class="sxs-lookup"><span data-stu-id="53091-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="53091-133">Pilih **Pasangkan tambahan baharu**.</span><span class="sxs-lookup"><span data-stu-id="53091-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="53091-134">Pilih **Perkhidmatan Pengurusan Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="53091-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="53091-135">Ikuti panduan pemasangan dan bersetuju dengan terma dan syarat.</span><span class="sxs-lookup"><span data-stu-id="53091-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="53091-136">Pilih **Pasang**.</span><span class="sxs-lookup"><span data-stu-id="53091-136">Select **Install**.</span></span>

<span data-ttu-id="53091-137">Dalam ruang kerja **Pengurusan ciri**, hidupkan ciri berikut:</span><span class="sxs-lookup"><span data-stu-id="53091-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="53091-138">Laporan perbelanjaan digambarkan semula</span><span class="sxs-lookup"><span data-stu-id="53091-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="53091-139">Padankan secara automatik dan cipta perbelanjaan daripada resit</span><span class="sxs-lookup"><span data-stu-id="53091-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="53091-140">Apabila anda menghidupkan ciri ini, tindakan berikut berlaku:</span><span class="sxs-lookup"><span data-stu-id="53091-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="53091-141">Ruang kerja **Pengurusan perbelanjaan** sedia ada diganti dengan ruang kerja baharu.</span><span class="sxs-lookup"><span data-stu-id="53091-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="53091-142">Item menu baharu untuk keterlihatan medan perbelanjaan ditambah.</span><span class="sxs-lookup"><span data-stu-id="53091-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="53091-143">Anda masih boleh membuka halaman **Laporan perbelanjaan** dengan pergi ke **Pengurusan perbelanjaan > Perbelanjaan saya > Laporan perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="53091-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="53091-144">Aliran kerja dan sebarang kelulusan masih akan membawa anda ke halaman laporan perbelanjaan sedia ada.</span><span class="sxs-lookup"><span data-stu-id="53091-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="53091-145">Resit akan diproses melalui Microsoft Azure Cognitive Services dan metadata akan diekstrak dan ditambah.</span><span class="sxs-lookup"><span data-stu-id="53091-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="53091-146">Pilihan ditambah membolehkan anda mencipta laporan perbelanjaan yang merangkumi resit yang tidak dilampirkan dipadankan.</span><span class="sxs-lookup"><span data-stu-id="53091-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="53091-147">Pilihan yang ditambahkan ke laporan perbelanjaan membolehkan anda mencipta baris perbelanjaan daripada resit atau cuba untuk memadankan resit sedia ada ke baris perbelanjaan sedia ada.</span><span class="sxs-lookup"><span data-stu-id="53091-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="53091-148">Soalan lazim</span><span class="sxs-lookup"><span data-stu-id="53091-148">Frequently asked questions</span></span>

<span data-ttu-id="53091-149">**Adakah Microsoft menggunakan data saya untuk modelnya?**</span><span class="sxs-lookup"><span data-stu-id="53091-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="53091-150">Tidak, Microsoft telah membina model pembelajaran mesin umum untuk perkhidmatan pemprosesan penerimaannya.</span><span class="sxs-lookup"><span data-stu-id="53091-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="53091-151">Model ini tidak berasaskan pada resit yang anda muat naik.</span><span class="sxs-lookup"><span data-stu-id="53091-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="53091-152">**Di manakah ciri ini tersedia dan diproses?**</span><span class="sxs-lookup"><span data-stu-id="53091-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="53091-153">Pada masa ini, Amerika Syarikat disokong.</span><span class="sxs-lookup"><span data-stu-id="53091-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="53091-154">**Di manakah resit saya pergi?**</span><span class="sxs-lookup"><span data-stu-id="53091-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="53091-155">Kewangan akan menghubungi Perkhidmatan Kognitif untuk mengekstrak data medan.</span><span class="sxs-lookup"><span data-stu-id="53091-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="53091-156">Perkhidmatan Kognitif akan menyimpan salinan resit anda untuk tempoh masa hingga 24 jam selepas pemprosesan berlaku.</span><span class="sxs-lookup"><span data-stu-id="53091-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="53091-157">Selepas pemprosesan selesai, Perkhidmatan Kognitif akan mengalih keluar resit.</span><span class="sxs-lookup"><span data-stu-id="53091-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="53091-158">Resit masih disimpan dalam Kewangan.</span><span class="sxs-lookup"><span data-stu-id="53091-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="53091-159">Untuk maklumat lanjut, lihat [Dayakan pemahaman resit dengan keupayaan baharu Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="53091-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
