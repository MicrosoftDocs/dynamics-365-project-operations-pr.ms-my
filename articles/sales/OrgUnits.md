---
title: Unit organisasi
description: Topik ini menerangkan konsep unit organisasi, dan menerangkan cara membuat dan mengekalkan unit organisasi di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581387"
---
# <a name="organizational-units-overview"></a>Gambaran keseluruhan unit organisasi

Dalam Microsoft Dynamics 365 Project Operations, *unit organisasi adalah kumpulan* atau bahagian yang berbeza dalam syarikat perkhidmatan profesional yang menggunakan sumber yang boleh dibilkan yang mempunyai kadar kos.

Bagi syarikat perkhidmatan profesional yang menggunakan sumber teknikal dalam bidang amalan yang berbeza atau garis perniagaan, kos untuk mengisi peranan mungkin berbeza-beza, bergantung pada kawasan amalan atau garis perniagaan di mana peranan diisi. Dalam senario ini, konsep unit organisasi membantu dengan menyediakan cara untuk mengumpulkan satu set peranan yang boleh dibilkan dalam pembahagian syarikat yang mempunyai struktur kos yang berbeza untuk peranan tersebut.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Konsep unit organisasi dalam Operasi Projek

Dalam Operasi Projek, unit organisasi mempunyai mata wang tertentu dan senarai harga kos tertentu.

Mata wang unit organisasi ialah mata wang utama yang digunakan untuk menjejak kos.

Satu atau lebih senarai harga kos boleh dilampirkan kepada setiap unit organisasi. Operasi Projek meletakkan had berikut pada senarai harga yang boleh dilampirkan pada unit organisasi:

- Senarai harga mestilah dalam mata wang unit organisasi.
- Senarai harga mestilah senarai harga kos.

Di samping itu, entiti Sumber termasuk atribut untuk unit organisasi. Setiap sumber boleh ditugaskan kepada satu unit organisasi.

### <a name="roles-of-organizational-units"></a>Peranan unit organisasi

Unit organisasi memainkan dua peranan dalam Operasi Projek:

- **Unit kontrak** – Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan. Unit kontrak dikenal pasti oleh medan **Unit kontrak** dalam bahagian pengepala halaman **Peluang**, **Sebut Harga**, **Kontrak Projek** dan **Projek**.
- **Unit Sumber** – Unit organisasi yang mana sumber tergolong dalam atau ditugaskan. Unit organisasi ini boleh menyediakan sumber untuk beberapa peranan mengenai pernyataan kerja (SOWs) dan projek yang dimiliki oleh unit kontrak.

