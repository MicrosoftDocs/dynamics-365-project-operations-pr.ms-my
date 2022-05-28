---
title: Log penjadualan projek
description: Topik ini menyediakan maklumat dan sampel yang akan membantu anda menggunakan log Penjadualan Projek untuk mengesan kegagalan yang berkaitan dengan Perkhidmatan Penjadualan Projek dan API Penjadualan Projek.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589529"
---
# <a name="project-scheduling-logs"></a>Log penjadualan projek

_**Digunakan Untuk:** Operasi Projek untuk senario berasaskan sumber / bukan stok, penggunaan Lite - berurusan dengan invois proforma_, _Projek untuk Web_

Microsoft Dynamics 365 Project Operations menggunakan [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) sebagai enjin penjadualan utamanya. Daripada menggunakan antara muka pengaturcaraan aplikasi Web standard Microsoft Dataverse (API), Operasi Projek menggunakan API Penjadualan Projek baharu untuk mencipta, mengemas kini dan memadam tugas projek, tugasan sumber, kebergantungan tugas, baldi projek dan ahli pasukan projek. Walau bagaimanapun, apabila operasi mencipta, mengemas kini atau memadam dijalankan secara programatik pada entiti struktur pecahan kerja (WBS), ralat mungkin berlaku. Untuk mengesan kesilapan ini dan sejarah operasi, dua log pentadbiran baru telah dilaksanakan: **Set Operasi dan** Perkhidmatan Penjadualan Projek (PSS) **·**. Untuk mengakses log ini, pergi ke Penyepaduan **Jadual Tetapan** \> **.**

Ilustrasi berikut menunjukkan model data untuk log Penjadualan Projek.

