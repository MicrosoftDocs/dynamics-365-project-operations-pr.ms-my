---
title: Segerakkan sebenar projek terus dari Automasi Perkhidmatan Projek ke jurnal integrasi projek untuk pengeposan dalam Kewangan dan Operasi
description: Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan sebenar projek terus dari Microsoft Dynamics 365 Project Service Automation ke Kewangan dan Operasi.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7d912a11d9c7bc66ed43911ee32f25092d551cd6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929501"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Segerakkan sebenar projek terus dari Automasi Perkhidmatan Projek ke jurnal integrasi projek untuk pengeposan dalam Kewangan dan Operasi

[!include[banner](../includes/banner.md)]

Artikel ini menerangkan templat dan tugas asas yang digunakan untuk menyegerakkan sebenar projek terus dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.

Templat menyegerakkan transaksi daripada Project Service Automation kepada jadual pemeringkatan dalam Finance. Selepas penyegerakan selesai, anda **mesti** mengimport data daripada jadual pemeringkatan ke dalam jurnal integrasi.

> [!NOTE]
> - Integrasi aktual projek tersedia bermula dalam versi 8.0.1.
> - Jika anda menggunakan Enterprise Edition 7.3.0 selepas anda memasang KB 4132657 dan KB 4132660, anda akan dapat menggunakan templat untuk mengintegrasikan tugas projek, kategori transaksi perbelanjaan, anggaran jam, anggaran perbelanjaan dan aktual serta untuk mengkonfigurasi fungsi penguncian. Jika anda mesti tetapkan semula pengedaran perakaunan, kami mengesyorkan agar anda juga memasang KB 4131710.
> - Jika anda menggunakan versi 7.3.0 dan anda sedang membawa transaksi yuran daripada Project Service Automation, anda mesti memasang KB 4345320 untuk memasukkan yuran tersebut dalam invois projek.
> - Jika anda memasukkan jumlah cukai jualan pada transaksi masa atau perbelanjaan dalam Project Service Automation, anda mesti memasang Kemas kini 7 Project Service Automation. Jika tidak, aktual cukai tidak akan dipautkan kepada aktual masa atau perbelanjaan yang berkaitan, dan ia tidak akan disegerakkan kepada Finance. Untuk maklumat lebih lanjut, hubungi Sokongan.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation kepada Finance

Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat integrasi yang tersedia dengan ciri integrasi Data mendayakan aliran data tentang aktual projek daripada Project Service Automation kepada Finance.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Automasi Perkhidmatan Projek dengan Kewangan dan Operasi.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Aktual projek daripada Project Service Automation

### <a name="template-and-tasks"></a>Templat dan tugas

Untuk mengakses templat yang tersedia, dalam pusat pentadbiran Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.

Templat dan tugas dasar berikut digunakan untuk segerakkan aktual projek daripada Project Service Automation kepada Finance:

