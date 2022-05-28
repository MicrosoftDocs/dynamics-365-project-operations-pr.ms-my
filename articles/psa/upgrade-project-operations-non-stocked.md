---
title: Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek
description: Topik ini memberikan gambaran keseluruhan proses untuk menaik taraf dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626742"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek

Kami teruja untuk mengumumkan fasa pertama daripada tiga fasa untuk naik taraf dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations. Topik ini memberikan gambaran keseluruhan untuk pelanggan yang memulakan perjalanan yang menarik ini. Topik masa depan akan merangkumi pertimbangan pembangun dan perincian mengenai peningkatan ciri. Mereka bukan sahaja akan memberikan panduan untuk membantu anda bersedia untuk menaik taraf anda kepada Operasi Projek tetapi juga menerangkan perkara yang anda boleh jangkakan selepas anda menaik taraf.

Program penghantaran naik taraf akan dibahagikan kepada tiga fasa.

| Naik taraf penghantaran | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada pergantungan pada struktur pecahan kerja (WBS) untuk projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam had Operasi Projek yang disokong pada masa ini | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Operasi Projek yang disokong pada masa ini, termasuk sokongan untuk klien desktop Projek | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Ciri proses naik taraf 

Sebagai sebahagian daripada proses naik taraf, kami telah menambah log naik taraf ke peta tapak, supaya pentadbir dapat mendiagnosis kegagalan dengan lebih mudah. Sebagai tambahan kepada antara muka baru, peraturan pengesahan baru akan ditambah untuk memastikan integriti data selepas peningkatan. Pengesahihan berikut akan ditambah ke proses naik taraf.

| Pengesahan | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan disahkan terhadap pelanggaran integriti data biasa (contohnya, tugasan sumber yang dikaitkan dengan tugas induk yang sama tetapi mempunyai projek induk yang berbeza). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap had yang diketahui klien desktop Project. | |  | :heavy_check_mark: |
| Sumber yang boleh ditempah dan kalendar projek akan dinilai terhadap pengecualian peraturan kalendar biasa yang tidak serasi. | | :heavy_check_mark: | :heavy_check_mark: |

Dalam fasa 2, pelanggan yang menaik taraf kepada Operasi Projek akan menaik taraf projek sedia ada mereka kepada pengalaman baca sahaja untuk perancangan projek. Dalam pengalaman baca sahaja ini, WBS penuh akan kelihatan dalam grid penjejakan. Untuk mengedit WBS, pengurus projek boleh memilih **Tukar** pada halaman Projek utama.**·** Proses latar belakang kemudian akan mengemas kini projek supaya ia menyokong pengalaman penjadualan projek baru dari Project for the Web. Fasa ini sesuai untuk pelanggan yang mempunyai projek yang sesuai dengan [had Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) yang diketahui.

Dalam fasa 3, sokongan untuk klien desktop Projek akan ditambah, untuk kepentingan pelanggan yang ingin terus mengedit projek mereka dari aplikasi tersebut. Walau bagaimanapun, jika projek sedia ada ditukar kepada Projek baru untuk pengalaman Web, capaian kepada tambahan akan dinyahdayakan untuk setiap projek yang ditukar.

## <a name="prerequisites"></a>Prasyarat

Untuk layak untuk naik taraf fasa 1, pelanggan mesti memenuhi kriteria berikut:

- Persekitaran sasaran tidak boleh mengandungi sebarang rekod dalam **entiti msdyn_projecttask**.
- Lesen Operasi Projek yang sah mesti diperuntukkan kepada semua pengguna aktif pelanggan. 
- Pelanggan mesti mengesahkan proses peningkatan dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mempunyai set data wakil yang sejajar dengan data pengeluaran.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Automasi Project Service 41 (3.10.62.162) atau lebih baru.

Prasyarat untuk fasa 2 dan fasa 3 akan dikemas kini apabila tarikh ketersediaan umum menghampiri.

## <a name="licensing"></a>Pelesenan

Jika anda mempunyai lesen aktif untuk Automasi Perkhidmatan Projek, anda boleh memasang dan menggunakan Operasi Projek, yang termasuk semua keupayaan Automasi Perkhidmatan Projek dan banyak lagi. Dengan cara ini, anda boleh menguji keupayaan Operasi Projek semasa anda terus menggunakan Automasi Perkhidmatan Projek dalam pengeluaran. Selepas lesen Automasi Project Service anda tamat tempoh, anda perlu beralih kepada Operasi Projek. Apabila anda merancang peralihan ini, anda mesti mengambil kira hakikat bahawa lesen Operasi Projek tidak termasuk lesen Automasi Perkhidmatan Projek.

