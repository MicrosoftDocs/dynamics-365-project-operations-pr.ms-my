---
title: Import dan selenggara transaksi kad kredit
description: Topik ini menerangkan cara mengimport dan mengekalkan transaksi kad kredit yang berkaitan dengan perbelanjaan. Transaksi ini boleh disediakan supaya ia diimport secara automatik pada jadual yang berulang, atau ia boleh diimport secara manual mengikut keperluan.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005172"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="276b6-104">Import dan selenggara transaksi kad kredit</span><span class="sxs-lookup"><span data-stu-id="276b6-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="276b6-105">Transaksi kad kredit berkaitan perbelanjaan boleh ditetapkan supaya ia diimport secara automatik pada jadual yang berulang.</span><span class="sxs-lookup"><span data-stu-id="276b6-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="276b6-106">Secara alternatif, transaksi boleh diimport secara manual apabila diperlukan.</span><span class="sxs-lookup"><span data-stu-id="276b6-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="276b6-107">Transaksi kad kredit diimport melalui entiti data transaksi kad Kredit.</span><span class="sxs-lookup"><span data-stu-id="276b6-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="276b6-108">Untuk mendapatkan maklumat lanjut tentang entiti data, lihat [Entiti data](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="276b6-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="276b6-109">Import transaksi kad kredit</span><span class="sxs-lookup"><span data-stu-id="276b6-109">Import credit card transactions</span></span>

1. <span data-ttu-id="276b6-110">Pada halaman **Transaksi kad kredit**, pilih **Import transaksi**.</span><span class="sxs-lookup"><span data-stu-id="276b6-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="276b6-111">Jika anda sedang membuka pengurusan data buat kali pertama, sistem mesti mengemas kini senarai entiti data sebelum anda boleh meneruskan.</span><span class="sxs-lookup"><span data-stu-id="276b6-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="276b6-112">Dalam medan **Nama**, masukkan description unik bagi kerja import.</span><span class="sxs-lookup"><span data-stu-id="276b6-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="276b6-113">Dalam medan **Format data sumber**, pilih format fail yang mengandungi transaksi kad kredit untuk diimport.</span><span class="sxs-lookup"><span data-stu-id="276b6-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="276b6-114">Pilih **Muat naik** dan kemudian cari serta pilih fail untuk diimport.</span><span class="sxs-lookup"><span data-stu-id="276b6-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="276b6-115">Selepas fail dimuat naik, sahkan fail transaksi kad kredit dan lajur entiti data transaksi kad kredit dengan memilih pautan **Lihat peta** pada jubin.</span><span class="sxs-lookup"><span data-stu-id="276b6-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="276b6-116">Jika terdapat ralat pemetaan atau jika anda mesti mengubah pemetaan, membuat perubahan pemetaan sama ada dalam tab **Visualisasi Pemetaan** atau tab **Butiran Pemetaan**.</span><span class="sxs-lookup"><span data-stu-id="276b6-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="276b6-117">Untuk mengautomasikan transaksi kad kredit, pilih **Cipta kerja data berulang**.</span><span class="sxs-lookup"><span data-stu-id="276b6-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="276b6-118">Anda kemudian boleh menetapkan pengulangan yang menakrifkan kekerapan transaksi kad kredit diimport.</span><span class="sxs-lookup"><span data-stu-id="276b6-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="276b6-119">Apabila anda telah selesai, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="276b6-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="276b6-120">Untuk mengimport fail yang dipilih sekarang, pilih **Import**.</span><span class="sxs-lookup"><span data-stu-id="276b6-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="276b6-121">Jika ralat berlaku semasa import, anda boleh melihat log pelaksanaan atau data pementasan untuk melihat ralat yang mesti anda baiki bagi membantu menjamin import yang berjaya.</span><span class="sxs-lookup"><span data-stu-id="276b6-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="276b6-122">Jika anda mesti mengimport lebih daripada satu format fail, anda mesti mencipta kerja import berasingan untuk setiap jenis format.</span><span class="sxs-lookup"><span data-stu-id="276b6-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="276b6-123">Tugaskan semula transaksi kad kredit untuk pekerja yang telah ditamatkan</span><span class="sxs-lookup"><span data-stu-id="276b6-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="276b6-124">Selepas rekod pekerja ditamatkan, akaun Active Directory Domain Services (AD DS) pekerja dinyahdayakan.</span><span class="sxs-lookup"><span data-stu-id="276b6-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="276b6-125">Walau bagaimanapun, kemungkinan terdapat transaksi kad kredit aktif yang masih perlu dibelanjakan dan dibayar balik.</span><span class="sxs-lookup"><span data-stu-id="276b6-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="276b6-126">Daripada halaman **Transaksi kad kredit**, anda boleh menugaskan semula pekerja untuk sebarang transaksi kad kredit bagi pekerja berkaitan yang telah ditamatkan.</span><span class="sxs-lookup"><span data-stu-id="276b6-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="276b6-127">Pilih satu atau lebih transaksi kad kredit dan kemudian pilih **Tugaskan semula transaksi**.</span><span class="sxs-lookup"><span data-stu-id="276b6-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="276b6-128">Anda kemudian boleh memilih pekerja lain untuk transaksi kad kredit yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="276b6-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="276b6-129">Selepas transaksi kad kredit telah ditugaskan semula, ia boleh dipilih untuk laporan perbelanjaan dan dibayar melalui proses biasa bagi pembayaran balik laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="276b6-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]