---
title: Anggaran perbelanjaan
description: Topik ini memberikan maklumat mengenai mentakrifkan atau menganggarkan perbelanjaan berasaskan projek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081150"
---
# <a name="expense-estimates"></a><span data-ttu-id="e79f0-103">Anggaran perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="e79f0-103">Expense estimates</span></span>
<span data-ttu-id="e79f0-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="e79f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e79f0-105">Bersama dengan mentakrifkan anggaran berasaskan sumber, Operasi Projek Dynamics 365 membolehkan pengurus projek mentakrifkan perbelanjaan berasaskan projek untuk setiap projek.</span><span class="sxs-lookup"><span data-stu-id="e79f0-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="e79f0-106">Setiap item perbelanjaan boleh dikaitkan dengan peranan atau kategori projek tertentu.</span><span class="sxs-lookup"><span data-stu-id="e79f0-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="e79f0-107">Kategori perbelanjaan biasanya ditakrifkan pada peringkat organisasi.</span><span class="sxs-lookup"><span data-stu-id="e79f0-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="e79f0-108">Penetapan harga untuk setiap kategori perbelanjaan biasanya ditakrifkan dalam hierarki yang berikut:</span><span class="sxs-lookup"><span data-stu-id="e79f0-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="e79f0-109">Organisasi</span><span class="sxs-lookup"><span data-stu-id="e79f0-109">Organization</span></span>
- <span data-ttu-id="e79f0-110">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="e79f0-110">Customer</span></span>
- <span data-ttu-id="e79f0-111">Sebut harga/kontrak</span><span class="sxs-lookup"><span data-stu-id="e79f0-111">Quote/contract</span></span>

<span data-ttu-id="e79f0-112">Lengkapkan langkah berikut untuk melihat, menambah atau memadamkan perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="e79f0-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="e79f0-113">Pergi ke **Projek** dan pilih projek yang anda mahu usahakan.</span><span class="sxs-lookup"><span data-stu-id="e79f0-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="e79f0-114">Pilih tab **Anggaran Projek** dan lihat senarai perbelanjaan projek.</span><span class="sxs-lookup"><span data-stu-id="e79f0-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="e79f0-115">Pilih **Perbelanjaan Baharu** untuk menambahkan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e79f0-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="e79f0-116">Atau pilih satu belanja untuk dipadamkan dan kemudian pilih **Padamkan Perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="e79f0-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="e79f0-117">Atribut berikut ditakrifkan untuk setiap item baris perbelanjaan:</span><span class="sxs-lookup"><span data-stu-id="e79f0-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="e79f0-118">**Kategori** : Kumpulan biasa yang digunakan untuk menjelaskan semua perbelanjaan yang dilakukan ke atas projek.</span><span class="sxs-lookup"><span data-stu-id="e79f0-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="e79f0-119">**Tarikh Mula** : Tarikh apabila perbelanjaan diramalkan akan ditanggung.</span><span class="sxs-lookup"><span data-stu-id="e79f0-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="e79f0-120">**Kuantiti** : Anggaran bilangan item perbelanjaan untuk kategori tertentu.</span><span class="sxs-lookup"><span data-stu-id="e79f0-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="e79f0-121">**Unit Harga Kos** : Harga unit yang digunakan untuk pengiraan kos perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e79f0-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="e79f0-122">**Unit Harga Jualan** : Harga unit yang digunakan untuk pengiraan harga jualan perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="e79f0-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

