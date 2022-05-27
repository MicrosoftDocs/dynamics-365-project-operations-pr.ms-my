---
title: Daftar untuk langganan pratonton Operasi Projek untuk senario sumber/bukan stok
description: Topik ini memberikan maklumat mengenai cara untuk melanggan dan menggunakan Operasi Projek untuk senario berasaskan sumber/bukan stok.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575821"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Daftar untuk langganan pratonton Operasi Projek untuk senario sumber/bukan stok

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_



Topik ini menerangkan cara untuk melanggan tawaran percubaan dan mengatur letak persekitaran Project Operations untuk senario berdasarkan sumber/tidak distok.

## <a name="prerequisites"></a>Prasyarat
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure. Anda boleh mencipta penyewa semasa penebusan tawaran pertama. 
- Mengatur persekitaran Kewangan memerlukan langganan Azure yang sah yang akan dibilkan bagi setiap persekitaran. Anda boleh menggunakan langganan sedia ada organisasi anda atau gunakan [percubaan Azure](https://azure.microsoft.com/free/) untuk memulakan. Persekitaran CDS akan disediakan percuma untuk tempoh 30 hari terhad.

> [!IMPORTANT]
> Hanya satu orang, pentadbir penyewa, dalam organisasi perlu melaksanakan tugas ini. Jika anda bukan pelanggan kepada keluaran ini, tunggu sehingga organisasi anda didaftarkan dan anda menerima kelayakan pengguna anda.
> 
> Percubaan adalah kegunaan tunggal dalam penyewa. Anda hanya boleh menjalankan percubaan pada satu masa. Kami mengesyorkan anda agar mencipta penyewa baharu untuk tujuan percubaan.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Percubaan Pratonton 

Sebelum anda mulakan, pastikan anda dilog masuk ke pelayar dengan akaun kerja pengguna dalam penyewa yang anda mahu pratonton Operasi Projek.

1. Tebus kod tawaran pertama, **Dynamics 365 Project Operations** di sini [Percubaan Project Operations](https://aka.ms/try-po).
2. Sahkan pesanan anda.

  Anda akan melihat tawaran pengesahan berjaya ditebus.

### <a name="dynamics-365-finance-preview-trial"></a>Percubaan pratonton Dynamics 365 Finance

Pergi ke [Percubaan Pratonton Dynamics 365 for Finance](https://aka.ms/trypoche) dan ulang langka daripada bahagian sebelumnya dengan tawaran, Daftar untuk Persekitaran Berhos Awan.  

## <a name="assign-licenses"></a>Tugaskan lesen

> [!IMPORTANT]
> Anda akan memerlukan akses pentadbiran ke portal Microsoft 365 organisasi anda untuk melengkapkan langkah berikut.

1. Pergi ke [Microsoft 365 pusat](https://portal.office.com/) pentadbiran untuk memperuntukkan lesen kepada pengguna anda.

2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.

3. Tentu sahkan bahawa lesen **Dynamics 365 Project Operations** telah dipilih dan pilih **Simpan perubahan**.

> [!NOTE]
> Tawaran percubaan kewangan tidak perlu ditugaskan kepada pengguna.

## <a name="start-a-new-project-in-lcs"></a>Mulakan projek LCS baharu dalam LCS

Cipta projek LCS baharu seperti yang diterangkan dalam topik, [Mulakan projek baru dalam LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tambah langganan Azure untuk projek LCS

Untuk menyelesaikan tugas ini, ikuti langkah dalam topik, [Tambah langganan Azure untuk projek LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Mengatur persekitaran demo kewangan dengan Operasi Projek untuk senario sumber/bukan stok

Ikuti panduan dalam topik, [Peruntukan persekitaran baharu](resource-provision-new-environment.md) untuk melengkapkan pelaksanaan. Gunakan jenis pelaksanaan untuk pratonton [persekitaran demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment). 

## <a name="install-cds-setup-and-configuration-data"></a>Pasangkan data persediaan dan konfigurasi CDS

Pasangkan data persediaan dan konfigurasi CD seperti yang diterangkan dalam topik, [Sediakan dan gunakan data konfigurasi dalam Common Data Service](resource-apply-pro-setup-config-data.md).
Lengkapkan langkah ini hanya selepas persekitaran demo Finance diatur letak dan data demo bersedia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
