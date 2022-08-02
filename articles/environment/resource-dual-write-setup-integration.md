---
title: Persediaan Project Operations dan integrasi data konfigurasi
description: Artikel ini memberikan maklumat tentang menyediakan dan mengkonfigurasi peta dwi-tulis Operasi Projek.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029163"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Persediaan Project Operations dan integrasi data konfigurasi

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini memberikan maklumat tentang integrasi dwi-tulis Project Operations untuk entiti persediaan dan konfigurasi.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrak Projek, baris kontrak dan projek

Kontrak projek, garis kontrak dan projek dicipta Dataverse dan disegerakkan kepada aplikasi kewangan dan operasi untuk perakaunan tambahan. Rekod dalam entiti ini boleh dicipta dan dipadam hanya dalam Dataverse. Walau bagaimanapun, atribut perakaunan seperti keingkaran kumpulan cukai jualan dan dimensi kewangan boleh ditambah kepada rekod ini dalam aplikasi kewangan dan operasi.

  ![Konsep integrasi kontrak projek.](./media/1ProjectContract.jpg)

Petunjuk, peluang dan sebut harga aktiviti jualan dijejaki Dataverse dan tidak disegerakkan ke aplikasi kewangan dan operasi kerana tidak ada perakaunan hiliran yang berkaitan dengan aktiviti ini.

Fungsi kontrak projek dalam Dataverse mencipta rekod kontrak projek dalam aplikasi kewangan dan operasi menggunakan **peta jadual pengepala kontrak Projek (jurujual).** Menyimpan kontrak projek dalam Dataverse turut memulakan penciptaan rekod entiti pelanggan kontrak projek. Rekod ini disegerakkan ke aplikasi kewangan dan operasi menggunakan **peta jadual sumber pembiayaan Projek (msdyn\_ projectcontractssplitbillingrules**). Peta ini juga menyegerakkan penambahan, pengemaskinian dan pemadaman pelanggan kontrak projek. Peratusan pengebilan berpecah antara pelanggan kontrak projek hanya Dataverse dikuasai dan tidak disegerakkan ke aplikasi kewangan dan operasi.

Selepas kontrak projek dibuat, Dataverse akauntan projek boleh mengemas kini atribut perakaunan untuk kontrak projek ini dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan** > **Projek dan kontrak Projek perakaunan** > **Sediakan** > **Tunjukkan perakaunan** lalai. Akauntan boleh menyemak atribut kontrak projek operasi, seperti tarikh penghantaran yang diminta dan jumlah kontrak dengan memilih ID kontrak projek dalam aplikasi kewangan dan operasi yang membuka rekod kontrak projek yang berkaitan dalam Dataverse.

Entiti projek disegerakkan ke aplikasi kewangan dan operasi menggunakan **peta jadual Projek V2 (projek\_ msdyn**). Akauntan projek boleh:

  - Semak projek dalam aplikasi kewangan dan operasi dengan pergi ke **Pengurusan Projek dan perakaunan** > **Semua projek**. 
  - Kemas kini atribut perakaunan untuk projek dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan Projek dan perakaunan** > **Semua projek** > **Sediakan** > **Tunjukkan perakaunan** lalai.  
  - Semak atribut projek operasi, seperti anggaran tarikh mula dan tamat, dengan memilih ID projek dalam aplikasi kewangan dan operasi yang membuka rekod projek yang berkaitan dalam Dataverse.

Projek dikaitkan dengan kontrak projek melalui entiti **Baris kontrak projek**.

Garis kontrak projek dalam Dataverse mencipta peraturan pengebilan kontrak projek dalam aplikasi kewangan dan operasi menggunakan **peta jadual baris kontrak Projek (salesorderdetails**). Kaedah pengebilan mentakrifkan jenis peraturan pengebilan kontrak projek dalam aplikasi kewangan dan operasi:

  - Baris kontrak projek dengan kaedah pengebilan masa dan bahan mencipta peraturan pengebilan masa dan jenis bahan.
  - Baris kontrak kaedah pengebilan harga tetap mencipta peraturan pengebilan pencapaian.

