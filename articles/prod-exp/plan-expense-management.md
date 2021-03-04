---
title: Konfigurasikan pengurusan perbelanjaan
description: Artikel ini menerangkan pertimbangan dan keputusan yang anda mesti lakukan semasa proses perancangan sebelum anda mengkonfigurasi Pengurusan perbelanjaan dalam Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960348"
---
# <a name="configure-expense-management"></a>Konfigurasikan pengurusan perbelanjaan

Topik ini menerangkan pertimbangan dan keputusan yang anda mesti lakukan semasa proses perancangan sebelum anda mengkonfigurasi Pengurusan perbelanjaan. Dalam Pengurusan perbelanjaan, anda boleh menyimpan maklumat tentang kaedah pembayaran, permintaan perjalanan, laporan perbelanjaan, dasar, dan sebagainya.

Disebabkan oleh kebanyakan keputusan yang anda lakukan apabila anda merancang konfigurasi anda untuk Pengurusan perbelanjaan adalah berdasarkan hierarki dan struktur kewangan organisasi anda, anda mesti merujuk kepada dokumen perancangan untuk kawasan tersebut.

## <a name="intercompany-expenses"></a>Perbelanjaan antara syarikat

Apabila anda mendayakan perbelanjaan antara syarikat, anda membenarkan entiti sah dan pekerja untuk menanggung perbelanjaan bagi pihak entiti sah yang lain, dan mengumpulkan pembayaran daripada entiti sah pekerjaan dalam organisasi anda. Contohnya, pekerja dalam entiti sah A melengkapkan projek untuk entiti sah B, dan projek itu menanggung perbelanjaan berkaitan perjalanan. Jika perbelanjaan antara syarikat didayakan, pekerja tersebut boleh memfailkan laporan perbelanjaan yang akan menyiarkan perbelanjaan ke entiti sah B, dan perbelanjaan tersebut mesti dibayar oleh entiti sah A. Jika organisasi anda tidak mempunyai berbilang entiti sah, anda tidak perlu mendayakan perbelanjaan antara syarikat.

**Keputusan:** Adakah anda mahu mendayakan perbelanjaan antara syarikat?

## <a name="financial-management"></a>Pengurusan kewangan

Pengurusan perbelanjaan diintegrasikan kemas dengan pengurusan kewangan organisasi anda. Banyak konfigurasi anda untuk Pengurusan perbelanjaan akan berdasarkan pada keputusan yang telah anda lakukan tentang kewangan organisasi anda. Bahagian berikut menerangkan pelbagai bidang yang memerlukan perancangan dan keputusan, berdasarkan keputusan kewangan organisasi anda dan panduan daripada pasukan kepimpinan anda.

### <a name="per-diems"></a>Harian

Anda mesti mentakrifkan pekerja bagi sehari yang organisasi anda sediakan. Oleh kerana bagi sehari biasanya digunakan untuk menampung perbelanjaan seperti makanan, penginapan, dan perbelanjaan sampingan yang lain, anda boleh mencipta peraturan untuk elaun bagi sehari yang ditawarkan oleh organisasi anda. kadar bagi sehari boleh didasarkan pada masa dalam tahun, lokasi perjalanan, atau kedua-duanya. Apabila anda menakrif peraturan bagi sehari, anda boleh menentukan bahawa peratusan kadar bagi sehari akan ditahan jika pekerja menerima hidangan atau perkhidmatan percuma. Anda juga boleh menakrif tahap kadar bagi sehari untuk menetapkan bilangan jam minimum dan maksimum yang kadar bagi sehari boleh digunakan kepada perjalanan pekerja.

**Keputusan:**

- Peraturan bagi sehari lalai untuk hari pertama dan terakhir:

    - Berapakah bilangan jam minimum yang boleh dituntut oleh pekerja untuk sehari dan masih menerima bagi sehari?
    - Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk hidangan untuk hari pertama dan hari terakhir? Jika terdapat pengurangan, berapakah peratusan pengurangan?
    - Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk hotel untuk hari pertama dan hari terakhir? Jika terdapat pengurangan, berapakah peratusan pengurangan?
    - Adakah terdapat pengurangan dalam amaun yang ditawarkan untuk perbelanjaan lain yang berlaku pada hari pertama dan hari terakhir? Jika terdapat pengurangan, berapakah peratusan pengurangan?

