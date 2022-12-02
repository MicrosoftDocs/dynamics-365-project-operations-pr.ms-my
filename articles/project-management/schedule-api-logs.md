---
title: Log penjadualan projek
description: Artikel ini memberikan maklumat dan sampel yang akan membantu anda menggunakan log Penjadualan Projek untuk menjejaki kegagalan yang berkaitan dengan Perkhidmatan Penjadualan Projek dan API Penjadualan Projek.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923706"
---
# <a name="project-scheduling-logs"></a>Log penjadualan projek

_**Digunakan Untuk:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Lite - urusan untuk penginvoisan proforma_, _Project for the Web_

Microsoft Dynamics 365 Project Operations menggunakan [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) sebagai enjin penjadualan utama. Daripada menggunakan antara muka pengaturcaraan aplikasi (API) Web standard Microsoft Dataverse, Project Operations menggunakan API Penjadualan Projek baharu untuk mencipta, mengemas kini, dan memadamkan tugas projek, tugas sumber, kebergantungan tugas, baldi projek, dan ahli pasukan projek. Walau bagaimanapun, apabila mencipta, mengemas kini atau memadamkan operasi yang dijalankan secara programatik pada entiti struktur pecahan kerja (WBS), ralat mungkin berlaku. Untuk menjejaki ralat ini dan sejarah operasi, dua log pentadbiran baharu telah dilaksanakan: **Set Operasi** dan **Perkhidmatan Penjadualan Projek (PSS)**. Untuk mencapai log ini, pergi ke **Penyepaduan Tetapan** \> **Jadual**.

Ilustrasi berikut menunjukkan model data untuk log Penjadualan Projek.

