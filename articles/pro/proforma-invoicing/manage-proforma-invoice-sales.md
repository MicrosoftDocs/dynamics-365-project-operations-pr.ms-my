---
title: Urus invois projek proforma
description: Topik ini menyediakan maklumat tentang cara bekerja dengan invois projek proforma.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2146e62bddc4a6286fa303ff2cc2c5622ea3133c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866917"
---
# <a name="manage-a-proforma-project-invoice"></a>Urus invois projek proforma 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, invois proforma dibina sebagai sambungan kepada invois dalam Dynamics 365 Sales. Walau bagaimanapun, terdapat banyak perbezaan dalam proses penginvoisan antara jualan dengan Project Operations semasa penginvoisan dibuat. Contohnya, tidak mungkin untuk mencipta invois baharu daripada halaman **Senarai Invois** dalam Project Operations, tetapi adalah mungkin untuk berbuat demikian dalam Jualan. Perbezaan dan sambungan ini tersedia untuk menyokong proses penginvoisan untuk projek yang berbeza daripada invois biasa untuk pesanan jualan.

> [!IMPORTANT]
> Disebabkan perbezaan, jangan gunakan invois dalam Jualan dan Project Operations secara bergantian.

## <a name="invoice-header"></a>Pengepala invois

Maklumat berikut tersedia pada pengepala invois proforma dalam Project Operations.

| Medan | Lokasi | Penerangan  | Kesan hiliran |
| --- | --- | --- | --- |
| **ID Invois** | Tab **Ringkasan** | ID yang dijana secara automatik apabila invois proforma dicipta. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan sebagai rujukan bagi setiap invois proforma. |
| **Nama** | Tab **Ringkasan** | Ditetapkan kepada nama kontrak projek secara lalai. Medan ini boleh diedit oleh pengguna. | &nbsp;  |
| **Mata wang** | Tab **Ringkasan** | Ditetapkan kepada mata wang kontrak projek secara lalai. Medan baca sahaja yang dikunci daripada pengeditan. |&nbsp; |
| **Senarai harga** | Tab **Ringkasan** | Ditetapkan kepada senarai harga kontrak projek secara lalai. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Peluang** | Tab **Ringkasan** | Rujukan kepada peluang yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp;  |
| **Kontrak** | Tab **Ringkasan** | Rujukan kepada kontrak projek yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Pelanggan** | Tab **Ringkasan** | Rujukan kepada kontrak projek yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. |&nbsp;  |
| **Perihalan** | Tab **Ringkasan** | Medan teks yang menerangkan invois. Medan ini boleh diedit oleh pengguna. | &nbsp; |
| **Bil Ke** dan medan yang berkaitan | **Tab Ringkasan** | Lalai ditetapkan daripada pelanggan kontrak projek. Medan ini boleh diedit oleh pengguna.  | &nbsp; |
| **Status** | Tab **Ringkasan** | Tetapkan pilihan berikut: **Aktif**, **Tertutup**, **Dibayar** dan **Dibatalkan** dan boleh diedit oleh pengguna. | Status tidak disokong untuk Project Operations termasuk **Tertutup** dan **Dibatalkan**. </br> Status ditetapkan kepada **Aktif** apabila invois dicipta. </br>Status hendaklah ditetapkan kepada **Dibayar** hanya selepas invois disahkan. |
| **Status Invois Projek** | Tab **Ringkasan** | Tetapkan pilihan berikut: **Aktif**, **Dalam semakan** dan **Disahkan** dan boleh diedit oleh pengguna. | Dalam status **Draf** dan **Dalam Semakan**, invois boleh diedit. Invois tidak boleh diedit selepas invois disahkan. |
| **Amaun Butiran** | Tab **Ringkasan** | Jumlah amaun pada semua baris invois selepas pendahuluan dan potongan. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan untuk mengira amaun akhir. |
| **Diskaun (%)** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan peratusan diskaun. Medan ini tidak disokong oleh kefungsian Project Operations. | Medan ini ialah medan yang tidak disokong. |
| **Amaun Diskaun** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan amaun diskaun. Medan ini tidak disokong oleh kefungsian Project Operations. | Medan ini ialah medan yang tidak disokong. |
| **Amaun Pra Penghantaran** | **Tab Ringkasan** | Jumlah amaun invois selepas diskaun digunakan. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan untuk mengira amaun akhir. |
| **Amaun Pengangkutan** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan amaun pengangkutan. Medan ini tidak disokong oleh kefungsian Project Operations. | Medan ini ialah medan yang tidak disokong. |
| **Jumlah Cukai** | Tab **Ringkasan** | Jumlah cukai daripada semua baris invois ke atas invois. Medan baca sahaja yang dikunci daripada pengeditan. | Tiada. |
| **Jumlah Amaun** | Tab **Ringkasan** | Jumlah amaun selepas diskaun dan cukai. | Jumlah tersebut ialah amaun yang perlu dibayar oleh pelanggan. |
## <a name="project-based-invoice-lines"></a>Baris invois berasaskan projek

