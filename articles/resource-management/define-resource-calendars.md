---
title: Takrifkan kalendar sumber
description: Topik ini memberikan maklumat mengenai cara untuk mentakrifkan kalendar waktu kerja untuk sumber dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123929"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="239f5-103">Takrifkan kalendar sumber</span><span class="sxs-lookup"><span data-stu-id="239f5-103">Define resource calendars</span></span>

<span data-ttu-id="239f5-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="239f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="239f5-105">Setiap sumber boleh ditempah yang mengendalikan projek mesti mempunyai kalendar waktu kerja untuk menentukan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="239f5-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="239f5-106">Waktu kerja untuk sumber boleh ditakrifkan dalam dua cara:</span><span class="sxs-lookup"><span data-stu-id="239f5-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="239f5-107">Takrifkan peraturan kalendar individu untuk sumber</span><span class="sxs-lookup"><span data-stu-id="239f5-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="239f5-108">Gunakan templat kalendar sedia ada untuk sumber</span><span class="sxs-lookup"><span data-stu-id="239f5-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="239f5-109">Takrifkan waktu kerja sumber</span><span class="sxs-lookup"><span data-stu-id="239f5-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="239f5-110">Pada menu **Sumber**, pilih **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="239f5-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="239f5-111">Daripada pandangan grid, pilih **Sumber Boleh Ditempah** yang berkenaan.</span><span class="sxs-lookup"><span data-stu-id="239f5-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="239f5-112">Pada halaman **Butiran Sumber**, pilih tab **Waktu Kerja**. Secara lalai, kalendar sumber boleh ditempah menjadi lalai kepada waktu kerja bagi templat waktu kerja lalai yang ditakrifkan untuk organisasi.</span><span class="sxs-lookup"><span data-stu-id="239f5-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="239f5-113">Untuk mengemas kini waktu kerja, klik kanan pada tarikh mula peraturan kalendar yang dicadangkan untuk ditakrifkan.</span><span class="sxs-lookup"><span data-stu-id="239f5-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="239f5-114">Gunakan menu peraturan kalendar untuk mentakrifkan peraturan kalendar untuk hari tertentu, baki siri atau keseluruhan kalendar.</span><span class="sxs-lookup"><span data-stu-id="239f5-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="239f5-115">Selepas pilihan dipilih, anda boleh mentakrifkan:</span><span class="sxs-lookup"><span data-stu-id="239f5-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="239f5-116">Hari minggu yang mana waktu kerja akan diguna pakai.</span><span class="sxs-lookup"><span data-stu-id="239f5-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="239f5-117">Waktu kerja dalam setiap hari.</span><span class="sxs-lookup"><span data-stu-id="239f5-117">The working times within each day.</span></span>
    - <span data-ttu-id="239f5-118">Zon waktu untuk peraturan kalendar.</span><span class="sxs-lookup"><span data-stu-id="239f5-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="239f5-119">Jika sesuai, waktu bukan kerja juga boleh ditentukan untuk peraturan.</span><span class="sxs-lookup"><span data-stu-id="239f5-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="239f5-120">Menggunakan templat kalendar pada sumber</span><span class="sxs-lookup"><span data-stu-id="239f5-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="239f5-121">Pada menu **Sumber**, pilih **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="239f5-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="239f5-122">Daripada pandangan grid, pilih sehingga 25 **Sumber Boleh Ditempah** untuk dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="239f5-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="239f5-123">Pilih **Tetapkan kalendar** dan dialog akan menggesa anda dengan senarai templat waktu kerja yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="239f5-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="239f5-124">Pilih templat yang anda mahu gunakan, dan kemudian pilih **Gunakan**.</span><span class="sxs-lookup"><span data-stu-id="239f5-124">Select the template you want to use, and then select **Apply**.</span></span>
