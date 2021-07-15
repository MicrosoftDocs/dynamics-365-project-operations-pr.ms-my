---
title: Halaman utama pelaporan
description: Topik ini memberikan maklumat tentang pelaporan dalam Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 03/01/2019
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
ms.openlocfilehash: b074f1a1dd45cb66f57c68b4b7f9df64250dcee4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368757"
---
# <a name="reporting-home-page"></a><span data-ttu-id="5d874-103">Melaporkan laman utama</span><span class="sxs-lookup"><span data-stu-id="5d874-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5d874-104">Microsoft Dynamics 365 Project Service Automation membolehkan organisasi berasaskan projek menguruskan operasi perniagaan mereka dengan cekap.</span><span class="sxs-lookup"><span data-stu-id="5d874-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="5d874-105">Pada sebarang projek, ahli pasukan mesti menguruskan peluang, sebut harga dan merancang kerja, memberikan sumber kepada projek, menguruskan kerja mengikut pelan, bil untuk kerja dan kemudian melakukan kerja untuk menyelesaikan projek.</span><span class="sxs-lookup"><span data-stu-id="5d874-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="5d874-106">Keupayaan untuk melaporkan operasi adalah kunci untuk menentukan kesihatan organisasi dan mengambil sebarang tindakan pembetulan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="5d874-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="5d874-107">PSA menggunakan kaedah pelaporan dan teknologi Microsoft Dynamics 365 untuk semua pelaporannya.</span><span class="sxs-lookup"><span data-stu-id="5d874-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="5d874-108">Untuk mendapatkan maklumat lanjut tentang pilihan bagi pelaporan, lihat [Panduan penulisan laporan untuk Dynamics 365 Customer Engagement (on-premises), versi 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="5d874-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="5d874-109">Wizard Laporan</span><span class="sxs-lookup"><span data-stu-id="5d874-109">Report Wizard</span></span>

<span data-ttu-id="5d874-110">Wizard Laporan membolehkan bukan pembangun mencipta laporan ringkas.</span><span class="sxs-lookup"><span data-stu-id="5d874-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="5d874-111">Oleh sebab aplikasi ini dibina pada platform sedia ada, pengalaman adalah sama dengan pengalaman yang didokumenkan dalam [Cipta atau edit laporan menggunakan Wizard Laporan](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="5d874-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="5d874-112">Walau bagaimanapun, anda akan menggunakan entiti khusus Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5d874-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="5d874-113">Laporan SQL Server Reporting Services tersuai</span><span class="sxs-lookup"><span data-stu-id="5d874-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="5d874-114">Jika perniagaan anda memerlukan laporan khusus yang tidak boleh dicipta dengan menggunakan Wizard Laporan, anda boleh mencipta laporan tersuai.</span><span class="sxs-lookup"><span data-stu-id="5d874-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="5d874-115">Anda mesti memasang Microsoft Visual Studio bersama-sama dengan Microsoft SQL Server Data Tools dan Sambungan Pengarangan Laporan yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="5d874-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="5d874-116">Untuk mendapatkan maklumat lanjut tentang alat dan versi, lihat [Persekitaran penulisan laporan menggunakan SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="5d874-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="5d874-117">Untuk mendapatkan maklumat tentang cara untuk mencipta laporan tersuai, lihat [Cipta laporan baharu menggunakan SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="5d874-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="5d874-118">Aplikasi Insights Power BI</span><span class="sxs-lookup"><span data-stu-id="5d874-118">Power BI insights apps</span></span>

<span data-ttu-id="5d874-119">Bersama-sama, Microsoft Power BI dan Dynamics 365 memberikan anda cara yang hebat untuk bekerja dengan data anda, dalam bentuk aplikasi Insights.</span><span class="sxs-lookup"><span data-stu-id="5d874-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="5d874-120">Untuk mendapatkan maklumat tentang ketersediaan aplikasi Insights, lihat [Halaman aplikasi Insights Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="5d874-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5d874-121">Sumber tambahan</span><span class="sxs-lookup"><span data-stu-id="5d874-121">Additional resources</span></span>
<span data-ttu-id="5d874-122">Untuk mendapatkan maklumat lanjut tentang pelaporan dalam PSA, lihat topik berikut:</span><span class="sxs-lookup"><span data-stu-id="5d874-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="5d874-123">Bekerja dengan model data Project Service</span><span class="sxs-lookup"><span data-stu-id="5d874-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="5d874-124">Papan Pemuka</span><span class="sxs-lookup"><span data-stu-id="5d874-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]