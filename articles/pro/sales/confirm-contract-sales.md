---
title: Sahkan kontrak projek
description: Topik ini menyediakan maklumat tentang cara mengesahkan kontrak dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273839"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="05f8b-103">Sahkan kontrak projek</span><span class="sxs-lookup"><span data-stu-id="05f8b-103">Confirm a project contract</span></span>

<span data-ttu-id="05f8b-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="05f8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="05f8b-105">Kontrak projek dalam Dynamics 365 Project Operations boleh aktif dengan sebab **Disahkan** atau ditutup dengan sebab **Hilang**.</span><span class="sxs-lookup"><span data-stu-id="05f8b-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="05f8b-106">Apabila anda mengesahkan kontrak projek, kemas kini status daripada **Draf** kepada **Aktif** dan sebab status **Disahkan**.</span><span class="sxs-lookup"><span data-stu-id="05f8b-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="05f8b-107">Kontrak aktif atau tertutup tidak boleh diedit atau dibuka semula.</span><span class="sxs-lookup"><span data-stu-id="05f8b-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="05f8b-108">Kesan kewangan kerana mengesahkan kontrak projek</span><span class="sxs-lookup"><span data-stu-id="05f8b-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="05f8b-109">Selepas kontrak projek disahkan, aplikasi mengira semula kos dengan menterbalikkan aktual kos yang lama dan mencipta semula aktual kos yang baharu.</span><span class="sxs-lookup"><span data-stu-id="05f8b-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="05f8b-110">Aktual kos baharu kemudian diproses berdasarkan kepada kaedah pengebilan bagi baris kontrak projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="05f8b-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="05f8b-111">Jika aktual kos merujuk kepada baris kontrak Masa dan Bahan, aplikasi secara automatik mencipta semula aktual jualan yang belum dibilkan yang serupa.</span><span class="sxs-lookup"><span data-stu-id="05f8b-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="05f8b-112">Jika aktual kos merujuk kepada baris kontrak Harga Tetap, aplikasi berhenti memproses semula aktual kos.</span><span class="sxs-lookup"><span data-stu-id="05f8b-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="05f8b-113">Had tidak melebihi, persediaan boleh dituntut dan penetapan harga dan kos berdasarkan sebenar dinilai dan kemudian dikemas kini sebagai sebahagian daripada proses pengesahan.</span><span class="sxs-lookup"><span data-stu-id="05f8b-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="05f8b-114">Tutup kontrak projek sebagai hilang</span><span class="sxs-lookup"><span data-stu-id="05f8b-114">Close a project contract as lost</span></span>

<span data-ttu-id="05f8b-115">Apabila anda menutup kontrak projek sebagai hilang, status kontrak dikemas kini kepada **Ditutup** dan sebab status **Hilang**.</span><span class="sxs-lookup"><span data-stu-id="05f8b-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="05f8b-116">Kontrak projek menjadi baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="05f8b-116">The project contract becomes read-only.</span></span> <span data-ttu-id="05f8b-117">Dialog pengesahan diberikan sebelum perubahan selesai kerana anda tidak boleh membuka semula kontrak projek yang ditutup.</span><span class="sxs-lookup"><span data-stu-id="05f8b-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="05f8b-118">Jika kontrak projek yang ditutup sebagai hilang merujuk kepada projek pada barisnya, projek itu juga ditandakan sebagai ditutup.</span><span class="sxs-lookup"><span data-stu-id="05f8b-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="05f8b-119">Sebarang tempahan sumber dari hari tersebut ke hadapan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="05f8b-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="05f8b-120">Sebarang aktual jualan yang tidak dibilkan pada kontrak projek yang belum ada pada invois akan diterbalikkan.</span><span class="sxs-lookup"><span data-stu-id="05f8b-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="05f8b-121">Dalam Dynamics 365 Project Operations, menutup kontrak projek sebagai hilang tidak akan memberi kesan kepada status peluang yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="05f8b-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="05f8b-122">Peluang akan kekal terbuka dan mesti ditutup secara manual.</span><span class="sxs-lookup"><span data-stu-id="05f8b-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]