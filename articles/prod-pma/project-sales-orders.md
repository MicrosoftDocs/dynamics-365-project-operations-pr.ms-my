---
title: Projek pesanan jualan untuk projek masa dan bahan
description: Topik ini menjelaskan cara untuk mencipta pesanan jualan berasaskan projek untuk projek masa dan bahan.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009672"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="4735a-103">Projek pesanan jualan untuk projek masa dan bahan</span><span class="sxs-lookup"><span data-stu-id="4735a-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4735a-104">Topik ini menerangkan cara untuk mencipta pesanan jualan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="4735a-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="4735a-105">Pesanan jualan hanya boleh dicipta untuk projek jenis **masa dan bahan**.</span><span class="sxs-lookup"><span data-stu-id="4735a-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="4735a-106">Jika projek masa dan bahan mempunyai pelbagai sumber pembiayaan pada kontrak projek, anda mesti mendayakan **Benarkan pesanan jualan untuk projek dengan pelbagai sumber pembiayaan** parameter pada halaman **Pengurusan projek dan parameter perakaunan**.</span><span class="sxs-lookup"><span data-stu-id="4735a-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="4735a-107">Sokongan untuk pesanan jualan projek dengan sumber pembiayaan tersedia bermula dengan keluaran aplikasi 10.0.2 dan lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="4735a-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="4735a-108">Parameter untuk mendayakan sokongan untuk pesanan jualan projek dengan pelbagai sumber pembiayaan akan dialih keluar dalam gelombang keluaran April 2020, yang mana kefungsian akan sentiasa didayakan.</span><span class="sxs-lookup"><span data-stu-id="4735a-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="4735a-109">Anda boleh mencipta pesanan jualan berasaskan projek dalam dua cara:</span><span class="sxs-lookup"><span data-stu-id="4735a-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="4735a-110">Pergi ke projek itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="4735a-110">Go to the project itself.</span></span> <span data-ttu-id="4735a-111">Pada Anak Tetingkap Tindakan, pilih **Urus > tugas Item > Pesanan jualan**.</span><span class="sxs-lookup"><span data-stu-id="4735a-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="4735a-112">Maklumat projek akan menjadi lalai kepada pesanan jualan daripada projek.</span><span class="sxs-lookup"><span data-stu-id="4735a-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="4735a-113">Jika kontrak projek mempunyai lebih daripada satu sumber pembiayaan, anda akan perlu untuk memilih sumber pembiayaan untuk menetapkan pelanggan bagi pesanan jualan.</span><span class="sxs-lookup"><span data-stu-id="4735a-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="4735a-114">Jika terdapat hanya satu pembiayaan untuk projek itu, pelanggan akan ditetapkan secara automatik.</span><span class="sxs-lookup"><span data-stu-id="4735a-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="4735a-115">Pergi ke halaman senarai **Semua pesanan jualan** dan cipta pesanan jualan baharu.</span><span class="sxs-lookup"><span data-stu-id="4735a-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="4735a-116">Anda akan perlu untuk memilih projek bagi pesanan jualan.</span><span class="sxs-lookup"><span data-stu-id="4735a-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="4735a-117">Selepas projek itu dipilih, pelanggan akan ditetapkan daripada sumber pembiayaan atau anda akan perlu untuk memilih sumber pembiayaan jika kontrak projek mempunyai pelbagai sumber pembiayaan.</span><span class="sxs-lookup"><span data-stu-id="4735a-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]