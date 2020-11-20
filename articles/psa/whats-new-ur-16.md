---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 16, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121589"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="b846c-103">Project Service Automation, Keluaran Kemas kini 16, V3</span><span class="sxs-lookup"><span data-stu-id="b846c-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="b846c-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b846c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b846c-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="b846c-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="b846c-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b846c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b846c-107">Untuk mengemas kini kepada keluaran ini, lawati Pusat Pentadbir untuk Dynamics 365 online, halaman penyelesaian untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="b846c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="b846c-108">Untuk maklumat lanjut, lihat [Pasang, Kemas kini Penyelesaian Pilihan](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="b846c-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="b846c-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk PSA V3, Keluaran Kemas kini 16.</span><span class="sxs-lookup"><span data-stu-id="b846c-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="b846c-110">Versi ini mempunyai nombor binaan V3.10.6.34 dan secara amnya boleh didapati melalui kemas kini kendiri pada Januari 2020.</span><span class="sxs-lookup"><span data-stu-id="b846c-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="b846c-111">Keluaran Kemas kini 16</span><span class="sxs-lookup"><span data-stu-id="b846c-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b846c-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="b846c-112">Bug fixes</span></span>

-   <span data-ttu-id="b846c-113">Masa dan Perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="b846c-113">Time and Expense</span></span>

    -   <span data-ttu-id="b846c-114">Dibetulkan: Pengguna yang cuba menyerahkan entri masa dan perbelanjaan yang dipadamkan untuk kelulusan kini akan menerima mesej ralat yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="b846c-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="b846c-115">Pengurusan Projek</span><span class="sxs-lookup"><span data-stu-id="b846c-115">Project Management</span></span>

    -   <span data-ttu-id="b846c-116">Dibetulkan: Unit sumber yang ditakrifkan untuk ahli pasukan dalam templat yang diambil kira dengan templat digunakan untuk projek baharu.</span><span class="sxs-lookup"><span data-stu-id="b846c-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="b846c-117">Dibetulkan: Pengendalian yang dipertingkatkan terhadap penyerahan semula pemilikan rekod.</span><span class="sxs-lookup"><span data-stu-id="b846c-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="b846c-118">Dibetulkan: Projek yang sedang dalam proses disalin tidak akan dibenarkan untuk disalin sehingga semua operasi salinan selesai.</span><span class="sxs-lookup"><span data-stu-id="b846c-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="b846c-119">Pengurusan Sumber</span><span class="sxs-lookup"><span data-stu-id="b846c-119">Resource Management</span></span>

    -   <span data-ttu-id="b846c-120">Dibetulkan: Melanjutkan tempahan kini mengendalikan jangka masa pendek dengan betul dan tidak lagi menghasilkan jam sifar untuk tempahan yang dilanjutkan.</span><span class="sxs-lookup"><span data-stu-id="b846c-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="b846c-121">Dibetulkan: Pandangan penyesuaian kini sedang dipaparkan apabila zon waktu projek ialah +5:30 GMT dan masa pengguna berbeza.</span><span class="sxs-lookup"><span data-stu-id="b846c-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="b846c-122">Sales</span><span class="sxs-lookup"><span data-stu-id="b846c-122">Sales</span></span>

    -   <span data-ttu-id="b846c-123">Dibetulkan: Apabila projek dipetakan ke baris kontrak dialih keluar dan projek baru dipetakan, rekod sebenar pada projek baharu tidak dinilai semula berdasarkan peraturan pengebilan dan penetapan harga yang ditakrifkan dalam baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b846c-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="b846c-124">Ini telah dibetulkan dalam keluaran ini.</span><span class="sxs-lookup"><span data-stu-id="b846c-124">This has been fixed in this release.</span></span> <span data-ttu-id="b846c-125">Penetapan harga dan rekod sebenar projek yang baru dipetakan akan diterbalikkan dan diciptakan semula dengan betul berdasarkan penetapan harga dan pengebilan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b846c-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="b846c-126">Rekod sebenar projek yang tidak dipetakan juga akan dinilai semula dan dicipta semula sebagai hasilnya.</span><span class="sxs-lookup"><span data-stu-id="b846c-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="b846c-127">Dibetulkan: Pengesahan tambahan telah ditambahkan pada medan baris anggaran **Jumlah** untuk memastikan bahawa nilai nol tidak akan diteruskan.</span><span class="sxs-lookup"><span data-stu-id="b846c-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="b846c-128">Dibetulkan: Apabila aktual telah dikemas kini pada projek, butang segar semula telah ditambah pada borang utama projek untuk membolehkan pengguna menyegerakkan semula aktual.</span><span class="sxs-lookup"><span data-stu-id="b846c-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="b846c-129">Dibetulkan: Apabila pengguna menaik taraf daripada 2.X kepada 3.X, projek dengan nilai NOL untuk nama projek akan dibenarkan.</span><span class="sxs-lookup"><span data-stu-id="b846c-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

