---
title: Sediakan kadar kos dan jualan untuk produk katalog - ringan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274469"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="11bba-103">Sediakan kadar kos dan jualan untuk produk katalog - ringan</span><span class="sxs-lookup"><span data-stu-id="11bba-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="11bba-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="11bba-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="11bba-105">Menyediakan harga untuk item katalog produk dalam Dynamics 365 Project Operations adalah sama seperti dalam Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="11bba-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="11bba-106">Dalam Project Operations, produk tidak boleh dianggarkan atau digunakan pada projek, maka harga katalog produk tidak perlu ditetapkan pada senarai harga projek untuk sebut harga dan kontrak.</span><span class="sxs-lookup"><span data-stu-id="11bba-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="11bba-107">Gunakan medan **Harga Produk** bagi sebut harga, kontrak atau akaun untuk menyediakan harga katalog produk.</span><span class="sxs-lookup"><span data-stu-id="11bba-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="11bba-108">Jangan sediakan harga katalog produk dalam senarai harga projek.</span><span class="sxs-lookup"><span data-stu-id="11bba-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="11bba-109">Senarai harga projek adalah eksklusif untuk Operasi Projek.</span><span class="sxs-lookup"><span data-stu-id="11bba-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="11bba-110">Logik perniagaan khusus aplikasi menyalin senarai harga daripada sebut harga kepada kontrak.</span><span class="sxs-lookup"><span data-stu-id="11bba-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="11bba-111">Hasilnya ialah senarai harga projek khusus kontrak.</span><span class="sxs-lookup"><span data-stu-id="11bba-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="11bba-112">Operasi salinan boleh melambatkan proses memenangi sebut harga jika senarai harga projek pada sebut harga terlalu besar.</span><span class="sxs-lookup"><span data-stu-id="11bba-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="11bba-113">Senarai harga produk tidak disalin untuk mencipta senarai harga tersuai pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="11bba-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="11bba-114">Disebabkan tiada salinan yang terlibat, prestasi proses sebut harga tidak terjejas.</span><span class="sxs-lookup"><span data-stu-id="11bba-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]