- **Nama templat dalam integrasi Data:** Aktual projek (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:**

    - Aktual
    - TransactionConnections

### <a name="entity-set"></a>Set entiti

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Aktual                    | Entiti integrasi untuk aktual projek                   |
| Sambungan Transaksi    | Entiti integrasi untuk hubungan transaksi projek |

### <a name="entity-flow"></a>Aliran entiti

Aktual projek diuruskan dalam Project Service Automation, dan ia disegerakkan kepada jurnal integrasi projek dalam Finance. Perakaunan akan digunakan berdasarkan dimensi kewangan lalai dan persediaan penyiaran.

### <a name="prerequisites"></a>Prasyarat

Sebelum penyegerakan aktual boleh berlaku, anda mesti mengkonfigurasikan parameter integrasi Project Service Automation dan menyegerakkan projek, tugas projek serta kategori transaksi perbelanjaan projek.

### <a name="power-query"></a>Power Query

Dalam templat sebenar projek, anda mesti menggunakan Microsoft Power Query for Excel untuk melengkapkan tugas ini:

- Mengubah jenis transaksi dalam Project Service Automation kepada jenis transaksi yang betul dalam Finance. Perubahan ini telah ditakrifkan dalam templat Aktual projek (PSA kepada Fin dan Ops).
- Mengubah jenis pengebilan dalam Project Service Automation kepada jenis pengebilan yang betul dalam Finance. Perubahan ini telah ditakrifkan dalam templat Aktual projek (PSA kepada Fin dan Ops). Jenis pengebilan kemudian dipetakan kepada sifat baris, berdasarkan konfigurasi pada halaman **parameter integrasi Project Service Automation**.
- Tapis kepada unit organisasi sumber khusus yang mesti disegerakkan dengan templat ini.
- Jika aktual masa antara syarikat atau perbelanjaan antara syarikat akan disegerakkan kepada Finance, anda mesti mengubah unit organisasi kontrak kepada entiti undang-undang yang betul dalam Finance. Dalam templat Aktual projek (PSA kepada Fin dan Ops), lajur bersyarat ditakrifkan berdasarkan data demo. Anda mesti mengemas kini lajur bersyarat yang terakhir dimasukkan kepada entiti undang-undang yang betul. Jika tidak, sama ada ralat integrasi mungkin berlaku, atau transaksi aktual yang salah mungkin diimport ke dalam Finance.
- Jika aktual masa antara syarikat atau perbelanjaan antara syarikat tidak akan disegerakkan kepada Finance, anda mesti memadamkan lajur bersyarat yang terakhir dimasukkan daripada templat anda. Jika tidak, sama ada ralat integrasi mungkin berlaku, atau transaksi aktual yang salah mungkin diimport ke dalam Finance.

#### <a name="contract-organizational-unit"></a>Unit organisasi kontrak
Untuk mengemas kini lajur bersyarat yang dimasukkan dalam templat, klik anak panah **Peta** untuk membuka pemetaan. **Pilih pautan Pertanyaan Lanjutan dan Penapisan** untuk dibuka Power Query.

- Jika anda menggunakan templat sebenar Projek lalai (PSA hingga Fin dan Ops), dalam Power Query, pilih Keadaan **Dimasukkan terakhir** daripada **seksyen Langkah** Gunaan. Dalam entri **Fungsi**, gantikan **USSI** dengan nama entiti undang-undang yang harus digunakan dengan integrasi. Tambah syarat tambahan pada entri **Fungsi** yang anda perlukan, dan kemas kini keadaan **lain** daripada **USMF** kepada entiti undang-undang yang betul.
- Jika anda mencipta templat baharu, anda mesti menambah lajur untuk menyokong masa dan perbelanjaan antara syarikat. Pilih **Tambah Lajur Bersyarat**, dan masukkan nama untuk lajur, seperti **LegalEntity**. Masukkan syarat untuk lajur, di mana, jika **msdyn\_contractorganizationalunitid.msdyn\_nama** adalah \<organizational unit\>, kemudian \<enter the legal entity\>; jika tidak nol.

### <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi berikut menunjukkan contoh pemetaan tugas templat dalam Integrasi data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat - Aktual.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Pemetaan template - Sambungan transaksi.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Import daripada jadual pemeringkatan selepas integrasi daripada Project Service Automation

Proses berkala Import daripada jadual pemeringkatan mesti dijalankan selepas penyegerakan aktual daripada Project Service Automation kepada Finance. Proses ini akan mengimport transaksi projek daripada jadual pemeringkatan kepada jurnal integrasi Project Service Automation, di mana perakaunan digunakan dan transaksi yang diimport dapat disiarkan. Kami mengesyorkan agar anda menjalankan proses ini dalam mod kelompok; ia boleh ditetapkan secara pilihan untuk berjalan sebagai kelompok yang berulang.

## <a name="update-actuals-from-finance"></a>Kemas kini aktual daripada Finance

### <a name="template-and-tasks"></a>Templat dan tugas

Templat dan tugas asas berikut digunakan untuk menyegerakkan nombor baucar dan cukai jualan bagi transaksi projek yang disiarkan daripada Finance kepada Project Service Automation:

- **Nama templat dalam Integrasi data:** Kemas kini aktual projek (Fin Ops kepada PSA)
- **Nama tugas dalam projek:**

    - Aktual 
    - TransactionConnections

### <a name="entity-set"></a>Set entiti

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entiti integrasi untuk aktual projek                   | Aktual                    |
| Entiti integrasi untuk hubungan transaksi projek | Sambungan Transaksi    |

### <a name="entity-flow"></a>Aliran entiti

Aktual projek diuruskan dalam Project Service Automation, dan ia disegerakkan kepada jurnal integrasi projek dalam Finance. Selepas aktual disiarkan dalam Finance, ia dikemas kini dalam Project Service Automation dengan nombor baucar daripada Finance. Jika cukai jualan telah ditambah dalam Finance, aktual cukai baharu dicipta dalam Project Service Automation.

### <a name="power-query"></a>Power Query

Dalam templat kemas kini sebenar projek, anda mesti gunakan Power Query untuk melengkapkan tugas ini:

- Mengubah jenis transaksi dalam Finance kepada jenis transaksi yang betul dalam Project Service Automation. Perubahan ini telah ditakrifkan dalam templat kemas kini Aktual projek (Fin Ops kepada PSA).
- Mengubah jenis pengebilan dalam Finance kepada jenis pengebilan yang betul dalam Project Service Automation. Perubahan ini telah ditakrifkan dalam templat kemas kini Aktual projek (Fin Ops kepada PSA).

### <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

Ilustrasi yang berikut menunjukkan contoh pemetaan tugas templat dalam integrasi Data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Finance kepada Project Service Automation.

[![Pemetaan templat - kemas kini Aktual.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Pemetaan templat - kemas kini Transaksi.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]