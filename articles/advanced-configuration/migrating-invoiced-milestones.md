---
title: Pindahkan tonggak pengebilan yang diinvois sepenuhnya semasa pemotongan
description: Artikel ini menerangkan cara memindahkan tonggak pengebilan berharga tetap yang telah diinvois kepada pelanggan untuk kontrak projek terbuka sebelum tarikh langsung.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028713"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Pindahkan tonggak pengebilan yang diinvois sepenuhnya semasa pemotongan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="scenario"></a>Senario

Contoso akan disiarkan secara langsung dengan Microsoft Dynamics 365 Project Operations untuk senario sumber/bukan stok. Sebagai sebahagian daripada aktiviti pemotongan, pasukan pelaksana mesti memindahkan kontrak projek terbuka dari sistem lama. Beberapa kontrak projek termasuk garis kontrak yang menggunakan kaedah pengebilan harga tetap dan telah diinvois sebahagiannya kepada pelanggan akhir. Pasukan pelaksana mesti memindahkan tonggak pengebilan ini sebagai **invois Pelanggan yang disiarkan**, kerana ia mesti dimasukkan dalam jumlah nilai kontrak untuk tujuan pengiktirafan hasil. Walau bagaimanapun, baki pelanggan dalam Akaun belum terima dan lejar Am tidak boleh terjejas.

## <a name="solution"></a>Penyelesaian

### <a name="prerequisites"></a>Prasyarat

- Dynamics 365 Finance 10.0.24 atau lebih baru mesti dipasang.
- Persekitaran di mana langkah-langkah migrasi akan selesai mestilah dalam mod penyelenggaraan. Tiada aktiviti lain yang perlu dilakukan semasa peristiwa penting sedang dipindahkan.
- Langkah-langkah penghijrahan mesti diikuti seperti yang diterangkan di sini dan boleh digunakan hanya untuk aktiviti pemotongan. Microsoft tidak menyokong penggunaan lain keupayaan ini.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Cipta versi cutover bagi kontrak integrasi Project Operations baris tonggak dwi-tulis peta 

1. Pastikan pemetaan sasaran untuk **entiti tonggak** kontrak integrasi Project Operations adalah terkini. 

    1. Dalam Kewangan, pergi ke **entiti** Data Pengurusan \>**Data**, dan pilih **entiti tonggak** kontrak integrasi Operasi Projek. 
    2. Pilih **Ubah suai pemetaan** sasaran. 
    3. **Pada pementasan Peta ke halaman sasaran**, pilih **Jana pemetaan**, kemudian sahkan bahawa anda ingin menjana pemetaan.

2. Berhenti dan segar semula **tonggak** baris kontrak integrasi Project Operations (**msdyn\_ kontraklinescheduleofvalues**) peta dwi-tulis. 

    1. Pergi ke **Pengurusan** \> **data Dwi-tulis**, pilih peta dan buka butirannya. 
    2. Pilih **Berhenti**, dan tunggu sehingga sistem menghentikan peta. 
    3. Pilih **Segar semula jadual**.

3. Tambah pemetaan untuk status transaksi.

    1. Pilih **Tambah pemetaan**.
    2. Pada baris baharu, dalam **lajur Aplikasi** Kewangan dan Operasi, pilih **medan TRANSSTATUS \[TRANSSTATUS TRANSSTATUS\]**.
    3. **Microsoft Dataverse** Dalam lajur, pilih **status\_ Invois invois msdyn\[\]**.
    4. **Dalam lajur Jenis** peta, pilih anak panah kanan (**\>**).
    5. Dalam kotak dialog yang muncul, dalam **medan Arah** segerak, pilih **Dataverse kepada app** Kewangan dan Operasi.
    6. Pilih **Tambah transformasi**.
    7. **Dalam medan Jenis** Transform, pilih **ValueMap**.
    8. Pilih **Tambah pemetaan** nilai.
    9. Di medan kiri, masukkan **4**. Dalam medan kanan, masukkan **192350001**. 
    10. Pilih **Simpan**, kemudian tutup kotak dialog.

4. Pilih **Simpan untuk** menyimpan versi peta dwi-tulis. 
5. **Dalam anak tetingkap Tambah jadual**, dalam **medan Publisher**, pilih **Penerbit** lalai.
6. Dalam medan **Versi**, masukkan versi.
7. Dalam medan **Perihalan**, masukkan nota tentang versi potong peta ini. 
8. Pilih **Simpan**.
9. Mulakan peta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Pindahkan tonggak yang diinvois ke Dataverse persekitaran

1. Dalam persekitaran Operasi Dataverse Projek, cipta peristiwa penting yang mempunyai status **invois Sedia untuk invois**. Pada ketika ini, jangan memindahkan sebarang peristiwa penting yang belum diinvois.

    > [!NOTE]
    > Sebelum anda memindahkan tonggak pengebilan, pastikan dimensi kewangan yang berkaitan dengan garis kontrak projek ditetapkan seperti yang diharapkan. Dimensi kewangan tidak boleh diedit selepas migrasi selesai.

2. Selepas semua tonggak dipindahkan, hentikan peta dwi-tulis berikut:

    - Tonggak kontrak integrasi Project Operations (msdyn\_ contractlinescheduleofvalues)
    - Aktual integrasi Project Operations (msdyn\_actuals)
    - Cadangan invois projek V2 (invois)

    Untuk menghentikan peta, ikuti langkah berikut:

    1. Dalam Kewangan, pergi ke **Pengurusan** \> **data Dwi-tulis**, pilih peta, dan buka butirannya.
    2. Pilih **Berhenti**, dan tunggu sehingga sistem menghentikan peta.

3. Dalam persekitaran Operasi Dataverse Projek, cipta dan sahkan invois pro-forma untuk pencapaian pengebilan. 

    1. Dalam peta tapak, pergi ke kontrak projek, pilih kontrak, kemudian pilih **Buat invois**.
    2. Selepas invois dicipta, bukanya daripada **menu Invois** dalam peta tapak, kemudian pilih **Sahkan**.

    Langkah ini mencipta rekod yang diperlukan dalam Dataverse persekitaran. Walau bagaimanapun, ia tidak menjejaskan kewangan dan akaun belum terima, kerana peta dwi-tulis yang disenaraikan sebelum ini telah dihentikan.

4. Selepas semua invois pro-forma disahkan, kembalikan semua peta dwi-tulis ke keadaan awal mereka.

    1. Kemas kini versi **tonggak** baris kontrak integrasi Project Operations (**msdyn\_ kontraklinescheduleofvalues) dwi-tulis peta kembali kepada yang** asal. 
    2. Pilih peta dwi-tulis dalam senarai peta, pilih **Versi peta jadual**, kemudian pilih versi asal peta jadual.
    3. Pilih **Simpan**.
    4. Mulakan semula peta dwi-tulis berikut:

        - Tonggak kontrak integrasi Project Operations (msdyn\_ contractlinescheduleofvalues)
        - Aktual integrasi Project Operations (msdyn\_actuals)
        - Cadangan invois projek V2 (invois)

Tonggak kini dipindahkan, dan sistem bersedia untuk langkah seterusnya dalam aktiviti pemotongan.
