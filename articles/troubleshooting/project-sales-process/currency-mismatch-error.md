---
title: Ralat ketakpadanan mata wang
description: Artikel ini menyediakan maklumat penyelesaian masalah tentang ralat ketakpadanan yang berlaku apabila anda menyimpan jenis rekod tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914735"
---
# <a name="currency-mismatch-error"></a>Ralat ketakpadanan mata wang 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila anda menyimpan projek, kontrak, sebut harga atau sumber yang boleh ditempah, anda mungkin menerima ralat, **Mata wang syarikat pemilikan tidak sepadan dengan mata wang unit kontrak. Pilih syarikat pemilikan atau unit kontrak yang berbeza untuk meneruskan**. Hal ini kerana terdapat ketakpadanan mata wang antara mata wang unit kontrak untuk rekod dan mata wang syarikat pemilikan.


## <a name="resolution"></a>Resolusi

Untuk menyelesaikan isu ini, lakukan perkara berikut:
- Sahkan mata wang unit kontrak untuk rekod ini. Anda boleh melihat mata wang dengan membuka rekod unit organisasi dan mengesahkan nilai pada tab **Umum** dalam medan **Mata Wang**.
- Sahkan mata wang syarikat pemilikan. Anda boleh melihat mata wang dengan pergi ke **Berkaitan** > **Lejar** dalam rekod syarikat. Dwiklik rekod lejar yang berkaitan dengan syarikat dan sahkan nilai pada tab **Umum** dalam medan **Mata wang perakaunan**.

Jika mata wang yang ditetapkan dalam unit kontrak dan rekod lejar tidak sepadan, laraskan konfigurasi atau pilih nilai yang berbeza apabila anda menyimpan rekod. Sistem memerlukan rekod-rekod ini sepadan bagi memastikan aliran invois antara syarikat yang betul. Untuk mendapatkan maklumat lanjut tentang konfigurasi antara syarikat, lihat [Cipta transaksi antara syarikat](../../project-accounting/create-intercompany-transactions.md).

Jika rekod syarikat tidak mempunyai rekod lejar yang berkaitan, ini menunjukkan bahawa terdapat konfigurasi yang hilang apabila menyediakan persekitaran. Konfigurasi mesti dibetulkan oleh pentadbir sistem. Pentadbir sistem mesti pergi ke **Konfigurasi dwitulis** dan berhenti dan memulakan semula **Peta dwitulis lejar** dengan penyegerakan awal peta ini dan prasyaratnya. Untuk mendapatkan maklumat lanjut, lihat [versi peta dwitulis Project Operations](../../environment/resource-dual-write-maps.md).
