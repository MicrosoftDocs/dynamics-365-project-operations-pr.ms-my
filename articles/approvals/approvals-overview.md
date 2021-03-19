---
title: Gambaran keseluruhan kelulusan
description: Topik ini memberikan maklumat tentang bekerja dengan kelulusan dalam Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a7573b95998387453b72dbcb73c3de977ed7d913
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290370"
---
# <a name="approvals-overview"></a>Gambaran keseluruhan kelulusan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Serahan Masa dan Perbelanjaan bergerak melalui aliran kerja kelulusan. Selepas entri diluluskan, transaksi direkodkan dalam aktual atau masa ditempah dalam jadual.

## <a name="approvals-workflow"></a>Aliran kerja kelulusan
Apabila anda mencipta dan menyerahkan entri masa atau perbelanjaan, entri kelulusan akan dicipta. Pelulus Projek atau pengurus anda menyemak dan meluluskan entri anda. Jika entri berkaitan dengan projek, apabila ia diluluskan, aktual akan dicipta. Ini membolehkan kos dan pengebilan dijejak. 

## <a name="approve-an-entry"></a>Meluluskan entri
Borang **Kelulusan** membolehkan anda bertukar antara pandangan yang berbeza supaya anda boleh melihat jenis kelulusan yang berbeza.
  
1. Pergi ke borang **Kelulusan** dan pilih **Perbelanjaan**, **Masa** atau **Tarik balik**.
2. Semak setiap kelulusan dan pilih kelulusan yang anda mahu luluskan.
3. Pilih **Luluskan** untuk meluluskan entri yang dipilih.
Sistem akan memproses entri ini dan mencipta aktual atau tempahan.

## <a name="reject-an-entry"></a>Tolak entri
Sebagai pelulus Projek, anda mungkin perlu menghantar semula entri kepada pengguna untuk pembetulan.
  
1. Pergi ke borang **Kelulusan** dan pilih entri untuk ditolak. 
2. Pilih **Tolak**.
3. Pilihan - Tambah komen dalam dialog **Komen penolakan** untuk memberitahu pengguna sebab entri tersebut ditolak.
4. Pilih **OK**. Entri tersebut akan dikembalikan kepada pengguna.
  
## <a name="recall-entries"></a>Tarik balik entri
Pada satu ketika, anda mungkin perlu menarik balik entri yang telah diserahkan. Jika entri tersebut tidak diluluskan, ia akan dikembalikan dengan segera. Entri yang telah diluluskan bagaimanapun, mungkin mempunyai kesan bahan. Pelulus Projek dikehendaki meluluskan tarik balik ini untuk membalikkan transaksi dalam Aktual.

## <a name="specify-project-approvers"></a>Nyatakan Pelulus projek
Setiap projek mempunyai beberapa orang ahli pasukan projek. Anda boleh menentukan ahli pasukan yang juga merupakan pelulus projek.

1. Pergi ke borang **Projek** dan buka projek daripada senarai.
2. Pada tab **Pasukan**, pilih ahli pasukan yang akan menjadi Pelulus projek dan kemudian pilih **Edit**.
3. Tetapkan medan **Pelulus Projek** kepada **Ya**.
4. Pilih **Simpan**.
5. Ulangi langkah 2-4 untuk menambah Pelulus projek tambahan.

## <a name="configure-the-users-manager"></a>Konfigurasikan pengurus pengguna

1. Pergi ke **Tetapan** > **Keselamatan** > **Pengguna**.
2. Pilih pengguna yang anda akan tugaskan seorang pengurus dan dalam kawasan **Maklumat Organisasi**, pilih pengurus daripada senarai. 
3. Pilih **Simpan**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]