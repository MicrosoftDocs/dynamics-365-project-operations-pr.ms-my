---
title: Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan
description: Topik ini menyediakan maklumat dan sampel untuk menggunakan API Jadual.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116808"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Gunakan API jadual untuk melaksanakan operasi dengan entiti Penjadualan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

> [!IMPORTANT] 
> Sesetengah atau semua kefungsian yang dinyatakan dalam topik ini tersedia sebagai sebahagian daripada keluaran pratonton. Kandungan dan fungsi adalah tertakluk kepada perubahan. 

## <a name="scheduling-entities"></a>Entiti penjadualan

Api Jadual menyediakan keupayaan untuk melaksanakan operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan**. Entiti ini diuruskan melalui enjin Penjadualan dalam Projek untuk web. Operasi mencipta, mengemas kini dan memadam dengan **Entiti penjadualan** telah dihadkan dalam keluaran Dynamics 365 Project Operations sebelum ini.

Jadual berikut menyediakan senarai lengkap **Entiti penjadualan**.

| Nama entiti  | Nama logik entiti |
| --- | --- |
| Project | msdyn_project |
| Tugas Projek  | msdyn_projecttask  |
| Kebergantungan Tugas Projek  | msdyn_projecttaskdependency  |
| Tugasan Sumber | msdyn_resourceassignment |
| Baldi Projek  | msdyn_projectbucket |
| Ahli Pasukan Projek | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet ialah corak unit kerja yang boleh digunakan apabila beberapa jadual yang mempengaruhi permintaan mesti diproses dalam transaksi.

## <a name="schedule-apis"></a>API Jadual

Berikut ialah senarai API Jadual semasa.

- **msdyn_CreateProjectV1**: API ini boleh digunakan untuk mencipta projek. Projek dan baldi projek lalai dicipta dengan serta-merta.
- **msdyn_CreateTeamMemberV1**: API ini boleh digunakan untuk mencipta ahli pasukan projek. Rekod ahli pasukan dicipta dengan serta-merta.
- **msdyn_CreateOperationSetV1**: API ini boleh digunakan untuk menjadualkan beberapa permintaan yang mesti dilaksanakan dalam transaksi.
- **msdyn_PSSCreateV1**: API ini boleh digunakan untuk mencipta entiti. Entiti boleh jadi sebarang entiti Penjadualan yang menyokong penciptaan operasi.
- **msdyn_PSSUpdateV1**: API ini boleh digunakan untuk mengemas kini entiti. Entiti boleh jadi sebarang entiti Penjadualan yang menyokong kemas kini operasi.
- **msdyn_PSSDeleteV1**: API ini boleh digunakan untuk memadamkan entiti. Entiti boleh jadi sebarang entiti Penjadualan yang menyokong pemadaman operasi.
- **msdyn_ExecuteOperationSetV1**: API ini digunakan untuk melaksanakan semua operasi dalam set operasi yang diberikan.

## <a name="using-schedule-apis-with-operationset"></a>Menggunakan API Jadual dengan OperationSet

Kerana rekod dengan kedua-dua **CreateProjectV1** dan **CreateTeamMemberV1** dicipta dengan serta-merta, API ini tidak boleh digunakan dalam **OperationSet** secara langsung. Walau bagaimanapun, anda boleh menggunakan API untuk mencipta rekod yang diperlukan, cipta **OperationSet** dan kemudian gunakan rekod yang dipracipta dalam **OperationSet**.

## <a name="supported-operations"></a>Operasi yang disokong

| Entiti penjadualan | Cipta | Kemas kini  | Delete | Pertimbangan penting |
| --- | --- | --- | --- | --- |
Tugas projek | Ya | Ya | Ya | Tiada |
| Pergantungan tugas projek | Ya | Ya | | Rekod pergantungan tugas projek tidak dikemas kini. Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta. |
| Penugasan sumber | Ya | Ya | | Operasi dengan medan berikut tidak disokong: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** dan **PlannedWork**. Rekod penugasan sumber tidak dikemas kini. Sebaliknya, rekod lama boleh dipadamkan dan rekod baharu boleh dicipta. |
| Baldi projek | T/B | T/B | T/B | Baldi lalai dicipta menggunakan API **CreateProjectV1**. |
| Ahli pasukan projek | Ya | Ya | Ya | Untuk mencipta operasi, gunakan API **CreateTeamMemberV1**. |
| Project | Ya | Ya | T/B | Operasi dengan medan berikut tidak disokong: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** dan **Duration**. |

