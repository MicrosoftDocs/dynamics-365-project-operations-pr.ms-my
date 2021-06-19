---
title: Tempahan lwn penugasan
description: Topik ini memberikan maklumat tentang perbezaan antara tempahan sumber dan penugasan sumber.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012777"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="f1afb-103">Tempahan lwn penugasan</span><span class="sxs-lookup"><span data-stu-id="f1afb-103">Bookings vs assignments</span></span>

<span data-ttu-id="f1afb-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="f1afb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1afb-105">Penempahan ialah pengagihan sumber yang cetak atau lembut kepada projek.</span><span class="sxs-lookup"><span data-stu-id="f1afb-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="f1afb-106">Penempahan keras menggunakan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="f1afb-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="f1afb-107">Tempahan mewakili konsep organisasi untuk pasukan supaya mereka dapat memahami cara sumber akan terlibat merentasi pelbagai projek.</span><span class="sxs-lookup"><span data-stu-id="f1afb-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="f1afb-108">Dynamics 365 Project Operations mempertimbangkan penempahan konsep peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="f1afb-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="f1afb-109">Tidak seperti tempahan, tugasan adalah komitmen sumber untuk tugas projek dalam jadual projek.</span><span class="sxs-lookup"><span data-stu-id="f1afb-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="f1afb-110">Sumber boleh dinamakan atau generik.</span><span class="sxs-lookup"><span data-stu-id="f1afb-110">The resources can be named or generic.</span></span>  <span data-ttu-id="f1afb-111">Apabila keperluan sumber diperolehi daripada tugasan kerja projek, Project Operations menggunakan kontur usaha bagi penugasan sumber untuk membina kontur bagi butiran keperluan sumber.</span><span class="sxs-lookup"><span data-stu-id="f1afb-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="f1afb-112">Walau bagaimanapun, rujukan kepada tugasan sumber tidak dikekalkan.</span><span class="sxs-lookup"><span data-stu-id="f1afb-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="f1afb-113">Kemas kini kepada penempahan yang diperoleh daripada keperluan sumber tidak akan mengemas kini sebarang tugas sumber.</span><span class="sxs-lookup"><span data-stu-id="f1afb-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="f1afb-114">Biasanya, jumlah tempahan untuk sumber akan sama dengan jumlah subjek tugas sumber merentasi satu atau banyak tugas.</span><span class="sxs-lookup"><span data-stu-id="f1afb-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="f1afb-115">Walau bagaimanapun, Project Operations tidak menguatkuasakan perjanjian ini.</span><span class="sxs-lookup"><span data-stu-id="f1afb-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="f1afb-116">Pandangan **Penyesuaian** menunjukkan Pengurus projek tempat tempahan sumber dan tugasan tidak sama.</span><span class="sxs-lookup"><span data-stu-id="f1afb-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]