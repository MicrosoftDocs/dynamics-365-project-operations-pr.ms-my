---
title: Integrasi dwi tulis Project Operations
description: Topik ini memberikan gambaran keseluruhan bagi integrasi dwi tulis Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955669"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="1aa70-103">Gambaran keseluruhan integrasi dwi tulis Project Operations</span><span class="sxs-lookup"><span data-stu-id="1aa70-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="1aa70-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="1aa70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1aa70-105">Project Operations menggunakan [keupayaan dwi tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) untuk menyegerakkan data merentasi Microsoft Dataverse dan Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1aa70-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="1aa70-106">Ilustrasi berikut menunjukkan cara data disegerakkan sebagai sebahagian daripada integrasi ini antara Dataverse dan Kewangan.</span><span class="sxs-lookup"><span data-stu-id="1aa70-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Gambaran keseluruhan aliran data Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="1aa70-108">Project Operations pada Dataverse menyediakan antara muka pengguna moden (UI) dan kebolehpanjangan mudah tanpa kod/kod rendah menggunakan keupayaan Power Platform.</span><span class="sxs-lookup"><span data-stu-id="1aa70-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="1aa70-109">Pengurus Projek, pengurus Sumber, ahli pasukan Projek dan persona pejabat depan yang lain, melaksanakan aktiviti mereka dalam Project Operations pada Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1aa70-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="1aa70-110">Project Operations dalam Kewangan menyediakan perakaunan projek dan sokongan pengiktirafan hasil.</span><span class="sxs-lookup"><span data-stu-id="1aa70-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="1aa70-111">Pasang masuk Project Operations ke kerangka kerja kewangan dalam Kewangan untuk pengiraan cukai jualan, kadar pertukaran mata wang, pelaporan dimensi kewangan dan banyak lagi.</span><span class="sxs-lookup"><span data-stu-id="1aa70-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="1aa70-112">Pengalaman akauntan Projek kebanyakannya berasaskan dalam kewangan.</span><span class="sxs-lookup"><span data-stu-id="1aa70-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="1aa70-113">Integrasi Project Operations terdiri daripada integrasi komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="1aa70-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="1aa70-114">Persediaan Project Operations dan integrasi data konfigurasi</span><span class="sxs-lookup"><span data-stu-id="1aa70-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="1aa70-115">Anggaran dan aktual Projek</span><span class="sxs-lookup"><span data-stu-id="1aa70-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="1aa70-116">Invois projek</span><span class="sxs-lookup"><span data-stu-id="1aa70-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="1aa70-117">Pengurusan perbelanjaan</span><span class="sxs-lookup"><span data-stu-id="1aa70-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="1aa70-118">Invois vendor</span><span class="sxs-lookup"><span data-stu-id="1aa70-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
