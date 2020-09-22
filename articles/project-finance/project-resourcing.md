---
title: Penyumberan projek
description: Topik ini memberikan maklumat tentang penyumberan projek.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753842"
---
# <a name="project-resourcing"></a>Penyumberan projek

[!include [banner](../includes/banner.md)]

Topik ini memberikan maklumat tentang penyumberan projek.

Satu cabaran untuk pengurus projek dan pengurus sumber semasa peringkat perancangan projek ialah peruntukan sumber, di mana mereka mesti menentukan dan menguntukkan sumber yang betul untuk kerja projek. Dalam Dynamics 365 Finance, keupayaan penyumberan untuk projek membolehkan anda mentakrifkan peranan yang dianggap sebagai sumber sementara yang boleh diperuntukkan untuk penglibatan khusus atau sebahagian daripada penglibatan. Jenis penyumberan ini membolehkan pengurus projek dan pengurus sumber melengkapkan tugas berikut:

- Mentakrifkan peranan yang mempunyai kecekapan yang diperlukan, supaya mudah untuk dipadankan dengan sumber.
- Gunakan peranan untuk mentakrifkan jadual penglibatan awal yang berdasarkan sumber diperuntukkan.
- Anggaran kos dan menentukan belanjawan awal, berdasarkan peranan dan sumber yang ditugaskan untuk projek.
- Gunakan peranan untuk menganggarkan bilangan tempahan sumber yang diperlukan untuk setiap penglibatan.
- Anggaran bilangan sumber yang diperlukan untuk seluruh kitaran hayat projek.
- Draf struktur pecahan kerja (WBS) dengan menggunakan tugasan sumber awal.

