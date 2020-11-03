---
title: Mencipta invois proforma manual
description: Topik ini menyediakan maklumat tentang mencipta invois proforma manual dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081457"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="40d26-103">Mencipta invois proforma manual</span><span class="sxs-lookup"><span data-stu-id="40d26-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="40d26-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="40d26-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40d26-105">Dalam Dynamics 365 Project Operations, invois proforma boleh dicipta secara manual apabila diperlukan.</span><span class="sxs-lookup"><span data-stu-id="40d26-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="40d26-106">Anda boleh mencipta invois proforma secara manual daripada halaman senarai **Kontrak Projek** atau daripada halaman butiran **Kontrak Projek**.</span><span class="sxs-lookup"><span data-stu-id="40d26-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="40d26-107">Halaman senarai Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="40d26-107">Project Contracts list page</span></span>

<span data-ttu-id="40d26-108">Daripada halaman senarai **Kontrak Projek** , pilih satu atau lebih kontrak projek dan cipta invois untuk semua rekod yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="40d26-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="40d26-109">Sistem menyemak untuk melihat kontrak projek yang dipilih yang mempunyai tunggakan **Bersedia untuk Invois** bertarikh sebelum tarikh hari ini.</span><span class="sxs-lookup"><span data-stu-id="40d26-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="40d26-110">Daripada kontrak tersebut, sistem mencipta invois proforma draf.</span><span class="sxs-lookup"><span data-stu-id="40d26-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="40d26-111">Jika kontrak projek mempunyai berbilang pelanggan, mungkin terdapat satu invois yang dicipta bagi setiap pelanggan dan berbilang invois bagi setiap kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="40d26-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="40d26-112">Semua invois projek yang dicipta tersedia pada halaman **Invois** dalam bahagian **Pengebilan** bagi kawasan **Jualan**.</span><span class="sxs-lookup"><span data-stu-id="40d26-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="40d26-113">Halaman butiran Kontrak Projek</span><span class="sxs-lookup"><span data-stu-id="40d26-113">Project Contract details page</span></span>

<span data-ttu-id="40d26-114">Invois proforma juga boleh dicipta daripada halaman butiran **Kontrak Projek** , yang mencipta invois untuk kontrak projek khusus tersebut.</span><span class="sxs-lookup"><span data-stu-id="40d26-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="40d26-115">Sistem mengesahkan bahawa kontrak projek mempunyai tunggakan **Bersedia untuk Invois** yang bertarikh sebelum tarikh hari ini.</span><span class="sxs-lookup"><span data-stu-id="40d26-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="40d26-116">Daripada kontrak ini, sistem mencipta invois proforma draf berdasarkan bilangan pelanggan pada setiap baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="40d26-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="40d26-117">Apabila terdapat invois proforma tunggal yang dicipta, halaman **Invois** dibuka.</span><span class="sxs-lookup"><span data-stu-id="40d26-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="40d26-118">Jika terdapat berbilang invois yang dicipta untuk kontrak projek tersebut, maka halaman senarai **Invois** dibuka untuk menunjukkan semua invois yang dicipta.</span><span class="sxs-lookup"><span data-stu-id="40d26-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
