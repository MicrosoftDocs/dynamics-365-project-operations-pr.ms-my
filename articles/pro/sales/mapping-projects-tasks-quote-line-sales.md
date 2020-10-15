---
title: Petakan projek dan tugas kepada baris sebut harga berasaskan projek
description: Topik ini memberikan maklumat mengenai cara untuk memetakan projek dan tugas kepada baris tugas berasaskan projek.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964918"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="9f136-103">Petakan projek dan tugas kepada baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="9f136-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="9f136-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="9f136-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f136-105">Pada baris sebut harga berasaskan projek, anda boleh memetakan tugas khusus projek yang sudah dikaitkan kepada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="9f136-106">Apabila anda memetakan tugas kepada baris sebut harga, item berikut yang anda takrifkan pada baris sebut harga hanya akan digunakan pada tugas tersebut:</span><span class="sxs-lookup"><span data-stu-id="9f136-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="9f136-107">Kaedah pengebilan</span><span class="sxs-lookup"><span data-stu-id="9f136-107">Billing method</span></span>
- <span data-ttu-id="9f136-108">Pilihan boleh dikenakan caj</span><span class="sxs-lookup"><span data-stu-id="9f136-108">Chargeability options</span></span>
- <span data-ttu-id="9f136-109">Had yang tidak melebihi</span><span class="sxs-lookup"><span data-stu-id="9f136-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="9f136-110">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="9f136-110">Customers</span></span>

<span data-ttu-id="9f136-111">Contohnya, anda mungkin mempunyai projek yang satu fasa adalah harga tetap dan semua fasa lain adalah masa dan bahan.</span><span class="sxs-lookup"><span data-stu-id="9f136-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="9f136-112">Dalam kes ini, anda boleh mengaitkan fasa pertama dan semua tugas anak kepada baris sebut harga untuk fasa tersebut dengan kaedah pengebilan harga tetap.</span><span class="sxs-lookup"><span data-stu-id="9f136-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="9f136-113">Anda kemudian boleh mengaitkan semua fasa lain kepada masa dan baris sebut harga berasaskan bahan.</span><span class="sxs-lookup"><span data-stu-id="9f136-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="9f136-114">Kaitkan tugas kepada baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="9f136-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="9f136-115">Anda boleh mengaitkan tugas dengan baris sebut harga daripada lokasi berikut:</span><span class="sxs-lookup"><span data-stu-id="9f136-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="9f136-116">Halaman **Projek** > tab **Pengebilan tugas** (optimum)</span><span class="sxs-lookup"><span data-stu-id="9f136-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="9f136-117">Halaman **Baris Sebut Harga** > tab **Tugas boleh dicaj**</span><span class="sxs-lookup"><span data-stu-id="9f136-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="9f136-118">Daripada halaman Projek</span><span class="sxs-lookup"><span data-stu-id="9f136-118">From the Project page</span></span>

<span data-ttu-id="9f136-119">Halaman **Projek** menyediakan pengalaman optimum untuk mengaitkan tugas kepada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="9f136-120">Anda boleh menggunakan halaman ini untuk memilih berbilang tugas dan mengaitkan semuanya, ditambah dengan tugas anaknya kepada baris sebut harga terpilih.</span><span class="sxs-lookup"><span data-stu-id="9f136-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="9f136-121">Pada tab **Umum** bagi baris sebut harga berasaskan projek, sahkan medan **Projek** telah diisi.</span><span class="sxs-lookup"><span data-stu-id="9f136-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="9f136-122">Dalam medan **Tugas yang disertakan**, pilih **Tugas terpilih sahaja**.</span><span class="sxs-lookup"><span data-stu-id="9f136-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="9f136-123">Simpan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-123">Save the project-based quote line.</span></span> <span data-ttu-id="9f136-124">Apabila borang disegar semula, tab **Tugas boleh dicaj** dipaparkan.</span><span class="sxs-lookup"><span data-stu-id="9f136-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="9f136-125">Pada tab **Umum**, pilih pautan untuk projek daripada medan **Projek**.</span><span class="sxs-lookup"><span data-stu-id="9f136-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="9f136-126">Pada halaman **Projek**, pilih tab **Pengebilan tugas**.</span><span class="sxs-lookup"><span data-stu-id="9f136-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="9f136-127">Dalam grid kedua, yang digunakan kepada persediaan pengebilan berkhususkan tugas, pilih satu atau lebih tugas dan kemudian pilih **Kaitkan baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="9f136-128">Dalam halaman dialog yang muncul, pilih baris sebut harga yang memaparkan baris sebut harga berasaskan projek pada sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="9f136-129">Dalam medan **Jenis pengebilan**, menunjukkan jika tugas ini boleh dikenakan caj atau tidak boleh dikenakan caj.</span><span class="sxs-lookup"><span data-stu-id="9f136-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="9f136-130">Pilih kotak semak untuk menunjukkan jika perkaitan harus memasukkan tugas anak bagi tugas terpilih.</span><span class="sxs-lookup"><span data-stu-id="9f136-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="9f136-131">Menyemak kotak akan mengaitkan tugas anak bagi tugas terpilih kepada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="9f136-132">Pilih **OK** untuk menutup dialog.</span><span class="sxs-lookup"><span data-stu-id="9f136-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="9f136-133">Daripada halaman baris sebut harga</span><span class="sxs-lookup"><span data-stu-id="9f136-133">From the Quote line page</span></span>

