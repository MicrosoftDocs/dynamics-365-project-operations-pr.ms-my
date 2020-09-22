---
title: Jejaki status projek
description: Cara untuk menjejaki status projek dalam Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753977"
---
# <a name="track-a-projects-status-project-service"></a>Jejak status projek (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Gunakan [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] untuk menjejaki kemajuan projek klien.  

Sebagaimana kemajuan penglibatan, peringkat projek dikemas kini untuk menunjukkan peringkat penglibatan:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Baharu**    | Apabila anda mencipta projek, peringkat ditetapkan kepada **Baharu**. Jika anda mencipta projek daripada templat, pada peringkat ini, projek mungkin mempunyai jadual, anggaran dan data pasukan. Sebaliknya, hanya terdapat rangka projek dan anda perlu memasukkan komponen projek yang lain secara manual. |
|  **Sebut Harga**   |      Apabila anda mengaitkan projek dengan sebut harga atau menciptanya daripada sebut harga, peringkat projek ditetapkan kepada **Sebut Harga** dan anggaran tarikh mula dan tamat juga dikemas kini. Apabila projek berada dalam peringkat sebut harga, butiran sebut harga dipaparkan pada tab **Sales** di halaman **Projek**.      |
|   **Pelan**   |                                     Apabila anda menang sebut harga yang dikaitkan dengan projek dan apabila penglibatan mara ke peringkat kontrak, peringkat projek dikemas kini kepada **Pelan**. Butiran kontrak dipaparkan pada tab **Sales** di halaman **Projek**.                                      |
| **Selesai** |                    Apabila kerja projek selesai, anda boleh menukar peringkat kepada **Selesai**. Apabila peringkat projek ditetapkan kepada selesai, difahami bahawa kerja 100% selesai tetapi projek terus dibuka untuk sebarang masa menunggu atau entri perbelanjaan direkodkan.                     |
|  **Tutup**   |           Apabila semua transaksi telah direkodkan pada projek dan tiada lagi transaksi untuk dilogkan, anda boleh menetapkan peringkat secara manual kepada **Tutup**. Apabila projek ditetapkan kepada **Tutup**, tiada lagi transaksi boleh dilogkan pada projek dan projek akan menjadi baca sahaja.           |

## <a name="to-track-a-projects-status"></a>Untuk menjejaki status projek  

1.  Pergi ke **Project Service > Projek**.  

2.  Klik program y ang anda mahu kerjakan.  

3.  Dalam bar yang merentas bahagian atas skrin, pilih anak panah ke bawah di sebelah nama projek dan kemudian klik **Penjejakan Projek**.  

4.  Pilih **Penjejakan Usaha** atau **Penjejakan Kos** dalam senarai juntai bawah di atas senarai tugas.  

5.  Dwiklik mana-mana tugas untuk mengeditnya. Anda juga boleh mengalihkan atau mengubah saiz bar dalam carta Gantt untuk mengubah masa dan kemajuan untuk tugas.  

### <a name="see-also"></a>Lihat Juga  
 [Panduan Pengurus Projek](../project-service/project-manager-guide.md)
