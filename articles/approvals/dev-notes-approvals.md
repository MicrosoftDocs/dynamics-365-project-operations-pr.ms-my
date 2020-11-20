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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483959"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="ae84c-103">Nota pemaju untuk Kelulusan</span><span class="sxs-lookup"><span data-stu-id="ae84c-103">Developer notes for Approvals</span></span>

<span data-ttu-id="ae84c-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="ae84c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae84c-105">Dynamics 365 Project Operations termasuk logik pengesahan yang memastikan peralihan rekod yang betul melalui peringkat kelulusan.</span><span class="sxs-lookup"><span data-stu-id="ae84c-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="ae84c-106">Rekod peralihan yang betul pastikan:</span><span class="sxs-lookup"><span data-stu-id="ae84c-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="ae84c-107">Semua baris sokongan dicipta dalam jadual yang berkaitan, seperti jurnal dan aktual.</span><span class="sxs-lookup"><span data-stu-id="ae84c-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="ae84c-108">Pelulus tersebut ditandakan sebagai **Pelulus Projek** dalam projek itu sebelum meneruskan.</span><span class="sxs-lookup"><span data-stu-id="ae84c-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
