---
title: Fahami status projek
description: Topik ini menyediakan maklumat tentang status untuk projek yang ditugaskan dalam Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965687"
---
# <a name="understand-project-status"></a><span data-ttu-id="50a83-103">Fahami status projek</span><span class="sxs-lookup"><span data-stu-id="50a83-103">Understand project status</span></span>

<span data-ttu-id="50a83-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="50a83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="50a83-105">Seksyen **Status** pada halaman **Entiti Projek** menyediakan ringkasan kesihatan projek berdasarkan kos dan usaha.</span><span class="sxs-lookup"><span data-stu-id="50a83-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="50a83-106">Medan ringkasan status</span><span class="sxs-lookup"><span data-stu-id="50a83-106">Status summary fields</span></span>

- <span data-ttu-id="50a83-107">Medan **Status keseluruhan projek** ialah medan boleh diedit yang menunjukkan status keseluruhan projek.</span><span class="sxs-lookup"><span data-stu-id="50a83-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="50a83-108">Medan ini menggunakan pengekodan warna, seperti hijau, kuning, dan merah, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="50a83-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="50a83-109">Medan **Komen** membolehkan pengurus projek memasukkan komen khusus tentang status.</span><span class="sxs-lookup"><span data-stu-id="50a83-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="50a83-110">Medan **Status dikemas kini pada** tidak boleh diedit.</span><span class="sxs-lookup"><span data-stu-id="50a83-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="50a83-111">Nilai dalam medan ini ialah cap masa yang menunjukkan apabila status terakhir dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="50a83-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="50a83-112">Medan **Prestasi jadual** dan **Prestasi kos** ditetapkan daripada grid penjejakan.</span><span class="sxs-lookup"><span data-stu-id="50a83-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="50a83-113">Apabila varians jadual dan kos untuk nod akar dalam pandangan **Penjejakan usaha** adalah positif, medan ini dikemas kini kepada **Ahead**.</span><span class="sxs-lookup"><span data-stu-id="50a83-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="50a83-114">Apabila varians jadual dan kos untuk nod akar adalah negatif, medan ini ditetapkan kepada **Di Belakang**.</span><span class="sxs-lookup"><span data-stu-id="50a83-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
