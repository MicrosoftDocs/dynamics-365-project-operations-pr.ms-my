---
title: Unit organisasi
description: Artikel ini menghuraikan konsep unit organisasi dan menerangkan cara untuk mencipta dan menyenggara unit organisasi dalam Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921635"
---
# <a name="organizational-units-overview"></a>Gambaran keseluruhan unit organisasi

Dalam Microsoft Dynamics 365 Project Operations, *unit organisasi* ialah kumpulan atau bahagian yang berbeza dalam syarikat perkhidmatan profesional yang menggunakan sumber boleh dibilkan yang mempunyai kadar kos.

Untuk syarikat perkhidmatan profesional yang menggunakan sumber teknikal dalam bidang amalan atau baris perniagaan yang berbeza, kos untuk mengisi peranan mungkin berbeza bergantung pada kawasan amalan atau baris perniagaan tempat peranan diisi. Dalam senario ini, konsep unit organisasi konsep membantu dengan menyediakan cara untuk mengumpulkan set peranan yang boleh dibilkan dalam bahagian syarikat yang mempunyai struktur kos yang berbeza untuk peranan tersebut.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Konsep unit organisasi dalam Project Operations

Dalam Project Operations, unit organisasi mempunyai mata wang yang tertentu dan senarai harga kos tertentu.

Mata wang unit organisasi ialah mata wang utama yang digunakan untuk menjejak kos.

Satu atau lebih senarai harga kos boleh dilampirkan kepada setiap unit organisasi. Project Operations meletakkan had berikut pada senarai harga yang boleh dilampirkan pada unit organisasi:

- Senarai harga hendaklah dalam mata wang unit organisasi.
- Senarai harga mestilah senarai harga kos.

Di samping itu, entiti sumber merangkumi atribut untuk unit organisasi. Setiap sumber boleh ditugaskan kepada satu unit organisasi.

### <a name="roles-of-organizational-units"></a>Peranan unit organisasi

Unit organisasi memainkan dua peranan dalam Project Operations:

- **Unit kontrak** – Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan. Unit kontrak dikenal pasti oleh medan **Unit kontrak** dalam bahagian pengepala halaman **Peluang**, **Sebut Harga**, **Kontrak Projek** dan **Projek**.
- **Unit Sumber** – Unit organisasi yang mana sumber tergolong dalam atau ditugaskan. Unit organisasi ini boleh menyediakan sumber untuk beberapa peranan mengenai pernyataan kerja (SOWs) dan projek yang dimiliki oleh unit kontrak.

