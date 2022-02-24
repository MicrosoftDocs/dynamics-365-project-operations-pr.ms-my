---
title: Bangunkan templat projek dengan Salin Projek
description: Topik ini menyediakan maklumat tentang cara untuk mencipta templat projek menggunakan tindakan tersuai Salin Projek.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045020"
---
# <a name="develop-project-templates-with-copy-project"></a>Bangunkan templat projek dengan Salin Projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations menyokong keupayaan untuk menyalin projek dan mengembalikan sebarang tugasan kembali ke sumber generik yang mewakili peranan. Pelanggan boleh menggunakan kefungsian ini untuk membina templat projek asas.

Apabila anda memilih **Salin Projek**, status projek sasaran akan dikemas kini. Gunakan **Sebab Status** untuk menentukan apabila tindakan salin selesai. Memilih **Salin Projek** juga mengemas kini tarikh mula projek kepada tarikh mula semasa jika tiada tarikh sasaran dikesan dalam entiti projek sasaran.

## <a name="copy-project-custom-action"></a>Tindakan tersuai Salin Projek 

### <a name="name"></a>Nama 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parameter input
Terdapat tiga parameter input:

| Parameter          | Jenis   | Nilai                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Jalur | **{"removeNamedResources":true}** atau **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Rujukan Entiti | Projek Sumber |
| Sasaran             | Rujukan Entiti | Projek Sasaran |


- **{"clearTeamsAndAssignments":true}**: Tingkah laku lalai untuk Projek untuk Web dan akan mengalih keluar semua tugasan dan ahli pasukan.
- **{"removeNamedResources":true}** Tingkah laku lalai untuk Project Operations dan akan menukar tugasan kembali kepada sumber generik.

Untuk mendapatkan lebih banyak lalai pada tindakan, lihat [Gunakan tindakan API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Tentukan medan untuk disalin 
Apabila tindakan dipanggil, **Salin Projek** akan melihat pandangan projek **Lajur Salin Projek** untuk menentukan medan untuk disalin apabila projek dicipta.


### <a name="example"></a>Contoh
Contoh berikut menunjukkan cara untuk memanggil tindakan tersuai **Salin Projek** dengan set parameter **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
