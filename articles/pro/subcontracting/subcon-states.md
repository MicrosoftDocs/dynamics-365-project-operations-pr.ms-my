---
title: Peralihan keadaan pada subkontrak
description: Artikel ini menerangkan peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations kerana subkontrak dicipta, dilaksanakan dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261286"
---
# <a name="state-transitions-on-a-subcontract"></a>Peralihan keadaan pada subkontrak 

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini menerangkan peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations. Setiap negeri diwakili sebagai sama ada draf, disahkan, ditutup, atau dibatalkan. Imej berikut mewakili peralihan negeri.

![Model negeri subkontrak](../media/SubconStates.png)  

Jadual berikut menyediakan perihalan tentang perkara yang setiap negeri wakili dalam kitaran hayat subkontrak dalam Operasi Projek.

| Negeri | Description | Peralihan yang dibenarkan |
| --- | --- | --- |
| Draf | Ini mewakili keadaan awal subkontrak. Rundingan dengan vendor sedang berjalan. Garis dan harga tertakluk kepada pengubahsuaian. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini boleh diedit dan dipadamkan. | Disahkan |
| Disahkan | Ini mewakili peringkat subkontrak selepas rundingan dengan vendor mengenai harga dan item talian yang dibeli selesai. Walau bagaimanapun, penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak masih berterusan. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. Butang **Batal** membolehkan anda membatalkan subkontrak yang disahkan. Butang **Buka** semula membolehkan anda membuka semula subkontrak untuk membawanya kembali ke **status Draf**. Gunakan butang **Tutup** untuk menutup subkontrak yang disahkan. | Tertutup <br> Dibatalkan <br> Draf |
| Tertutup | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak selesai. Subkontrak di negeri ini tidak lagi boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Juga, ia tidak lagi boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |
| Dibatalkan | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak tidak lagi diperlukan. Subkontrak di negeri ini tidak boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan atau, tidak boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada sesuatu projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dipadamkan. | Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