![Unit kontrak dan unit sumber.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Soalan lazim unit organisasi

Berikut ialah beberapa soalan lazim mengenai unit organisasi.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Bagaimanakah entiti Unit Organisasi dalam Project Operations berkaitan dengan entiti Organisasi yang sudah wujud dalam Dynamics 365?

Entiti Organisasi dalam Dynamics 365 mewakili nama tika Dynamics 365 global. Nama ini biasanya nama perusahaan global.

Entiti Unit Organisasi mewakili kumpulan atau bahagian dalam perusahaan global. Kumpulan atau bahagian ini mempunyai satu set peranan dan senarai harga kos untuk peranan tersebut, dan peranan serta senarai harga berbeza daripada peranan dan senarai harga kumpulan atau bahagian dalam perusahaan.

Apabila Project Operations dipasang, unit organisasi lalai dicipta berdasarkan organisasi. Semua sumber sedia ada ditugaskan untuk unit organisasi lalai. Jika mana-mana pengguna atau sumber Active Directory baharu diimport ke dalam Dynamics 365, proses import pengguna menguntukkan mereka kepada unit organisasi lalai dalam Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Bagaimanakah entiti Unit Organisasi berbeza daripada entiti Unit Perniagaan?

Dalam Dynamics 365, entiti Unit Perniagaan ialah satu binaan keselamatan. Persatuan pengguna dengan unit perniagaan menentukan entiti dan rekod entiti yang pengguna mempunyai akses. Ia juga menentukan keizinan (Cipta, Baca, Tulis, Padam, Tambah, Tambah Kepada, Tugaskan atau Kongsi) yang pengguna ada untuk rekod entiti tersebut.

Entiti Unit Organisasi mewakili kumpulan syarikat atau bahagian yang mempunyai kadar kos berbeza untuk pekerja yang ditugaskan kepadanya. Persatuan sumber dengan unit organisasi menentukan kos sumber kepada keterlibatan projek.

Apabila anda melaksanakan Dynamics 365, optimumkan pengesahan keselamatan untuk hierarki unit perniagaan dan penugasan pengguna kepada unit perniagaan. Tugaskan semua pengguna yang biasanya mesti mengakses set rekod yang sama kepada unit perniagaan yang sama. Unit organisasi tidak memberi kesan terhadap pemberian kuasa keselamatan atau akses.

**Contoh yang menunjukkan satu perbezaan yang berpotensi dalam pemodelan unit organisasi dan unit perniagaan**

Contoso, Ltd. mempunyai amalan teknologi Microsoft yang berkembang maju. Abu Talib dan Nurhafizah adalah kedua-dua pemaju C\#, tetapi Nurhafizah terletak di Amerika Syarikat, manakala Abu Talib berada di India. Kebanyakan penglibatan projek memerlukan sumber daripada kedua-dua Contoso India dan Contoso AS, dan Abu Talib dan Nurhafizah memerlukan tahap akses keselamatan yang sama untuk projek dalam kawasan amalan ini. Walau bagaimanapun, kos pemaju dari Contoso India berbeza secara ketara daripada kos pemaju dari Contoso AS.

Berikut ialah cara optimum untuk mereka bentuk bagi senario ini menggunakan Dynamics 365 dan Project Operations.

1. Cipta amalan teknologi Microsoft sebagai unit perniagaan dan kaitkan Abu Talib dan Nurhafizah dengannya. Dengan cara ini, anda membantu dalam memastikan bahawa kedua-dua pekerja mempunyai tahap akses keselamatan yang sama kepada mana-mana projek dalam kawasan amalan tersebut. Mereka berdua akan dapat menyemak kemajuan dan masa laporan, perbelanjaan, penggunaan bahan dan kemas kini tugas.
2. Cipta dua unit organisasi untuk membantu dalam memastikan bahawa kos untuk projek tersebut ditunjukkan dengan betul.
3. Kaitkan Nurhafizah dengan Contoso AS dan Abu Talib dengan Contoso India.
4. Tugaskan senarai harga kos bersesuaian untuk kedua-dua unit organisasi. Dengan cara ini, anda membantu dalam memastikan bahawa kos yang direkodkan pada projek untuk Abu Talib dan Nurhafizah menunjukkan perbezaan dalam kos antara Contoso AS dan Contoso India dengan tepat.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Adakah unit organisasi berkaitan dengan wilayah jualan dalam Dynamics 365?

Tiada persatuan atau perhubungan antara wilayah jualan dan unit organisasi. Wilayah jualan biasanya merupakan kawasan geografi yang mana jualan berlaku. Senarai harga jualan boleh dikaitkan dengan setiap wilayah jualan.

Unit organisasi ialah kumpulan atau bahagian dalaman dalam syarikat yang menjejaki kos untuk sebuah set peranan yang dijual kepada bahagian lain atau pelanggan luar.

**Contoh yang menunjukkan satu perbezaan yang berpotensi dalam pemodelan unit organisasi dan wilayah jualan**

Contoso, Ltd. mempunyai dua pusat pembangunan: Contoso AS dan Contoso India. Kos sumber amat berbeza antara kedua-dua pusat pembangunan ini. Contoso menjual perkhidmatan teknologi maklumat (IT) dalam banyak pasaran antarabangsa, seperti Amerika Latin, Amerika Utara, Asia Pasifik, Eropah Barat dan Timur Tengah. Kadar bil untuk peranan projek yang sama boleh berbeza-beza secara meluas merentasi pasaran ini. Contoso AS dan Contoso India harus ditubuhkan sebagai unit organisasi, dan setiap unit organisasi mesti mempunyai senarai harga kosnya sendiri. Asia Pasifik, Amerika Latin, Amerika Utara, Eropah Barat, dan Timur Tengah hendaklah disediakann sebagai wilayah jualan, dan setiap wilayah jualan perlu mempunyai senarai harga jualan sendiri.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Mengapakah terdapat sekatan terhadap persatuan senarai harga dengan unit organisasi?

Harga jualan biasanya unik untuk kawasan geografi atau pasaran yang perkhidmatan dijual. Bahagian dalaman syarikat selalunya tidak mempunyai harga jualan mereka sendiri untuk jenis perkhidmatan yang sama. Walau bagaimanapun, bahagian dalaman mempunyai kos yang berbeza bagi barangan yang dijual (COGS), bergantung kepada kemahiran pekerja yang mereka ambil dan keadaan buruh rantau tempat mereka beroperasi. Kerana unit organisasi dimodalkan sebagai bahagian dalaman syarikat, mereka boleh mempunyai senarai harga kos.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Mengapakah kita tidak dapat mengaitkan senarai harga jualan dengan unit organisasi?

Dalam Project Operations, senarai harga jualan boleh dikaitkan dengan pelanggan dan wilayah jualan. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek, dan Projek menggunakan senarai harga jualan yang dilampirkan kepada akaun pelanggan atau wilayah jualan bagi menentukan kadar bil dan potensi pendapatan untuk penglibatan projek.

Senarai harga kos dikaitkan dengan unit organisasi. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek dan Projek menggunakan senarai harga kos yang dilampirkan kepada unit kontrak untuk menentukan kos kepada penglibatan projek.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Adakah unit organisasi berhierarki dalam Project Operations?

Tidak. Dalam keluaran semasa Project Operations, unit organisasi tidak berhierarki. Oleh itu, anda tidak boleh melaksanakan tugas berikut:

- Mengkonfigurasi corak untuk memasukkan harga kos lalai yang melintasi hierarki.
- Melaporkan pendapatan atau kos yang digulung balik pada peringkat berbeza hierarki unit organisasi.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami sebuah syarikat multinasional besar yang mempunyai hierarki berbilang tahap yang rumit bagi pusat kos, bahagian dan pejabat pengebilan. Bagaimanakah cara terbaik kami menggunakan konsep unit organisasi dalam versi semasa Project Operations?

Apabila anda mempunyai hierarki rumit bagi pusat kos, bahagian, pejabat pengebilan dan sebagainya, tetapkan nod daun bagi hierarki itu sebagai unit organisasi berbeza.

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

Jika hierarki anda menyerupai contoh ini, anda mesti menetapkannya sebagai senarai rata, seperti yang ditunjukkan di sini:

- Contoso India - Amalan SAP - Perunding Teknikal
- Contoso India - Amalan SAP - Perunding Fungsi
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi
- Contoso AS - Amalan SAP - Perunding Teknikal
- Contoso AS - Amalan SAP - Perunding Fungsi
- Contoso AS - Amalan Teknologi Microsoft - Perunding Teknikal
- Contoso AS - Amalan Teknologi Microsoft - Perunding Fungsi

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Kami adalah sebuah syarikat perkhidmatan profesional kecil yang beroperasi sebagai satu bahagian sahaja. Bagaimanakah cara terbaik kami menggunakan konsep unit organisasi dalam versi semasa Project Operations?

Jika syarikat anda beroperasi sebagai satu unit yang mempunyai satu senarai harga kos, anda tidak perlu menyediakan sebarang unit organisasi. Pemasangan Project Operations mewujudkan satu unit organisasi lalai yang mempunyai nama yang sama dengan organisasi. Secara lalai, semua pengguna ditugaskan untuk unit organisasi ini. Apabila sistem memerlukan unit organisasi dipilih, unit organisasi ini dipilih secara lalai.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Apabila projek dicipta daripada sebut harga atau baris kontrak projek, unit kontrak lalai datang daripada kontrak sebut harga atau projek. Apakah unit kontrak lalai jika projek dicipta sebelum entiti jualan seperti Sebut Harga atau Kontrak Projek?

Apabila projek dicipta sendiri, unit kontrak lalai projek ini adalah berdasarkan pengguna yang menciptanya. Pengguna itu juga ialah pengurus projek lalai. Jika projek dipetakan kepada entiti jualan seperti sebut harga atau kontrak projek, unit kontrak bagi projek adalah berdasarkan kepada entiti jualan. Dalam hal ini, anggaran projek mungkin akan dikira semula kerana senarai harga kos digunakan untuk mengira perubahan anggaran kos jika unit kontrak ditukar. Senarai harga jualan digunakan untuk mengira anggaran jualan yang akan ditukar supaya ia disegerakkan dengan senarai harga projek bagi sebut harga.

Medan **Unit Kontrak** dan **Mata Wang** bagi projek dikunci untuk edit kerana ia mesti segerak dengan nilai bagi entiti jualan (sebut harga atau kontrak projek) yang projek tersebut dipetakan.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Cipta dan selenggara unit organisasi dalam Project Operations

Untuk mencipta unit organisasi dalam Project Operations, ikut langkah ini.

1. Pergi ke **Tetapan \> Unit Organisasi**.
2. Pilih **Baharu**.
3. Dalam kawasan **Umum**, dalam medan **Nama**, masukkan nama untuk unit organisasi. Kemudian tetapkan medan lain seperti yang diperlukan.
4. Pilih **Simpan** untuk mencipta rekod supaya anda boleh terus mengeditnya.
5. Di bawah **Senarai Harga Kos**, pilih tanda tambah (**+**) untuk menambah senarai harga. Anda hanya boleh menambah senarai harga yang mempunyai konteks **Kos** di sini.
6. Di dalam **Medan nama**, pilih butang **Carian** dan pilih senarai harga yang anda mahu jadikan tersedia kepada unit organisasi. Teruskan menambah senarai harga seperti yang diperlukan.
7. Apabila anda selesai menambah senarai harga, pilih **Simpan** di sudut kanan bawah halaman.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
