---
title: Daftar untuk langganan pratonton - lite
description: Topik ini memberikan maklumat mengenai cara untuk melanggan dan melaksanakan pelaksanaan lite Project Operations - berurusan dengan penginvoisan proforma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290055"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Daftar untuk langganan pratonton - lite 

Topik ini menerangkan cara untuk melanggan tawaran rakan kongsi pratonton dan melaksanakan pelaksanaan ringan Dynamics 365 Project Operations - berurusan untuk invois proforma.

> [!NOTE]
> Proses ini akan berubah dalam keluaran Project Operations yang akan datang.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima e-mel yang menjemput anda menyertai pratonton. Anda boleh meminta pratonton pada [tapak web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure.
- Semak semua terma dan syarat.

## <a name="subscribe"></a>Melanggan

Apabila anda menerima kelulusan [permintaan pratonton](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), anda akan menerima dua tawaran daripada Microsoft melalui e-mel. Tawaran ini membolehkan anda menggunakan Pratonton Project Operations:

- Dynamics 365 Project Operations (CRM) - Percubaan Pratonton
- Operasi Projek Office 365- Percubaan Pratonton

> [!IMPORTANT]
> Hanya satu orang, pentadbir penyewa, dalam organisasi perlu melaksanakan tugas ini. Jika anda bukan pelanggan kepada keluaran ini, tunggu sehingga organisasi anda didaftarkan dan anda menerima kelayakan pengguna anda.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Percubaan Pratonton 

Sebelum anda mulakan, pastikan anda dilog masuk ke pelayar dengan akaun kerja pengguna dalam penyewa yang anda mahu pratonton Operasi Projek.

1. Tebus kod tawaran pertama, **Dynamics 365 Project Operations (CRM) - Percubaan Pratonton** dengan menampalkannya ke dalam URL pelayar.

![Tebus Tawaran](./media/16RedeemFirstOfferNew.png)

2. Sahkan pesanan anda.
![Sahkan pesanan](./media/17ConfirmOrderNew.png)

Anda akan melihat tawaran pengesahan berjaya ditebus.

![Pengesahan](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Operasi Projek Office 365- Percubaan Pratonton

Ulangi langkah yang sama dengan kod tawaran pertama. Pastikan untuk menambah kod tawaran kedua menggunakan akaun pengguna yang sama yang digunakan dengan kod tawaran pertama.

## <a name="assign-licenses"></a>Tugaskan lesen

> [!IMPORTANT]
> Anda akan memerlukan akses pentadbiran ke portal organisasi Microsoft 365 anda untuk melengkapkan langkah berikut.


1. Pergi ke [pusat pentadbir Microsoft 365](https://portal.office.com/) untuk tugaskan lesen kepada pengguna anda.

![Laman utama pusat pentadbiran](./media/14AdminPortal.png)

2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.

![Tugaskan Lesen](./media/15AssignLicenses.png)

3. Sahkan bahawa lesen **Pratonton Dynamics 365 Project Operations (CRM)** dan **Office 365 Project Operations - Pratonton** dipilih. 
4. Pilih **Simpan perubahan**.

## <a name="create-a-new-cds-environment"></a>Cipta persekitaran CDS

1. Peruntukkan persekitaran pelaksanaan CDS Project Operations baharu dengan mengikuti arahan dalam topik, [model pelaksanaan CDS](lite-deployment.md). Apabila anda memilih jenis persekitaran, pastikan untuk menggunakan **Percubaan (Berasaskan langganan)**.
![Persekitaran baru](./media/19CreateEnvironment.png)

2. Pilih **Dayakan tetapan Dynamics 365**, dan biarkan **Laksanakan secara automatik aplikasi ini** kosong.  
3. Pilih **Simpan** untuk mencipta persekitaran.

![Tambah pangkalan data](./media/20CreateEnvironment1.png)

4. Selepas persekitaran dicipta, pasang penyelesaian **Microsoft Dynamics 365 Project Operations**. 

![Pasang Penyelesaian](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Pasangkan konfigurasi CDS dan data demo persediaan

Pasang konfigurasi CDS dan sediakan data demo dengan mengikut arahan berikut dalam topik, [Gunakan persediaan demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]