Dalam Project Operations, sentiasa ada satu baris invois untuk setiap baris kontrak projek. Baris invois dicipta walaupun tiada aktual. Maklumat berikut tersedia pada baris invois proforma.

| Medan | Lokasi | Penerangan  | Kesan hiliran |
| --- | --- | --- | --- |
| **ID Invois** | Tab **Umum** | Rujukan kepada ID invois. Medan baca sahaja yang dikunci daripada pengeditan. | Pautan ID invois boleh digunakan untuk menavigasi kembali ke pengepala invois. |
| **Nama** | Tab **Umum** | Nama baris invois ditetapkan secara lalai daripada nama baris kontrak. Medan ini boleh diedit oleh pengguna. | &nbsp; |
| **Project** | Tab **Umum** | Projek berkenaan baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. | Pautan projek boleh digunakan untuk menavigasi ke projek. |
| **Kaedah Pengebilan** | Tab **Umum** | Kaedah pengebilan berkenaan baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Amaun Baris Kontrak** | Tab **Umum** | Amaun kontrak pada baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Diinvois hingga Tarikh** | Tab **Umum** | Jumlah amaun pada semua butiran baris invois bagi invois ini. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Amaun** | Tab **Umum** | Jumlah amaun pada semua butiran baris invois bagi invois ini yang boleh dituntut. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan untuk mengira amaun akhir pada pengepala invois. |
| **Cukai** | Tab **Umum** | Jumlah amaun cukai pada semua butiran baris invois bagi baris invois ini. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan untuk mengira amaun cukai akhir pada pengepala invois. |
| **Amaun Dilanjutkan** | Tab **Umum** | Jumlah amaun (**Cukai + Amaun**) pada semua butiran baris invois bagi baris invois ini yang boleh dituntut. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini digunakan untuk mengira amaun akhir pada pengepala invois. |


## <a name="invoice-line-details"></a>Butiran baris invois

Setiap baris invois dalam invois projek termasuk butiran baris invois. Butiran baris ini berkaitan dengan aktual jualan yang belum dibilkan dan pencapaian yang berkaitan dengan baris kontrak yang dirujuk mengikut baris invois. Semua transaksi ini ditanda **Bersedia untuk Diinvois**.

Untuk baris **Invois Masa dan Bahan**, butiran baris invois dikumpulkan ke dalam **Boleh dituntut**, **Tidak boleh dituntut** dan **Percuma** pada halaman **Baris Invois**. Butiran **Baris Invois Boleh Dituntut** menambah sehingga jumlah baris invois. **Percuma** dan **Aktual yang tidak boleh dituntut** tidak akan ditambah pada jumlah baris invois.

Untuk baris **Invois Harga Tetap**, butiran baris invois dicipta daripada pencapaian yang ditandakan sebagai **Sedia untuk diinvois** pada baris kontrak yang berkaitan. Selepas butiran baris invois dicipta daripada pencapaian, status pengebilan pada pencapaian dikemas kini kepada **Invois Pelanggan Dicipta**.

### <a name="edit-invoice-line-details"></a>Edit butiran baris invois

Medan berikut tersedia pada butiran baris invois yang disokong oleh aktual jualan yang belum dibilkan:

