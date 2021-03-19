---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 17, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 12df166e1bd1b5f0e11d79dc24122fb1ed7e6e6c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280814"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="633c5-103">Project Service Automation, Keluaran Kemas kini 17, V3</span><span class="sxs-lookup"><span data-stu-id="633c5-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="633c5-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="633c5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="633c5-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="633c5-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="633c5-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="633c5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="633c5-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="633c5-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="633c5-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="633c5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="633c5-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 17.</span><span class="sxs-lookup"><span data-stu-id="633c5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="633c5-110">Versi ini mempunyai nombor binaan V3.10.6.34 dan secara amnya tersedia melalui kemas kini kendiri pada Mac 2020.</span><span class="sxs-lookup"><span data-stu-id="633c5-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="633c5-111">Keluaran Kemas kini 17</span><span class="sxs-lookup"><span data-stu-id="633c5-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="633c5-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="633c5-112">Bug fixes</span></span>

<span data-ttu-id="633c5-113">**Umum**</span><span class="sxs-lookup"><span data-stu-id="633c5-113">**General**</span></span>

- <span data-ttu-id="633c5-114">Dibetulkan: Kemas kini Project Service Automation untuk kuat kuasakan lesen Ahli Pasukan (Hab Sumber Projek akan menyertakan pelan Perkhidmatan Ahli Pasukan metadata 3.x)</span><span class="sxs-lookup"><span data-stu-id="633c5-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="633c5-115">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="633c5-115">**Time and Expense**</span></span>

- <span data-ttu-id="633c5-116">Dibetulkan: Tidak boleh mengubah anggaran perbelanjaan daripada harga bukan sifar kepada sifar (0).</span><span class="sxs-lookup"><span data-stu-id="633c5-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="633c5-117">Perubahan diabaikan.</span><span class="sxs-lookup"><span data-stu-id="633c5-117">The change is ignored.</span></span>

<span data-ttu-id="633c5-118">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="633c5-118">**Project Management**</span></span>

- <span data-ttu-id="633c5-119">Dibetulkan: Semakan untuk nilai nol telah ditambah pada nama kedudukan ahli pasukan.</span><span class="sxs-lookup"><span data-stu-id="633c5-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="633c5-120">Dibetulkan: medan **msdyn_userresourceid** pada entiti **msdyn_resourceassignment** telah ditamatkan.</span><span class="sxs-lookup"><span data-stu-id="633c5-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="633c5-121">Dibetulkan: Naik taraf daripada 2.x kepada 3.x kini mengendalikan kontur usaha kosong pada penugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="633c5-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="633c5-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="633c5-122">**Sales**</span></span>

- <span data-ttu-id="633c5-123">Dibetulkan: **Invois.PreValidateInvoiceUpdate** kini mengendalikan senario menugaskan semula pemilik rekod dengan betul.</span><span class="sxs-lookup"><span data-stu-id="633c5-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="633c5-124">Dibetulkan: Apabila kelas transaksi ialah **Masa**, **UnitGroup** adalah tidak boleh diedit untuk semua entiti termasuk, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, dan **ContractLineDetails.**</span><span class="sxs-lookup"><span data-stu-id="633c5-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="633c5-125">Walau bagaimanapun, **Unit** adalah tidak boleh diedit hanya untuk **JournalLine** dan **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="633c5-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]