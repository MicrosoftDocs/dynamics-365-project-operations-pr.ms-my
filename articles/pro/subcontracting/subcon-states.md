---
title: Peralihan keadaan pada subkontrak
description: Artikel ini menerangkan peralihan negeri pada subkontrak dalam Microsoft Dynamics 365 Project Operations sebagai subkontrak dicipta, dilaksanakan dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919749"
---
# <a name="state-transitions-on-a-subcontract"></a>Peralihan keadaan pada subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan peralihan negeri pada subkontrak dalam Microsoft Dynamics 365 Project Operations. Setiap negeri diwakili sebagai sama ada draf, disahkan, ditutup, atau dibatalkan. Imej berikut mewakili peralihan negeri.

![Model keadaan subkontrak](../media/SubconStates.png)  

Jadual berikut memberikan perihalan tentang apa yang diwakili oleh setiap negeri dalam kitaran hayat subkontrak dalam Operasi Projek.

| Negeri | Description | Peralihan yang dibenarkan |
| --- | --- | --- |
| Draf | Ini mewakili keadaan awal subkontrak. Rundingan dengan vendor sedang berjalan. Garisan dan harga adalah tertakluk kepada pengubahsuaian. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini boleh diedit dan dipadamkan. | Disahkan |
| Disahkan | Ini mewakili peringkat subkontrak selepas rundingan dengan vendor mengenai harga dan item baris yang dibeli selesai. Walau bagaimanapun, penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak masih berterusan. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. Butang **Batal** membolehkan anda membatalkan subkontrak yang disahkan. Butang **Buka** semula membolehkan anda membuka semula subkontrak untuk membawanya kembali ke **status Draf**. Gunakan butang **Tutup** untuk menutup subkontrak yang disahkan. | Tertutup <br> Dibatalkan <br> Draf |
| Tertutup | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak selesai. Subkontrak di negeri ini tidak lagi boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Juga, ia tidak lagi boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. | Tiada |
| Dibatalkan | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan/atau kerja oleh sumber subkontrak tidak lagi diperlukan. Subkontrak di negeri ini tidak boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan dan juga tidak boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. | Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
