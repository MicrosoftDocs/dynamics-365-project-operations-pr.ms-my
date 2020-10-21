---
title: Daftar untuk langganan pratonton Operasi Projek untuk senario sumber/bukan stok
description: Topik ini memberikan maklumat mengenai cara untuk melanggan dan menggunakan Operasi Projek untuk senario berasaskan sumber/bukan stok.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948992"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Daftar untuk langganan pratonton Operasi Projek untuk senario sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menerangkan cara untuk melanggan tawaran pratonton/rakan kongsi dan menggunakan persekitaran Operasi Projek untuk senario berasaskan sumber/bukan stok.

## <a name="prerequisites"></a>Prasyarat

- Anda akan menerima e-mel yang menjemput anda menyertai pratonton. Anda boleh meminta pratonton pada [tapak web Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure.
- Mengatur persekitaran Kewangan memerlukan langganan Azure yang sah yang akan dibilkan bagi setiap persekitaran. Anda boleh menggunakan langganan sedia ada organisasi anda atau gunakan [percubaan Azure](https://azure.microsoft.com/en-us/free/) untuk memulakan. Persekitaran CDS akan disediakan percuma untuk tempoh 30 hari terhad.

## <a name="subscribe"></a>Melanggan

Apabila [permintaan pratonton](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) anda diluluskan, anda akan menerima dua tawaran daripada Microsoft melalui e-mel. Tawaran ini membolehkan anda menggunakan Pratonton Project Operations:

- Operasi Projek Dynamics 365 – Percubaan Pratonton
- Percubaan Pratonton Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Hanya satu orang, pentadbir penyewa, dalam organisasi perlu melaksanakan tugas ini. Jika anda bukan pelanggan kepada keluaran ini, tunggu sehingga organisasi anda didaftarkan dan anda menerima kelayakan pengguna anda.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – Percubaan pratonton

1. Tebus tawaran pertama, **Percubaan Operasi Projek Dynamics 365**, dengan URL yang diberikan dalam e-mel alu-aluan anda.

![Tawaran Pertama](./media/1FirstOffer.png)

2. Sahkan bahawa anda log masuk sebagai pengguna yang tergolong dalam organisasi yang akan melanggan perkhidmatan tersebut.
3. Teruskan dengan penebusan tawaran. 
4. Pilih **Ya, tambahkan pada akaun saya**.

![Tebus Tawaran](./media/2RedeemFirstOffer.png)

![Sahkan Tawaran](./media/3ConfirmFirstOffer.png)

![Tawaran Ditebus](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Percubaan pratonton Dynamics 365 Finance

Ulangi langkah yang sama dengan tawaran kedua daripada e-mel alu-aluan.

## <a name="assign-licenses"></a>Tugaskan Lesen

> [!IMPORTANT]
> Anda akan memerlukan akses pentadbiran ke portal Office 365 organisasi anda untuk melengkapkan langkah berikut.

1. Pergi ke [Pusat pentadbir Microsoft 365](https://portal.office.com/) untuk tugaskan lesen kepada pengguna anda.

![Portal Pentadbir Pejabat](./media/5OfficeAdminPortal.png)

2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.

![Tugaskan Lesen](./media/6AssignLicenses.png)

3. Sahkan bahawa lesen Operasi Projek telah dipilih dan pilih **Simpan perubahan**. 

> [!NOTE]
> Tawaran percubaan kewangan tidak perlu ditugaskan kepada pengguna.

## <a name="start-a-new-project-in-lcs"></a>Mulakan projek LCS baharu dalam LCS

Cipta projek LCS baharu seperti yang diterangkan dalam topik, [Mulakan projek baru dalam LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tambah langganan Azure untuk projek LCS

Untuk menyelesaikan tugas ini, ikuti langkah dalam topik, [Tambah langganan Azure untuk projek LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Mengatur persekitaran demo kewangan dengan Operasi Projek untuk senario sumber/bukan stok

Ikuti panduan dalam topik, [Peruntukan persekitaran baharu](resource-provision-new-environment.md) untuk melengkapkan pelaksanaan. Gunakan jenis pelaksanaan untuk pratonton [persekitaran demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment).

## <a name="install-cds-setup-and-configuration-data"></a>Pasangkan data persediaan dan konfigurasi CDS

Pasangkan data persediaan dan konfigurasi CD seperti yang diterangkan dalam topik, [Sediakan dan gunakan data konfigurasi dalam Common Data Service](resource-apply-pro-setup-config-data.md).

