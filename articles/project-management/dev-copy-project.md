---
title: Bangunkan templat projek dengan Salin Projek
description: Artikel ini menyediakan maklumat tentang cara untuk mencipta templat projek menggunakan tindakan tersuai Salin Projek.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923843"
---
# <a name="develop-project-templates-with-copy-project"></a>Bangunkan templat projek dengan Salin Projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menyokong keupayaan untuk menyalin projek dan mengembalikan sebarang tugasan kembali ke sumber generik yang mewakili peranan. Pelanggan boleh menggunakan kefungsian ini untuk membina templat projek asas.

Apabila anda memilih **Salin Projek**, status projek sasaran akan dikemas kini. Gunakan **Sebab Status** untuk menentukan apabila tindakan salin selesai. Memilih **Salin Projek** juga mengemas kini tarikh mula projek kepada tarikh mula semasa jika tiada tarikh sasaran dikesan dalam entiti projek sasaran.

## <a name="copy-project-custom-action"></a>Tindakan tersuai Salin Projek

### <a name="name"></a>Nama 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parameter input

Terdapat tiga parameter input:

- **ReplaceNamedResources** atau **ClearTeamsAndAssignments** – Tetapkan hanya salah satu daripada pilihan. Jangan tetapkan kedua-duanya.

    - **\{"ReplaceNamedResources":true\}** – Tingkah laku lalai untuk Project Operations. Mana-mana sumber yang dinamakan digantikan dengan sumber generik.
    - **\{"ClearTeamsAndAssignments":true\}** – Tingkah laku lalai untuk Project for the Web. Semua tugasan dan ahli pasukan dialih keluar.

- **SourceProject** – Rujukan entiti projek sumber untuk disalin. Parameter ini tidak boleh nol.
- **Target** – Rujukan entiti bagi projek sasaran untuk disalin kepadanya. Parameter ini tidak boleh nol.

Jadual berikut memberikan ringkasan tiga parameter tersebut.

| Parameter_                | Taip             | Nilai                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Benar** atau **Palsu** |
| ClearTeamsAndAssignments | Boolean          | **Benar** atau **Palsu** |
| SourceProject            | Rujukan Entiti | Projek sumber    |
| Sasaran                   | Rujukan Entiti | Projek sasaran    |

Untuk mendapatkan lebih banyak lalai pada tindakan, lihat [Gunakan tindakan API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Pensahihan

Pensahihan berikut telah dilakukan.

1. Semakan nol mendapatkan projek sumber dan sasaran untuk mengesahkan kewujudan kedua-dua projek dalam organisasi.
2. Sistem mengesahkan bahawa projek sasaran adalah sah untuk penyalinan dengan mengesahkan syarat berikut:

    - Tiada aktiviti sebelumnya pada projek (termasuk pemilihan tab **Tugas**) dan projek baru dicipta.
    - Tiada salinan sebelumnya, tiada Import telah diminta pada projek ini dan projek tidak mempunyai status **Gagal**.

3. Operasi tidak dipanggil dengan menggunakan HTTP.

## <a name="specify-fields-to-copy"></a>Tentukan medan untuk disalin

Apabila tindakan dipanggil, **Salin Projek** akan melihat pandangan projek **Lajur Salin Projek** untuk menentukan medan untuk disalin apabila projek dicipta.

### <a name="example"></a>Contoh

Contoh berikut menunjukkan cara untuk memanggil tindakan tersuai **CopyProjectV3** dengan set parameter **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
