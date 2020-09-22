---
title: Keperluan tempah lembut
description: Topik ini memberikan maklumat tentang cara untuk memenuhi keperluan tempahan lembut.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753983"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="836c1-103">Keperluan tempah lembut</span><span class="sxs-lookup"><span data-stu-id="836c1-103">Soft-book requirements</span></span>

<span data-ttu-id="836c1-104">Keperluan sumber boleh ditempah cetak.</span><span class="sxs-lookup"><span data-stu-id="836c1-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="836c1-105">Penempahan cetak mencipta cadangan yang menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="836c1-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="836c1-106">Cadangan kemudiannya dihantar kembali ke peminta untuk kelulusan.</span><span class="sxs-lookup"><span data-stu-id="836c1-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="836c1-107">Penempahan lembut secara tentatif menambah sumber kepada pasukan projek dan mempunyai status berbeza pada Papan Jadual tetapi ia tidak mengambil kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="836c1-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="836c1-108">Untuk membuat pilihan lembut sumber daripada Papan Jadual, tetapkan medan **Status Tempahan** kepada **Lembut**.</span><span class="sxs-lookup"><span data-stu-id="836c1-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Status Penempahan ditetapkan kepada Lembut](media/Resource-Management-image77.png)

<span data-ttu-id="836c1-110">Apabila tab **Pasukan** berada dalam pandangan **Ahli Pasukan Dinamakan**, sumber muncul di sana.</span><span class="sxs-lookup"><span data-stu-id="836c1-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="836c1-111">Waktu yang ditempah lembut dilaporkan dalam lajur **Jam yang Ditempah Lembut**.</span><span class="sxs-lookup"><span data-stu-id="836c1-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Jam yang ditempah lembut dalam pandangan Ahli Pasukan Dinamakan](media/Resource-Management-image78.png)

<span data-ttu-id="836c1-113">Ahli pasukan ditempah lembut boleh ditugaskan kepada tugas.</span><span class="sxs-lookup"><span data-stu-id="836c1-113">Soft-booked team members can be assigned to tasks.</span></span>

![Ahli pasukan ditempah lembut boleh ditugaskan kepada satu tugas.](media/Resource-Management-image79.png)

<span data-ttu-id="836c1-115">Pada tab **Penyesuaian**, tiada tempahan ditunjukkan untuk sumber tempahan lembut, kerana tab **Penyesuaian** yang menganggap hanya tempahan cetak.</span><span class="sxs-lookup"><span data-stu-id="836c1-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Sumber tempahan lembut tanpa sebarang tempahan pada tab Penyesuaian](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="836c1-117">Anda tidak boleh menempah lembut sumber daripada keperluan yang telah dijana daripada ahli pasukan generik.</span><span class="sxs-lookup"><span data-stu-id="836c1-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="836c1-118">Pada Papan Jadual, pewarna yang berbeza digunakan untuk tempahan lembut untuk sumber.</span><span class="sxs-lookup"><span data-stu-id="836c1-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Tempah lembut pada Papan Jadual](media/Resource-Management-image81.png)

<span data-ttu-id="836c1-120">Untuk menukar Tempahan lembut kepada penempahan keras, pada papan Jadual, klik kanan dengan tempahan lembut dan kemudian pilih **Ubah status** \> **Tempahan Cetak** \> **Cetak**.</span><span class="sxs-lookup"><span data-stu-id="836c1-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Mengubah status penempahan kepada Cetak](media/Resource-Management-image82.png)

<span data-ttu-id="836c1-122">Penempahan ditukar dan status ditukar pada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="836c1-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="836c1-123">Oleh kerana status penempahan kini **Cetak**, sumber ditunjukkan sebagai telah ditempah dan keupayaan dan ketersediaan akan dilaraskan.</span><span class="sxs-lookup"><span data-stu-id="836c1-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="836c1-124">Anda boleh menggunakan kaedah yang sama untuk membatalkan tempahan cetak atau membuat tempahan lembut daripada Papan Jadual.</span><span class="sxs-lookup"><span data-stu-id="836c1-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="836c1-125">Untuk menukar sumber yang lembut ditempah untuk ditempah keras pada tab **Pasukan** projek, pilih sumber dan kemudian pilih **Sahkan**.</span><span class="sxs-lookup"><span data-stu-id="836c1-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Sahkan perintah](media/Resource-Management-image83.png)
