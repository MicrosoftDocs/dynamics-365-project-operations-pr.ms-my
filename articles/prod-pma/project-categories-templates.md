---
title: Menyegerakkan kategori perbelanjaan projek antara Kewangan dan Operasi dan Automasi Perkhidmatan Projek
description: Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan kategori perbelanjaan projek antara Microsoft Dynamics 365 Kewangan dan Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 630c4fa7a159aa46b46984736080cd007d519a6c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927247"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Menyegerakkan kategori perbelanjaan projek antara Kewangan dan Operasi dan Automasi Perkhidmatan Projek

[!include[banner](../includes/banner.md)]

Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan kategori perbelanjaan projek antara Dynamics 365 Finance dan Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integrasi tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan penguncian fungsi tersedia dalam versi 8.0.
> - Integrasi aktual tersedia dalam versi 8.0.1 atau kemudian.
> - Jika anda menggunakan Enterprise Edition 7.3.0, selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian. Jika anda mesti tetapkan semula pengedaran perakaunan, kami mengesyorkan agar anda juga memasang KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Aliran data untuk Project Service Automation dan Finance

Penyelesaian integrasi Project Service Automation dan Finance menggunakan ciri Integrasi data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat integrasi yang tersedia dengan ciri Integrasi data mendayakan aliran data tentang kategori transaksi perbelanjaan projek antara Finance dan Project Service Automation.

Jika kategori perbelanjaan projek dikuasai dalam Finance, aliran integrasi adalah mulanya daripada Finance kepada Project Service Automation. ID integrasi kategori perbelanjaan projek kemudian dikemas kini melalui penyegerakan daripada Project Service Automation kepada Finance.

Jika kategori perbelanjaan projek dikuasai dalam Project Service Automation, aliran integrasi adalah mulanya daripada Project Service Automation kepada Finance. Kategori projek mesti telah dikonfigurasikan dalam Finance sebelum penyegerakan daripada Project Service Automation. Kemudian segerakkan daripada Finance kembali kepada Project Service Automation, dan kemudian segerakkan daripada Project Service Automation kepada Finance semula. Dengan cara ini, anda membantu menjamin bahawa kategori telah dipautkan dan tiada pendua dihasilkan.

> [!NOTE]
> Lazimnya, kategori perbelanjaan projek dikuasai dalam Finance. Walau bagaimanapun, jika ia tidak dikuasai dalam Finance, atau jika kategori perbelanjaan telah dicipta dalam Project Service Automation, anda mesti segerakkan terlebih dahulu dengan menggunakan templat Kategori transaksi perbelanjaan projek (PSA kepada Fin dan Ops). Kemudian segerakkan dengan menggunakan templat Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA). Kemudian anda perlu menjalankan penyegerakan daripada Project Service Automation kepada Finance sekali lagi.
>
> Jika anda menyegerakkan dahulu daripada Project Service Automation, keperluan berikut mesti dipenuhi dalam Finance sebelum penyegerakan dijalankan:
>
> - Kategori dikongsi yang sepadan dengan kategori projek yang ditetapkan dalam Project Service Automation mesti wujud dan ia mesti didayakan untuk **Projek** dan **Perbelanjaan**.
> - Bagi setiap entiti undang-undang Finance yang mesti diintegrasikan dengannya, kategori projek berikut mesti wujud:
>
>     - **Kategori projek** wujud. 
>     - **Penggunaan dalam Perbelanjaan** didayakan.
>     - **Aktif dalam jurnal** didayakan.
>     - **Jenis transaksi** ditetapkan kepada **Perbelanjaan**.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Kewangan.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Penyegerakan kategori perbelanjaan projek daripada Finance kepada Project Service Automation

### <a name="template-and-task"></a>Templat dan tugas

Untuk mengakses templat, dalam pusat pentadbir Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.

Templat dan tugas asas berikut digunakan untuk menyegerakkan kategori perbelanjaan projek daripada Finance kepada Project Service Automation:

- **Nama templat dalam Integrasi data:** Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA)
- **Nama tugas dalam projek:** Segerakkan kategori kepada PSA

### <a name="entity-set"></a>Set entiti

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entiti integrasi untuk kategori | Kategori transaksi     |

### <a name="entity-flow"></a>Aliran entiti

Kategori perbelanjaan projek dikendalikan dalam Finance, dan disegerakkan kepada Project Service Automation sebagai kategori transaksi.

### <a name="power-query"></a>Power Query

Apabila anda menyegerakkan ke Project Service Automation, anda mesti menggunakan Microsoft Power Query for Excel untuk mengesetkan jenis pengebilan pada kategori transaksi. Templat kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA) menyediakan lajur dan pemetaan lalai. Jika anda mencipta templat anda sendiri, anda mesti menambah lajur bersyarat dalam Power Query. Ikut langkah ini.

1. Klik anak panah untuk membuka pemetaan tugas kategori perbelanjaan projek dalam Kategori transaksi perbelanjaan projek (Fin dan Ops kepada PSA).
2. **Klik pautan Pertanyaan Pendahuluan dan Penapisan** untuk membuka Power Query.
2. Pilih **Tambah Lajur Bersyarat**.
3. Masukkan nama untuk lajur baharu, seperti **BillingType**.
4. Masukkan syarat berikut: **jika CATEGORYID tidak sama dengan nol, maka 19235001, Sebaliknya, nol**.
5. Klik **OK** pada lajur.
6. Pastikan anda memetakan lajur baharu ini pada halaman pemetaan.

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Finance kepada Project Service Automation.

[![Pemetaan templat Kategori perbelanjaan projek kepada Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Penyegerakan kategori perbelanjaan projek daripada Project Service Automation kepada Finance

### <a name="template-and-task"></a>Templat dan tugas

Templat dan tugas asas berikut digunakan untuk menyegerakkan kategori perbelanjaan projek daripada Project Service Automation kepada Finance:

- **Nama templat dalam Integrasi data:** Kategori transaksi perbelanjaan projek (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:** Segerakkan kategori kepada Fin Ops

### <a name="entity-set"></a>Set entiti

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Kategori transaksi     | Entiti integrasi untuk kategori |

### <a name="entity-flow"></a>Aliran entiti

Kategori perbelanjaan projek dikendalikan dalam Finance, dan disegerakkan kepada Project Service Automation sebagai kategori transaksi. Penyegerakan kembali kepada Finance mengemas kini kategori projek dalam Finance dengan ID integrasi daripada Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data.

> [!NOTE]
> Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat Project Service Automation kepada Kewangan.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]