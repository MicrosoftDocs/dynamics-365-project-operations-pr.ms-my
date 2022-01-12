---
title: Ralat tidak sepadan mata wang
description: Topik ini menyediakan maklumat penyelesaian masalah tentang ralat tidak sepadan mata wang yang berlaku apabila anda menyimpan jenis rekod tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903740"
---
# <a name="currency-mismatch-error"></a>Ralat tidak sepadan mata wang 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila anda menyimpan projek, kontrak, sebut harga atau sumber boleh ditempah, anda mungkin menerima ralat, **Memiliki mata wang syarikat tidak sepadan dengan mata wang unit kontrak. Pilih syarikat pemilik atau unit kontrak yang berbeza untuk diteruskan**. Ini kerana terdapat ketidakpadanan mata wang antara mata wang unit kontrak untuk rekod dan mata wang syarikat pemilik.


## <a name="resolution"></a>Resolusi

Untuk menyelesaikan isu ini, lakukan perkara berikut:
- Sahkan mata wang unit kontrak untuk rekod ini. Anda boleh melihat mata wang dengan membuka rekod unit organisasi dan mengesahkan nilai pada **tab Umum dalam medan Mata** **Wang**.
- Sahkan mata wang syarikat pemilik. Anda boleh melihat mata wang dengan pergi ke **Lejar Berkaitan** > **dalam rekod** syarikat. Dwiklik rekod lejar yang dikaitkan dengan syarikat dan sahkan nilai pada **tab Umum dalam medan Mata wang** **Perakaunan**.

Jika mata wang yang ditetapkan dalam unit kontrak dan rekod lejar tidak sepadan, laraskan konfigurasi atau pilih nilai yang berbeza apabila anda menyimpan rekod. Sistem ini memerlukan rekod-rekod ini sepadan untuk memastikan aliran invois antara syarikat yang betul. Untuk maklumat lanjut tentang konfigurasi antara syarikat, lihat [Mencipta transaksi antara syarikat](../../project-accounting/create-intercompany-transactions.md).

Jika rekod syarikat tidak mempunyai rekod lejar yang berkaitan, ini menunjukkan bahawa terdapat konfigurasi yang hilang semasa menyediakan persekitaran. Konfigurasi mesti diperbetulkan oleh pentadbir sistem. Pentadbir sistem mesti pergi ke **konfigurasi dwi-tulis** dan berhenti dan mulakan semula peta **dwi-tulis Ledgers** dengan penyegerakan awal peta ini dan ia adalah prasyarat. Untuk mendapatkan maklumat lanjut, lihat [versi peta dwitulis Project Operations](../../environment/resource-dual-write-maps.md).
