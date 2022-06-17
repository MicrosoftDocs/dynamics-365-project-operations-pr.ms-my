---
title: Tambah borang entiti tersuai baharu (Project Service Automation 2.x)
description: Artikel ini menyediakan maklumat tentang cara menambah borang entiti tersuai untuk peluang, sebut harga, pesanan atau invois dalam Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922739"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Tambah borang entiti tersuai baharu (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Medan jenis 

Dynamics 365 Project Service Automation bergantung pada **Jenis** medan (**msdyn\_ordertype**) bagi entiti Peluang, Sebut Harga, Pesanan dan Invois untuk membezakan versi **berasaskan kerja** bagi entiti-entiti ini daripada versi **berasaskan item** dan **berasaskan perkhidmatan**. Versi berasaskan kerja bagi entiti-entiti ini diuruskan oleh PSA. Banyak logik perniagaan pada sisi klien dan pelayan bagi penyelesaian bergantung pada medan **Jenis**. Oleh itu, adalah penting bahawa medan diawalkan dengan nilai yang betul apabila entiti dicipta. Nilai yang salah boleh menyebabkan tingkah laku yang salah, dan sesetengah logik perniagaan mungkin tidak berjalan dengan betul.

## <a name="automatic-form-switching"></a>Penukaran borang automatik

Untuk mengelakkan daripada potensi rasuah data dan tingkah laku tidak diduga yang disebabkan oleh pengawalan yang salah dan pengeditan rekod entiti jualan, PSA kini termasuk logik untuk penukaran borang automatik dalam borang siap sedia. Logik ini membawa pengguna kepada borang yang betul untuk berkerja dengan versi berasaskan kerja atau sebarang jenis entiti Peluang, Sebut Harga, Pesanan atau Invois yang lain. Apabila pengguna membuka versi berasaskan kerja untuk entiti Peluang, Sebut Harga, Pesanan atau Invois, borang ditukar kepada **Maklumat Projek**.

Logik penukaran borang automatik bergantung pada pemetaan antara nilai **formid** dan medan **msdyn\_ordertype**. Semua borang siap sedia telah ditambah ke pemetaan tersebut. Walau bagaimanapun, borang tersuai mesti ditambah secara manual untuk menunjukkan versi entiti yang dimaksudkan untuk pengendalian. Ini berdasarkan medan **msdyn\_ordertype**. Jika penukaran borang hilang daripada pemetaan, logik akan bertukar kepada borang siap sedia, berdasarkan nilai yang disimpan dalam medan entiti **msdyn\_ordertype**.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Tambah borang tersuai dan hidupkan logik penukaran borang

Contoh berikut menunjukkan cara untuk menambah borang tersuai, **Maklumat Projek Saya**, supaya ia berfungsi dengan peluang berasaskan kerja. Proses yang sama digunakan untuk menambah borang tersuai supaya ia berfungsi dengan sebut harga, pesanan dan invois.

Ikuti langkah ini untuk mencipta versi tersuai borang **Maklumat Projek**.

1. Dalam entiti Peluang, buka borang **Maklumat Projek** dan simpan salinan di bawah nama **Maklumat Projek Saya**.
2. Buka borang baharu, dan kemudian, dalam sifat, pastikan bahawa skrip permulaan borang daripada borang **Maklumat Projek** wujud. 

    > [!IMPORTANT]
    > Jangan keluarkan skrip. Jika tidak, sesetengah data mungkin dimulakan dengan tidak betul.

3. Sahkan bahawa medan **Jenis** (**msdyn\_ordertype**) hadir dalam borang. 

    > [!IMPORTANT]
    > Jangan keluarkan medan ini. Jika tidak, skrip permulaan akan gagal.

4. Cari nilai **formid** borang baharu. Anda boleh melengkapkan langkah ini dalam dua cara yang berbeza:

    - Eksport borang **Maklumat Projek Saya** sebagai sebahagian daripada penyelesaian tak terurus, dan kemudian lihat nilai **formid** dalam fail penyesuaian.xml daripada penyelesaian yang dieksport.
    - Buka borang **Maklumat Projek Saya** dalam editor borang, dan kemudian cari pengecam unik global (GUID) di sebelah parameter **fromid** dalam URL, seperti ditunjukkan dalam ilustrasi berikut.

    ![Nilai formId bagi borang baharu dalam URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Cipta pemetaan **msdyn\_ordertype** untuk nilai **formid** dengan mengedit sumber web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Alih keluarkan kod daripada sumber dan gantikannya dengan kod berikut.

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

6. Simpan dan kemudian terbitkan penyesuaian.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
