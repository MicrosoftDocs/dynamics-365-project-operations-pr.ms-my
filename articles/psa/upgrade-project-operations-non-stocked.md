---
title: Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek
description: Topik ini memberikan gambaran keseluruhan proses untuk menaik taraf dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954298"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek

Kami teruja untuk mengumumkan tiga fasa pertama untuk menaik taraf dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Project Operations. Topik ini memberikan gambaran keseluruhan bagi pelanggan yang memulakan perjalanan yang menarik ini. Topik masa depan akan merangkumi pertimbangan pemaju dan butiran mengenai peningkatan ciri. Mereka bukan sahaja akan memberikan panduan untuk membantu anda mempersiapkan peningkatan anda ke Operasi Projek tetapi juga menerangkan apa yang boleh anda harapkan setelah anda menaik taraf.

Program penghantaran naik taraf akan dibahagikan kepada tiga fasa.

| Naik taraf penghantaran | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3 (Gelombang April 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Tiada kebergantungan kepada struktur pecahan kerja (WBS) untuk projek | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS dalam had Operasi Projek yang disokong pada masa ini | | :heavy_check_mark: | :heavy_check_mark: |
| WBS di luar had Operasi Projek yang disokong pada masa ini, termasuk sokongan untuk klien desktop Projek | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Ciri proses naik taraf 

Sebagai sebahagian daripada proses naik taraf, kami telah menambah log naik taraf ke peta tapak, supaya pentadbir dapat mendiagnosis kegagalan dengan lebih mudah. Sebagai tambahan kepada antara muka baru, peraturan pengesahan baru akan ditambah untuk memastikan integriti data selepas naik taraf. Pengesahihan berikut akan ditambah ke proses naik taraf.

| Pengesahan | Fasa 1 (Januari 2022) | Fasa 2 (Gelombang April 2022) | Fasa 3 (Gelombang April 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS akan disahkan terhadap pelanggaran integriti data biasa (contohnya, tugasan sumber yang dikaitkan dengan tugas induk yang sama tetapi mempunyai projek induk yang berbeza). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS akan disahkan terhadap had yang diketahui klien desktop Projek. | | :heavy_check_mark: | :heavy_check_mark: |
| Sumber boleh ditempah dan kalendar projek akan dinilai terhadap pengecualian peraturan kalendar yang tidak serasi. | | :heavy_check_mark: | :heavy_check_mark: |

Dalam fasa 2, pelanggan yang menaik taraf kepada Operasi Projek akan menaik taraf projek sedia ada mereka kepada pengalaman baca sahaja untuk perancangan projek. Dalam pengalaman baca sahaja ini, WBS penuh akan dapat dilihat dalam grid penjejakan. Untuk mengedit WBS, pengurus projek boleh memilih **Tukar pada halaman Projek** **utama**. Proses latar belakang kemudian akan mengemas kini projek supaya ia menyokong pengalaman penjadualan projek baru dari Project for the Web. Fasa ini sesuai untuk pelanggan yang mempunyai projek yang sesuai dengan [had Projek yang diketahui untuk Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Dalam fasa 3, sokongan untuk pelanggan desktop Projek akan ditambah, untuk manfaat pelanggan yang ingin terus mengedit projek mereka dari aplikasi itu. Walau bagaimanapun, jika projek sedia ada ditukar kepada Projek baru untuk pengalaman Web, akses kepada tambahan akan dinyahdayakan untuk setiap projek yang ditukar.

## <a name="prerequisites"></a>Prasyarat

Untuk layak untuk naik taraf fasa 1, pelanggan mesti memenuhi kriteria berikut:

- Persekitaran sasaran tidak boleh mengandungi sebarang rekod dalam **entiti** msdyn_projecttask.
- Lesen Operasi Projek yang sah mesti diberikan kepada semua pengguna aktif pelanggan. 
- Pelanggan mesti mengesahkan proses naik taraf dalam sekurang-kurangnya satu persekitaran bukan pengeluaran yang mempunyai set data perwakilan yang sejajar dengan data pengeluaran.
- Persekitaran sasaran mesti dikemas kini kepada Keluaran Kemas Kini Automasi Project Service 38 atau lebih baru.

Prasyarat untuk fasa 2 dan fasa 3 akan dikemas kini sebagai pendekatan tarikh ketersediaan umum.

## <a name="licensing"></a>Pelesenan

Jika anda mempunyai lesen aktif untuk Project Service Automation, anda boleh memasang dan menggunakan Operasi Projek, yang merangkumi semua keupayaan Automasi Perkhidmatan Projek dan banyak lagi. Dengan cara ini, anda boleh menguji keupayaan Operasi Projek semasa anda terus menggunakan Automasi Perkhidmatan Projek dalam pengeluaran. Selepas lesen Project Service Automation anda tamat tempoh, anda perlu beralih ke Operasi Projek. Apabila anda merancang peralihan ini, anda mesti mengambil kira hakikat bahawa lesen Operasi Projek tidak termasuk lesen Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Menguji dan membuat penyesuaian semula

Sebagai titik permulaan, import semua penyesuaian ke dalam persekitaran Operasi Projek (lite) yang bersih untuk mengesahkan bahawa import berjaya, dan operasi perniagaan berkelakuan seperti yang diharapkan.

Berikut adalah beberapa perkara yang perlu diperhatikan untuk:

- Import mungkin gagal kerana kebergantungan yang hilang. Dalam erti kata lain, medan rujukan penyesuaian atau komponen lain yang telah dialih keluar dalam Operasi Projek. Dalam kes ini, keluarkan kebergantungan ini dari persekitaran pembangunan.
- Jika penyelesaian tidak terurus dan terurus anda termasuk komponen yang tidak disesuaikan, alih keluar komponen tersebut daripada penyelesaian. Sebagai contoh, apabila anda menyesuaikan **entiti** Projek, hanya tambahkan pengepala entiti pada penyelesaian anda. Jangan tambah semua medan. Jika anda telah menambah semua subkomponen sebelum ini, anda mungkin perlu mencipta penyelesaian baharu secara manual dan menambah komponen yang berkaitan padanya.
- Borang dan pandangan mungkin tidak muncul sebagai tidak dijangka. Dalam sesetengah keadaan, jika anda telah menyesuaikan sebarang borang atau pandangan di luar kotak, penyesuaian mungkin menghalang kemas kini baharu dalam Operasi Projek daripada berkuat kuasa. Untuk mengenal pasti isu ini, kami mengesyorkan agar anda melakukan semakan sebelah menyebelah mengenai pemasangan Operasi Projek yang bersih dan pemasangan Operasi Projek yang merangkumi penyesuaian anda. Bandingkan borang yang paling biasa digunakan dalam perniagaan anda untuk mengesahkan bahawa versi borang anda masih masuk akal dan tidak kehilangan sesuatu daripada versi borang yang bersih. Lakukan jenis ulasan sebelah menyebelah yang sama untuk sebarang pandangan yang telah anda sesuaikan.
- Logik perniagaan mungkin gagal pada masa jalanan. Oleh sebab rujukan kepada medan dalam pemalam anda tidak disahkan pada masa import, logik perniagaan mungkin gagal kerana rujukan kepada medan yang tidak lagi wujud dan anda mungkin menerima mesej ralat yang menyerupai contoh berikut: entiti "Projek' tidak mengandungi atribut dengan Nama = 'msdyn_plannedhours' dan Peta Nama = 'Logik'." Dalam kes ini, ubah suai penyesuaian anda supaya mereka menggunakan medan baharu. Jika anda menggunakan kelas proksi yang dijana secara automatik dan rujukan jenis yang kuat dalam logik pemalam anda, pertimbangkan untuk menjana semula proksi tersebut daripada pemasangan yang bersih. Dengan cara ini, anda boleh mengenal pasti semua tempat di mana pemalam anda bergantung pada medan yang telah ditamatkan.

Selepas anda mengemas kini penyesuaian anda untuk mengimport Operasi Projek secara bersih, teruskan ke langkah seterusnya.

## <a name="end-to-end-testing-in-lower-environments"></a>Ujian hujung ke hujung dalam persekitaran yang lebih rendah

### <a name="run-the-upgrade-in-production"></a>Jalankan naik taraf dalam pengeluaran

1. Dalam Power Platform pusat pentadbiran, cari dan pilih persekitaran anda. Kemudian, dalam aplikasi, cari dan pilih **Dynamics 365 Project Operations**.
2. Pilih **Pasang untuk memulakan** penataran. Power Platform Pusat pentadbiran akan membentangkan pemasangan ini sebagai pemasangan baru. Walau bagaimanapun, kehadiran versi terdahulu Project Service Automation akan dikesan, dan pemasangan sedia ada akan dinaik taraf.

    Selepas naik taraf selesai, persekitaran harus menunjukkan bahawa Operasi Projek dipasang dan Automasi Perkhidmatan Projek tidak dipasang.

    > [!NOTE]
    > Bergantung pada jumlah data dalam persekitaran, naik taraf mungkin mengambil masa beberapa jam. Pasukan teras yang menguruskan naik taraf harus merancang dengan sewajarnya dan menjalankan naik taraf semasa waktu bukan perniagaan. Dalam sesetengah kes, jika jumlah data besar, peningkatan harus dijalankan pada hujung minggu. Keputusan mengenai penjadualan harus berdasarkan keputusan ujian dalam persekitaran yang lebih rendah.

3. Naik taraf penyelesaian tersuai mengikut kesesuaian. Pada ketika ini, gunakan sebarang perubahan yang anda buat pada penyesuaian anda dalam [bahagian Ujian dan penyesuaian refactoring topik](#testing-and-refactoring-customizations) ini.
4. Pergi **ke** \> **Penyelesaian** Seting, dan pilih untuk membuang pemasangan **penyelesaian Komponen Lapuk Operasi** Projek.

    Penyelesaian ini adalah penyelesaian sementara yang memegang model dan komponen data sedia ada yang hadir semasa naik taraf. Dengan mengalih keluar penyelesaian ini, anda mengalih keluar semua medan dan komponen yang tidak lagi digunakan. Dengan cara ini, anda membantu memudahkan antara muka dan menjadikan integrasi dan pelanjutan lebih mudah.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Perubahan utama antara Automasi Perkhidmatan Projek dan Operasi Projek

Bahagian ini menyediakan ringkasan perubahan utama yang boleh anda jangkakan antara Automasi Perkhidmatan Projek dan Operasi Projek.

### <a name="project-planning"></a>Perancangan projek

Keupayaan perancangan projek dalam Operasi Projek tidak lagi bergantung pada gabungan logik sisi pelanggan dan logik bahagian pelayan. Sebaliknya, Operasi Projek menggunakan Projek untuk Web kerana ia adalah enjin penjadualan. Perubahan dalam keupayaan penjadualan ini membolehkan beberapa ciri baru, seperti pandangan Lembaga dan Gantt, perancangan didorong sumber, [item senarai semak tugas dan mod penjadualan](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) projek. Keupayaan penjadualan baru juga disokong oleh satu set kaya antara muka pengaturcaraan aplikasi baru [(API)](../project-management/schedule-api-preview.md). API ini bertujuan untuk membantu memastikan tiada operasi programatik untuk mencipta, mengemas kini atau memadam entiti dalam WBS merosakkan medan yang dikira dalam jadual.

## <a name="billing-and-pricing"></a>Pengebilan dan harga

Sebagai sebahagian daripada pelaburan berterusan dalam Operasi Projek, beberapa keupayaan baru boleh didapati dalam Pengebilan dan harga. Berikut adalah beberapa contoh:

- [Merekodkan penggunaan bahan pada projek dan tugas projek](../material/material-usage-log.md)
- [Pengurusan subkontrak](../pro/subcontracting/managing-subcontracts-overview.md)
- [Kontrak berasaskan pendahuluan dan retainer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status kontrak tidak melebihi status dan pengesahan](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Pengebilan berasaskan tugas

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Jenis penggunaan mana yang disokong untuk penataran pada masa ini?

| Sumber                                                 | Sasaran                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Automasi Perkhidmatan Projek                             | Operasi Projek Lite Deployment                        | Disokong               |
| Dynamics 365 Finance Pengurusan Projek dan Perakaunan | Operasi Projek Lite Deployment                        | Tidak disokong buat masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Pengurusan Projek Kewangan dan Perakaunan              | Project Operations untuk senario pesanan distok/pengeluaran | Tidak disokong buat masa ini |
| Automasi Perkhidmatan Projek 3.x                         | Project Operations untuk senario sumber/tidak distok     | Tidak disokong buat masa ini |
| Projek untuk Web (persekitaran khusus)            | Operasi Projek Lite Deployment                        | Tidak disokong buat masa ini |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Bagaimanakah saya boleh memasang Operasi Projek sebelum alat naik taraf tersedia?

Terdapat dua pilihan untuk memasang Operasi Projek sebelum alat naik taraf tersedia:

- Menyediakan persekitaran baru.
- Gunakan Operasi Projek secara berasingan pada mana-mana organisasi jualan yang tidak hadir dalam Project Service Automation.

> [!NOTE]
> Jika Project Service Automation dipasang pada organisasi, tetapi ia tidak digunakan, ia boleh dinyahpasang. Selepas anda mengalih keluar Automasi Perkhidmatan Projek sepenuhnya, Operasi Projek boleh dipasang pada organisasi yang sama.
