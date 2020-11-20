---
title: Bagaimanakah saya menyesuaikan aliran proses perniagaan Project Stages?
description: Gambaran keseluruhan tentang cara menyesuaikan aliran proses perniagaan Peringkat Projek.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125054"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="078dc-103">Bagaimanakah saya menyesuaikan aliran proses perniagaan Project Stages?</span><span class="sxs-lookup"><span data-stu-id="078dc-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="078dc-104">Terdapat pengehadan yang diketahui dalam versi awal aplikasi Project Service yang nama peringkat dalam aliran proses perniagaan Project Stages mesti betul-betul sepadan dengan nama Bahasa Inggeris yang dijangka (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="078dc-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="078dc-105">Jika tidak, logik perniagaan, yang bergantung pada nama peringkat bahasa Inggeris, tidak berfungsi seperti yang diharapkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="078dc-106">Itulah sebabnya anda tidak melihat tindakan biasa seperti **Tukar Proses** atau **Edit Proses** tersedia pada borang projek dan menyesuaikan aliran proses perniagaan adalah tidak digalakkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="078dc-107">Had ini telah ditangani dalam versi 2.4.5.48 dan kemudian.</span><span class="sxs-lookup"><span data-stu-id="078dc-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="078dc-108">Artikel ini menyediakan penyelesaian sementara yang dicadangkan jika anda perlu menyesuaikan aliran proses perniagaan lalai untuk versi terdahulu.</span><span class="sxs-lookup"><span data-stu-id="078dc-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="078dc-109">Logik perniagaan memerlukan padanan yang tepat dengan nama Bahasa Inggeris peringkat.</span><span class="sxs-lookup"><span data-stu-id="078dc-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="078dc-110">Aliran proses perniagaan Project Stages termasuk logik perniagaan yang mendorong tingkah laku yang berikut dalam aplikasi:</span><span class="sxs-lookup"><span data-stu-id="078dc-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="078dc-111">Apabila projek dikaitkan dengan sebut harga, kod ini menetapkan aliran proses perniagaan kepada peringkat **Quote**.</span><span class="sxs-lookup"><span data-stu-id="078dc-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="078dc-112">Apabila projek dikaitkan dengan kontrak, kod ini menetapkan aliran proses perniagaan kepada peringkat **Plan**.</span><span class="sxs-lookup"><span data-stu-id="078dc-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="078dc-113">Apabila aliran proses perniagaan maju ke peringkat **Close**, rekod projek dinyahaktifkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="078dc-114">Apabila projek dinyahaktifkan, borang projek dan struktur pecahan kerja (WBS) ditetapkan kepada baca sahaja, tempahan sumber yang dinamakan dikeluarkan dan sebarang senarai harga yang berkaitan dinyahaktifkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="078dc-115">Logik perniagaan ini bergantung pada nama Bahasa Inggeris untuk peringkat projek.</span><span class="sxs-lookup"><span data-stu-id="078dc-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="078dc-116">Pergantungan pada nama Bahasa Inggeris peringkat ini adalah sebab utama penyesuaian aliran proses perniagaan Project Stages tidak digalakkan, serta sebab anda tidak dapat melihat tindakan aliran proses perniagaan biasa seperti **Tukar Proses** atau **Edit Proses** pada entiti projek.</span><span class="sxs-lookup"><span data-stu-id="078dc-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="078dc-117">Apakah yang akan berlaku jika nama peringkat tidak sepadan dengan nama Bahasa Inggeris?</span><span class="sxs-lookup"><span data-stu-id="078dc-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="078dc-118">Dalam aplikasi Project Service versi 1.x pada platform 8.2, apabila nama peringkat dalam aliran proses perniagaan tidak sepadan dengan tepat dengan nama Bahasa Inggeris, logik perniagaan yang menetapkan peringkat yang betul untuk sebut harga atau kontrak atau yang menutup projek itu telah dilangkau.</span><span class="sxs-lookup"><span data-stu-id="078dc-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="078dc-119">Tiada mesej ralat dipaparkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-119">No error messages are displayed.</span></span> <span data-ttu-id="078dc-120">Oleh itu, nampaknya anda dapat menyesuaikan aliran proses perniagaan Project Stages.</span><span class="sxs-lookup"><span data-stu-id="078dc-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="078dc-121">Walau bagaimanapun, anda tidak akan melihat sebarang proses automatik berfungsi untuk sebut harga, kontrak dan tutup projek.</span><span class="sxs-lookup"><span data-stu-id="078dc-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="078dc-122">Dalam versi aplikasi Project Service 2.4.4.30 atau lebih awal pada platform 9.0, terdapat perubahan seni bina yang ketara kepada aliran proses perniagaan yang memerlukan logik perniagaan aliran proses perniagaan ditulis semula.</span><span class="sxs-lookup"><span data-stu-id="078dc-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="078dc-123">Akibatnya, jika nama peringkat proses tidak sepadan dengan nama Bahasa Inggeris yang dijangkakan, anda akan menerima mesej ralat.</span><span class="sxs-lookup"><span data-stu-id="078dc-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="078dc-124">Oleh itu, jika anda mahu untuk menyesuaikan aliran proses perniagaan Project Stages bagi entiti projek, anda hanya boleh menambah peringkat baru kepada aliran proses perniagaan lalai bagi entiti projek, sambil mengekalkan peringkat **Quote**, **Plan** dan **Close** seadanya.</span><span class="sxs-lookup"><span data-stu-id="078dc-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="078dc-125">Pengehadan ini memastikan yang anda tidak mendapat ralat daripada logik perniagaan yang menjangkakan nama Bahasa Inggeris peringkat dalam aliran proses perniagaan.</span><span class="sxs-lookup"><span data-stu-id="078dc-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="078dc-126">Dalam versi 2.4.5.48 atau kemudian, logik perniagaan yang diterangkan dalam artikel ini telah dikeluarkan dari aliran proses perniagaan lalai bagi entiti projek.</span><span class="sxs-lookup"><span data-stu-id="078dc-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="078dc-127">Menaik taraf kepada versi itu atau kemudian akan membolehkan anda menyesuaikan atau menggantikan aliran proses perniagaan lalai dengan salah satu daripada aliran proses perniagaan anda sendiri.</span><span class="sxs-lookup"><span data-stu-id="078dc-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="078dc-128">Penyelesaian untuk versi lebih awal</span><span class="sxs-lookup"><span data-stu-id="078dc-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="078dc-129">Jika menaik taraf bukan satu pilihan, anda boleh menyesuaikan aliran proses perniagaan Project Stages bagi entiti projek dalam satu daripada dua cara ini:</span><span class="sxs-lookup"><span data-stu-id="078dc-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="078dc-130">Tambah peringkat tambahan kepada konfigurasi lalai, sementara mengekalkan nama Bahasa Inggeris peringkat untuk **Quote**, **Plan** dan **Close**.</span><span class="sxs-lookup"><span data-stu-id="078dc-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Tangkap layar bagi penambahan peringkat kepada konfigurasi lalai](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="078dc-132">Cipta aliran proses perniagaan anda sendiri dan jadikannya aliran proses perniagaan utama bagi entiti projek yang membolehkan anda mempunyai sebarang nama peringkat yang anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="078dc-133">Walau bagaimanapun, jika anda mahu menggunakan standard peringkat projek **Quote**, **Plan** dan **Close** yang sama, anda perlu melakukan beberapa penyesuaian yang memaksa keluar nama peringkat tersuai anda.</span><span class="sxs-lookup"><span data-stu-id="078dc-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="078dc-134">Logik yang lebih kompleks adalah dalam penutupan projek, yang anda masih boleh cetuskan dengan hanya menyahaktifkan rekod projek.</span><span class="sxs-lookup"><span data-stu-id="078dc-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Penyesuaian BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="078dc-136">Pertimbangan tambahan bagi aplikasi Project Service versi 2.4.4.30 atau lebih awal pada platform 9.0</span><span class="sxs-lookup"><span data-stu-id="078dc-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="078dc-137">Dalam Project Service 2.4.4.30 atau lebih awal pada platform 9.0, dengan aliran proses perniagaan tersuai, medan **Nama Peringkat** pada entiti projek yang digunakan dalam carta **Projek Mengikut Peringkat** dan pandangan senarai projek tidak akan kemas kini, kerana ia digandingkan kepada aliran proses perniagaan Project Stages lalai.</span><span class="sxs-lookup"><span data-stu-id="078dc-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="078dc-138">Anda boleh mengemukakan isu ini dengan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="078dc-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="078dc-139">Tambah medan tersuai untuk merekodkan peringkat aliran proses perniagaan semasa yang dikemas kini apabila pengguna maju menerusi aliran proses perniagaan tersuai.</span><span class="sxs-lookup"><span data-stu-id="078dc-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="078dc-140">Ubah suai carta **Projek Mengikut Peringkat** untuk berfungsi dengan medan tersuai anda dan bukannya konfigurasi lalai.</span><span class="sxs-lookup"><span data-stu-id="078dc-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="078dc-141">Langkah-langkah untuk mencipta aliran proses perniagaan anda sendiri bagi entiti projek</span><span class="sxs-lookup"><span data-stu-id="078dc-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="078dc-142">Untuk mencipta aliran proses perniagaan anda sendiri bagi entiti projek, lakukan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="078dc-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="078dc-143">Pergi ke **Tetapan** > **Pusat Proses**.</span><span class="sxs-lookup"><span data-stu-id="078dc-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="078dc-144">Jangan menyalin aliran proses perniagaan Project Stages kerana itu turut menyalin logik perniagaan Project Service.</span><span class="sxs-lookup"><span data-stu-id="078dc-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Cipta proses](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="078dc-146">Gunakan Pereka Proses untuk mencipta nama peringkat yang anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="078dc-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="078dc-147">Jika anda mahu fungsi yang sama sebagai peringkat lalai untuk **Quote**, **Plan** dan **Close**, anda perlu mencipta fungsi itu berdasarkan nama peringkat aliran proses perniagaan tersuai anda.</span><span class="sxs-lookup"><span data-stu-id="078dc-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Tangkap layar Pereka Proses yang digunakan untuk menyesuaikan BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="078dc-149">Dalam Pereka Proses, klik **Aliran Proses Pesanan** untuk menjadikan aliran proses perniagaan tersuai sebagai aliran proses perniagaan utama bagi entiti projek dengan memindahkannya di atas aliran proses perniagaan Project Stages ke bahagian atas senarai.</span><span class="sxs-lookup"><span data-stu-id="078dc-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="078dc-150">Tangkap layar penggunaan Aliran Proses Pesanan</span><span class="sxs-lookup"><span data-stu-id="078dc-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="078dc-151">Langkah-langkah berikut digunakan pada aplikasi Project Service 2.4.4.30 atau lebih awal pada platform 9.0</span><span class="sxs-lookup"><span data-stu-id="078dc-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="078dc-152">Tambah medan tersuai baru kepada entiti projek untuk merekodkan peringkat tersuai dalam aliran proses perniagaan tersuai anda.</span><span class="sxs-lookup"><span data-stu-id="078dc-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="078dc-153">Anda perlu menambah logik perniagaan (plugin/aliran kerja) untuk mengemas kini medan ini apabila peringkat pada aliran proses perniagaan tersuai dikemas kini.</span><span class="sxs-lookup"><span data-stu-id="078dc-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Tangkap layar penyesuaian Entiti projek](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="078dc-155">Ubah suai carta **Projek Mengikut Peringkat** untuk menggunakan medan tersuai baru anda bagi peringkat.</span><span class="sxs-lookup"><span data-stu-id="078dc-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Tangkap layar penggunaan carta Projek Mengikut Peringkat](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="078dc-157">Ubah suai sebarang pandangan bagi entiti projek untuk memasukkan medan tersuai baru anda bagi peringkat.</span><span class="sxs-lookup"><span data-stu-id="078dc-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Tangkap layar pengubahsuaian pandangan pada Entiti projek](media/FAQ-Customize-BPF-8-720.png)

