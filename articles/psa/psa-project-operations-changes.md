---
title: Perubahan ciri daripada Project Service Automation kepada Project Operations
description: Artikel ini memberikan gambaran keseluruhan perubahan ciri daripada Project Service Automation kepada Dynamics 365 Project Operations.
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459938"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Perubahan ciri daripada Project Service Automation kepada Project Operations

Naik taraf daripada Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations Lite akan dihantar dalam tiga fasa. Artikel ini memberikan maklumat tentang perubahan besar yang boleh anda jangkakan apabila naik taraf telah selesai.

| Penghantaran naik taraf | Fasa 1 <br>(Januari 2022) | Fasa 2 <br>(November 2022) | Fasa 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada kebersandaran pada struktur pecahan kerja (WBS) untuk projek. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS termasuk dalam had Project Operations yang disokong pada masa ini. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Project Operations yang disokong pada masa ini, termasuk sokongan untuk Project desktop client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Pengurusan projek

Perubahan yang paling ketara dalam pengalaman pengguna akan berada dalam bidang perancangan projek. Project Operations menggunakan pengalaman moden yang baharu untuk menguruskan struktur pecahan kerja (WBS) dengan memanfaatkan keupayaan penjadualan yang disediakan oleh [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Perbezaan pengalaman penjadualan

Jadual berikut meringkaskan perbezaan penjadualan antara Project Service Automation dan Project Operations.

|  Penjadualan     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Templat projek - Keupayaan untuk mentakrifkan dan menggunakan templat projek apabila projek dicipta  |  &nbsp;    | :heavy_check_mark: |
| Integrasi struktur pecahan kerja (WBS) projek dengan klien desktop   |    &nbsp;  | :heavy_check_mark: |
| Kekangan - Mula tidak lebih awal dari, siapkan tidak lebih lewat dari  | :heavy_check_mark: |   &nbsp;  |
| Pencapaian - Tugas dengan tempoh sifar   | :heavy_check_mark:  |  &nbsp;  |
| Tugas yang didorong oleh sumber akan menghormati ketersediaan sumber yang ditugaskan   | :heavy_check_mark: |  &nbsp;    |
| Pengeditan fasa bermasa - Edit pelan dan kerja hari demi hari   |   &nbsp;  | :heavy_check_mark: |
| Penjadualan automatik/manual - Gunakan enjin penjadualan Projek untuk menjadualkan tugas secara automatik atau secara manual |  &nbsp; | :heavy_check_mark:  |
| Edit projek besar secara langsung dalam antara muka pengguna: Tiada had untuk saiz pelan yang boleh diedit  | 500 had tugas  | :heavy_check_mark:       |
| Peratus siap - Tandakan kemajuan tugas   | :heavy_check_mark:  |  &nbsp;  |
| [Mod Jadual Projek](../project-management/scheduling-modes.md) - Tentukan projek sebagai unit tetap, usaha tetap atau tempoh tetap | :heavy_check_mark: | &nbsp; |
| Garis masa - Bina dan sesuaikan pandangan garis masa untuk menggambarkan butiran jadual dan berkomunikasi dengan pemegang amanah. | :heavy_check_mark:  | &nbsp; |
| Tugas yang didorong oleh usaha - Sokongan enjin penjadualan untuk penjadualan tugas sebagai usaha didorong  | :heavy_check_mark:  | &nbsp; |
| Kotak dialog **maklumat tugas** - Simpan butiran tugas menggunakan kotak dialog | :heavy_check_mark:  |  &nbsp;  |
| Seret dan lepas - Pilih berbilang tugas dan ubah suai kedudukan tugas pada WBS | :heavy_check_mark: | &nbsp;  |
| Pandangan berterusan fleksibel - Takrifkan lebih banyak pandangan terperinci atribut tugas   | :heavy_check_mark:  | &nbsp; |
| Isih dan tapis WBS  | :heavy_check_mark:  | &nbsp; |
| Pandangan papan untuk penghantaran projek bukan air terjun  | :heavy_check_mark:   | &nbsp; |
| Pandangan garis masa - Carta Gantt interaktif digunakan untuk menggambarkan dan mengedit WBS   | :heavy_check_mark:  | &nbsp; |
| Pintasan Papan Kekunci - Gunakan pintasan papan kekunci untuk operasi biasa, seperti engsot atau sisip  | :heavy_check_mark:  |  &nbsp; |
| Buat asal berbilang tahap - Menjalankan analisis bagaimana jika untuk memahami sepenuhnya kesan perubahan dengan membalikkan dan menggunakan semula keseluruhan set operasi | :heavy_check_mark: | &nbsp; |
| Potong/Salin/Tampal - Bekerjasama pada pembangunan jadual dengan menyalin dan menampal butiran jadual antara aplikasi  | :heavy_check_mark: | &nbsp; |
| Senarai semak tugas - Tambah sehingga 20 item senarai semak kepada tugas   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Perancangan projek

Halaman **Projek** dalam Project Operations mempunyai bilangan besar perbezaan berbanding dengan halaman **Projek** dalam Project Service Automation.

Tindakan berikut telah dialih keluar daripada halaman **Projek** sebagai sebahagian daripada naik taraf Fasa 1:

  - **Buka dalam MS Project**
  - **Cipta Templat**
  - **Nyahpaut dari MS Project**

Halaman **Projek** dalam Project Operations termasuk tab baharu berikut.

- **Anggaran Bahan**
- **Persediaan Pengebilan Tugas**

Tab **Status** telah dialih keluar dan medan **Status** kini berada pada tab **Ringkasan** dengan mod penjadualan projek.

   ![Kemas kini kepada halaman Projek.](media/projectform.png)

Tab **Jadual** telah dinamakan semula kepada tab **Tugas** dan menampilkan pengalaman perancangan projek baharu dengan Project for the Web.

   ![Tab tugas Projek baharu.](media/tasktab.png)

## <a name="scheduling-modes"></a>Mod penjadualan

Project Operations telah memperkenalkan ciri baharu, [mod Penjadualan](../project-management/scheduling-modes.md). Semua projek Project Service Automation sedia ada akan lalai ke **Tempoh Tetap** dalam Project Operations. Walau bagaimanapun, lalai untuk projek baharu boleh diuruskan dengan pergi ke **Tetapan** > **Parameter** > **Parameter** > **Mod Jadual**.

   ![Tetapan parameter projek untuk mod Jadual.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Had perancangan projek

Project Operations bergantung pada Project for the Web untuk semua operasi penjadualan projek. Project for the Web menguruskan struktur pecahan kerja menggunakan had dalam jadual berikut.

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

## <a name="project-planning-extensibility-and-development"></a>Kebolehpanjangan dan pembangunan perancangan projek

Selepas anda menaik taraf kepada Project Operations, anda mesti menggunakan API Penjadualan Projek untuk melaksanakan operasi cipta, kemas kini dan padam pada entiti berikut:

|   Nama entiti           |   Nama logik entiti       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tugas Projek            | msdyn_projecttask           |
| Kebergantungan Tugas Projek | msdyn_projecttaskdependency |
| Tugasan Sumber     | msdyn_resourceassignment    |
| Baldi Projek          | msdyn_projectbucket         |
| Ahli Pasukan Projek     | msdyn_projectteam           |

Jika anda mempunyai penyesuaian yang melibatkan entiti ini pada masa ini, lihat [Gunakan API jadual Projek untuk menjalankan operasi dengan entiti Penjadualan](../project-management/schedule-api-preview.md) untuk panduan pelaksanaan.

## <a name="data-model-changes"></a>Perubahan model data

Sebagai sebahagian daripada Naik Taraf Fasa 1, terdapat perubahan pada model data. Perubahan ini ialah perubahan medan terutamanya pada entiti yang sedia ada. Dalam Fasa 1, entiti, **msydn_project** dan **msdyn_projectteam** ialah pemfaktoran semula penyesuaian. 

> [!IMPORTANT]
> Bahagian ini akan dikemas kini dengan entiti tambahan kerana fasa naik taraf masa depan telah disiapkan.

Medan berikut telah digantikan dengan medan baharu.

|   EntitI          |   Nama logik lama   |   Nama logik baharu    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Medan berikut telah ditambahkan.

|   EntitI          |   Nama logik                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Menunjukkan agregat jualan yuran sebenar pada projek. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_actualmaterialcost                     | Menunjukkan agregat kos bahan sebenar pada projek. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_actualmaterialsales                    | Menunjukkan agregat jualan bahan sebenar pada projek. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Baris kontrak yang dikaitkan dengan projek ini. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Ini ialah medan sistem dalaman yang digunakan untuk **Salin Projek** yang dikaitkan dengan Pengecam Korelasi. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Ini ialah medan sistem dalaman, yang digunakan untuk **Salin Projek** yang dikaitkan dengan Pengecam Sesi. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Token Semakan Global xRM penyegerakan akhir daripada perkhidmatan penjadualan Projek. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokumen Microsoft Project yang tergolong dalam projek. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Agregat kos bahan yang dirancang pada projek. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Agregat jualan bahan yang dirancang pada projek. Untuk kegunaan dalam Project Service Automation sahaja. |
| msdyn_project     | msdyn_program                                | Program yang projek ini dikaitkan. |
| msdyn_project     | msdyn_quotelineproject                       | Baris Sebut Harga yang dikaitkan dengan projek ini. |
| msdyn_project     | msdyn_replaylogheader                        | Pengepala untuk log main semula. |
| msdyn_project     | msdyn_schedulemode                           | Mod penjadualan lalai yang digunakan untuk semua tugas pada projek.  |
| msdyn_project     | msdyn_taskearlieststart                      | Tarikh mula terawal mana-mana tugas dalam projek.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Ahli pasukan projek yang disalin untuk ahli pasukan projek ini. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Menunjukkan sama ada untuk mencipta keperluan sumber bagi ahli pasukan generik yang baharu dicipta.  |
| msdyn_projectteam | msdyn_deletestatus                           | Status padam ahli pasukan yang akan dijejaki jika terdapat permintaan padam dihantar kepada perkhidmatan penjadualan Projek dan sama ada ia berjaya menghantar semula respons dan dalam tetingkap masa yang dijangka. |
| msdyn_projectteam | msdyn_effortcompleted                        | Menjejak usaha yang dicapai oleh ahli pasukan dalam tugasan mereka. |
| msdyn_projectteam | msdyn_effortremaining                        | Menjejak usaha yang belum dilengkapkan oleh ahli pasukan dalam tugasan mereka. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Tempoh menunggu apabila ahli pasukan menghantar permintaan padam kepada perkhidmatan penjadualan Projek sehingga ahli pasukan sebenarnya dipadamkan Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Cap masa untuk direkodkan apabila permintaan pemadaman ahli pasukan dihantar ke perkhidmatan penjadualan Projek. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Tunjukkan ahli pasukan projek yang ahli pasukan projek ini telah disalin.  |

## <a name="project-templates"></a>Templat projek

Project Operations tidak memberikan sokongan untuk templat projek. Walau bagaimanapun, anda boleh meniru banyak fungsi teras dengan penggunaan [API Salin Projek](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Sokongan tambahan desktop

Sokongan untuk tambahan Desktop Microsoft Project tidak akan tersedia dalam 2 fasa pertama naik taraf. Dalam Fasa 3, pelanggan yang mempunyai projek yang lebih besar daripada had projek yang disokong Project for the Web pada masa ini akan dapat menggunakan tambahan desktop.

## <a name="editing-resource-assignment-contours"></a>Mengedit kontur tugasan sumber

Keupayaan untuk mengedit kontur penugasan sumber akan tersedia apabila naik taraf Fasa 2 tersedia.

## <a name="billing-and-pricing"></a>Pengebilan dan harga

Ciri baharu berikut telah ditambahkan dalam Project Operations. Ciri ini ialah tambahan secara semula jadi dan tidak memberi kesan kepada model data Project Service Automation.

- [Penggunaan bahan rekod pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan pengesahan kontrak yang tidak boleh dilebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Pengebilan berasaskan tugas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Komponen ditamatkan

Jadual berikut mendokumenkan semua medan yang ditamatkan yang dipindahkan ke penyelesaian komponen ditamatkan selepas naik taraf. Untuk mendapatkan maklumat lanjut dan pautan penyelesaian, lihat [Dynamics 365 Project Service Automation 3x untuk Project Operations 4x komponen ditamatkan](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

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
| msdyn_projectteam.msdyn_applicantcount                                                        |
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

