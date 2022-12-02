---
title: Pindahkan pencapaian pengebilan invois penuh pada pemotongan
description: Artikel ini menerangkan cara memindahkan pencapaian pengebilan berharga tetap yang telah diinvois kepada pelanggan untuk kontrak projek terbuka sebelum tarikh mula beroperasi.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Pindahkan pencapaian pengebilan invois penuh pada pemotongan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="scenario"></a>Senario

Contoso akan bersiaran langsung dengan Microsoft Dynamics 365 Project Operations untuk senario sumber/bukan stok. Sebagai sebahagian daripada aktiviti pemotongan yang dijalankan, pasukan pelaksanaan mesti memindahkan kontrak projek terbuka daripada sistem lama. Sesetengah kontrak projek termasuk baris kontrak yang menggunakan kaedah pengebilan berharga tetap dan telah diinvoiskan separa kepada pelanggan akhir. Pasukan pelaksanaan mesti memindahkan pencapaian pengebilan ini sebagai **Invois pelanggan disiarkan**, kerana ia mesti dimasukkan dalam jumlah nilai kontrak untuk tujuan pengiktirafan hasil. Walau bagaimanapun, baki pelanggan dalam Akaun belum terima dan Lejar umum tidak boleh terjejas.

## <a name="solution"></a>Penyelesaian

### <a name="prerequisites"></a>Prasyarat

- Dynamics 365 Finance 10.0.24 atau lebih baharu mesti dipasang.
- Persekitaran tempat langkah pemindahan akan dilengkapkan mesti berada dalam mod penyelenggaraan. Tiada aktiviti lain yang patut dilakukan ketika pencapaian sedang dipindahkan.
- Langkah pemindahan mesti diikuti dengan tepat seperti yang diterangkan di sini dan hanya boleh digunakan untuk aktiviti pemotongan. Microsoft tidak menyokong penggunaan lain keupayaan ini.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Cipta versi pemotongan peta dwitulis pencapaian baris kontrak integrasi Project Operations 

1. Pastikan pemetaan sasaran bagi entiti **pencapaian baris kontrak integrasi Project Operations** adalah terkini. 

    1. Dalam Finance, pergi ke **Pengurusan Data** \> **Entiti data** dan pilih entiti **pencapaian baris kontrak integrasi Project Operations**. 
    2. Pilih **Ubah suai pemetaan sasaran**. 
    3. Pada halaman **Pemeringkatan peta kepada sasaran**, pilih **Jana pemetaan** dan kemudian sahkan bahawa anda mahu menjana pemetaan.

2. Berhenti dan segar semula peta dwitulis **pencapaian baris kontrak integrasi Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Pergi ke **Pengurusan data** \> **Dwitulis**, pilih peta dan buka butirannya. 
    2. Pilih **Berhenti** dan tunggu sehingga sistem menghentikan peta. 
    3. Pilih **Segar semula jadual**.

3. Tambah pemetaan untuk status transaksi.

    1. Pilih **Tambah pemetaan**.
    2. Pada baris baharu, dalam lajur **Aplikasi kewangan dan operasi**, pilih medan **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Dalam lajur **Microsoft Dataverse**, pilih **msdyn\_invoicestatus \[Status invois\]**.
    4. Dalam lajur **Jenis peta**, pilih anak panah kanan (**\>**).
    5. Dalam kotak dialog yang muncul, dalam medan **Arah penyegerakan**, pilih **Dataverse ke aplikasi Kewangan dan Operasi**.
    6. Pilih **Tambah transformasi**.
    7. Dalam medan **Jenis transformasi**, pilih **ValueMap**.
    8. Pilih **Tambah pemetaan nilai**.
    9. Dalam medan kiri, masukkan **4**. Dalam medan kanan, masukkan **192350001**. 
    10. Pilih **Simpan** dan kemudian tutup kotak dialog.

4. Pilih **Simpan sebagai** untuk menyimpan versi peta dwitulis. 
5. Dalam anak tetingkap **Tambah jadual**, dalam medan **Penerbit**, pilih **Penerbit lalai**.
6. Dalam medan **Versi**, masukkan versi.
7. Dalam medan **Perihalan**, masukkan nota tentang versi pemotongan peta ini. 
8. Pilih **Simpan**.
9. Mulakan peta.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Pindahkan pencapaian diinvoiskan ke persekitaran Dataverse

1. Dalam persekitaran Dataverse Project Operations, cipta pencapaian yang mempunyai status invois **Redia untuk penginvoisan**. Pada masa ini, jangan pindahkan apa-apa pencapaian yang belum diinvoiskan.

    > [!NOTE]
    > Sebelum anda memindahkan pencapaian pengebilan, pastikan bahawa dimensi kewangan yang berkaitan dengan baris kontrak projek ditetapkan seperti yang dijangkakan. Dimensi kewangan tidak boleh diedit selepas pemindahan selesai.

2. Selepas semua pencapaian dipindahkan, hentikan peta dwitulis berikut:

    - Pencapaian baris kontrak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)
    - Aktual integrasi Project Operations (msdyn\_actuals)
    - Cadangan invois projek V2 (invois)

    Untuk menghentikan peta, ikut langkah ini:

    1. Dalam Finance, pergi ke **Pengurusan data** \> **Dwitulis**, pilih satu peta dan buka butirannya.
    2. Pilih **Berhenti** dan tunggu sehingga sistem menghentikan peta.

3. Dalam persekitaran Dataverse Project Operations, cipta dan sahkan invois proforma untuk pencapaian pengebilan. 

    1. Dalam peta tapak, pergi ke kontrak projek, pilih kontrak dan kemudian pilih **Cipta invois**.
    2. Selepas invois dicipta, buka invois daripada menu **Invois** dalam peta tapak dan kemudian pilih **Sahkan**.

    Langkah ini mencipta rekod yang diperlukan dalam persekitaran Dataverse. Walau bagaimanapun, ia tidak menjejaskan kewangan dan akaun belum terima kerana peta dwitulis disenaraikan sebelumnya telah dihentikan.

4. Selepas semua invois proforma disahkan, kembalikan semua peta dwitulis kepada keadaan awal mereka.

    1. Kemas kini versi peta dwitulis **pencapaian baris kontrak integrasi Project Operations** (**msdyn\_contractlinescheduleofvalues**) kembali ke versi asal. 
    2. Pilih peta dwitulis dalam senarai peta, pilih **Versi peta jadual** dan kemudian pilih versi asal peta jadual.
    3. Pilih **Simpan**.
    4. Mulakan semula peta dwitulis berikut:

        - Pencapaian baris kontrak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)
        - Aktual integrasi Project Operations (msdyn\_actuals)
        - Cadangan invois projek V2 (invois)

Pencapaian kini dipindahkan, dan sistem bersedia untuk langkah seterusnya dalam aktiviti pemotongan.
