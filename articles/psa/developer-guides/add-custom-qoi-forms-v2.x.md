---
title: Tambah borang entiti tersuai baharu (Project Service Automation 2.x)
description: Topik ini memberikan maklumat tentng cara untuk menambah borang entiti tersuai untuk peluang, sebut harga, pesanan atau invois dalam Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144604"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="162ac-103">Tambah borang entiti tersuai baharu (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="162ac-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="162ac-104">Medan jenis</span><span class="sxs-lookup"><span data-stu-id="162ac-104">Type field</span></span> 

<span data-ttu-id="162ac-105">Dynamics 365 Project Service Automation bergantung pada **Jenis** medan (**msdyn\_ordertype**) bagi entiti Peluang, Sebut Harga, Pesanan dan Invois untuk membezakan versi **berasaskan kerja** bagi entiti-entiti ini daripada versi **berasaskan item** dan **berasaskan perkhidmatan**.</span><span class="sxs-lookup"><span data-stu-id="162ac-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="162ac-106">Versi berasaskan kerja bagi entiti-entiti ini diuruskan oleh PSA.</span><span class="sxs-lookup"><span data-stu-id="162ac-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="162ac-107">Banyak logik perniagaan pada sisi klien dan pelayan bagi penyelesaian bergantung pada medan **Jenis**.</span><span class="sxs-lookup"><span data-stu-id="162ac-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="162ac-108">Oleh itu, adalah penting bahawa medan diawalkan dengan nilai yang betul apabila entiti dicipta.</span><span class="sxs-lookup"><span data-stu-id="162ac-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="162ac-109">Nilai yang salah boleh menyebabkan tingkah laku yang salah, dan sesetengah logik perniagaan mungkin tidak berjalan dengan betul.</span><span class="sxs-lookup"><span data-stu-id="162ac-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="162ac-110">Penukaran borang automatik</span><span class="sxs-lookup"><span data-stu-id="162ac-110">Automatic form switching</span></span>

<span data-ttu-id="162ac-111">Untuk mengelakkan daripada potensi rasuah data dan tingkah laku tidak diduga yang disebabkan oleh pengawalan yang salah dan pengeditan rekod entiti jualan, PSA kini termasuk logik untuk penukaran borang automatik dalam borang siap sedia.</span><span class="sxs-lookup"><span data-stu-id="162ac-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="162ac-112">Logik ini membawa pengguna kepada borang yang betul untuk berkerja dengan versi berasaskan kerja atau sebarang jenis entiti Peluang, Sebut Harga, Pesanan atau Invois yang lain.</span><span class="sxs-lookup"><span data-stu-id="162ac-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="162ac-113">Apabila pengguna membuka versi berasaskan kerja untuk entiti Peluang, Sebut Harga, Pesanan atau Invois, borang ditukar kepada **Maklumat Projek**.</span><span class="sxs-lookup"><span data-stu-id="162ac-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="162ac-114">Logik penukaran borang automatik bergantung pada pemetaan antara nilai **formid** dan medan **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="162ac-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="162ac-115">Semua borang siap sedia telah ditambah ke pemetaan tersebut.</span><span class="sxs-lookup"><span data-stu-id="162ac-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="162ac-116">Walau bagaimanapun, borang tersuai mesti ditambah secara manual untuk menunjukkan versi entiti yang dimaksudkan untuk pengendalian.</span><span class="sxs-lookup"><span data-stu-id="162ac-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="162ac-117">Ini berdasarkan medan **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="162ac-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="162ac-118">Jika penukaran borang hilang daripada pemetaan, logik akan bertukar kepada borang siap sedia, berdasarkan nilai yang disimpan dalam medan entiti **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="162ac-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="162ac-119">Tambah borang tersuai dan hidupkan logik penukaran borang</span><span class="sxs-lookup"><span data-stu-id="162ac-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="162ac-120">Contoh berikut menunjukkan cara untuk menambah borang tersuai, **Maklumat Projek Saya**, supaya ia berfungsi dengan peluang berasaskan kerja.</span><span class="sxs-lookup"><span data-stu-id="162ac-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="162ac-121">Proses yang sama digunakan untuk menambah borang tersuai supaya ia berfungsi dengan sebut harga, pesanan dan invois.</span><span class="sxs-lookup"><span data-stu-id="162ac-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="162ac-122">Ikuti langkah ini untuk mencipta versi tersuai borang **Maklumat Projek**.</span><span class="sxs-lookup"><span data-stu-id="162ac-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="162ac-123">Dalam entiti Peluang, buka borang **Maklumat Projek** dan simpan salinan di bawah nama **Maklumat Projek Saya**.</span><span class="sxs-lookup"><span data-stu-id="162ac-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="162ac-124">Buka borang baharu, dan kemudian, dalam sifat, pastikan bahawa skrip permulaan borang daripada borang **Maklumat Projek** wujud.</span><span class="sxs-lookup"><span data-stu-id="162ac-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="162ac-125">Jangan keluarkan skrip.</span><span class="sxs-lookup"><span data-stu-id="162ac-125">Don't remove the scripts.</span></span> <span data-ttu-id="162ac-126">Jika tidak, sesetengah data mungkin dimulakan dengan tidak betul.</span><span class="sxs-lookup"><span data-stu-id="162ac-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="162ac-127">Sahkan bahawa medan **Jenis** (**msdyn\_ordertype**) hadir dalam borang.</span><span class="sxs-lookup"><span data-stu-id="162ac-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="162ac-128">Jangan keluarkan medan ini.</span><span class="sxs-lookup"><span data-stu-id="162ac-128">Don't remove this field.</span></span> <span data-ttu-id="162ac-129">Jika tidak, skrip permulaan akan gagal.</span><span class="sxs-lookup"><span data-stu-id="162ac-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="162ac-130">Cari nilai **formid** borang baharu.</span><span class="sxs-lookup"><span data-stu-id="162ac-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="162ac-131">Anda boleh melengkapkan langkah ini dalam dua cara yang berbeza:</span><span class="sxs-lookup"><span data-stu-id="162ac-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="162ac-132">Eksport borang **Maklumat Projek Saya** sebagai sebahagian daripada penyelesaian tak terurus, dan kemudian lihat nilai **formid** dalam fail penyesuaian.xml daripada penyelesaian yang dieksport.</span><span class="sxs-lookup"><span data-stu-id="162ac-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="162ac-133">Buka borang **Maklumat Projek Saya** dalam editor borang, dan kemudian cari pengecam unik global (GUID) di sebelah parameter **fromid** dalam URL, seperti ditunjukkan dalam ilustrasi berikut.</span><span class="sxs-lookup"><span data-stu-id="162ac-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Nilai formId bagi borang baharu dalam URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="162ac-135">Cipta pemetaan **msdyn\_ordertype** untuk nilai **formid** dengan mengedit sumber web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="162ac-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="162ac-136">Alih keluarkan kod daripada sumber dan gantikannya dengan kod berikut.</span><span class="sxs-lookup"><span data-stu-id="162ac-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="162ac-137">Simpan dan kemudian terbitkan penyesuaian.</span><span class="sxs-lookup"><span data-stu-id="162ac-137">Save and then publish the customizations.</span></span>
