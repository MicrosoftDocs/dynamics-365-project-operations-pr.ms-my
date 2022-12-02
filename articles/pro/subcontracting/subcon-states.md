---
title: Peralihan keadaan pada subkontrak
description: Artikel ini menerangkan tentang peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations apabila subkontrak dicipta, dilaksanakan dan ditutup.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522942"
---
# <a name="state-transitions-on-a-subcontract"></a>Peralihan keadaan pada subkontrak 

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini menerangkan tentang peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations. Setiap keadaan diwakili sebagai sama ada draf, disahkan, ditutup atau dibatalkan. Imej berikut mewakili peralihan keadaan.

![Model keadaan subkontrak](../media/SubconStates.png)  

Jadual berikut menyediakan penerangan tentang perkara yang diwakili oleh setiap keadaan dalam kitaran hayat subkontrak dalam Project Operations.

| Negeri | Description | Peralihan dibenarkan |
| --- | --- | --- |
| Draf | Ini mewakili keadaan awal subkontrak. Rundingan dengan penjual sedang berjalan. Baris dan harga tertakluk pada pengubahsuaian. Satu subkontrak dalam keadaan ini boleh digunakan untuk anggaran dan keperluan projek kakitangan untuk sumber dan bahan. Boleh juga dirujuk pada masa, perbelanjaan dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini boleh diedit dan dipadamkan. | Disahkan |
| Disahkan | Ini mewakili peringkat subkontrak selepas rundingan dengan vendor berkenaan harga dan item baris yang dibeli adalah lengkap. Walau bagaimanapun, penghantaran bahan yang sebenar dan/atau kerja oleh sumber subkontrak masih berterusan. Satu subkontrak dalam keadaan ini boleh digunakan untuk anggaran dan keperluan projek kakitangan untuk sumber dan bahan. Boleh juga dirujuk pada masa, perbelanjaan dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. Butang **Batal** membolehkan anda membatalkan subkontrak yang disahkan. Butang **Buka semula** membolehkan anda membuka semula subkontrak untuk mengembalikannya kepada status **Draf**. Gunakan butang **Tutup** untuk menutup subkontrak yang disahkan. | Tertutup <br> Dibatalkan <br> Draf |
| Tertutup | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak adalah lengkap. Satu subkontrak dalam keadaan ini tidak boleh lagi digunakan untuk anggaran dan keperluan projek kakitangan untuk sumber dan bahan. Selain itu, tidak boleh lagi dirujuk pada masa, perbelanjaan dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |
| Dibatalkan | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak tidak lagi diperlukan. Satu subkontrak dalam keadaan ini tidak boleh digunakan untuk anggaran dan keperluan projek kakitangan bagi sumber dan bahan dan juga tidak boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