## <a name="testing-and-refactoring-customizations"></a>Menguji dan menfaktorkan semula penyesuaian

Sebagai titik permulaan, import semua penyesuaian ke dalam persekitaran Operasi Projek (lite) yang bersih untuk mengesahkan bahawa import berjaya, dan operasi perniagaan berkelakuan seperti yang diharapkan.

Berikut adalah beberapa perkara yang perlu diberi perhatian:

- Import mungkin gagal kerana kebergantungan yang hilang. Dengan kata lain, medan rujukan penyesuaian atau komponen lain yang telah dialih keluar dalam Operasi Projek. Dalam kes ini, keluarkan kebergantungan ini dari persekitaran pembangunan.
- Jika penyelesaian anda yang tidak terurus dan terurus termasuk komponen yang tidak disesuaikan, alih keluar komponen tersebut daripada penyelesaian. Contohnya, apabila anda menyesuaikan **entiti Projek**, tambahkan pengepala entiti pada penyelesaian anda sahaja. Jangan tambah semua medan. Jika anda telah menambah semua subkomponen sebelum ini, anda mungkin perlu mencipta penyelesaian baharu secara manual dan menambah komponen yang berkaitan dengannya.
- Borang dan pandangan mungkin tidak muncul seperti yang dijangkakan. Dalam sesetengah keadaan, jika anda telah menyesuaikan mana-mana borang atau pandangan di luar kotak, penyesuaian mungkin menghalang kemas kini baharu dalam Operasi Projek daripada berkuat kuasa. Untuk mengenal pasti isu-isu ini, kami mengesyorkan agar anda melakukan semakan sebelah-menyebelah pemasangan Operasi Projek yang bersih dan pemasangan Operasi Projek yang merangkumi penyesuaian anda. Bandingkan borang yang paling biasa digunakan dalam perniagaan anda untuk mengesahkan bahawa versi borang anda masih masuk akal dan tidak kehilangan sesuatu daripada versi borang yang bersih. Lakukan jenis semakan sebelah-menyebelah yang sama untuk sebarang pandangan yang telah anda sesuaikan.
- Logik perniagaan mungkin gagal pada masa jalan. Oleh kerana rujukan kepada medan dalam pemalam anda tidak disahkan pada masa import, logik perniagaan mungkin gagal kerana rujukan kepada medan yang tidak lagi wujud dan anda mungkin menerima mesej ralat yang menyerupai contoh berikut: entiti "'Projek' tidak mengandungi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logik'." Dalam kes ini, ubah suai penyesuaian anda supaya mereka menggunakan medan baru. Jika anda menggunakan kelas proksi yang dijana secara automatik dan rujukan jenis yang kuat dalam logik pemalam anda, pertimbangkan untuk menjana semula proksi tersebut daripada pemasangan yang bersih. Dengan cara ini, anda boleh mengenal pasti semua tempat di mana pemalam anda bergantung pada medan yang telah lapuk.

Selepas anda mengemas kini penyesuaian anda untuk mengimport Operasi Projek dengan bersih, teruskan ke langkah seterusnya.

## <a name="end-to-end-testing-in-development-environments"></a>Ujian hujung ke hujung dalam persekitaran pembangunan

### <a name="initiate-upgrade"></a>Mulakan naik taraf 

1. Power Platform Dalam pusat pentadbiran, cari dan pilih persekitaran anda. Kemudian, dalam aplikasi, cari dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Pasang** untuk memulakan naik taraf. Pusat Power Platform pentadbiran akan membentangkan pemasangan ini sebagai pemasangan baru. Walau bagaimanapun, kehadiran versi terdahulu Project Service Automation akan dikesan, dan pemasangan sedia ada akan dinaik taraf.

    Selepas naik taraf selesai, persekitaran harus menunjukkan bahawa Operasi Projek dipasang dan Automasi Perkhidmatan Projek tidak dipasang.

    > [!NOTE]
    > Bergantung pada jumlah data dalam persekitaran, naik taraf mungkin mengambil masa beberapa jam. Pasukan teras yang menguruskan naik taraf harus merancang dengan sewajarnya dan menjalankan peningkatan semasa waktu bukan perniagaan. Dalam sesetengah kes, jika jumlah data adalah besar, peningkatan harus dijalankan pada hujung minggu. Keputusan mengenai penjadualan harus berdasarkan keputusan ujian dalam persekitaran yang lebih rendah.

