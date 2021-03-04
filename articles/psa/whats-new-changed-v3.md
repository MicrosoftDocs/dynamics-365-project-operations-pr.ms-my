---
title: Perkara baharu atau berubah dalam Project Service Automation versi 3
description: Topik ini menyediakan maklumat tentang perkara baharu dan diubah dalam Project Service Automation versi 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150679"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Perkara baharu atau berubah dalam Project Service Automation versi 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini menyediakan maklumat tentang perubahan kepada antara muka pengguna (UI), fungsi dan istilah dalam Project Service Automation antara versi 2 atau versi 1 dan versi 3.

## <a name="project-scheduling"></a>Penjadualan projek
Jadual projek yang dikenali sebagai Struktur Pecahan Kerja (WBS) dalam versi terdahulu, telah dinamakan semula sebagai Jadual dan diakses dengan mengklik tab **Jadual**. 

![Jadual Projek](media/psa-schedule-01.png)

Jadual kini mempunyai permukaan baharu untuk interaksi yang moden dan boleh diakses. Walau bagaimanapun, enjin penjadualan Project Service Automation asas tidak berubah. Butang kawalan dalam reben grid jadual membolehkan anda berinteraksi dengan jadual yang serupa dengan versi terdahulu Project Service Automation. Perubahan tambahan kepada jadual termasuk:

- **Carta Gantt** - Carta Gantt tidak lagi wujud. Visualisasi Gannt baharu akan kembali dalam kemas kini masa depan.
- **Pengepala lajur** - Anda boleh menyembunyikan pengepala lajur dalam grid dengan mengklik penunjuk bawah bersebelahan dengan tajuk lajur. 
- **Lajur** - Anda boleh menunjukkan lajur tersembunyi dengan mengklik **Tambah lajur**. 
- **Kategori transaksi** - Carian **Kategori transaksi** telah ditambah kepada grid jadual dan ditunjukkan secara lalai. 
 
## <a name="project-templates"></a>Templat projek
Perubahan berikut telah dibuat pada fungsi templat projek.

### <a name="create-a-project-template"></a>Cipta templat projek 
Anda boleh mencipta templat projek dalam versi 3 yang serupa dengan versi terdahulu Project Service Automation. Templat ini hanya boleh mengandungi jadual dan jadual boleh termasuk tugasan tetapi ia tidak diperlukan. Jika jadual mempunyai tugasan, ia hanya boleh untuk sumber generik. Anda boleh menjana keperluan sumber untuk sumber generik tetapi ia tidak boleh ditempah dengan sumber sebenar dalam templat. Anda tidak boleh menempah sumber sebenar kepada pasukan dalam templat. 

### <a name="create-a-template-from-an-existing-template"></a>Cipta templat daripada templat sedia ada
Apabila anda mencipta templat projek baharu daripada templat sedia ada dalam Project Service Automation versi 3, perkara berikut akan berlaku: 

- Jadual projek sumber disalin ke dalam templat. 
- Sumber generik disalin ke dalam pasukan dan mana-mana tugasan sumber generik akan disalin. Keperluan untuk sumber generik tidak akan disalin. 

### <a name="create-a-template-from-an-existing-project"></a>Cipta templat daripada projek sedia ada
Apabila anda mencipta templat projek baharu daripada projek sedia ada, perkara berikut akan berlaku: 

- Jadual projek sumber disalin ke dalam templat. 
- Sumber generik disalin ke dalam pasukan dan mana-mana tugasan sumber generik akan dikekalkan. Keperluan untuk sumber generik tidak akan disalin.    
- Sumber yang dinamakan, yang ditugaskan atau tidak ditugaskan akan dialih keluar daripada pasukan dan digantikan dengan sumber generik.
- Jika wujud, maklumat pelanggan akan dialih keluar. 
- Jika wujud, rujukan tentang sebut harga dan kontrak dialih keluar. 

### <a name="create-a-project-from-a-template"></a>Cipta projek daripada templat
Dalam Project Service Automation versi 3, apabila anda mencipta projek baharu daripada templat, perkara berikut akan berlaku:

