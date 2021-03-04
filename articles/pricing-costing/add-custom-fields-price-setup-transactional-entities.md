---
title: Tambah medan tersuai yang diperlukan untuk persediaan harga dan entiti transaksi
description: Topik ini menyediakan maklumat tentang cara menambah rujukan medan tersuai yang diperlukan ke entiti dan ke borang serta pandangan.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c324e0e8797d0b6d3a06ffc2a40b787a475c49b5
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590912"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Tambah medan tersuai yang diperlukan untuk persediaan harga dan entiti transaksi

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Topik ini menganggap bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai yang digunakan sebagai dimensi penetapan harga](create-custom-fields-entities-pricing-dimensions.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini. 

Dalam topik ini, prosedur akan menunjukkan anda cara menambah medan tersuai diperlukan yang merujuk kepada entiti dan kepada unsur antara muka pengguna (UI) seperti borang dan pandangan.

## <a name="add-custom-pricing-dimension-fields"></a>Tambah medan dimensi penentuan harga tersuai 
Selepas medan dan entiti tersuai dicipta, langkah seterusnya ialah untuk membuat persediaan harga dan entiti yang maklum dengan entiti tersuai atau set pilihan dengan mencipta medan keutamaan. Bergantung pada sama ada senarai dimensi penentuan harga anda memasukkan dimensi set pilihan atau dimensi entiti atau kedua-duanya, ikuti hanya langkah dalam **Dimensi penentuan harga tersuai berasaskan set pilihan** atau **Dimensi penentuan harga tersuai berasaskan entiti**, atau kedua-duanya, masing-masing.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensi penentuan harga tersuai berasaskan set pilihan
Apabila dimensi penetapan harga tersuai adalah berasaskan set pilihan, tambahkannya sebagai medan ke entiti utama. Dalam prosedur berikut, **Lokasi Kerja Sumber** dan **Waktu Bekerja Sumber** digunakan sebagai dimensi penentuan harga berasaskan set pilihan. Ini mestilah terlebih dahulu ditambah sebagai medan untuk entiti penentuan harga, **Harga Peranan** dan **Tokokan Harga Peranan**.

1. Dalam Project operations, pilih **Tetapan** > **Penyelesaian** dan klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Harga Peranan**.
3. Kembangkan entiti **Harga Peranan** dan pilih **Medan**.
4. Pilih **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih **Set Pilihan** sebagai jenis medan. 
5. Pilih **Gunakan set Pilihan sedia ada**, pilih set pilihan **Lokasi Kerja Sumber**, kemudian pilih **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan pada entiti **Tokokan Harga Peranan**. 
7. Ulangi langkah 1 - 5 untuk set pilihan **Waktu Bekerja Sumber**.

> [!IMPORTANT]
> Apabila anda menambah medan kepada lebih daripada satu entiti, guna nama medan sama dalam semua entiti. 

> ![Menambah Lokasi Kerja Sumber pada Harga Peranan](media/RWL-Field.png)

Dalam jualan dan fasa anggaran untuk projek, anggaran untuk usaha kerja yang diperlukan untuk melengkapkan kerja **Tempatan** dan **Di Tapak**, dalam **Jam biasa** dan **Jam lebih masa**  digunakan untuk menganggarkan nilai Sebut Harga/Projek Medan **Lokasi Kerja Sumber** dan **Waktu Bekerja Sumber** akan ditambah dalam entiti anggaran, **Butiran Baris Sebut Harga**, **Butiran Baris Kontrak**, **Ahli Pasukan Projek**, dan **Baris Anggaran**.

1. Dalam Project operations, pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Butiran Baris Sebut Harga**.
3. Kembangkan entiti **Butiran Baris Sebut Harga** dan pilih **Medan**.
4. Pilih **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih jenis medan **Set Pilihan**. 
5. Pilih **Guna set pilihan sedia ada** dan **Lokasi Kerja Sumber** dan kemudian pilih **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan pada **Butiran baris Kontrak Projek**, **Ahli Pasukan Projek**, dan entiti **Baris Anggaran**.
7. Ulangi langkah 1 - 6 untuk set pilihan **Waktu Bekerja Sumber**. 

> ![Menambah Lokasi Kerja Sumber pada Baris Anggaran](media/RWL-Default-Value.png)

Untuk penghantaran dan pengivoisan, kerja yang telah selesai perlukan diberikan harga dengan tepat untuk memilih sama ada ia dijalankan secara **Tempatan** atau **Di Tapak**, dan sama ada ia dilengkapkan semasa **Jam biasa** atau **lebih masa** dalam Aktual Projek. Medan **Lokasi Kerja Sumber** dan **Jam Kerja Sumber** hendaklah ditambah pada entiti **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Baris Jurnal**.

1. Pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**.
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Entri Masa**.
3. Kembangkan entiti **Butiran Baris Sebut Harga** dan pilih **Medan**.
4. Pilih **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih **Set Pilihan** sebagai jenis medan. 
5. Pilih **Gunakan set Pilihan sedia ada**, pilih set pilihan **Lokasi Kerja Sumber**, kemudian pilih **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan pada entiti **Aktual**, **Butiran Baris Invois**, dan **Baris Jurnal**.
7. Ulangi langkah 1 - 6 untuk set pilihan **Waktu Bekerja Sumber**. 

> ![Menambah Lokasi Kerja Sumber pada Entri Masa](media/RWL-time-entry.png)

Ini melengkapkan perubahan skema yang diperlukan untuk dimensi tersuai berasaskan pilihan.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensi penentuan harga tersuai berasaskan entiti

Apabila dimensi penetapan harga tersuai adalah entiti, anda akan menambah hubungan 1:N antara entiti dimensi dan entiti utama. Menggunakan contoh Jawatan Standard dari atas, adalah munasabah untuk menjangkakan setiap pekerja ditugaskan jawatan standard. Hasilnya, anda perlu hubungan 1:N daripada Jawatan Standard untuk Sumber Boleh Ditempah, atau hubungan N:1 jika ia dicipta daripada Sumber Boleh Ditempah untuk Jawatan Standard.

1. Dalam Project operations, pilih **Tetapan** > **Penyelesaian** dan kemudian klik dua kali **\<your organization name> dimensi penetapan harga**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
3. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
4. Pilih **Baharu** untuk mencipta hubungan 1:N baharu yang dipanggil **Gelaran Standard untuk Sumber Boleh Ditempah**. Masukkan maklumat diperlukan dan kemudian pilih **Simpan**.

> ![Menambah Jawatan Standard sebagai medan rujukan untuk Sumber Boleh Ditempah](media/ST-BR.png)

Gelaran Standard juga perlu ditambah pada entiti Penetapan Harga, **Harga Peranan** dan **Tokokan Harga Peranan**. Ini juga dilengkapkan menggunakan hubungan 1:N antaran entiti **Jawatan Standard** dan **Harga Peranan** dan entiti **Jawatan Standard** dan **Tokokan Harga Peranan**.

1. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
2. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
3. Pilih **Baharu** untuk mencipta hubungan 1:N baharu yang dipanggil **Gelaran Standard untuk Harga Peranan**. Masukkan maklumat diperlukan dan kemudian pilih **Simpan**.
4. Ulangi langkah 1 - 4 untuk mencipta hubungan 1:N antara entiti **Jawatan Standard** dan **Tokokan Harga Peranan**,

Dalam jualan dan fasa anggaran untuk projek, untuk memberikan harga bagi Sebut Harga/Projek, anggaran usaha kerja diperlukan untuk setiap jawatan standard. Ini bermakna hubungan 1:N daripada Tajuk Standard untuk setiap entiti anggaran ini diperlukan: 

- **Butiran Baris Sebut Harga**
- **Butiran Baris Kontrak Projek**
- **Ahli Pasukan Projek**
- **Garisan Anggaran**

5. Ulangi langkah 1 - 5 untuk mencipta hubungan 1:N dari **Jawatan Standard** kepada **Butiran Baris Sebut Harga**, **Butiran Baris Kontrak Projek**, **Ahli Pasukan Projek**, dan **Baris Anggaran**.

> ![Menambah Jawatan Standard sebagai medan rujukan untuk Baris Anggaran](media/ST-Estimate-Line.png)

  Dalam fasa Penghantaran dan Penginvoisan, kerja yang selesai oleh setiap jawatan standard mestilah diberikan harga dengan tepat dalam Aktual Projek. Ini bermakna perlulah ada hubungan 1:N dari **Jawatan Standard** kepada **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Entiti Baris Jurnal**.

6. Ulangi langkah 1- 6 untuk mencipta hubungan 1:N dari **Jawatan Standard** kepada **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Entiti Baris Jurnal**.

> ![Menambah Jawatan Standard sebagai medan rujukan untuk Entri Masa](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Sediakan lalai nilai dimensi menggunakan ciri pemetaan platform.
Untuk Entri Masa, ia tentu membantu mempunyai lalai sistem jawatan standard dalam Entri Masa dari Sumber Boleh Ditempah yang merekod entri masa. Gunakan langkah berikut untuk menambah pemetaan medan dalam hubungan 1:N dari **Sumber Boleh Ditempah** kepada **Entri Masa**.

1. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
2. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
3. Klik dua kali **Sumber Boleh Tempah untuk Entri Masa**. Dalam halaman **Hubungan**, pilih **Gunakan pemetaan Medan**. 
4. Pilih **Baharu** untuk mencipta pemetaan medan baharu antara medan **Gelaran Standard** dalam entiti **Sumber Boleh Ditempah** kepada medan rujukan **Gelaran Standard** dalam entiti **Entri Masa**. 

> ![Menyediakan pemetaan medan untuk membolehkan lalai Jawatan Standard daripada Sumber Boleh Ditempah kepada Entri Masa](media/ST-Mapping2.png)

Ini melengkapkan perubahan skema yang diperlukan untuk dimensi tersuai berasaskan entiti.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Tambahn medan tersuai pada borang ,pandangan dan peraturan perniagaan

Selepas anda membuat semua perubahan skema yang diperlukan, langkah seterusnya adalah menjadikan medan boleh dilihat dalam UI dengan menambah medan pada borang dan pandangan.

1. Buka borang atau pandangan. Dalam anak tetingkap navigasi kanan, pilih medan dan seret ke atas kanvas borang. 
2. Jika anda mengedit pandangan, gunakan anak tetingkap navigasi kanan, pilih **Tambah Medan** dan dalam kotak dialog **Penyenaraian medan**, pilih medan yang anda perlukan dan pilih **Ok**.

Jadual berikut memberikan senarai penyeluruh borang dan pandangan luar kotak, mengikut entiti, yang perlu dikemas kini dengan medan baharu. Jika anda ada pandangan atau borang tambahan dalam penyesuaian anda ke atas entiti ini, tambah medan baharu ke atasnya juga.

| EntitI        | Borang yang memerlukan medan baharu   |Pandangan yang memerlukan medan baharu      |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan|• Maklumat |•Harga Kategori Sumber Aktif<br> •Pandangan Berkaitan Harga Kategori Sumber|
|  Tokokan Harga Peranan|• Maklumat|• Tokokan Harga Peranan aktif<br>• Pandangan Berkaitan Tokokan Harga Peranan|
|  Butiran baris sebut harga|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Sebut Harga Aktif<br>• Butiran Baris Sebut Harga Digabungkan<br>• Pandangan Berkaitan Butiran Baris Sebut Harga|
|  Butiran baris Kontrak Projek|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Kontrak Digabungkan<br>• Butiran Baris Kontrak Aktif<br>• Pandangan Butiran Baris Kontrak Berkaitan|
|  Ahli Pasukan Projek|• Maklumat<br>• Borang Baharu|• Ahli Pasukan Projek Aktif<br>• Ahli Pasukan Projek<br>• Pandangan Berkaitan Ahli Pasukan Projek|
|  Entri Masa|• Maklumat<br>• Cipta Entri Masa|• Entri Masa Saya Mengikut Tarikh<br>• Entri Masa Saya untuk minggu ini<br>• Entri masa untuk kelulusan|
|  Garisan Jurnal|• Maklumat<br>• Cipta pantas|• Baris jurnal aktif<br>• Pandangan Berkaitan Barisan Jurnal|
|  Butiran Baris Invois|• Maklumat<br>• Cipta pantas|• Butiran Baris Invois Aktif<br>• Transaksi Invois Boleh Dituntut<br>• Transaksi Invois Percuma<br>• Pandangan Berkaitan Butiran Baris Invois<br>• Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar|• Maklumat<br>• Aktif Sebenar|• Pandangan Berkaitan Aktual|

Medan tersuai juga perlu ditambah dalam peraturan perniagaan bergantung pada apa yang anda telah takrifkan. Satu contoh luar kotak ialah untuk peraturan perniagaan **Keboleheditan Entri Masa berasaskan status**. Peraturan ini mentakrifkan jenis medan yang perlu dikunci apabila Entri Masa berada dalam status tidak boleh diedit seperti **Diluluskan**. Tambah medan pada peraturan perniagaan ini agar medan dikunci untuk pengeditan apabila Entri Masa berada dalam status selain daripada **Draf** atau **Dikembalikan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]