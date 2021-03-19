---
title: Nota pemaju untuk Kelulusan
description: Topik ini menyediakan maklumat tambahan pembagun tentang bekerja dengan pelulus.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290280"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="f63a6-103">Nota pemaju untuk Kelulusan</span><span class="sxs-lookup"><span data-stu-id="f63a6-103">Developer notes for Approvals</span></span>

<span data-ttu-id="f63a6-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="f63a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f63a6-105">Dynamics 365 Project Operations termasuk logik pengesahan yang memastikan peralihan rekod yang betul melalui peringkat kelulusan.</span><span class="sxs-lookup"><span data-stu-id="f63a6-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="f63a6-106">Rekod peralihan yang betul pastikan:</span><span class="sxs-lookup"><span data-stu-id="f63a6-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="f63a6-107">Semua baris sokongan dicipta dalam jadual yang berkaitan, seperti jurnal dan aktual.</span><span class="sxs-lookup"><span data-stu-id="f63a6-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="f63a6-108">Pelulus tersebut ditandakan sebagai **Pelulus Projek** dalam projek itu sebelum meneruskan.</span><span class="sxs-lookup"><span data-stu-id="f63a6-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]