---
title: Baris peluang berdasarkan produk
description: Topik ini memberikan maklumat tentang item baris peluang berdasarkan produk dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896247"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="45c67-103">Baris peluang berdasarkan produk</span><span class="sxs-lookup"><span data-stu-id="45c67-103">Product-based opportunity lines</span></span>

<span data-ttu-id="45c67-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="45c67-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45c67-105">Baris peluang berdasarkan produk ialah item baris pada Peluang.</span><span class="sxs-lookup"><span data-stu-id="45c67-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="45c67-106">Baris ini disampaikan kepada pelanggan sebagai item baris yang berbeza pada invois akhirnya tanpa sebarang perkhidmatan ditambahkan nilai yang lain.</span><span class="sxs-lookup"><span data-stu-id="45c67-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="45c67-107">Perbelanjaan dan penggunaan yang berkaitan tidak dijejak pada tugas bagi sebarang projek yang berkaitan.</span><span class="sxs-lookup"><span data-stu-id="45c67-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="45c67-108">Baris berdasarkan produk boleh menjadi item katalog atau produk masukan manual.</span><span class="sxs-lookup"><span data-stu-id="45c67-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="45c67-109">Kebanyakan kefungsian pada baris berdasarkan produk Peluang mengikut kefungsian yang disediakan oleh aplikasi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="45c67-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="45c67-110">Untuk maklumat lanjut tentang baris peluang berdasarkan produk, lihat [Tambahkan produk pada peluang](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="45c67-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="45c67-111">Satu konsep tentang baris peluang berdasarkan produk yang khusus untuk peluang berdasarkan produk ialah **Belanjawan Pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="45c67-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="45c67-112">Gunakan medan ini untuk menjejaki amaun yang pelanggan sanggup bayar untuk item baris.</span><span class="sxs-lookup"><span data-stu-id="45c67-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="45c67-113">Jika kaedah hasil bagi ringkasan Peluang ditetapkan kepada **Dikira Sistem**, nilai belanjawan pelanggan merentasi baris berdasarkan produk dan projek diringkaskan untuk mengira anggaran hasil.</span><span class="sxs-lookup"><span data-stu-id="45c67-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