![Model data untuk log Penjadualan Projek.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log Set Operasi

Log Set Operasi menjejaki pelaksanaan set operasi yang digunakan untuk menjalankan satu atau banyak operasi cipta, kemas kini atau padam secara pukal pada projek, tugas projek, tugas sumber, kebergantungan tugas, baldi projek atau ahli pasukan projek. Medan **Operasi dalam Status** menunjukkan status keseluruhan bagi set operasi. Butiran muat beban set operasi diambil dalam rekod Butiran Set Operasi yang berkaitan.

### <a name="operation-set"></a>Set Operasi

Jadual berikut menunjukkan medan yang berkaitan dengan entiti **Set Operasi**.

| Nama Skema            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Tarikh/masa sewaktu set operasi diselesaikan atau gagal.                                                | CompletedOn            |
| msdyn_correlationid   | Nilai **correlationId** permintaan.                                                                  | CorrelationId          |
| msdyn_description     | Perihalan set operasi.                                                                        | Description            |
| msdyn_executedon      | Tarikh/masa apabila rekod telah dijalankan.                                                                       | Dilaksanakan Pada            |
| msdyn_operationsetId  | Pengecam unik tika entiti.                                                                   | OperationSet           |
| msdyn_Project         | Projek yang berkaitan dengan set operasi.                                                            | Project                |
| msdyn_projectid       | Nilai **projectId** permintaan.                                                                      | ProjectId (Ditamatkan) |
| msdyn_projectName     | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_PSSErrorLog     | Pengecam unik log ralat Perkhidmatan Penjadualan Projek yang berkaitan dengan set operasi. | Log Ralat PSS          |
| msdyn_PSSErrorLogName | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_status          | Status set operasi.                                                                             | Status                 |
| msdyn_statusName      | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_useraadid       | ID objek Azure Active Directory (Azure AD) pengguna yang permintaan ini tergolong.                     | UserAADID              |

### <a name="operation-set-detail"></a>Butiran Set Operasi

Jadual berikut menunjukkan medan yang berkaitan dengan entiti **Butiran Set Operasi**.

| Nama Skema                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Medan Dataverse bersiri untuk permintaan.                                            | CdsPayload            |
| msdyn_entityname           | Nama entiti bagi permintaan ini.                                                     | EntityName            |
| msdyn_httpverb             | Kaedah permintaan.                                                                         | Kata Kerja HTTP (Ditamatkan) |
| msdyn_httpverbName         | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_operationset         | Pengecam unik set operasi yang rekod ini tergolong.                      | OperationSet          |
| msdyn_operationsetdetailId | Pengecam unik tika entiti.                                                  | Butiran OperationSet   |
| msdyn_operationsetName     | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_operationtype        | Jenis operasi untuk butiran set operasi.                                             | JenisOperasi         |
| msdyn_operationtypeName    | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_psspayload           | Medan Perkhidmatan Penjadualan Projek bersiri untuk permintaan.                           | PssPayload            |
| msdyn_recordid             | Pengecam bagi rekod permintaan.                                                       | ID Rekod             |
| msdyn_requestnumber        | Nombor dijana secara automatik yang mengenal pasti urutan yang permintaan telah diterima. | Nombor Permintaan        |

## <a name="project-scheduling-service-error-logs"></a>Log ralat Perkhidmatan Penjadualan Projek

Log ralat Perkhidmatan Penjadualan Projek yang merakam kegagalan yang berlaku apabila Perkhidmatan Penjadualan Projek cuba **Simpan** atau **Buka** operasi. Terdapat tiga senario yang disokong apabila log ini dijana:

- Tindakan yang dimulakan oleh pengguna mengalami gagal yang kritikal (contohnya, tugasan tidak boleh dicipta kerana tiada kelayakan).
- Perkhidmatan Penjadualan Projek tidak boleh mencipta, mengemas kini, memadamkan atau melaksanakan sebarang operasi lata pada entiti secara programatik.
- Pengguna mengalami ralat apabila rekod gagal dibuka (sebagai contoh, apabila projek dibuka atau maklumat ahli pasukan dikemas kini).

### <a name="project-scheduling-service-log"></a>Log Perkhidmatan Penjadualan Projek

Jadual berikut menunjukkan medan yang disertakan dalam log Perkhidmatan Penjadualan Projek.

| Nama Skema          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Tindanan panggilan pengecualian.                                               | Tindanan Panggilan     |
| msdyn_correlationid | ID korelasi ralat.                                               | CorrelationId  |
| msdyn_errorcode     | Medan yang digunakan untuk menyimpan kod ralat Dataverse atau kod ralat HTTP. | Kod Ralat     |
| msdyn_HelpLink      | Pautan ke dokumentasi Bantuan awam.                                       | Pautan Bantuan      |
| msdyn_log           | Log daripada Perkhidmatan Penjadualan Projek.                                   | Log            |
| msdyn_project       | Projek yang dikaitkan dengan log ralat ini.                             | Project        |
| msdyn_projectName   | Nama projek jika muat beban bagi set operasi akan berterusan. | Tidak berkenaan |
| msdyn_psserrorlogId | Pengecam unik tika entiti.                                     | Log Ralat PSS  |
| msdyn_SessionId     | ID sesi projek.                                                        | Id Sesi     |

## <a name="error-log-cleanup"></a>Pembersihan loh ralat

Secara lalai, kedua-dua log ralat Perkhidmatan Penjadualan Projek dan log Set Operasi boleh dibersihkan setiap 90 hari. Sebarang rekod kegagalan yang lebih lama dari 90 hari akan dipadamkan. Walau bagaimanapun, dengan mengubah nilai medan **msdyn_StateOperationSetAge** pada halaman **Parameter Projek**, pentadbir boleh melaraskan julat pembersihan supaya menjadi antara 1 hingga 120 hari. Beberapa kaedah untuk mengubah nilai ini boleh didapati:

- Sesuaikan entiti **Parameter Projek** dengan mencipta halaman tersuai dan menambahkan medan **Usia Set Operasi Lapuk**.
- Gunakan kod klien yang menggunakan [kit pembangunan perisian WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Gunakan kod SDK Perkhidmatan yang menggunakan kaedah Xrm SDK **updateRecord** (Rujukan API klien) dalam aplikasi berpandukan model. Power Apps termasuk perihalan dan parameter yang disokong untuk kaedah **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
