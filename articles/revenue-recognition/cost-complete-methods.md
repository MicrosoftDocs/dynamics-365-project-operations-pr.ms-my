---
title: Kos untuk melengkapkan kaedah
description: Topik ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279059"
---
# <a name="cost-to-complete-methods"></a><span data-ttu-id="b7ee1-103">Kos untuk melengkapkan kaedah</span><span class="sxs-lookup"><span data-stu-id="b7ee1-103">Cost to complete methods</span></span>

<span data-ttu-id="b7ee1-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="b7ee1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b7ee1-105">Topik ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-105">This topic provides information about the methods used to calculate the cost to complete a project.</span></span> <span data-ttu-id="b7ee1-106">Terdapat berbilang kaedah yang boleh anda gunakan untuk mengira kos untuk melengkapkan projek.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-106">There are multiple methods you can use to calculate the cost to complete a project.</span></span> 

<span data-ttu-id="b7ee1-107">Apabila anda mencipta anggaran untuk projek, pada halaman **Cipta anggaran**, dalam medan **Kos untuk melengkapkan kaedah**, anda boleh memilih salah satu daripada kos berikut untuk melengkapkan kaedah.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-107">When you create an estimate for a project, on the **Create estimate** page, in the **Cost to complete method** field, you can select one of the following cost to complete methods.</span></span>

| <span data-ttu-id="b7ee1-108">Kos untuk melengkapkan kaedah</span><span class="sxs-lookup"><span data-stu-id="b7ee1-108">Cost to complete method</span></span>    | <span data-ttu-id="b7ee1-109">Penerangan </span><span class="sxs-lookup"><span data-stu-id="b7ee1-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ee1-110">Jumlah kos sebenar</span><span class="sxs-lookup"><span data-stu-id="b7ee1-110">Total cost-actual</span></span>            | <span data-ttu-id="b7ee1-111">Masukkan kos anggaran secara manual dalam medan **Jumlah kos** atau **Jumlah kuantiti** menggunakan butang **Anggaran kos** pada **Halaman anggaran**.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-111">Enter estimate costs manually in the **Total cost** or **Total quantity** fields using the **Cost estimate** button on the **Estimate page**.</span></span> <span data-ttu-id="b7ee1-112">Sistem menolak kos sebenar daripada jumlah yang anda masukkan.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-112">The system subtracts the actual costs from the totals you entered.</span></span> <span data-ttu-id="b7ee1-113">Jumlah ini merupakan kos untuk melengkapkan projek.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-113">The total is the cost to complete the project.</span></span> <span data-ttu-id="b7ee1-114">Kaedah ini tidak menggunakan anggaran perbelanjaan dan penugasan sumber yang dimasukkan dalam Project Operations dibina dalam Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-114">This method doesn't use the expense estimates and resources assignments entered in Project Operations built within Microsoft Dataverse.</span></span> <span data-ttu-id="b7ee1-115">Jumlah kos atau jumlah kuantiti boleh dikemas kini secara manual seperti yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-115">The total cost or total quantity can be updated manually as needed.</span></span>  |
| <span data-ttu-id="b7ee1-116">Jumlah ramalan sebenar</span><span class="sxs-lookup"><span data-stu-id="b7ee1-116">Total forecast-actual</span></span>        | <span data-ttu-id="b7ee1-117">Penugasan sumber dan anggaran perbelanjaan digunakan untuk menentukan jumlah amaun ramalan projek.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-117">Resource assignments and expense estimates are used to determine the total project forecast amount.</span></span> <span data-ttu-id="b7ee1-118">Kos sebenar dibandingkan dengan ramalan ini untuk mengira kos untuk dilengkapkan.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-118">Actual costs are compared against this forecast to calculate the cost to complete.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b7ee1-119">Seperti anggaran sebelumnya</span><span class="sxs-lookup"><span data-stu-id="b7ee1-119">As previous estimate</span></span>         | <span data-ttu-id="b7ee1-120">Kaedah anggaran sama yang digunakan dalam tempoh sebelumnya digunakan di sini.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-120">The same estimate methods that was used in the previous period is used here.</span></span> <span data-ttu-id="b7ee1-121">Kaedah ini memerlukan model ramalan jika tempoh sebelumnya memerlukan model ramalan.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-121">This method requires a forecast model if the previous period required a forecast model.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b7ee1-122">Tetapkan kos untuk selesaikan kepada sifar</span><span class="sxs-lookup"><span data-stu-id="b7ee1-122">Set cost to complete to zero</span></span> | <span data-ttu-id="b7ee1-123">Lazimnya digunakan sebelum projek anggaran disingkirkan, kaedah ini sepadan dengan jumlah anggaran dengan transaksi sebenar yang disiarkan dan membersihkan lajur **Kos untuk melengkapkan**.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-123">Typically used before the estimate project is eliminated, this method matches total estimates with posted actual transactions and clears the **Cost to complete** column.</span></span> <span data-ttu-id="b7ee1-124">Apabila selesai, hasilnya sentiasa 100 peratus.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-124">When complete, the result is always 100 percent.</span></span> <span data-ttu-id="b7ee1-125">Untuk setiap baris kos yang anda cipta, kotak semak **Ramalan** telah dikosongkan dan jumlah anggaran disalin daripada anggaran kos sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-125">For each cost line that you create, the **Forecasting** check box is cleared and the total estimate is copied from the previous cost estimate.</span></span> <span data-ttu-id="b7ee1-126">Penggunaan sebenar bagi tempoh anggaran ditolak daripada kos untuk selesaikan projek.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-126">The actual consumption for the estimate period is deducted from the cost to complete the project.</span></span>              |
| <span data-ttu-id="b7ee1-127">Daripada templat kos</span><span class="sxs-lookup"><span data-stu-id="b7ee1-127">From cost template</span></span>           | <span data-ttu-id="b7ee1-128">Kos untuk melengkapkan kaedah yang disediakan dalam templat kos yang berkaitan dengan projek anggaran yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="b7ee1-128">The cost to complete method that is set up in the cost template that's associated with the selected estimate project.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]