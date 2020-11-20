---
title: Mengapakah harga ditetapkan lalai kepada sifar pada masa kos sebenar?
description: Penyelesaian masalah sebab harga ditetapkan lalai kepada 0 pada masa kos sebenar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131385"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="8d89c-103">Mengapakah harga ditetapkan lalai kepada sifar pada masa kos sebenar?</span><span class="sxs-lookup"><span data-stu-id="8d89c-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8d89c-104">Soalan lazim (FAQ) ini digunakan untuk kelas transaksi sebenar ditetapkan kepada Masa dan jenis transaksi adalah Kos.</span><span class="sxs-lookup"><span data-stu-id="8d89c-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="8d89c-105">Tiga semakan berikut akan membantu anda menyelesaikan masalah sebab harga ditetapkan lalai kepada 0 pada masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="8d89c-106">Semak 1: Kenal pasti senarai harga kos untuk projek</span><span class="sxs-lookup"><span data-stu-id="8d89c-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="8d89c-107">Cari projek dari medan projek sebenar dan kemudian pergi ke halaman projek.</span><span class="sxs-lookup"><span data-stu-id="8d89c-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="8d89c-108">Klik pada pautan unit kontrak dalam medan.</span><span class="sxs-lookup"><span data-stu-id="8d89c-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="8d89c-109">Pada halaman Unit Kontrak, semak jika unit kontrak mempunyai senarai harga dalam grid Senarai Harga Kos.</span><span class="sxs-lookup"><span data-stu-id="8d89c-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="8d89c-110">Jika terdapat lebih daripada satu senarai harga, anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="8d89c-111">Project Service hanya menyokong satu senarai harga setiap unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="8d89c-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="8d89c-112">Keluarkan semua senarai harga daripada entiti ini sehingga terdapat hanya satu senarai harga yang dilampirkan dalam grid Senarai Harga Kos Unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="8d89c-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="8d89c-113">Jika tiada senarai harga yang dilampirkan pada Unit Organisasi, buat catatan mata wang unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="8d89c-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="8d89c-114">Pergi ke Project Service dan kemudian Parameter dan buka tab Senarai Harga. Semak jika terdapat mana-mana senarai harga dengan konteks ditetapkan kepada Kos dan mata wang yang sepadan dengan mata wang Unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="8d89c-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="8d89c-115">Jika tiada senarai harga yang sepadan dengan kriteria itu, anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="8d89c-116">Pastikan anda mempunyai sekurang-kurangnya satu senarai harga yang konteksnya ditetapkan kepada Kos dan mata wangnya sepadan dengan mata wang Unit Organisasi.</span><span class="sxs-lookup"><span data-stu-id="8d89c-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="8d89c-117">Jika terdapat lebih daripada satu senarai harga yang sepadan dengan kriteria itu, teruskan membaca dokumen ini untuk membuat lebih banyak semakan.</span><span class="sxs-lookup"><span data-stu-id="8d89c-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="8d89c-118">Semak 2: Adakah mana-mana senarai harga yang dikenal pasti di atas sah untuk tarikh tertentu bagi masa kos sebenar?</span><span class="sxs-lookup"><span data-stu-id="8d89c-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="8d89c-119">Untuk Project Service mempertimbangkan senarai harga untuk menetapkan harga lalai, senarai harga itu seharusnya boleh digunakan untuk tarikh pada masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="8d89c-120">Semak perkara berikut untuk melihat jika senarai harga yang dikenal pasti di atas boleh digunakan:</span><span class="sxs-lookup"><span data-stu-id="8d89c-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="8d89c-121">Semak jika tarikh mula dan akhir pada tab umum untuk senarai harga yang dilampirkan tidak kosong.</span><span class="sxs-lookup"><span data-stu-id="8d89c-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="8d89c-122">Jika tarikh mula dan akhir pada senarai harga yang dikenal pasti di atas adalah kosong, anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="8d89c-123">Buat catatan medan tarikh mula pada masa kos sebenar dan semak jika mana-mana senarai harga yang dikenal pasti boleh digunakan untuk tarikh itu.</span><span class="sxs-lookup"><span data-stu-id="8d89c-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="8d89c-124">Sebagai contoh, tarikh masa kos sebenar seharusnya jatuh pada tarikh mula dan tarikh akhir pada senarai harga.</span><span class="sxs-lookup"><span data-stu-id="8d89c-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="8d89c-125">Jika tiada senarai harga yang meliputi tarikh itu pada masa kos sebenar, anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="8d89c-126">Ubah suai tarikh mula dan akhir bagi senarai harga untuk memastikan senarai harga meliputi tarikh masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="8d89c-127">Jika terdapat lebih daripada satu senarai harga yang meliputi tarikh masa kos sebenar, anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="8d89c-128">Anda boleh membetulkan ini dengan mengedit tarikh mula dan akhir senarai harga supaya terdapat hanya satu senarai harga yang meliputi tarikh masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="8d89c-129">Jika terdapat hanya satu senarai harga yang meliputi tarikh masa kos sebenar, beralih ke semakan seterusnya dalam dokumen.</span><span class="sxs-lookup"><span data-stu-id="8d89c-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="8d89c-130">Setelah anda selesai membuat pembetulan yang diperlukan, cipta semula entri masa, luluskannya dan sahkan bahawa masa kos sebenarnya menunjukkan harga sah.</span><span class="sxs-lookup"><span data-stu-id="8d89c-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="8d89c-131">Semak 3: Adakah terdapat harga sah dalam senarai harga untuk dimensi penentuan harga pada masa kos sebenar?</span><span class="sxs-lookup"><span data-stu-id="8d89c-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="8d89c-132">Jika anda telah berjaya melengkapkan Semak 1 dan Semak 2, anda kini hanya mempunyai satu senarai harga projek yang boleh digunakan untuk tarikh masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="8d89c-133">Buka Senarai Harga Projek ini dan pergi ke tab Harga Peranan. Pastikan terdapat baris dalam grid untuk dimensi penentuan harga pada masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="8d89c-134">Jika tiada baris dalam grid harga peranan untuk dimensi penentuan harga pada masa kos sebenar, maka anda telah mengasingkan masalah tersebut.</span><span class="sxs-lookup"><span data-stu-id="8d89c-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="8d89c-135">Cipta baris dalam grid harga Peranan untuk dimensi penentuan harga pada masa kos sebenar.</span><span class="sxs-lookup"><span data-stu-id="8d89c-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="8d89c-136">Setelah ini selesai, cipta semula entri masa, luluskannya dan sahkan bahawa masa kos sebenarnya menunjukkan harga sah.</span><span class="sxs-lookup"><span data-stu-id="8d89c-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="8d89c-137">Jika anda masih tidak melihat harga sah pada masa kos sebenar anda selepas anda melakukan tiga semakan di atas, sila log tiket sokongan.</span><span class="sxs-lookup"><span data-stu-id="8d89c-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



