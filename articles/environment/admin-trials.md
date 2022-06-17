---
title: Daftar untuk percubaan Project Operations
description: Artikel ini memberikan maklumat tentang cara menggunakan versi percubaan Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 7db7ea6b3cffe6eb43ee0519bbaccfc9092c9311
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959698"
---
# <a name="sign-up-for-project-operations-trials"></a>Daftar untuk percubaan Project Operations 

_**Digunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma dan Project Operations untuk senario berasaskan stok/pengeluaran_ 



Artikel ini menerangkan cara melanggan tawaran rakan kongsi pratonton dan menggunakan Dynamics 365 Project Operations persekitaran.

Dengan percubaan Project Operations baharu, anda boleh menggunakan mana-mana satu daripada tiga senario pelaksanaan yang disokong secara automatik dengan melengkapkan soal selidik yang mencadangkan pendekatan pelaksanaan yang terbaik. Artikel ini memberikan maklumat tentang cara:

- Menebus tawaran percubaan anda.
- Memulakan peruntukan.
- Mengkonfigurasikan dwitulis.
- Ketahui lebih lanjut tentang Project Operations. 

Jadual berikut menggariskan butiran tawaran percubaan baharu.

| **Item tawaran**               | **Butiran**                                  |
|------------------------------|----------------------------------------------|
| Jenis tawaran                   | Jenis tawaran ini adalah diketuai Pentadbir, jadi pentadbir penyewa diperlukan untuk menebus. |
| Penggunaan tawaran                    | Satu kali bagi setiap penyewa                          |
| Tempoh tawaran               | 30 hari kalendar                             |
| Tebusan bagi setiap penyewa       | 1                                            |
| Sambungan                    | 1 sambungan, 30 hari kalendar               |
| Bilangan persekitaran percubaan | 3                                            |


## <a name="admin-trial-details"></a>Butiran percubaan pentadbir
Jadual berikut menyenaraikan butiran percubaan dan cara percubaan terpakai pada setiap jenis pelaksanaan.

| **Padam Item**                      | **Ringan**                                     | **Bahan bukan stok** | **Bahan stok** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Data persediaan yang diberikan           | Ya                                          | Ya                       | Ya (USSI)            |
| Data transaksi            | Tidak                                           | Tidak                        | Tidak                    |
| Masa peruntukan dalam minit  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Prasyarat
Prasyarat berikut diperlukan untuk melaksanakan percubaan Dynamics 365 Project Operations.

