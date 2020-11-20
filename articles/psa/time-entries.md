---
title: Cipta entri masa
description: Topik ini memberikan maklumat tentang cara untuk mencipta entri masa.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131294"
---
# <a name="create-time-entries"></a><span data-ttu-id="a5404-103">Cipta entri masa</span><span class="sxs-lookup"><span data-stu-id="a5404-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a5404-104">Dalam versi sebelumnya Dynamics 365 Project Service Automation, entri masa penyertaan telah dimasukkan pada setiap minggu.</span><span class="sxs-lookup"><span data-stu-id="a5404-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="a5404-105">Dalam versi 3 Project Service Automation, penyertaan masa akan dimasukkan pada setiap hari.</span><span class="sxs-lookup"><span data-stu-id="a5404-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="a5404-106">Namun, selepas beberapa penyertaan masa telah dicipta, anda boleh membuat atau menyalinnya secara pukal.</span><span class="sxs-lookup"><span data-stu-id="a5404-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="a5404-107">Cipta entri masa</span><span class="sxs-lookup"><span data-stu-id="a5404-107">Create a time entry</span></span>

<span data-ttu-id="a5404-108">Ikuti langkah ini untuk mencipta entri masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="a5404-109">Pada halaman **Entri Masa** , pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="a5404-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="a5404-110">Dalam kotak dialog **Cipta Pantas: Entri Masa**, masukkan tempoh masa penyertaan dalam minit, jam, atau hari.</span><span class="sxs-lookup"><span data-stu-id="a5404-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="a5404-111">Tempoh mesti di masukkan dalam format berikut: *x* minit , *x* jam atau *x* hari.</span><span class="sxs-lookup"><span data-stu-id="a5404-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="a5404-112">Jam dan hari boleh juga dimasukkan menggunakan nilai perpuluhan, seperti *x.x* jam atau *x.x* hari.</span><span class="sxs-lookup"><span data-stu-id="a5404-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="a5404-113">Pilih jenis kemasukan masa dan projek yang anda masukkan entri masa untuk anda.</span><span class="sxs-lookup"><span data-stu-id="a5404-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="a5404-114">Dalam medan **Tugas Projek**, cari tugas untuk entri masa ini.</span><span class="sxs-lookup"><span data-stu-id="a5404-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a5404-115">Jika anda mencipta entri masa untuk tugas yang tidak ditugaskan kepada pengguna, dalam medan **Tugas Projek**, pilih butang **Carian**, pilih **Ubah Pandangan** dan kemudian pilih **Semua Tugas Projek Aktif** ke senarai semua tugas.</span><span class="sxs-lookup"><span data-stu-id="a5404-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="a5404-116">Masukkan perihalan, jika perihalan diperlukan dan kemudian pilih **Simpan dan Tutup.**</span><span class="sxs-lookup"><span data-stu-id="a5404-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="a5404-117">Selepas kemasukan masa dicipta dan disimpan, anda boleh mengeditnya dalam grid kemasukan masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="a5404-118">Grid entri masa menyokong dua format:</span><span class="sxs-lookup"><span data-stu-id="a5404-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="a5404-119">Anda boleh masukkan penyertaan masa dalam **format hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="a5404-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="a5404-120">Format ini kemudian ditukar kepada jam dan fractions.</span><span class="sxs-lookup"><span data-stu-id="a5404-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="a5404-121">Anda boleh masukkan jam dan pecahan secara langsung.</span><span class="sxs-lookup"><span data-stu-id="a5404-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="a5404-122">Perhatikan bahawa pecahan sejam tidak minit.</span><span class="sxs-lookup"><span data-stu-id="a5404-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="a5404-123">Oleh itu, 1.5 jam mewakili 1 jam dan 30 minit.</span><span class="sxs-lookup"><span data-stu-id="a5404-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="a5404-124">Peraturan yang sama diguna pakai untuk pecahan hari.</span><span class="sxs-lookup"><span data-stu-id="a5404-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="a5404-125">Satu hari adalah 24 jam, dan 0.5 hari mewakili 12 jam.</span><span class="sxs-lookup"><span data-stu-id="a5404-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="a5404-126">Cipta entri masa pukal</span><span class="sxs-lookup"><span data-stu-id="a5404-126">Bulk create time entries</span></span>

<span data-ttu-id="a5404-127">Selepas beberapa kali entri telah dicipta, anda boleh salin ia untuk mencipta entri masa tambahan dalam pukal.</span><span class="sxs-lookup"><span data-stu-id="a5404-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="a5404-128">Pada halaman **Entri Masa** , pilih **Salin Minggu**.</span><span class="sxs-lookup"><span data-stu-id="a5404-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="a5404-129">Dalam kumpulan medan **Dari Tempoh** dalam **Tarikh Mula** dan **Tarikh Akhir** tentukan julat tarikh untuk menyalin entri masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="a5404-130">Dalam kumpulan medan **Ke Tempoh** dalam medan **Tarikh Mula**. tentukan tarikh untuk mencipta penyertaan masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="a5404-131">Pilih **Salin** untuk mencipta salinan penyertaan masa yang sesuai dengan hari minggu yang ditentukan dalam kumpulan medan **Ke Tempoh**.</span><span class="sxs-lookup"><span data-stu-id="a5404-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="a5404-132">Sebagai contoh, kemasukan masa untuk Isnin minggu lepas disalin ke hari Isnin minggu yang ditetapkan dalam kumpulan medan **Ke Tempoh**.</span><span class="sxs-lookup"><span data-stu-id="a5404-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="a5404-133">Import data untuk entri masa</span><span class="sxs-lookup"><span data-stu-id="a5404-133">Import data for time entries</span></span>

<span data-ttu-id="a5404-134">Anda boleh mengimport data daripada penempahan projek dan tugasan.</span><span class="sxs-lookup"><span data-stu-id="a5404-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="a5404-135">Apabila anda mengimport data, anda boleh menentukan julat tarikh bagi penempahan untuk diimport dan kemudian secara eksplisit memilih penempahan yang sepatutnya dicipta sebagai **Draf** entiti masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="a5404-136">Kumpul mengikut, isih, cari dan keupayaan menapis</span><span class="sxs-lookup"><span data-stu-id="a5404-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="a5404-137">Anda boleh mengumpulkan dan menapis entri masa dengan dimensi yang ditetapkan dalam lajur.</span><span class="sxs-lookup"><span data-stu-id="a5404-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="a5404-138">Dalam medan **Kumpulkan dengan**, pilih dimensi yang akan digunakan untuk menapis entri masa.</span><span class="sxs-lookup"><span data-stu-id="a5404-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="a5404-139">Anda juga boleh mengisih rekod kemasukan masa dalam urutan menaik atau menurun dengan menggunakan anak panah isih pada pengepala lajur.</span><span class="sxs-lookup"><span data-stu-id="a5404-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="a5404-140">Selain itu, anda boleh menunjukkan atau menyembunyikan entri dengan memilih butang **Tapis** pada tajuk lajur dan kemudian, dalam kotak **Carian**, memasukkan teks yang sepatutnya digunakan untuk mencari penyertaan masa dengan nama projek, tugas projek, masa entri atau sumber.</span><span class="sxs-lookup"><span data-stu-id="a5404-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