Barisan kontrak projek boleh disemak oleh akauntan projek dalam aplikasi kewangan dan operasi dengan pergi ke **pengurusan Projek dan perakaunan** > **kontrak** > **Projek Sediakan** > **Tunjukkan perakaunan** lalai, dan menyemak butiran pada **tab Garis** kontrak. Akauntan juga boleh menetapkan dimensi kewangan lalai untuk garis kontrak kaedah pengebilan harga tetap pada tab ini.

## <a name="billing-milestones"></a>Pencapaian pengebilan

Baris kontrak projek yang menggunakan kaedah pengebilan harga tetap diinvois melalui pencapaian pengebilan. Tonggak pengebilan disegerakkan ke transaksi dalam akaun projek dalam aplikasi kewangan dan operasi dengan menggunakan **peta jadual baris kontrak integrasi Project Operations (msdyn\_ contractlinescheduleofvalues**).

  ![Integrasi pencapaian pengebilan.](./media/2Milestones.jpg)

Akauntan boleh menyemak semula transaksi pada akaun dan melaraskan atribut perakaunan untuk transaksi itu dengan pergi ke **Pengurusan dan perakaunan projek** > **Kontrak projek** > **Kekalkan** > **Transaksi pada akaun** atau **Pengurusan dan perakaunan projek** > **Semua projek** > **Kekalkan** > **Transaksi pada akaun**.

Apabila pertama kali anda mencipta pencapaian pengebilan untuk baris kontrak projek yang diberikan, sistem secara automatik mencipta projek anggaran hasil tetap untuk projek yang berkaitan dengan baris kontrak ini. Projek anggaran hasil harga tetap boleh disemak semula dengan pergi ke **Pengurusan dan perakaunan projek** > **Projek anggaran hasil harga tetap**.

### <a name="project-tasks"></a>Tugas projek

Tugas projek disegerakkan ke aplikasi kewangan dan operasi melalui **peta jadual Tugas Projek (msdyn\_ projecttasks)** untuk tujuan rujukan sahaja. Mencipta, mengemas kini dan memadam operasi tidak disokong melalui aplikasi kewangan dan operasi.

  ![Integrasi tugas projek.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Sumber projek

Entiti **peranan** sumber Projek disegerakkan ke aplikasi kewangan dan operasi menggunakan **peranan sumber Projek untuk semua peta jadual syarikat (bookableresourcecategories)** untuk tujuan rujukan sahaja. Oleh kerana peranan Dataverse sumber tidak khusus syarikat, sistem ini secara automatik membuat rekod peranan sumber khusus syarikat masing-masing dalam aplikasi kewangan dan operasi secara automatik untuk semua entiti undang-undang yang termasuk dalam skop integrasi dwi-tulis.

![Integrasi peranan sumber.](./media/5Resources.jpg)

Sumber projek dalam Operasi Projek dikekalkan Dataverse dan tidak disegerakkan ke aplikasi kewangan dan operasi.

### <a name="transaction-categories"></a>Kategori transaksi

Kategori transaksi dikekalkan Dataverse dan disegerakkan ke aplikasi kewangan dan operasi menggunakan **peta jadual kategori transaksi Projek (msdyn\_ transactioncategories**). Selepas rekod kategori transaksi disegerakkan, sistem secara automatik mencipta empat rekod kategori dikongsi. Setiap rekod sepadan dengan jenis transaksi dalam aplikasi kewangan dan operasi dan memautkannya ke rekod kategori transaksi.

![Integrasi kategori transaksi.](./media/4TransactionCategories.jpg)

Menggunakan kategori transaksi untuk anggaran dan aktual memerlukan akauntan projek atau pentadbir sistem untuk mencipta kategori projek yang berkaitan dalam setiap entiti sah. Untuk maklumat lanjut, lihat [Konfigurasikan kategori projek](../project-accounting/configure-project-categories.md).