| Medan | Penerangan | Kesan hiliran |
| --- | --- | --- |
| **Baris invois** | Rujukan kepada **ID Baris Invois**. Medan baca sahaja dikunci untuk pengeditan. | Pautan ini boleh digunakan untuk menavigasi kembali ke pengepala invois. |
| **Perihalan** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada medan **Komen Dalaman** pada **Entri Masa** dan daripada medan **Perihalan** pada **Entri Perbelanjaan**. Medan boleh diedit oleh pengguna.| &nbsp; |
| **Perihalan Luaran** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada medan **Komen Luaran** pada **Entri Masa** dan medan **Perihalan** pada **Entri Perbelanjaan**. Medan boleh diedit oleh pengguna. | Perihalan ini boleh digunakan untuk menentukan perkara yang sepatutnya ada pada invois bercetak yang akan dihantar kepada pelanggan. Dalam Project Operations, invois proforma tidak mempunyai semua kefungsian yang diperlukan untuk mengkonfigurasikan tetapan cetak untuk invois. |
| **Tarikh Mula** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan ini boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. |
| **Project** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Ditetapkan secara lalai kepada projek pada baris kontrak yang berkaitan. |
| **Tugas** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. Senarai juntai bawah menunjukkan semua tugas yang dikaitkan dengan baris kontrak projek yang berkaitan.  |
| **Kategori transaksi** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh sumber sebenar. |
| **Peranan** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. |
| **Sumber Boleh Ditempah** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh sumber sebenar. |
| **Unit Sumber** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. |
| **Kuantiti** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. |
| **Jadual Unit** | Untuk butiran baris invois untuk masa, ini sentiasa ditetapkan kepada masa dan tidak boleh diedit. Untuk perbelanjaan, ini ditetapkan secara lalai daripada aktual perbelanjaan sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Ditetapkan secara lalai kepada **Masa** pada butiran baris invois baharu yang tidak disokong oleh aktual. |
| **Unit** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber |
| **Harga** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Medan boleh diedit pada butiran baris invois baharu yang tidak disokong oleh aktual sumber. Jika tiada nilai yang dimasukkan, ia ditetapkan secara lalai selepas **Simpan**. |
| **Mata wang** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Ditetapkan secara lalai daripada pengepala invois apabila mencipta butiran invois baharu tanpa sokongan sebenar.  Medan baca sahaja yang dikunci daripada pengeditan. |
| **Amaun** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Dikira sebagai **Kuantiti \* Harga** apabila mencipta butiran invois baharu tanpa aktual sokongan. Ia dikira selepas **Simpan**. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Cukai** | Ditetapkan secara lalai daripada aktual sumber. Medan boleh diedit oleh pengguna | Medan boleh diedit oleh pengguna apabila mencipta butiran baris invois baharu tanpa aktual sokongan. |
| **Amaun Dilanjutkan** | Medan dikira, dikira sebagai **Amaun + Cukai**. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Jenis Pengebilan** | Ditetapkan secara lalai daripada aktual sumber. Medan boleh diedit oleh pengguna. | Memilih **Boleh Dituntut** menambah baris kepada jumlah baris invois. **Percuma** dan **Tidak Boleh Dituntut** akan mengecualikannya daripada jumlah baris invois. |
| **Pilih Produk** | Ditetapkan secara lalai daripada aktual sumber, ini ialah medan baca sahaja. | Apabila anda mencipta butiran baris invois baharu tanpa membuat aktual sandaran, medan ini boleh diedit. |
| **Produk** | Ditetapkan secara lalai daripada aktual sumber, ini ialah medan baca sahaja. | Apabila anda mencipta butiran baris invois baharu tanpa membuat aktual sandaran, medan ini boleh diedit jika medan **Pilih Produk** ditetapkan kepada **Produk sedia ada**. |
| **Nama Produk** | Ditetapkan secara lalai daripada aktual sumber, ini ialah medan baca sahaja. | Pada butiran baris invois baharu, yang ID produk dipilih daripada katalog, medan ini ditetapkan kepada nama produk. Untuk produk masukan manual, medan akan ditetapkan kepada nama masukan manual. |
| **Perihalan Masukan Manual** | Ditetapkan secara lalai daripada aktual sumber, ini medan baca sahaja. | Apabila anda mencipta butiran baris invois baharu tanpa aktual sandaran, anda boleh menambahkan perihalan masukan manual untuk produk tersebut. |
| **Jenis Transaksi** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Ditetapkan secara lalai kepada **Jualan Dibilkan** dan dikunci apabila mencipta **butiran baris invois** baharu tanpa aktual sandaran.  |
| **Kelas Transaksi** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | Ditetapkan secara lalai berdasarkan sama ada pengguna memilih untuk mencipta butiran baris **Masa**, **Perbelanjaan**, **Bahan** atau **Yuran** sambil turut mencipta **Butiran baris invois** baharu tanpa aktual sandaran. Dikunci daripada pengeditan. |

