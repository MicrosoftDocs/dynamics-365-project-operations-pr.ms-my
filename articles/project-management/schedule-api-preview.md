---
title: Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan
description: Artikel ini menyediakan maklumat dan sampel untuk menggunakan API jadual Projek.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541136"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Gunakan API jadual Projek untuk melaksanakan operasi dengan entiti Penjadualan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_


**Entiti penjadualan**

API jadual Projek memberikan keupayaan untuk melaksanakan operasi cipta, kemas kini dan padam dengan **Entiti penjadualan**. Entiti ini diuruskan melalui enjin Penjadualan dalam Projek untuk web. Operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan** telah dihadkan dalam keluaran Dynamics 365 Project Operations sebelum ini.

Jadual berikut memberikan senarai lengkap entiti jadual Projek.

| **Nama entiti**         | **Nama logik entiti**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tugas Projek            | msdyn_projecttask           |
| Kebergantungan Tugas Projek | msdyn_projecttaskdependency |
| Tugasan Sumber     | msdyn_resourceassignment    |
| Baldi Projek          | msdyn_projectbucket         |
| Ahli Pasukan Projek     | msdyn_projectteam           |
| Senarai Semak Projek      | msdyn_projectchecklist      |
| Label Projek           | msdyn_projectlabel          |
| Tugas Projek untuk Dilabelkan   | msdyn_projecttasktolabel    |
| Lelaran Projek          | msdyn_projectsprint         |

**OperationSet**

OperationSet ialah corak unit kerja yang boleh digunakan apabila beberapa jadual yang mempengaruhi permintaan mesti diproses dalam transaksi.

**API jadual Projek**

Berikut ialah senarai API jadual Projek semasa.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | API ini digunakan untuk mencipta projek. Baldi projek dan lalai dibuat serta-merta.                         |
| **msdyn_CreateTeamMemberV1**            | API ini digunakan untuk mencipta ahli pasukan projek. Rekod ahli pasukan dicipta dengan serta-merta.                                  |
| **msdyn_CreateOperationSetV1**          | API ini digunakan untuk menjadualkan beberapa permintaan yang mesti dilakukan dalam transaksi.                                        |
| **msdyn_PssCreateV1**                   | API ini digunakan untuk mencipta entiti. Entiti boleh menjadi sebarang entiti penjadualan Projek yang menyokong operasi cipta. |
| **msdyn_PssUpdateV1**                   | API ini digunakan untuk mengemas kini entiti. Entiti boleh menjadi mana-mana entiti penjadual Projek yang menyokong operasi kemas kini  |
| **msdyn_PssDeleteV1**                   | API ini digunakan untuk memadam entiti. Entiti boleh menjadi sebarang entiti penjadualan Projek yang menyokong operasi padam. |
| **msdyn_ExecuteOperationSetV1**         | API ini digunakan untuk melaksanakan semua operasi dalam set operasi yang diberikan.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | API ini digunakan untuk mengemas kini kontur kerja tugasan sumber yang dirancang.                                                        |



**Menggunakan API jadual Projek dengan OperationSet**

Kerana rekod dengan kedua-dua **CreateProjectV1** dan **CreateTeamMemberV1** dicipta dengan serta-merta, API ini tidak boleh digunakan dalam **OperationSet** secara langsung. Walau bagaimanapun, anda boleh menggunakan API untuk mencipta rekod yang diperlukan, cipta **OperationSet** dan kemudian gunakan rekod yang dipracipta dalam **OperationSet**.

**Operasi yang disokong**

