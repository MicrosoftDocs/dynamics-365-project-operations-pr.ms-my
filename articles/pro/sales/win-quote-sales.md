---
title: Tutup sebut harga
description: Topik ini menyediakan maklumat tentang penutupan sebut harga dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896202"
---
# <a name="close-quotes"></a><span data-ttu-id="3bd80-103">Tutup sebut harga</span><span class="sxs-lookup"><span data-stu-id="3bd80-103">Close quotes</span></span> 

<span data-ttu-id="3bd80-104">_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_</span><span class="sxs-lookup"><span data-stu-id="3bd80-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3bd80-105">Sebut harga projek boleh ditutup sebagai Menang atau Hilang.</span><span class="sxs-lookup"><span data-stu-id="3bd80-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="3bd80-106">Operasi Aktifkan dan Semak Semula pada sebut harga tidak disokong dalam Microsoft Dynamics 365 Project Operations, jadi draf sebut harga boleh ditutup.</span><span class="sxs-lookup"><span data-stu-id="3bd80-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="3bd80-107">Tutup sebut harga sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="3bd80-107">Close a quote as Won</span></span>

<span data-ttu-id="3bd80-108">Menutup sebut harga projek sebagai Menang akan tutup sebut harga dengan status ditetapkan kepada Ditutup dan sebab status ditetapkan kepada Menang.</span><span class="sxs-lookup"><span data-stu-id="3bd80-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="3bd80-109">Menutup sebut harga menjadikan sebut harga projek baca sahaja dan mencipta draf kontrak projek yang mengandungi maklumat sebut harga.</span><span class="sxs-lookup"><span data-stu-id="3bd80-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="3bd80-110">Oleh kerana sebut harga ditutup tidak boleh dibuka semula, dialog pengesahan Terdapat dialog pengesahan sebelum perubahan dilakukan memandangkan sebut harga tidak boleh dibuka semula dan perubahan tidak boleh diubah balik.</span><span class="sxs-lookup"><span data-stu-id="3bd80-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="3bd80-111">Jika sebut harga dilampirkan kepada peluang, sebarang sebut harga projek lain untuk peluang ditutup secara automatik sebagai hilang.</span><span class="sxs-lookup"><span data-stu-id="3bd80-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="3bd80-112">Kesan kewangan untuk menutup sebut harga sebagai Menang</span><span class="sxs-lookup"><span data-stu-id="3bd80-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="3bd80-113">Jika telah ada sebarang masa yang sebenar direkodkan pada projek semasa ia masih dilampirkan pada draf sebut harga, hanya kos masa atau perbelanjaan direkodkan.</span><span class="sxs-lookup"><span data-stu-id="3bd80-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="3bd80-114">Selepas sebut harga ditutup sebagai Menang, aplikasi itu akan faktor semula kos dengan menterbalikkan kos sebenar yang lebih lama dan mencipta semula kos sebenar yang baharu.</span><span class="sxs-lookup"><span data-stu-id="3bd80-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="3bd80-115">Aplikasi akan memproses kos sebenar berdasarkan kepada Kaedah pengebilan bagi baris kontrak projek berkaitan.</span><span class="sxs-lookup"><span data-stu-id="3bd80-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="3bd80-116">Jika kos sebenar merujuk pada masa dan baris kontrak bahan, sistem akan secara automatik akan mencipta jualan sebenar yang belum dibilkan untuk apabila sebut harga ditutup dan kontrak projek dicipta.</span><span class="sxs-lookup"><span data-stu-id="3bd80-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="3bd80-117">Jika kos sebenar merujuk kepada baris kontrak harga tetap, aplikasi akan berhenti untuk memproses semula kos sebenar berdasarkan peraturan pengebilan pecahan untuk pelanggan kontrak projek.</span><span class="sxs-lookup"><span data-stu-id="3bd80-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="3bd80-118">Menutup sebut harga sebagai hilang:</span><span class="sxs-lookup"><span data-stu-id="3bd80-118">Closing a quote as lost:</span></span>

<span data-ttu-id="3bd80-119">Menutup sebut harga projek sebagai Hilang akan menetapkan status sebut harga kepada Tutup dan sebab status kepada Hilang.</span><span class="sxs-lookup"><span data-stu-id="3bd80-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="3bd80-120">Menutup sebut harga menjadikan sebut harga projek baca sahaja.</span><span class="sxs-lookup"><span data-stu-id="3bd80-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="3bd80-121">Oleh kerana sebut harga ditutup tidak boleh dibuka semula dan, sebelum anda tutup sebut harga, dialog pengesahan akan mengesahkan perubahan anda.</span><span class="sxs-lookup"><span data-stu-id="3bd80-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3bd80-122">Jika projek sebut harga yang ditutup sebagai Hilang mempunyai projek yang dirujuk pada sebarang baris, projek tersebut juga ditandakan sebagai Tutup dan sebarang penempahan sumber dari hari ke hadapan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="3bd80-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="3bd80-123">Dalam Project Operations, menutup sebut harga sebagai Menang atau Hilang tidak akan memberi kesan bahawa status Peluang, yang akan kekal terbuka sehingga ia secara manual ditutup.</span><span class="sxs-lookup"><span data-stu-id="3bd80-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