- Peraturan bagi sehari lalai:

    - Adakah terdapat pengurangan peratusan bagi elaun bagi sehari untuk setiap hidangan jika, contohnya, hidangan adalah percuma? Jika terdapat pengurangan, berapakah peratusan pengurangan untuk setiap hidangan?
    - Adakah pengurangan hidangan dikira setiap hari, setiap perjalanan, atau dengan bilangan hidangan setiap hari?
    - Perlukah amaun bagi sehari akan dibundarkan mengikut cara biasa atau dibundarkan?
    - Adakah bagi sehari dikira pada tempoh 24 jam atau pada hari kalendar?

- Peraturan bagi sehari yang didasarkan pada lokasi:

    - Adakah kadar bagi sehari berbeza mengikut lokasi? Lokasi apakah yang disertakan?
    - Jika kadar bagi sehari berbeza mengikut lokasi, untuk setiap lokasi, apakah amaun peratusan yang disediakan untuk jenis perbelanjaan berikut:

        - Hidangan
        - Hotel
        - Perbelanjaan lain

### <a name="expense-management-journals-and-accounts"></a>Jurnal pengurusan perbelanjaan dan akaun

Pengurusan perbelanjaan memerlukan anda menggunakan berbilang jurnal dan akaun. Anda mesti memutuskan, contohnya, sama ada akaun yang sama digunakan untuk pendahuluan tunai dan pertikaian kad kredit.

**Keputusan:**

- Jurnal lejar manakah adalah laporan perbelanjaan diluluskan yang disiarkan?
- Akaun manakah yang digunakan untuk pendahuluan tunai?
- Perlukah pendahuluan tunai disiarkan dengan segera?

### <a name="payment-methods"></a>Kaedah pembayaran

Apabila anda membenarkan pekerja menanggung perbelanjaan bagi pihak perniagaan anda, anda mesti mentakrifkan kaedah pembayaran yang pekerja dibenarkan untuk menggunakan. Contohnya, anda mungkin membenarkan pekerja menggunakan wang tunai atau kad kredit korporat. Anda juga boleh membenarkan pekerja untuk menggunakan kad kredit peribadi, dan kemudian membayar balik pekerja. Anda mesti membuat keputusan berikut untuk setiap kaedah pembayaran yang anda benarkan.

**Keputusan:**

- Apakah kaedah pembayaran yang dibenarkan?
- Siapakah memiliki perbelanjaan kaedah pembayaran?
- Adakah terdapat jenis akaun ofset? Jika terdapat jenis akaun ofset, apakah ia?
- Jika terdapat akaun ofset, apakah akaun tersebut?
- Jika kaedah pembayaran adalah kad kredit, perlukah kaedah pembayaran digunakan hanya dengan transaksi yang diimport?

### <a name="expense-categories-and-shared-categories"></a>Kategori perbelanjaan dan kategori dikongsi

Apabila pekerja mencipta laporan perbelanjaan, setiap perbelanjaan yang mereka rekod mesti dikaitkan dengan kategori perbelanjaan. Kategori perbelanjaan diperoleh daripada kategori dikongsi yang boleh dikongsi merentasi entiti yang sah dalam organisasi anda. Kategori ini juga boleh dikongsi dalam Pengurusan projek dan perakaunan, bergantung kepada cara organisasi anda ditakrifkan. Berdasarkan definisi organisasi dan panduan anda daripada pasukan pelaksanaan, menentukan sama ada kategori yang digunakan dalam Pengurusan perbelanjaan akan digunakan hanya dalam Pengurusan perbelanjaan, atau sama ada mereka hendaklah dikongsi di antara Pengurusan projek dan perakaunan dan Pengurusan perbelanjaan. Ambil perhatian kategori ini boleh dikongsi di antara Projek dan Perbelanjaan atau Projek dan Pengeluaran, tetapi tidak di antara Perbelanjaan dan Pengeluaran. Anda mesti membuat keputusan berikut untuk setiap kategori perbelanjaan.

