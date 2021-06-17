---
title: Cipta templat waktu kerja
description: Topik ini menerangkan cara mencipta templat waktu kerja dalam Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997207"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="d7a98-103">Cipta templat waktu kerja (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d7a98-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d7a98-104">Untuk mencipta dan mengurus projek, anda mesti menggunakan templat kalendar ke projek.</span><span class="sxs-lookup"><span data-stu-id="d7a98-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d7a98-105">Templat kalendar mentakrifkan atribut projek berikut:</span><span class="sxs-lookup"><span data-stu-id="d7a98-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d7a98-106">Waktu bekerja termasuk masa mula dan masa tamat</span><span class="sxs-lookup"><span data-stu-id="d7a98-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="d7a98-107">Hari bekerja</span><span class="sxs-lookup"><span data-stu-id="d7a98-107">Working days</span></span>
- <span data-ttu-id="d7a98-108">Pengecualian kalendar seperti hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="d7a98-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d7a98-109">Templat kalendar yang digunakan ke projek ialah salinan templat kalendar yang ditakrifkan dalam tetapan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="d7a98-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d7a98-110">Jika anda menukar templat kalendar, perubahan itu tidak tersebar ke waktu kerja projek.</span><span class="sxs-lookup"><span data-stu-id="d7a98-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d7a98-111">Untuk menukar waktu kerja projek, templat baharu mesti digunakan.</span><span class="sxs-lookup"><span data-stu-id="d7a98-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d7a98-112">Untuk mencipta templat kalendar bagi organisasi anda, terdapat dua keperluan utama:</span><span class="sxs-lookup"><span data-stu-id="d7a98-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d7a98-113">Takrifkan waktu kerja yang dikehendaki bagi templat menggunakan sumber boleh ditempah baharu atau sedia ada.</span><span class="sxs-lookup"><span data-stu-id="d7a98-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d7a98-114">Cipta templat kalendar baharu dan kaitkan templat dengan sumber oleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="d7a98-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d7a98-115">**Takrif waktu bekerja bagi templat**</span><span class="sxs-lookup"><span data-stu-id="d7a98-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d7a98-116">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="d7a98-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d7a98-117">Cipta sumber baharu untuk dirujuk dalam templat kalendar atau pilih sumber sedia ada.</span><span class="sxs-lookup"><span data-stu-id="d7a98-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d7a98-118">Pilih tab **Waktu Kerja** bagi sumber dan lengkapkan arahan dalam [Tetapkan waktu kerja untuk sumber](/dynamics365/field-service/set-work-hours-resource.md) untuk mengkonfigurasikan peraturan kalendar.</span><span class="sxs-lookup"><span data-stu-id="d7a98-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="d7a98-119">**Cipta templat kalendar baharu**</span><span class="sxs-lookup"><span data-stu-id="d7a98-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d7a98-120">Pergi ke **Tetapan** \> **Templat Kalendar**.</span><span class="sxs-lookup"><span data-stu-id="d7a98-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d7a98-121">Pilih **Baharu** dan masukkan nama, perihalan dan sumber templat.</span><span class="sxs-lookup"><span data-stu-id="d7a98-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="d7a98-122">Apabila sumber dirujuk dalam templat kalendar, salinan kalendar sumber dikaitkan dengan templat kalendar.</span><span class="sxs-lookup"><span data-stu-id="d7a98-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d7a98-123">Jika waktu bekerja bagi templat yang disalin berubah, perubahan itu tidak tersebar ke templat kalendar.</span><span class="sxs-lookup"><span data-stu-id="d7a98-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="d7a98-124">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="d7a98-124">See Also</span></span>  
 [<span data-ttu-id="d7a98-125">Sediakan sumber</span><span class="sxs-lookup"><span data-stu-id="d7a98-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
