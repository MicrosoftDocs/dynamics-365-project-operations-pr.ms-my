---
title: Takrifkan kalendar projek
description: Topik ini menyediakan maklumat tentang menggunakan kalendar projek untuk menjejak jadual projek.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081402"
---
# <a name="define-project-calendars"></a><span data-ttu-id="9e07d-103">Takrifkan kalendar projek</span><span class="sxs-lookup"><span data-stu-id="9e07d-103">Define project calendars</span></span>

<span data-ttu-id="9e07d-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="9e07d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e07d-105">Untuk mencipta jadual projek, anda cipta templat kalendar projek yang mentakrifkan bilangan jam kerja setiap hari dan sebarang penutupan perniagaan.</span><span class="sxs-lookup"><span data-stu-id="9e07d-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="9e07d-106">Untuk mencipta templat kalendar projek, anda kaitkan templat kerja dengan medan **Templat kalendar** untuk projek.</span><span class="sxs-lookup"><span data-stu-id="9e07d-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="9e07d-107">Ikuti langkah ini untuk mencipta templat kerja.</span><span class="sxs-lookup"><span data-stu-id="9e07d-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="9e07d-108">Pada anak tetingkap navigasi kiri, pilih **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="9e07d-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="9e07d-109">Pada halaman senarai **Sumber** , buka rekod pengguna dan kemudian pilih **Tunjuk Jam Kerja**.</span><span class="sxs-lookup"><span data-stu-id="9e07d-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9e07d-110">Pastikan anda membenarkan tetimbul pada halaman pelayar.</span><span class="sxs-lookup"><span data-stu-id="9e07d-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="9e07d-111">Ini membenarkan anda melihat jam kerja yang ditetapkan untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="9e07d-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="9e07d-112">Pada tab **Pandangan Bulanan** , pilih **Sediakan**.</span><span class="sxs-lookup"><span data-stu-id="9e07d-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="9e07d-113">Satu senarai tiga pilihan muncul:</span><span class="sxs-lookup"><span data-stu-id="9e07d-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="9e07d-114">Jadual Mingguan Baharu</span><span class="sxs-lookup"><span data-stu-id="9e07d-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="9e07d-115">Jadual Kerja untuk Satu Hari</span><span class="sxs-lookup"><span data-stu-id="9e07d-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="9e07d-116">Masa Rehat</span><span class="sxs-lookup"><span data-stu-id="9e07d-116">Time Off</span></span>

4. <span data-ttu-id="9e07d-117">Pilih **Jadual Mingguan Baharu** dan kemudian tetapkan pilihan untuk jadual sumber ini.</span><span class="sxs-lookup"><span data-stu-id="9e07d-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="9e07d-118">Anda boleh menetapkan jadual mingguan berulang, parameter jam harian, penutupan perniagaan dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="9e07d-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="9e07d-119">Tetapkan julat tarikh, pilih **Simpan** dan kemudian pilih **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="9e07d-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="9e07d-120">Kembali ke halaman senarai **Sumber** dan pilih sumber yang anda tetapkan jam kerja.</span><span class="sxs-lookup"><span data-stu-id="9e07d-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="9e07d-121">Pilih **Tetapkan Kalendar Sebagai** untuk menetapkan templat kerja.</span><span class="sxs-lookup"><span data-stu-id="9e07d-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="9e07d-122">Dalam kotak dialog **Templat Kerja** , masukkan nama untuk templat kerja dan kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="9e07d-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="9e07d-123">Kini anda boleh mengaitkan templat kerja dengan templat kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="9e07d-123">You can now associate the work template with a project calendar template.</span></span>
