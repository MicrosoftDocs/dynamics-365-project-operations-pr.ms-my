---
title: Konfigurasi perakaunan untuk projek dalaman
description: Topik ini menyediakan maklumat tentang cara untuk menyediakan amalan perakaunan bagi projek dalaman dalamProject Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857989"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="9642b-103">Konfigurasi perakaunan untuk projek dalaman</span><span class="sxs-lookup"><span data-stu-id="9642b-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="9642b-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="9642b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9642b-105">Projek dalaman membolehkan syarikat menjejak kos yang berkaitan dengan aktiviti yang tidak dibilkan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="9642b-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="9642b-106">Contoh projek dalaman termasuk:</span><span class="sxs-lookup"><span data-stu-id="9642b-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="9642b-107">Membangunkan produk, seperti aplikasi mudah alih dan menjejaki kos yang berkaitan dengan pembangunan.</span><span class="sxs-lookup"><span data-stu-id="9642b-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="9642b-108">Menguruskan masa dan perbelanjaan prajualan.</span><span class="sxs-lookup"><span data-stu-id="9642b-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="9642b-109">Projek dalaman prajualan ini boleh ditukar kemudian kepada projek yang boleh dibilkan jika sebut harga dimenangi.</span><span class="sxs-lookup"><span data-stu-id="9642b-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="9642b-110">Mana-mana projek yang tidak dikaitkan dengan kontrak dalam Dynamics 365 Project Operations dianggap sebagai dalaman.</span><span class="sxs-lookup"><span data-stu-id="9642b-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="9642b-111">Profil kos dan hasil projek tidak digunakan untuk menentukan peraturan perakaunan untuk projek.</span><span class="sxs-lookup"><span data-stu-id="9642b-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="9642b-112">Kos projek dalaman sentiasa disiar menggunakan prinsip keuntungan dan kerugian.</span><span class="sxs-lookup"><span data-stu-id="9642b-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="9642b-113">Akaun lejar untuk siaran ditakrifkan pada halaman **Penyediaan penyiaran lejar**.</span><span class="sxs-lookup"><span data-stu-id="9642b-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="9642b-114">Transaksi masa disiarkan dengan mendebitkan akaun **Kos** dan mengkreditkan akaun **Peruntukan gaji**.</span><span class="sxs-lookup"><span data-stu-id="9642b-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="9642b-115">Transaksi perbelanjaan disiarkan dengan mendebitkan akaun **Kos** dan mengkreditkan **Akaun ofset untuk perbelanjaan**.</span><span class="sxs-lookup"><span data-stu-id="9642b-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="9642b-116">Transaksi item akan disiarkan dengan mendebitkan akaun **Kos** dan mengkreditkan akaun **Kos - Item**.</span><span class="sxs-lookup"><span data-stu-id="9642b-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="9642b-117">Selepas transaksi disiarkan kepada projek, jika projek tersebut dikaitkan dengan kontrak projek, sistem membalikkan semua transaksi terkumpul dan mencipta transaksi boleh dibilkan baharu.</span><span class="sxs-lookup"><span data-stu-id="9642b-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="9642b-118">Transaksi boleh dibilkan mengikut peraturan perakaunan yang ditakrifkan dalam kos Projek dan profil hasil.</span><span class="sxs-lookup"><span data-stu-id="9642b-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
