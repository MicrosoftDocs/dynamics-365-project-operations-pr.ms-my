---
title: Unit organisasi
description: Topik ini menyediakan maklumat mengenai unit organisasi dalam Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 755eee6ab9993c72ff1db46e0993527ac0826bfe
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130634"
---
# <a name="organizational-units"></a>Unit organisasi 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, unit organisasi ialah kumpulan atau bahagian yang berbeza dalam syarikat perkhidmatan profesional yang menggunakan sumber boleh dibilkan yang mempunyai kadar kos.

Untuk syarikat perkhidmatan profesional yang menggunakan sumber teknikal dalam pelbagai bidang amalan atau baris perniagaan, kos untuk mengisi peranan dalam satu kawasan amalan atau baris perniagaan mungkin berbeza daripada kos untuk mengisi peranan dalam kawasan amalan atau baris perniagaan lain. Unit organisasi konsep membantu dalam senario ini dengan menyediakan cara untuk mengumpulkan peranan yang boleh dibilkan dalam bahagian syarikat yang mempunyai struktur kos yang berbeza untuk peranan ini.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Atribut utama dan Ppersatuan unit organisasi

Dalam PSA, unit organisasi dalam PSA mempunyai mata wang yang tertentu dan senarai harga kos tertentu.

Mata wang unit organisasi ialah mata wang utama yang digunakan untuk menjejak kos.

Satu atau lebih senarai harga kos boleh dilampirkan kepada setiap unit organisasi. PSA meletakkan had berikut pada senarai harga yang boleh dilampirkan oleh unit organisasi:

- Senarai harga hendaklah dalam mata wang unit organisasi
- Senarai harga mestilag senarai harga kos

Di samping itu, terdapat atribut untuk unit organisasi pada entiti Sumber. Setiap sumber boleh ditugaskan kepada satu unit organisasi.

## <a name="roles-of-organizational-units"></a>Peranan unit organisasi

Unit organisasi memainkan dua peranan dalam PSA:

- **Unit kontrak** – Unit organisasi yang mewakili kumpulan atau bahagian syarikat yang bertanggungjawab terutamanya untuk memenangi jualan dan menguruskan penyampaian kerja dan perkhidmatan kepada pelanggan. Unit kontrak dikenal pasti oleh medan **Unit kontrak** dalam bahagian pengepala halaman **Peluang**, **Sebut Harga**, **Kontrak Projek** dan **Projek**.
- **Unit Sumber** – Unit organisasi yang mana sumber tergolong dalam atau ditugaskan. Unit organisasi ini boleh menyediakan sumber untuk beberapa peranan mengenai pernyataan kerja (SOWs) dan projek yang dimiliki oleh unit kontrak.