- Jadual, pasukan dan tugasan akan disalin kepada projek baharu.   
- Tarikh mula adalah sama ada tarikh disalin atau tarikh yang dipilih oleh pengguna.   
- Untuk mana-mana ahli pasukan generik dengan keperluan sumber dalam templat, keperluan tidak disalin atau dijana secara automatik. Anda akan perlu menjana mereka. 

## <a name="copy-a-project"></a>Salin projek
Dalam Project Service Automation versi 3, apabila anda menyalin projek, perkara berikut akan berlaku: 

- Anggaran tarikh mula akan disalin tetapi boleh berubah.  
- Jadual dan tugas projek disalin. 
- Sumber generik dan tugasannya disalin. Keperluan sumber untuk sumber generik tidak disalin. Anda akan perlu menjananya semula. 
- Sumber sebenar dan tugasannya tidak disalin. Sebaliknya, ia digantikan dengan sumber generik. 
- Aktual tidak disalin kepada projek baharu. 

## <a name="move-a-scheduled-project"></a>Alihkan projek berjadual
Apabila anda mengalihkan jadual projek sedia ada ke hadapan, perkara berikut akan berlaku: 

- Tarikh tugas dialihkan secara automatik untuk dipadankan dengan tempoh pergerakan. 
- Sumber generik yang ditugaskan kekal ditugaskan.   
- Jika ia dijana sebelum projek dialihkan, keperluan untuk sumber generik kekal sama dan tidak dijana semula secara automatik. Anda perlu menjananya sekali lagi untuk menunjukkan tugasan baharu kerana pergerakan tugas. 
- Tugasan tentang sumber sebenar berubah untuk dipadankan dengan pergerakan tarikh tugas. Tempahan pada sumber sebenar tidak berubah. Anda akan perlu mengubah suai tempahan menggunakan pandangan penyelarasan. 
- Sumber pasukan dengan tempahan tanpa tugasan tidak berubah. 
- Aktual tidak dialihkan. 

## <a name="estimates"></a>Anggaran
Anggaran telah dibahagikan kepada dua tab, **Tugasan sumber** dan **Anggaran**. Tab **Tugasan sumber** mengandungi anggaran usaha dan menunjukkan tugasan sumber untuk tugas dalam pandangan berfasa masa. Anda boleh mengedit anggaran berdasarkan pada enjin penjadualan yang dijana.

![Tab tugasan sumber menunjukkan anggaran usaha dan tugasan sumber untuk tugas](media/resource-assignments-tab-02.png)

Tab **Anggaran** menunjukkan kos dan jumlah jualan untuk tugasan sumber. Jumlah baca sahaja. Penentuan harga pengekosan dan jualan kini didorong oleh tugasan ahli pasukan pada jadual. Ini bermakna jika anda mempunyai tugas tanpa sebarang tugasan, tugas itu akan ditunjukkan di bawah baldi tidak ditugaskan. Ini juga bermakna tanpa **peranan**, yang merupakan dimensi penentuan harga lalai, tiada kos atau jualan anggaran jika anda mempunyai pelanggan atau kontrak/sebut harga yang berkaitan dengan projek. 

![Anggaran tab menunjukkan jumlah kos dan jualan](media/estimates-tab-03.png)
  
Kategori juga disokong pada tugas dalam pandangan jadual. Dikumpulkan mengikut kategori pada pandangan anggaran berfasa masa akan menyediakan pengalaman yang lebih baik terutamanya apabila anda juga mempunyai anggaran perbelanjaan dalam projek anda. Anggaran perbelanjaan dimasukkan menggunakan grid pada tab berasingan. 

Anggaran perbelanjaan boleh dimasukkan dalam grid pada tab **Anggaran perbelanjaan**. 

