---
title: Tambah medan tersuai untuk persediaan harga dan entiti transaksi
description: Topik ini memberikan maklumat tentang menambah medan tersuai untuk persediaan harga dan entiti transaksi.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3ca48b8d5d55b1b2178f9bd84e19d9599f057aa296a728cca57577c18fdaf307
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985782"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Tambah medan tersuai untuk persediaan harga dan entiti transaksi 

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini menganggap bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai](create-custom-fields-entities.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini. 

Dalam topik ini, prosedur akan menunjukkan anda cara menambah medan tersuai diperlukan yang merujuk kepada entiti dan kepada unsur antara muka pengguna (UI) seperti borang dan pandangan.

## <a name="add-custom-pricing-dimension-fields"></a>Tambah medan dimensi penentuan harga tersuai 
Selepas medan dan entiti tersuai dicipta, langkah seterusnya ialah untuk membuat persediaan harga dan entiti yang maklum dengan entiti tersuai atau set pilihan dengan mencipta medan keutamaan. Bergantung pada sama ada senarai dimensi penentuan harga anda memasukkan dimensi set pilihan atau dimensi entiti atau kedua-duanya, ikuti hanya langkah dalam **Dimensi penentuan harga tersuai berasaskan set pilihan** atau **Dimensi penentuan harga tersuai berasaskan entiti**, atau kedua-duanya, masing-masing.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensi penentuan harga tersuai berasaskan set pilihan
Apabila dimensi penentuan harga tersuai adalah berasaskan set pilihan, tambah ia sebagai medan pada entiti Project Service utama. Dalam prosedur berikut, **Lokasi Kerja Sumber** dan **Waktu Bekerja Sumber** digunakan sebagai dimensi penentuan harga berasaskan set pilihan. Ini mestilah terlebih dahulu ditambah sebagai medan untuk entiti penentuan harga, **Harga Peranan** dan **Tokokan Harga Peranan**.

1. Dalam Project Service Automation (PSA), klik **Tetapan** > **Penyelesaian**, kemudian klik dua kali dimensi penentuan harga **\<your organization name>**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Harga Peranan**.
3. Kembangkan entiti **Harga Peranan** dan pilih **Medan**.
4. Klik **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih **Set Pilihan** sebagai jenis medan. 
5. Pilih **Guna set pilihan sedia ada**, pilih set pilihan **Lokasi Kerja Sumber**, kemudian klik **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan pada entiti **Tokokan Harga Peranan**. 
7. Ulangi langkah 1 - 5 untuk set pilihan **Waktu Bekerja Sumber**.

> [!IMPORTANT]
> Apabila anda menambah medan kepada lebih daripada satu entiti, guna nama medan sama dalam semua entiti. 

> ![Menambah Lokasi Kerja Sumber pada Harga Peranan.](media/RWL-Field.png)

Dalam jualan dan fasa anggaran untuk projek, anggaran untuk usaha kerja yang diperlukan untuk melengkapkan kerja **Tempatan** dan **Di Tapak**, dalam **Jam biasa** dan **Jam lebih masa**  digunakan untuk menganggarkan nilai Sebut Harga/Projek Medan **Lokasi Kerja Sumber** dan **Waktu Kerja Sumber** akan ditambah pada entiti anggaran, **Butiran Baris Sebut Harga**, **Butiran Baris Kontrak**, **Tugas Projek**, **Ahli Pasukan Projek**, dan **Baris Anggaran**.

1. Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Butiran Baris Sebut Harga**.
3. Kembangkan entiti **Butiran Baris Sebut Harga** dan pilih **Medan**.
4. Klik **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih jenis medan **Set Pilihan**. 
5. Pilih **Guna set pilihan sedia ada**, dan **Lokasi Kerja Sumber**, kemudian klik **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan ini pada entiti **Butiran Baris Kontrak Projek**,**Tugas Projek**, **Ahli Pasukan Projek**, dan **Baris Anggaran**.
7. Ulangi langkah 1 - 6 untuk set pilihan **Waktu Bekerja Sumber**. 

> ![Menambah Lokasi Kerja Sumber pada Baris Anggaran.](media/RWL-Default-Value.png)


Untuk penghantaran dan pengivoisan, kerja yang telah selesai perlukan diberikan harga dengan tepat untuk memilih sama ada ia dijalankan secara **Tempatan** atau **Di Tapak**, dan sama ada ia dilengkapkan semasa **Jam biasa** atau **lebih masa** dalam Aktual Projek. Medan **Lokasi Kerja Sumber** dan **Jam Kerja Sumber** hendaklah ditambah pada entiti **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Baris Jurnal**.

1. Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**.
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Entri Masa**.
3. Kembangkan entiti **Butiran Baris Sebut Harga** dan pilih **Medan**.
4. Klik **Baharu** untuk mencipta medan baharu dipanggil **Lokasi Kerja Sumber** dan pilih **Set Pilihan** sebagai jenis medan. 
5. Pilih **Guna set pilihan sedia ada**, pilih set pilihan **Lokasi Kerja Sumber**, kemudian klik **Simpan**.
6. Ulangi langkah 1 - 5 untuk menambah medan pada entiti **Aktual**, **Butiran Baris Invois**, dan **Baris Jurnal**.
7. Ulangi langkah 1 - 6 untuk set pilihan **Waktu Bekerja Sumber**. 

> ![Menambah Lokasi Kerja Sumber pada Entri Masa.](media/RWL-time-entry.png)

Ini melengkapkan perubahan skema yang diperlukan untuk dimensi tersuai berasaskan pilihan.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensi penentuan harga tersuai berasaskan entiti

Apabila dimensi penentuan harga tersuai adalah entiti, anda akan menambah Hubungan 1:N antara entiti dimensi dan entiti Project Service utama. Menggunakan contoh Jawatan Standard dari atas, adalah munasabah untuk menjangkakan setiap pekerja ditugaskan jawatan standard. Hasilnya, anda perlu hubungan 1:N daripada Jawatan Standard untuk Sumber Boleh Ditempah, atau hubungan N:1 jika ia dicipta daripada Sumber Boleh Ditempah untuk Jawatan Standard.

1. Dalam PSA, klik **Tetapan** > **Penyelesaian** dan kemudian klik dua kali dimensi penetapan harga **\<your organization name>**. 
2. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
3. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
4. Klik **Baharu** untuk mencipta hubungan 1:N baharu yang dipanggil **Jawatan Standard untuk Sumber Boleh Ditempah**. Masukkan maklumat diperlukan, kemudian klik **Simpan**.

> ![Menambah Jawatan Standard sebagai medan rujukan kepada Sumber Boleh Ditempah.](media/ST-BR.png)

Jawatan Standard juga perlu ditambah pada entiti Penentuan Harga Project Service, **Harga Peranan** dan **Tokokan Harga Peranan**. Ini juga dilengkapkan menggunakan hubungan 1:N antaran entiti **Jawatan Standard** dan **Harga Peranan** dan entiti **Jawatan Standard** dan **Tokokan Harga Peranan**.

1. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
2. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
3. Klik **Baharu** untuk mencipta hubungan 1:N baharu yang dipanggil **Jawatan Standard untuk Harga Peranan**. Masukkan maklumat diperlukan, kemudian klik **Simpan**.
4. Ulangi langkah 1 - 4 untuk mencipta hubungan 1:N antara entiti **Jawatan Standard** dan **Tokokan Harga Peranan**,

Dalam jualan dan fasa anggaran untuk projek, untuk memberikan harga bagi Sebut Harga/Projek, anggaran usaha kerja diperlukan untuk setiap jawatan standard. Ini bermakna hubungan 1:N daripada Jawatan Standard untuk setiap entiti anggaran ini dalam Project Service diperlukan: 

- **Butiran Baris Sebut Harga**
- **Butiran Baris Kontrak Projek**
- **Tugas Projek**
- **Ahli Pasukan Projek**
- **Garisan Anggaran**

5. Ulangi langkah 1 - 5 untuk mencipta hubungan 1:N daripada **Tajuk Standard** kepada **Butiran Baris Sebut Harga**, **Butiran Baris Kontrak Projek**, **Tugas Projek**, **Ahli Pasukan Projek**, dan **Baris Anggaran**.

> ![Menambah Jawatan Standard sebagai medan rujukan kepada Baris Anggaran.](media/ST-Estimate-Line.png)

Dalam fasa Penghantaran dan Penginvoisan, kerja yang selesai oleh setiap jawatan standard mestilah diberikan harga dengan tepat dalam Aktual Projek. Ini bermakna perlulah ada hubungan 1:N dari **Jawatan Standard** kepada **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Entiti Baris Jurnal**.

6. Ulangi langkah 1- 6 untuk mencipta hubungan 1:N dari **Jawatan Standard** kepada **Entri Masa**, **Aktual**, **Butiran Baris Invois**, dan **Entiti Baris Jurnal**.

> ![Menambah Jawatan Standard sebagai medan rujukan kepada Entri Masa.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Sediakan lalai nilai dimensi menggunakan ciri pemetaan platform.
Untuk Entri Masa, ia tentu membantu mempunyai lalai sistem jawatan standard dalam Entri Masa dari Sumber Boleh Ditempah yang merekod entri masa. Gunakan langkah berikut untuk menambah pemetaan medan dalam hubungan 1:N dari **Sumber Boleh Ditempah** kepada **Entri Masa**.

1. Dalam Solution Explorer, pada anak tetingkap navigasi kiri, pilih **Entiti > Jawatan Standard**.
2. Kembangkan entiti **Jawatan Standard** dan pilih **Hubungan 1:N**.
3. Klik dua kali **Sumber Boleh Tempah untuk Entri Masa**. Dalam halaman **Hubungan**, klik **Guna pemetaan Medan**. 
4. Klik **Baharu** untuk mencipta pemetaan medan baharu antara medan **Jawatan Standard** dalam entiti **Sumber Boleh Ditempah** kepada medan rujukan **Jawatan Standard** dalam entiti **Entri Masa**. 

> ![Menyediakan pemetaan medan untuk membolehkan penetapan lalai Jawatan Standard daripada Sumber Boleh Ditempah kepada Entri Masa.](media/ST-Mapping2.png)


Ini melengkapkan perubahan skema yang diperlukan untuk dimensi tersuai berasaskan entiti.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Tambahn medan tersuai pada borang ,pandangan dan peraturan perniagaan

Selepas anda membuat semua perubahan skema yang diperlukan, langkah seterusnya adalah menjadikan medan boleh dilihat dalam UI dengan menambah medan pada borang dan pandangan.

1. Buka borang atau pandangan. Dalam anak tetingkap navigasi kanan, pilih medan dan seret ke atas kanvas borang. 
2. Jika anda mengedit pandangan, guna anak tetingkap navigasi kanan, klik **Tambah Medan**, dan dalam kotak dialog **Penyenaraian Medan**, pilih medan yang anda perlukan dan klik **Ok**.

Jadual berikut memberikan senarai penyeluruh borang dan pandangan luar kotak, mengikut entiti, yang perlu dikemas kini dengan medan baharu. Jika anda ada pandangan atau borang tambahan dalam penyesuaian anda ke atas entiti ini, tambah medan baharu ke atasnya juga.

| Entiti Project Service        | Borang yang memerlukan medan baharu   |Pandangan yang memerlukan medan baharu      |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peranan|• Maklumat |•Harga Kategori Sumber Aktif<br> •Pandangan Berkaitan Harga Kategori Sumber|
|  Tokokan Harga Peranan|• Maklumat|• Tokokan Harga Peranan aktif<br>• Pandangan Berkaitan Tokokan Harga Peranan|
|  Butiran baris sebut harga|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Sebut Harga Aktif<br>• Butiran Baris Sebut Harga Digabungkan<br>• Pandangan Berkaitan Butiran Baris Sebut Harga|
|  Butiran baris Kontrak Projek|• Maklumat Projek<br>• Cipta Cepat Projek|• Butiran Baris Kontrak Digabungkan<br>• Butiran Baris Kontrak Aktif<br>• Pandangan Butiran Baris Kontrak Berkaitan|
|  Tugas Projek|•Maklumat<br>• Borang Baharu||
|  Ahli Pasukan Projek|•Maklumat<br>• Borang Baharu|• Ahli Pasukan Projek Aktif<br>• Ahli Pasukan Projek<br>• Pandangan Berkaitan Ahli Pasukan Projek|
|  Entri Masa|• Maklumat<br>• Cipta Entri Masa|• Entri Masa Saya Mengikut Tarikh<br>• Entri Masa Saya untuk minggu ini<br>• Entri masa untuk kelulusan|
|  Garisan Jurnal|• Maklumat<br>• Cipta pantas|• Baris jurnal aktif<br>• Pandangan Berkaitan Barisan Jurnal|
|  Butiran Baris Invois|• Maklumat<br>• Cipta pantas|• Butiran Baris Invois Aktif<br>• Transaksi Invois Boleh Dituntut<br>• Transaksi Invois Percuma<br>• Pandangan Berkaitan Butiran Baris Invois<br>• Transaksi Invois Tidak Boleh Dituntut|
|  Sebenar|• Maklumat<br>• Aktif Sebenar|• Pandangan Berkaitan Aktual|

Medan tersuai juga perlu ditambah dalam peraturan perniagaan bergantung pada apa yang anda telah takrifkan. Satu contoh luar kotak ialah untuk peraturan perniagaan **Keboleheditan Entri Masa berasaskan status**. Peraturan ini mentakrifkan jenis medan yang perlu dikunci apabila Entri Masa berada dalam status tidak boleh diedit seperti **Diluluskan**. Tambah medan pada peraturan perniagaan ini agar medan dikunci untuk pengeditan apabila Entri Masa berada dalam status selain daripada **Draf** atau **Dikembalikan**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]