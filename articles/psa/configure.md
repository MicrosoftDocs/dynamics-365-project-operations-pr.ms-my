---
title: Konfigurasikan Project Service Automation
description: Langkah untuk mengkonfigurasikan Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129194"
---
# <a name="configure-project-service"></a><span data-ttu-id="525e0-103">Konfigurasikan Project Service</span><span class="sxs-lookup"><span data-stu-id="525e0-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="525e0-104">Sebelum anda menggunakan keupayaan automasi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dalam [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] untuk mengurus akaun, projek dan sumber anda, anda perlu beberapa langkah konfigurasi untuk memastikan penyelesaian [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sepadan dengan keperluan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="525e0-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="525e0-105">Langkah-langkah ini termasuk:</span><span class="sxs-lookup"><span data-stu-id="525e0-105">These steps include:</span></span>  
  
-   <span data-ttu-id="525e0-106">[Sediakan unit masa](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="525e0-107">Konfigurasikan unit masa dalam katalog produk yang akan anda gunakan sebagai asas untuk penjadualan dan pengebilan projek anda.</span><span class="sxs-lookup"><span data-stu-id="525e0-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="525e0-108">[Sediakan mata wang dan kadar pertukaran](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="525e0-109">Sediakan mata wang untuk kegunaan projek anda.</span><span class="sxs-lookup"><span data-stu-id="525e0-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="525e0-110">[Cipta unit organisasi](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="525e0-111">Sediakan kumpulan yang syarikat anda gunakan untuk membahagikan perniagaannya, sama ada mengikut geografi, fungsi perniagaan atau bahagian logik lain.</span><span class="sxs-lookup"><span data-stu-id="525e0-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="525e0-112">[Sediakan kekerapan invois](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="525e0-113">Sediakan tempoh masa yang anda mahu gunakan untuk pengebilan klien anda.</span><span class="sxs-lookup"><span data-stu-id="525e0-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="525e0-114">[Konfigurasikan kategori transaksi](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="525e0-115">Sediakan kategori transaksi yang perunding anda boleh kenakan caj perbelanjaan boleh dibilkan dan tidak boleh dibilkan padanya.</span><span class="sxs-lookup"><span data-stu-id="525e0-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="525e0-116">[Konfigurasikan kategori perbelanjaan](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="525e0-117">Sediakan kategori yang perunding anda boleh kenakan caj perbelanjaan boleh dibilkan dan tidak boleh dibilkan padanya.</span><span class="sxs-lookup"><span data-stu-id="525e0-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="525e0-118">[Cipta item katalog produk](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="525e0-119">Tambah produk yang anda jual, seperti lesen perisian, pada katalog produk.</span><span class="sxs-lookup"><span data-stu-id="525e0-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="525e0-120">[Cipta senarai harga](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="525e0-121">Konfigurasikan senarai harga berbeza, bergantung pada jumlah caj yang anda mahu kenakan pada klien adan bagi setiap peranan yang projek mereka perlukan.</span><span class="sxs-lookup"><span data-stu-id="525e0-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="525e0-122">[Sediakan sumber](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="525e0-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="525e0-123">Tambah kemahiran, kecekapan, peranan sumber dan maklumat sumber lain yang akan anda perlukan untuk projek anda.</span><span class="sxs-lookup"><span data-stu-id="525e0-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="525e0-124">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="525e0-124">See Also</span></span>  
 <span data-ttu-id="525e0-125">[Gambaran Keseluruhan Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="525e0-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="525e0-126">[Konfigurasikan Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="525e0-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="525e0-127">[Panduan Pengurus Akaun](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="525e0-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="525e0-128">[Panduan Pengurus Projek](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="525e0-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="525e0-129">[Panduan Pengurus Sumber](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="525e0-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="525e0-130">Panduan Masa, Perbelanjaan dan Kerjasama</span><span class="sxs-lookup"><span data-stu-id="525e0-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
