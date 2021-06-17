---
title: Berikan anggaran kerja untuk projek semasa proses jualan
description: Cara untuk menyediakan anggaran kerja untuk projek sepanjang proses jualan dalam Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998242"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="c2029-103">Sediakan anggaran kerja untuk projek sepanjang proses jualan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c2029-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c2029-104">Sepanjang proses jualan, anda boleh menghasilkan anggaran jualan dari asas dengan barisan sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c2029-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="c2029-105">Keupayaan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dalam [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] menyediakan lebih banyak cara saintifik dan berketentuan yang datang dengan anggaran jualan dengan memecahkan item kerja dan mengaitkan atribut berkaitan yang menyumbang terhadap anggaran untuk projek dalam struktur pecahan kerja,</span><span class="sxs-lookup"><span data-stu-id="c2029-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="c2029-106">Sebaik sahaja anda memenangi jualan, anda boleh menggunakan struktur pecahan kerja berkaitan dalam rancangan projek anda, menghalusinya seperti yang diperlukan untuk berjaya melengkapkan projek anda.</span><span class="sxs-lookup"><span data-stu-id="c2029-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="c2029-107">Pautkan projek dengan barisan sebut harga</span><span class="sxs-lookup"><span data-stu-id="c2029-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="c2029-108">Apabila mencipta barisan sebut harga berdasarkan projek, anda boleh mencipta projek baharu daripada barisan sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c2029-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="c2029-109">Anda kemudiannya boleh menggunakan templat projek yang sama ada rancangan projek standard yang diprakonfigurasikan dan anggaran kewangan yang biasa untuk organisasi anda atau salinan rancangan projek dan anggaran daripada projek terdahulu.</span><span class="sxs-lookup"><span data-stu-id="c2029-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="c2029-110">Apabila anda mencipta projek, memilih templat projek menyediakan asas untuk menghalusi rancangan projek, anggaran dan keperluan peranan.</span><span class="sxs-lookup"><span data-stu-id="c2029-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="c2029-111">Dengan mencipta projek anda daripada sebut harga, projek dikaitkan secara automatik dengan barisan sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c2029-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="c2029-112">Komponen anggaran projek</span><span class="sxs-lookup"><span data-stu-id="c2029-112">Project estimate components</span></span>  
 <span data-ttu-id="c2029-113">Struktur pecahan kerja dalam projek menyediakan cara untuk memecahkan kerja kepada tugas, mengekalkan hierarki tugas dan menguntukkan anggaran usaha yang diperlukan untuk melengkapkan setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="c2029-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="c2029-114">Anda juga boleh mengaitkan peranan dengan tugas untuk menunjukkan anggaran jenis sumber yang diperlukan bagi melengkapkan tugas dan jadual.</span><span class="sxs-lookup"><span data-stu-id="c2029-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="c2029-115">Struktur pecahan kerja membantu anda menentukan usaha kerja dan anggaran jadual.</span><span class="sxs-lookup"><span data-stu-id="c2029-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="c2029-116">Secara lalai, projek ini menggunakan senarai harga lalai yang anda takrifkan lebih awal.</span><span class="sxs-lookup"><span data-stu-id="c2029-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="c2029-117">Kos dan harga jualan yang ditakrifkan dalam senarai harga membantu menentukan anggaran kewangan untuk pecahan kerja projek.</span><span class="sxs-lookup"><span data-stu-id="c2029-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="c2029-118">Jika projek anda dikaitkan dengan sebut harga dan sebut harga tersebut mempunyai senarai harga yang berbeza daripada lalai, senarai harga sebut harga digunakan untuk anggaran kewangan.</span><span class="sxs-lookup"><span data-stu-id="c2029-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c2029-119">Import anggaran daripada projek ke dalam sebut harga</span><span class="sxs-lookup"><span data-stu-id="c2029-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="c2029-120">Sebaik sahaja anda mempunyai anggaran projek dalam projek, anda boleh mengimport anggaran ini ke dalam baris sebut harga:</span><span class="sxs-lookup"><span data-stu-id="c2029-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="c2029-121">Dalam **Butiran Barisan Sebut Harga**, klik **Import daripada anggaran**.</span><span class="sxs-lookup"><span data-stu-id="c2029-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="c2029-122">Pilih sama ada hendak mengimport anggaran projek yang diringkaskan oleh jenis transaksi atau tahap nod struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="c2029-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c2029-123">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="c2029-123">See Also</span></span>  
 [<span data-ttu-id="c2029-124">Panduan Pengurus Projek</span><span class="sxs-lookup"><span data-stu-id="c2029-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]