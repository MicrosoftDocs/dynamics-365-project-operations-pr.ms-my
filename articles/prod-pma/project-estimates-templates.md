---
title: Segerakkan anggaran projek secara langsung daripada Project Service Automation kepada Finance and Operations
description: Topik ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan anggaran jam projek dan anggaran perbelanjaan projek secara langsung daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988212"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Segerakkan anggaran projek secara langsung daripada Project Service Automation kepada Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan anggaran jam projek dan anggaran perbelanjaan projek secara langsung daripada Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.

> [!NOTE]
> - Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation kepada Finance

Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat integrasi yang tersedia dengan ciri Integrasi data mendayakan aliran data tentang anggaran jam projek dan anggaran perbelanjaan projek daripada Project Service Automation kepada Kewangan.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Kewangan.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Anggaran jam projek

### <a name="template-and-tasks"></a>Templat dan tugas

Untuk mengakses templat yang tersedia, dalam pusat pentadbiran Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.

Templat dan tugas asas berikut digunakan untuk menyegerakkan anggaran jam projek daripada Project Service Automation kepada Kewangan:

- **Nama templat dalam Integrasi data:** Anggaran jam projek (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:**

    - Hubungan transaksi
    - Anggaran perbelanjaan

### <a name="entity-set"></a>Set entiti

| Project Service Automation | Kewangan                                       |
|----------------------------|-----------------------------------------------|
| Tugas projek              | Entiti integrasi untuk anggaran jam projek |

### <a name="entity-flow"></a>Aliran entiti

Anggaran jam projek diuruskan dalam Project Service Automation dan ia disegerakkan kepada Kewangan sebagai ramalan jam projek.

### <a name="prerequisites"></a>Prasyarat

Sebelum penyegerakan anggaran jam projek boleh dijalankan, anda mesti menyegerakkan projek, tugas projek dan kategori transaksi perbelanjaan projek.

### <a name="power-query"></a>Pertanyaan Kuasa

Dalam templat anggaran jam projek, anda mesti menggunakan Microsoft Power Query for Excel untuk melengkapkan tugas ini:

- Tetapkan ID model ramalan lalai yang akan digunakan apabila integrasi mencipta ramalan jam baharu.
- Tapis keluar mana-mana rekod khusus sumber dalam tugas yang akan gagalkan integrasi ke dalam ramalan jam.
- Tapis keluar mana-mana baris kategori transaksi yang kosong. Kegagalan untuk melengkapkan tugas ini mungkin menghasilkan ramalan jam yang tidak betul.

#### <a name="set-the-default-forecast-model-id"></a>Tetapkan ID model ramalan lalai

Untuk mengemas kini ID model ramalan lalai dalam templat, klik anak panah **Peta** untuk membuka pemetaan. Kemudian pilih pautan **Pertanyaan Lanjutan dan Penapisan**.

- Jika anda menggunakan templat anggaran jam Projek lalai (PSA kepada Fin dan Ops), pilih **Syarat yang Dimasukkan** dalam senarai **Langkah Digunakan**. Dalam entri **Fungsi**, gantikan **O\_forecast** dengan nama ID model ramalan yang harus digunakan dengan integrasi. Templat lalai mempunyai ID model ramalan daripada data demo.
- Jika anda mencipta templat baharu, anda mesti menambah lajur ini. Dalam Power Query, pilih **Tambah Lajur Bersyarat**, dan masukkan nama untuk lajur baharu, seperti **ModelID**. Masukkan syarat untuk lajur, di mana, jika tugas Projek bukan nol, maka \<enter the forecast model ID\>; jika tidak nol.

#### <a name="filter-out-resource-specific-records"></a>Tapis keluar rekod khusus sumber

Templat anggaran jam Projek (PSA kepada Fin dan Ops) mempunyai penapis lalai yang mengalih keluar apa-apa rekod khusus sumber. Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini. Pilih pautan **Pertanyaan Lanjutan dan Penapisan** untuk menapis pada lajur **msdyn\_islinetask** supaya hanya rekod **Salah** disertakan.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tapis keluar baris kategori transaksi yang kosong

Anda mesti menambah penapis untuk mengalih keluar mana-mana baris yang mempunyai kategori transaksi yang kosong. Tugas ini diperlukan, tanpa mengira sama ada anda menggunakan templat lalai atau mencipta templat anda sendiri. Penapis ini mengalih keluar mana-mana baris ringkasan daripada Project Service Automation yang mungkin menyebabkan ramalan jam dalam Kewangan menjadi tidak betul. Pilih pautan **Pertanyaan Lanjutan dan Penapisan** untuk menapis keluar rekod nol dalam lajur **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan tugas templat dalam integrasi data.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Anggaran perbelanjaan projek

### <a name="template-and-tasks"></a>Templat dan tugas

Templat dan tugas asas berikut digunakan untuk menyegerakkan anggaran perbelanjaan projek daripada Project Service Automation kepada Kewangan:

- **Nama templat dalam Integrasi data:** Anggaran perbelanjaan projek (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:**

    - Hubungan transaksi 
    - Anggaran perbelanjaan

### <a name="entity-set"></a>Set entiti

| Project Service Automation | Kewangan                                                  |
|----------------------------|----------------------------------------------------------|
| Sambungan Transaksi    | Entiti integrasi untuk hubungan transaksi projek |
| Garisan Anggaran             | Entiti integrasi untuk anggaran perbelanjaan projek         |

### <a name="entity-flow"></a>Aliran entiti

Anggaran perbelanjaan projek diuruskan dalam Project Service Automation dan ia disegerakkan kepada Kewangan sebagai ramalan perbelanjaan projek.

### <a name="prerequisites"></a>Prasyarat

Sebelum penyegerakan anggaran perbelanjaan projek boleh dijalankan, anda mesti menyegerakkan projek, tugas projek dan kategori transaksi perbelanjaan projek.

### <a name="power-query"></a>Pertanyaan Kuasa

Dalam templat anggaran perbelanjaan projek, anda mesti menggunakan Power Query untuk melengkapkan tugas berikut:

- Penapis untuk hanya menyertakan rekod baris anggaran perbelanjaan.
- Tetapkan ID model ramalan lalai yang akan digunakan apabila integrasi mencipta ramalan jam baharu.
- Mengubah jenis pengebilan.
- Mengubah jenis transaksi.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Penapis untuk hanya menyertakan baris anggaran perbelanjaan

Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) mempunyai penapis lalai yang hanya menyertakan baris perbelanjaan dalam integrasi. Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini. Pilih tugas **Hubungan transaksi**, dan kemudian klik anak panah **Peta** untuk membuka pemetaan. Pilih pautan **Pertanyaan Lanjutan dan Penapisan**. Tapis lajur **msdyn\_transactiontype1** supaya ia hanya menyertakan **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Tetapkan ID model ramalan lalai

Untuk mengemas kini ID model ramalan lalai dalam templat, pilih tugas **Anggaran perbelanjaan**, dan kemudian klik anak panah **Peta** untuk membuka pemetaan. Pilih pautan **Pertanyaan Lanjutan dan Penapisan**.

- Jika anda menggunakan templat anggaran perbelanjaan Projek lalai (PSA kepada Fin dan Ops), dalam Power Query, pilih **Syarat yang Dimasukkan** pertama daripada bahagian **Langkah Digunakan**. Dalam entri **Fungsi**, gantikan **O\_forecast** dengan nama ID model ramalan yang harus digunakan dengan integrasi. Templat lalai mempunyai ID model ramalan daripada data demo.
- Jika anda mencipta templat baharu, anda mesti menambah lajur ini. Dalam Power Query, pilih **Tambah Lajur Bersyarat**, dan masukkan nama untuk lajur baharu, seperti **ModelID**. Masukkan syarat untuk lajur, di mana, jika ID baris Anggaran bukan nol, maka \<enter the forecast model ID\>; jika tidak nol.

#### <a name="transform-the-billing-types"></a>Mengubah jenis pengebilan

Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) termasuk lajur bersyarat yang digunakan untuk mengubah jenis pengebilan yang diterima daripada Project Service Automation semasa integrasi. Jika anda mencipta templat anda sendiri, anda mesti menambah lajur bersyarat ini. Pilih pautan **Pertanyaan Lanjutan dan Penapisan** dan kemudian pilih **Tambah Lajur Bersyarat**. Masukkan nama untuk lajur baharu, seperti **BillingType**. Kemudian masukkan syarat berikut:

Jika **msdyn\_billingtype** = 192350000, maka **NonChargeable**  
jika tidak, jika **msdyn\_billingtype** = 192350001, maka **Chargeable**  
jika tidak, jika **msdyn\_billingtype** = 192350002, maka **Complimentary**  
jika tidak, **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Mengubah jenis transaksi

Templat anggaran perbelanjaan Projek (PSA kepada Fin dan Ops) termasuk lajur bersyarat yang digunakan untuk mengubah jenis transaksi yang diterima daripada Project Service Automation semasa integrasi. Jika anda mencipta templat anda sendiri, anda mesti menambah lajur bersyarat ini. Pilih pautan **Pertanyaan Lanjutan dan Penapisan** dan kemudian pilih **Tambah Lajur Bersyarat**. Masukkan nama untuk lajur baharu, seperti **TransactionType**. Kemudian masukkan syarat berikut:

Jika **msdyn\_transactiontypecode** = 192350000, maka **Cost**  
jika tidak, jika **msdyn\_transactiontypecode** = 192350005, maka **Sales**  
jika tidak, **null**

### <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi yang berikut menunjukkan contoh pemetaan tugas templat dalam integrasi Data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat transaksi anggaran perbelanjaan.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Pemetaan templat anggaran perbelanjaan.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]