Medan berikut tersedia pada butiran baris invois yang disokong oleh pencapaian:

| Medan | Penerangan  | Kesan hiliran |
| --- | --- | --- |
| **Baris invois** | Rujukan kepada **ID Baris Invois**. Medan baca sahaja yang dikunci daripada pengeditan. | Pautan boleh digunakan untuk menavigasi kembali ke pengepala invois. |
| **Perihalan** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada perihalan pencapaian sumber. | &nbsp; |
|**Perihalan Luaran** | Perihalan butiran baris invois yang ditetapkan secara lalai daripada perihalan pencapaian sumber. | Medan ini boleh digunakan untuk menentukan perkara yang sepatutnya ada pada invois bercetak yang akan dihantar kepada pelanggan. Invois proforma dalam Project Operations tidak mempunyai semua kefungsian yang diperlukan untuk mengkonfigurasikan tetapan cetak untuk invois. |
| **Tarikh Mula** | Ditetapkan secara lalai dari tarikh **Pencapaian** pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Project** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Tugas** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Kategori transaksi** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Peranan** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Sumber Boleh Ditempah** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Unit Sumber** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Jadual Unit** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Unit** | Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Harga** | Ditetapkan secara lalai daripada amaun pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Mata wang** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. |&nbsp; |
| **Amaun** | Ditetapkan secara lalai daripada amaun pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Cukai** | Ditetapkan secara lalai daripada amaun cukai pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Amaun Dilanjutkan** | Ditetapkan secara lalai daripada amaun dilanjutkan pada pencapaian sumber. Medan boleh diedit oleh pengguna | &nbsp; |
| **Jenis Pengebilan** | Sentiasa ditetapkan secara lalai kepada **Boleh Dituntut**. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Jenis Transaksi** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |
| **Kelas Transaksi** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Cipta butiran baris invois baharu

Pada baris masa dan invois bahan, anda boleh mencipta butiran baris invois baharu. Butiran baris invois ini tidak disokong oleh aktual. Pada baris invois bagi baris masa dan invois bahan, anda boleh memilih **Baharu** untuk mencipta butiran baris invois baharu untuk kelas transaksi yang disertakan pada baris kontrak.

## <a name="refresh-invoice-transactions"></a>Segar semula transaksi invois

Jika anda mempunyai aktual yang datang selepas invois dicipta, anda boleh memasukkan aktual ini pada invois.

1. Dalam **Pandangan Tunggakan Pengebilan**, tandakan data sebagai **Bersedia untuk Diinvois**.   
2. Buka draf invois proforma dan pada reben **Tindakan**, klik **Segar Semula Transaksi Baris Invois**.

  Ini mencipta butiran baris invois untuk mana-mana aktual yang terdahulu dan ditandakan sebagai **Bersedia untuk Diinvois**; tetapi tidak dimasukkan dalam invois.

## <a name="product-based-invoice-lines"></a>Baris invois berasaskan produk

Dalam Project Operations, anda boleh mencipta baris invois untuk produk yang tidak diguna pakai untuk mana-mana projek atau untuk semua projek bersama dengan baris invois berasaskan projek. Baris invois ini dicipta sebagai baris kontrak berasaskan produk dan selepas baris ditandakan sebagai bersedia dengan diinvois, baris tersebut ditambah sebagai baris invois berasaskan produk.

Selepas anda menambah baris invois berasaskan produk, baris tersebut tidak boleh ditukar. Walau bagaimanapun, baris boleh dipadamkan daripada draf invois proforma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
