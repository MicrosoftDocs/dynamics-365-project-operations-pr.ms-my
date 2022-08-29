---
title: Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek
description: Artikel ini menyediakan gambaran keseluruhan proses untuk menaik taraf daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Project Operations.
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
ms.openlocfilehash: c7958c1474820361269f19ea8c9279b96f087d7a
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230263"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek

Kami teruja untuk mengumumkan fasa pertama daripada tiga fasa untuk dinaik taraf daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Project Operations. Artikel ini memberikan gambaran keseluruhan untuk pelanggan yang memulakan perjalanan menarik ini. Artikel masa depan akan merangkumi pertimbangan pemaju dan butiran mengenai peningkatan ciri. Mereka bukan sahaja akan memberikan panduan untuk membantu anda mempersiapkan naik taraf anda ke Operasi Projek tetapi juga menerangkan perkara yang boleh anda jangkakan selepas anda menaik taraf.

Program penyampaian naik taraf akan dibahagikan kepada tiga fasa.

| Naik taraf penghantaran | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada kebergantungan kepada struktur pecahan kerja (WBS) untuk projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam had Operasi Projek yang disokong pada masa ini | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Operasi Projek yang disokong pada masa ini, termasuk sokongan untuk klien desktop Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Ciri proses naik taraf 

Sebagai sebahagian daripada proses naik taraf, kami telah menambah log naik taraf ke peta laman, supaya pentadbir dapat mendiagnosis kegagalan dengan lebih mudah. Sebagai tambahan kepada antara muka baharu, peraturan pengesahihan baharu akan ditambah untuk memastikan integriti data selepas naik taraf. Pengesahihan berikut akan ditambahkan pada proses naik taraf.

| Pengesahan | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan disahkan terhadap pelanggaran integriti data biasa (contohnya, tugasan sumber yang dikaitkan dengan tugas induk yang sama tetapi mempunyai projek induk yang berbeza). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap had yang diketahui klien desktop Projek. | |  | :heavy_check_mark: |
| Sumber yang boleh ditempah dan kalendar projek akan dinilai terhadap pengecualian peraturan kalendar yang tidak serasi. | | :heavy_check_mark: | :heavy_check_mark: |

