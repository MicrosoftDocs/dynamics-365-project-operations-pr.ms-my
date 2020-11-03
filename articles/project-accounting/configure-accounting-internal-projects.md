---
title: Konfigurasi perakaunan untuk projek dalaman
description: Topik ini menyediakan maklumat tentang cara untuk menyediakan amalan perakaunan bagi projek dalaman dalamProject Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081162"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurasi perakaunan untuk projek dalaman

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Projek dalaman membolehkan syarikat menjejak kos yang berkaitan dengan aktiviti yang tidak dibilkan kepada pelanggan. Contoh projek dalaman termasuk:

- Membangunkan produk, seperti aplikasi mudah alih dan menjejaki kos yang berkaitan dengan pembangunan.
- Menguruskan masa dan perbelanjaan prajualan. Projek dalaman prajualan ini boleh ditukar kemudian kepada projek yang boleh dibilkan jika sebut harga dimenangi.

Sebarang projek yang tidak dikaitkan dengan kontrak dalam Dynamics 365 Project Operations dianggap sebagai dalaman. Profil kos dan hasil projek tidak digunakan untuk menentukan peraturan perakaunan untuk projek. Kos projek dalaman sentiasa disiar menggunakan prinsip keuntungan dan kerugian. Akaun lejar untuk siaran ditakrifkan pada halaman **Penyediaan penyiaran lejar**.

- Transaksi masa disiarkan dengan mendebitkan akaun **Kos** dan mengkreditkan akaun **Peruntukan gaji**.
- Transaksi perbelanjaan disiarkan dengan mendebitkan akaun **Kos** dan mengkreditkan **Akaun ofset untuk perbelanjaan**.

Selepas transaksi disiarkan kepada projek, jika projek tersebut dikaitkan dengan kontrak projek, sistem membalikkan semua transaksi terkumpul dan mencipta transaksi boleh dibilkan baharu. Transaksi boleh dibilkan mengikut peraturan perakaunan yang ditakrifkan dalam kos Projek dan profil hasil.