3. Naik taraf penyelesaian tersuai mengikut kesesuaian. Pada ketika ini, gunakan sebarang perubahan yang anda buat pada penyesuaian anda di [bahagian Ujian dan penyusunan semula penyesuaian](#testing-and-refactoring-customizations) topik ini.
4. Pergi ke **Penyelesaian** Tetapan \>**dan** pilih untuk menyahpasang **penyelesaian Komponen** Ditamatkan Operasi Projek.

    Penyelesaian ini adalah penyelesaian sementara yang memegang model dan komponen data sedia ada yang hadir semasa naik taraf. Dengan mengalih keluar penyelesaian ini, anda mengalih keluar semua medan dan komponen yang tidak lagi digunakan. Dengan cara ini, anda membantu memudahkan antara muka dan menjadikan integrasi dan sambungan lebih mudah.
    
### <a name="validate-common-scenarios"></a>Sahkan senario biasa

Apabila anda mengesahkan penyesuaian khusus anda, kami mengesyorkan agar anda juga menyemak proses perniagaan yang disokong di seluruh aplikasi. Proses perniagaan ini termasuk, tetapi tidak terhad kepada, penciptaan entiti jualan seperti sebut harga dan kontrak, dan penciptaan projek yang merangkumi WBS dan kelulusan sebenar.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan utama antara Automasi Perkhidmatan Projek dan Operasi Projek

Bahagian ini menyediakan ringkasan perubahan utama yang boleh anda jangkakan antara Automasi Perkhidmatan Projek dan Operasi Projek.

### <a name="project-planning"></a>Perancangan projek

Keupayaan perancangan projek dalam Operasi Projek tidak lagi bergantung pada logik sisi pelanggan gabungan dan logik sisi pelayan. Sebaliknya, Project Operations menggunakan Project untuk Web kerana ia adalah enjin penjadualan. Perubahan dalam keupayaan penjadualan ini membolehkan beberapa ciri baru, seperti pandangan Papan dan Gantt, perancangan berdasarkan sumber, [item](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) senarai semak tugas, dan mod penjadualan projek. Keupayaan penjadualan baru juga disokong oleh set pelbagai antara muka pengaturcaraan aplikasi baru [(API)](../project-management/schedule-api-preview.md). API ini bertujuan untuk membantu memastikan tiada operasi programatik untuk mencipta, mengemas kini atau memadam entiti dalam WBS merosakkan medan yang dikira dalam jadual.

## <a name="billing-and-pricing"></a>Pengebilan dan harga

Sebagai sebahagian daripada pelaburan berterusan dalam Operasi Projek, beberapa keupayaan baru tersedia dalam Pengebilan dan harga. Berikut adalah beberapa contoh:

- [Penggunaan bahan rakaman pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status dan pengesahan kontrak tidak melebihi](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Pengebilan berasaskan tugas

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penggunaan yang manakah yang sedang disokong untuk naik taraf?

| Sumber                                                 | Sasaran                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Perkhidmatan Projek                             | Operasi Projek Lite Penggunaan                        | Disokong               |
| Dynamics 365 Finance Pengurusan Projek dan Perakaunan | Operasi Projek Lite Penggunaan                        | Tidak disokong buat masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario pesanan distok/pengeluaran | Tidak disokong buat masa ini |
| Automasi Perkhidmatan Projek 3.x                         | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Projek untuk Web (persekitaran khusus)            | Operasi Projek Lite Penggunaan                        | Tidak disokong buat masa ini |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimanakah saya boleh memasang Operasi Projek sebelum alat naik taraf tersedia?

Terdapat dua pilihan untuk memasang Operasi Projek sebelum alat naik taraf tersedia:

- Sediakan persekitaran baru.
- Gunakan Operasi Projek secara berasingan pada mana-mana organisasi jualan di mana Automasi Perkhidmatan Projek tidak hadir.

> [!NOTE]
> Jika Automasi Perkhidmatan Projek dipasang pada organisasi, tetapi ia tidak digunakan, ia boleh dinyahpasang. Selepas anda mengalih keluar Automasi Perkhidmatan Projek sepenuhnya, Operasi Projek boleh dipasang pada organisasi yang sama.
