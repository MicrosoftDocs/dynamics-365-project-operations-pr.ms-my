---
title: Sediakan integrasi kad kredit
description: Topik ini menerangkan cara mengimport dan mengekalkan transaksi kad kredit yang berkaitan dengan perbelanjaan.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276179"
---
# <a name="set-up-credit-card-integration"></a>Sediakan integrasi kad kredit

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Transaksi kad kredit berkaitan perbelanjaan boleh ditetapkan supaya ia diimport secara automatik pada jadual yang berulang. Secara alternatif, transaksi boleh diimport secara manual apabila diperlukan. Transaksi kad kredit diimport melalui entiti data transaksi kad Kredit.

## <a name="import-credit-card-transactions"></a>Import transaksi kad kredit

1. Pada halaman **Transaksi kad kredit**, pilih **Import transaksi**. Jika anda sedang membuka pengurusan data buat kali pertama, sistem mesti mengemas kini senarai entiti data sebelum anda boleh meneruskan.
2. Dalam medan **Nama**, masukkan description unik bagi kerja import.
3. Dalam medan **Format data sumber**, pilih format fail yang mengandungi transaksi kad kredit untuk diimport.
4. Pilih **Muat naik** dan kemudian cari serta pilih fail untuk diimport.
5. Selepas fail dimuat naik, sahkan fail transaksi kad kredit dan lajur entiti data transaksi kad kredit dengan memilih pautan **Lihat peta** pada jubin. Jika terdapat ralat pemetaan atau jika anda mesti mengubah pemetaan, membuat perubahan pemetaan sama ada dalam tab **Visualisasi Pemetaan** atau tab **Butiran Pemetaan**.
6. Untuk mengautomasikan transaksi kad kredit, pilih **Cipta kerja data berulang**. Anda kemudian boleh menetapkan pengulangan yang menakrifkan kekerapan transaksi kad kredit diimport. Apabila anda telah selesai, pilih **OK**.
7. Untuk mengimport fail yang dipilih sekarang, pilih **Import**.
8. Jika ralat berlaku semasa import, anda boleh melihat log pelaksanaan atau data pementasan untuk melihat ralat yang mesti anda baiki bagi membantu menjamin import yang berjaya.

> [!NOTE]
> Jika anda mesti mengimport lebih daripada satu format fail, anda mesti mencipta kerja import berasingan untuk setiap jenis format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Tugaskan semula transaksi kad kredit untuk pekerja yang telah ditamatkan

Selepas rekod pekerja ditamatkan, akaun Active Directory Domain Services (AD DS) pekerja dinyahdayakan. Walau bagaimanapun, kemungkinan terdapat transaksi kad kredit aktif yang masih perlu dibelanjakan dan dibayar balik. Daripada halaman **Transaksi kad kredit**, anda boleh menugaskan semula pekerja untuk sebarang transaksi kad kredit bagi pekerja berkaitan yang telah ditamatkan.

Pilih satu atau lebih transaksi kad kredit dan kemudian pilih **Tugaskan semula transaksi**. Anda kemudian boleh memilih pekerja lain untuk transaksi kad kredit yang ditugaskan. Selepas transaksi kad kredit telah ditugaskan semula, ia boleh dipilih untuk laporan perbelanjaan dan dibayar melalui proses biasa bagi pembayaran balik laporan perbelanjaan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]