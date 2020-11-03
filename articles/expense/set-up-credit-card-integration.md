---
title: Sediakan integrasi kad kredit
description: Topik ini menerangkan cara mengimport dan mengekalkan transaksi kad kredit yang berkaitan dengan perbelanjaan.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081191"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="46373-103">Sediakan integrasi kad kredit</span><span class="sxs-lookup"><span data-stu-id="46373-103">Set up credit card integration</span></span>

<span data-ttu-id="46373-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="46373-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46373-105">Transaksi kad kredit berkaitan perbelanjaan boleh ditetapkan supaya ia diimport secara automatik pada jadual yang berulang.</span><span class="sxs-lookup"><span data-stu-id="46373-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="46373-106">Secara alternatif, transaksi boleh diimport secara manual apabila diperlukan.</span><span class="sxs-lookup"><span data-stu-id="46373-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="46373-107">Transaksi kad kredit diimport melalui entiti data transaksi kad Kredit.</span><span class="sxs-lookup"><span data-stu-id="46373-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="46373-108">Import transaksi kad kredit</span><span class="sxs-lookup"><span data-stu-id="46373-108">Import credit card transactions</span></span>

1. <span data-ttu-id="46373-109">Pada halaman **Transaksi kad kredit** , pilih **Import transaksi**.</span><span class="sxs-lookup"><span data-stu-id="46373-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="46373-110">Jika anda sedang membuka pengurusan data buat kali pertama, sistem mesti mengemas kini senarai entiti data sebelum anda boleh meneruskan.</span><span class="sxs-lookup"><span data-stu-id="46373-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="46373-111">Dalam medan **Nama** , masukkan description unik bagi kerja import.</span><span class="sxs-lookup"><span data-stu-id="46373-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="46373-112">Dalam medan **Format data sumber** , pilih format fail yang mengandungi transaksi kad kredit untuk diimport.</span><span class="sxs-lookup"><span data-stu-id="46373-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="46373-113">Pilih **Muat naik** dan kemudian cari serta pilih fail untuk diimport.</span><span class="sxs-lookup"><span data-stu-id="46373-113">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="46373-114">Selepas fail dimuat naik, sahkan fail transaksi kad kredit dan lajur entiti data transaksi kad kredit dengan memilih pautan **Lihat peta** pada jubin.</span><span class="sxs-lookup"><span data-stu-id="46373-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="46373-115">Jika terdapat ralat pemetaan atau jika anda mesti mengubah pemetaan, membuat perubahan pemetaan sama ada dalam tab **Visualisasi Pemetaan** atau tab **Butiran Pemetaan**.</span><span class="sxs-lookup"><span data-stu-id="46373-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="46373-116">Untuk mengautomasikan transaksi kad kredit, pilih **Cipta kerja data berulang**.</span><span class="sxs-lookup"><span data-stu-id="46373-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="46373-117">Anda kemudian boleh menetapkan pengulangan yang menakrifkan kekerapan transaksi kad kredit diimport.</span><span class="sxs-lookup"><span data-stu-id="46373-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="46373-118">Apabila anda telah selesai, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="46373-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="46373-119">Untuk mengimport fail yang dipilih sekarang, pilih **Import**.</span><span class="sxs-lookup"><span data-stu-id="46373-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="46373-120">Jika ralat berlaku semasa import, anda boleh melihat log pelaksanaan atau data pementasan untuk melihat ralat yang mesti anda baiki bagi membantu menjamin import yang berjaya.</span><span class="sxs-lookup"><span data-stu-id="46373-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="46373-121">Jika anda mesti mengimport lebih daripada satu format fail, anda mesti mencipta kerja import berasingan untuk setiap jenis format.</span><span class="sxs-lookup"><span data-stu-id="46373-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="46373-122">Tugaskan semula transaksi kad kredit untuk pekerja yang telah ditamatkan</span><span class="sxs-lookup"><span data-stu-id="46373-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="46373-123">Selepas rekod pekerja ditamatkan, akaun Active Directory Domain Services (AD DS) pekerja dinyahdayakan.</span><span class="sxs-lookup"><span data-stu-id="46373-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="46373-124">Walau bagaimanapun, kemungkinan terdapat transaksi kad kredit aktif yang masih perlu dibelanjakan dan dibayar balik.</span><span class="sxs-lookup"><span data-stu-id="46373-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="46373-125">Daripada halaman **Transaksi kad kredit** , anda boleh menugaskan semula pekerja untuk sebarang transaksi kad kredit bagi pekerja berkaitan yang telah ditamatkan.</span><span class="sxs-lookup"><span data-stu-id="46373-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="46373-126">Pilih satu atau lebih transaksi kad kredit dan kemudian pilih **Tugaskan semula transaksi**.</span><span class="sxs-lookup"><span data-stu-id="46373-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="46373-127">Anda kemudian boleh memilih pekerja lain untuk transaksi kad kredit yang ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="46373-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="46373-128">Selepas transaksi kad kredit telah ditugaskan semula, ia boleh dipilih untuk laporan perbelanjaan dan dibayar melalui proses biasa bagi pembayaran balik laporan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="46373-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
