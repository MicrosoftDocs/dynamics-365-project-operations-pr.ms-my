---
title: Urus invois berdasarkan projek proforma
description: Topik ini menyediakan maklumat tentang cara mengurus dan bekerja dengan invois berdasarkan projek proforma.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fd357648f8166cbcbe91ca1922739585f9fcfa9
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867232"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Urus invois berdasarkan projek proforma

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Dalam Dynamics 365 Project Operations, invois proforma dibina sebagai sambungan kepada invois dalam Dynamics 365 Sales. Walau bagaimanapun, terdapat banyak perbezaan dalam proses penginvoisan antara jualan dengan Project Operations semasa penginvoisan dibuat. Contohnya, tidak mungkin untuk mencipta invois baharu daripada halaman **Senarai Invois** dalam Project Operations, tetapi adalah mungkin untuk berbuat demikian dalam Jualan. Perbezaan dan sambungan ini tersedia untuk menyokong proses penginvoisan untuk projek yang berbeza daripada invois biasa untuk pesanan jualan.

> [!IMPORTANT]
> Disebabkan perbezaan, jangan gunakan invois dalam Jualan dan Project Operations secara bergantian.

## <a name="invoice-header"></a>Pengepala invois

Maklumat berikut tersedia pada pengepala invois proforma dalam Project Operations.

| Medan | Lokasi | Penerangan |
| --- | --- | --- | 
| **ID Invois** | Tab **Ringkasan** | ID yang dijana secara automatik apabila invois proforma dicipta. Medan baca sahaja yang dikunci daripada pengeditan. Medan ini digunakan sebagai rujukan bagi setiap invois proforma. |
| **Nama** | Tab **Ringkasan** | Ditetapkan kepada nama kontrak projek secara lalai. Medan ini boleh diedit. | 
| **Mata wang** | Tab **Ringkasan** | Ditetapkan kepada mata wang kontrak projek secara lalai. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Senarai harga** | Tab **Ringkasan** | Ditetapkan kepada senarai harga kontrak projek secara lalai. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Peluang** | Tab **Ringkasan** | Rujukan kepada peluang yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Kontrak** | Tab **Ringkasan** | Rujukan kepada kontrak projek yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Pelanggan** | Tab **Ringkasan** | Rujukan kepada kontrak projek yang dipautkan. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Perihalan** | Tab **Ringkasan** | Medan teks yang menerangkan invois. Medan ini boleh diedit. | 
| **Bil Ke** dan medan yang berkaitan | **Tab Ringkasan** | Lalai ditetapkan daripada pelanggan kontrak projek. Medan ini boleh diedit.  | 
| **Status** | Tab **Ringkasan** | Tetapkan pilihan yang berikut: **Aktif**, **Ditutup**, **Berbayar** dan **Dibatalkan**, dan boleh diedit. Status tidak disokong untuk Project Operations termasuk **Tertutup** dan **Dibatalkan**. </br> Status ditetapkan kepada **Aktif** apabila invois dicipta. </br>Status hendaklah ditetapkan kepada **Dibayar** hanya selepas invois disahkan.  | 
| **Status Invois Projek** | Tab **Ringkasan** | Tetapkan pilihan yang berikut: **Draf**, **Dalam semakan** dan **Disahkan**, dan boleh diedit. Dalam status **Draf** dan **Dalam Semakan**, invois boleh diedit. Invois tidak boleh diedit selepas invois disahkan. | 
| **Amaun Butiran** | Tab **Ringkasan** | Jumlah amaun pada semua baris invois selepas pendahuluan dan potongan. Medan baca sahaja yang dikunci daripada pengeditan.  Medan ini digunakan untuk mengira amaun akhir. | 
| **Diskaun (%)** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan peratusan diskaun. Medan ini tidak disokong oleh kefungsian Project Operations. Medan ini ialah medan yang tidak disokong.|  
| **Amaun Diskaun** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan amaun diskaun. Medan ini tidak disokong oleh kefungsian Project Operations. Medan ini ialah medan yang tidak disokong. |  
| **Amaun Pra Penghantaran** | **Tab Ringkasan** | Jumlah amaun invois selepas diskaun digunakan. Medan baca sahaja yang dikunci daripada pengeditan. Medan ini digunakan untuk mengira amaun akhir.  | 
| **Amaun Pengangkutan** | Tab **Ringkasan** | Medan ini boleh diedit untuk memasukkan amaun pengangkutan. Medan ini tidak disokong oleh kefungsian Project Operations. Medan ini ialah medan yang tidak disokong. |
| **Jumlah Cukai** | Tab **Ringkasan** | Jumlah cukai daripada semua baris invois ke atas invois. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Jumlah Amaun** | Tab **Ringkasan** | Jumlah amaun selepas diskaun dan cukai. Jumlah tersebut ialah amaun yang perlu dibayar oleh pelanggan. | 