Api ini boleh dipanggil dengan objek entiti yang termasuk medan tersuai.

Sifat ID adalah pilihan. Jika ia disediakan, sistem cuba untuk menggunakannya dan memberikan pengecualian jika ia tidak boleh digunakan. Jika ia tidak disediakan, sistem akan menjananya.

## <a name="restricted-fields"></a>Medan terhad

Jadual berikut mentakrifkan medan yang terhad daripada **Cipta** dan **Edit.**

### <a name="project-task"></a>Tugas projek

| **Nama logik**                       | **Boleh cipta** | **Boleh edit**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | tidak             | tidak               |
| msdyn_actualcost_base                  | tidak             | tidak               |
| msdyn_actualend                        | tidak             | tidak               |
| msdyn_actualsales                      | tidak             | tidak               |
| msdyn_actualsales_base                 | tidak             | tidak               |
| msdyn_actualstart                      | tidak             | tidak               |
| msdyn_costatcompleteestimate           | tidak             | tidak               |
| msdyn_costatcompleteestimate_base      | tidak             | tidak               |
| msdyn_costconsumptionpercentage        | tidak             | tidak               |
| msdyn_effortcompleted                  | tidak             | tidak               |
| msdyn_effortestimateatcomplete         | tidak             | tidak               |
| msdyn_iscritical                       | tidak             | tidak               |
| msdyn_iscriticalname                   | tidak             | tidak               |
| msdyn_ismanual                         | tidak             | tidak               |
| msdyn_ismanualname                     | tidak             | tidak               |
| msdyn_ismilestone                      | tidak             | tidak               |
| msdyn_ismilestonename                  | tidak             | tidak               |
| msdyn_LinkStatus                       | tidak             | tidak               |
| msdyn_linkstatusname                   | tidak             | tidak               |
| msdyn_msprojectclientid                | tidak             | tidak               |
| msdyn_plannedcost                      | tidak             | tidak               |
| msdyn_plannedcost_base                 | tidak             | tidak               |
| msdyn_plannedsales                     | tidak             | tidak               |
| msdyn_plannedsales_base                | tidak             | tidak               |
| msdyn_pluginprocessingdata             | tidak             | tidak               |
| msdyn_progress                         | tidak             | tidak (ya untuk P4W) |
| msdyn_remainingcost                    | tidak             | tidak               |
| msdyn_remainingcost_base               | tidak             | tidak               |
| msdyn_remainingsales                   | tidak             | tidak               |
| msdyn_remainingsales_base              | tidak             | tidak               |
| msdyn_requestedhours                   | tidak             | tidak               |
| msdyn_resourcecategory                 | tidak             | tidak               |
| msdyn_resourcecategoryname             | tidak             | tidak               |
| msdyn_resourceorganizationalunitid     | tidak             | tidak               |
| msdyn_resourceorganizationalunitidname | tidak             | tidak               |
| msdyn_salesconsumptionpercentage       | tidak             | tidak               |
| msdyn_salesestimateatcomplete          | tidak             | tidak               |
| msdyn_salesestimateatcomplete_base     | tidak             | tidak               |
| msdyn_salesvariance                    | tidak             | tidak               |
| msdyn_salesvariance_base               | tidak             | tidak               |
| msdyn_scheduleddurationminutes         | tidak             | tidak               |
| msdyn_scheduledend                     | tidak             | tidak               |
| msdyn_scheduledstart                   | tidak             | tidak               |
| msdyn_schedulevariance                 | tidak             | tidak               |
| msdyn_skipupdateestimateline           | tidak             | tidak               |
| msdyn_skipupdateestimatelinename       | tidak             | tidak               |
| msdyn_summary                          | tidak             | tidak               |
| msdyn_varianceofcost                   | tidak             | tidak               |
| msdyn_varianceofcost_base              | tidak             | tidak               |

### <a name="project-task-dependency"></a>Pergantungan tugas projek

