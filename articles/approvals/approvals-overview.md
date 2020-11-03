---
title: Gambaran keseluruhan kelulusan
description: Topik ini memberikan maklumat tentang bekerja dengan kelulusan dalam Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081088"
---
# <a name="approvals-overview"></a><span data-ttu-id="eeaec-103">Gambaran keseluruhan kelulusan</span><span class="sxs-lookup"><span data-stu-id="eeaec-103">Approvals overview</span></span>

<span data-ttu-id="eeaec-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="eeaec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eeaec-105">Serahan Masa dan Perbelanjaan bergerak melalui aliran kerja kelulusan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="eeaec-106">Selepas entri diluluskan, transaksi direkodkan dalam aktual atau masa ditempah dalam jadual.</span><span class="sxs-lookup"><span data-stu-id="eeaec-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="eeaec-107">Aliran kerja kelulusan</span><span class="sxs-lookup"><span data-stu-id="eeaec-107">Approvals workflow</span></span>
<span data-ttu-id="eeaec-108">Apabila anda mencipta dan menyerahkan entri masa atau perbelanjaan, entri kelulusan akan dicipta.</span><span class="sxs-lookup"><span data-stu-id="eeaec-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="eeaec-109">Pelulus Projek atau pengurus anda menyemak dan meluluskan entri anda.</span><span class="sxs-lookup"><span data-stu-id="eeaec-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="eeaec-110">Jika entri berkaitan dengan projek, apabila ia diluluskan, aktual akan dicipta.</span><span class="sxs-lookup"><span data-stu-id="eeaec-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="eeaec-111">Ini membolehkan kos dan pengebilan dijejak.</span><span class="sxs-lookup"><span data-stu-id="eeaec-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="eeaec-112">Meluluskan entri</span><span class="sxs-lookup"><span data-stu-id="eeaec-112">Approve an entry</span></span>
<span data-ttu-id="eeaec-113">Borang **Kelulusan** membolehkan anda bertukar antara pandangan yang berbeza supaya anda boleh melihat jenis kelulusan yang berbeza.</span><span class="sxs-lookup"><span data-stu-id="eeaec-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="eeaec-114">Pergi ke borang **Kelulusan** dan pilih **Perbelanjaan** , **Masa** atau **Tarik balik**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="eeaec-115">Semak setiap kelulusan dan pilih kelulusan yang anda mahu luluskan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="eeaec-116">Pilih **Luluskan** untuk meluluskan entri yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="eeaec-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="eeaec-117">Sistem akan memproses entri ini dan mencipta aktual atau tempahan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="eeaec-118">Tolak entri</span><span class="sxs-lookup"><span data-stu-id="eeaec-118">Reject an entry</span></span>
<span data-ttu-id="eeaec-119">Sebagai pelulus Projek, anda mungkin perlu menghantar semula entri kepada pengguna untuk pembetulan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="eeaec-120">Pergi ke borang **Kelulusan** dan pilih entri untuk ditolak.</span><span class="sxs-lookup"><span data-stu-id="eeaec-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="eeaec-121">Pilih **Tolak**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-121">Select **Reject**.</span></span>
3. <span data-ttu-id="eeaec-122">Pilihan - Tambah komen dalam dialog **Komen penolakan** untuk memberitahu pengguna sebab entri tersebut ditolak.</span><span class="sxs-lookup"><span data-stu-id="eeaec-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="eeaec-123">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-123">Select **OK**.</span></span> <span data-ttu-id="eeaec-124">Entri tersebut akan dikembalikan kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="eeaec-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="eeaec-125">Tarik balik entri</span><span class="sxs-lookup"><span data-stu-id="eeaec-125">Recall entries</span></span>
<span data-ttu-id="eeaec-126">Pada satu ketika, anda mungkin perlu menarik balik entri yang telah diserahkan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="eeaec-127">Jika entri tersebut tidak diluluskan, ia akan dikembalikan dengan segera.</span><span class="sxs-lookup"><span data-stu-id="eeaec-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="eeaec-128">Entri yang telah diluluskan bagaimanapun, mungkin mempunyai kesan bahan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="eeaec-129">Pelulus Projek dikehendaki meluluskan tarik balik ini untuk membalikkan transaksi dalam Aktual.</span><span class="sxs-lookup"><span data-stu-id="eeaec-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="eeaec-130">Nyatakan Pelulus projek</span><span class="sxs-lookup"><span data-stu-id="eeaec-130">Specify Project approvers</span></span>
<span data-ttu-id="eeaec-131">Setiap projek mempunyai beberapa orang ahli pasukan projek.</span><span class="sxs-lookup"><span data-stu-id="eeaec-131">Each project has a number of project team members.</span></span> <span data-ttu-id="eeaec-132">Anda boleh menentukan ahli pasukan yang juga merupakan pelulus projek.</span><span class="sxs-lookup"><span data-stu-id="eeaec-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="eeaec-133">Pergi ke borang **Projek** dan buka projek daripada senarai.</span><span class="sxs-lookup"><span data-stu-id="eeaec-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="eeaec-134">Pada tab **Pasukan** , pilih ahli pasukan yang akan menjadi Pelulus projek dan kemudian pilih **Edit**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="eeaec-135">Tetapkan medan **Pelulus Projek** kepada **Ya**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="eeaec-136">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-136">Select **Save**.</span></span>
5. <span data-ttu-id="eeaec-137">Ulangi langkah 2-4 untuk menambah Pelulus projek tambahan.</span><span class="sxs-lookup"><span data-stu-id="eeaec-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="eeaec-138">Konfigurasikan pengurus pengguna</span><span class="sxs-lookup"><span data-stu-id="eeaec-138">Configure the user's manager</span></span>

1. <span data-ttu-id="eeaec-139">Pergi ke **Tetapan** > **Keselamatan** > **Pengguna**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="eeaec-140">Pilih pengguna yang anda akan tugaskan seorang pengurus dan dalam kawasan **Maklumat Organisasi** , pilih pengurus daripada senarai.</span><span class="sxs-lookup"><span data-stu-id="eeaec-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="eeaec-141">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="eeaec-141">Select **Save**.</span></span>


