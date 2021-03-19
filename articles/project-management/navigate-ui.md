---
title: Menavigasi antara muka pengguna
description: Topik ini memberikan maklumat tentang Pengurusan projek dalam Operasi projek Dynamics 365.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286754"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="b6592-103">Menavigasi antara muka pengguna</span><span class="sxs-lookup"><span data-stu-id="b6592-103">Navigating the user interface</span></span>

<span data-ttu-id="b6592-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="b6592-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="b6592-105">Gambaran keseluruhan</span><span class="sxs-lookup"><span data-stu-id="b6592-105">Overview</span></span>

<span data-ttu-id="b6592-106">Borang projek utama dipisahkan kepada beberapa tab.</span><span class="sxs-lookup"><span data-stu-id="b6592-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="b6592-107">Setiap tab mewakili tahap butiran yang berbeza dalam projek.</span><span class="sxs-lookup"><span data-stu-id="b6592-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="b6592-108">**Ringkasan**: Menyediakan perihalan projek dan agregat kedua-duanya prestasi projek yang dirancang dan sebenar.</span><span class="sxs-lookup"><span data-stu-id="b6592-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Tab dan medan ringkasan](media/navigation7.png)

- <span data-ttu-id="b6592-110">**Tugas**: Menyediakan butiran berkenaan struktur pecahan kerja yang diwakili oleh pandangan grid, pandangan papan dan gantt.</span><span class="sxs-lookup"><span data-stu-id="b6592-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Tab dan medan tugas](media/navigation8.png)

- <span data-ttu-id="b6592-112">**Pasukan**: Menyediakan butiran berkenaan peserta projek.</span><span class="sxs-lookup"><span data-stu-id="b6592-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="b6592-113">Usaha setiap ahli pasukan yang diperuntukkan juga diringkaskan dalam pandangan ini.</span><span class="sxs-lookup"><span data-stu-id="b6592-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Tab dan medan pasukan](media/navigation9.png)

- <span data-ttu-id="b6592-115">**Tugasan sumber**: Menyediakan pandangan usaha berfasa masa untuk setiap sumber pada projek.</span><span class="sxs-lookup"><span data-stu-id="b6592-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Tab dan medan tugasan sumber](media/navigation10.png)

- <span data-ttu-id="b6592-117">**Penyesuaian sumber**: Menyediakan pandangan perbezaan berfasa masa antara tugasan setiap sumber bernama dan tempahannya.</span><span class="sxs-lookup"><span data-stu-id="b6592-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Tab dan medan penyesuaian sumber](media/navigation11.png)

- <span data-ttu-id="b6592-119">**Anggaran**: Menyediakan pandangan anggaran kos dan jualan projek berfasa masa.</span><span class="sxs-lookup"><span data-stu-id="b6592-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Tab dan medan anggaran](media/navigation12.png)

- <span data-ttu-id="b6592-121">**Penjejakan**: Menyediakan pandangan yang menunjukkan kemajuan tugas dalam struktur pecahan kerja untuk usaha, kos dan jualan.</span><span class="sxs-lookup"><span data-stu-id="b6592-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Tab dan medan penjejakan](media/navigation13.png)

- <span data-ttu-id="b6592-123">**Jualan**: Menyediakan pautan mendalam kepada sebut harga dan kontrak yang berkaitan dengan projek.</span><span class="sxs-lookup"><span data-stu-id="b6592-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="b6592-124">**Anggaran Perbelanjaan**: Menyediakan grid yang mentakrifkan perbelanjaan projek berdasarkan kategori perbelanjaan organisasi.</span><span class="sxs-lookup"><span data-stu-id="b6592-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Tab dan medan anggaran perbelanjaan](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="b6592-126">Kawalan grid</span><span class="sxs-lookup"><span data-stu-id="b6592-126">Grid controls</span></span>

<span data-ttu-id="b6592-127">Berikut ialah gambaran ringkas kawalan biasa yang ditemui pada pelbagai tab perancangan projek.</span><span class="sxs-lookup"><span data-stu-id="b6592-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="b6592-128">Muat Semula</span><span class="sxs-lookup"><span data-stu-id="b6592-128">Refresh</span></span>

<span data-ttu-id="b6592-129">**Segar Semula**: Mendapatkan semula data terkini daripada pelayan jika sebarang perubahan berlaku selepas grid dimuatkan.</span><span class="sxs-lookup"><span data-stu-id="b6592-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Butang segar semula](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="b6592-131">Kelompokkan mengikut</span><span class="sxs-lookup"><span data-stu-id="b6592-131">Group by</span></span>

<span data-ttu-id="b6592-132">**Kelompokkan mengikut**: Mengemas kini pengelompokan baris dalam grid untuk menunjukkan sama ada sumber, peranan atau kategori berdasarkan keperluan pengguna.</span><span class="sxs-lookup"><span data-stu-id="b6592-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Butang Kelompokkan mengikut](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="b6592-134">Sebelumnya/Seterusnya</span><span class="sxs-lookup"><span data-stu-id="b6592-134">Previous/Next</span></span>

<span data-ttu-id="b6592-135">**Sebelumnya**/**Seterusnya**: Kemas kini tempoh masa kelihatan pada grid berfasa masa.</span><span class="sxs-lookup"><span data-stu-id="b6592-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Butang Sebelumnya dan Seterusnya](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="b6592-137">Skala masa</span><span class="sxs-lookup"><span data-stu-id="b6592-137">Timescale</span></span>

<span data-ttu-id="b6592-138">**Skala masa**: Ubah agregat data berfasa masa antara hari, minggu, bulan dan tahun.</span><span class="sxs-lookup"><span data-stu-id="b6592-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Butang Skala masa](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="b6592-140">Kembangkan</span><span class="sxs-lookup"><span data-stu-id="b6592-140">Expand</span></span>

<span data-ttu-id="b6592-141">**Kembangkan**: Memaparkan grid boleh dilihat kepada skrin penuh yang menyediakan lebih banyak keupayaan untuk melihat peranan tambahan.</span><span class="sxs-lookup"><span data-stu-id="b6592-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Butang Kembangkan](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="b6592-143">Fasa masa mengikut</span><span class="sxs-lookup"><span data-stu-id="b6592-143">Time-phase by</span></span>

<span data-ttu-id="b6592-144">**Fasa masa mengikut**: Mengemas kini pengelompokan baris dalam grid untuk menunjukkan anggaran kos untuk anggaran jualan.</span><span class="sxs-lookup"><span data-stu-id="b6592-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="b6592-145">Kawalan ini juga digunakan kepada skrip anggaran dan grid penjejakan.</span><span class="sxs-lookup"><span data-stu-id="b6592-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Butang Fasa masa mengikut](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="b6592-147">Tambahkan lajur</span><span class="sxs-lookup"><span data-stu-id="b6592-147">Add column</span></span>

<span data-ttu-id="b6592-148">**Tambahkan lajur**: Membolehkan pengguna mentakrifkan lajur boleh dilihat dalam grid.</span><span class="sxs-lookup"><span data-stu-id="b6592-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="b6592-149">Hanya lajur siap guna boleh ditambahkan pada grid dalam borang **Perancangan Projek**.</span><span class="sxs-lookup"><span data-stu-id="b6592-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Butang Tambahkan lajur](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]