| **Nama logik**              | **Boleh cipta** | **Boleh edit** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | tidak             | tidak           |
| msdyn_linktypename            | tidak             | tidak           |
| msdyn_predecessortask         | ya            | tidak           |
| msdyn_predecessortaskname     | ya            | tidak           |
| msdyn_project                 | ya            | tidak           |
| msdyn_projectname             | ya            | tidak           |
| msdyn_projecttaskdependencyid | ya            | tidak           |
| msdyn_successortask           | ya            | tidak           |
| msdyn_successortaskname       | ya            | tidak           |

### <a name="resource-assignment"></a>Penugasan sumber

| **Nama logik**             | **Boleh cipta** | **Boleh edit** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | ya            | tidak           |
| msdyn_bookableresourceidname | ya            | tidak           |
| msdyn_bookingstatusid        | tidak             | tidak           |
| msdyn_bookingstatusidname    | tidak             | tidak           |
| msdyn_committype             | tidak             | tidak           |
| msdyn_committypename         | tidak             | tidak           |
| msdyn_effort                 | tidak             | tidak           |
| msdyn_effortcompleted        | tidak             | tidak           |
| msdyn_effortremaining        | tidak             | tidak           |
| msdyn_finish                 | tidak             | tidak           |
| msdyn_plannedcost            | tidak             | tidak           |
| msdyn_plannedcost_base       | tidak             | tidak           |
| msdyn_plannedcostcontour     | tidak             | tidak           |
| msdyn_plannedsales           | tidak             | tidak           |
| msdyn_plannedsales_base      | tidak             | tidak           |
| msdyn_plannedsalescontour    | tidak             | tidak           |
| msdyn_plannedwork            | tidak             | tidak           |
| msdyn_projectid              | ya            | tidak           |
| msdyn_projectidname          | tidak             | tidak           |
| msdyn_projectteamid          | tidak             | tidak           |
| msdyn_projectteamidname      | tidak             | tidak           |
| msdyn_start                  | tidak             | tidak           |
| msdyn_taskid                 | tidak             | tidak           |
| msdyn_taskidname             | tidak             | tidak           |
| msdyn_userresourceid         | tidak             | tidak           |

### <a name="project-team-member"></a>Ahli pasukan projek

| **Nama logik**                                 | **Boleh cipta** | **Boleh edit** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | tidak             | tidak           |
| msdyn_creategenericteammemberwithrequirementname | tidak             | tidak           |
| msdyn_deletestatus                               | tidak             | tidak           |
| msdyn_deletestatusname                           | tidak             | tidak           |
| msdyn_effort                                     | tidak             | tidak           |
| msdyn_effortcompleted                            | tidak             | tidak           |
| msdyn_effortremaining                            | tidak             | tidak           |
| msdyn_finish                                     | tidak             | tidak           |
| msdyn_hardbookedhours                            | tidak             | tidak           |
| msdyn_hours                                      | tidak             | tidak           |
| msdyn_markedfordeletiontimer                     | tidak             | tidak           |
| msdyn_markedfordeletiontimestamp                 | tidak             | tidak           |
| msdyn_msprojectclientid                          | tidak             | tidak           |
| msdyn_percentage                                 | tidak             | tidak           |
| msdyn_requiredhours                              | tidak             | tidak           |
| msdyn_softbookedhours                            | tidak             | tidak           |
| msdyn_start                                      | tidak             | tidak           |

### <a name="project"></a>Project

