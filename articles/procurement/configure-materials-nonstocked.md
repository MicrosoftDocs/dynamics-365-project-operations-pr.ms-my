---
title: Konfigurasi bahan bukan stok dan invois vendor yang belum selesai
description: Topik ini menerangkan cara mendayakan bahan bukan stok dan invois vendor yang belum selesai.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24418f3aad8356bd209eef7487a47a3870bce10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993922"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurasi bahan bukan stok dan invois vendor yang belum selesai

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

## <a name="minimum-version-requirement"></a>Keperluan versi minimum

Menggunakan bahan bukan stok dan invois vendor yang belum selesai untuk senario berasaskan bukan stok/sumber Dynamics 365 Project Operations memerlukan versi berikut:

Penyelesaian Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 atau lebih tinggi
- Penyelesaian pengorkestraan aplikasi dwi tulis - 2.2.2.23 atau lebih tinggi

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) atau lebih tinggi. Pastikan persekitaran Kewangan anda terkini dan semua kemas kini kualiti digunakan untuk memenuhi keperluan versi minimum.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Jalankan peta Dwi tulis untuk bahan bukan stok dan integrasi invois vendor

Bahagian ini menyediakan maklumat tentang peta khusus yang diperlukan untuk bahan bukan stok dan invois vendor. Sahkan bahawa peta prasyarat yang disenaraikan dalam topik [Peruntukan persekitaran baharu](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) berjalan pada persekitaran anda.

1. Pergi ke Lifecycle Services (LCS), navigasi ke projek LCS anda dan pergi ke halaman **Butiran persekitaran**.
2. Dalam bahagian Maklumat Persekitaran **Common Data Service**, pilih **Paut ke CDS untuk Aplikasi**. Selepas anda memilih pautan tersebut, anda akan dihalakan semula ke senarai entiti dalam pemetaan.
3. Pastikan peta berikut berjalan. Jika peta tidak berjalan, mulakan mereka dan pastikan untuk memasukkan semua peta jadual yang berkaitan.

    - CDS mengeluarkan produk yang berbeza (produk)
    - Vendor v2 (msdyn_vendors)
    - Jadual Project Operations untuk anggaran bahan (msdyn_estimatelines)
    - Entiti eksport invois projek integrasi Project Operations (msdyn_projectvendorinvoices)
    - Entiti eksport baris invois vendor projek integrasi Project Operations (msdyn_projectvendorinvoicelines)
    - Aktual integrasi Project Operations (msdyn_actuals). Pastikan anda sedang menjalankan peta versi 1.0.0.14 atau lebih tinggi. Anda boleh melihat versi aktif peta dalam lajur **Versi** pada halaman **Dwi Tulis**. Anda boleh mengaktifkan versi baharu peta dengan memilih **Versi peta jadual** dan kemudian menyimpan versi yang dipilih.

Jika anda menggunakan data demo standard, anda juga perlu berhenti dan memulakan semula peta entiti berikut dengan penyegerakan awal:
  - Hari pembayaran CDS V2 (msdyn_paymentdays)
  - Jadual pembayaran (msdyn_paymentschedules)
  - Terma pembayaran (msdyn_paymentterms)
  - Kumpulan vendor (msdyn_vendorgroups)
  - Unit (uom)

> [!NOTE]
> Penyegerakan awal untuk kumpulan vendor dan unit mungkin gagal untuk beberapa rekod dalam set data demo yang sedia ada. Anda boleh mengabaikan kegagalan kerana mereka tidak akan menghalang anda daripada menggunakan data demo dengan Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurasikan prasyarat dalam Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktifkan aliran kerja untuk mencipta akaun berdasarkan pada entiti vendor

