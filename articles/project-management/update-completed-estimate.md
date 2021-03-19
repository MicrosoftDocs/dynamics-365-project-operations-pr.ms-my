---
title: Kemas kini anggaran ketika selesai
description: Topik ini menyediakan maklumat tentang pengemaskinian unjuran usaha ke atas projek.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286439"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="d5f59-103">Kemas kini anggaran ketika selesai</span><span class="sxs-lookup"><span data-stu-id="d5f59-103">Update estimate at completion</span></span>

<span data-ttu-id="d5f59-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="d5f59-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5f59-105">Ia adalah perkara biasa bagi pengurus projek untuk menyemak semula anggaran asal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="d5f59-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="d5f59-106">Unjuran semula projek ialah persepsi pengurus projek berkenaan anggaran, memandangkan keadaan projek semasa.</span><span class="sxs-lookup"><span data-stu-id="d5f59-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="d5f59-107">Walau bagaimanapun, kami tidak mengesyorkan agar pengurus projek mengubah nombor garis dasar, kerana garis dasar projek mewakili sumber kebenaran yang sudah mantap bagi jadual dan anggaran kos projek, dan semua pemegang amanah projek telah bersetuju dengannya.</span><span class="sxs-lookup"><span data-stu-id="d5f59-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="d5f59-108">Terdapat dua cara pengurus projek boleh mengunjurkan semula usaha pada tugas:</span><span class="sxs-lookup"><span data-stu-id="d5f59-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="d5f59-109">Menggantikan anggaran lalai untuk melengkapkan (ETC) dengan anggaran baharu bagi usaha aktual yang tinggal pada tugas.</span><span class="sxs-lookup"><span data-stu-id="d5f59-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="d5f59-110">Ganti peratusan kemajuan lalai dengan anggaran baharu bagi kemajuan sebenar tugas.</span><span class="sxs-lookup"><span data-stu-id="d5f59-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="d5f59-111">Setiap pendekatan ini menyebabkan pengiraan semula ETC, anggaran ketika selesai (EAC) dan peratusan kemajuan tugas serta varians usaha yang diunjurkan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="d5f59-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="d5f59-112">EAC, ETC dan peratusan kemajuan pada tugas ringkasan juga dikira semula dan menghasilkan unjuran baharu bagi varians usaha.</span><span class="sxs-lookup"><span data-stu-id="d5f59-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]