---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 20, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147124"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="c5b44-103">Project Service Automation Keluaran Kemas kini 20, V3</span><span class="sxs-lookup"><span data-stu-id="c5b44-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c5b44-104">Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c5b44-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c5b44-105">Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan.</span><span class="sxs-lookup"><span data-stu-id="c5b44-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c5b44-106">Keluaran ini serasi dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c5b44-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c5b44-107">Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini.</span><span class="sxs-lookup"><span data-stu-id="c5b44-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c5b44-108">Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c5b44-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c5b44-109">Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 20.</span><span class="sxs-lookup"><span data-stu-id="c5b44-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="c5b44-110">Versi ini mempunyai nombor binaan V 3.10.31.37 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.</span><span class="sxs-lookup"><span data-stu-id="c5b44-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="c5b44-111">Keluaran Kemas kini 20</span><span class="sxs-lookup"><span data-stu-id="c5b44-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c5b44-112">Pembetulan pepijat</span><span class="sxs-lookup"><span data-stu-id="c5b44-112">Bug fixes</span></span>

<span data-ttu-id="c5b44-113">**Pengurusan Projek**</span><span class="sxs-lookup"><span data-stu-id="c5b44-113">**Project Management**</span></span>

<span data-ttu-id="c5b44-114">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="c5b44-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c5b44-115">Mengimport ahli pasukan projek dengan kaedah peruntukan yang memerlukan masa untuk mendapatkan mesej ralat yang tidak jelas apabila masa yang ditentukan adalah sifar.</span><span class="sxs-lookup"><span data-stu-id="c5b44-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="c5b44-116">Pengguna menerima ralat yang salah apabila bilangan maksimum aksara telah dimasukkan ke dalam medan **Perihalan** untuk tugas projek.</span><span class="sxs-lookup"><span data-stu-id="c5b44-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="c5b44-117">**Muat turun pasang masuk Microsoft Dynamics 365 Project Service Automation** diarahkan semula ke halaman muat turun Bahasa Inggeris apabila tetapan bahasa pengguna ditetapkan kepada Bahasa Jepun.</span><span class="sxs-lookup"><span data-stu-id="c5b44-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="c5b44-118">Apabila ralat pelayan berlaku, label penyegerakan pada tab **Jadual** bagi borang **Projek** kadangkala kekal.</span><span class="sxs-lookup"><span data-stu-id="c5b44-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="c5b44-119">Kemas kini tugas berlebihan dihantar kepada pelayan apabila tugas diubah suai.</span><span class="sxs-lookup"><span data-stu-id="c5b44-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="c5b44-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c5b44-120">**Sales**</span></span>

<span data-ttu-id="c5b44-121">Isu berikut telah dibaiki:</span><span class="sxs-lookup"><span data-stu-id="c5b44-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="c5b44-122">Pada borang **Kontrak**, klik dua kali  **Cipta invois** mencipta dua invois untuk rekod aktual tunggal.</span><span class="sxs-lookup"><span data-stu-id="c5b44-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="c5b44-123">Dalam Internet Explorer 11, pengguna tidak dapat mencipta entri perbelanjaan.</span><span class="sxs-lookup"><span data-stu-id="c5b44-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="c5b44-124">Pembalikan Kos dan pembalikan Jualan yang Tidak Dibilkan adalah tidak berkaitan.</span><span class="sxs-lookup"><span data-stu-id="c5b44-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="c5b44-125">Butang **Segar semula Aktual** pada borang **Projek** tidak menyegarkan semula **Tugas Masa Sebenar**.</span><span class="sxs-lookup"><span data-stu-id="c5b44-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="c5b44-126">Pasang masuk **Plug-in PreValidateProjectTeamMemberCreate** boleh mencipta sumber boleh ditempah generik pendua apabila atribut **msdyn_isgenericresourceprojectscoped** ditetapkan kepada **Palsu**.</span><span class="sxs-lookup"><span data-stu-id="c5b44-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="c5b44-127">**Mengira semula** kos boleh dituntut butiran baris sebut harga berdasarkan produk dan butiran baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="c5b44-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="c5b44-128">Dalam senario tertentu, pasang masuk **PostEstimateLineUpdate** memaparkan ralat teferi pengecualian yang tidak sah.</span><span class="sxs-lookup"><span data-stu-id="c5b44-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="c5b44-129">Tempoh masa fasa pada **Carta Analisis Keuntungan** tidak padan dengan tempoh kos dalam garis sebut harga tetap baris butiran sebut harga.</span><span class="sxs-lookup"><span data-stu-id="c5b44-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="c5b44-130">Unit dan unit nilai kumpulan tidak lalai dengan betul untuk kategori perbelanjaan pada **Butiran Baris Kontrak** dan borang **Butiran Baris Sebut Harga**.</span><span class="sxs-lookup"><span data-stu-id="c5b44-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="c5b44-131">Senarai permit **Harga Kos Organisasi Unit** bertindih pada tarikh penguatkuasaan.</span><span class="sxs-lookup"><span data-stu-id="c5b44-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="c5b44-132">Pengguna tidak dibenarkan untuk mengubah **OrgUnit** apabila jenis pesanan tidak berasaskan kerja kerana ia akan membawa kepada ralat pengecualian rujukan yang tidak sah.</span><span class="sxs-lookup"><span data-stu-id="c5b44-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="c5b44-133">Apabila cuba untuk menavigasi dari borang **Butiran Baris Sebut Harga**, kembali ke tab **Sebut Harga**, borang menyegar semula dan memaparkan tab **Ringkasan**.</span><span class="sxs-lookup"><span data-stu-id="c5b44-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
