---
title: Cipta invois proforma manual - ringan
description: Topik ini menyediakan maklumat tentang mencipta invois proforma manual dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274199"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="88b3d-103">Cipta invois proforma manual - ringan</span><span class="sxs-lookup"><span data-stu-id="88b3d-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="88b3d-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="88b3d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="88b3d-105">Dalam Dynamics 365 Project Operations, invois proforma boleh dicipta secara manual seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="88b3d-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="88b3d-106">Anda boleh mencipta invois proforma secara manual daripada halaman senarai **Kontrak Projek** atau daripada halaman butiran **Kontrak Projek**.</span><span class="sxs-lookup"><span data-stu-id="88b3d-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="88b3d-107">Halaman senarai Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="88b3d-107">Project Contracts list page</span></span>

<span data-ttu-id="88b3d-108">Daripada halaman senarai **Kontrak Projek**, pilih satu atau lebih kontrak projek dan cipta invois untuk semua rekod yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="88b3d-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="88b3d-109">Sistem menyemak untuk melihat kontrak projek dipilih yang mempunyai tunggakan **Sedia untuk Invois** bertarikh sebelum tarikh hari ini.</span><span class="sxs-lookup"><span data-stu-id="88b3d-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="88b3d-110">Daripada kontrak tersebut, sistem mencipta invois proforma draf.</span><span class="sxs-lookup"><span data-stu-id="88b3d-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="88b3d-111">Jika kontrak projek mempunyai berbilang pelanggan, mungkin terdapat satu invois yang dicipta bagi setiap pelanggan dan berbilang invois bagi setiap kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="88b3d-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="88b3d-112">Semua invois projek yang dicipta tersedia pada halaman **Invois** dalam bahagian **Pengebilan** bagi kawasan **Jualan**.</span><span class="sxs-lookup"><span data-stu-id="88b3d-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="88b3d-113">Halaman butiran Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="88b3d-113">Project Contract details page</span></span>

<span data-ttu-id="88b3d-114">Invois proforma juga boleh dicipta daripada halaman butiran **Kontrak Projek**.</span><span class="sxs-lookup"><span data-stu-id="88b3d-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="88b3d-115">Sistem mengesahkan kontrak projek mempunyai tunggakan **Sedia untuk Invois** bertarikh sebelum tarikh hari ini.</span><span class="sxs-lookup"><span data-stu-id="88b3d-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="88b3d-116">Daripada kontrak ini, sistem mencipta invois proforma draf berdasarkan bilangan pelanggan pada setiap baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="88b3d-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="88b3d-117">Apabila terdapat invois proforma tunggal yang dicipta, halaman **Invois** dibuka.</span><span class="sxs-lookup"><span data-stu-id="88b3d-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="88b3d-118">Jika berbilang invois dicipta untuk kontrak projek tersebut, halaman senarai **Invois** dibuka untuk menunjukkan semua invois yang dicipta.</span><span class="sxs-lookup"><span data-stu-id="88b3d-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]