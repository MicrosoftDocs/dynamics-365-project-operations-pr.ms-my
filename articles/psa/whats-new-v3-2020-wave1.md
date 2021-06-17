---
title: Perkara baharu atau diubah dalam Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996847"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="63774-103">Perkara baharu atau diubah dalam Project Service Automation versi 3 gelombang 1 2020</span><span class="sxs-lookup"><span data-stu-id="63774-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="63774-104">Topik ini menyerlahkan pertimbangan naik taraf utama apabila beralih ke keluaran terkini Project Service Automation (PSA) versi 3.x gelombang 1 2020.</span><span class="sxs-lookup"><span data-stu-id="63774-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="63774-105">Entri masa</span><span class="sxs-lookup"><span data-stu-id="63774-105">Time entry</span></span>
<span data-ttu-id="63774-106">Pengalaman entri masa telah dilanjutkan untuk menyampaikan keupayaan bagi melanjutkan entri masa ke dalam lebih banyak senario pelanggan.</span><span class="sxs-lookup"><span data-stu-id="63774-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="63774-107">Ini termasuk keupayaan untuk menambah jenis entri yang kini mendorong tingkah laku khusus berdasarkan nama skema medan **Tetapan Entri Masa**, dipaparkan sebagai **Sumber Masa**.</span><span class="sxs-lookup"><span data-stu-id="63774-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="63774-108">Penyelesaian baharu, yang dipanggil Masa, Perbelanjaan, Penstatusan dan Kelulusan (TESA) telah ditambah untuk menyokong fungsi ini.</span><span class="sxs-lookup"><span data-stu-id="63774-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="63774-109">Pertimbangan naik taraf</span><span class="sxs-lookup"><span data-stu-id="63774-109">Upgrade consideration</span></span>
<span data-ttu-id="63774-110">Untuk menyokong fungsi ini, peranan dalam PSA telah dikemas kini untuk menyertakan kelayakan baharu.</span><span class="sxs-lookup"><span data-stu-id="63774-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="63774-111">Kelayakan ini memberikan akses baca kepada entiti baharu, **Tetapan Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="63774-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="63774-112">Pengguna yang memerlukan keupayaan untuk log masa harus diberikan peranan pengguna **Pengguna Entri Masa** selain peranan yang sedia ada.</span><span class="sxs-lookup"><span data-stu-id="63774-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="63774-113">Peranan ini termasuk fungsi baharu dan memastikan entri masa akan terus berfungsi.</span><span class="sxs-lookup"><span data-stu-id="63774-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="63774-114">Selain itu, jika anda mempunyai sebarang modul aplikasi tersuai yang termasuk semua borang untuk entiti kemasukan masa, anda akan dikehendaki untuk mengalih keluar **Borang Cipta Cepat Entri TESA** dari modul.</span><span class="sxs-lookup"><span data-stu-id="63774-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="63774-115">Perubahan entri masa yang dilanjutkan buat masa ini</span><span class="sxs-lookup"><span data-stu-id="63774-115">Currently extended time entry changes</span></span>
<span data-ttu-id="63774-116">Untuk meminimumkan kesan kepada pengguna semasa entri masa, perubahan peranan ini adalah satu-satunya keperluan teras yang diperlukan untuk terus menggunakan entri masa.</span><span class="sxs-lookup"><span data-stu-id="63774-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="63774-117">Jika anda telah mencipta pandangan tersuai atau pengalaman entri masa yang berasingan, anda mesti menetapkan medan **Tetapan Entri Masa** kepada nilai PSA yang betul.</span><span class="sxs-lookup"><span data-stu-id="63774-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]