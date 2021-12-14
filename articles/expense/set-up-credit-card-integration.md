---
title: Sediakan integrasi kad kredit
description: Topik ini menerangkan cara bekerja dengan transaksi kad kredit berkaitan perbelanjaan.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 49c8f2369a8be41fbc04c74bdb6b565b4f4b7b79
ms.sourcegitcommit: 9f26cf8bb640af1eb9f7f0872805965d7ffcb9d3
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/19/2021
ms.locfileid: "7826267"
---
# <a name="set-up-credit-card-integration"></a>Sediakan integrasi kad kredit

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Transaksi kad kredit berkaitan perbelanjaan boleh ditetapkan supaya ia diimport secara automatik pada jadual yang berulang. Secara alternatif, transaksi boleh diimport secara manual apabila diperlukan. Transaksi kad kredit diimport melalui entiti data transaksi kad kredit.

## <a name="import-credit-card-transactions"></a>Import transaksi kad kredit

Untuk mengimport transaksi kad kredit, ikut langkah ini:

1. Pada halaman **Transaksi kad kredit**, pilih **Import transaksi**. Jika anda membuka pengurusan data buat kali pertama, sistem mesti mengemas kini senarai entiti data sebelum anda boleh meneruskan.
2. Dalam medan **Nama**, masukkan perihalan unik untuk kerja import.
3. Dalam medan **Format data sumber**, pilih format fail yang mengandungi transaksi kad kredit untuk diimport.
4. Pilih **Muat naik** dan kemudian cari serta pilih fail untuk diimport.
5. Selepas fail telah dimuat naik, sahkan pemetaan fail transaksi kad kredit dan lajur entiti data transaksi kad kredit dengan memilih pautan **Lihat peta** pada jubin. Jika terdapat ralat pemetaan atau jika anda mesti mengubah pemetaan, membuat perubahan pemetaan sama ada dalam tab **Visualisasi Pemetaan** atau tab **Butiran Pemetaan**.
6. Untuk mengautomasikan transaksi kad kredit, pilih **Cipta kerja data berulang**. Anda kemudian boleh menetapkan pengulangan yang menakrifkan kekerapan transaksi kad kredit diimport. Apabila anda selesai, pilih **OK**.
7. Untuk mengimport fail yang dipilih sekarang, pilih **Import**.
8. Jika ralat berlaku semasa import, anda boleh melihat log pelaksanaan atau data pementasan untuk melihat ralat yang anda mesti betulkan untuk membantu memastikan import yang berjaya.

> [!NOTE]
> Jika anda perlu mengimport lebih daripada satu format fail, anda mesti mencipta kerja import berasingan untuk setiap jenis format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tugaskan semula transaksi kad kredit untuk pekerja yang telah ditamatkan

Selepas rekod pekerja ditamatkan, akaun Perkhidmatan Domain Active Directory (AD DS) pekerja dinyahdayakan. Walau bagaimanapun, kemungkinan terdapat transaksi kad kredit aktif yang masih perlu dibelanjakan dan dibayar balik. Pada halaman **Transaksi kad kredit**, anda boleh menugaskan pekerja untuk sebarang transaksi kad kredit yang pekerja berkaitan telah ditamatkan.

Pilih satu atau lebih transaksi kad kredit dan kemudian pilih **Tugaskan semula transaksi**. Anda kemudian boleh memilih pekerja lain untuk transaksi kad kredit yang ditugaskan. Selepas transaksi kad kredit telah ditugaskan semula, ia boleh dipilih untuk laporan perbelanjaan dan dibayar melalui proses biasa bagi pembayaran balik laporan perbelanjaan.

## <a name="delete-credit-card-transactions"></a>Padamkan transaksi kad kredit 

Kadangkala, selepas transaksi kad kredit diimport, transaksi tertentu mungkin perlu dipadamkan. Ini mungkin kerana transaksi adalah pendua atau kerana data tidak tepat. Pentadbir boleh menggunakan ciri **"Padamkan transaksi kad kredit"** untuk memilih dan memadamkan transaksi kad kredit yang **tidak dilampirkan** kepada laporan perbelanjaan. 

1. Pergi ke **Tugas berkala** > **Padamkan transaksi kad kredit**.
2. Pilih **Tapis** dan sediakan maklumat untuk mengenal pasti rekod untuk disertakan.
3. Pilih **OK** untuk memadamkan rekod. 

## <a name="storing-credit-card-numbers"></a>Menyimpan nombor kad kredit

Tiga pilihan tersedia untuk menyimpan nombor kad kredit. Nombor kad kredit disimpan di **halaman Parameter pengurusan** perbelanjaan.

- **Halang kemasukan nombor kad** - Nombor kad kredit tidak disimpan.
- **Nombor kad cincangan (simpan empat digit terakhir)** - Empat digit terakhir nombor kad kredit disimpan dalam format yang disulitkan.
- **Nombor kad** kedai - Nombor kad kredit disimpan dalam format yang tidak disulitkan. Pilihan ini tidak mematuhi Standard Keselamatan Data Industri Kad Pembayaran (PCI). Oleh itu, untuk memastikan organisasi mereka mematuhi peraturan PCI DSS, pentadbir organisasi harus memilih sama ada untuk tidak menyimpan nombor kad kredit atau menyimpan nombor kad hash.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
