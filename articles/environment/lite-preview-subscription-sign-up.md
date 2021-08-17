---
title: Daftar untuk langganan pratonton - lite
description: Topik ini memberikan maklumat mengenai cara untuk melanggan dan melaksanakan pelaksanaan lite Project Operations - berurusan dengan penginvoisan proforma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5ba43ba9f917da068415fb62067ab73433b701139ee07014b6bd8c02612008ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991542"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Daftar untuk langganan pratonton - (ringan) 

Topik ini menerangkan cara untuk melanggan tawaran percubaan dan mengatur letak Dynamics 365 Project Operations pelaksanaan ringan - urusan untuk penginvoisan proforma.

> [!NOTE]
> Proses ini akan berubah dalam keluaran Project Operations yang akan datang.

## <a name="prerequisites"></a>Prasyarat
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure. Anda boleh mencipta penyewa semasa penebusan tawaran pertama.

> [!IMPORTANT]
> Hanya satu orang, pentadbir penyewa, dalam organisasi perlu melaksanakan tugas ini. Jika anda bukan pelanggan kepada keluaran ini, tunggu sehingga organisasi anda didaftarkan dan anda menerima kelayakan pengguna anda.
> 
> Percubaan adalah kegunaan tunggal dalam penyewa. Anda hanya boleh menjalankan percubaan pada satu masa. Kami mengesyorkan anda agar mencipta penyewa baharu untuk tujuan percubaan.

### <a name="dynamics-365-project-operations-trial"></a>Percubaan Dynamics 365 Project Operations 

Sebelum anda mulakan, pastikan anda dilog masuk ke pelayar dengan akaun kerja pengguna dalam penyewa yang anda mahu pratonton Operasi Projek.

1. Pergi ke [Percubaan Project Operations](https://aka.ms/try-po) untuk menebus kod tawaran pertama, **Dynamics 365 Project Operations**.
2. Sahkan pesanan anda.

  Anda akan melihat tawaran pengesahan telah berjaya ditebus.

## <a name="assign-licenses"></a>Tugaskan lesen

> [!IMPORTANT]
> Anda akan memerlukan akses pentadbiran ke portal organisasi Microsoft 365 anda untuk melengkapkan langkah berikut.


1. Pergi ke [pusat pentadbir Microsoft 365](https://portal.office.com/) untuk tugaskan lesen kepada pengguna anda.
2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.
3. Tentu sahkan bahawa lesen **Dynamics 365 Project Operations** dipilih. 
4. Pilih **Simpan perubahan**.

## <a name="create-a-new-dataverse-environment"></a>Cipta persekitaran Dataverse baharu

1. Peruntukkan persekitaran pelaksanaan Project Operations Dataverse dengan mengikuti arahan berikut dalam topik, [Model pelaksanaan Dataverse](lite-deployment.md). Apabila anda memilih jenis persekitaran, pastikan untuk menggunakan **Percubaan (Berasaskan langganan)**.

  ![Persekitaran baharu.](./media/19CreateEnvironment.png)

2. Pilih **Dayakan tetapan Dynamics 365**, dan biarkan **Laksanakan secara automatik aplikasi ini** kosong.  
3. Pilih **Simpan** untuk mencipta persekitaran.

  ![Tambah pangkalan data.](./media/20CreateEnvironment1.png)

4. Selepas persekitaran dicipta, pasang penyelesaian **Microsoft Dynamics 365 Project Operations**. 

![Pasang Penyelesaian.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Pasangkan konfigurasi CDS dan data demo persediaan

Pasang konfigurasi CDS dan sediakan data demo dengan mengikut arahan berikut dalam topik, [Gunakan persediaan demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
