---
title: Ralat tidak sepadan mata wang
description: Topik ini menyediakan maklumat penyelesaian masalah tentang ralat ketidakpadanan mata wang yang berlaku apabila anda menyimpan jenis rekod tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589759"
---
# <a name="currency-mismatch-error"></a>Ralat tidak sepadan mata wang 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila anda menyimpan projek, kontrak, sebut harga, atau sumber yang boleh ditempah, anda mungkin menerima ralat, **Memiliki mata wang syarikat tidak sepadan dengan mata wang unit kontrak. Pilih syarikat pemilik atau unit kontrak yang berbeza untuk meneruskan**. Ini kerana terdapat ketidakpadanan mata wang antara mata wang unit kontrak untuk rekod dan mata wang syarikat yang memiliki.


## <a name="resolution"></a>Resolusi

Untuk menyelesaikan isu ini, lakukan perkara berikut:
- Sahkan mata wang unit kontrak untuk rekod ini. Anda boleh melihat mata wang dengan membuka rekod unit organisasi dan mengesahkan nilai pada **tab Umum** dalam **medan Mata Wang**.
- Sahkan mata wang syarikat pemilik. Anda boleh melihat mata wang dengan pergi ke **Lejar** > **Berkaitan** dalam rekod syarikat. Dwiklik rekod lejar yang dikaitkan dengan syarikat dan sahkan nilai pada **tab Umum** dalam **medan Mata wang** Perakaunan.

Jika mata wang yang ditetapkan dalam unit kontrak dan rekod lejar tidak sepadan, laraskan konfigurasi atau pilih nilai yang berbeza apabila anda menyimpan rekod. Sistem ini memerlukan rekod ini untuk dipadankan untuk memastikan aliran invois antara syarikat yang betul. Untuk maklumat lanjut tentang konfigurasi antara syarikat, lihat [Mencipta transaksi antara syarikat](../../project-accounting/create-intercompany-transactions.md).

Jika rekod syarikat tidak mempunyai rekod lejar yang berkaitan, ini menunjukkan bahawa terdapat konfigurasi yang hilang semasa menyediakan persekitaran. Konfigurasi mesti diperbetulkan oleh pentadbir sistem. Pentadbir sistem mesti pergi ke **konfigurasi** Dwi-tulis dan berhenti dan memulakan semula **Ledgers dwi-tulis peta** dengan penyegerakan awal peta ini dan prasyaratnya. Untuk mendapatkan maklumat lanjut, lihat [versi peta dwitulis Project Operations](../../environment/resource-dual-write-maps.md).
