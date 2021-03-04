---
title: Tutup sebut harga - ringkas
description: Topik ini menyediakan maklumat tentang penutupan sebut harga dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764875"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="40a9d-103">Tutup sebut harga - ringkas</span><span class="sxs-lookup"><span data-stu-id="40a9d-103">Close a quote - lite</span></span>

<span data-ttu-id="40a9d-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="40a9d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40a9d-105">Sebut harga projek boleh ditutup sebagai Menang atau Hilang.</span><span class="sxs-lookup"><span data-stu-id="40a9d-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="40a9d-106">Sebut harga draf boleh ditutup kerana operasi Aktifkan dan Semak Semula pada sebut harga tidak disokong dalam Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="40a9d-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="40a9d-107">Tutup sebut harga sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="40a9d-107">Close a quote as Won</span></span>

<span data-ttu-id="40a9d-108">Apabila anda menutup sebut harga projek sebagai Dimenangi, status ditetapkan ke Ditutup dan sebab status ialah Dimenangi.</span><span class="sxs-lookup"><span data-stu-id="40a9d-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="40a9d-109">Menutup sebut harga menjadikan sebut harga projek baca sahaja dan mencipta draf kontrak projek yang mengandungi maklumat sebut harga.</span><span class="sxs-lookup"><span data-stu-id="40a9d-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="40a9d-110">Oleh kerana sebut harga yang ditutup tidak boleh dibuka semula, dialog pengesahan akan mengesahkan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="40a9d-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="40a9d-111">Jika sebut harga dilampirkan kepada peluang, sebarang sebut harga projek lain untuk peluang ditutup secara automatik sebagai hilang.</span><span class="sxs-lookup"><span data-stu-id="40a9d-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="40a9d-112">Kesan kewangan untuk menutup sebut harga sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="40a9d-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="40a9d-113">Jika terdapat mana-mana aktual untuk masa pada projek semasa masih dilampirkan ke draf sebut harga, hanya kos masa atau perbelanjaan direkodkan.</span><span class="sxs-lookup"><span data-stu-id="40a9d-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="40a9d-114">Selepas sebut harga ditutup sebagai Menang, aplikasi itu akan faktor semula kos dengan menterbalikkan kos sebenar yang lebih lama dan mencipta semula kos sebenar yang baharu.</span><span class="sxs-lookup"><span data-stu-id="40a9d-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="40a9d-115">Aplikasi akan memproses kos sebenar berdasarkan kepada Kaedah pengebilan bagi baris kontrak projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="40a9d-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="40a9d-116">Jika kos aktual merujuk kepada masa dan baris kontrak bahan, aktual jualan yang belum dibil berkaitan akan dicipta untuk apabila sebut harga ditutup dan kontrak projek dicipta.</span><span class="sxs-lookup"><span data-stu-id="40a9d-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="40a9d-117">Jika aktual kos merujuk kepada baris kontrak harga tetap, permohonan akan berhenti memproses semula aktual kos yang berdasarkan pada pecahan peraturan pengebilan untuk pelanggan kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="40a9d-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="40a9d-118">Menutup sebut harga sebagai hilang:</span><span class="sxs-lookup"><span data-stu-id="40a9d-118">Closing a quote as lost:</span></span>

<span data-ttu-id="40a9d-119">Apabila anda menutup sebut harga projek sebagai Kalah, status ditetapkan ke Ditutup dan sebab status ialah Kalah.</span><span class="sxs-lookup"><span data-stu-id="40a9d-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="40a9d-120">Menutup sebut harga menjadikan sebut harga projek baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="40a9d-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="40a9d-121">Oleh kerana sebut harga ditutup tidak boleh dibuka semula dan, sebelum anda tutup sebut harga, dialog pengesahan akan mengesahkan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="40a9d-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="40a9d-122">Jika sebut harga projek ditutup sebagai Kalah merujuk kepada projek pada salah satu baris, projek itu juga ditandakan sebagai Ditutup.</span><span class="sxs-lookup"><span data-stu-id="40a9d-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="40a9d-123">Sebarang tempahan sumber dari hari tersebut ke hadapan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="40a9d-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="40a9d-124">Dalam Project Operations, menutup sebut harga sebagai Menang atau Hilang tidak akan memberi kesan bahawa status Peluang, yang akan kekal terbuka sehingga ia secara manual ditutup.</span><span class="sxs-lookup"><span data-stu-id="40a9d-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