Penyelesaian Pengorkestraan Dwi Tulis menyediakan [Integrasi induk vendor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md). Sebagai prasyarat untuk ciri ini, data vendor mesti dicipta dalam entiti **Akaun**. Aktifkan proses aliran kerja templat untuk mencipta vendor dalam jadual **Akaun** seperti diterangkan dalam [Tukar antara reka bentuk vendor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Tetapkan produk untuk dicipta sebagai aktif

Bahan bukan stok mesti dikonfigurasikan sebagai **Mengeluarkan produk** dalam Kewangan. Penyelesaian Pengorkestraan Dwi Tulis menyediakan produk [Mengeluarkan integrasi produk ke katalog Produk Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md) di luar kotak. Secara lalai, produk daripada Kewangan disegerakkan ke Dataverse dalam keadaan draf. Untuk menyegerakkan produk ke keadaan aktif supaya produk boleh digunakan secara langsung dalam dokumen penggunaan bahan atau invois vendor yang belum selesai, pergi ke **Sistem** > **Pentadbiran** > **Pentadbiran sistem** > **Tetapan sistem** dan pada tab **Jualan**, tetapkan **Cipta produk dalam keadaan aktif** ke **Ya**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurasikan prasyarat dalam Kewangan

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Dayakan kunci ciri untuk invois vendor yang belum selesai

Lengkapkan langkah berikut untuk mendayakan kefungsian bagi menambah butiran projek pada baris invois vendor yang belum selesai.

1. Dalam Kewangan, pergi ke ruang kerja **Pengurusan Ciri**.
2. Dalam senarai ciri, cari ciri **Dayakan invois vendor yang belum selesai pada Project Operations untuk senario berdasarkan sumber/bukan stok** dan pilih **Dayakan**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Takrifkan kumpulan kategori dan kategori projek untuk item

Konfigurasikan sekurang-kurangnya satu kumpulan kategori untuk jenis transaksi **Item** dan sekurang-kurangnya satu kategori projek menggunakan kumpulan ini. Untuk maklumat lanjut, lihat [Konfigurasikan kategori projek](../project-accounting/configure-project-categories.md#category-groups).

Semak kos projek serta profil hasil dan konfigurasikan persediaan penyiaran lejar untuk transaksi item. Untuk maklumat lanjut, lihat [Konfigurasi perakaunan untuk projek boleh dibil](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Sediakan produk masukan manual

Dalam Project Operations, anda boleh merekod anggaran bahan dan penggunaan produk katalog yang dikonfigurasikan dalam katalog produk yang dikeluarkan dan untuk produk masukan manual. Menggunakan produk masukan manual memerlukan produk keluaran tunggal yang dikonfigurasikan dalam Kewangan untuk tujuan ini. Lengkapkan langkah berikut untuk mengkonfigurasi produk masukan manual. Ulangi langkah ini dalam setiap entiti sah yang menggunakan Project Operations untuk senario sumber/bukan stok.

1. Dalam Kewangan, pergi ke **Pengurusan Maklumat Produk** > **Produk** > **Produk dikeluarkan** dan pilih **Baharu**.
2. Dalam medan **Jenis produk**, pilih **Item** dan dalam medan **subjenis produk**, pilih **Produk**.
3. Masukkan nombor produk (WRITEIN) dan nama produk (Produk Masukan Manual).
4. Pilih kumpulan model item. Pastikan kumpulan model item yang anda pilih mempunyai medan **Polisi inventori produk Stok** ditetapkan ke **Palsu**.
5. Pilih nilai dalam medan **Kumpulan item**, **Kumpulan dimensi storan** dan **Kumpulan dimensi penjejakan**. Gunakan **Dimensi storan** untuk **Tapak** sahaja dan jangan tetapkan sebarang dimensi penjejakan.
6. Pilih nilai dalam medan **Unit inventori**, **Unit pembelian** dan **Unit jualan** dan kemudian simpan perubahan anda.
7. Dalam tab **Pelan**, tetapkan tetapan pesanan lalai dan pada tab **Inventori**, tetapkan tapak dan gudang lalai.
8. Pergi ke **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek** dan buka **Project Operations pada Dynamics 365 Dataverse**. 
9. Pada tab **Bahan**, dalam medan **Produk masukan manual**, pilih produk yang anda cipta.
10. Dalam persekitaran Dataverse anda, dalam petak tapak, buka entiti **Produk** cari rekod produk masukan manual. 
11. Buka butiran rekod dan tetapkan keadaan produk ke **Ditamatkan**. Keadaan produk ini menghalang sesiapa daripada menggunakan rekod ini secara tidak sengaja dalam anggaran bahan dan dokumen penggunaan.

### <a name="set-up-a-procurement-integration-account"></a>Sediakan akaun integrasi perolehan

Akaun integrasi perolehan digunakan sebagai akaun pengosongan apabila menyiarkan invois vendor yang belum selesai dengan baris yang diatributkan ke projek.

Apabila sistem menyiarkan invois vendor yang belum selesai, akaun ini digunakan untuk amaun kos projek. Butiran invois vendor diproses dalam Dataverse dan aktual projek yang berkaitan dicipta. Maklumat daripada aktual projek ditambah ke jurnal integrasi Project Operations. Apabila anda menyiarkan jurnal integrasi, amaun dikosongkan daripada akaun integrasi perolehan dan direkodkan ke kos projek.

1. Untuk menyediakan akaun integrasi perolehan, pergi ke **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek** dan buka **Project Operations pada Dynamics 365 Dataverse**. 
2. Pilih tab **Bahan** dan pilih nilai dalam medan **Akaun integrasi perolehan**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Sediakan kategori projek lalai untuk item

1. Dalam Kewangan, pergi ke **Pengurusan dan perakaunan projek** > **Sediakan** > **Parameter pengurusan dan perakaunan projek** dan buka **Project Operations pada Dynamics 365 Dataverse**. 
2. Pada tab **Kategori projek lalai** dalam medan **Item**, pilih nilai. Kategori projek ini digunakan untuk transaksi bahan jika kategori projek tidak ditetapkan pada rekod aktual projek.