| **Nama logik**                       | **Boleh cipta** | **Boleh edit** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | tidak             | tidak           |
| msdyn_actualexpensecost_base           | tidak             | tidak           |
| msdyn_actuallaborcost                  | tidak             | tidak           |
| msdyn_actuallaborcost_base             | tidak             | tidak           |
| msdyn_actualsales                      | tidak             | tidak           |
| msdyn_actualsales_base                 | tidak             | tidak           |
| msdyn_contractlineproject              | ya            | tidak           |
| msdyn_contractorganizationalunitid     | ya            | tidak           |
| msdyn_contractorganizationalunitidname | ya            | tidak           |
| msdyn_costconsumption                  | tidak             | tidak           |
| msdyn_costestimateatcomplete           | tidak             | tidak           |
| msdyn_costestimateatcomplete_base      | tidak             | tidak           |
| msdyn_costvariance                     | tidak             | tidak           |
| msdyn_costvariance_base                | tidak             | tidak           |
| msdyn_duration                         | tidak             | tidak           |
| msdyn_effort                           | tidak             | tidak           |
| msdyn_effortcompleted                  | tidak             | tidak           |
| msdyn_effortestimateatcompleteeac      | tidak             | tidak           |
| msdyn_effortremaining                  | tidak             | tidak           |
| msdyn_finish                           | ya            | ya          |
| msdyn_globalrevisiontoken              | tidak             | tidak           |
| msdyn_islinkedtomsprojectclient        | tidak             | tidak           |
| msdyn_islinkedtomsprojectclientname    | tidak             | tidak           |
| msdyn_linkeddocumenturl                | tidak             | tidak           |
| msdyn_msprojectdocument                | tidak             | tidak           |
| msdyn_msprojectdocumentname            | tidak             | tidak           |
| msdyn_plannedexpensecost               | tidak             | tidak           |
| msdyn_plannedexpensecost_base          | tidak             | tidak           |
| msdyn_plannedlaborcost                 | tidak             | tidak           |
| msdyn_plannedlaborcost_base            | tidak             | tidak           |
| msdyn_plannedsales                     | tidak             | tidak           |
| msdyn_plannedsales_base                | tidak             | tidak           |
| msdyn_progress                         | tidak             | tidak           |
| msdyn_remainingcost                    | tidak             | tidak           |
| msdyn_remainingcost_base               | tidak             | tidak           |
| msdyn_remainingsales                   | tidak             | tidak           |
| msdyn_remainingsales_base              | tidak             | tidak           |
| msdyn_replaylogheader                  | tidak             | tidak           |
| msdyn_salesconsumption                 | tidak             | tidak           |
| msdyn_salesestimateatcompleteeac       | tidak             | tidak           |
| msdyn_salesestimateatcompleteeac_base  | tidak             | tidak           |
| msdyn_salesvariance                    | tidak             | tidak           |
| msdyn_salesvariance_base               | tidak             | tidak           |
| msdyn_scheduleperformance              | tidak             | tidak           |
| msdyn_scheduleperformancename          | tidak             | tidak           |
| msdyn_schedulevariance                 | tidak             | tidak           |
| msdyn_taskearlieststart                | tidak             | tidak           |
| msdyn_teamsize                         | tidak             | tidak           |
| msdyn_teamsize_date                    | tidak             | tidak           |
| msdyn_teamsize_state                   | tidak             | tidak           |
| msdyn_totalactualcost                  | tidak             | tidak           |
| msdyn_totalactualcost_base             | tidak             | tidak           |
| msdyn_totalplannedcost                 | tidak             | tidak           |
| msdyn_totalplannedcost_base            | tidak             | tidak           |


## <a name="limitations-and-known-issues"></a>Pengehadan dan isu yang diketahui
Berikut ialah senarai pengehadan dan isu yang diketahui:

- API Jadual hanya boleh digunakan oleh **Pengguna dengan Lesen Microsoft Project.** Ia tidak boleh digunakan oleh:
    - Pengguna aplikasi
    - Pengguna sistem
    - Pengguna integrasi
    - Pengguna lain yang tidak mempunyai lesen yang diperlukan
- Setiap **OperationSet** hanya boleh mempunyai maksimum 100 operasi.
- Setiap pengguna hanya boleh mempunyai maksimum 10 **OperationSet** terbuka.
- Project Operations menyokong jumlah maksimum 500 tugas pada sesuatu projek pada masa ini.
- Status kegagalan **OperationSet** dan log kegagalan tidak tersedia pada masa ini.
- [Had dan sempadan pada projek dan tugas](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Pengendalian ralat

   - Untuk menyemak ralat yang dijana daripada Set Operasi, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Set Operasi**.
   - Untuk menyemak ralat yang dijana daripada Perkhidmatan Penjadualan Projek, pergi ke **Tetapan** \> **Jadualkan Integrasi** \> **Log Ralat PSS**.

## <a name="sample-scenario"></a>Senario sampel

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

## <a name="additional-samples"></a>Sampel tambahan

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
    task["msdyn_progress"] = 0.34m;
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
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

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