| **Entiti penjadualan**   | **Cipta** | **Kemas kini** | **Delete** | **Pertimbangan penting**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tugas projek            | Ya        | Ya        | Ya        | Medan **Progress**, **EffortCompleted** dan **EffortRemaining** boleh diedit dalam Project for the Web, tetapi ia tidak boleh diedit dalam Operasi Projek.                                                                                                                                                                                             |
| Pergantungan tugas projek | Ya        | No         | Ya        | Rekod pergantungan tugas projek tidak dikemas kini. Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta.                                                                                                                                                                                                                                 |
| Penugasan sumber     | Ya        | Ya\*      | Ya        | Operasi dengan medan berikut tidak disokong: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** dan **PlannedWork**. Rekod penugasan sumber tidak dikemas kini. Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta. API berasingan telah disediakan untuk mengemas kini kontur Tugasan Sumber. |
| Baldi projek          | Ya        | Ya        | Ya        | Baldi lalai dicipta menggunakan **API CreateProjectV1**. Sokongan untuk mencipta dan memadam baldi projek telah ditambah dalam Kemas Kini Keluaran 16.                                                                                                                                                                                                   |
| Ahli pasukan projek     | Ya        | Ya        | Ya        | Untuk mencipta operasi, gunakan API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ya        | Ya        |            | Operasi dengan medan berikut tidak disokong: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** dan **Duration**.                                                                                       |
| Senarai Semak Projek      | Ya        | Ya        | Ya        |                                                                                                                                                                                                                                                                                                                                                         |
| Label Projek           | No         | Ya        | No         | Nama label boleh diubah. Ciri ini hanya tersedia untuk Project for the Web                                                                                                                                                                                                                                                                      |
| Tugas Projek untuk Dilabelkan   | Ya        | No         | Ya        | Ciri ini hanya tersedia untuk Project for the Web                                                                                                                                                                                                                                                                                                  |
| Lelaran Projek          | Ya        | Ya        | Ya        | Medan **Mula** mesti mempunyai tarikh yang lebih awal daripada **medan Selesai**. Sprint untuk projek yang sama tidak boleh bertindih antara satu sama lain. Ciri ini hanya tersedia untuk Project for the Web                                                                                                                                                                    |




Sifat ID adalah pilihan. Jika ia disediakan, sistem cuba untuk menggunakannya dan memberikan pengecualian jika ia tidak boleh digunakan. Jika ia tidak disediakan, sistem akan menjananya.

**Pengehadan dan isu yang diketahui**

Berikut ialah senarai pengehadan dan isu yang diketahui:

-   API Jadual Projek hanya boleh digunakan oleh **Pengguna dengan Lesen** Microsoft Project. Ia tidak boleh digunakan oleh:
    -   Pengguna aplikasi
    -   Pengguna sistem
    -   Pengguna integrasi
    -   Pengguna lain yang tidak mempunyai lesen yang diperlukan
-   Setiap **OperationSet** hanya boleh mempunyai maksimum 100 operasi.
-   Setiap pengguna hanya boleh mempunyai maksimum 10 **OperationSet** terbuka.
-   Project Operations menyokong jumlah maksimum 500 tugas pada sesuatu projek pada masa ini.
-   Setiap Operasi Kontur Tugasan Sumber Kemas Kini dikira sebagai satu operasi.
-   Setiap senarai kontur yang dikemas kini boleh mengandungi maksimum 100 keping masa.
-   Status kegagalan **OperationSet** dan log kegagalan tidak tersedia pada masa ini.
-   Terdapat maksimum 400 pecut bagi setiap projek.
-   [Had dan sempadan pada projek dan tugas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Label kini hanya tersedia untuk Project for web.

**Pengendalian ralat**

-   Untuk menyemak ralat yang dijana daripada Set Operasi, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Set Operasi**.
-   Untuk menyemak ralat yang dijana daripada Perkhidmatan jadual Projek, pergi ke **Tetapan** \> **Integrasi Jadual** \> **Log Ralat PSS**.

**Mengedit Kontur Tugasan Sumber**

Tidak seperti semua API penjadualan projek lain yang mengemas kini entiti, API kontur tugasan sumber bertanggungjawab sepenuhnya untuk kemas kini ke satu medan, msdyn_plannedwork, pada satu entiti, msydn_resourceassignment.

Mod jadual yang diberikan ialah:

-   **unit tetap**
-   Kalendar projek ialah 9-5p ialah 9-5pst, Mon, Tue, Thurs, Jumaat (TIADA KERJA RABUS)
-   Dan kalendar sumber ialah 9-1p PST Isnin hingga Jumaat

Tugasan ini adalah selama seminggu, empat jam sehari. Ini kerana kalendar sumber adalah dari 9-1 PST, atau empat jam sehari.

| &nbsp;     | Tugas | Tarikh Mula | Tarikh Tamat  | Kuantiti | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pekerja |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Sebagai contoh, jika anda mahu pekerja hanya bekerja tiga jam setiap hari minggu ini dan membenarkan satu jam untuk tugas lain.

#### <a name="updatedcontours-sample-payload"></a>Muatan sampel UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Ini ialah tugasan selepas API Jadual Kontur Kemas Kini dijalankan.

| &nbsp;     | Tugas | Tarikh Mula | Tarikh Tamat  | Kuantiti | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pekerja | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Senario sampel**

Dalam senario ini, anda akan mencipta projek, ahli pasukan, empat tugas dan dua penugasan sumber. Seterusnya, anda akan mengemas kini satu tugas, mengemas kini projek, memadamkan satu tugas, memadamkan satu penugasan sumber dan mencipta pergantungan tugas.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

** Sampel tambahan

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
   
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
