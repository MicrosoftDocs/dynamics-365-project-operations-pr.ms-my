---
title: Daftar untuk langganan pratonton
description: Topik ini memberikan maklumat mengenai cara untuk melanggan dan melaksanakan pelaksanaan lite Project Operations - berurusan dengan penginvoisan proforma.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948989"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Daftar untuk langganan pratonton untuk pelaksanaan Lite – urusan untuk penginvoisan proforma

Topik ini menjelaskan cara untuk melanggan tawaran rakan kongsi pratonton dan melaksanakan pelaksanaan lite Dynamics 365 Project Operations - urusan untuk penginvoisan proforma.

> [!NOTE]
> Proses ini akan berubah dalam keluaran Project Operations yang akan datang.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima e-mel yang menjemput anda menyertai pratonton. Anda boleh meminta pratonton pada [tapak web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure.
- Pengguna yang menggunakan pratonton akan memerlukan nombor telefon dan kad kredit yang sah. Semasa mendaftar, tiada caj dikenakan untuk kad selama enam bulan. Selepas enam bulan, anda perlu membatalkan langganan. 
- Semak semua terma dan syarat.

## <a name="subscribe"></a>Melanggan

Apabila anda menerima kelulusan [permintaan pratonton](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), anda akan menerima dua tawaran daripada Microsoft melalui e-mel. Tawaran ini membolehkan anda menggunakan Pratonton Project Operations:

- Percubaan pratonton Dynamics 365 Customer Service - kod penggunaan tunggal
- Dynamics 365 Project Operations – percubaan pratonton

### <a name="dynamics-365-customer-service-paid-offer"></a>Tawaran berbayar Dynamics 365 Customer Service

1. Menggunakan tetingkap pelayar InPrivate/Inkognito, tebus kod tawaran pertama untuk Dynamics 365 Customer Service. Untuk mendaftar untuk Customer Service, anda akan memerlukan:

- Nombor telefon
- Kad kredit. Apabila mendaftar, tiada caj dikenakan untuk kad selama enam bulan. Selepas enam bulan, anda perlu membatalkan langganan.
- Semak semua terma dan syarat.

2. Berikan maklumat hubungan anda.

![Maklumat Kenalan](./media/1ContactInformation.png)

3. Berikan butiran penyewa baharu.

![Cipta ID Pengguna](./media/2CreateUserID.png)

4. Sahkan identiti anda, simpan ID pengguna baharu anda dan kemudian pilih **Sediakan**.

![Simpan Maklumat](./media/3SaveInfo.png)

5. Lengkapkan pendaftaran kad kredit dan semak semua terma dan syarat. 

![Lengkapkan Kad Kredit](./media/4CompleteCreditCard.png)

![Daftar Keluar Kad Kredit](./media/5CreditCardCheckout.png)

![Simpan Pesanan](./media/6SaveOrder.png)

![Maklumat kad kredit](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Batalkan tawaran perusahaan Dynamics 365 Customer Service

Tawaran Perusahaan Dynamics 365 Customer Service disediakan secara percuma selama enam bulan. Tawaran ini akan diperbaharui pada kadar penuh pada akhir tempoh enam bulan. Untuk membatalkan sebelum tarikh pembaharuan, lengkapkan arahan berikut. 

> [!NOTE]
> Selepas anda melengkapkan langkah ini, anda tidak akan lagi dapat menggunakan persekitaran pratonton awam Project Operations.

1. Pergi ke [Portal pentadbir](https://admin.microsoft.com/) dan di bawah **Pengebilan**, pilih **Produk Anda**.

![Portal Pentadbir, Halaman produk anda](./media/8AdminPortal.png)

2. Pilih **Tawaran Perusahaan Dynamics 365 Customer Service**.

![Batalkan Langganan](./media/9CancelSubscription.png)

3. Pilih **Tetapan** > **Tindakan** > **Batalkan Langganan**.
4. Pada borang **Pembatalan langganan**, masukkan maklumat dalam medan yang diperlukan.
5. Pilih **Batalkan** > **Langganan.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Percubaan pratonton

1. Tebus tawaran kedua, Percubaan Dynamics 365 Project Operations dengan URL yang diberikan dalam e-mel alu-aluan anda.

![Tebus Tawaran 2](./media/10RedeemOffer2.png)

2. Sahkan bahawa anda telah log masuk sebagai pengguna yang tergolong dalam organisasi yang sama yang dilanggan menggunakan kod tawaran pertama dan teruskan penebusan tawaran. 
3. Pilih **Ya, tambahkan pada akaun saya**.

![Tambah pada Akaun](./media/11AddToAccount.png)

![Cuba Skrin Sekarang](./media/12TryNow.png)

![Butiran pesanan](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Tugaskan lesen

> [!IMPORTANT]
> Anda akan memerlukan akses pentadbiran ke portal Office 365 organisasi anda untuk melengkapkan langkah berikut.

1. Pergi ke [pusat pentadbir Microsoft 365](https://portal.office.com/) untuk tugaskan lesen kepada pengguna anda.

![Laman utama pusat pentadbiran](./media/14AdminPortal.png)

2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.

![Tugaskan Lesen](./media/15AssignLicenses.png)

3. Sahkan bahawa **Perusahaan Customer Service** dan lesen **Project Operations** telah dipilih dan pilih **Simpan perubahan**.

## <a name="create-a-new-cds-environment"></a>Cipta persekitaran CDS

Peruntukkan persekitaran pelaksanaan CDS Project Operations baharu dengan mengikuti arahan dalam topik, [model pelaksanaan CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Pasangkan konfigurasi CDS dan data demo persediaan

Pasang konfigurasi CDS dan sediakan data demo dengan mengikut arahan berikut dalam topik, [Gunakan persediaan demo dan data konfigurasi](lite-apply-demo-setup-config-data.md).
