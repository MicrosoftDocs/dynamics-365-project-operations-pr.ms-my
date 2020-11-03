---
title: Cipta templat waktu kerja
description: Cara untuk mencipta templat waktu kerja dalam Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081238"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="31ac6-103">Cipta templat waktu kerja (Project Service)</span><span class="sxs-lookup"><span data-stu-id="31ac6-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="31ac6-104">Sebelum anda mencipta jadual projek, anda perlu menyediakan kalendar projek yang mentakrifkan bilangan waktu bekerja untuk diberikan setiap hari dalam jadual dan mana-mana penutupan perniagaan.</span><span class="sxs-lookup"><span data-stu-id="31ac6-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="31ac6-105">Anda melakukan ini dengan tempat jam kerja yang mengandungi butiran mengenai jam kerja setiap hari, hari cuti dan mana-mana penutupan perniagaan lain.</span><span class="sxs-lookup"><span data-stu-id="31ac6-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="31ac6-106">Apabila anda mencipta projek, anda mengaitkan templat kerja dengan kalendar projek untuk menggunakan jadual untuk projek.</span><span class="sxs-lookup"><span data-stu-id="31ac6-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="31ac6-107">Terdapat dua cara anda boleh mencipta templat jam kerja:</span><span class="sxs-lookup"><span data-stu-id="31ac6-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="31ac6-108">Cipta templat waktu kerja berdasarkan kalendar sumber.</span><span class="sxs-lookup"><span data-stu-id="31ac6-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="31ac6-109">Cipta templat waktu kerja baharu.</span><span class="sxs-lookup"><span data-stu-id="31ac6-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="31ac6-110">Untuk mencipta templat jam kerja berdasarkan kalendar sumber.</span><span class="sxs-lookup"><span data-stu-id="31ac6-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="31ac6-111">Pergi ke **Project Service > Sumber**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="31ac6-112">Pilih sumber yang anda mahu jadikan asas waktu kerja anda.</span><span class="sxs-lookup"><span data-stu-id="31ac6-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="31ac6-113">Klik **Simpan Kalendar Sebagai** , masukkan nama untuk templat waktu kerja dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="31ac6-114">Apabila anda selesai mengubah pilihan, klik **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="31ac6-115">Klik butang **Simpan** di sudut kanan bawah skrin.</span><span class="sxs-lookup"><span data-stu-id="31ac6-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="31ac6-116">Untuk mencipta templat jam kerja baharu</span><span class="sxs-lookup"><span data-stu-id="31ac6-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="31ac6-117">Pergi ke **Project Service > Templat Waktu Kerja**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="31ac6-118">Klik **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="31ac6-119">Masukkan nama untuk templat waktu kerja.</span><span class="sxs-lookup"><span data-stu-id="31ac6-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="31ac6-120">Pilih sumber untuk menjadi asas jam kerja dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="31ac6-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="31ac6-121">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="31ac6-121">See Also</span></span>  
 [<span data-ttu-id="31ac6-122">Sediakan sumber</span><span class="sxs-lookup"><span data-stu-id="31ac6-122">Set up resources</span></span>](../psa/set-up-resources.md)
