---
title: Gunakan data demo pada persekitaran berhos Awan Kewangan
description: Topik ini menerangkan cara menggunakan data demo daripada Operasi Projek kepada persekitaran yang dihoskan oleh Awan Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e4ccc7eb02fabdc0476fe454f33bff637ab8b835
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588977"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Gunakan data demo pada persekitaran berhos Awan Kewangan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

> [!IMPORTANT]
> Topik ini hanya boleh digunakan Microsoft Dynamics 365 Kewangan versi 10.0.13 dan boleh dilakukan hanya pada persekitaran yang dihoskan oleh Cloud. Lengkapkan langkah dalam topik ini **SEBELUM** anda menggunakan kemas kini kualiti kepada persekitaran.

1. Dalam projek LCS anda, buka halaman **Butiran persekitaran**. Perhatikan bahawa ia termasuk butiran yang diperlukan untuk menyambung ke persekitaran dengan menggunakan Protokol Desktop Jarak Jauh (RDP).

![Butiran Persekitaran.](./media/1EnvironmentDetails.png)

Set kelayakan pertama yang diserlahkan ialah kelayakan akaun tempatan dan mengandungi hiperpautan ke sambungan desktop jarak jauh. Kelayakan termasuk nama pengguna pentadbir persekitaran dan kata laluan. Set kedua kelayakan digunakan untuk log masuk ke Pelayan SQL dalam persekitaran ini.

2. Sambung kepada persekitaran oleh hiperpautan dalam **Akaun Tempatan** dan gunakan **Kelayakan Akaun Tempatan** untuk pengesahan.
3. Pergi ke **Perkhidmatan Maklumat Internet** > **Himpunan Aplikasi** > **PerkhidmatanAOS** dan menghentikan perkhidmatan. Anda akan menghentikan perkhidmatan pada masa ini supaya anda boleh terus menggantikan pangkalan data SQL.

![Hentikan AOS.](./media/2StopAOS.png)

4. Pergi ke **Perkhidmatan** dan hentikan dua item berikut:

- Microsoft Dynamics 365 Unified Operations: Perkhidmatan Pengurusan Kelompok
- Microsoft Dynamics 365 Unified Operations : Rangka Kerja Eksport Import Data

![Hentikan Perkhidmatan.](./media/3StopServices.png)

5. Buka Studio Pengurusan Microsoft SQL Server. Log masuk dengan kelayakan pelayan SQL dan gunakan pengguna axdbadmin dan kata laluan daripada halaman **Butiran persekitaran** LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Dalam Explorer Objek, **Pangkalan Data** dan cari **AXDB**. Anda akan menggantikan pangkalan data dengan pangkalan data baru yang terletak di [Pusat Muat turun](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Salin fail zip ke VM yang anda akan diasingkan dan ekstrak kandungan zip.
8. Dalam Studio Pengurusan Pelayan SQL, klik kanan **AxDB**, dan kemudian pilih **Tugas** > **Pulihkan** > **Pangkalan Data**.

![Pulihkan Pangkalan Data.](./media/5RestoreDatabase.png)

9. Pilih **Peranti Sumber** dan navigasi ke fail yang diekstrak dari zip yang disalin.

![Peranti Sumber.](./media/6SourceDevice.png)

10. Pilih **Pilihan** dan kemudian pilih **Tulis Ganti pangkalan data sedia ada** dan **Tutup sambungan sedia ada ke pangkalan data destinasi**. 
11. Pilih **OK**.

![Pulihkan Tetapan.](./media/7RestoreSetting.png)

Anda akan menerima pengesahan bahawa pemulihan AXDB telah berjaya. Selepas anda menerima pengesahan ini, anda boleh menutup Studio Pengurusan Perkhidmatan SQL.

12. Pergi ke **Perkhidmatan Maklumat Internet** > **Himpunan Aplikasi** > **PerkhidmatanAOS** dan memulakan PerkhidmatanAOS.
13. Pergi ke **Perkhidmatan** dan memulakan dua perkhidmatan yang anda telah berhenti lebih awal.

14. Mencari alat AdminUserProvisioning pada VM ini. Lihat di bawah, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Jalankan fail .ext menggunakan alamat pengguna anda dalam medan **Alamat E-mel**. 
16. Pilih **Serahkan**.

![Peruntukan Pengguna Pentadbir.](./media/8AdminUserProvisioning.png)

Ini mengambil masa beberapa minit untuk dilengkapkan. Anda akan menerima mesej pengesahan yang pengguna Pentadbir telah berjaya dikemas kini.

17. Akhir sekali, jalankan Prom Arahan sebagai Pentadbir dan lakukan iisset semula

![Tetapan Semula IIS.](./media/9IISReset.png)

18. Tutup sesi desktop jarak jauh dan gunakan halaman **butiran persekitaran LCS** untuk log masuk ke persekitaran bagi mengesahkannya, ia berfungsi seperti yang dijangkakan.

![Kewangan dan Operasi.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]