![Unit kontrak dan unit sumber.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Soalan Lazim unit organisasi

Berikut ialah beberapa soalan lazim mengenai unit organisasi.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Bagaimanakah entiti Unit Organisasi dalam Operasi Projek berkaitan dengan entiti Organisasi yang sudah wujud dalam Dynamics 365?

Entiti Organisasi dalam Dynamics 365 mewakili nama contoh Dynamics 365 global. Nama ini biasanya nama perusahaan global.

Entiti Unit Organisasi mewakili kumpulan atau bahagian dalam perusahaan global. Kumpulan atau bahagian ini mempunyai satu set peranan dan senarai harga kos untuk peranan tersebut, dan peranan serta senarai harga berbeza daripada peranan dan senarai harga kumpulan atau bahagian dalam perusahaan.

Apabila Operasi Projek dipasang, unit organisasi lalai dicipta berdasarkan organisasi. Semua sumber sedia ada ditugaskan untuk unit organisasi lalai. Jika mana-mana pengguna atau sumber Active Directory baru diimport ke dalam Dynamics 365, proses import pengguna memperuntukkannya kepada unit organisasi lalai dalam Operasi Projek.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Bagaimanakah entiti Unit Organisasi berbeza daripada entiti Unit Perniagaan?

Dalam Dynamics 365, entiti Unit Perniagaan ialah satu binaan keselamatan. Persatuan pengguna dengan unit perniagaan menentukan entiti dan rekod entiti yang pengguna mempunyai akses. Ia juga menentukan keizinan (Cipta, Baca, Tulis, Padam, Tambah, Tambah Kepada, Tugaskan atau Kongsi) yang pengguna ada untuk rekod entiti tersebut.

Entiti Unit Organisasi mewakili kumpulan syarikat atau bahagian yang mempunyai kadar kos berbeza untuk pekerja yang ditugaskan kepadanya. Persatuan sumber dengan unit organisasi menentukan kos sumber kepada keterlibatan projek.

Apabila anda melaksanakan Dynamics 365, optimumkan pengesahan keselamatan untuk hierarki unit perniagaan dan penugasan pengguna kepada unit perniagaan. Tugaskan semua pengguna yang biasanya mesti mengakses set rekod yang sama kepada unit perniagaan yang sama. Unit organisasi tidak memberi kesan terhadap pemberian kuasa keselamatan atau akses.

**Contoh yang menunjukkan satu perbezaan potensi dalam pemodelan unit organisasi dan unit perniagaan**

Contoso, Ltd. mempunyai amalan teknologi Microsoft yang berkembang maju. Abu Talib dan Nurhafizah adalah kedua-dua pemaju C\#, tetapi Nurhafizah terletak di Amerika Syarikat, manakala Abu Talib berada di India. Sebilangan besar penglibatan projek memerlukan sumber dari Contoso India dan Contoso AS, dan Prakash dan Tricia memerlukan tahap akses keselamatan yang sama ke projek di kawasan latihan ini. Walau bagaimanapun, kos pemaju dari Contoso India berbeza secara ketara daripada kos pemaju dari Contoso AS.

Berikut ialah cara yang optimum untuk mereka bentuk untuk senario ini dengan menggunakan Dynamics 365 dan Project Operations.

1. Cipta amalan teknologi Microsoft sebagai unit perniagaan dan kaitkan Abu Talib dan Nurhafizah dengannya. Dengan cara ini, anda membantu memastikan bahawa kedua-dua pekerja mempunyai tahap akses keselamatan yang sama ke mana-mana projek di kawasan amalan tersebut. Kedua-duanya akan dapat menyemak kemajuan dan melaporkan masa, perbelanjaan, penggunaan bahan dan kemas kini tugas.
2. Buat dua unit organisasi untuk membantu memastikan bahawa kos untuk projek itu dicerminkan dengan betul.
3. Kaitkan Tricia dengan Contoso AS dan Prakash dengan Contoso India.
4. Tugaskan senarai harga kos bersesuaian untuk kedua-dua unit organisasi. Dengan cara ini, anda membantu memastikan bahawa kos yang direkodkan pada projek untuk Prakash dan Tricia dengan tepat mencerminkan perbezaan kos antara Contoso AS dan Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Adakah unit organisasi berkaitan dengan wilayah jualan dalam Dynamics 365?

Tiada persatuan atau perhubungan antara wilayah jualan dan unit organisasi. Wilayah jualan biasanya merupakan kawasan geografi yang mana jualan berlaku. Senarai harga jualan boleh dikaitkan dengan setiap wilayah jualan.

Unit organisasi ialah kumpulan atau bahagian dalaman dalam syarikat yang menjejaki kos untuk sebuah set peranan yang dijual kepada bahagian lain atau pelanggan luar.

**Contoh yang menunjukkan satu perbezaan potensi dalam pemodelan unit organisasi dan wilayah jualan**

Contoso, Ltd. mempunyai dua pusat pembangunan: Contoso AS dan Contoso India. Kos sumber sangat berbeza antara kedua-dua pusat pembangunan ini. Contoso menjual perkhidmatan teknologi maklumat (IT) di banyak pasaran antarabangsa, seperti Amerika Latin, Amerika Utara, Asia-Pasifik, Eropah Barat, dan Timur Tengah. Kadar bil untuk peranan projek yang sama boleh berbeza-beza secara meluas merentasi pasaran ini. Contoso AS dan Contoso India harus ditubuhkan sebagai unit organisasi, dan setiap unit organisasi mesti mempunyai senarai harga kosnya sendiri. Asia Pasifik, Amerika Latin, Amerika Utara, Eropah Barat, dan Timur Tengah hendaklah disediakann sebagai wilayah jualan, dan setiap wilayah jualan perlu mempunyai senarai harga jualan sendiri.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Mengapakah terdapat sekatan terhadap persatuan senarai harga dengan unit organisasi?

Harga jualan biasanya unik untuk kawasan geografi atau pasaran yang perkhidmatan dijual. Bahagian dalaman syarikat selalunya tidak mempunyai harga jualan mereka sendiri untuk jenis perkhidmatan yang sama. Walau bagaimanapun, bahagian dalaman mempunyai kos yang berbeza bagi barangan yang dijual (COGS), bergantung kepada kemahiran pekerja yang mereka ambil dan keadaan buruh rantau tempat mereka beroperasi. Kerana unit organisasi dimodalkan sebagai bahagian dalaman syarikat, mereka boleh mempunyai senarai harga kos.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Mengapa kita tidak boleh mengaitkan senarai harga jualan dengan unit organisasi?

Dalam Operasi Projek, senarai harga jualan boleh dikaitkan dengan pelanggan dan wilayah jualan. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek, dan Projek menggunakan senarai harga jualan yang dilampirkan pada akaun pelanggan atau wilayah jualan untuk menentukan kadar bil dan potensi pendapatan untuk penglibatan projek.

Senarai harga kos dikaitkan dengan unit organisasi. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek, dan senarai harga kos penggunaan Projek yang dilampirkan pada unit kontrak untuk menentukan kos kepada penglibatan projek.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Adakah unit organisasi hierarki dalam Operasi Projek?

Tidak. Dalam keluaran Semasa Operasi Projek, unit organisasi bukan hierarki. Oleh itu, anda tidak boleh melakukan tugas berikut:

- Konfigurasikan corak untuk memasukkan harga kos lalai yang merentasi hierarki.
- Laporkan hasil atau kos yang digulung pada tahap hierarki unit organisasi yang berbeza.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami adalah firma multinasional besar yang mempunyai hierarki pusat kos, bahagian, dan pejabat penagihan yang kompleks dan pelbagai peringkat. Bagaimanakah kita boleh menggunakan konsep unit organisasi dalam versi Operasi Projek semasa?

Apabila anda mempunyai hierarki kompleks pusat kos, bahagian, pejabat pengebilan, dan sebagainya, sediakan nod daun hierarki itu sebagai unit organisasi yang berbeza.

Contoh berikut menunjukkan hierarki biasa.

**Contoso India**

- Amalan SAP

    - Perunding Teknikal
    - Perunding Fungsi

- Amalan Teknologi Microsoft

    - Perunding Teknikal
    - Perunding Fungsi

**Contoso AS**

- Amalan SAP

    - Perunding Teknikal
    - Perunding Fungsi

- Amalan Teknologi Microsoft

    - Perunding Teknikal
    - Perunding Fungsi

Jika hierarki anda menyerupai contoh ini, anda mesti menyediakannya sebagai senarai rata, seperti yang ditunjukkan di sini:

- Contoso India - Amalan SAP - Perunding Teknikal
- Contoso India - Amalan SAP - Perunding Fungsi
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi
- Contoso AS - Amalan SAP - Perunding Teknikal
- Contoso AS - Amalan SAP - Perunding Fungsi
- Contoso AS - Amalan Teknologi Microsoft - Perunding Teknikal
- Contoso AS - Amalan Teknologi Microsoft - Perunding Fungsi

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami adalah sebuah syarikat perkhidmatan profesional kecil yang beroperasi sebagai satu bahagian sahaja. Bagaimanakah kita boleh menggunakan konsep unit organisasi dalam versi Operasi Projek semasa?

Jika syarikat anda beroperasi sebagai satu unit yang mempunyai satu senarai harga kos, anda tidak perlu menyediakan sebarang unit organisasi. Pemasangan Operasi Projek mencipta satu unit organisasi lalai yang mempunyai nama yang sama dengan organisasi. Secara lalai, semua pengguna ditugaskan untuk unit organisasi ini. Apabila sistem memerlukan unit organisasi dipilih, unit organisasi ini dipilih secara lalai.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Apabila projek dicipta daripada sebut harga atau baris kontrak projek, unit kontrak lalai datang daripada kontrak sebut harga atau projek. Apakah unit kontrak lalai jika projek dicipta sebelum entiti jualan seperti Sebut Harga atau Kontrak Projek?

Apabila projek dicipta sendiri, unit kontrak lalai projek ini adalah berdasarkan pengguna yang menciptanya. Pengguna itu juga ialah pengurus projek lalai. Sekiranya projek itu dipetakan kepada entiti penjualan seperti sebut harga atau kontrak projek, unit kontrak projek adalah berdasarkan entiti penjualan. Dalam hal ini, anggaran projek mungkin akan dikira semula kerana senarai harga kos digunakan untuk mengira perubahan anggaran kos jika unit kontrak ditukar. Senarai harga jualan digunakan untuk mengira anggaran jualan yang akan diubah supaya ia selaras dengan senarai harga projek sebut harga.

Unit **Kontrak** dan **medan Mata Wang** projek dikunci untuk penyuntingan, kerana ia mesti selaras dengan nilai entiti jualan (sebut harga atau kontrak projek) yang projek itu dipetakan.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Mencipta dan menyelenggara unit organisasi dalam Operasi Projek

Untuk mencipta unit organisasi dalam Operasi Projek, ikuti langkah ini.

1. Pergi ke **Tetapan \> Unit** Organisasi.
2. Pilih **Baharu**.
3. **Dalam kawasan Umum**, dalam **medan Nama**, masukkan nama untuk unit organisasi. Kemudian tetapkan medan lain seperti yang diperlukan.
4. Pilih **Simpan** untuk mencipta rekod supaya anda boleh terus mengeditnya.
5. Di bawah **Senarai** Harga Kos, pilih tanda tambah (**+**) untuk menambah senarai harga. Anda hanya boleh menambah senarai harga yang mempunyai **konteks Kos** di sini.
6. **Dalam medan Nama**, pilih **butang Carian** dan pilih senarai harga yang anda ingin sediakan kepada unit organisasi. Teruskan menambah senarai harga seperti yang diperlukan.
7. Apabila anda telah selesai menambah senarai harga, pilih **Simpan** di penjuru kanan bawah halaman.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