**Keputusan:**

- Apakah itu kategori perbelanjaan? Contohnya termasuk kategori untuk penerbangan, hotel, atau perbatuan.
- Bolehkah kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan?
- Apakah itu jenis perbelanjaan?
- Apakah itu kaedah pembayaran lalai untuk kategori perbelanjaan?
- Adakah perbelanjaan dalam kategori perbelanjaan perlu diperincikan?
- Apakah itu akaun lalai utama untuk kategori perbelanjaan?
- Apakah itu kumpulan cukai jualan item lalai untuk kategori perbelanjaan?
- Adakah kaedah pembayaran tambahan dibenarkan untuk kategori perbelanjaan? Jika kaedah pembayaran tambahan dibenarkan, apakah itu?
- Adakah terdapat subkategori dalam kategori perbelanjaan ini? Jika terdapat subkategori, anda juga mesti membuat keputusan berikut:

    - Adakah sebarang subkategori dikecualikan daripada pemulihan cukai?
    - Apakah itu kumpulan cukai jualan item subkategori?

Jika kategori perbelanjaan juga digunakan dalam Pengurusan projek dan perakaunan, jawab soalan yang tinggal. Jika tidak, alihkan ke bahagian seterusnya.

- Akaun kos manakah akan digunakan untuk perbelanjaan yang berikut?

    - Kos
    - Peruntukan gaji
    - WIP-nilai kos
    - Kos-item
    - WIP-nilai kos-item
    - Kerugian terakru
    - WIP-kerugian terakru

- Akaun hasil manakah akan digunakan untuk yang berikut?

    - Hasil diinvois
    - Hasil terakru-nilai jualan
    - WIP-nilai jualan
    - Hasil terakru-pengeluaran
    - WIP-pengeluaran
    - Hasil terakru-keuntungan
    - WIP-keuntungan
    - Hasil terakru-langganan
    - WIP-langganan

### <a name="taxes"></a>Cukai

Untuk cukai berkaitan perbelanjaan, anda mesti menentukan apa yang disertakan atau didayakan pada laporan perbelanjaan.

**Keputusan:**

- Adakah cukai jualan dimasukkan ke dalam amaun perbelanjaan?
- Perlukah pemulihan cukai didayakan pada perbelanjaan?

    > [!NOTE]
    > Apabila anda merancang lejar umum, jika anda memutuskan untuk menggunakan cukai jualan AS dan menggunakan peraturan cukai, anda tidak boleh mendayakan pemulihan cukai pada perbelanjaan. (Untuk menggunakan cukai jualan AS dan menggunakan peraturan cukai, tetapkan pilihan **Gunakan peraturan percukaian cukai jualan** kepada **Ya**.)

## <a name="policies"></a>Dasar

Dengan mencipta dasar laporan perbelanjaan, anda boleh membantu organisasi anda menjimatkan masa dan wang apabila pekerja menanggung perbelanjaan bagi pihaknya. Dasar membantu menjamin pekerja kekal dalam belanjawan, memberikan semua maklumat yang diperlukan, dan membelanjakan wang hanya apabila mereka memerlukannya. Anda mesti membuat keputusan berikut untuk setiap dasar laporan perbelanjaan dan setiap dasar kelulusan laporan perbelanjaan yang anda cipta.

**Keputusan:**

- Apakah nama dasar itu?
- Untuk apakah dasar perbelanjaan?
- Jika anda sebelum ini memutuskan untuk mendayakan perbelanjaan antara syarikat, syarikat mana dalam organisasi anda akan menggunakan dasar ini?
- Bilakah dasar ini berkuat kuasa?
- Bilakah dasar ini tamat tempoh?
- Apakah itu peraturan dasar?
- Apakah hasil peraturan dasar itu?
