---
title: Peruntukan persekitaran baharu
description: Topik ini memberikan maklumat tentang cara menyediakan persekitaran Operasi Projek baru.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949373"
---
# <a name="provision-a-new-environment"></a>Peruntukan persekitaran baharu

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini memberikan maklumat mengenai cara untuk menyediakan persekitaran Operasi Projek Dynamics 365 baru untuk senario berasaskan sumber/bukan stok.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Dayakan peruntukan automatik Operasi Projek dalam projek LCS

Gunakan langkah berikut untuk mendayakan aliran peruntukan automatik Operasi Projek untuk projek LCS anda.

1. Pergi ke [LCS](https://lcs.dynamics.com/v2) dan pilih jubin **Pengurusan ciri pratonton**.
2. Dalam senarai **Ciri pratonton**, pilih **Operasi Projek** dan pilih **Ciri pratonton didayakan** untuk mendayakan Operasi Projek.

> [!NOTE]
> Langkah ini dilaksanakan hanya satu kali bagi setiap projek LCS.

## <a name="provision-a-project-operations-environment"></a>Menyediakan persekitaran Operasi Projek

1. Buka Dynamics 365 Finance [persekitaran demo baharu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) atau pelaksanaan [persekitaran pengeluaran/bukan pengeluaran bersama](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Ikuti wizard **Peruntukan persekitaran**. 

> [!IMPORTANT]
> Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.

3. Untuk memperuntukkan Operasi Projek, di bawah **Tetapan awal**, pilih **Common Data Service**. 
4. Dayakan Tetapan **Common Data Service** dengan memilih **Ya** dan kemudian masukkan maklumat dalam medan yang diperlukan:

  - Nama
  - Rantau
  - Bahasa
  - Mata wang
 
5. Dalam medan Templat **Common Data Service**, pilih **Operasi Projek** 

6. Pilih jenis persekitaran untuk pelaksanaan anda. Percubaan berasaskan langganan membolehkan anda melaksanakan persekitaran CDS selama 30 hari. 

![Tetapan Pelaksanaan](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Pilih **Setuju** untuk mengakui terma perkhidmatan dan kemudian pilih **Selesai** untuk kembali ke tetapan pelaksanaan.

![Persetujuan Pelaksanaan](./media/2DeploymentConsent.png)

7. Lengkapkan baki medan yang diperlukan dalam wizard dan sahkan pelaksanaan. Masa peruntukan persekitaran berbeza mengikut jenis persekitaran. Peruntukan mungkin mengambil masa sehingga enam jam.

  Selepas pelaksanaan berjaya diselesaikan, persekitaran akan ditunjukkan seperti yang **Dilaksanakan**.

8. Untuk mengesahkan persekitaran yang berjaya dilaksanakan, pilih **Log Masuk** dan log pada persekitaran untuk mengesahkan.

![Butiran Persekitaran](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Mohon data demo Kewangan Operasi Projek (langkah pilihan)

Mohon data demo Kewangan Operasi Projek ke Persekitaran Berhos Awan keluaran perkhidmatan 10.0.13 seperti yang diterangkan dalam [artikel ini](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Gunakan kemas kini kepada persekitaran kewangan

Operasi Projek memerlukan persekitaran kewangan dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.

Anda mungkin perlu menggunakan kemas kini kualiti kepada persekitaran kewangan anda untuk menerima versi ini.

1. Dalam LCS, pada halaman **Butiran persekitaran**, dalam bahagian **Kemas Kini Tersedia**, pilih **Lihat Kemas Kini**.

![Lihat Kemas Kini](./media/5ViewUpdates.png)

2. Pada halaman **Kemas kini Penduaan**, pilih **Simpan pakej.**

![Simpan pakej](./media/6SavePackage.png)

3. Klik **Pilih semua** dan kemudian **Simpan pakej**.

![Semak dan simpan kemas kini](./media/7ReviewAndSaveUpdates.png)

4. Masukkan nama dan perihalan pakej, dan kemudian pilih **Simpan**. Proses ini mungkin mengambil sedikit masa bergantung pada sambungan internet.

![Muat naik pakej ke Perpustakaan Aset](./media/8UploadPackageToAssetsLibrary.png)

5. Selepas pakej disimpan, pilih **Selesai** dan simpan pakej ini ke Perpustakaan Aset dalam projek LCS anda.

Menyimpan dan mengesahkan pakej mungkin mengambil masa ~ 15 minit.

6. Untuk menggunakan kemas kini, navigasi ke halaman **Butiran persekitaran** dalam LCS dan pilih **Kekalkan** > **Gunakan kemas kini**.

![Kekalkan Persekitaran](./media/9MaintainEnvironment.png)

7. Dalam senarai kemas kini pilih pakej yang anda cipta dan pilih **Gunakan**.

![Gunakan Kemas Kini](./media/10ApplyUpdates.png)

Perkhidmatan persekitaran akan mengambil sedikit masa. Selepas selesai, persekitaran akan kembali ke keadaan yang dilaksanakan.

![Laksanakan Persekitaran](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Wujudkan sambungan Dual Write 

1. Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.
2. Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautan ke CDS untuk Aplikasi**.
3. Selepas pautan selesai, pilih **Pautkan ke CDS untuk Aplikasi** semula. Anda akan dihalakan semula ke Dual Write dalam kewangan.

![Pautkan ke CDS](./media/12LinktoCDS.png)

4. Pilih **Gunakan Penyelesaian** untuk mengakses entiti yang akan dipetakan dalam integrasi.

![Gunakan Penyelesaian](./media/13ApplySolutions.png)

5. Pilih kedua-dua penyelesaian, Peta Entiti Dual Write **Dynamics 365 Finance and Operations** dan **Peta Entiti Dual Write Operasi Projek Dynamics 365**, dan kemudian pilih **Gunakan**.

![Sahkan Penyelesaian](./media/14ConfirmSolutions.png)

Selepas penyelesaian digunakan, entiti Dual Write digunakan untuk persekitaran.

![Gunakan Penyelesaian](./media/15ApplyingSolutions.png)

Selepas entiti digunakan, semua pemetaan yang sedia ada disenaraikan dalam persekitaran.

![Peta Dual Write](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Segar semula entiti data selepas kemas kini

1. Dalam Kewangan, pergi ke ruang kerja **Pengurusan data**.

![Ruang kerja Pengurusan Data](./media/16DataManagement.png)

2. Pilih jubin **Parameter rangka kerja**.

![Parameter Rangka Kerja](./media/17FrameworkParameters.png)

3. Pada halaman **Tetapan entiti**, pilih senarai **Entiti Segar Semula**.

![Senarai Entiti Segar Semula](./media/18RefreshEntityList.png)

Segar semula akan mengambil masa kira-kira 20 minit. Anda akan menerima isyarat apabila ia selesai.

![Pengesahan Segar Semula](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Jalankan peta Dual Write Operasi Projek

1. Dalam projek LCS anda, pergi ke halaman **Butiran persekitaran**.
2. Di bawah Maklumat Persekitaran **Common Data Service**, pilih **Pautkan ke CDS untuk Aplikasi.** Selepas anda memilih pautan tersebut, anda akan dihalakan semula ke senarai entiti dalam pemetaan.
3. Mulakan peta seperti yang diterangkan dalam jadual berikut. Pastikan anda mengikuti urutan seperti yang disenaraikan.

| **Peta Entiti** | **Entiti segar semula** | **Penyegerakan awal** | **Induk untuk penyegerakan awal** | **Jalankan prasyarat:** | **Segerakkan permulaan prasyarat** |
| --- | --- | --- | --- | --- | --- |
| **Peranan Sumber Projek untuk Semua Syarikat (bookableresourcecategories)** | Tidak | Ya | Common Data Service | Tidak | T\A |
| **Entiti sah (cdm\_syarikat)** | Tidak | Ya | Aplikasi Finance and Operations | Tidak | T\A |
| **Aktual integrasi Operasi Projek (msdyn\_aktual)** | Tidak | Tidak | T\A | Ya | Tidak |
| **Baris kontrak projek (salesorderdetails)** | Tidak | Tidak | T\A | Tidak | Tidak |
| **Entiti integrasi untuk hubungan transaksi projek (msdyn\_transactionconnections)** | Tidak | Tidak | T\A | Tidak | T\A |
| **Pencapaian baris kontrak integrasi Operasi Projek (msdyn\_contractlinesscheduleofvalues)** | Tidak | Tidak | T\A | Tidak | T\A |
| **Entiti integrasi Operasi Projek untuk anggaran perbelanjaan (msdyn\_estimateslines)** | Tidak | Tidak | T\A | Tidak | T\A |
| **Entiti integrasi Operasi Projek untuk anggaran jam (msdyn\_estimateslines)** | Tidak | Tidak | T\A | Tidak | T\A |
| **Perbelanjaan projek integrasi Operasi Projek entiti eksport (msdyn\_perbelanjaan)** | Ya | Tidak | T\A | Tidak | T\A |
| **Entiti integrasi Operasi Projek untuk anggaran jam (msdyn\_estimateslines)** | Ya | Tidak | T\A | Tidak | T\A |

4. Untuk menyegarkan semula entiti, pilih nama peta dan kemudian pilih **Segar semula entiti**. 
5. Teruskan dengan menjalankan peta selepas segar semula selesai.

![Segar Semula Peta](./media/20RefreshMapping.png)

Sebelum anda mendayakan peta seterusnya, sahkan bahawa peta dalam jadual dalam keadaan **Berjalan**. Jalankan peta dengan bilangan prasyarat yang lebih besar mungkin mengambil sedikit masa.

Untuk menjalankan peta dengan prasyarat, dayakan togol **Tunjukkan peta entiti berkaitan**. Jika jadual menunjukkan **Penyegerakkan awal pra-syarat** **Tidak**, sahkan bahawa bendera **Penyegerakkan awal** **Dipadamkan** dalam semua peta pra-syarat sebelum anda menjalankannya.

![Jalankan Peta](./media/21RunMap.png)

6. Mengesahkan semua peta berkaitan projek adalah dalam keadaan berjalan.

![Semua Peta Berjalan](./media/22AllMapsRunning.png)

Persekitaran Operasi Projek anda kini diperuntukkan dan dikonfigurasikan.
