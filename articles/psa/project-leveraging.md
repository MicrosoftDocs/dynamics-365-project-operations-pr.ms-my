---
title: Anggaran projek dan jualan
description: Topik ini menyediakan maklumat mengenai cara untuk mengambil kesempatan daripada jadual dan anggaran dalam proses jualan.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148384"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="4e162-103">Anggaran projek dan jualan</span><span class="sxs-lookup"><span data-stu-id="4e162-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4e162-104">Semasa proses jualan, anda boleh mencipta anggaran jualan dengan memautkan projek kepada sebut harga jualan.</span><span class="sxs-lookup"><span data-stu-id="4e162-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="4e162-105">Dengan cara ini, anggaran berketentuan boleh berlaku semasa proses jualan, untuk mengambil kesempatan penjadualan projek dan keupayaan anggaran.</span><span class="sxs-lookup"><span data-stu-id="4e162-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="4e162-106">Jika jualan berjaya, jadual yang digunakan untuk tujuan anggaran jualan boleh digunakan sebagai asas untuk penghalusan lanjut pelan projek.</span><span class="sxs-lookup"><span data-stu-id="4e162-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="4e162-107">Memautkan projek kepada baris sebut harga</span><span class="sxs-lookup"><span data-stu-id="4e162-107">Linking a project to a quote line</span></span>

<span data-ttu-id="4e162-108">Apabila anda mencipta baris sebut harga berdasarkan projek, anda boleh mencipta projek baharu atau mengaitkan projek sedia ada pada halaman **Baris Sebut Harga**.</span><span class="sxs-lookup"><span data-stu-id="4e162-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Borang Baris Sebut Harga](media/project-8.png)
 
<span data-ttu-id="4e162-110">Apabila anda mencipta projek baharu daripada butiran baris sebut harga, anda boleh mengambil kesempatan daripada templat projek.</span><span class="sxs-lookup"><span data-stu-id="4e162-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="4e162-111">Templat projek ialah projek model yang mewakili rancangan projek standard dan anggaran kewangan yang biasa dalam sesebuah organisasi.</span><span class="sxs-lookup"><span data-stu-id="4e162-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="4e162-112">Ia juga boleh mewakili salinan rancangan projek dan anggaran dari projek yang lepas.</span><span class="sxs-lookup"><span data-stu-id="4e162-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Butiran baris sebut harga](media/project-9.png)
  
<span data-ttu-id="4e162-114">Apabila anda mencipta projek daripada sebut harga, projek secara automatik dikaitkan dengan baris sebut harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="4e162-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="4e162-115">Komponen anggaran dalam projek</span><span class="sxs-lookup"><span data-stu-id="4e162-115">Components of estimates in a project</span></span>

<span data-ttu-id="4e162-116">Jadual membolehkan anda membahagikan kerja ke dalam tugas, mengekalkan hierarki tugas, menentukan sumber yang diperlukan untuk melengkapkan tugas dan menugaskan anggaran usaha yang diperlukan untuk melengkapkan tugas.</span><span class="sxs-lookup"><span data-stu-id="4e162-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="4e162-117">Anda boleh mentakrifkan usaha kerja dan menjadualkan anggaran dengan menggunakan medan pada tab **Jadual** halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="4e162-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="4e162-118">Oleh sebab senarai harga dikaitkan dengan projek, anggaran kewangan dikira dengan menggunakan harga kos dan jualan yang ditentukan dalam senarai harga.</span><span class="sxs-lookup"><span data-stu-id="4e162-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="4e162-119">Mengimport anggaran daripada projek ke dalam sebut harga</span><span class="sxs-lookup"><span data-stu-id="4e162-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="4e162-120">Selepas anda mentakrifkan anggaran projek, anda boleh mengimportnya ke dalam baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="4e162-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="4e162-121">Pada halaman **Butiran Baris Sebut Harga**, pilih **Import daripada anggaran** pada reben untuk merumuskan anggaran projek mengikut jenis transaksi, peranan atau peringkat tugas.</span><span class="sxs-lookup"><span data-stu-id="4e162-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
