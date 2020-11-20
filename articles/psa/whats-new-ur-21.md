---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 21, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126719"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="1db5f-103">Project Service Automation, Keluaran Kemas kini 21, V3</span><span class="sxs-lookup"><span data-stu-id="1db5f-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="1db5f-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1db5f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1db5f-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="1db5f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1db5f-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1db5f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1db5f-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="1db5f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1db5f-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1db5f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1db5f-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 21.</span><span class="sxs-lookup"><span data-stu-id="1db5f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="1db5f-110">Versi ini mempunyai nombor binaan V 3.10.32.50 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.</span><span class="sxs-lookup"><span data-stu-id="1db5f-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="1db5f-111">Keluaran Kemas kini 21</span><span class="sxs-lookup"><span data-stu-id="1db5f-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1db5f-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="1db5f-112">Bug fixes</span></span>

<span data-ttu-id="1db5f-113">**Masa dan Perbelanjaan**</span><span class="sxs-lookup"><span data-stu-id="1db5f-113">**Time and Expense**</span></span>

<span data-ttu-id="1db5f-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="1db5f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1db5f-115">Apabila mengehoskan **Kawalan Grid Entri Masa** dalam Papan Pemuka, grid tidak menggunakan lebar penuh bekas grid papan pemuka.</span><span class="sxs-lookup"><span data-stu-id="1db5f-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="1db5f-116">Untuk zon masa tertentu, kawalan grid **Entri Masa** tidak memaparkan rekod.</span><span class="sxs-lookup"><span data-stu-id="1db5f-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="1db5f-117">Entri masa yang selepas 9:00 MLM muncul pada hari yang salah.</span><span class="sxs-lookup"><span data-stu-id="1db5f-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="1db5f-118">Pengguna tidak dapat menyerahkan perbelanjaan jika kategori perbelanjaan, **Resit perbelanjaan yang diperlukan** tidak mempunyai nilai.</span><span class="sxs-lookup"><span data-stu-id="1db5f-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="1db5f-119">**Pengurusan Sumber**</span><span class="sxs-lookup"><span data-stu-id="1db5f-119">**Resource Management**</span></span>

<span data-ttu-id="1db5f-120">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="1db5f-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="1db5f-121">Penempahan tidak aktif dipaparkan dalam pandangan **Penyelarasan**.</span><span class="sxs-lookup"><span data-stu-id="1db5f-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="1db5f-122">Pencapaian sumber generik tiada pengesahan untuk memastikan status penempahan yang sah wujud.</span><span class="sxs-lookup"><span data-stu-id="1db5f-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="1db5f-123">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="1db5f-123">**Project Management**</span></span>

<span data-ttu-id="1db5f-124">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="1db5f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="1db5f-125">Grid borang **Projek** ( **Tugasan Sumber**, **Tugas**, pandangan **Penyelarasan**, **Anggaran Perbelanjaan**) tetap boleh diedit walaupun semasa projek tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="1db5f-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="1db5f-126">Pelanggan duplikasi tidak boleh digabungkan dengan pelanggan yang dipautkan kepada kontrak projek yang telah disahkan.</span><span class="sxs-lookup"><span data-stu-id="1db5f-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="1db5f-127">Apabila sumber yang tidak mempunyai kalendar yang sah ditambah, sistem tidak akan mengembalikan mesej ralat mesra pengguna.</span><span class="sxs-lookup"><span data-stu-id="1db5f-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="1db5f-128">Butang **Tambah Tugas** pada grid tugas didayakan apabila projek dipautkan kepada **Tambahan Projek Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="1db5f-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="1db5f-129">Usaha bertambah tidak terkawal apabila tugas dengan kategori ditugaskan kepada sumber dengan peranan yang terdapat harga kos yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="1db5f-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="1db5f-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1db5f-130">**Sales**</span></span>

<span data-ttu-id="1db5f-131">Peningkatan berikut telah dibuat:</span><span class="sxs-lookup"><span data-stu-id="1db5f-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="1db5f-132">**Kekerapan Invois** dan **Permulaan Pengebilan** telah dipindahkan ke tab **Jadual invois**.</span><span class="sxs-lookup"><span data-stu-id="1db5f-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="1db5f-133">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="1db5f-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="1db5f-134">**Jumlah Harga Jualan** ialah sifar (0) bagi **Kategori** walaupun **Peranan** mempunyai jumlah harga jualan yang bukan sifar.</span><span class="sxs-lookup"><span data-stu-id="1db5f-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="1db5f-135">Pelanggan tidak boleh mengubah nilai medan **Status Invois** untuk **Bersedia untuk penginvoisan** apabila proses tersuai lain mengemas kini medan tambahan.</span><span class="sxs-lookup"><span data-stu-id="1db5f-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="1db5f-136">Butang **Segar Semula Baris Invois** boleh mencipta beberapa baris pendua jika ia dipilih berulang kali.</span><span class="sxs-lookup"><span data-stu-id="1db5f-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="1db5f-137">Butang **Kemas Kini Harga** tidak berfungsi pada subgrid **Harga Peranan** dalam borang **Pandangan Cepat**.</span><span class="sxs-lookup"><span data-stu-id="1db5f-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="1db5f-138">Logik **Ketetapan Senarai Harga Jualan** tidak mengendalikan zon masa dengan betul, menyebabkan pemilihan senarai harga yang salah.</span><span class="sxs-lookup"><span data-stu-id="1db5f-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="1db5f-139">**Jumlah Kos Sebenar** projek boleh dimatikan oleh jumlah pecahan selepas entri masa tunggal diluluskan.</span><span class="sxs-lookup"><span data-stu-id="1db5f-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="1db5f-140">Logik **Ketetapan Harga** tidak memberikan mesej ralat mesra pengguna jika **RolePrice yang didapatkan semula** tidak mempunyai nilai dalam medan **'Unit utama'** dan **'Harga Dalam Unit Utama**.</span><span class="sxs-lookup"><span data-stu-id="1db5f-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