![Model data untuk log Penjadualan Projek.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Log Set Operasi

Log Set Operasi menjejaki pelaksanaan set operasi yang digunakan untuk menjalankan satu atau banyak mencipta, mengemas kini atau memadam operasi dalam kelompok pada projek, tugas projek, tugasan sumber, kebergantungan tugas, baldi projek atau ahli pasukan projek. Medan **Operasi dalam Status** menunjukkan status keseluruhan set operasi. Butiran operasi set muatan ditangkap dalam rekod Operasi Set Detail yang berkaitan.

### <a name="operation-set"></a>Set Operasi

Jadual berikut menunjukkan medan yang berkaitan **dengan entiti Set** Operasi.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Tarikh/masa apabila set operasi telah selesai atau gagal.                                                | CompletedOn            |
| msdyn_correlationid   | Nilai **korelasiId** permintaan.                                                                  | CorrelationId          |
| msdyn_description     | Perihalan set operasi.                                                                        | Description            |
| msdyn_executedon      | Tarikh/masa apabila rekod dijalankan.                                                                       | Dilaksanakan Pada            |
| msdyn_operationsetId  | Pengenalpasti unik bagi kejadian entiti.                                                                   | OperationSet           |
| msdyn_Project         | Projek yang berkaitan dengan set operasi.                                                            | Project                |
| msdyn_projectid       | Nilai **projectId** permintaan.                                                                      | ProjectId (Ditamatkan) |
| msdyn_projectName     | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_PSSErrorLog     | Pengenalpasti unik log ralat Perkhidmatan Penjadualan Projek yang dikaitkan dengan set operasi. | Log Ralat PSS          |
| msdyn_PSSErrorLogName | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_status          | Status set operasi.                                                                             | Status                 |
| msdyn_statusName      | Tidak berkenaan.                                                                                              | Tidak berkenaan         |
| msdyn_useraadid       | Azure Active Directory ID objek (Azure AD) pengguna yang mana permintaan itu dimiliki.                     | UserAADID              |

### <a name="operation-set-detail"></a>Butiran Set Operasi

Jadual berikut menunjukkan medan yang berkaitan **dengan entiti Butiran** Set Operasi.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Medan bersiri Dataverse untuk permintaan.                                            | CdsPayload            |
| msdyn_entityname           | Nama entiti untuk permintaan itu.                                                     | EntityName            |
| msdyn_httpverb             | Kaedah permintaan.                                                                         | Kata Kerja HTTP (Ditamatkan) |
| msdyn_httpverbName         | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_operationset         | Pengenalpasti unik operasi menetapkan bahawa rekod itu dimiliki.                      | OperationSet          |
| msdyn_operationsetdetailId | Pengenalpasti unik bagi kejadian entiti.                                                  | Butiran OperationSet   |
| msdyn_operationsetName     | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_operationtype        | Jenis operasi operasi set terperinci.                                             | JenisOperasi         |
| msdyn_operationtypeName    | Tidak berkenaan.                                                                             | Tidak berkenaan        |
| msdyn_psspayload           | Medan Perkhidmatan Penjadualan Projek bersiri untuk permintaan.                           | PssPayload            |
| msdyn_recordid             | Pengenalpasti rekod permintaan.                                                       | ID Rekod             |
| msdyn_requestnumber        | Nombor yang dijana secara automatik yang mengenal pasti tertib yang diminta telah diterima. | Nombor Permintaan        |

## <a name="project-scheduling-service-error-logs"></a>Log ralat Perkhidmatan Penjadualan Projek

Log ralat Perkhidmatan Penjadualan Projek menangkap kegagalan yang berlaku apabila Perkhidmatan Penjadualan Projek mencuba **operasi Simpan** atau **Buka**. Terdapat tiga senario yang disokong di mana log ini dijana:

- Tindakan yang dimulakan pengguna gagal secara kritikal (contohnya, tugasan tidak dapat dicipta kerana keistimewaan yang hilang).
- Perkhidmatan Penjadualan Projek tidak boleh mencipta, mengemas kini, memadam atau melaksanakan sebarang operasi melata lain secara programatik pada entiti secara programatik.
- Pengguna mengalami ralat apabila rekod gagal dibuka (contohnya, apabila projek dibuka atau maklumat ahli pasukan dikemas kini).

### <a name="project-scheduling-service-log"></a>Log Perkhidmatan Penjadualan Projek

Jadual berikut menunjukkan medan yang disertakan dalam log Perkhidmatan Penjadualan Projek.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Tindanan panggilan pengecualian.                                               | Tindanan Panggilan     |
| msdyn_correlationid | ID korelasi ralat.                                               | CorrelationId  |
| msdyn_errorcode     | Medan yang digunakan untuk menyimpan Dataverse kod ralat atau kod ralat HTTP. | Kod Ralat     |
| msdyn_HelpLink      | Pautan ke dokumentasi Bantuan awam.                                       | Pautan Bantuan      |
| msdyn_log           | Log dari Perkhidmatan Penjadualan Projek.                                   | Log            |
| msdyn_project       | Projek yang dikaitkan dengan log ralat.                             | Project        |
| msdyn_projectName   | Nama projek jika muatan set operasi akan berterusan. | Tidak berkenaan |
| msdyn_psserrorlogId | Pengenalpasti unik bagi kejadian entiti.                                     | Log Ralat PSS  |
| msdyn_SessionId     | ID sesi projek.                                                        | Id Sesi     |

## <a name="error-log-cleanup"></a>Pembersihan log ralat

Secara lalai, kedua-dua log ralat Perkhidmatan Penjadualan Projek dan log Set Operasi boleh dibersihkan setiap 90 hari. Sebarang rekod yang lebih lama daripada 90 hari akan dipadamkan. Walau bagaimanapun, dengan **mengubah nilai medan msdyn_StateOperationSetAge** pada **halaman Parameter** Projek, pentadbir boleh melaraskan julat pembersihan supaya ia antara 1 dan 120 hari. Beberapa kaedah untuk menukar nilai ini boleh didapati:

- **Sesuaikan entiti Parameter** Projek dengan mencipta halaman tersuai dan menambah **medan Set Umur** Operasi Basi.
- Gunakan kod klien yang menggunakan [kit pembangunan perisian WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Gunakan kod SDK Perkhidmatan yang menggunakan kaedah Xrm SDK **updateRecord** (rujukan API Pelanggan) dalam aplikasi berpandukan model. Power Apps termasuk penerangan dan parameter yang disokong untuk **kaedah updateRecord**.

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
