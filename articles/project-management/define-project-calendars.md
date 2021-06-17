---
title: Takrifkan kalendar projek
description: Topik ini menyediakan maklumat tentang cara menggunakan templat kalendar ke projek untuk menjejak jadual projek.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999007"
---
# <a name="define-project-calendars"></a><span data-ttu-id="48e13-103">Takrifkan kalendar projek</span><span class="sxs-lookup"><span data-stu-id="48e13-103">Define project calendars</span></span>

<span data-ttu-id="48e13-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="48e13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48e13-105">Untuk mencipta dan mengurus projek, anda mesti menggunakan templat kalendar ke projek.</span><span class="sxs-lookup"><span data-stu-id="48e13-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="48e13-106">Templat kalendar mentakrifkan atribut projek berikut:</span><span class="sxs-lookup"><span data-stu-id="48e13-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="48e13-107">Waktu bekerja termasuk masa mula dan masa tamat</span><span class="sxs-lookup"><span data-stu-id="48e13-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="48e13-108">Hari bekerja</span><span class="sxs-lookup"><span data-stu-id="48e13-108">Working days</span></span>
- <span data-ttu-id="48e13-109">Pengecualian kalendar seperti hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="48e13-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="48e13-110">Templat kalendar yang digunakan ke projek ialah salinan templat kalendar yang ditakrifkan dalam tetapan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="48e13-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="48e13-111">Jika anda menukar templat kalendar, perubahan itu tidak tersebar ke waktu kerja projek.</span><span class="sxs-lookup"><span data-stu-id="48e13-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="48e13-112">Untuk menukar waktu kerja projek, templat baharu mesti digunakan.</span><span class="sxs-lookup"><span data-stu-id="48e13-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="48e13-113">Untuk mencipta templat kalendar bagi organisasi anda, terdapat dua keperluan utama:</span><span class="sxs-lookup"><span data-stu-id="48e13-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="48e13-114">Takrifkan waktu kerja yang dikehendaki bagi templat menggunakan sumber boleh ditempah baharu atau sedia ada.</span><span class="sxs-lookup"><span data-stu-id="48e13-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="48e13-115">Cipta templat kalendar baharu dan kaitkan templat dengan sumber oleh ditempah.</span><span class="sxs-lookup"><span data-stu-id="48e13-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="48e13-116">**Takrif waktu bekerja bagi templat**</span><span class="sxs-lookup"><span data-stu-id="48e13-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="48e13-117">Pergi ke **Sumber** \> **Sumber**.</span><span class="sxs-lookup"><span data-stu-id="48e13-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="48e13-118">Cipta sumber baharu untuk dirujuk dalam templat kalendar atau pilih sumber sedia ada.</span><span class="sxs-lookup"><span data-stu-id="48e13-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="48e13-119">Pilih tab **Waktu Kerja** bagi sumber dan lengkapkan arahan dalam [Tetapkan waktu kerja untuk sumber](/dynamics365/field-service/set-work-hours-resource.md) untuk mengkonfigurasikan peraturan kalendar.</span><span class="sxs-lookup"><span data-stu-id="48e13-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="48e13-120">**Cipta templat kalendar baharu**</span><span class="sxs-lookup"><span data-stu-id="48e13-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="48e13-121">Pergi ke **Tetapan** \> **Templat Kalendar**.</span><span class="sxs-lookup"><span data-stu-id="48e13-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="48e13-122">Pilih **Baharu** dan masukkan nama, perihalan dan sumber templat.</span><span class="sxs-lookup"><span data-stu-id="48e13-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="48e13-123">Apabila sumber dirujuk dalam templat kalendar, salinan kalendar sumber dikaitkan dengan templat kalendar.</span><span class="sxs-lookup"><span data-stu-id="48e13-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="48e13-124">Jika waktu bekerja bagi templat yang disalin berubah, perubahan itu tidak tersebar ke templat kalendar.</span><span class="sxs-lookup"><span data-stu-id="48e13-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="48e13-125">Kini anda boleh mengaitkan templat kerja dengan templat kalendar projek.</span><span class="sxs-lookup"><span data-stu-id="48e13-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

