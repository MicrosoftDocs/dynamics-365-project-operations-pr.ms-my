---
title: Pembelian bahan bukan stok menggunakan invois vendor yang belum selesai
description: Topik ini menerangkan cara untuk merekodkan invois vendor yang belum selesai.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993815"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="904c2-103">Pembelian bahan bukan stok menggunakan invois vendor yang belum selesai</span><span class="sxs-lookup"><span data-stu-id="904c2-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="904c2-104">_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_</span><span class="sxs-lookup"><span data-stu-id="904c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="904c2-105">Oleh kerana syarikat memperoleh bahan bukan ada stok untuk projek, kos boleh direkod dengan segera berbanding projek itu.</span><span class="sxs-lookup"><span data-stu-id="904c2-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="904c2-106">Contohnya, Contoso Robotics US melaksanakan projek pembaharuan peralatan dan memerlukan lesen perisian.</span><span class="sxs-lookup"><span data-stu-id="904c2-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="904c2-107">Lesen ini diperoleh daripada vendor pihak ketiga.</span><span class="sxs-lookup"><span data-stu-id="904c2-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="904c2-108">Menggunakan Dynamics 365 Finance, kerani Akaun belum bayar merekodkan dokumen invois yang belum selesai dan mengatributkan kos lesen secara langsung terhadap projek pembaharuan peralatan.</span><span class="sxs-lookup"><span data-stu-id="904c2-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="904c2-109">Sebelum anda menggunakan kefungsian yang diterangkan dalam topik ini, semak dan gunakan konfigurasi yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="904c2-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="904c2-110">Untuk maklumat lanjut, lihat [Dayakan bahan bukan stok dan invois vendor yang belum selesai](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="904c2-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="904c2-111">Siarkan invois vendor berkaitan projek yang belum selesai</span><span class="sxs-lookup"><span data-stu-id="904c2-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="904c2-112">Invois vendor yang belum selesai boleh direkodkan pada halaman **Invois vendor yang belum selesai** (**Akaun belum bayar** > **Invois** > **Invois vendor yang belum selesai**).</span><span class="sxs-lookup"><span data-stu-id="904c2-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="904c2-113">Lengkapkan langkah berikut untuk menyiarkan invois vendor yang berkaitan dengan projek:</span><span class="sxs-lookup"><span data-stu-id="904c2-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="904c2-114">Pergi ke **Akaun belum bayar** > **Invois** dan pilih **Baharu**.</span><span class="sxs-lookup"><span data-stu-id="904c2-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="904c2-115">Dalam medan **Akaun invois**, pilih vendor dan dalam medan **Nombor**, masukkan pengenalan invois vendor.</span><span class="sxs-lookup"><span data-stu-id="904c2-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="904c2-116">Tambah baris ke invois vendor dan dalam medan **Nombor item**, pilih item bukan stok yang dibeli daripada vendor.</span><span class="sxs-lookup"><span data-stu-id="904c2-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="904c2-117">Baris invois vendor yang berdasarkan pada kategori perolehan tidak boleh direkodkan terhadap projek.</span><span class="sxs-lookup"><span data-stu-id="904c2-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="904c2-118">Tambah kuantiti yang dibeli.</span><span class="sxs-lookup"><span data-stu-id="904c2-118">Add the quantity purchased.</span></span> <span data-ttu-id="904c2-119">Sistem akan mengisi harga unit berdasarkan pada konfigurasi harga item bukan stok.</span><span class="sxs-lookup"><span data-stu-id="904c2-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="904c2-120">Sahkan jumlah amaun dan butiran lain yang diperlukan pada baris.</span><span class="sxs-lookup"><span data-stu-id="904c2-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="904c2-121">Pada butiran baris, pada tab **Projek**, pilih ID projek yang akan merekodkan item.</span><span class="sxs-lookup"><span data-stu-id="904c2-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="904c2-122">Secara pilihan, pilih nombor aktiviti dan kemas kini kategori projek dan sifat baris.</span><span class="sxs-lookup"><span data-stu-id="904c2-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="904c2-123">Siarkan invois vendor yang belum selesai.</span><span class="sxs-lookup"><span data-stu-id="904c2-123">Post pending vendor invoice.</span></span> <span data-ttu-id="904c2-124">Apabila invois disiarkan, sistem merekodkan:</span><span class="sxs-lookup"><span data-stu-id="904c2-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="904c2-125">Amaun baki vendor.</span><span class="sxs-lookup"><span data-stu-id="904c2-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="904c2-126">Amaun cukai jualan.</span><span class="sxs-lookup"><span data-stu-id="904c2-126">The sales tax amount.</span></span>
    - <span data-ttu-id="904c2-127">Kos daripada projek itu direkodkan dalam akaun integrasi perolehan.</span><span class="sxs-lookup"><span data-stu-id="904c2-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="904c2-128">Transaksi sebenar projek dalam Dataverse.</span><span class="sxs-lookup"><span data-stu-id="904c2-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="904c2-129">Transaksi ini akan diproses lebih lanjut menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="904c2-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="904c2-130">Penyiaran jurnal ini memindahkan amaun daripada akaun integrasi perolehan ke akaun kos projek.</span><span class="sxs-lookup"><span data-stu-id="904c2-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