<span data-ttu-id="9f136-134">Anda boleh mengaitkan tugas projek kepada baris sebut harga daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="9f136-135">Tempat yang optimum untuk mengaitkan tugas projek kepada baris sebut harga pada tab **Pengebilan tugas** pada halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="9f136-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="9f136-136">Jika anda mengaitkan tugas daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**, anda mesti mengaitkan setiap projek secara manual.</span><span class="sxs-lookup"><span data-stu-id="9f136-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="9f136-137">Pada tab **Umum** bagi baris sebut harga berasaskan projek, sahkan terdapat projek terpilih di dalam medan **Projek**.</span><span class="sxs-lookup"><span data-stu-id="9f136-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="9f136-138">Dalam medan **Tugas yang disertakan**, pilih **Tugas terpilih sahaja**.</span><span class="sxs-lookup"><span data-stu-id="9f136-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="9f136-139">Simpan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-139">Save the project-based quote line.</span></span> <span data-ttu-id="9f136-140">Apabila borang disegar semula, tab **Tugas boleh dicaj** dipaparkan.</span><span class="sxs-lookup"><span data-stu-id="9f136-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="9f136-141">Pada tab **Tugas boleh dicaj**, pilih **Tambah tugas baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="9f136-142">Pada halaman **Tugas baris sebut harga**, di dalam medan **Tugas**, pilih tugas dan di dalam medan **Jenis pengebilan**, pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9f136-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="9f136-143">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="9f136-143">Close the page.</span></span> <span data-ttu-id="9f136-144">Tugas terpilih kini dikaitkan kepada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="9f136-145">Pisahkan tugas kepada baris sebut harga berasaskan projek</span><span class="sxs-lookup"><span data-stu-id="9f136-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="9f136-146">Daripada halaman Projek</span><span class="sxs-lookup"><span data-stu-id="9f136-146">From the Project page</span></span>

<span data-ttu-id="9f136-147">Kaedah ini menyediakan pengalaman paling optimum untuk memisahkan tugas daripada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="9f136-148">Anda boleh memilih berbilang tugas dan memisahkan semuanya, ditambah dengan tugas anaknya daripada baris sebut harga terpilih.</span><span class="sxs-lookup"><span data-stu-id="9f136-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="9f136-149">Pada tab **Umum** bagi baris sebut harga berasaskan projek, di dalam medan **Projek**, pilih pautan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="9f136-150">Pada halaman **Projek**, pilih tab **Pengebilan tugas**.</span><span class="sxs-lookup"><span data-stu-id="9f136-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="9f136-151">Dalam grid kedua, yang digunakan kepada persediaan pengebilan berkhususkan tugas, pilih satu atau lebih tugas dan kemudian pilih **Pisahkan baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="9f136-152">Dalam halaman dialog yang muncul, pilih baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="9f136-153">Pilih kotak semak untuk menunjukkan sama ada hubungan juga harus dialih keluar daripada tugas anak bagi tugas terpilih.</span><span class="sxs-lookup"><span data-stu-id="9f136-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="9f136-154">Menyemak kotak juga akan memisahkan tugas anak bagi tugas terpilih kepada baris sebut harga.</span><span class="sxs-lookup"><span data-stu-id="9f136-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="9f136-155">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f136-155">Select **OK**.</span></span> <span data-ttu-id="9f136-156">Mesej amaran memberitahu anda bahawa jika anda telah mengalih keluar perkaitan ini, sebarang rekod pada tugas sebelum ini boleh diterbalikkan.</span><span class="sxs-lookup"><span data-stu-id="9f136-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="9f136-157">Pilih **OK** untuk meneruskan dan mengalih keluar perkaitan antara tugas dan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="9f136-158">Daripada halaman baris sebut harga</span><span class="sxs-lookup"><span data-stu-id="9f136-158">From the Quote line page</span></span>

<span data-ttu-id="9f136-159">Anda juga boleh memisahkan tugas projek kepada baris sebut harga daripada tab **Tugas boleh dicaj** pada halaman **Baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="9f136-160">Pada tab **Tugas boleh dicaj**, pilih **Padam tugas baris sebut harga**.</span><span class="sxs-lookup"><span data-stu-id="9f136-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="9f136-161">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f136-161">Select **OK**.</span></span> <span data-ttu-id="9f136-162">Mesej amaran memberitahu anda bahawa jika anda telah mengalih keluar perkaitan ini, sebarang rekod pada tugas sebelum ini boleh diterbalikkan.</span><span class="sxs-lookup"><span data-stu-id="9f136-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="9f136-163">Pilih **OK** untuk meneruskan dan mengalih keluar perkaitan antara tugas dan baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="9f136-164">Prosedur ini tidak memadam tugas daripada projek tersebut.</span><span class="sxs-lookup"><span data-stu-id="9f136-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="9f136-165">Ia hanya mengalih keluar perkaitan tugas daripada baris sebut harga berasaskan projek.</span><span class="sxs-lookup"><span data-stu-id="9f136-165">It only removes the task association from the project-based quote line.</span></span>