[![Kitaran hayat projek](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Semasa perancangan projek berjalan, sumber yang dirancang boleh digantikan dengan sumber diperlukan. Pengurus Projek juga boleh kembali dan mengemas kini tempahan penyumberan semasa sebarang peringkat projek.

## <a name="set-up-project-resources"></a>Sediakan sumber projek
Anda mesti menyediakan kalendar dan kaitkannya dengan pekerja atau pekerja. Kalendar digunakan untuk menjadualkan projek dan masa kerja sumber yang diperuntukkan untuk projek. Semasa persediaan kalendar, pengurus projek boleh lakukan pelarasan sumber sebagai sebahagian daripada pengoptimuman sumber. Berdasarkan jadual kalendar, sekatan boleh diletakkan pada sumber. Anda boleh menyediakan kalendar pada halaman **Kalendar**.

Apabila anda menyediakan pekerja sebagai sumber projek, anda boleh memilih daripada pekerja yang bekerja dalam syarikat tempat anda menyediakan sumber. Secara alternatif, anda boleh memilih pekerja daripada syarikat lain dalam organisasi anda. Pekerja ini dikenali sebagai sumber antara syarikat.

Prosedur berikut menerangkan cara untuk menyediakan pekerja sebagai sumber projek dalam syarikat anda dan cara untuk menyediakan sumber projek antara syarikat.

### <a name="set-up-a-worker-as-a-project-resource"></a>Sediakan pekerja sebagai sumber projek

1. Pada halaman **Pekerja**, dalam senarai **Pekerja**, pilih pekerja yang anda tambah sebagai sumber projek dan buka rekod pekerja.
2. Pada Anak Tetingkap Tindakan, pilih **Projek** &gt; **Persediaan** &gt; **Persediaan projek**.
3. Pilih kalendar, dan kemudian tutup halaman.

Anda juga boleh menentukan projek lalai untuk sumber sebagai jenis pra-tugasan. Pra-tugasan boleh digunakan apabila pengurus sumber atau pengurus projek mengetahui projek sumber yang mana akan berjalan terlebih dahulu. Pra-tugasan juga boleh berdasarkan kepada permintaan penaja projek atau pelanggan. Untuk membuat pra-tugaskan projek, pada halaman **Tugaskan projek**, pada tab **Projek**, dalam senarai **Baki projek**, pilih projek yang sesuai.

### <a name="set-up-an-intercompany-resource"></a>Sediakan sumber antara syarikat

Apabila anda menyediakan pekerja sebagai sumber antara syarikat, anda mesti melengkapkan persediaan dalam kedua-dua syarikat pinjaman dan syarikat peminjaman.

**Dalam syarikat pinjaman**

1. Dalam Kewangan, sahkan bahawa syarikat pinjaman dipilih, dan kemudian lengkapkan prosedur dalam bahagian sebelumnya, "Sediakan pekerja sebagai sumber projek."
2. Pada halaman **Perakaunan antara syarikat**, pilih **Baharu**.
3. Dalam medan **ID entiti undang-undang**, pilih syarikat pinjaman. Isikan medan yang selebihnya mengikut kesesuaian, dan kemudian pilih **Simpan**.
4. Pada halaman **Pemindahan harga**, pilih **Baharu**.
5. Dalam medan **Entiti undang-undang peminjaman**, pilih syarikat yang sesuai.
6. Untuk meminjamkan syarikat peminjaman hanya sumber yang anda cipta pada permulaan bahagian ini, dalam medan **Sumber**, pilih nama sumber yang anda cipta. Untuk menjadikan semua sumber dalam syarikat pinjaman tersedia kepada syarikat peminjaman, sila tinggalkan medan **Sumber** kosong.
7. Pada halaman **Pengurusan projek dan parameter perakaunan**, pada tab **Antara Syarikat**, tetapkan pilihan **Dayakan penjadualan sumber antara syarikat dan lembaran masa** kepada **Ya**.

**Dalam syarikat peminjaman**

- Pada halaman **Senarai sumber**, dalam penapis carian, masukkan nama sumber yang anda cipta untuk syarikat pinjaman, untuk mengesahkan bahawa nama tersebut disertakan dalam senarai sumber untuk syarikat peminjaman.

## <a name="manage-resource-competencies"></a>Urus kecekapan sumber
Kecekapan sumber merupakan bahagian penting dalam pengurusan sumber. Kecekapan boleh digunakan sebagai garis dasar untuk menentukan sumber yang mempunyai keseimbangan kemahiran, pendidikan, pensijilan dan pengalaman projek yang betul. Anda harus menyediakan maklumat ini untuk setiap sumber dan kemas kini secara tetap. Dengan cara ini, anda boleh memaksimumkan keupayaan apabila kecekapan sumber khusus dipadankan semasa tugasan sumber projek.

[![Contoh kemahiran, persijilan, pendidikan dan pengalaman projek](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Prosedur berikut menerangkan cara untuk menyediakan beberapa kecekapan untuk sumber.

Untuk menyediakan kecekapan untuk pekerja, anda boleh menggunakan sama ada halaman senarai **Pekerja** dalam Sumber manusia atau halaman senarai **Sumber** dalam Pengurusan projek dan perakaunan. Untuk prosedur berikut, halaman senarai **Pekerja** dalam Sumber manusia digunakan.

### <a name="set-up-competencies-certificates"></a>Sediakan kecekapan: Sijil

1. Pada halaman senarai **Pekerja**, pilih baris untuk pekerja untuk menambah maklumat sijil.
2. Pada Anak Tetingkap Tindakan, pada tab **Pekerja**, dalam kumpulan **Kecekapan**, pilih **Sijil**.
3. Pilih **Baharu**, dan kemudian, dalam medan **Jenis sijil**, pilih **PMP**.
4. Dalam medan **Tarikh mula**, pilih **10/1/2015**, dan pilih **Simpan**.

### <a name="set-up-competencies-skills"></a>Sediakan kecekapan: Kemahiran

1. Pada halaman senarai **Pekerja**, pastikan bahawa pekerja yang anda gunakan dalam prosedur sebelumnya masih dipilih. Kemudian, pada Anak Tetingkap Tindakan, pada tab **Pekerja**, dalam kumpulan **Kecekapan**, pilih **Kemahiran**.
2. Pilih **Baharu**.
3. Dalam medan **Kemahiran**, pilih **Pengurusan projek**.
4. Dalam medan **Tahap**, pilih **5 Pakar**.
5. Dalam medan **Tarikh tahap**, pilih **14/1-/2014**.
6. Dalam medan **Tahun pengalaman**, masukkan **10**.
7. Pilih **Simpan**, dan kemudian tutup halaman.

## <a name="create-a-new-project"></a>Cipta projek baharu
1. Pada halaman **Pengurusan projek**, pilih **Projek baharu**, dan masukkan nilai berikut:

    - **Jenis projek:** Masa dan bahan
    - **Nama projek:** Naik taraf XYZ Fasa 2
    - **Kumpulan projek:** TM\_WIP
    - **ID kontrak projek:** 00000002

2. Pilih **Cipta projek**.

### <a name="assign-a-resource-to-a-project"></a>Tugaskan sumber kepada projek

1. Pada halaman **Pekerja**, dalam senarai **Pekerja**, pilih rekod untuk pekerja yang sebelum ini anda sediakan kecekapan, dan buka rekod pekerja.
2. Pada Anak Tetingkap Tindakan, pada tab **Projek**, dalam kumpulan **Persediaan**, pilih **Tugaskan projek**.
3. Pada halaman **Tugasan projek pengesahan sumber**, pada tab **Projek**, dalam medan **Tambah projek ke projek dipilih**, tapis pada projek **Naik taraf XYZ Fasa 2**.
4. Dalam anak tetingkap **Baki projek**, pilih projek, dan kemudian pilih butang anak panah untuk menambahnya ke anak tetingkap **Projek dipilih**.

Anda juga boleh tugaskan kategori untuk sumber yang anda perlukan. Jenis kategori ialah sama ada **Kos** atau **Hasil**. Jenis kategori adalah ditentukan oleh organisasi anda. Jika tiada kategori ditugaskan untuk sumber, Kewangan mencari kategori lalai pada harga jam bagi kos dan hasil.

### <a name="set-up-project-resource-and-role-characteristics"></a>Sediakan sumber projek dan ciri peranan

Pengurus projek boleh menggunakan kefungsian penyumberan projek untuk mencipta peranan yang diperlukan untuk projek. Peranan boleh digunakan jika sumber yang disahkan masih tidak diketahui apabila sumber diperuntukkan. Peranan boleh diperuntukkan sementara sebagai sumber yang dirancang, supaya anda boleh meneruskan peringkat perancangan projek.

[![Contoh peranan](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senario:** Ariffin diupah untuk melengkapkan Projek masa dan bahan yang mempunyai piagam projek yang diluluskan. Pengurus projek muda masih melengkapkan skop projek. Resource manager pada masa ini sedang mengenal pasti sumber tertentu yang akan diperuntukkan untuk bekerja pada projek baharu. Oleh kerana sifat kritikal projek itu, penaja projek meminta Pengurus projek kanan sebagai salah satu peranan. Resource manager mesti mendapatkan sumber baharu dan mentakrifkan peranan dalam sistem sekiranya pengurus projek muda memerlukan maklumat sumber semasa perancangan projek.

Langkah berikut menunjukkan cara resource manager boleh menyediakan peranan Pengurus projek kanan dan kaitkan ciri sumber dengannya. Kemudian, peranan boleh digunakan untuk carian sumber tersedia yang sepadan dengan kecekapan sumber yang diperlukan.

1. Pada halaman **Peranan persediaan**, pilih **Baharu**, dan masukkan nilai berikut:

    - **ID peranan:** Pengurus Projek Kanan
    - **Perihalan** Pengurus Projek Kanan

2. Pilih **Cipta**.
3. Pilih peranan **Pengurus Projek Kanan**, dan kemudian pilih **Ciri konfigurasi**.
4. Dalam medan **Jenis ciri**, pilih **Kemahiran**.
5. Dalam medan **Ciri tersedia**, masukkan kemahiran untuk carian.
6. Dalam medan **Jenis ciri**, pilih **Sijil**.
7. Dalam medan **Ciri tersedia**, masukkan jenis sijil untuk carian.

### <a name="assign-a-project-resource-to-a-project"></a>Tugaskan sumber projek kepada projek

1. Pada halaman **Semua projek**, pilih projek **Naik taraf XYZ Fasa 2**.
2. Pada tab **Pasukan projek dan penjadualan**, pilih **Tambah**.
3. Dalam medan **Peranan**, pilih **Ahli pasukan**.
4. Pilih **Tempah daripada kalendar**.
5. Pada halaman **Ketersediaan sumber**, pilih **Pandangan tetapan**.
6. Pada halaman **Laraskan pandangan tetapan**, masukkan nilai berikut:

    - **Format untuk tarikh pandangan julat:** Hari
    - **Paparan perihalan ketersediaan:** Ya
    - **Paparan kapasiti baki:** Ya

7. Dalam senarai sumber, pilih sumber.
8. Pilih **Tempah Keras** dan **Kapasiti penuh**.


### <a name="assign-a-resource-to-a-default-role"></a>Tugaskan sumber kepada peranan lalai

Untuk membantu projek atau pengurus projek boleh gerudi bawah lebih lanjut tentang sumber yang boleh diperuntukkan untuk projek. Anda boleh kaitkan peranan lalai dengan sumber sedia ada atau sumber yang baharu diperolehi. Contohnya, apabila Daniel diupah, beliau mempunyai pengalaman dan kemahiran untuk mengisi peranan Penganalisis perniagaan. Resource manager ditugaskan peranan ini sebagai peranan lalai Daniel. Oleh itu, resource manager menambah Daniel kepada himpunan penganalisa perniagaan yang bersedia untuk mengerjakan projek.

Semasa tempahan sumber, pengurus projek boleh menapis sumber peranan yang tersedia untuk mengerjakan projek. Mereka boleh menggunakan maklumat ini sebagai satu kriteria apabila mereka melaksanakan analisis keputusan berbilang kriteria semasa pemenuhan sumber. Mereka juga boleh menambah ciri sumber lain kepada penapis untuk carian sumber yang mempunyai kemahiran, pendidikan, dan pengalaman khusus untuk projek yang diberikan.

**Senario:** Projek yang diluluskan telah dimulakan, dan peranan Pengurus projek kanan telah diperuntukkan sebagai sumber yang dirancang semasa peringkat perancangan projek. Resource manager kini telah memperolehi sumber untuk memenuhi peranan Pengurus projek kanan.

1. Pada halaman **Senarai sumber**, pilih **Daniel Goldschmidt**.
2. Pada halaman **Peranan sumber**, pilih **Baharu**, dan masukkan nilai berikut:

    - **Berkuat kuasa:** Masukkan tarikh semasa.
    - **Tamat tempoh:** Masukkan **Jangan sekali-kali**.
    - **Peranan:** Masukkan **Pengurus Projek Kanan**.

3. Pilih **Simpan**, dan kemudian tutup halaman.
4. Pada tab **Kecekapan**, tambah kemahiran **ProjectMgmt** dan sijil **PMP**.

## <a name="set-up-role-based-pricing"></a>Sediakan harga berasaskan peranan
Semua kos, jualan dan harga pemindahan boleh disediakan untuk peranan.

1. Pada halaman **Harga jualan (jam)**, pilih **Baharu**, dan masukkan tarikh berkuat kuasa.
2. Dalam lajur **Peranan**, pilih peranan.
3. Dalam lajur **Harga**, masukkan harga untuk peranan sumber yang dipilih.

## <a name="form-a-project-team"></a>Bentuk pasukan projek
Untuk menggunakan peranan yang sebelum ini disediakan dalam projek, pengurus projek mesti kaitkan peranan dengan projek. Berbilang peranan boleh ditugaskan untuk projek. Untuk mengelakkan kekeliruan, peranan ini dilabelkan secara automatik semasa penempahan. Contohnya, jika pengurus projek memerlukan tiga jurutera perisian, tiga peranan jurutera Perisian yang mempunyai **jurutera perisian 1**, **perisian Jurutera 2**, dan **jurutera perisian 3** sebagai label mereka dijana secara automatik. Jika ciri peranan sebelum ini telah ditetapkan untuk peranan, ia akan digunakan sebagai penapis semasa mencari sumber. Ciri tambahan boleh ditambah apabila diperlukan untuk sempurnakan lagi carian.

Tetapan pandangan juga boleh disesuaikan untuk memberi pandangan yang lebih baik tentang ketersediaan sumber. Terdapat pilihan untuk menunjukkan ketersediaan setiap jam, harian, mingguan, bulanan, suku tahunan, dan tahunan. Terdapat juga pilihan untuk menunjukkan kapasiti pada sumber yang tersedia dan yang selebihnya. Pilihan ini berguna untuk pengurusan masa, apabila anda menganggarkan masa tersedia untuk aktiviti atau ketersediaan sumber.

Pengurus projek boleh memilih peranan pada halaman dan kemudian, jika terdapat sumber tersedia yang sesuai dengan keperluan, pilih untuk menguntukkan sumber untuk memenuhi peranan. Ambil perhatian bahawa sumber tidak perlu diperuntukkan pada masa ini dalam peringkat perancangan. Apabila anda mencipta WBS, anda boleh menggantikan peranan dengan sumber diperlukan untuk projek. Jika peranan digantikan dengan sumber diperlukan dalam WBS, persediaan sumber secara automatik mengemas kini senarai pasukan dan penjadualan projek.

[![Senarai pasukan projek yang merangkumi kedua-dua peranan dan sumber sebenar](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Pengurus projek mempunyai pelbagai pilihan untuk menempah sumber untuk projek, seperti **Baki kapasiti**, **Kapasiti penuh**, **Peratusan kapasiti** dan **Tentukan jam**. Pilihan penempahan ini boleh dibatalkan pada bila-bila masa jika tugasan sumber berubah. Dua jenis penempahan disokong:

- **Tempah Keras** – Tempahan sumber telah diluluskan dan disahkan untuk bekerja pada perikatan untuk tempoh yang ditetapkan.
- **Tempah sementara** – Tempahan sumber telah secara sementara ditetapkan untuk bekerja pada perikatan untuk tempoh yang ditetapkan.

Prosedur berikut menjelaskan cara mencipta pasukan projek.

### <a name="create-a-project-team"></a>Cipta pasukan projek

1. Pada halaman senarai **Semua projek**, pilih projek, dan kemudian pilih **Edit**.
2. Pada tab **Pasukan projek dan penjadualan**, dalam medan **Tarikh akhir jadual**, masukkan tarikh mula jadual tambah satu bulan. Contohnya, jika tarikh mula jadual adalah 24 Jun, 2017 (24/06/2017), masukkan **24/07/2017**.
3. Pilih **Tambah**.
4. Dalam anak tetingkap **Tambah peranan kepada projek**, dalam medan **Peranan**, pilih **Pengurus Projek Kanan**.
5. Pilih **Kecekapan yang diperlukan**.
6. Pada halaman **Pilih ciri**, ciri yang anda tetapkan sebelum ini untuk peranan Pengurus projek kanan dipilih secara lalai. Pilih **OK**.
7. Pada halaman **Tambah peranan kepada projek**, dalam medan **Bilangan sumber**, masukkan **1**.
8. Dalam medan **Sumber**, carian menunjukkan semua sumber yang mempunyai kecekapan yang diperlukan. Pilih **Daniel Goldschmidt**, dan kemudian pilih **Cipta**.
9. Pada halaman **Projek**, pilih **Tambah**.
10. Dalam anak tetingkap **Tambah peranan kepada projek**, dalam medan **Peranan**, pilih **Ahli pasukan**. Dalam medan **Bilangan sumber**, masukkan **5**.
11. Pilih **Cipta**.
12. Pada halaman **Projek**, pilih **Memenuhi sumber**.

## <a name="resource-capacity-synchronization"></a>Penyegerakan kapasiti sumber
Proses untuk penyegerakan sumber membantu menjamin yang maklumat untuk kalendar dan kalendar asas masuk ke dalam penjadualan sumber projek. Jika kalendar diubah, proses membuat kemas kini yang diperlukan untuk penjadualan sumber projek. Proses ini juga membantu menambah baik prestasi, kerana maklumat sumber kalendar disegerakkan lebih awal. Oleh itu, kemas kini kepada maklumat penjadualan sumber berlaku lebih cepat. Kami mengesyorkan anda menjadualkan proses sebagai kelompok dan bukannya satu demi satu. Jika tidak, ada risiko bahawa seseorang akan melupakan tarikh yang terangkum apabila maklumat terakhir disegerakkan. Jika tarikh yang terangkum tidak digunakan, jurang boleh berlaku semasa tarikh penyegerakan.

![Penyegerakan kalendar](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Segerakkan gulungan kapasiti sumber

Proses penyegerakan direka untuk segerakkan semua maklumat kalendar sumber. Maklumat ini termasuk maklumat kalendar asas mengenai sebarang perubahan kepada jadual Kapasiti kalendar sumber projek. Jika sumber baharu ditambah dalam projek ini, penyegerakan membantu menjamin bahawa maklumat kalendar yang dikemas kini tersedia. Penyegerakan ini boleh dilakukan pada bila-bila masa.

Kami mengesyorkan agar anda menggunakan kelompok. Pilihan boleh tersedia semasa penyegerakan penempahan kapasiti.

1. Pilih **Pengurusan projek dan perakaunan** &gt; **Berkala** &gt; **Penyegerakan kapasiti** &gt; **Segerakkan gulungan kapasiti sumber**.
2. Tetapkan pilihan dalam jadual berikut.

    | Pilihan      | Penerangan |
    |-------------|-------------|
    | Kod tempoh | Secara alternatif pilih kod selang tarikh Lejar am untuk menetapkan tarikh mula dan tamat untuk proses penyegerakan untuk gulungan kapasiti sumber. |
    | Tarikh mula  | Masukkan tarikh mula untuk proses penyegerakan untuk gulungan kapasiti sumber. |
    | Tarikh tamat    | Masukkan tarikh tamat untuk proses penyegerakan untuk gulungan kapasiti sumber. |

[![Proses penyegerakan](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Sediakan peranan pada templat WBS
Pengurus projek boleh menyediakan templat WBS yang boleh mereka menggunakan apabila mereka mencipta WBS untuk projek baharu. Pengurus projek boleh menambah peranan apabila mereka mencipta templat. Gunakan prosedur berikut untuk tugaskan peranan kepada templat WBS.

1. Pilih **Pengurusan projek dan perakaunan** &gt; **Persediaan** &gt; **Projek** &gt; **Templat struktur pecahan kerja**.
2. Pilih **Butiran** untuk templat WBS yang dipilih.
3. Pilih tugas dalam senarai, dan kemudian, dalam medan **Peranan**, pilih peranan untuk tugaskan kepada tugas tersebut.

### <a name="work-with-a-wbs"></a>Bekerja dengan WBS

Anda boleh mencipta WBS baharu, atau anda boleh menyalin WBS daripada templat WBS sedia ada. Pengurus projek boleh mengurus sumber dengan mudah dengan menugaskan peranan kepada tugas baharu dalam WBS. Peranan boleh digantikan sama ada selepas sumber diperolehi atau selepas sumber yang disahkan untuk kerja pada tugas adalah dikenal pasti. Fleksibiliti ini membolehkan pengurus projek melaksanakan tugas berikut:

- Kenal pasti bilangan sumber yang diperlukan untuk pakej kerja WBS.
- Anggarkan kos projek.
- Tentukan belanjawan awal.
- Anggarkan tempoh aktiviti, berdasarkan peranan dan sumber.
- Bangunkan beberapa pelan pengurusan projek, berdasarkan maklumat projek yang tersedia.

Pilihan tambahan telah ditambah dalam WBS untuk menggunakan kefungsian penyumberan dengan lebih baik.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pilihan</th>
<th>Penerangan</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Penugasan sumber</td>
<td>Lihat sumber, tarikh, bilangan jam, dan jenis tempahan yang diberikan untuk tugas pada WBS.</td>
</tr>
<tr class="even">
<td>Menjana pasukan secara automatik</td>
<td>Tambah sumber yang dirancang secara automatik dengan menggunakan peranan yang berkaitan dengan tugas. Kewangan secara automatik mencadangkan sumber yang dirancang dengan menggunakan analisis keputusan berbilang kriteria berdasarkan peranan. Selepas peranan dan usaha (jam) telah ditetapkan untuk tugas dalam WBS, dan selepas struktur telah dikeluarkan, pilih <strong>Menjana pasukan secara automatik</strong>. Bilangan sumber yang dirancang yang diperlukan akan ditambahkan ke WBS dan tab <strong>Penjadualan projek dan pasukan</strong>.</td>
</tr>
<tr class="odd">
<td>Sumber (senarai juntai bawah)</td>
<td>Pada halaman <strong>Lancarkan tugasan sumber</strong>, anda boleh memilih sumber untuk menempah tetap atau menempah sementara, berdasarkan tempoh yang ditentukan. Anda boleh melaraskan tetapan pandangan untuk melihat dan menetapkan tempoh aktiviti sumber. Anda boleh memilih dan tugaskan sumber pada tahap pakej kerja dengan menggunakan pilihan berikut:
<ul>
<li><strong>Terima</strong> – Sahkan perubahan kepada sumber yang ditugaskan kepada tugas.</li>
<li><strong>Batalkan</strong> – Batalkan perubahan kepada sumber yang ditugaskan kepada tugas.</li>
<li><strong>Tugaskan secara automatik</strong> – Sumber diperlukan tersedia yang mempunyai peranan sepadan yang dipilih secara automatik dan ditugaskan kepada tugas yang dipilih.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Pada halaman **Semua projek**, pilih projek **Naik taraf XYZ Fasa 2**.
2. Pilih **Rancang** &gt; **Aktiviti** &gt; **Struktur pecahan kerja**.
3. Pilih **Baharu** untuk menambah aktiviti tahap satu yang berikut kepada WBS:

    - Memulakan
    - Perancangan
    - Melaksanakan
    - Pemantauan dan Kawalan
    - Tutup

4. Tetapkan tarikh dan usaha (jam), seperti yang ditunjukkan dalam ilustrasi berikut.

    [![Tetapan tarikh dan usaha](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pilih baris tugas **Memulakan**, dan kemudian, dalam medan **Peranan**, pilih **Pengurus Projek Kanan**.
6. Pilih **Terbitkan**.
7. Pada baris yang sama, dalam medan **Sumber**, pilih **Daniel Goldschmidt**, dan kemudian pilih **Terima**.
8. Pilih baris tugas **Perancangan**, dan kemudian, dalam medan **Peranan**, pilih **Penganalisis perniagaan**.
9. Pilih **Terbitkan**, dan kemudian pilih **Menjana pasukan secara automatik**.
10. Dalam kotak mesej yang muncul, pilih **Ya**.
11. Dalam medan **Sumber**, sahkan bahawa nilai adalah **Penganalisis perniagaan 1**.
12. Untuk sumber **Penganalisis perniagaan 1**, buka carian, dan pilih **Lancarkan tugasan sumber**. Kemudian pilih pekerja untuk tugas itu.
13. Pilih **Tugaskan sementara** &gt; **Kapasiti penuh**.

    > [!NOTE] 
    > Anda tidak menerima amaran bahawa sumber yang ditentukan adalah kini 2, kerana bilangan sumber kekal 1.

14. Pada halaman **Struktur pecahan kerja**, mengesahkan tugasan sumber pada WBS, dan kemudian pilih **Simpan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Pemenuhan sumber untuk sumber yang dirancang
Pengurus projek boleh merancang peranan sumber yang diperlukan untuk projek. Pengurus sumber akan melihat sumber yang dirancang ini sebagai permintaan pada halaman **Pemenuhan sumber** dan boleh tugaskan sumber sebenar.

1. Pada halaman **Semua projek**, pilih projek **Naik taraf XYZ Fasa 2**.
2. Pilih **Projek**, dan kemudian pilih **Edit**.
3. Pada tab **Pasukan projek dan penjadualan**, pilih **Tambah**.
4. Dalam kotak dialog **Tambah peranan**, pilih peranan **Pembangun perisian**.
5. Pilih **Cipta**, dan kemudian tutup halaman projek.
6. Pada halaman **Pemenuhan sumber**, pilih **Pembangun perisian 1** untuk projek **Projek naik taraf XYZ Fasa 2**.
7. Pilih pekerja, dan kemudian pilih **Tugaskan**.
8. Sahkan bahawa baris untuk **Pembangun perisian 1** telah dialih keluar untuk projek **Projek naik taraf XYZ Fasa 2**.
9. Pada tab **Pasukan dan penjadualan projek**, untuk **Projek naik taraf XYZ Fasa 2**, sahkan bahawa pekerja yang anda pilih dalam langkah sebelumnya telah ditambah sebagai **Pembangun perisian**.

## <a name="requests-for-project-resources"></a>Permintaan untuk sumber projek
Kefungsian untuk penjadualan sumber projek hanya membolehkan pengurus sumber edarkan sumber yang diperlukan dalam penglibatan atau projek. Untuk mendayakan kefungsian ini, lengkapkan tugas berikut, atau sahkan yang telah dilengkapkan:

- Sediakan jujukan nombor.
- Sediakan aliran kerja pengurusan projek dan perakaunan.
- Dayakan aliran kerja permintaan sumber.

Selepas tugas sebelum ini dilengkapkan, anda boleh melengkapkan tugas berikut seperti yang anda perlukan:

- Cipta permintaan sumber daripada sumber diperlukan yang ditempah sementara.
- Pantau permintaan sumber.
- Penuhi permintaan sumber.
- Minta sumber yang diperlukan daripada WBS.
- Tempah sumber untuk projek tanpa mempunyai permintaan untuk sumber yang diperlukan.

## <a name="monitor-project-teams"></a>Pantau pasukan projek
1. Pada halaman **Semua projek**, pilih paut **Projek ID** untuk projek **Naik taraf XYZ Fasa 2**.
2. Pada Fasttab **Pasukan dan penjadualan projek**, mengesahkan bahawa sumber projek yang disenaraikan adalah betul.