- Daftar untuk [Dynamics 365 Project Operations - Percubaan Pratonton](https://www.aka.ms/try-po).
- Pengguna yang menggunakan pratonton mesti mempunyai hak pentadbir global penyewa Azure.

> [!IMPORTANT]
> Hanya satu orang dalam organisasi, pentadbir penyewa, perlu melaksanakan tugas ini. Jika anda bukan pelanggan kepada keluaran ini, tunggu sehingga organisasi anda didaftarkan dan anda menerima kelayakan pengguna anda.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Percubaan pratonton 

Sebelum anda bermula, daftar masuk ke pelayar dengan akaun kerja pengguna dalam penyewa yang anda mahu pratontonkan Project Operations.

1. Tebus kod tawaran pertama, **Dynamics 365 Project Operations - Percubaan Pratonton** dengan menampalkannya ke dalam URL pelayar.

    ![Tebus Tawaran](./media/16RedeemFirstOfferNew.png)

2. Sahkan pesanan anda.

    ![Sahkan pesanan](./media/17ConfirmOrderNew.png)

  Anda akan melihat tawaran pengesahan telah berjaya ditebus.

   ![Pengesahan](./media/18OrderConfirmationNew.png)

  Anda akan dihalakan semula ke [Pusat pentadbiran Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Soal selidik dan peruntukan

1.  Pergi ke [Pusat pentadbiran Power Platform](https://admin.powerplatform.com/projectoperationstrial) dan lengkapkan soal selidik.  
2.  Semak jenis pelaksanaan yang disyorkan dan pilih **Mulakan Persediaan** untuk memulakan peruntukan.
3.  Semak terma dan syarat, dan kemudian pilih **Mula**.

   Selepas peruntukan bermula, anda dihalakan semula ke senarai persekitaran dalam pusat pentadbiran Power Platform. Sementara peruntukan sedang berjalan, keadaan persekitaran anda ialah **PreparingInstance**.
 
  Apabila peruntukan selesai, keadaan persekitaran anda menjadi **Bersedia**. Peruntukan persekitaran termasuk melaksanakan data demo.
 
4.  Pilih URL masing-masing Microsoft Dataverse dan URL aplikasi Kewangan dan Operasi untuk mengesahkan penggunaan.

## <a name="configuring-dual-write"></a>Mengkonfigurasikan dwitulis
- Untuk mengkonfigurasi peranan keselamatan untuk dwi-tulis, lihat [Kemas kini seting keselamatan pada Operasi Projek dalam Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Untuk mengakses konfigurasi dwi-tulis, Navigasi ke contoh Kewangan dan Operasi, kemudian navigasi ke **Pengurusan** > **Data Dual Write**.
- Untuk mengkonfigurasi peta dwi-tulis, lihat [Jalankan peta](resource-provision-new-environment.md#run-project-operations-dual-write-maps) dwi-tulis Operasi Projek.

## <a name="assign-licenses"></a>Peruntukkan lesen

Anda akan memerlukan akses pentadbiran ke portal Microsoft 365 organisasi anda untuk melengkapkan langkah berikut.

1. Pergi ke [Microsoft 365 pusat](https://portal.office.com/) pentadbiran untuk memperuntukkan lesen kepada pengguna anda.

   ![Laman utama pusat pentadbiran](./media/14AdminPortal.png)

2. Pada halaman **Pengguna aktif**, pilih pengguna yang anda mahu peruntukkan lesen.

   ![Tugaskan Lesen](./media/15AssignLicenses.png)

3. Sahkan bahawa lesen **Pratonton Dynamics 365 Project Operations** telah dipilih dan kemudian pilih **Simpan perubahan**.

## <a name="additional-resources"></a>Sumber tambahan

Sumber berikut menyediakan panduan berguna sambil anda memulakan perjalanan anda dengan Project Operations:

- [Siri Video - Gambaran keseluruhan, selaman dalam ciri dan hala tuju Project Operations](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Tentukan jenis pelaksanaan anda](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Bagaimana jika saya memerlukan ALM atau ELM untuk persekitaran aplikasi Kewangan dan Operasi saya?

- Untuk rakan kongsi yang memerlukan keupayaan pengurusan kitaran hayat persekitaran penuh, lihat [Permintaan Lesen Kotak Pasir Rakan Kongsi](https://experience.dynamics.com/requestlicense) untuk menyemak tawaran rakan kongsi baharu. 
- Untuk rakan kongsi yang mencari maklumat lanjut tentang Hak Penggunaan Dalaman, lihat [Manfaat awan dan perisian Hak Penggunaan Dalaman (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Adakah saya boleh melanjutkan percubaan saya lebih daripada 30 hari?
Untuk melanjutkan percubaan anda, lengkapkan langkah berikut.

1. **Microsoft 365 Dalam Pusat** Pentadbiran, pergi ke **Pengebilan** > **produk** Anda.
2. Pilih **Dynamics 365 Project Operations (CE) - Percubaan Pratonton**.
3. Di bawah **Tarikh Tamat Tempoh**, pilih **Lanjutkan Tarikh**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Adakah saya boleh menaik taraf daripada pelaksanaan ringan kepada pelaksanaan senario berasaskan sumber/bukan stok?
Pada masa ini, tiada sokongan untuk menaik taraf persekitaran daripada ringan kepada pelaksanaan berasaskan bukan stok.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Adakah saya boleh mencapai Lifecycle Services (LCS) untuk persekitaran Kewangan saya?  
Tidak. Untuk percubaan ini, pelaksanaan akan diuruskan melalui Pusat Pentadbiran Power Platform. Capaian kepada persekitaran Kewangan adalah terhad.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Adakah saya boleh memasang percubaan saya pada persekitaran yang sedia ada?
Jika anda mempunyai persekitaran yang sedia ada, anda akan dibenarkan untuk memasang pelaksanaan ringan pada persekitaran Dataverse jualan yang sedia ada daripada Pusat Pentadbiran Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