## <a name="project-based-invoice-lines"></a>Baris invois berasaskan projek

Dalam Project Operations, sentiasa ada satu baris invois untuk setiap baris kontrak projek. Baris invois dicipta walaupun tiada aktual. Maklumat berikut tersedia pada baris invois proforma.

| Medan | Lokasi | Penerangan | 
| --- | --- | --- |
| **ID Invois** | Tab **Umum** | Rujukan kepada ID invois. Medan baca sahaja yang dikunci daripada pengeditan. Pautan ID invois boleh digunakan untuk menavigasi kembali ke pengepala invois. | 
| **Nama** | Tab **Umum** | Nama baris invois ditetapkan secara lalai daripada nama baris kontrak. Medan ini boleh diedit. |
| **Project** | Tab **Umum** | Projek berkenaan baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. Pautan projek boleh digunakan untuk menavigasi ke projek. | 
| **Kaedah Pengebilan** | Tab **Umum** | Kaedah pengebilan berkenaan baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Amaun Baris Kontrak** | Tab **Umum** | Amaun kontrak pada baris kontrak projek yang berkaitan. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Diinvois hingga Tarikh** | Tab **Umum** | Jumlah amaun pada semua butiran baris invois bagi invois ini. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Amaun** | Tab **Umum** | Jumlah amaun pada semua butiran baris invois bagi invois ini yang boleh dituntut. Medan baca sahaja yang dikunci daripada pengeditan. Medan ini digunakan untuk mengira amaun akhir pada pengepala invois. | 
| **Cukai** | Tab **Umum** | Jumlah amaun cukai pada semua butiran baris invois bagi baris invois ini. Medan baca sahaja yang dikunci daripada pengeditan. Medan ini digunakan untuk mengira amaun cukai akhir pada pengepala invois. | 
| **Amaun Dilanjutkan** | Tab **Umum** | Jumlah amaun (**Cukai + Amaun**) pada semua butiran baris invois bagi baris invois ini yang boleh dituntut. Medan baca sahaja yang dikunci daripada pengeditan. Medan ini digunakan untuk mengira amaun akhir pada pengepala invois. |

## <a name="invoice-line-details"></a>Butiran baris invois

Setiap baris invois dalam invois projek termasuk butiran baris invois. Butiran baris ini berkaitan dengan aktual jualan yang belum dibilkan dan pencapaian yang berkaitan dengan baris kontrak yang dirujuk mengikut baris invois. Semua transaksi ini ditanda **Bersedia untuk Diinvois**.

Untuk baris **Invois Masa dan Bahan**, butiran baris invois dikumpulkan ke dalam **Boleh dituntut**, **Tidak boleh dituntut** dan **Percuma** pada halaman **Baris Invois**. Butiran **Baris Invois Boleh Dituntut** menambah sehingga jumlah baris invois. **Aktual Percuma** dan **Tidak Boleh Dituntut** tidak menambah sehingga jumlah baris invois.

Untuk baris **Invois Harga Tetap**, butiran baris invois dicipta daripada pencapaian yang ditandakan sebagai **Sedia untuk diinvois** pada baris kontrak yang berkaitan. Selepas butiran baris invois dicipta daripada pencapaian, status pengebilan pada pencapaian dikemas kini kepada **Invois Pelanggan Dicipta**.

### <a name="edit-invoice-line-details"></a>Edit butiran baris invois

Medan berikut tersedia pada butiran baris invois yang disokong oleh aktual jualan yang belum dibilkan.

