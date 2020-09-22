---
title: Perkara baharu atau diubah dalam Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753901"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="0a905-103">Perkara baharu atau diubah dalam Project Service Automation versi 3 gelombang 1 2020</span><span class="sxs-lookup"><span data-stu-id="0a905-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="0a905-104">Topik ini menyerlahkan pertimbangan naik taraf utama apabila beralih ke keluaran terkini Project Service Automation (PSA) versi 3.x gelombang 1 2020.</span><span class="sxs-lookup"><span data-stu-id="0a905-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="0a905-105">Entri masa</span><span class="sxs-lookup"><span data-stu-id="0a905-105">Time entry</span></span>
<span data-ttu-id="0a905-106">Pengalaman entri masa telah dilanjutkan untuk menyampaikan keupayaan bagi melanjutkan entri masa ke dalam lebih banyak senario pelanggan.</span><span class="sxs-lookup"><span data-stu-id="0a905-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="0a905-107">Ini termasuk keupayaan untuk menambah jenis entri yang kini mendorong tingkah laku khusus berdasarkan nama skema medan **Tetapan Entri Masa**, dipaparkan sebagai **Sumber Masa**.</span><span class="sxs-lookup"><span data-stu-id="0a905-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="0a905-108">Pertimbangan naik taraf</span><span class="sxs-lookup"><span data-stu-id="0a905-108">Upgrade consideration</span></span>
<span data-ttu-id="0a905-109">Untuk menyokong fungsi ini, peranan dalam PSA telah dikemas kini untuk menyertakan kelayakan baharu.</span><span class="sxs-lookup"><span data-stu-id="0a905-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="0a905-110">Kelayakan ini memberikan akses baca kepada entiti baharu, **Tetapan Entri Masa**.</span><span class="sxs-lookup"><span data-stu-id="0a905-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="0a905-111">Pengguna yang memerlukan keupayaan untuk log masa harus diberikan peranan pengguna **Pengguna Entri Masa** selain peranan yang sedia ada.</span><span class="sxs-lookup"><span data-stu-id="0a905-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="0a905-112">Peranan ini termasuk fungsi baharu dan memastikan entri masa akan terus berfungsi.</span><span class="sxs-lookup"><span data-stu-id="0a905-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="0a905-113">Perubahan entri masa yang dilanjutkan buat masa ini</span><span class="sxs-lookup"><span data-stu-id="0a905-113">Currently extended time entry changes</span></span>
<span data-ttu-id="0a905-114">Untuk meminimumkan kesan kepada pengguna semasa entri masa, perubahan peranan ini adalah satu-satunya keperluan teras yang diperlukan untuk terus menggunakan entri masa.</span><span class="sxs-lookup"><span data-stu-id="0a905-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="0a905-115">Jika anda telah mencipta pandangan tersuai atau pengalaman entri masa yang berasingan, anda mesti menetapkan medan **Tetapan Entri Masa** kepada nilai PSA yang betul.</span><span class="sxs-lookup"><span data-stu-id="0a905-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
