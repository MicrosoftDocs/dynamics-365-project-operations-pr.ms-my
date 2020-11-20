---
title: Fahami status projek
description: Topik ini menyediakan maklumat tentang status untuk projek yang ditugaskan dalam Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127304"
---
# <a name="understand-project-status"></a><span data-ttu-id="bc645-103">Fahami status projek</span><span class="sxs-lookup"><span data-stu-id="bc645-103">Understand project status</span></span>

<span data-ttu-id="bc645-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="bc645-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bc645-105">Bahagian **Status** pada halaman **Entiti Projek** menyediakan ringkasan kesihatan projek berdasarkan kos dan usaha.</span><span class="sxs-lookup"><span data-stu-id="bc645-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="bc645-106">Medan ringkasan status</span><span class="sxs-lookup"><span data-stu-id="bc645-106">Status summary fields</span></span>

- <span data-ttu-id="bc645-107">Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="bc645-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="bc645-108">Medan ini menggunakan pengekodan warna, seperti hijau, kuning, dan merah, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="bc645-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="bc645-109">Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status.</span><span class="sxs-lookup"><span data-stu-id="bc645-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="bc645-110">Medan **Status yang dikemas kini pada** tidak boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="bc645-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="bc645-111">Nilai dalam medan ini ialah cap masa yang menunjukkan apabila status terakhir dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="bc645-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="bc645-112">Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan daripada grid penjejakan.</span><span class="sxs-lookup"><span data-stu-id="bc645-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="bc645-113">Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, medan ini dikemas kini kepada **Di Hadapan**.</span><span class="sxs-lookup"><span data-stu-id="bc645-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="bc645-114">Apabila jadual dan varians kos untuk nod akar adalah negatif, medan ini ditetapkan kepada **Di Belakang**.</span><span class="sxs-lookup"><span data-stu-id="bc645-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
