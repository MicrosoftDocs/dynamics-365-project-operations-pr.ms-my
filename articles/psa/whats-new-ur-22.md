---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 22, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150994"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="dc102-103">Project Service Automation, Keluaran Kemas kini 22, V3</span><span class="sxs-lookup"><span data-stu-id="dc102-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dc102-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dc102-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dc102-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="dc102-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dc102-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dc102-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dc102-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="dc102-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="dc102-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dc102-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dc102-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 22.</span><span class="sxs-lookup"><span data-stu-id="dc102-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="dc102-110">Versi ini mempunyai nombor binaan V 3.10.33.48 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.</span><span class="sxs-lookup"><span data-stu-id="dc102-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="dc102-111">Keluaran Kemas kini 22</span><span class="sxs-lookup"><span data-stu-id="dc102-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dc102-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="dc102-112">Bug fixes</span></span>



<span data-ttu-id="dc102-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="dc102-113">**Time and Expense**</span></span>

<span data-ttu-id="dc102-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="dc102-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc102-115">**Entri masa** tidak ditambah secara automatik dalam Entri masa selepas import.</span><span class="sxs-lookup"><span data-stu-id="dc102-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="dc102-116">Pemilih tarikh grid **Entri masa** tidak mengenali tetapan serantau pengguna.</span><span class="sxs-lookup"><span data-stu-id="dc102-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="dc102-117">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="dc102-117">**Resource Management**</span></span>

<span data-ttu-id="dc102-118">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="dc102-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc102-119">Dalam mod manual, perubahan pada kontur **Tugasan Sumber** tidak dikenali semasa menjana **Keperluan Sumber**.</span><span class="sxs-lookup"><span data-stu-id="dc102-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="dc102-120">**Permintaan Sumber** tidak menyokong status permintaan tersuai.</span><span class="sxs-lookup"><span data-stu-id="dc102-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="dc102-121">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="dc102-121">**Project Management**</span></span>

<span data-ttu-id="dc102-122">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="dc102-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc102-123">Menggunakan klik dua kali pada EstimateGridControl tidak akan menghuraikan nombor format Belanda dengan betul.</span><span class="sxs-lookup"><span data-stu-id="dc102-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="dc102-124">Masa yang diberikan tidak dikemas kini dengan betul apabila tugasan ditukar menggunakan tambahan klien desktop Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="dc102-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="dc102-125">Grid Penjejakan dan Anggaran Projek memaparkan kod mata wang penjualan yang salah apabila mata wang kontrak berbeza daripada mata wang pelanggan dan organisasi dikonfigurasikan untuk memaparkan kod mata wang dan bukan simbol mata wang.</span><span class="sxs-lookup"><span data-stu-id="dc102-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="dc102-126">Tarikh tamat ahli Pasukan akan menambah satu hari jika jadual waktu kerja adalah 24 jam sehari.</span><span class="sxs-lookup"><span data-stu-id="dc102-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="dc102-127">Pada Jadual Projek, menambahkan Kategori Transaksi kepada tugas tidak mencetuskan simpan automatik.</span><span class="sxs-lookup"><span data-stu-id="dc102-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="dc102-128">Kesalahan berikut ditunjukkan apabila menambahkan ahli pasukan pada Templat Projek: "Keperluan sumber tidak boleh dikaitkan dengan templat projek".</span><span class="sxs-lookup"><span data-stu-id="dc102-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="dc102-129">Skrip peraturan reben "msdyn.Approval.CanApproveOrReject" memaparkan ralat masa tamat.</span><span class="sxs-lookup"><span data-stu-id="dc102-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="dc102-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="dc102-130">**Sales**</span></span>

<span data-ttu-id="dc102-131">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="dc102-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="dc102-132">Mesej ralat pengesahan tidak dipaparkan apabila Senarai Harga Kos dipilih dalam carian Senarai Harga pada borang/entiti 'Senarai Harga Projek Sebut Harga Baharu'.</span><span class="sxs-lookup"><span data-stu-id="dc102-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="dc102-133">Menutup sebut harga sebagai dimenangi tidak menavigasi ke kontrak yang dicipta jika BPF yang dilampirkan pada sebut harga berada dalam peringkat akhir.</span><span class="sxs-lookup"><span data-stu-id="dc102-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="dc102-134">Membalikkan **Jualan yang Belum Dibilkan** dikaitkan dengan kos asal apabila entri masa dipanggil semula.</span><span class="sxs-lookup"><span data-stu-id="dc102-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="dc102-135">Selepas memilih butang **Sahkan**, status invois tidak berubah kepada **Disahkan** melainkan invois disegar semula.</span><span class="sxs-lookup"><span data-stu-id="dc102-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
