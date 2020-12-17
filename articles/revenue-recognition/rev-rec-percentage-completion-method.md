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
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531504"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="fd694-103">Projek anggaran hasil harga tetap</span><span class="sxs-lookup"><span data-stu-id="fd694-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="fd694-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="fd694-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fd694-105">Apabila anda mencipta baris kontrak projek dengan atribut berikut dalam Dynamics 365 Project Operations pada Microsoft Dataverse, sistem secara automatik mencipta projek anggaran hasil harga tetap.</span><span class="sxs-lookup"><span data-stu-id="fd694-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="fd694-106">Maklumat dalam projek ini adalah berdasarkan perkara berikut:</span><span class="sxs-lookup"><span data-stu-id="fd694-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="fd694-107">Kaedah pengebilan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="fd694-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="fd694-108">Projek yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="fd694-108">An associated project.</span></span>
  - <span data-ttu-id="fd694-109">Sekurang-kurangnya satu pencapaian ditakrifkan pada tab **Jadual invois** pada halaman **Baris kontrak projek**.</span><span class="sxs-lookup"><span data-stu-id="fd694-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="fd694-110">Semak projek anggaran hasil harga tetap</span><span class="sxs-lookup"><span data-stu-id="fd694-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="fd694-111">Untuk menyemak projek anggaran hasil harga tetap, lengkapkan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="fd694-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="fd694-112">Dalam persekitaran Dynamics 365 Finance, pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Projek anggaran hasil harga tetap**.</span><span class="sxs-lookup"><span data-stu-id="fd694-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="fd694-113">Pilih projek yang anda mahu lihat dan klik dua kali pada **ID projek anggaran** untuk membuka rekod dan menyemak butiran projek.</span><span class="sxs-lookup"><span data-stu-id="fd694-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="fd694-114">Kembangkan tab **Projek**. Anda akan melihat satu projek dalam grid **Projek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="fd694-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="fd694-115">Sistem ini menggunakan ini sebagai projek lalai kerana ia merupakan projek yang berkaitan dengan baris kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="fd694-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="fd694-116">Untuk mengubah perkaitan itu, pilih projek tambahan dan tambahkannya pada grid **Projek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="fd694-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="fd694-117">Jika berbilang projek dipilih dalam grid ini, peratusan penyelesaian projek dan anggaran hasil dikira bersama untuk semua projek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="fd694-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="fd694-118">Kos projek, profil hasil, templat kos dan kod tempoh boleh ditetapkan secara manual.</span><span class="sxs-lookup"><span data-stu-id="fd694-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="fd694-119">Jika ia tidak ditetapkan secara manual, nilai lalai semasa pengiraan anggaran pertama untuk projek menggunakan peraturan yang dikonfigurasikan untuk kos projek dan profil hasil.</span><span class="sxs-lookup"><span data-stu-id="fd694-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

