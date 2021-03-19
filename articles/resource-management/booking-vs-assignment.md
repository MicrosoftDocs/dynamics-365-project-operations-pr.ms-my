---
title: Tempahan lwn penugasan
description: Topik ini memberikan maklumat tentang perbezaan antara tempahan sumber dan penugasan sumber.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279914"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="315b0-103">Tempahan lwn penugasan</span><span class="sxs-lookup"><span data-stu-id="315b0-103">Bookings vs assignments</span></span>

<span data-ttu-id="315b0-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="315b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="315b0-105">Penempahan ialah pengagihan sumber yang cetak atau lembut kepada projek.</span><span class="sxs-lookup"><span data-stu-id="315b0-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="315b0-106">Penempahan keras menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="315b0-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="315b0-107">Tempahan mewakili konsep organisasi untuk pasukan supaya mereka dapat memahami cara sumber akan terlibat merentasi pelbagai projek.</span><span class="sxs-lookup"><span data-stu-id="315b0-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="315b0-108">Dynamics 365 Project Operations mempertimbangkan penempahan konsep peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="315b0-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="315b0-109">Tidak seperti tempahan, tugasan adalah komitmen sumber untuk tugas projek dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="315b0-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="315b0-110">Sumber boleh dinamakan atau generik.</span><span class="sxs-lookup"><span data-stu-id="315b0-110">The resources can be named or generic.</span></span>  <span data-ttu-id="315b0-111">Apabila keperluan sumber diperolehi daripada tugasan kerja projek, Project Operations menggunakan kontur usaha bagi penugasan sumber untuk membina kontur bagi butiran keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="315b0-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="315b0-112">Walau bagaimanapun, rujukan kepada tugasan sumber tidak dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="315b0-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="315b0-113">Kemas kini kepada penempahan yang diperoleh daripada keperluan sumber tidak akan mengemas kini sebarang tugas sumber.</span><span class="sxs-lookup"><span data-stu-id="315b0-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="315b0-114">Biasanya, jumlah tempahan untuk sumber akan sama dengan jumlah subjek tugas sumber merentasi satu atau banyak tugas.</span><span class="sxs-lookup"><span data-stu-id="315b0-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="315b0-115">Walau bagaimanapun, Project Operations tidak menguatkuasakan perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="315b0-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="315b0-116">Pandangan **Penyesuaian** menunjukkan Pengurus projek tempat tempahan sumber dan tugasan tidak sama.</span><span class="sxs-lookup"><span data-stu-id="315b0-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]