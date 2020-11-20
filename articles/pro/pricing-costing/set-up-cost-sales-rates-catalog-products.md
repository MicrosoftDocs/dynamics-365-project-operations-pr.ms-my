---
title: Sediakan kadar kos dan jualan untuk produk katalog - ringan
description: Topik ini memberikan maklumat tentang cara menetapkan kadar kos dan jualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176712"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="a37cc-103">Sediakan kadar kos dan jualan untuk produk katalog - ringan</span><span class="sxs-lookup"><span data-stu-id="a37cc-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="a37cc-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="a37cc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a37cc-105">Menyediakan penetapan harga untuk item katalog produk dalam Dynamics 365 Project Operations adalah sama seperti dalam Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a37cc-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="a37cc-106">Oleh kerana produk tidak dapat dianggarkan atau digunakan pada projek dalam Operasi Projek, jadi tidak perlu menetapkan harga katalog produk pada senarai harga projek untuk sebut harga dan kontrak.</span><span class="sxs-lookup"><span data-stu-id="a37cc-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="a37cc-107">Harga katalog produk perlu disediakan dalam medan **Harga Produk** bagi sebut harga, kontrak atau akaun.</span><span class="sxs-lookup"><span data-stu-id="a37cc-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="a37cc-108">Jangan sediakan harga katalog produk dalam senarai harga projek untuk entiti ini.</span><span class="sxs-lookup"><span data-stu-id="a37cc-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="a37cc-109">Senarai harga projek adalah eksklusif untuk Operasi Projek.</span><span class="sxs-lookup"><span data-stu-id="a37cc-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="a37cc-110">Terdapat logik perniagaan khusus aplikasi yang menyalin senarai harga daripada sebut harga kepada kontrak.</span><span class="sxs-lookup"><span data-stu-id="a37cc-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="a37cc-111">Hasilnya ialah senarai harga projek khusus kontrak.</span><span class="sxs-lookup"><span data-stu-id="a37cc-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="a37cc-112">Operasi salinan boleh melambatkan proses memenangi sebut harga jika senarai harga projek pada sebut harga terlalu besar.</span><span class="sxs-lookup"><span data-stu-id="a37cc-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="a37cc-113">Senarai harga produk tidak disalin untuk mencipta senarai harga tersuai pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="a37cc-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="a37cc-114">Ini bermaksud bahawa senarai harga produk tidak akan memberi kesan pada prestasi proses memenangi sebut harga.</span><span class="sxs-lookup"><span data-stu-id="a37cc-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
