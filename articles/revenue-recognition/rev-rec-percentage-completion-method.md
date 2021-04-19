---
title: Projek anggaran hasil harga tetap
description: Topik ini memberikan maklumat tentang hasil harga tetap dalam projek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278924"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="de036-103">Projek anggaran hasil harga tetap</span><span class="sxs-lookup"><span data-stu-id="de036-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="de036-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="de036-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="de036-105">Apabila anda mencipta baris kontrak projek dengan atribut berikut dalam Dynamics 365 Project Operations pada Microsoft Dataverse, sistem secara automatik mencipta projek anggaran hasil harga tetap.</span><span class="sxs-lookup"><span data-stu-id="de036-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="de036-106">Maklumat dalam projek ini adalah berdasarkan perkara berikut:</span><span class="sxs-lookup"><span data-stu-id="de036-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="de036-107">Kaedah pengebilan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="de036-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="de036-108">Projek yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="de036-108">An associated project.</span></span>
  - <span data-ttu-id="de036-109">Sekurang-kurangnya satu pencapaian ditakrifkan pada tab **Jadual invois** pada halaman **Baris kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="de036-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="de036-110">Semak projek anggaran hasil harga tetap</span><span class="sxs-lookup"><span data-stu-id="de036-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="de036-111">Untuk menyemak projek anggaran hasil harga tetap, lengkapkan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="de036-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="de036-112">Dalam persekitaran Dynamics 365 Finance, pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Projek anggaran hasil harga tetap**.</span><span class="sxs-lookup"><span data-stu-id="de036-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="de036-113">Pilih projek yang anda mahu lihat dan klik dua kali pada **ID projek anggaran** untuk membuka rekod dan menyemak butiran projek.</span><span class="sxs-lookup"><span data-stu-id="de036-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="de036-114">Kembangkan tab **Projek**. Anda akan melihat satu projek dalam grid **Projek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="de036-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="de036-115">Sistem ini menggunakan ini sebagai projek lalai kerana ia merupakan projek yang berkaitan dengan baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="de036-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="de036-116">Untuk mengubah perkaitan itu, pilih projek tambahan dan tambahkannya pada grid **Projek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="de036-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="de036-117">Jika berbilang projek dipilih dalam grid ini, peratusan penyelesaian projek dan anggaran hasil dikira bersama untuk semua projek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="de036-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="de036-118">Kos projek, profil hasil, templat kos dan kod tempoh boleh ditetapkan secara manual.</span><span class="sxs-lookup"><span data-stu-id="de036-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="de036-119">Jika ia tidak ditetapkan secara manual, nilai lalai semasa pengiraan anggaran pertama untuk projek menggunakan peraturan yang dikonfigurasikan untuk kos projek dan profil hasil.</span><span class="sxs-lookup"><span data-stu-id="de036-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]