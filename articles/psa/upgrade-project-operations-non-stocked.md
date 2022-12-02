---
title: Naik taraf daripada Project Service Automation kepada Project Operations
description: Artikel ini memberikan gambaran keseluruhan proses untuk menatar daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Project Operations.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736678"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naik taraf daripada Project Service Automation kepada Project Operations

Kami amat gembira untuk mengumumkan fasa kedua daripada tiga fasa untuk menatar daripada Microsoft Dynamics 365 Project Service Automation kepada Microsoft Dynamics 365 Project Operations. Artikel ini memberikan gambaran keseluruhan untuk pelanggan yang memulakan perjalanan yang menyeronokkan ini. 

Program penghantaran tatar akan dibahagikan kepada tiga fasa.

| Penghantaran tatar | Fasa 1 (Januari 2022) | Fasa 2 (November 2022) | Fasa 3 (Gelombang April 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada kebersandaran pada struktur pecahan kerja (WBS) untuk projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam lingkungan had Project Operations yang disokong pada masa ini | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Project Operations yang disokong pada masa ini, termasuk sokongan untuk Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Ciri proses tatar 

Sebagai sebahagian daripada proses tatar, kami telah menambahkan log tatar pada peta tapak untuk mendayakan pentadbir agar mendapatkan kegagalan diagnosis dengan lebih mudah. Sebagai tambahan kepada antara muka baharu, peraturan pensahihan baharu akan ditambahkan untuk memastikan integriti data selepas tatar. Pensahihan berikut akan ditambah pada proses tatar.

| Pensahihan URL | Fasa 1 (Januari 2022) | Fasa 2 (November 2022) | Fasa 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan disahkan berdasarkan pelanggaran integriti data lazim (contohnya, tugas sumber yang berkaitan dengan tugas induk yang sama tetapi mempunyai projek induk yang berbeza). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan berdasarkan [had Project for the Web yang diketahui](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan berdasarkan had Project Desktop Client yang diketahui. | |  | :heavy_check_mark: |
| Sumber boleh ditempah dan kalendar projek akan dinilai berdasarkan pengecualian peraturan kalendar tidak serasi yang lazim. | | :heavy_check_mark: | :heavy_check_mark: |

Dalam fasa 2, pelanggan yang menatar kepada Project Operations akan menatar projek sedia ada mereka kepada pengalaman baca sahaja untuk perancangan projek. Dalam pengalaman baca sahaja ini, WBS penuh akan boleh dilihat dalam grid penjejakan. Untuk mengedit WBS, pengurus projek boleh memilih [**Tukar**](/PSA-Upgrade-Project-Conversion.md) pada halaman utama projek. Proses latar belakang kemudian mengemas kini projek itu supaya projek itu menyokong pengalaman penjadualan projek baharu daripada Project for the Web. Fasa ini sesuai untuk pelanggan yang mempunyai projek yang sesuai dengan [had Project for the Web yang diketahui](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Dalam fasa 3, sokongan untuk Project Desktop Client akan ditambahkan, untuk manfaat pelanggan yang mahu terus mengedit projek mereka daripada aplikasi tersebut. Walau bagaimanapun, jika projek sedia ada ditukar kepada pengalaman Project for the Web baharu, akses kepada tambahan akan dinyahdayakan untuk setiap projek yang ditukar.

## <a name="prerequisites"></a>Prasyarat

Untuk layak tatar Fasa 1, anda mesti memenuhi kriteria berikut:

- Persekitaran sasaran tidak perlu mengandungi sebarang rekod dalam entiti **msdyn_projecttask**.
- Lesen Project Operations sah mesti diuntukkan untuk semua pengguna aktif. 
- Anda mesti mengesahkan proses tatar dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mengandungi wakil set data yang sejajar dengan persekitaran pengeluaran anda.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Project Service Automation 37 (V 3.10.58.120) atau kemudian.

Untuk layak tatar Fasa 2, anda mesti memenuhi kriteria berikut:

- Lesen Project Operations sah mesti diuntukkan untuk semua pengguna aktif. 
- Anda mesti mengesahkan proses tatar dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mengandungi wakil set data yang sejajar dengan persekitaran pengeluaran anda.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Project Service Automation 37 (V 3.10.58.120) atau kemudian.
- Persekitaran yang mengandungi tugas (msdyn_projecttask) disokong hanya jika jumlah kerja setiap projek ialah 500 atau kurang.

Prasyarat untuk Fasa 3 akan dikemas kini apabila tarikh ketersediaan umum semakin hampir.

## <a name="licensing"></a>Pelesenan

Jika anda mempunyai lesen aktif untuk Project Service Automation, anda boleh memasang dan menggunakan Project Operations, yang termasuk semua keupayaan Project Service Automation dan banyak lagi. Dengan cara ini, anda boleh menguji keupayaan Project Operations sambil anda terus menggunakan Project Service Automation dalam pengeluaran. Selepas lesen Project Service Automation anda tamat tempoh, anda akan perlu beralih ke Project Operations. Apabila anda merancang peralihan ini, anda mesti mengambil kira fakta bahawa lesen Project Operations tidak termasuk lesen Project Service Automation. Pelanggan yang mempunyai senario yang mereka telah menggunakan Project Service Automation dan perlu terus menggunakan atau meningkatkan lesen mereka untuk PSA sementara mereka merancang untuk beralih ke Project Operations, boleh meminta lesen sementara PSA berdasarkan lesen Project Operations yang dibeli. Salah satu lesen Project Service Automation akan dikeluarkan untuk satu lesen Project Operations. Lesen sementara PSA boleh diminta menggunakan pautan ini: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Pengujian dan penyesuaian pemfaktoran semula

Sebagai titik permulaan, import semua penyesuaian ke dalam persekitaran Project Operations (Lite) yang bersih untuk mengesahkan bahawa import berjaya, dan operasi perniagaan berkelakuan seperti yang dijangkakan.

Berikut merupakan beberapa perkara yang perlu diberikan perhatian:

- Import mungkin gagal kerana kehilangan kebergantungan. Dalam erti kata lain, medan rujukan penyesuaian atau komponen lain yang telah dialih keluar dalam Project Operations. Dalam kes ini, alih keluar kebergantungan daripada persekitaran pembangunan.
- Jika penyelesaian tidak terurus dan terurus anda termasuk komponen yang tidak tersuai, alih keluar komponen tersebut daripada penyelesaian. Sebagai contoh, apabila anda sesuaikan entiti **Project**, tambah hanya pengepala entiti pada penyelesaian anda. Jangan tambah semua medan. Jika anda telah menambahkan semua subkomponen sebelum ini, anda mungkin perlu mencipta penyelesaian baharu secara manual dan menambahkan komponen yang berkaitan padanya.
- Borang dan pandangan mungkin tidak muncul seperti yang dijangkakan. Dalam sesetengah keadaan, jika anda telah menyesuaikan sebarang borang atau pandangan di luar kotak, penyesuaian mungkin akan menghalang kemas kini baharu dalam Project Operations daripada dikuatkuasakan. Untuk mengenal pasti isu ini, kami mengesyorkan agar anda melakukan semakan sisi dengan sisi pemasangan bersih Project Operations dan pemasangan Project Operations yang termasuk penyesuaian anda. Bandingkan borang yang paling biasa digunakan dalam perniagaan anda untuk mengesahkan bahawa versi borang anda masih masuk akal dan tidak akan kehilangan sesuatu daripada versi borang bersih. Lakukan perkara yang sama bagi semakan sisi dengan sisi untuk sebarang pandangan yang telah anda sesuaikan.
- Logik perniagaan mungkin gagal pada masa jalanan. Sebab rujukan kepada medan dalam pasang masuk anda tidak disahkan pada masa import, logik perniagaan mungkin gagal kerana rujukan kepada medan yang tidak lagi wujud dan anda mungkin menerima mesej ralat yang menyerupai contoh berikut: "entiti 'Project' tidak mengandungi atribut dengan Nama = 'msdyn_plannedhours ' dan NameMapping = 'Logical'." Dalam kes ini, ubah suai penyesuaian anda supaya penyesuaian itu menggunakan medan baharu. Jika anda menggunakan kelas proksi yang dijana secara automatik dan rujukan jenis yang kukuh dalam logik pasang masuk anda, pertimbangkan untuk menjana semula proksi tersebut daripada pemasangan bersih. Dengan cara ini, anda boleh mengenal pasti semua tempat yang pasang masuk anda bergantung pada medan yang ditamatkan.

Selepas anda mengemas kini penyesuaian anda untuk mengimport Project Operations dengan bersih, beralih ke langkah seterusnya.

## <a name="end-to-end-testing-in-development-environments"></a>Ujian hujung ke hujung dalam persekitaran pembangunan

### <a name="initiate-upgrade"></a>Memulakan tatar 

1. Dalam pusat pentadbir Power Platform, cari dan pilih persekitaran anda. Kemudian, dalam aplikasi, cari dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Pasang** untuk memulakan tatar. Pusat pentadbir Power Platform akan membentangkan pemasangan ini sebagai pemasangan baharu. Walau bagaimanapun, kehadiran versi Project Service Automation yang lebih awal akan dikesan, dan pemasangan yang sedia ada akan ditatar.

    Selepas naik taraf selesai, persekitaran harus menunjukkan bahawa Project Operations telah dipasang, dan bahawa Project Service Automation tidak dipasang.

    Bergantung pada amaun data dalam persekitaran, tatar mungkin mengambil masa sehingga beberapa jam. Pasukan teras yang mengurus tatar hendaklah merancang dengan sewajarnya dan menjalankan tatar pada waktu bukan perniagaan. Dalam sesetengah keadaan, jika jumlah data lebih besar, tatar hendaklah berjalan pada hujung minggu. Keputusan tentang penjadualan hendaklah berdasarkan keputusan ujian dalam persekitaran yang lebih rendah.

3. Tatar penyelesaian tersuai mengikut kesesuaian. Pada masa ini, menggunakan sebarang perubahan yang anda lakukan pada penyesuaian anda dalam bahagian [Ujian dan pemfaktoran semula penyesuaian](#testing-and-refactoring-customizations) pada artikel ini.
4. Pergi ke **make.powerapps.com**, pilih persekitaran anda daripada senarai juntai bawah di bahagian atas sebelah kanan portal, pilih **Penyelesaian** daripada menu kiri, pilih penyelesaian **Komponen Ditamatkan Project Operations** dan **Nyahpasang**.

    Penyelesaian ini ialah penyelesaian sementara yang memegang model data sedia ada dan komponen yang hadir semasa tatar. Dengan mengalih keluar penyelesaian ini, anda akan mengalih keluar semua medan dan komponen yang tidak digunakan lagi. Dengan cara ini, anda membantu untuk memudahkan antara muka dan menjadikan penyepaduan dan sambungan lebih mudah.
    
### <a name="upgrade-to-project-operations-lite"></a>Tatar kepada Project Operations Lite

Langkah berikut menerangkan proses tatar dan pengelogan ralat yang berkaitan:

1. **Semakan Versi PSA:** Untuk memasang Project Operations, anda mesti mempunyai V3.10.58.120 atau lebih tinggi.
1. **Pra-pengesahan:** Apabila pentadbir memulakan tatar, sistem akan menjalankan operasi pra-pengesahan pada setiap entiti yang merupakan teras kepada penyelesaian Project Operations. Langkah ini mengesahkan semua rujukan entiti adalah sah dan memastikan data yang berkaitan dengan WBS berada dalam had Project for the Web yang diterbitkan.
1. **Tatar metadata:** Selepas pra-pengesahan yang berjaya, sistem ini memulakan perubahan pada skema dan mencipta penyelesaian komponen yang ditamatkan. Anda boleh mengalih keluar penyelesaian yang ditamatkan ini selepas anda menyelesaikan semua pemfaktoran semula yang diperlukan bagi penyesuaian. Langkah ini merupakan bahagian paling lama dalam proses tatar dan boleh mengambil masa sehingga empat jam untuk dilengkapkan.
1. **Tatar data:** Selepas semua perubahan skema yang diperlukan telah dilengkapkan dalam langkah tatar metadata, data anda akan dipindahkan ke skema baharu dan sebarang penetapan nilai lalai yang diperlukan dan pengiraan semula dilakukan.
1. **Kemas kini enjin jadual projek:** Selepas tatar data berjaya, tab **Jadual** pada halaman utama ialah **Tugas** yang dilabelkan semula. Apabila pengguna memilih tab ini selepas tatar, mereka diarahkan untuk menavigasi ke grid penjejakan untuk melihat versi baca sahaja WBS. Untuk mengedit WBS, mereka mesti memulakan [proses penukaran jadual](/PSA-Upgrade-Project-Conversion.md). Semua projek tanpa WBS sedia ada boleh menggunakan pengalaman penjadualan baharu secara langsung, tanpa penukaran.
 
### <a name="validate-common-scenarios"></a>Sahkan senario lazim

Apabila anda mengesahkan penyesuaian khusus anda, kami mengesyorkan agar anda juga menyemak proses perniagaan yang disokong merentasi aplikasi. Proses perniagaan ini termasuk, tetapi tidak terhad kepada, penciptaan entiti jualan seperti sebut harga dan kontrak serta penciptaan projek yang termasuk WBS dan kelulusan aktual.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Project Service Automation dengan Project Operations

Bahagian ini memberikan ringkasan perubahan besar yang boleh anda jangkakan antara Project Service Automation dengan Project Operations.

### <a name="project-planning"></a>Perancangan projek

Keupayaan perancangan projek dalam Project Operations tidak lagi bergantung pada kombinasi logik pihak klien dan logik pihak pelayan. Sebaliknya, Project Operations menggunakan Project for the Web sebagai enjin penjadualan. Perubahan dalam keupayaan penjadualan ini mendayakan beberapa ciri baharu, seperti pandangan Papan dan Gantt, perancangan yang didorong oleh sumber, [item senarai semak tugas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), dan mod penjadualan projek. Keupayaan penjadualan yang baharu juga disokong oleh set kaya [antara muka pengaturcaraan aplikasi baharu (API)](../project-management/schedule-api-preview.md). API ini bertujuan untuk membantu dalam memastikan bahawa tiada operasi programatik untuk penciptaan, pengemaskinian atau pemadaman sebuah entiti dalam WBS akan merosakkan medan dikira dalam jadual.

### <a name="billing-and-pricing"></a>Pengebilan dan harga

Sebagai sebahagian daripada pelaburan berterusan dalam Project Operations, beberapa keupayaan baharu boleh didapati dalam Pengebilan dan harga. Berikut adalah beberapa contoh:

- [Penggunaan bahan rekod pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan pengesahan kontrak yang tidak boleh dilebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Pengebilan berasaskan tugas

### <a name="resource-management"></a>Pengurusan sumber

Project Operations menyediakan sokongan opsyenal untuk lembaga Universal Resource Scheduling (URS) dan pembantu penjadualan. Pengalaman baharu ini akan menjadi wajib dalam gelombang April 2023.

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Apakah jenis pengerahan yang kini disokong untuk tatar?

| Sumber                                                 | Sasaran                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Perkhidmatan Projek                             | Pengerahan Project Operations Lite                        | Disokong               |
| Pengurusan Projek dan Perakaunan Dynamics 365 Finance | Pengerahan Project Operations Lite                        | Tidak disokong pada masa ini |
| Pengurusan Projek dan Perakaunan Kewangan              | Project Operations untuk senario sumber/tidak distok     | Tidak disokong pada masa ini |
| Project Service Automation 3.x                         | Project Operations untuk senario sumber/tidak distok     | Tidak disokong pada masa ini |
| Project for the Web (persekitaran khusus)            | Pengerahan Project Operations Lite                        | Tidak disokong pada masa ini |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimanakah saya boleh memasang Project Operations sebelum peralatan tatar tersedia?

Terdapat dua pilihan untuk memasang Project Operations sebelum peralatan tatar tersedia:

- Peruntukan persekitaran baharu.
- Guna Project Operations secara berasingan pada sebarang organisasi jualan yang Project Service Automation tidak hadir.

Jika Project Service Automation dipasang pada organisasi, tetapi tidak digunakan, Project Service Automation boleh dinyahpasang. Selepas anda mengalih keluar Project Service Automation sepenuhnya, Project Operations boleh dipasang pada organisasi yang sama.
