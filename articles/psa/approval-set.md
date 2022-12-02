---
title: Set kelulusan dalam Project Service Automation
description: Artikel ini menyediakan maklumat tentang set, permintaan kelulusan dan subset operasi tersebut.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 568815967b909d2a5ee9bf40b4fee97e0ad4d295
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927063"
---
# <a name="approval-sets-in-project-service-automation"></a>Set kelulusan dalam Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Set kelulusan mengumpulkan permintaan kelulusan bersama ke dalam subset operasi yang lebih kecil. Pengumpulan ini membolehkan kelulusan diproses mengikut pelaksanaan Projek dan membolehkan untuk mencuba semula dan penjujukan. Pengumpulan meningkatkan kebolehpercayaan dan kebolehkesanan pemprosesan kelulusan untuk jumlah kelulusan yang besar.

Set kelulusan menunjukkan keadaan pemprosesan keseluruhan bagi rekod yang berkaitan. Apabila rekod kelulusan diproses dengan menggunakan set kelulusan, rekod bergerak daripada **Diserahkan** kepada **Diluluskan** dan dinyahpautkan daripada set kelulusan. Jika rekod gagal apabila ia diserahkan untuk diluluskan, rekod masih dalam status **Diserahkan** dan set kelulusan ditanda sebagai gagal. Set kelulusan log mesej ralat kegagalan.

## <a name="processing-approvals-and-approval-sets"></a>Kelulusan pemprosean dan set kelulusan
Kelulusan yang dibariskan untuk pemprosesan boleh dilihat dalam pandangan **Kelulusan Pemprosesan**. Sistem mencuba untuk memproses semua penyertaan beberapa kali secara segerak, termasuk mencuba semula kelulusan jika percubaan sebelumnya gagal.

Medan **Set Kelulusan Seumur Hidup** merekodkan bilangan baki percubaan untuk memproses set sebelum ia ditanda sebagai gagal.

## <a name="failed-approvals-and-approval-sets"></a>Kelulusan gagal dan set kelulusan
Pandangan **Kelulusan gagal** menyenaraikan semua kelulusan yang memerlukan campur tangan pengguna. Buka log set kelulusan berkaitan untuk mengenal pasti punca kegagalan.
Memilih **Cuba semula** mennambah kepada kiraan jangka hayat set kelulusan, mengalih keluar kelulusan yang ditetapkan kembali ke status **Pemprosesan** dan percubaan untuk memproses baki rekod.

## <a name="configure-approval-sets"></a>Konfigurasikan set kelulusan

###  <a name="enable-the-approval-sets-feature"></a>dayakan ciri set Kelulusan
Sebelum anda mendayakan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.

- Pergi ke halaman **Parameter projek** dan pilih **Kawalan Ciri** > **Dayakan Kelulusan Moden**.

### <a name="turn-off-the-approval-sets-feature"></a>Matikan ciri set Kelulusan
Sebelum anda mematikan ciri set Kelulusan, sahkan bahawa tiada kelulusan diproses pada masa ini.

- Pergi ke halaman **Parameter Projek** dan pilih **Kawalan Ciri** > **Nyahdayakan Kelulusan Moden**.

### <a name="configuring-the-asynchronous-threshold"></a>Mengkonfigurasi ambang tidak segerak 
Apabila set kelulusan dicipta, pemprosesan bergerak ke latar belakang apabila bilangan rekod yang dipilih untuk diluluskan melebihi ambang yang dinyatakan. Gunakan medan **Ambang Tidak Segerak** untuk mengkonfigurasikan apabila pemprosesan kelulusan sepatutnya dijalankan secara segerak atau tidak segerak.
Nilai yang sah ialah:

  - Sifar: Semua permohonan perlu diproses secara tidak segerak. 
  - Bilangan yang lebih besar daripada sifar: Kelulusan diproses secara tidak segerak hanya apabila bilangan kelulusan yang diserahkan melebihi nilai ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
