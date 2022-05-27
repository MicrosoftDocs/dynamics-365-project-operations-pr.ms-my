---
title: Set kelulusan
description: Topik ini menerangkan cara bekerja dengan set kelulusan, permintaan dan subset operasi tersebut.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576235"
---
# <a name="approval-sets"></a>Set kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Set kelulusan mengumpulkan permintaan kelulusan bersama ke dalam subset operasi yang lebih kecil. Pengelompokan ini membolehkan kelulusan diproses mengikut projek, mengikut tertib dan membolehkan percubaan semula dan penjujukan. Mengelompokkan permintaan kelulusan bersama akan meningkatkan kebolehpercayaan dan kebolehjejakan pemprosesan kelulusan untuk jumlah kelulusan yang besar.

Set kelulusan menunjukkan keadaan pemprosesan keseluruhan bagi rekod yang berkaitan. Apabila rekod kelulusan diproses dengan menggunakan set kelulusan, rekod beralih daripada **Diserahkan** kepada **Diluluskan** dan tidak lagi dipautkan dengan set kelulusan. Jika rekod gagal apabila ia diserahkan untuk diluluskan, rekod masih dalam status **Diserahkan** dan set kelulusan ditanda sebagai gagal. Set kelulusan log mesej ralat kegagalan.

## <a name="processing-approvals-and-approval-sets"></a>Kelulusan pemprosean dan set kelulusan
Kelulusan yang dibariskan untuk pemprosesan boleh dilihat dalam pandangan **Kelulusan Pemprosesan**. Sistem memproses semua entri berbilang kali secara tak segerak, termasuk mencuba semula kelulusan jika percubaan sebelumnya gagal.

Medan **Set Kelulusan Seumur Hidup** merekodkan bilangan baki percubaan untuk memproses set sebelum ia ditanda sebagai gagal.

Set kelulusan diproses melalui pengaktifan berkala berdasarkan Aliran **Awan bernama** **Perkhidmatan Projek - Jadualkan Set Kelulusan Projek Berulang**. Ini terdapat dalam Penyelesaian **bernama** **Operasi Projek**. 

Pastikan aliran diaktifkan dengan melengkapkan langkah-langkah berikut.

1. Sebagai pentadbir, log masuk ke [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Di sudut kanan atas, beralih ke persekitaran yang anda gunakan untuk Dynamics 365 Project Operations.
3. Pilih **Penyelesaian** untuk menyenaraikan penyelesaian yang dipasang dalam persekitaran.
4. Dalam senarai penyelesaian, pilih **Operasi** Projek.
5. Tukar penapis daripada **Semua** kepada **Aliran** Awan.
6. Sahkan bahawa **Perkhidmatan Projek – Jadualkan Berulang Set** Kelulusan Projek disetkan kepada **Hidup**. Jika tidak, pilih aliran, kemudian pilih **Hidupkan**.
7. Sahkan bahawa pemprosesan berlaku setiap lima minit dengan **menyemak senarai Kerja** Sistem dalam **kawasan Tetapan** dalam persekitaran Operasi Dataverse Projek anda.

## <a name="failed-approvals-and-approval-sets"></a>Kelulusan gagal dan set kelulusan
Pandangan **Kelulusan Gagal** menyenaraikan semua kelulusan yang memerlukan campur tangan pengguna. Buka log set kelulusan berkaitan untuk mengenal pasti punca kegagalan.
Memilih **Cuba semula** mennambah kepada kiraan jangka hayat set kelulusan, mengalih keluar kelulusan yang ditetapkan kembali ke status **Pemprosesan** dan percubaan untuk memproses baki rekod.

## <a name="configure-approval-sets"></a>Konfigurasikan set kelulusan

### <a name="enable-the-approval-sets-feature"></a>dayakan ciri set Kelulusan
Sebelum anda mendayakan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.

- Pergi ke halaman **Parameter projek** dan pilih **Kawalan Ciri** > **Dayakan Kelulusan Moden**.

### <a name="turn-off-the-approval-sets-feature"></a>Matikan ciri set Kelulusan
Sebelum anda mematikan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.

- Pergi ke halaman **Parameter Projek** dan pilih **Kawalan Ciri** > **Nyahdayakan Kelulusan Moden**.

### <a name="configuring-the-asynchronous-threshold"></a>Mengkonfigurasi ambang tidak segerak 
Apabila set kelulusan dicipta, pemprosesan bergerak ke latar belakang apabila bilangan rekod yang dipilih untuk diluluskan melebihi ambang yang dinyatakan. Gunakan medan **Ambang Tidak Segerak** untuk mengkonfigurasikan apabila pemprosesan kelulusan sepatutnya dijalankan secara segerak atau tidak segerak. Pilih salah satu nilai yang berikut:

  - Sifar: Semua permohonan perlu diproses secara tidak segerak. 
  - Bilangan yang lebih besar daripada sifar: Kelulusan diproses secara tidak segerak hanya apabila bilangan kelulusan yang diserahkan melebihi nilai ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
