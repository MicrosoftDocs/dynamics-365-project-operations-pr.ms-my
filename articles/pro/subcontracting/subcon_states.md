---
title: Peralihan negeri pada subkontrak dalam Operasi Projek
description: Topik ini menerangkan peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations kerana subkontrak dicipta, dilaksanakan dan ditutup.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903064"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Peralihan negeri pada subkontrak dalam Operasi Projek

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Topik ini menerangkan peralihan keadaan pada subkontrak dalam Microsoft Dynamics 365 Project Operations. Setiap negeri diwakili sebagai draf, disahkan, ditutup, atau dibatalkan. Imej berikut mewakili peralihan keadaan.

![Model keadaan subkontrak](../media/SubconStates.png)  

Jadual berikut memberikan perihalan tentang apa yang diwakili oleh setiap negeri dalam kitaran hayat subkontrak dalam Operasi Projek.

| Negeri | Description | Peralihan yang dibenarkan |
| --- | --- | --- |
| Draf | Ini mewakili keadaan awal subkontrak. Rundingan dengan vendor sedang berjalan. Garisan dan harga adalah tertakluk kepada pengubahsuaian. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini boleh diedit dan dipadamkan. | Disahkan |
| Disahkan | Ini mewakili peringkat subkontrak selepas rundingan dengan vendor mengenai harga dan item baris yang dibeli selesai. Walau bagaimanapun, penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak masih berterusan. Subkontrak di negeri ini boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Ia juga boleh dirujuk mengenai masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. **Butang Batal membolehkan anda membatalkan** subkontrak yang disahkan. **Butang Buka Semula membolehkan anda membuka semula** subkontrak untuk membawanya kembali ke **status** Draf. Gunakan **butang Tutup** untuk menutup subkontrak yang disahkan. | Tertutup <br> Dibatalkan <br> Draf |
| Tertutup | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak selesai. Subkontrak di negeri ini tidak lagi boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan. Juga, ia tidak lagi boleh dirujuk pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. | Tiada |
| Dibatalkan | Ini mewakili peringkat subkontrak apabila penghantaran sebenar bahan dan / atau kerja oleh sumber subkontrak tidak lagi diperlukan. Subkontrak di negeri ini tidak boleh digunakan untuk menganggarkan dan keperluan projek kakitangan untuk sumber dan bahan atau, boleh dirujuk tepat pada masa, perbelanjaan, dan penggunaan bahan pada projek. Subkontrak dalam keadaan ini tidak boleh diedit atau dihapuskan. | Tiada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
