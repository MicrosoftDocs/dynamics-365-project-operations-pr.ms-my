---
title: Selesaikan masalah kerja dalam grid Tugas
description: Topik ini menyediakan maklumat penyelesaian masalah yang diperlukan apabila menggunakan grid Tugas.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213411"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="1a393-103">Selesaikan masalah kerja dalam grid Tugas</span><span class="sxs-lookup"><span data-stu-id="1a393-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="1a393-104">_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_</span><span class="sxs-lookup"><span data-stu-id="1a393-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a393-105">Topik ini menerangkan cara menyelesaikan masalah yang anda mungkin alami ketika menggunakan pengurusan kos.</span><span class="sxs-lookup"><span data-stu-id="1a393-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="1a393-106">Dayakan kuki</span><span class="sxs-lookup"><span data-stu-id="1a393-106">Enable cookies</span></span>

<span data-ttu-id="1a393-107">Project Operations memerlukan kuki pihak ketiga tersebut didayakan bagi memaparkan struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="1a393-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="1a393-108">Apabila kuki pihak ketiga tidak didayakan, anda tidak melihat tugas, tetapi anda akan melihat halaman kosong apabila anda memilih tab **Tugas** pada halaman **Projek**.</span><span class="sxs-lookup"><span data-stu-id="1a393-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tab kosong apabila kuki pihak ketiga tidak didayakan](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="1a393-110">Penyelesaian sementara</span><span class="sxs-lookup"><span data-stu-id="1a393-110">Workaround</span></span>
<span data-ttu-id="1a393-111">Untuk penyemak imbas Microsoft Edge atau Google Chrome, prosedur berikut menggariskan cara mengemas kini tetapan penyemak imbas anda untuk mendayakan kuki pihak ketiga.</span><span class="sxs-lookup"><span data-stu-id="1a393-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="1a393-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a393-112">Microsoft Edge</span></span>

1. <span data-ttu-id="1a393-113">Buka penyemak imbas Microsoft Edge anda.</span><span class="sxs-lookup"><span data-stu-id="1a393-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="1a393-114">Di penjuru sebelah kanan bahagian atas, pilih **elipsis** (...), dan kemudian pilih **Tetapan**.</span><span class="sxs-lookup"><span data-stu-id="1a393-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="1a393-115">Di bawah **Keizinan kuki dan tapak**, pilih **Kuki dan data tapak**.</span><span class="sxs-lookup"><span data-stu-id="1a393-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="1a393-116">Matikan **Sekat kuki pihak ketiga**.</span><span class="sxs-lookup"><span data-stu-id="1a393-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="1a393-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="1a393-117">Google Chrome</span></span>

1. <span data-ttu-id="1a393-118">Buka penyemak imbas Chrome anda.</span><span class="sxs-lookup"><span data-stu-id="1a393-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="1a393-119">Di penjuru sebelah kanan bahagian atas, pilih tiga titik menegak (...), dan kemudian pilih **Tetapan**.</span><span class="sxs-lookup"><span data-stu-id="1a393-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="1a393-120">Di bawah **Privasi dan keselamatan**, pilih **Kuki dan data tapak lain**.</span><span class="sxs-lookup"><span data-stu-id="1a393-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="1a393-121">Pilih **Benarkan semua kuki**.</span><span class="sxs-lookup"><span data-stu-id="1a393-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a393-122">Jika anda menyekat kuki pihak ketiga, semua kuki dan data tapak daripada tapak lain akan disekat, sekalipun tapak itu dibenarkan pada senarai pengecualian anda.</span><span class="sxs-lookup"><span data-stu-id="1a393-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="1a393-123">Titik Tamat PEX</span><span class="sxs-lookup"><span data-stu-id="1a393-123">PEX Endpoint</span></span>

<span data-ttu-id="1a393-124">Project Operations memerlukan parameter projek merujuk Titik Tamat PEX.</span><span class="sxs-lookup"><span data-stu-id="1a393-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="1a393-125">Titik tamat ini diperlukan untuk berkomunikasi dengan perkhidmatan yang digunakan untuk memaparkan struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="1a393-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="1a393-126">Jika parameter tidak didayakan, anda akan menerima ralat, "Parameter projek tidak sah".</span><span class="sxs-lookup"><span data-stu-id="1a393-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="1a393-127">Penyelesaian sementara</span><span class="sxs-lookup"><span data-stu-id="1a393-127">Workaround</span></span>
 ![Medan Titik Tamat PEX pada parameter projek](media/projectparameter.png)

1. <span data-ttu-id="1a393-129">Tambah medan **Titik Tamat PEX** pada halaman **Parameter Projek**.</span><span class="sxs-lookup"><span data-stu-id="1a393-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="1a393-130">Kemas kini medan dengan nilai berikut: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="1a393-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="1a393-131">Alih keluar medan daripada halaman **Parameter Projek**.</span><span class="sxs-lookup"><span data-stu-id="1a393-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="1a393-132">Kelayakan untuk Projek untuk Web</span><span class="sxs-lookup"><span data-stu-id="1a393-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="1a393-133">Project Operations bergantung pada perkhidmatan penjadualan luaran.</span><span class="sxs-lookup"><span data-stu-id="1a393-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="1a393-134">Perkhidmatan memerlukan pengguna mempunyai beberapa peranan ditugaskan untuk membaca dan menulis entiti berkaitan dengan struktur pecahan kerja.</span><span class="sxs-lookup"><span data-stu-id="1a393-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="1a393-135">Entiti ini termasuklah tugas projek, tugasan sumber dan kebersandaran tugas.</span><span class="sxs-lookup"><span data-stu-id="1a393-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="1a393-136">Jika pengguna tidak boleh memaparkan struktur pecahan kerja apabila mereka pergi ke tab **Tugas**, ia mungkin disebabkan Projek untuk Project Operations belum didayakan.</span><span class="sxs-lookup"><span data-stu-id="1a393-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="1a393-137">Pengguna mungkin menerima sama ada ralat peranan keselamatan atau ralat berkaitan dengan penafian akses.</span><span class="sxs-lookup"><span data-stu-id="1a393-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="1a393-138">Penyelesaian sementara</span><span class="sxs-lookup"><span data-stu-id="1a393-138">Workaround</span></span>

1. <span data-ttu-id="1a393-139">Pergi ke **Tetapan > Keselamatan > Pengguna > Pengguna Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="1a393-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Pembaca aplikasi](media/applicationuser.jpg)
   
2. <span data-ttu-id="1a393-141">Klik dua kali rekod pengguna aplikasi untuk mengesahkan perkara berikut:</span><span class="sxs-lookup"><span data-stu-id="1a393-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="1a393-142">Pengguna mempunyai capaian kepada projek.</span><span class="sxs-lookup"><span data-stu-id="1a393-142">The user has access to the project.</span></span> <span data-ttu-id="1a393-143">Pengesahan ini lazimnya dilakukan bagi memastikan pengguna mempunyai peranan keselamatan **Pengurus Projek**.</span><span class="sxs-lookup"><span data-stu-id="1a393-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="1a393-144">Pengguna aplikasi Microsoft Project wujud dan dikonfigurasikan dengan betul.</span><span class="sxs-lookup"><span data-stu-id="1a393-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="1a393-145">Jika pengguna ini tidak wujud, anda boleh mencipta rekod pengguna baharu.</span><span class="sxs-lookup"><span data-stu-id="1a393-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="1a393-146">Pilih **Pengguna Baharu**.</span><span class="sxs-lookup"><span data-stu-id="1a393-146">Select **New Users**.</span></span> <span data-ttu-id="1a393-147">Ubah borang entri kepada **Pengguna Aplikasi**, dan kemudian tambah **ID Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="1a393-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Butiran pengguna aplikasi](media/applicationuserdetails.jpg)

4. <span data-ttu-id="1a393-149">Sahkan bahawa pengguna telah ditugaskan lesen yang betul dan perkhidmatan didayakan dalam rancangan perkhidmatan untuk butiran lesen.</span><span class="sxs-lookup"><span data-stu-id="1a393-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="1a393-150">Sahkan bahawa pengguna boleh membuka project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1a393-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="1a393-151">Sahkan melalui parameter projek bahawa sistem sedang menghala kepada titik tamat projek yang betul.</span><span class="sxs-lookup"><span data-stu-id="1a393-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="1a393-152">Sahkan bahawa pengguna aplikasi projek dicipta.</span><span class="sxs-lookup"><span data-stu-id="1a393-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="1a393-153">Gunakan peranan keselamatan berikut kepada pengguna:</span><span class="sxs-lookup"><span data-stu-id="1a393-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="1a393-154">Pengguna Dataverse</span><span class="sxs-lookup"><span data-stu-id="1a393-154">Dataverse User</span></span>
  - <span data-ttu-id="1a393-155">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="1a393-155">Project Operations System</span></span>
  - <span data-ttu-id="1a393-156">Sistem Projek</span><span class="sxs-lookup"><span data-stu-id="1a393-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="1a393-157">Ralat semasa mengemas kini struktur pecahan kerja</span><span class="sxs-lookup"><span data-stu-id="1a393-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="1a393-158">Apabila satu atau lebih kemas kini dibuat kepada struktur pecahan kerja, perubahan akhirnya gagal dan tidak disimpan.</span><span class="sxs-lookup"><span data-stu-id="1a393-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="1a393-159">Ralat berlaku dalam grid jadual dan mencatatkan bahawa "Perubahan terkini yang anda buat tidak dapat disimpan."</span><span class="sxs-lookup"><span data-stu-id="1a393-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="1a393-160">Penyelesaian sementara</span><span class="sxs-lookup"><span data-stu-id="1a393-160">Workaround</span></span>

1. <span data-ttu-id="1a393-161">Sahkan bahawa pengguna telah ditugaskan lesen yang betul dan perkhidmatan didayakan dalam rancangan perkhidmatan untuk butiran lesen.</span><span class="sxs-lookup"><span data-stu-id="1a393-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="1a393-162">Sahkan bahawa pengguna boleh membuka project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1a393-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="1a393-163">Sahkan bahawa sistem sedang menghala kepada titik tamat projek yang betul.</span><span class="sxs-lookup"><span data-stu-id="1a393-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="1a393-164">Sahkan bahawa pengguna Aplikasi Projek telah dicipta.</span><span class="sxs-lookup"><span data-stu-id="1a393-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="1a393-165">Gunakan peranan keselamatan berikut kepada pengguna:</span><span class="sxs-lookup"><span data-stu-id="1a393-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="1a393-166">Pengguna Dataverse atau pengguna Pangkalan</span><span class="sxs-lookup"><span data-stu-id="1a393-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="1a393-167">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="1a393-167">Project Operations System</span></span>
  - <span data-ttu-id="1a393-168">Sistem Projek</span><span class="sxs-lookup"><span data-stu-id="1a393-168">Project System</span></span>
  - <span data-ttu-id="1a393-169">Sistem Dwitulis Project Operations (Peranan ini diperlukan jika anda menggunakan senario berdasarkan sumber/bukan stok bagi Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="1a393-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