![Tab anggaran perbelanjaan menunjukkan grid anggaran perbelanjaan](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Pengurusan sumber
Dalam Project Service Automation versi 3, dengan UI Klien Disatukan yang baharu dan perubahan dalam hubungan antara tempahan dan tugasan, pengambilan kakitangan untuk projek dengan sumber generik atau sebenar telah berubah secara mendadak daripada versi 2 dan versi 1. Walau bagaimanapun, konsep sumber boleh ditempah yang **sebenar** dan **generik** tetap sama seperti ahli pasukan, keperluan, tugasan dan tempahan.   

![Menggunakan pemilih sumber](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Tugaskan sumber boleh ditempah sebenar 
Dalam Project Service Automation versi 3, tempahan dan penugasan tugas tidak begitu berkaitan seperti dalam versi Project Service Automation sebelumnya. Anda boleh menggunakan grid pasukan untuk menempah ahli pasukan **sebenar** yang sama dengan pasaran.

Menggunakan pemilih sumber pada jadual, anda boleh memilih ahli pasukan yang dicipta dalam pandangan pasukan dan kemudian menugaskannya kepada tugas. Anda boleh terus menugaskan kepadanya, walaupun melepasi tempahannya. Gunakan tab **Penyelarasan** untuk menyelaraskan ahli pasukan yang mempunyai perbezaan dalam tempahan dan tugasan.

Pemilih sumber akan menunjukkan ahli pasukan untuk projek. Anda juga boleh menggunakan pemilih sumber untuk carian dan melihat sumber boleh ditempah lain yang bukan sebahagian daripada pasukan projek. Anda boleh menugaskannya kepada tugas dan ia akan menjadi sebahagian daripada pasukan projek. Anda akan perlu menempahnya dengan menggunakan tab **Papan jadual** atau **Penyelarasan**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Tugaskan sumber boleh ditempah yang generik pada tugas dan pasukan projek, dan kemudian penuhi dengan sumber sebenar melalui Papan Jadual 
Dalam Project Service Automation versi 3, fungsi jana pasukan tidak digunakan untuk sumber generik. Sebaliknya, anda boleh mencipta dan tugaskan secara langsung sumber generik daripada jadual dengan menaip nama kedudukan sumber generik dalam sel sumber jadual. Atau, anda boleh memilih ikon sumber dalam sel dan kemudian menggunakan pemilih sumber, taipkan nama sumber generik yang anda ingin ciptakan. Ini akan membuka panel cipta pantas yang membenarkan anda menetapkan peranan dan unit organisasi ahli pasukan sumber generik. Selepas anda mencipta sumber, ia ditugaskan untuk tugas itu dan anda boleh terus menugaskan sumber generik kepada tugas lain dalam jadual.    
 
Apabila anda telah menugaskan sumber kepada semua tugas yang sesuai, anda boleh menjana keperluan sumber dan kemudian memenuhinya dengan menempah secara terus dengan **Papan jadual** atau dengan menyerahkan permintaan sumber. Anda juga boleh menambah sumber generik secara terus kepada grid ahli pasukan. 

Sumber generik ditambah kepada pasukan projek tanpa keperluan sumber dengan tarikh mula/akhir projek sehingga keperluan sumber dijana. Untuk menjana keperluan, pilih sumber generik dan klik **Jana**. Pautan keperluan kini dipaparkan dan jam yang diperlukan akan diisi dengan jam ditugaskan. Anda boleh mengklik pautan untuk membuka dan mengemas kini keperluan.
  
Apabila tempahan selesai dan benar-benar dipenuhi oleh sumber yang dinamakan, sumber generik digantikan dengan sumber yang dinamakan dan tugasan pada jadual dikemas kini dengan sumber yang dinamakan. 

Sumber yang dicadangkan untuk keperluan kini disimpan pada tab dan bukannya pada bahagian yang berasingan.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Berbilang sumber yang dinamakan memenuhi sumber generik
Apabila keperluan dipenuhi dengan berbilang sumber, sumber generik kekal berada pada pasukan dan ditugaskan untuk tugas itu. Ahli pasukan yang dinamakan yang ditempah tidak ditugaskan sebagai sebahagian daripada kedudukan. Pengurus projek boleh menugaskan kerja yang diperlukan untuk sumber sebenar.  Pandangan **Penyelarasan** menyediakan pecahan tempahan merentasi berbilang sumber untuk berbilang tugasan tugas. Ini tidak dilakukan secara automatik kerana dalam senario yang lebih rumit seperti anda yang mempunyai pakej tugas yang menjadikan keperluan, niat cara pengurus projek ingin tugaskan, perlu diandaikan. Oleh seba sistem tidak boleh memahami niat, andaian mungkin akan berbeza daripada yang dicadangkan dan hasil yang salah atau tidak dapat diramalkan akan berlaku. Hasil boleh diramal adalah sumber generik yang kekal ditugaskan sehingga pengurus projek dengan sengaja menugaskan sumber menggunakan pandangan **Penyelarasan**.

### <a name="reconciliation"></a>Penyelarasan
Tab **Penyelarasan** menunjukkan tempahan dan semua tugasan untuk setiap ahli pasukan projek. Pandangan menunjukkan jam dalam sel yang boleh mewakili titik masa dari bulan ke hari. Pandangan ini membenarkan pengurus projek menyelaras tempahan ahli pasukan dan tugasannya untuk pasukan projeknya. Ini dapat membantu kerana tempahan dan tugasan tugas tidak terikat yang membenarkan lebih banyak kefleksibelan apabila merancang projek. 

![Tab penyelarasan menunjukkan tempahan dan tugasan untuk ahli pasukan projek](media/resource-reconciliation-tab-06.png)

Bagi setiap sumber, pandangan mengambil perbezaan antara tempahan ahli pasukan dan gulung atas tugasan tugasnya dan menunjukkan dua perbezaan berikut yang boleh berlaku dengan tempahan dan tugasan dalam projek: 

- **Kekurangan tempahan** - Kekurangan tempahan berlaku apabila sumber mempunyai lebih banyak tugasan daripada tempahan. Oleh sebab kapasiti ini belum ditempah, pengurus projek boleh membetulkan ini dengan melanjutkan tempahan sumber untuk menampung defisit. 
- **Tempahan berlebihan** - Tempahan berlebihan berlaku apabila sumber telah ditempah untuk projek tetapi belum ditugaskan kepada tugas.  Ini mungkin kejadian yang boleh diterima, sebagai contoh jika sumber telah ditempah sebelum tugasan tugas. Walau bagaimanapun dalam kes lain, sumber mungkin tidak dirancang untuk ditugaskan, dan PM harus mempertimbangkan untuk membatalkan tempahan sumber untuk membenarkan kapasiti digunakan bagi projek lain. 

Apabila anda mempunyai tugasan tugas untuk sumber tanpa tempahan (kekurangan tempahan), anda boleh memilih kekurangan tempahan agregat dan klik **Lanjutkan tempahan**. Dari sini, anda boleh melihat tempahan yang diperlukan untuk menangani kekurangan sumber dan ketersediaannya. 
 
## <a name="time-and-expense"></a>Masa dan perbelanjaan
Bahagian ini menyediakan maklumat tentang perubahan dalam masa, perbelanjaan dan kelulusan dalam versi 3 Project Service Automation. sebagai sebahagian penyelesaian Dynamics 365 Project Service Automation, ciri **Entri masa** telah disegar semula untuk memanfaatkan kerangka kerja Antara Muka Disatukan. Ini mendayakan penghantaran antara muka pengguna yang konsisten dan seragam mengikut reka bentuk responsif untuk pandangan optimum pada sebarang saiz skrin atau peranti. 

### <a name="landing-page"></a>Halaman pendaratan
Pengalaman entri masa tersuai yang tidak boleh dilanjutkan telah ditamatkan dalam versi 3. Sebaliknya, kini terdapat pengalaman grid asli yang boleh dilanjutkan dan boleh diakses. Anda boleh mengakses fungsi entri masa dengan menggunakan peta tapak di sebelah kiri. Dengan perubahan ini, anda tidak lagi boleh memasukkan masa untuk satu minggu pada satu masa. Sebaliknya, anda perlu mencipta entri masa untuk setiap hari dalam grid. Selepas beberapa kali entri dicipta, pengguna boleh mencipta entri masa dengan fungsi **Salin** diterangkan kemudian dalam topik ini. 

![Halaman pendaratan entri masa](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Cipta entri masa baharu 
Klik **Baharu** dalam reben untuk membuka halaman cipta pantas untuk entri masa tempat anda memasukkan tempoh dalam minit, jam atau hari. Untuk melakukan ini, hanya mula menaip h, m atau d bersama dengan kuantiti.  

![Cipta pantas entri masa](media/quick-create-time-entry-08.png)

Medan carian disokong oleh pandangan sistem. Contohnya, selepas anda memasukkan maklumat projek, medan **Tugas projek** ditetapkan secara lalai kepada pandangan **Tugas projek terbuka saya**. Bagi mencipta entri masa untuk tugas yang tidak ditugaskan kepada pengguna, klik **Ubah pandangan** pada carian dan pilih **Semua tugas projek Aktif**. Selepas entri masa telah dicipta dan ditunjukkan dalam grid, anda boleh mengedit sebarang nilai baris secara langsung dalam grid.  

### <a name="bulk-createcopy"></a>Cipta/salinan pukal 
Selepas beberapa kali entri telah dicipta, anda boleh menggunakan fungsi salin untuk mencipta entri masa tambahan. Klik **Salin** untuk membuka dialog **Salin**. Dalam **daripada tempoh: Tarikh Mula**, tetapkan julat tarikh dari tempoh masa yang mesti disalin. Dalam **Hingga Tempoh: Tarikh Mula**, tentukan tarikh untuk entri masa mesti dicipta. Klik **Salin** untuk menyalin entri masa pada hari sama dalam seminggu yang ditunjukkan dalam **Hingga Tempoh**. Contohnya, entri masa Isnin dari minggu lepas akan disalin ke Isnin untuk minggu yang dinyatakan dalam **Hingga Tempoh**. 

![Salin entri masa dalam pukal](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Import data 
Tugasan dan pertukaran mengikut corak UI sama membenarkan pengguna menentukan julat tarikh apabila tempahan perlu diimport. Anda mesti memilih tempahan secara jelas yang harus disalin ke dalam entri masa **Draf**. Dalam versi 3, anda tidak boleh melihat corak entri masa yang **Dicadangkan** pada grid dan kalendar.  

### <a name="change-in-calendar-control"></a>Perubahan dalam kawalan kalendar
Dalam versi 3, ia telah dialihkan daripada kawalan kalendar tersuai dan kini menggunakan Kalendar UC untuk memaparkan entri masa bagi minggu ini. Dengan kalendar ini, anda boleh melihat hari, minggu dan bulan. 

> [!NOTE]
> Pengehadan pada Kalendar adalah kawalan ini tidak menyokong tindakan pada item kalendar individu. Contohnya, anda tidak boleh memilih satu atau lebih item kalendar dan menyerahkan atau memadamkan item tersebut. Mengklik item kalendar akan membuka halaman **Entiti entri masa** untuk tindakan tambahan. 

### <a name="extensibility"></a>Dapat diperluas
**Rekodkan data pada medan tersuai dalam entiti entri masa dan perbelanjaan sahaja** - Entri masa menggunakan grid boleh diedit, grid baca sahaja dan kawalan kalendar daripada platform. Semua kawalan ini asli dan akan menyokong penyesuaian. Dalam Project Service Automation versi 3, anda boleh menambah medan tersuai tambahan, menyediakan medan carian dan menyandarkannya dengan pandangan tersuai. Anda juga boleh menetapkan logik perniagaan tersuai berdasarkan pada nilai yang dipilih dalam medan tersuai.  

**Rekodkan data pada medan tersuai dalam entri masa dan perbelanjaan dan menyebarkannya melalui entiti yang menyokong penyerahan dan aliran kelulusan** - Pemprosesan biasa entri masa ditunjukkan dalam diagram berikut.

![Proses aliran kemasukan masa](media/process-time-entries-10.png)

Jika keperluan perniagaan menetapkan entiti masa dan perbelanjaan mesti merekodkan dimensi penentuan harga tersuai dan menyebarkan nilai yang ditetapkan oleh sumber masa dan entri dalam dimensi penentuan harga tersuai melalui semua entiti dalam grafik sebelumnya, lihat [Tetapkan medan tersuai sebagai dimensi penentuan harga](set-up-pricing-dimensions.md)

Untuk menyokong keperluan perniagaan entiti masa dan perbelanjaan mesti merekodkan dimensi bukan penentuan harga tersuai dan menyebarkan nilai, anda boleh menggunakan persediaan dimensi penentuan harga dan menyatakan dimensi tersuai sebagai dimensi penentuan harga tanpa kos atau kadar bil. Satu lagi senario untuk menambah medan tersuai kepada setiap entiti menggunakan nama medan yang sama merentasi semua entiti. Pasang masuk tersuai boleh dicipta untuk mengaitkan rekod dalam entiti yang terlibat dalam aliran penyerahan/kelulusan menggunakan entiti asal transaksi dan sambungan transaksi.  

### <a name="delegate-time-and-expense-entry"></a>Wakilkan entri masa dan perbelanjaan
Platform Common Data Service tidak menyokong seorang pengguna menyamar sebagai pengguna yang lain, yang bermaksud dalam versi 3 Project Service Automation tidak ada sokongan untuk entri masa dan perbelanjaan wakil. Walau bagaimanapun, rakan kongsi dan pelanggan telah memanfaatkan penyelesaian sementara untuk mendayakan sokongan bagi pengalaman entri masa yang diwakilkan dalam versi 3. Ini hanya penyelesaian sementara dan bukan penyelesaian lengkap, maka penting untuk memahami pengehadan dan hanya menggunakan pendekatan ini jika pengehadan boleh diterima. 

> [!IMPORTANT]
> Maklumat ini hanya boleh dianggap panduan yang dicadangkan untuk pelaksanaan tersuai oleh rakan kongsi/pelanggan. Pasukan produk tidak akan menawarkan sokongan formal untuk fungsi ini melalui mana-mana saluran sokongan kami.

### <a name="customization-details"></a>Butiran penyesuaian 
Penyesuaian membenarkan anda menambah **Sumber boleh ditempah** untuk mencipta dan mengedit pengalaman, yang akan membenarkan pengguna bertindak sebagai wakil dengan mengubah medan **Sumber boleh ditempah** kepada pengguna lain yang entri masa dan perbelanjaan perlu direkodkan. Langkah-langkah berikut meliputi perwakilan entri masa. Maklumat sama digunakan ke atas perbelanjaan perwakilan entri. 
 
1.  Pastikan bahawa pengguna yang diwakilkan mempunyai akses keselamatan global ke atas projek dan tugas projek. 
1.  Oleh sebab medan **Sumber boleh ditempah** pada entiti **Entri masa** tidak didedahkan pada halaman **Cipta pantas**, anda perlu menambahkannya.

    -atau-

    Cipta pandangan tersuai, yang termasuk lajur **Sumber boleh ditempah**, untuk melihat hanya entri masa yang dicipta untuk sumber. Terbitkan penyesuaian pada pereka bentuk modul aplikasi untuk pandangan ini ditunjukkan di bawah **Lihat pemilih** pada halaman **Entri masa**. Terdapat dua pasang masuk yang mengendalikan tetapan pengurus untuk entri masa bukan projek:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Cipta pasang masuk untuk menulis ganti medan **Pengurus** kepada pengurus pengguna yang ditugaskan dalam medan **Sumber boleh ditempah**. Gunakan **Peringkat pelaksanaan** sebagai pasang masuk (prapengesahan) luar jalur (OOB) dan gunakan **Pesanan pelaksanaan** yang lebih tinggi daripada pasang masuk OOB (lebih besar daripada 1). Ini akan memastikan pasang masuk tersuai dilaksanakan selepas pasang masuk OOB.  
 
### <a name="end-user-experience"></a>Pengalaman pengguna akhir
1.  Apabila anda mencipta entri masa pada halaman cipta pantas, masukkan Projek dan butiran tugas Projek, dan kemudian pilih pengguna pada medan **Sumber boleh ditempah** yang mana entri masa perlu direkodkan. 
2.  Secara lalai, medan ini lalai kepada pengguna yang mengelog masuk, walau bagaimanapun pengguna mengatasi medan ini, entri masa kini dicipta untuk **Sumber boleh ditempah** yang dipilih.
3.  Apabila anda menyerahkan entri masa yang anda cipta untuk rekod ini, entri akan dibariskan untuk pelaksana dalam projek seperti yang dijangkakan. 
4.  Apabila anda menarik balik entri masa yang dicipta untuk pengguna lain, entri masa akan dikembalikan kepada keadaan **Draf** dengan medan **Sumber boleh ditempah** ditetapkan kepada pengguna lain. 
5.  Anda boleh menukar kepada pandangan tersuai secara alternatif bagi menapis entri masa yang dicipta untuk pengguna lain. 
 
### <a name="limitations"></a>Had-had
Fungsi **Salin** dan **Import** hanya berfungsi dalam konteks pengguna yang mengelog masuk. Ini bermaksud bahawa tidak mungkin untuk menyalin atau mengimport entri masa yang dicipta untuk pengguna yang mengelog masuk sebagai sumber boleh ditempah.

Entri masa yang bukan untuk projek akan dihalakan untuk kelulusan kepada pengurus sumber oleh ditempah hanya jika langkah 4 di bahagian **Butiran Penyesuaian** di atas selesai. Jika tidak, entri masa bukan projek untuk pengguna lain akan dihalakan secara salah kepada pengurus pengguna yang mengelog masuk. 

### <a name="other-changes"></a>Perubahan lain 
Kefungsian **Tempahan dan Tugas** telah dialih keluar. 

## <a name="multidimensional-pricing"></a>Penentuan harga berbilang dimensi
Untuk memaksimumkan kefleksibelan dan memenuhi keperluan perniagaan yang berbeza, versi 3 Project Service Automation menyokong aplikasi dimensi penentuan harga berasingan yang ditetapkan kepada kos dan kadar bil. Nilai dimensi boleh ditetapkan sebagai lalai dan kemudian disebarkan merentasi proses pengekosan dan penentuan harga daripada pemprofilan sumber kepada entri masa kepada aktual projek. Konfigurasi dan pengubahsuaian atau pelanjutan khusus pelanggan memanfaatkan infrastruktur boleh suai yang standard.

Project Service Automation menghantar dengan set dimensi penentuan harga dan peranan serta unit sumber lalai, dan membolehkan penyediaan harga dan kos bagi setiap gabungan unit Peranan dan Organisasi.

Bagi pelanggan Project Service Automation yang ingin terus menggunakan medan siap guna ini sebagai dimensi penentuan harga dalam versi 3, tidak akan ada sebarang perubahan yang dapat dilihat. Anda boleh terus menggunakan Project Service Automation seperti biasa. Walau bagaimanapun, jika anda perlu meletakkan harga atau kos untuk sumber anda menggunakan atribut tambahan yang lain, versi 3 membenarkan untuk menambah dimensi penentuan harga tersuai anda sendiri kepada Project Service Automation. Pelanjutan dimensi penentuan harga tersuai adalah pengalaman konfigurasi yang rumit. 

## <a name="quotes-and-contracts"></a>Sebut harga dan kontrak
Dalam versi 3 Project Service Automation, aspek persediaan dan pengurusan untuk sebut harga dan kontrak telah diubah. Bahagian berikut menyediakan maklumat lanjut yang terperinci.

### <a name="set-up-chargeability-options"></a>Sediakan pilihan kebolehtuntutan
Dalam versi 1 dan 2, persediaan kebolehtuntutan untuk peranan dan kategori bagi sebut harga dan kontrak tertentu telah dilakukan menggunakan pandangan **Kebolehtuntutan** yang berada dalam navigasi baris sebut harga atau baris kontrak. Inilah juga tempat anda boleh menyediakan harga bagi peranan dan Kategori perbelanjaan.

Seperti versi 3, persediaan pilihan kebolehtuntutan mengikut peranan dan Kategori perbelanjaan akan dilakukan pada peringkat sebut harga atau baris kontrak. Persediaan penentuan harga adalah berasingan daripada persediaan Kebolehtuntutan. Anda akan boleh mencari **Peranan boleh dituntut** dan **Kategori oleh dituntut** seperti tab pada halaman **Baris sebut harga** dan  **Baris kontrak** tanpa perlu menggunakan navigasi bahagian atas.

![Peranan boleh dituntut](media/chargeable-12.png)
 
Persediaan Peranan boleh dituntut dan Kategori boleh dituntut juga memanfaatkan kawalan grid boleh diedit siap guna. Bagi setiap peranan dan kategori, pilihan yang disokong untuk jenis pengebilan semasa fasa Penyebutan Harga dan Pengkontrakan kekal tidak berubah daripada versi terdahulu seperti **Boleh dituntut** dan **Tidak boleh dituntut**. **Percuma** bukan jenis yang disokong semasa fasa Penyebutan Harga atau Pengkontrakan. **Percuma** disokong hanya semasa kelulusan Masa atau Perbelanjaan.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Cipta dan edit penentuan harga tersuai untuk sebut harga dan kontrak projek Project Service Automation
Dalam versi 1 dan 2, menggunakan senarai harga tersuai untuk sebut harga dan kontrak tertentu dilakukan menggunakan **Edit harga** pada pandangan **Kebolehtuntutan**. Pandangan **Kebolehtuntutan** terletak pada navigasi atas baris sebut harga atau baris kontrak. Inilah juga tempat anda boleh menyediakan pilihan kebolehtuntutan untuk peranan dan atau kategori perbelanjaan.

Seperti versi 3, mencipta dan menggunakan senarai harga projek tersuai pada sebut harga Project Service Automation dan kontrak projek Project Service Automation telah dipisahkan daripada persediaan kebolehtuntutan. Sebut harga Project Service Automation dan kontrak projek Project Service Automation mempunyai tab baharu yang dipanggil **Senarai harga projek**. Tab ini menunjukkan pandangan berkaitan bagi semua Senarai harga projek yang dilampirkan pada sebut harga atau kontrak projek Project Service Automation. Untuk mencipta senarai harga tersuai daripada senarai harga sedia ada yang telah dikaitkan dengan sebut harga atau kontrak projek, klik **Cipta penentuan harga tersuai**. Ia akan membuat salinan semua senarai harga berkaitan dan melampirkannya kepada Sebut harga atau kontrak. Kini, anda boleh membuka senarai harga dan mengedit peranan atau harga kategori perbelanjaan supaya perubahan penentuan harga hanya akan digunakan untuk sebut harga atau kontrak ini. 
  
Grafik berikut adalah sebelum senarai harga tersuai telah dicipta.

![Sebelum senarai harga tersuai](media/before-custom-price-lists-13.png)

Grafik berikut ditunjukkan selepas senarai harga tersuai telah dicipta.

![Selepas senarai harga tersuai](media/after-custom-price-lists-14.png)

> [!NOTE]
> Sela pendek mungkin berlaku ketika anda mengklik **Cipta Penentuan Harga Tersuai** sehingga senarai harga tersuai dicipta. Kami mengesyorkan menyegar semula grid dan bukannya mengklik berbilang kali. Senarai harga tersuai telah dicipta jika nama senarai harga berkaitan mempunyai nama sebut harga atau nama kontrak projek yang ditambahkan kepadanya.


[!INCLUDE[footer-include](../includes/footer-banner.md)]