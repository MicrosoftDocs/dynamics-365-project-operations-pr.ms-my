---
title: Cipta templat projek
description: Cara untuk mencipta templat projek dalam Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177437"
---
# <a name="create-a-project-template-project-service"></a>Cipta templat projek (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Templat projek menjimatkan masa anda jika syarikat anda membida dengan kerap pada jenis produk yang serupa. Mereka menyediakan set peranan standard dan anggaran jam untuk jenis projek. Pengurus akaun dan pengurus projek boleh mencipta projek berdasarkan templat projek atau mereka boleh menyalin templat dan membuat templat mereka sendiri.  
  
## <a name="components-of-project-template"></a>Komponen templat projek
 Templat projek terdiri daripada tiga komponen:  
  
- **Struktur pecahan kerja**: Struktur pecahan kerja dalam templat projek mempunyai set elemen yang sama seperti dalam projek. Anda boleh mencipta hierarki tugas, mengaitkan peranan dengan tugas, mentakrifkan atribut jadual, mengesetkan kebergantungan dan melihat semua data dalam Gantt. Struktur pecahan kerja dalam templat projek juga menyokong mod tugas untuk setiap tugas. Tidak ada perbezaan antara templat projek dan projek semasa membuat jadual kerja.  
  
- **Anggaran projek**: Anggaran projek dalam templat mempunyai fungsi yang sama seperti dalam projek, kecuali senarai harga untuk penetapan lalai kos dan harga jualan sentiasa senarai kos dan harga jualan yang ditakrifkan dalam parameter [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Kefungsian yang lain sama seperti dalam projek.  
  
- **Pembentukan pasukan projek**: Apabila membentuk pasukan projek untuk templat projek, anda tidak boleh menempah sumber bernama dalam templat. Anda boleh menggunakan **Jana Pasukan Projek** dalam struktur pecahan kerja untuk menjana set sumber generik. Anda juga boleh menentukan kemahiran dan kecekapan yang diperlukan untuk sumber generik. Anda tidak boleh menggantikan sumber generik dengan sumber yang boleh ditempah dalam templat projek.  

## <a name="create-a-project-template-from-an-existing-project"></a>Mencipta templat projek daripada projek sedia ada
Anda boleh mencipta templat projek daripada projek dengan cara berikut:

- **Struktur** pecahan kerja: Struktur pecahan kerja dalam templat yang diperoleh daripada projek akan menyalin semua tugas dan kebergantungan. Tugasan yang dibuat akan berdasarkan ahli pasukan generik yang ditambahkan ke pasukan projek apabila templat projek dibuat.
- **Anggaran projek**: Apabila templat projek dicipta daripada projek sedia ada, anggaran daripada projek sumber disalin ke templat projek.
- **Ahli pasukan projek**: Apabila templat dicipta daripada projek sedia ada, semua ahli pasukan yang dinamakan digantikan dengan sumber generik organisasi. Semua nama dan peranan kedudukan dikekalkan.

## <a name="create-a-project-from-a-template"></a>Cipta projek daripada templat  
 Anda boleh mencipta projek daripada templat dengan cara berikut:  
  
-   Apabila mencipta projek daripada sebut harga, anda boleh memilih templat projek dalam borang cipta cepat projek.  
  
-   Apabila mencipta projek dengan mengklik **Projek Baharu**, borang projek memaparkan sebelum anda menyimpan rekod. Dari sini, anda boleh klik medan **Pilih templat** untuk memilih daripada templat projek yang ditakrifkan lebih awal dalam organisasi anda.  
  
-   Klik **Cipta projek daripada templat** pada halaman **Templat Projek** untuk mencipta projek daripada templat.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Menyalin komponen templat kepada projek  
 Apabila anda menyalin komponen templat ke dalam projek, terdapat beberapa perkara yang perlu anda tahu mengenainya.  
  
 **Menyalin struktur pecahan kerja**: Apabila anda menyalin struktur pecahan kerja daripada templat kerja, jika projek mempunyai kalendar projek yang berbeza daripada templat, waktu kerja daripada kalendar projek akan dikenakan kepada jadual tugas. Ini menyesuaikan jadual untuk kalendar projek sandaran. Begitu juga, tugas pertama pada struktur pecahan kerja mengambil tarikh mula, jadi jadual hierarki tugas lain dikemas kini berdasarkan tempoh dan kebergantungan yang ditentukan dalam struktur pecahan kerja templat.  
  
 **Menyalin anggaran projek**: Apabila anda menyalin merentasi garisan anggaran projek, senarai harga dikemas kini berdasarkan unit pemilikan projek untuk senarai harga kos dan pelanggan untuk senarai harga jualan. Kos unit dan harga jualan ditentukan daripada senarai harga ini pada projek yang dikaitkan dengan entiti jualan.  
  
 **Menyalin pasukan projek**: Apabila anda menyalin pasukan projek daripada templat kepada projek, sumber generik disalin merentasi, bersama dengan kemahiran dan kecekapan yang ditentukan dalam templat. Tugasan sumber generik juga dikekalkan sebagai mana dalam templat projek.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Pengurus Projek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
