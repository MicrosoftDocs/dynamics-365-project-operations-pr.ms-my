---
title: Fahami status projek
description: Topik ini memberikan maklumat tentang status yang diperuntukkan kepada projek dalam Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286484"
---
# <a name="understand-project-status"></a><span data-ttu-id="088a6-103">Fahami status projek</span><span class="sxs-lookup"><span data-stu-id="088a6-103">Understand project status</span></span>

<span data-ttu-id="088a6-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="088a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="088a6-105">Bahagian **Status** pada halaman **Entiti Projek** menyediakan ringkasan kesihatan projek berdasarkan kos dan usaha.</span><span class="sxs-lookup"><span data-stu-id="088a6-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="088a6-106">Medan ringkasan status</span><span class="sxs-lookup"><span data-stu-id="088a6-106">Status summary fields</span></span>

- <span data-ttu-id="088a6-107">Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="088a6-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="088a6-108">Medan ini menggunakan pengekodan warna, seperti hijau, kuning, dan merah, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="088a6-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="088a6-109">Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status.</span><span class="sxs-lookup"><span data-stu-id="088a6-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="088a6-110">Medan **Status yang dikemas kini pada** tidak boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="088a6-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="088a6-111">Nilai dalam medan ini ialah cap masa yang menunjukkan apabila status terakhir dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="088a6-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="088a6-112">Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan daripada grid penjejakan.</span><span class="sxs-lookup"><span data-stu-id="088a6-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="088a6-113">Apabila jadual dan varians kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, medan ini dikemas kini kepada **Di Hadapan**.</span><span class="sxs-lookup"><span data-stu-id="088a6-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="088a6-114">Apabila jadual dan varians kos untuk nod akar adalah negatif, medan ini ditetapkan kepada **Di Belakang**.</span><span class="sxs-lookup"><span data-stu-id="088a6-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]