> ![Unit kontrak dan unit sumber](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Soalan lazim unit organisasi

Berikut ialah beberapa soalan lazim mengenai unit organisasi.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Bagaimanakah entiti Unit Organisasi dalam PSA berkaitan dengan entiti Organisasi yang sudah wujud dalam Dynamics 365?

Entiti Organisasi dalam Microsoft Dynamics 365 mewakili nama tika Dynamics 365 global. Nama ini biasanya nama perusahaan global.

Entiti Unit Organisasi mewakili kumpulan atau bahagian dalam perusahaan global. Kumpulan atau bahagian ini mempunyai satu set peranan dan senarai harga kos untuk peranan tersebut, dan peranan serta senarai harga berbeza daripada peranan dan senarai harga kumpulan atau bahagian dalam perusahaan.

Apabila PSA dipasang, unit organisasi lalai berdasarkan organisasi. Semua sumber sedia ada ditugaskan untuk unit organisasi lalai. Jika mana-mana pengguna atau sumber Active Directory baharu diimport ke dalam Dynamics 365, proses import pengguna menguntukkan mereka kepada unit organisasi lalai dalam PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Bagaimanakah entiti unit organisasi berbeza daripada entiti unit perniagaan?

Dalam Dynamics 365, entiti Unit Perniagaan ialah satu binaan keselamatan. Persatuan pengguna dengan unit perniagaan menentukan entiti dan rekod entiti yang pengguna mempunyai akses. Ia juga menentukan keizinan (Cipta, Baca, Tulis, Padam, Tambah, Tambah Kepada, Tugaskan atau Kongsi) yang pengguna ada untuk rekod entiti tersebut.

Entiti Unit Organisasi mewakili kumpulan syarikat atau bahagian yang mempunyai kadar kos berbeza untuk pekerja yang ditugaskan kepadanya. Persatuan sumber dengan unit organisasi menentukan kos sumber kepada keterlibatan projek.

Apabila anda melaksanakan Dynamics 365, optimumkan pengesahan keselamatan untuk hierarki unit perniagaan dan penugasan pengguna kepada unit perniagaan. Tugaskan semua pengguna yang biasanya mesti mengakses set rekod yang sama kepada unit perniagaan yang sama. Unit organisasi tidak memberi kesan terhadap pemberian kuasa keselamatan atau akses.

#### <a name="example-of-organizational-units-and-business-units"></a>Contoh unit organisasi dan unit perniagaan

Contoso, Ltd. mempunyai amalan teknologi Microsoft yang berkembang maju. Abu Talib dan Nurhafizah adalah kedua-dua pemaju C\#, tetapi Nurhafizah terletak di Amerika Syarikat, manakala Abu Talib berada di India. Kebanyakan penglibatan projek memerlukan sumber daripada Contoso India dan Contoso AS, dan Abu Talib dan Nurhafizah memerlukan tahap akses keselamatan yang sama untuk projek dalam kawasan amalan ini. Walau bagaimanapun, kos pemaju dari Contoso India berbeza secara ketara daripada kos pemaju dari Contoso AS.

Berikut adalah cara optimum untuk mereka bentuk bagi senario ini menggunakan Dynamics 365 dan PSA.

1. Cipta amalan teknologi Microsoft sebagai unit perniagaan dan kaitkan Abu Talib dan Nurhafizah dengannya. Dengan cara ini, anda membantu menjamin bahawa kedua-dua pekerja mempunyai tahap akses keselamatan yang sama kepada mana-mana projek dalam kawasan amalan tersebut. Mereka berdua akan dapat menyemak kemajuan dan masa laporan, perbelanjaan, dan kemas kini tugas. 
2. Cipta dua unit organisasi untuk membantu menjamin bahawa kos untuk projek tersebut ditunjukkan dengan betul. 
3. Kaitkan Nurhafizah dengan Contoso AS dan kaitkan Abu Talib dengan Contoso India.
4. Tugaskan senarai harga kos bersesuaian untuk kedua-dua unit organisasi. Dengan cara ini, anda membantu menjamin bahawa kos yang direkodkan pada projek untuk Abu Talib dan Nurhafizah menunjukkan perbezaan dalam kos antara Contoso AS dan Contoso India dengan tepat.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Adakah unit organisasi berkaitan dengan wilayah jualan dalam Dynamics 365?

Tiada persatuan atau perhubungan antara wilayah jualan dan unit organisasi. Wilayah jualan biasanya merupakan kawasan geografi yang mana jualan berlaku. Senarai harga jualan boleh dikaitkan dengan setiap wilayah jualan.

Unit organisasi ialah kumpulan atau bahagian dalaman dalam syarikat yang menjejaki kos untuk sebuah set peranan yang dijual kepada bahagian lain atau pelanggan luar.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Contoh unit organisasi dan wilayah jualan

Contoso, Ltd. mempunyai dua pusat pembangunan: Contoso AS dan Contoso India. Kos sumber amat berbeza antara kedua-dua pusat pembangunan ini.

Contoso menjual perkhidmatan IT dalam banyak pasaran antarabangsa, seperti Amerika Latin, Amerika Utara, Asia Pasifik, Eropah Barat dan Timur Tengah. Kadar bil untuk peranan projek yang sama boleh berbeza-beza secara meluas merentasi pasaran ini.

Contoso AS dan Contoso India harus ditubuhkan sebagai unit organisasi, dan setiap unit organisasi mesti mempunyai senarai harga kosnya sendiri. Asia Pasifik, Amerika Latin, Amerika Utara, Eropah Barat, dan Timur Tengah hendaklah disediakann sebagai wilayah jualan, dan setiap wilayah jualan perlu mempunyai senarai harga jualan sendiri.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Mengapakah terdapat sekatan terhadap persatuan senarai harga dengan unit organisasi? 

Harga jualan biasanya unik untuk kawasan geografi atau pasaran yang perkhidmatan dijual. Bahagian dalaman syarikat selalunya tidak mempunyai harga jualan mereka sendiri untuk jenis perkhidmatan yang sama. Walau bagaimanapun, bahagian dalaman mempunyai kos yang berbeza bagi barangan yang dijual (COGS), bergantung kepada kemahiran pekerja yang mereka ambil dan keadaan buruh rantau tempat mereka beroperasi. Kerana unit organisasi dimodalkan sebagai bahagian dalaman syarikat, mereka boleh mempunyai senarai harga kos.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Mengapakah kita tidak dapat mengaitkan senarai harga jualan kepada unit organisasi?

Dalam PSA, senarai harga jualan boleh dikaitkan dengan pelanggan dan wilayah jualan. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek, dan Projek menggunakan senarai harga jualan yang dilampirkan kepada akaun pelanggan atau wilayah jualan bagi menentukan kadar bil dan potensi pendapatan pada penglibatan projek.

Senarai harga kos dikaitkan dengan unit organisasi. Entiti transaksi seperti Peluang, Sebut Harga, Kontrak Projek dan Projek menggunakan senarai harga kos yang dilampirkan kepada unit kontrak untuk menentukan kos kepada penglibatan projek.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Adakah unit organisasi berhierarki dalam PSA?

Tidak. Dalam keluaran semasa PSA, unit organisasi tidak berhierarki. Ini bermaksud anda tidak boleh:

- Konfigurasikan corak untuk harga kos lalai yang melintasi hierarki. 
- Melaporkan pendapatan atau kos gulung atas pada peringkat berbeza hierarki unit organisasi.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Kami sebuah syarikat multinasional besar dengan hierarki berbilang yang rumit bagi pusat kos, bahagian dan pejabat pengebilan. Bagaimanakah cara kami membuat penggunaan terbaik konsep unit organisasi dalam versi aplikasi Project Service?

Apabila anda mempunyai hierarki ruimit bagi pusat kos, bahagian, pejabat pengebilan, dan lain-lain, menetapkan nod daun bagi hierarki itu sebagai unit organisasi berbeza.
Contoh berikut menunjukkan hierarki biasa:

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
 
Jika hierarki anda serupa, anda mesti menetapkannya sebagai senarai rata, seperti yang ditunjukkan di sini:
- Contoso India - Amalan SAP - Perunding Teknikal 
- Contoso India - Amalan SAP - Perunding Fungsi       
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi 
- Contoso India - Amalan Teknologi Microsoft Perunding Fungsi 
- Contoso AS - Amalan SAP - Perunding Teknikal  
- Contoso AS - Amalan SAP - Perunding Fungsi  
- Contoso AS - Amalan Teknologi Microsoft - Perunding Teknikal 
- Contoso AS - Amalan Teknologi Microsoft - Perunding Fungsi

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Kami adalah sebuah syarikat perkhidmatan profesional kecil yang beroperasi sebagai satu bahagian sahaja. Bagaimanakah cara terbaik kami menggunakan konsep unit organisasi dalam versi semasa PSA?

Jika syarikat anda beroperasi sebagai satu unit yang mempunyai satu senarai harga kos, anda tidak perlu menyediakan sebarang unit organisasi. Semasa pemasangan PSA, Dynamics 365 mewujudkan satu unit organisasi lalai yang mempunyai nama yang sama dengan organisasi. Secara lalai, semua pengguna ditugaskan untuk unit organisasi ini. Apabila sistem memerlukan unit organisasi dipilih, unit organisasi ini dipilih secara lalai.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Apabila projek dicipta daripada sebut harga atau baris kontrak projek, unit kontrak lalai datang daripada kontrak sebut harga atau projek. Jika projek dicipta sebelum entiti jualan seperti sebut harga atau kontrak projek, apakah unit kontrak lalai?

Apabila projek dicipta sendiri, unit kontrak lalai projek ini adalah berdasarkan pengguna yang menciptanya. Pengguna itu juga ialah pengurus projek lalai. Jika projek dipetakan kepada entiti jualan seperti sebut harga atau kontrak projek, unit kontrak pada projek adalah berdasarkan kepada entiti jualan. Dalam hal ini, anggaran projek mungkin akan dikira semula kerana senarai harga kos digunakan untuk mengira perubahan anggaran kos jika unit kontrak ditukar. Senarai harga jualan digunakan untuk mengira anggaran jualan yang akan ditukar supaya ia disegerakkan dengan senarai harga projek pada sebut harga.

Medan **Unit Kontrak** dan **Mata Wang** pada projek dikunci untuk edit kerana ia mesti segerak dengan nilai pada entiti jualan (sebut harga atau kontrak projek) yang projek tersebut dipetakan.