| Medan | Penerangan |
| --- | --- | 
| **Baris invois** | Rujukan kepada **ID Baris Invois**. Medan ini baca sahaja dan dikunci untuk pengeditan. Pautan ini boleh digunakan untuk menavigasi kembali ke pengepala invois. | 
| **Perihalan** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada medan **Komen Dalaman** pada **Entri Masa** dan daripada medan **Perihalan** pada **Entri Perbelanjaan**. Medan boleh diedit.| 
| **Perihalan Luaran** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada medan **Komen Luaran** pada **Entri Masa** dan medan **Perihalan** pada **Entri Perbelanjaan**. Medan boleh diedit. Perihalan ini boleh digunakan untuk menentukan perkara yang sepatutnya ada pada invois bercetak yang akan dihantar kepada pelanggan. Dalam Project Operations, invois proforma tidak mempunyai semua kefungsian yang diperlukan untuk mengkonfigurasikan tetapan cetak untuk invois. | 
| **Tarikh Mula** | Ini ialah medan baca sahaja yang ditetapkan secara lalai daripada aktual sumber. |
| **Project** | Ini ialah medan baca sahaja yang ditetapkan secara lalai daripada aktual sumber kepada projek pada baris kontrak yang berkaitan. |  
| **Tugas** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Kategori transaksi** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Peranan** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |  
| **Sumber Boleh Ditempah** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Syarikat Penyumberan** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Unit Sumber** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Kuantiti** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |  
| **Jadual Unit** | Untuk butiran baris invois untuk masa, ini sentiasa ditetapkan kepada masa dan tidak boleh diedit. Untuk perbelanjaan, ini ditetapkan secara lalai daripada aktual perbelanjaan sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Unit** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |  
| **Harga** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Mata wang** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Amaun** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Cukai** | Ditetapkan secara lalai daripada aktual sumber. Medan boleh diedit.| 
| **Amaun Dilanjutkan** | Medan dikira, dikira sebagai **Amaun + Cukai**. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Jenis Pengebilan** | Ditetapkan secara lalai daripada aktual sumber. Medan boleh diedit. Memilih **Boleh Dituntut** menambah baris kepada jumlah baris invois. **Percuma** dan **Tidak Boleh Dituntut** akan mengecualikannya daripada jumlah baris invois.| 
| **Pilih Produk** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Produk** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Nama Produk** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |  
| **Perihalan Masukan Manual** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Jenis Transaksi** | Ini ialah medan baca sahaja yang ditetapkan secara lalai daripada aktual sumber kepada to **Jualan Dibilkan**. |  
| **Kelas Transaksi** | Ditetapkan secara lalai daripada aktual sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 

Medan berikut tersedia pada butiran baris invois yang disandarkan oleh pencapaian.

| Medan | Penerangan |
| --- | --- | 
| **Baris invois** | Rujukan kepada **ID Baris Invois**. Medan baca sahaja yang dikunci daripada pengeditan. Pautan boleh digunakan untuk menavigasi kembali ke pengepala invois.  | 
| **Perihalan** | Perihalan butiran baris invois. Ditetapkan secara lalai daripada perihalan pencapaian sumber. | 
|**Perihalan Luaran** | Perihalan butiran baris invois yang ditetapkan secara lalai daripada perihalan pencapaian sumber. Medan ini boleh digunakan untuk menentukan perkara yang sepatutnya ada pada invois bercetak yang akan dihantar kepada pelanggan. Invois proforma dalam Project Operations tidak mempunyai semua kefungsian yang diperlukan untuk mengkonfigurasikan tetapan cetak untuk invois. | 
| **Tarikh Mula** | Ditetapkan secara lalai dari tarikh **Pencapaian** pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Project** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Tugas** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Kategori transaksi** | Medan baca sahaja yang dikunci daripada pengeditan. |
| **Peranan** | Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Sumber Boleh Ditempah** | Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Unit Sumber** | Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Jadual Unit** | Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Unit** | Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Harga** | Ditetapkan secara lalai daripada amaun pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Mata wang** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Amaun** | Ditetapkan secara lalai daripada amaun pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Cukai** | Ditetapkan secara lalai daripada amaun cukai pada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Amaun Dilanjutkan** | Ditetapkan secara lalai daripada amaun dilanjutkan pada pencapaian sumber. Medan boleh diedit. | 
| **Jenis Pengebilan** | Sentiasa ditetapkan secara lalai kepada **Boleh Dituntut**. Medan baca sahaja yang dikunci daripada pengeditan. |
| **Jenis Transaksi** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 
| **Kelas Transaksi** | Ditetapkan secara lalai daripada pencapaian sumber. Medan baca sahaja yang dikunci daripada pengeditan. | 

## <a name="refresh-invoice-transactions"></a>Segar semula transaksi invois

Jika anda mempunyai aktual yang datang selepas invois dicipta, anda boleh memasukkan aktual ini pada invois.

1. Dalam **Pandangan Tunggakan Pengebilan**, tandakan data sebagai **Bersedia untuk Diinvois**.   
2. Buka invois proforma draf dan pada riben **Tindakan**, pilih **Segar Semula Transaksi Baris Invois**.

  Butiran baris invois dicipta untuk sebarang aktual yang bertarikh pada masa lalu dan ditandakan sebagai **Sedia untuk Diinvois** tetapi tidak disertakan pada invois.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