Dalam fasa 2, pelanggan yang menaik taraf kepada Operasi Projek akan menaik taraf projek sedia ada mereka kepada pengalaman baca sahaja untuk perancangan projek. Dalam pengalaman baca sahaja ini, WBS penuh akan kelihatan dalam grid penjejakan. Untuk mengedit WBS, pengurus projek boleh memilih **Tukar** pada halaman Projek **utama**. Proses latar belakang kemudiannya akan mengemas kini projek supaya ia menyokong pengalaman penjadualan projek baru daripada Project for the Web. Fasa ini sesuai untuk pelanggan yang mempunyai projek yang sesuai dalam [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Dalam fasa 3, sokongan untuk klien desktop Project akan ditambah, untuk manfaat pelanggan yang ingin terus mengedit projek mereka daripada aplikasi tersebut. Walau bagaimanapun, jika projek sedia ada ditukar kepada Projek baru untuk pengalaman Web, akses kepada tambahan akan dinyahdayakan untuk setiap projek yang ditukar.

## <a name="prerequisites"></a>Prasyarat

Untuk layak untuk naik taraf fasa 1, pelanggan mesti memenuhi kriteria berikut:

- Persekitaran sasaran tidak boleh mengandungi sebarang rekod dalam **entiti msdyn_projecttask**.
- Lesen Operasi Projek yang sah mesti diperuntukkan kepada semua pengguna aktif pelanggan. 
- Pelanggan mesti mengesahkan proses naik taraf dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mempunyai set data wakil yang sejajar dengan data pengeluaran.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Automasi Perkhidmatan Projek 41 (3.10.62.162) atau lebih baru.

Prasyarat untuk fasa 2 dan fasa 3 akan dikemas kini apabila tarikh ketersediaan umum semakin hampir.

## <a name="licensing"></a>Pelesenan

Jika anda mempunyai lesen aktif untuk Project Service Automation, anda boleh memasang dan menggunakan Operasi Projek, yang merangkumi semua keupayaan Project Service Automation dan banyak lagi. Dengan cara ini, anda boleh menguji keupayaan Operasi Projek semasa anda terus menggunakan Automasi Perkhidmatan Projek dalam pengeluaran. Selepas lesen Project Service Automation anda tamat tempoh, anda perlu beralih kepada Operasi Projek. Apabila anda merancang peralihan ini, anda mesti mengambil kira hakikat bahawa lesen Operasi Projek tidak termasuk lesen Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Menguji dan menyusun semula penyesuaian

Sebagai titik permulaan, import semua penyesuaian ke dalam persekitaran Operasi Projek (Lite) yang bersih untuk mengesahkan bahawa import berjaya, dan operasi perniagaan berkelakuan seperti yang diharapkan.

Berikut ialah beberapa perkara yang perlu diberi perhatian:

- Import mungkin gagal kerana tiada kebergantungan. Dalam erti kata lain, medan rujukan penyesuaian atau komponen lain yang telah dialih keluar dalam Operasi Projek. Dalam kes ini, keluarkan kebergantungan ini dari persekitaran pembangunan.
- Jika penyelesaian anda yang tidak diuruskan dan diuruskan termasuk komponen yang tidak disesuaikan, alih keluar komponen tersebut daripada penyelesaian. Contohnya, apabila anda menyesuaikan **entiti Projek**, tambahkan pengepala entiti pada penyelesaian anda sahaja. Jangan tambah semua medan. Jika anda telah menambah semua subkomponen sebelum ini, anda mungkin perlu mencipta penyelesaian baharu secara manual dan menambah komponen berkaitan padanya.
- Borang dan pandangan mungkin tidak muncul seperti yang dijangkakan. Di bawah sesetengah keadaan, jika anda telah menyesuaikan sebarang borang atau pandangan di luar kotak, penyesuaian mungkin menghalang kemas kini baru dalam Operasi Projek daripada berkesan. Untuk mengenal pasti isu-isu ini, kami mengesyorkan agar anda melakukan semakan sebelah-menyebelah pemasangan bersih Operasi Projek dan pemasangan Operasi Projek yang merangkumi penyesuaian anda. Bandingkan borang yang paling biasa digunakan dalam perniagaan anda untuk mengesahkan bahawa versi borang anda masih masuk akal dan tidak kehilangan sesuatu daripada versi borang yang bersih. Lakukan jenis semakan sebelah menyebelah yang sama untuk sebarang pandangan yang telah anda sesuaikan.
- Logik perniagaan mungkin gagal pada masa jalan. Oleh sebab rujukan kepada medan dalam pemalam anda tidak disahkan pada masa import, logik perniagaan mungkin gagal kerana rujukan kepada medan yang tidak lagi wujud dan anda mungkin menerima mesej ralat yang menyerupai contoh berikut: Entiti "Projek" tidak mengandungi atribut dengan Nama = 'msdyn_plannedhours' dan NameMapping = 'Logik'." Dalam kes ini, ubah suai penyesuaian anda supaya ia menggunakan medan baru. Jika anda menggunakan kelas proksi yang dijana secara automatik dan rujukan jenis yang kuat dalam logik pemalam anda, pertimbangkan untuk menjana semula proksi tersebut daripada pemasangan yang bersih. Dengan cara ini, anda boleh dengan mudah mengenal pasti semua tempat di mana pemalam anda bergantung pada medan yang ditamatkan.

Selepas anda mengemas kini penyesuaian anda untuk mengimport Operasi Projek dengan bersih, teruskan ke langkah seterusnya.

## <a name="end-to-end-testing-in-development-environments"></a>Ujian hujung ke hujung dalam persekitaran pembangunan

### <a name="initiate-upgrade"></a>Mulakan naik taraf 

1. Power Platform Dalam pusat pentadbiran, cari dan pilih persekitaran anda. Kemudian, dalam aplikasi, cari dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Pasang** untuk memulakan naik taraf. Pusat Power Platform pentadbiran akan membentangkan pemasangan ini sebagai pemasangan baru. Walau bagaimanapun, kehadiran versi awal Project Service Automation akan dikesan, dan pemasangan sedia ada akan dinaik taraf.

    Selepas naik taraf selesai, persekitaran harus menunjukkan bahawa Operasi Projek dipasang dan Automasi Perkhidmatan Projek tidak dipasang.

    > [!NOTE]
    > Bergantung pada jumlah data dalam persekitaran, naik taraf mungkin mengambil masa beberapa jam. Pasukan teras yang menguruskan naik taraf harus merancang dengan sewajarnya dan menjalankan peningkatan semasa waktu bukan perniagaan. Dalam sesetengah kes, jika jumlah data besar, peningkatan harus dijalankan pada hujung minggu. Keputusan mengenai penjadualan harus berdasarkan hasil ujian dalam persekitaran yang lebih rendah.

3. Menaik taraf penyelesaian tersuai mengikut kesesuaian. Pada ketika ini, gunakan sebarang perubahan yang anda buat pada penyesuaian anda dalam [bahagian Pengujian dan penyesuaian pemfaktoran](#testing-and-refactoring-customizations) semula artikel ini.
4. Pergi ke **Penyelesaian** Seting \>**dan** pilih untuk menyahpasang **penyelesaian Komponen** Ditamatkan Operasi Projek.

    Penyelesaian ini adalah penyelesaian sementara yang memegang model data dan komponen sedia ada yang hadir semasa naik taraf. Dengan mengalih keluar penyelesaian ini, anda mengalih keluar semua medan dan komponen yang tidak lagi digunakan. Dengan cara ini, anda membantu memudahkan antara muka dan menjadikan integrasi dan peluasan lebih mudah.
    
### <a name="validate-common-scenarios"></a>Sahkan senario biasa

Apabila anda mengesahkan penyesuaian khusus anda, kami mengesyorkan agar anda juga menyemak proses perniagaan yang disokong merentasi aplikasi. Proses perniagaan ini termasuk, tetapi tidak terhad kepada, penciptaan entiti jualan seperti sebut harga dan kontrak, dan penciptaan projek yang merangkumi WBS dan kelulusan sebenar.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan besar antara Automasi Perkhidmatan Projek dan Operasi Projek

Seksyen ini menyediakan ringkasan perubahan utama yang boleh anda jangkakan antara Automasi Perkhidmatan Projek dan Operasi Projek.

### <a name="project-planning"></a>Perancangan projek

Keupayaan perancangan projek dalam Operasi Projek tidak lagi bergantung pada gabungan logik pihak klien dan logik pihak pelayan. Sebaliknya, Operasi Projek menggunakan Project untuk Web kerana ia adalah enjin penjadualan. Perubahan dalam keupayaan penjadualan ini membolehkan beberapa ciri baharu, seperti pandangan Lembaga dan Gantt, perancangan dipacu sumber, [item](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) senarai semak tugas dan mod penjadualan projek. Keupayaan penjadualan baharu juga disokong oleh set antara muka pengaturcaraan aplikasi (API) [baharu yang kaya](../project-management/schedule-api-preview.md). API ini bertujuan untuk membantu memastikan tiada operasi programatik untuk mencipta, mengemas kini atau memadam entiti dalam WBS merosakkan medan yang dikira dalam jadual.

## <a name="billing-and-pricing"></a>Pengebilan dan harga

Sebagai sebahagian daripada pelaburan berterusan dalam Operasi Projek, beberapa keupayaan baru tersedia dalam Pengebilan dan harga. Berikut adalah beberapa contoh:

- [Merekodkan penggunaan bahan pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Kontrak tidak melebihi status dan pengesahan](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Pengebilan berasaskan tugas

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penggunaan manakah yang disokong untuk dinaik taraf?

| Sumber                                                 | Sasaran                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Perkhidmatan Projek                             | Operasi Projek Lite Deployment                        | Disokong               |
| Pengurusan dan Perakaunan Projek Dynamics 365 Finance | Operasi Projek Lite Deployment                        | Tidak disokong buat masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Automasi Perkhidmatan Projek 3.x                         | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Projek untuk Web (persekitaran khusus)            | Operasi Projek Lite Deployment                        | Tidak disokong buat masa ini |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimanakah saya boleh memasang Operasi Projek sebelum perkakas naik taraf tersedia?

Terdapat dua opsyen untuk memasang Operasi Projek sebelum perkakas naik taraf tersedia:

- Menyediakan persekitaran baru.
- Gunakan Operasi Projek secara berasingan pada mana-mana organisasi jualan yang Automasi Perkhidmatan Projek tidak hadir.

> [!NOTE]
> Jika Project Service Automation dipasang pada organisasi, tetapi ia tidak digunakan, ia boleh dinyahpasang. Selepas anda mengalih keluar sepenuhnya Automasi Perkhidmatan Projek, Operasi Projek boleh dipasang pada organisasi yang sama.
