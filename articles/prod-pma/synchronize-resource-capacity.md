---
title: Segerakkan kapasiti sumber
description: Topik ini memberikan maklumat mengenai cara menyegerakkan kapasiti sumber merentasi kalendar dan projek.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997522"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="7a39f-103">Segerakkan kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="7a39f-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a39f-104">Proses untuk penyegerakan sumber membantu menjamin yang maklumat untuk kalendar dan kalendar asas masuk ke dalam penjadualan sumber projek.</span><span class="sxs-lookup"><span data-stu-id="7a39f-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="7a39f-105">Jika kalendar diubah, proses membuat kemas kini yang diperlukan untuk penjadualan sumber projek.</span><span class="sxs-lookup"><span data-stu-id="7a39f-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="7a39f-106">Proses ini juga membantu menambah baik prestasi, kerana maklumat sumber kalendar disegerakkan lebih awal.</span><span class="sxs-lookup"><span data-stu-id="7a39f-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="7a39f-107">Oleh itu, kemas kini kepada maklumat penjadualan sumber berlaku lebih cepat.</span><span class="sxs-lookup"><span data-stu-id="7a39f-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="7a39f-108">Kami mengesyorkan anda menjadualkan proses sebagai kelompok dan bukannya satu demi satu.</span><span class="sxs-lookup"><span data-stu-id="7a39f-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="7a39f-109">Jika tidak, ada risiko bahawa seseorang akan melupakan tarikh yang terangkum apabila maklumat terakhir disegerakkan.</span><span class="sxs-lookup"><span data-stu-id="7a39f-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="7a39f-110">Jika tarikh yang terangkum tidak digunakan, jurang boleh berlaku semasa tarikh penyegerakan.</span><span class="sxs-lookup"><span data-stu-id="7a39f-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Penyegerakan kalendar](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="7a39f-112">Segerakkan gulungan kapasiti sumber</span><span class="sxs-lookup"><span data-stu-id="7a39f-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="7a39f-113">Proses penyegerakan direka untuk segerakkan semua maklumat kalendar sumber.</span><span class="sxs-lookup"><span data-stu-id="7a39f-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="7a39f-114">Maklumat ini termasuk maklumat kalendar asas mengenai sebarang perubahan kepada jadual Kapasiti kalendar sumber projek.</span><span class="sxs-lookup"><span data-stu-id="7a39f-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="7a39f-115">Jika sumber baharu ditambah dalam projek ini, penyegerakan membantu menjamin bahawa maklumat kalendar yang dikemas kini tersedia.</span><span class="sxs-lookup"><span data-stu-id="7a39f-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="7a39f-116">Penyegerakan ini boleh dilakukan pada bila-bila masa.</span><span class="sxs-lookup"><span data-stu-id="7a39f-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="7a39f-117">Kami mengesyorkan agar anda menggunakan kelompok.</span><span class="sxs-lookup"><span data-stu-id="7a39f-117">We recommend that you use a batch.</span></span> <span data-ttu-id="7a39f-118">Pilihan boleh tersedia semasa penyegerakan penempahan kapasiti.</span><span class="sxs-lookup"><span data-stu-id="7a39f-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="7a39f-119">Pilih **Pengurusan projek dan perakaunan** &gt; **Berkala** &gt; **Penyegerakan kapasiti** &gt; **Segerakkan gulungan kapasiti sumber**.</span><span class="sxs-lookup"><span data-stu-id="7a39f-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="7a39f-120">Tetapkan pilihan dalam jadual berikut.</span><span class="sxs-lookup"><span data-stu-id="7a39f-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="7a39f-121">Pilihan</span><span class="sxs-lookup"><span data-stu-id="7a39f-121">Option</span></span>      | <span data-ttu-id="7a39f-122">Penerangan</span><span class="sxs-lookup"><span data-stu-id="7a39f-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="7a39f-123">Kod tempoh</span><span class="sxs-lookup"><span data-stu-id="7a39f-123">Period code</span></span> | <span data-ttu-id="7a39f-124">Secara alternatif pilih kod selang tarikh Lejar am untuk menetapkan tarikh mula dan tamat untuk proses penyegerakan untuk gulungan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="7a39f-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7a39f-125">Tarikh mula</span><span class="sxs-lookup"><span data-stu-id="7a39f-125">Start date</span></span>  | <span data-ttu-id="7a39f-126">Masukkan tarikh mula untuk proses penyegerakan untuk gulungan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="7a39f-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7a39f-127">Tarikh tamat</span><span class="sxs-lookup"><span data-stu-id="7a39f-127">End date</span></span>    | <span data-ttu-id="7a39f-128">Masukkan tarikh tamat untuk proses penyegerakan untuk gulungan kapasiti sumber.</span><span class="sxs-lookup"><span data-stu-id="7a39f-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="7a39f-129">[![Proses penyegerakan](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a39f-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]