---
title: Set kelulusan
description: Artikel ini menerangkan cara bekerja dengan set kelulusan, permintaan dan subset operasi tersebut.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524928"
---
# <a name="approval-sets"></a>Set kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Set kelulusan mengumpulkan permintaan kelulusan bersama ke dalam subset operasi yang lebih kecil. Pengelompokan ini membolehkan kelulusan diproses mengikut projek, mengikut tertib dan membolehkan percubaan semula dan penjujukan. Mengelompokkan permintaan kelulusan bersama akan meningkatkan kebolehpercayaan dan kebolehjejakan pemprosesan kelulusan untuk jumlah kelulusan yang besar.

Set kelulusan menunjukkan keadaan pemprosesan keseluruhan bagi rekod yang berkaitan. Apabila rekod kelulusan diproses dengan menggunakan set kelulusan, rekod beralih daripada **Diserahkan** kepada **Diluluskan** dan tidak lagi dipautkan dengan set kelulusan. Jika rekod gagal apabila ia diserahkan untuk diluluskan, rekod masih dalam status **Diserahkan** dan set kelulusan ditanda sebagai gagal. Set kelulusan log mesej ralat kegagalan.

## <a name="processing-approvals-and-approval-sets"></a>Kelulusan pemprosean dan set kelulusan
Kelulusan yang dibariskan untuk pemprosesan boleh dilihat dalam pandangan **Kelulusan Pemprosesan**. Sistem memproses semua entri berbilang kali secara tak segerak, termasuk mencuba semula kelulusan jika percubaan sebelumnya gagal.

Medan **Set Kelulusan Seumur Hidup** merekodkan bilangan baki percubaan untuk memproses set sebelum ia ditanda sebagai gagal.

Set kelulusan diproses melalui pengaktifan berkala berdasarkan **Aliran Awan** dinamakan **Project Service - Jadualkan Set Kelulusan Projek Secara Berulang**. Ini boleh didapati dalam **Penyelesaian** yang dinamakan **Project Operations**. 

Pastikan bahawa aliran diaktifkan dengan melengkapkan langkah berikut.

1. Sebagai pentadbir, daftar masuk ke [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Di sudut kanan atas, bertukar ke persekitaran yang anda gunakan untuk Dynamics 365 Project Operations.
3. Pilih **Penyelesaian** untuk menyenaraikan penyelesaian yang dipasang dalam persekitaran.
4. Dalam senarai penyelesaian, pilih **Project Operations**.
5. Tukar penapis daripada **Semua** kepada **Aliran Awan**.
6. Sahkan bahawa aliran **Project Service – Jadualkan Set Kelulusan Projek Secara Berulang** ditetapkan kepada **Hidup**. Jika tidak, pilih aliran, kemudian **Hidupkan**.
7. Sahkan bahawa pemprosesan berlaku setiap lima minit dengan menyemak senarai **Kerja Sistem** dalam kawasan **Tetapan** dalam persekitaran Project Operations Dataverse anda.

## <a name="failed-approvals-and-approval-sets"></a>Kelulusan gagal dan set kelulusan
Pandangan **Kelulusan Gagal** menyenaraikan semua kelulusan yang memerlukan campur tangan pengguna. Buka log set kelulusan berkaitan untuk mengenal pasti punca kegagalan.
Memilih **Cuba semula** mennambah kepada kiraan jangka hayat set kelulusan, mengalih keluar kelulusan yang ditetapkan kembali ke status **Pemprosesan** dan percubaan untuk memproses baki rekod.

## <a name="configure-approval-sets"></a>Konfigurasikan set kelulusan

### <a name="enable-the-approval-sets-feature"></a>dayakan ciri set Kelulusan
Sebelum anda mendayakan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini. Selepas ciri ini didayakan, ia tidak boleh dinyahdayakan.

- Pergi ke halaman **Parameter projek** dan pilih **Kawalan Ciri** > **Dayakan Kelulusan Moden**.

### <a name="configuring-the-asynchronous-threshold"></a>Mengkonfigurasi ambang tidak segerak 
Apabila set kelulusan dicipta, pemprosesan bergerak ke latar belakang apabila bilangan rekod yang dipilih untuk diluluskan melebihi ambang yang dinyatakan. Gunakan medan **Ambang Tidak Segerak** untuk mengkonfigurasikan apabila pemprosesan kelulusan sepatutnya dijalankan secara segerak atau tidak segerak. Pilih salah satu nilai yang berikut:

  - Sifar: Semua permohonan perlu diproses secara tidak segerak. 
  - Bilangan yang lebih besar daripada sifar: Kelulusan diproses secara tidak segerak hanya apabila bilangan kelulusan yang diserahkan melebihi nilai ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
