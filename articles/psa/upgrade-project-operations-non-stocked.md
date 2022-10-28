---
title: Naik taraf daripada Project Service Automation kepada Project Operations
description: Artikel ini menyediakan gambaran keseluruhan proses untuk menaik taraf daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 06a4de89be8176049d3a14a8c0d6427e228744ba
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709456"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naik taraf daripada Project Service Automation kepada Project Operations

Kami teruja untuk mengumumkan fasa kedua daripada tiga fasa untuk menaik taraf daripada Microsoft Dynamics 365 Project Service Automation kepada Microsoft Dynamics 365 Project Operations. Artikel ini memberikan gambaran keseluruhan untuk pelanggan yang memulakan perjalanan yang menarik ini. 

Program penyampaian naik taraf akan dibahagikan kepada tiga fasa.

| Naik taraf penghantaran | Fasa 1 (Januari 2022) | Fasa 2 (November 2022) | Fasa 3 (Gelombang April 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada kebergantungan kepada struktur pecahan kerja (WBS) untuk projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam had Operasi Projek yang disokong pada masa ini | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Operasi Projek yang disokong pada masa ini, termasuk sokongan untuk klien desktop Projek | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Menaik taraf ciri proses 

Sebagai sebahagian daripada proses naik taraf, kami telah menambah log naik taraf ke peta tapak untuk membolehkan pentadbir mendiagnosis kegagalan dengan lebih mudah. Sebagai tambahan kepada antara muka baru, peraturan pengesahan baru akan ditambah untuk memastikan integriti data selepas naik taraf. Pengesahan berikut akan ditambahkan pada proses naik taraf.

| Pengesahan | Fasa 1 (Januari 2022) | Fasa 2 (November 2022) | Fasa 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan disahkan terhadap pelanggaran integriti data biasa (contohnya, tugasan sumber yang dikaitkan dengan tugas induk yang sama tetapi mempunyai projek induk yang berbeza). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap had diketahui klien desktop Projek. | |  | :heavy_check_mark: |
| Sumber yang boleh ditempah dan kalendar projek akan dinilai terhadap pengecualian peraturan kalendar yang tidak serasi. | | :heavy_check_mark: | :heavy_check_mark: |

Dalam fasa 2, pelanggan yang menaik taraf kepada Operasi Projek akan menaik taraf projek sedia ada kepada pengalaman baca sahaja untuk perancangan projek. Dalam pengalaman baca sahaja ini, WBS penuh akan kelihatan dalam grid penjejakan. Untuk mengedit WBS, pengurus projek boleh memilih [**Tukar**](/PSA-Upgrade-Project-Conversion.md) pada halaman utama projek. Proses latar belakang kemudian mengemas kini projek supaya ia menyokong pengalaman penjadualan projek baru daripada Project for the Web. Fasa ini sesuai untuk pelanggan yang mempunyai projek yang sesuai dengan [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Dalam fasa 3, sokongan untuk klien desktop Projek akan ditambah, untuk faedah pelanggan yang ingin terus mengedit projek mereka daripada aplikasi tersebut. Walau bagaimanapun, jika projek sedia ada ditukar kepada Projek baru untuk pengalaman Web, capaian kepada tambahan akan dinyahdayakan bagi setiap projek yang ditukar.

## <a name="prerequisites"></a>Prasyarat

Untuk layak mendapat naik taraf Fasa 1, anda mesti memenuhi kriteria berikut:

- Persekitaran sasaran tidak boleh mengandungi sebarang rekod dalam **entiti msdyn_projecttask**.
- Lesen Operasi Projek yang sah mesti diberikan kepada semua pengguna aktif. 
- Anda mesti mengesahkan proses naik taraf dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mengandungi set data wakil yang sejajar dengan persekitaran pengeluaran anda.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Automasi Perkhidmatan Projek 37 (V3.10.58.120) atau lebih baru.

Untuk layak mendapat naik taraf Fasa 2, anda mesti memenuhi kriteria berikut:

- Lesen Operasi Projek yang sah mesti diberikan kepada semua pengguna aktif. 
- Anda mesti mengesahkan proses naik taraf dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mengandungi set data wakil yang sejajar dengan persekitaran pengeluaran anda.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Automasi Perkhidmatan Projek 37 (V3.10.58.120) atau lebih baru.
- Persekitaran yang mengandungi tugas (msdyn_projecttask) disokong hanya jika jumlah tugas bagi setiap projek adalah 500 atau kurang.

Prasyarat untuk Fasa 3 akan dikemas kini apabila tarikh ketersediaan umum semakin hampir.

## <a name="licensing"></a>Pelesenan

Jika anda mempunyai lesen aktif untuk Project Service Automation, anda boleh memasang dan menggunakan Operasi Projek, yang merangkumi semua keupayaan Automasi Perkhidmatan Projek dan banyak lagi. Dengan cara ini, anda boleh menguji keupayaan Operasi Projek semasa anda terus menggunakan Automasi Perkhidmatan Projek dalam pengeluaran. Selepas lesen Automasi Project Service anda tamat tempoh, anda perlu beralih kepada Operasi Projek. Apabila anda merancang peralihan ini, anda mesti mengambil kira hakikat bahawa lesen Operasi Projek tidak termasuk lesen Automasi Perkhidmatan Projek. Pelanggan yang mempunyai senario di mana mereka telah menggunakan Automasi Perkhidmatan Projek dan perlu terus menggunakan atau meningkatkan lesen mereka untuk PSA semasa mereka merancang untuk berpindah ke Operasi Projek, boleh meminta lesen PSA sementara berdasarkan Lesen Operasi Projek yang dibeli. Satu lesen Automasi Perkhidmatan Projek akan dikeluarkan untuk satu lesen Operasi Projek. Lesen PSA sementara boleh diminta dengan menggunakan pautan ini: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Menguji dan memfaktorkan penyesuaian

Sebagai titik permulaan, import semua penyesuaian ke dalam persekitaran Operasi Projek (Lite) yang bersih untuk mengesahkan bahawa import berjaya, dan operasi perniagaan berkelakuan seperti yang diharapkan.

Berikut adalah beberapa perkara yang perlu diperhatikan:

- Import mungkin gagal kerana hilang kebergantungan. Dalam erti kata lain, medan rujukan penyesuaian atau komponen lain yang telah dialih keluar dalam Operasi Projek. Dalam kes ini, keluarkan kebergantungan ini dari persekitaran pembangunan.
- Jika penyelesaian tidak terurus dan terurus anda termasuk komponen yang tidak disesuaikan, alih keluar komponen tersebut daripada penyelesaian. Contohnya, apabila anda menyesuaikan **entiti Projek**, tambahkan pengepala entiti pada penyelesaian anda sahaja. Jangan tambah semua medan. Jika anda telah menambah semua subkomponen sebelum ini, anda mungkin perlu mencipta penyelesaian baharu secara manual dan menambah komponen yang berkaitan padanya.
- Borang dan pandangan mungkin tidak muncul seperti yang dijangkakan. Dalam keadaan tertentu, jika anda telah menyesuaikan sebarang borang atau pandangan di luar kotak, penyesuaian mungkin menghalang kemas kini baru dalam Operasi Projek daripada berkesan. Untuk mengenal pasti isu-isu ini, kami mengesyorkan agar anda melakukan semakan bersebelahan pemasangan bersih Operasi Projek dan pemasangan Operasi Projek yang merangkumi penyesuaian anda. Bandingkan borang yang paling biasa digunakan dalam perniagaan anda untuk mengesahkan bahawa versi borang anda masih masuk akal dan tidak kehilangan sesuatu daripada versi borang yang bersih. Lakukan jenis semakan sebelah-menyebelah yang sama untuk sebarang pandangan yang telah anda sesuaikan.
- Logik perniagaan mungkin gagal pada masa jalan. Oleh sebab rujukan kepada medan dalam pasang masuk anda tidak disahkan pada masa import, logik perniagaan mungkin gagal kerana rujukan kepada medan yang tidak lagi wujud dan anda mungkin menerima mesej ralat yang menyerupai contoh berikut: entiti "'Projek' tidak mengandungi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logik'." Dalam kes ini, ubah suai penyesuaian anda supaya menggunakan medan baru. Jika anda menggunakan kelas proksi yang dijana secara automatik dan rujukan jenis yang kuat dalam logik pemalam anda, pertimbangkan untuk menjana semula proksi tersebut daripada pemasangan yang bersih. Dengan cara ini, anda boleh mengenal pasti semua tempat di mana pemalam anda bergantung pada medan yang ditamatkan.

Selepas anda mengemas kini penyesuaian anda untuk mengimport Operasi Projek dengan bersih, teruskan ke langkah berikut.

## <a name="end-to-end-testing-in-development-environments"></a>Ujian hujung ke hujung dalam persekitaran pembangunan

### <a name="initiate-upgrade"></a>Mulakan naik taraf 

1. Dalam pusat Power Platform pentadbiran, cari dan pilih persekitaran anda. Kemudian, dalam aplikasi, cari dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Pasang** untuk memulakan naik taraf. Pusat Power Platform pentadbiran akan membentangkan pemasangan ini sebagai pemasangan baru. Walau bagaimanapun, kehadiran versi terdahulu Automasi Perkhidmatan Projek akan dikesan, dan pemasangan sedia ada akan dinaik taraf.

    Selepas naik taraf selesai, persekitaran harus menunjukkan bahawa Operasi Projek dipasang dan Automasi Perkhidmatan Projek tidak dipasang.

    Bergantung pada jumlah data dalam persekitaran, peningkatan mungkin mengambil masa beberapa jam. Pasukan teras yang menguruskan naik taraf harus merancang dengan sewajarnya dan menjalankan peningkatan semasa waktu bukan perniagaan. Dalam sesetengah kes, jika jumlah data besar, peningkatan harus dijalankan pada hujung minggu. Keputusan mengenai penjadualan harus berdasarkan hasil ujian dalam persekitaran yang lebih rendah.

3. Menaik taraf penyelesaian tersuai mengikut kesesuaian. Pada ketika ini, gunakan sebarang perubahan yang anda buat pada penyesuaian anda dalam [bahagian Penyesuaian](#testing-and-refactoring-customizations) Ujian dan pemfaktoran semula artikel ini.
4. Pergi ke **Penyelesaian** Seting \>**dan** pilih untuk menyahpasang **penyelesaian Komponen** Dimansuhkan Operasi Projek.

    Penyelesaian ini adalah penyelesaian sementara yang memegang model dan komponen data sedia ada yang hadir semasa naik taraf. Dengan mengalih keluar penyelesaian ini, anda mengalih keluar semua medan dan komponen yang tidak lagi digunakan. Dengan cara ini, anda membantu memudahkan antara muka dan menjadikan integrasi dan sambungan lebih mudah.
    
### <a name="upgrade-to-project-operations-lite"></a>Naik taraf kepada Project Operations Lite

Langkah berikut menerangkan proses naik taraf dan pengelogan ralat yang berkaitan:

1. **Semakan Versi PSA:** Untuk memasang Operasi Projek, anda mesti mempunyai V 3.10.58.120 atau lebih tinggi.
1. **Pra-pengesahan:** Apabila pentadbir memulakan naik taraf, sistem menjalankan operasi pra-pengesahan pada setiap entiti yang merupakan teras kepada penyelesaian Operasi Projek. Langkah ini mengesahkan bahawa semua rujukan entiti adalah sah, dan ia memastikan bahawa data yang berkaitan dengan WBS berada dalam had Projek untuk Web yang diterbitkan.
1. **Naik taraf metadata:** Selepas pra-pengesahan berjaya, sistem memulakan perubahan pada skema dan mencipta penyelesaian komponen yang ditamatkan. Anda boleh mengalih keluar penyelesaian yang ditamatkan ini selepas anda menyelesaikan semua pemfaktoran semula penyesuaian yang diperlukan. Langkah ini adalah bahagian paling lama dalam proses naik taraf dan boleh mengambil masa sehingga empat jam untuk disiapkan.
1. **Naik taraf data:** Selepas semua perubahan skema yang diperlukan telah selesai dalam langkah naik taraf metadata, data anda dipindahkan ke skema baru dan sebarang lalai dan pengiraan semula yang diperlukan dilakukan.
1. **Kemas kini enjin jadual projek:** Selepas naik taraf data berjaya, **tab Jadual** pada halaman utama dilancarkan semula **Tugas**. Apabila pengguna memilih tab ini selepas naik taraf, mereka diarahkan untuk menavigasi ke grid penjejakan untuk melihat versi WBS baca sahaja. Untuk mengedit WBS, mereka mesti memulakan proses [penukaran jadual](/PSA-Upgrade-Project-Conversion.md). Semua projek tanpa WBS yang sedia ada boleh menggunakan pengalaman penjadualan baharu secara langsung, tanpa penukaran.
 
### <a name="validate-common-scenarios"></a>Mengesahkan senario biasa

Apabila anda mengesahkan penyesuaian khusus anda, kami mengesyorkan agar anda menyemak semula proses perniagaan yang disokong merentasi aplikasi. Proses perniagaan ini termasuk, tetapi tidak terhad kepada, penciptaan entiti jualan seperti sebut harga dan kontrak, dan penciptaan projek yang merangkumi WBS dan kelulusan sebenar.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Automasi Perkhidmatan Projek dan Operasi Projek

Bahagian ini menyediakan ringkasan perubahan utama yang anda boleh jangkakan antara Automasi Perkhidmatan Projek dan Operasi Projek.

### <a name="project-planning"></a>Perancangan projek

Keupayaan perancangan projek dalam Operasi Projek tidak lagi bergantung pada gabungan logik pihak klien dan logik sisi pelayan. Sebaliknya, Project Operations menggunakan Project for the Web kerana ia adalah enjin penjadualan. Perubahan dalam keupayaan penjadualan ini membolehkan beberapa ciri baharu, seperti pandangan Papan dan Gantt, perancangan dipacu sumber, [item](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) senarai semak tugas dan mod penjadualan projek. Keupayaan penjadualan baharu juga disokong oleh sekumpulan antara muka pengaturcaraan aplikasi (API) [baharu](../project-management/schedule-api-preview.md) yang kaya. API ini bertujuan untuk membantu memastikan tiada operasi programatik untuk mencipta, mengemas kini atau memadam entiti dalam WBS merosakkan medan terhitung dalam jadual.

### <a name="billing-and-pricing"></a>Pengebilan dan harga

Sebagai sebahagian daripada pelaburan berterusan dalam Operasi Projek, beberapa keupayaan baharu tersedia dalam Pengebilan dan harga. Berikut adalah beberapa contoh:

- [Merakam penggunaan bahan pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontrak tidak melebihi status dan pengesahan](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Pengebilan berasaskan tugas

### <a name="resource-management"></a>Pengurusan sumber

Operasi Projek menyediakan sokongan pilihan untuk Universal Resource Scheduling lembaga (URS) dan pembantu penjadualan. Pengalaman baharu ini akan menjadi mandatori dalam gelombang April 2023.

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penggunaan manakah yang disokong untuk naik taraf pada masa ini?

| Sumber                                                 | Sasaran                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Perkhidmatan Projek                             | Penggunaan Operasi Projek Lite                        | Disokong               |
| Dynamics 365 Finance Pengurusan Projek dan Perakaunan | Penggunaan Operasi Projek Lite                        | Tidak disokong pada masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario sumber/tidak distok     | Tidak disokong pada masa ini |
| Projek Automasi Perkhidmatan 3.x                         | Project Operations untuk senario sumber/tidak distok     | Tidak disokong pada masa ini |
| Projek untuk Web (persekitaran khusus)            | Penggunaan Operasi Projek Lite                        | Tidak disokong pada masa ini |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimanakah saya boleh memasang Project Operations sebelum perkakas naik taraf tersedia?

Terdapat dua pilihan untuk memasang Operasi Projek sebelum perkakas naik taraf tersedia:

- Sediakan persekitaran baru.
- Gunakan Operasi Projek secara berasingan pada mana-mana organisasi jualan yang Automasi Perkhidmatan Projek tidak hadir.

Jika Automasi Perkhidmatan Projek dipasang pada organisasi, tetapi ia tidak digunakan, ia boleh dinyahpasang. Selepas anda mengalih keluar sepenuhnya Project Service Automation, Project Operations boleh dipasang pada organisasi yang sama.
