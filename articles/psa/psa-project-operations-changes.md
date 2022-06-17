---
title: Perubahan ciri daripada Project Service Automation kepada Project Operations
description: Artikel ini memberikan gambaran keseluruhan perubahan ciri daripada Automasi Perkhidmatan Projek kepada Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925361"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Perubahan ciri daripada Project Service Automation kepada Project Operations

Peningkatan dari Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations Lite akan dihantar dalam tiga fasa. Artikel ini menyediakan maklumat tentang perubahan besar yang anda boleh jangkakan untuk melihat apabila naik taraf selesai.

| Naik taraf penghantaran | Fasa 1 <br>(Januari 2022) | Fasa 2 <br>(Gelombang April 2022) | Fasa 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada pergantungan pada struktur pecahan kerja (WBS) untuk projek. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS termasuk dalam had Operasi Projek yang disokong pada masa ini. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Operasi Projek yang disokong pada masa ini, termasuk sokongan untuk klien desktop Projek. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Pengurusan projek

Perubahan yang paling ketara dalam pengalaman pengguna adalah dalam bidang perancangan projek. Operasi Projek menggunakan pengalaman moden baru untuk menguruskan struktur pecahan kerja (WBS) dengan memanfaatkan keupayaan penjadualan yang disediakan oleh [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Perbezaan dalam pengalaman penjadualan

Jadual berikut meringkaskan perbezaan penjadualan antara Automasi Perkhidmatan Projek dan Operasi Projek.

|  Penjadualan     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Templat projek - Keupayaan untuk menentukan dan menggunakan templat projek apabila projek dicipta  |  &nbsp;    | :heavy_check_mark: |
| Integrasi struktur pecahan kerja projek (WBS) dengan klien desktop   |    &nbsp;  | :heavy_check_mark: |
| Kekangan - Mulakan tidak lebih awal daripada, selesaikan tidak lewat daripada  | :heavy_check_mark: |   &nbsp;  |
| Milestones - Tugas dengan tempoh sifar   | :heavy_check_mark:  |  &nbsp;  |
| Tugas yang didorong oleh sumber akan menghormati ketersediaan sumber yang ditugaskan   | :heavy_check_mark: |  &nbsp;    |
| Penyuntingan berfasa masa - Edit rancangan dan bekerja setiap hari   |   &nbsp;  | :heavy_check_mark: |
| Penjadualan automatik/manual - Gunakan enjin penjadualan Projek untuk menjadualkan tugas secara automatik atau manual |  &nbsp; | :heavy_check_mark:  |
| Edit projek besar secara langsung dalam antara muka pengguna: Tiada had untuk saiz pelan yang boleh diedit  | 500 had tugas  | :heavy_check_mark:       |
| Peratus selesai - Tandakan kemajuan tugas   | :heavy_check_mark:  |  &nbsp;  |
| [Mod](../project-management/scheduling-modes.md) Jadual Projek - Tentukan projek sebagai unit tetap, usaha tetap, atau tempoh tetap | :heavy_check_mark: | &nbsp; |
| Garis masa - Bina dan sesuaikan paparan garis masa untuk menggambarkan butiran jadual dan berkomunikasi dengan pihak berkepentingan. | :heavy_check_mark:  | &nbsp; |
| Tugas yang didorong oleh usaha - Menjadualkan sokongan enjin untuk menjadualkan tugas sebagai usaha yang didorong oleh usaha  | :heavy_check_mark:  | &nbsp; |
| **Kotak dialog maklumat** tugas - Simpan butiran tugas menggunakan kotak dialog | :heavy_check_mark:  |  &nbsp;  |
| Seret dan lepas - Pelbagai tugas pilih dan ubah suai kedudukan mereka pada WBS | :heavy_check_mark: | &nbsp;  |
| Pandangan berterusan fleksibel - Takrifkan pandangan yang lebih terperinci bagi atribut tugas   | :heavy_check_mark:  | &nbsp; |
| Mengisih dan menapis WBS  | :heavy_check_mark:  | &nbsp; |
| Pandangan papan untuk penghantaran projek bukan air terjun  | :heavy_check_mark:   | &nbsp; |
| Paparan garis masa - Carta Gantt interaktif yang digunakan untuk memvisualisasikan dan mengedit WBS   | :heavy_check_mark:  | &nbsp; |
| Pintasan Papan Kekunci - Gunakan pintasan papan kekunci untuk operasi biasa, seperti inden atau selitkan  | :heavy_check_mark:  |  &nbsp; |
| Buat asal pelbagai peringkat - Lakukan analisis apa-jika untuk memahami sepenuhnya kesan perubahan dengan membalikkan dan memohon semula keseluruhan set operasi | :heavy_check_mark: | &nbsp; |
| Potong/Salin/Tampal - Bekerjasama pada pembangunan jadual dengan menyalin dan menampal butiran jadual antara aplikasi  | :heavy_check_mark: | &nbsp; |
| Senarai semak tugas - Tambah sehingga 20 item senarai semak pada tugas   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Perancangan projek

Halaman **Projek** dalam Operasi Projek mempunyai sejumlah besar perbezaan berbanding **dengan halaman Projek** dalam Automasi Perkhidmatan Projek.

Tindakan berikut telah dialih **keluar daripada halaman Projek** sebagai sebahagian daripada naik taraf Fasa 1:

  - **Buka dalam MS Project**
  - **Cipta Templat**
  - **Nyahpaut dari MS Project**

Halaman **Projek** dalam Operasi Projek termasuk tab baru berikut.

- **Anggaran Bahan**
- **Persediaan Pengebilan Tugas**

Tab **Status** telah dialih **keluar dan medan Status** kini berada di **tab Ringkasan** dengan mod penjadualan projek.

   ![Kemas kini pada halaman Projek.](media/projectform.png)

Tab **Jadual** telah dinamakan semula kepada **tab Tugas** dan menampilkan pengalaman perancangan projek baru dengan Project for the Web.

   ![Tab Tugas Projek Baru.](media/tasktab.png)

## <a name="scheduling-modes"></a>Mod penjadualan

Operasi Projek telah memperkenalkan ciri baru, [mod](../project-management/scheduling-modes.md) Penjadualan. Semua projek Automasi Perkhidmatan Projek sedia ada akan lalai kepada **Tempoh** Tetap dalam Operasi Projek. Walau bagaimanapun, lalai untuk projek baru boleh diuruskan dengan pergi ke **Mod** > **Jadual Parameter** > **Parameter** > **Tetapan**.

   ![Seting parameter projek untuk mod Jadual.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Had perancangan projek

Operasi Projek bergantung pada Project for the Web untuk semua operasi penjadualan projek. Projek untuk Web menguruskan struktur pecahan kerja menggunakan had dalam jadual berikut.

| **Medan**                                          | **Had**             |
|----------------------------------------------------|-----------------------|
| Jumlah tugas maksimum untuk projek                  | 500                   |
| Jumlah tempoh maksimum untuk projek               | 3,650 hari (10 tahun)  |
| Jumlah sumber maksimum untuk projek              | 300                   |
| Jumlah pautan maksimum (pengganti sahaja) untuk projek | 600                   |
| Jumlah medan tersuai maksimum untuk projek          | 10                    |
| Tahap hierarki maksimum                            | 10 tahap             |
| Pautan maksimum (pengganti + pendahulu)            | 20                    |
| Tempoh maksimum tugas daun                      | 1250 hari             |
| Tempoh maksimum tugas ringkasan                 | 3,650 hari (10 tahun)  |
| Sumber maksimum ditugaskan kepada tugas               | 20 sumber          |
| Julat tarikh yang disokong untuk tugas                    | 1/1/2000 - 31/12/2149 |
| Item senarai semak                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Kepanjangan dan pembangunan perancangan projek

Selepas anda menaik taraf kepada Project Operations, anda mesti menggunakan API Penjadualan Projek untuk melaksanakan penciptaan, kemas kini dan memadamkan operasi pada entiti berikut:

|   Nama entiti           |   Nama logik entiti       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tugas Projek            | msdyn_projecttask           |
| Kebergantungan Tugas Projek | msdyn_projecttaskdependency |
| Tugasan Sumber     | msdyn_resourceassignment    |
| Baldi Projek          | msdyn_projectbucket         |
| Ahli Pasukan Projek     | msdyn_projectteam           |

Jika anda mempunyai penyesuaian yang melibatkan entiti ini pada masa ini, lihat [Menggunakan API jadual Projek untuk melaksanakan operasi dengan entiti](../project-management/schedule-api-preview.md) Penjadualan untuk panduan pelaksanaan.

## <a name="data-model-changes"></a>Perubahan model data

Sebagai sebahagian daripada Naik Taraf Fasa 1, terdapat perubahan pada model data. Perubahan ini adalah terutamanya perubahan medan kepada entiti sedia ada. Dalam Fasa 1, entiti, **msydn_project** dan **msdyn_projectteam** adalah refactoring penyesuaian. 

> [!IMPORTANT]
> Bahagian ini akan dikemas kini dengan entiti tambahan apabila fasa naik taraf masa depan selesai.

Medan berikut telah digantikan dengan medan baru.

|   EntitI          |   Nama logik lama   |   Nama logik baru    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Medan berikut telah ditambah.

|   EntitI          |   Nama logik                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Menunjukkan agregat jualan yuran sebenar pada projek. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_actualmaterialcost                     | Menunjukkan agregat kos bahan sebenar pada projek. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_actualmaterialsales                    | Menunjukkan agregat jualan bahan sebenar pada projek. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Barisan kontrak yang berkaitan dengan projek ini. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ini ialah medan sistem dalaman yang digunakan untuk **Salin Projek** yang berkaitan dengan Pengenalpasti Korelasi. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ini ialah medan sistem dalaman, digunakan untuk **Salin Projek** yang berkaitan dengan Pengenalpasti Sesi. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Segerakkan terakhir Token Semakan Global xRM daripada perkhidmatan penjadualan Projek. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokumen Projek Microsoft yang tergolong dalam projek. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Agregat kos bahan yang dirancang pada projek itu. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Agregat jualan bahan yang dirancang pada projek itu. Untuk digunakan dalam Automasi Perkhidmatan Projek sahaja. |
| msdyn_project     | msdyn_program                                | Program yang projek ini dikaitkan. |
| msdyn_project     | msdyn_quotelineproject                       | Baris Petikan yang dikaitkan dengan projek ini. |
| msdyn_project     | msdyn_replaylogheader                        | Pengepala untuk log ulangan. |
| msdyn_project     | msdyn_schedulemode                           | Mod penjadualan lalai yang digunakan untuk semua tugas pada projek.  |
| msdyn_project     | msdyn_taskearlieststart                      | Tarikh mula terawal mana-mana tugas dalam projek.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Ahli pasukan projek yang telah disalin oleh ahli pasukan projek ini. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Menunjukkan sama ada untuk mencipta keperluan sumber untuk ahli pasukan generik yang baru dicipta.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status padam ahli pasukan untuk menjejak jika terdapat permintaan padam yang dihantar ke perkhidmatan penjadualan Projek dan sama ada ia berjaya menghantar respons kembali dalam tetingkap masa yang dijangkakan. |
| msdyn_projectteam | msdyn_effortcompleted                        | Menjejaki usaha yang dicapai oleh ahli pasukan dalam tugasan mereka. |
| msdyn_projectteam | msdyn_effortremaining                        | Menjejaki usaha yang belum selesai oleh ahli pasukan pada tugasan mereka. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Tempoh menunggu dari masa ahli pasukan menghantar permintaan padam kepada perkhidmatan penjadualan Projek sehingga ahli pasukan benar-benar dipadamkan pada Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Cap masa untuk merakam apabila permintaan pemadaman ahli pasukan dihantar ke perkhidmatan penjadualan Projek. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Tunjukkan ahli pasukan projek yang ahli pasukan projek ini telah disalin.  |

## <a name="project-templates"></a>Templat projek

Operasi Projek tidak memberikan sokongan untuk templat projek. Walau bagaimanapun, anda boleh meniru banyak fungsi teras dengan penggunaan [API Salinan Projek](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Sokongan tambahan desktop

Sokongan untuk tambahan Microsoft Project Desktop tidak akan tersedia dalam 2 fasa pertama naik taraf. Dalam Fasa 3, pelanggan yang mempunyai projek yang lebih besar daripada had Project yang disokong pada masa ini untuk Web akan dapat menggunakan tambahan desktop.

## <a name="editing-resource-assignment-contours"></a>Mengedit kontur tugasan sumber

Keupayaan untuk mengedit kontur tugasan sumber akan tersedia apabila Fasa 2 naik taraf tersedia.

## <a name="billing-and-pricing"></a>Pengebilan dan harga

Ciri baru berikut telah ditambah dalam Operasi Projek. Ciri-ciri ini bersifat tambahan dan tidak memberi kesan kepada model data Automasi Perkhidmatan Projek.

- [Penggunaan bahan rakaman pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan pengesahan kontrak tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Pengebilan berasaskan tugas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Komponen yang telah lapuk

Jadual berikut mendokumentasikan semua medan yang telah lapuk yang dialihkan ke naik taraf pasca penyelesaian komponen yang telah lapuk. Untuk maklumat lanjut dan pautan ke penyelesaian, lihat [Dynamics 365 Project Service Automation 3x ke Project Operations 4x komponen yang telah lapuk](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoisdetail

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantscount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Medan                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

