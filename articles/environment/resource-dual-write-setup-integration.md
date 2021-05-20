---
title: Persediaan Project Operations dan integrasi data konfigurasi
description: Topik ini menyediakan maklumat tentang menyediakan dan mengkonfigurasi Project Operations bagi peta dwi tulis.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939021"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Persediaan Project Operations dan integrasi data konfigurasi

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menyediakan maklumat tentang integrasi dwi tulis Project Operations untuk entiti penyediaan dan konfigurasi.

## <a name="project-contracts-contract-lines-and-projects"></a>Kontrak Projek, baris kontrak dan projek

Kontrak projek, baris kontrak dan projek dicipta dalam Dataverse dan disegerakkan ke aplikasi Finance and Operations untuk perakaunan tambahan. Rekod dalam entiti ini boleh dicipta dan dipadam hanya dalam Dataverse. Walau bagaimanapun, atribut perakaunan seperti kumpulan cukai jualan lalai dan dimensi kewangan boleh ditambah ke rekod ini dalam aplikasi Finance and Operations.

  ![Konsep integrasi kontrak projek](./media/1ProjectContract.jpg)

Aktiviti jualan bakal pelanggan dan sebut harga dijejak dalam Dataverse dan tidak disegerakkan ke aplikasi Finance and Operations kerana tiada perakaunan hiliran yang berkaitan dengan aktiviti ini.

Kefungsian kontrak projek dalam Dataverse mencipta rekod kontrak projek dalam aplikasi Finance and Operations menggunakan peta jadual **Pengepala kontrak projek (salesorders)**. Menyimpan kontrak projek dalam Dataverse turut memulakan penciptaan rekod entiti pelanggan kontrak projek. Rekod ini disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual **Sumber pembiayaan projek (msdyn\_projectcontractssplitbillingrules)**. Peta ini juga menyegerakkan penambahan, pengemaskinian dan pemadaman pelanggan kontrak projek. Pecahan peratusan pengebilan antara pelanggan kontrak projek adalah dikuasai hanya dalam Dataverse dan tidak disegerakkan ke aplikasi Finance and Operations.

Selepas kontrak projek dicipta dalam Dataverse, akauntan projek boleh mengemas kini atribut perakaunan untuk kontrak projek ini dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Kontrak projek** > **Sediakan** > **Tunjukkan perakaunan lalai**. Akauntan boleh menyemak semula atribut kontrak projek operasi seperti tarikh penghantaran yang diminta dan amaun kontrak dengan memilih ID kontrak projek dalam aplikasi Finance and Operations yang membuka rekod kontrak projek yang berkaitan dalam Dataverse.

Entiti projek disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual **Projek V2 (msdyn\_projects)**. Akauntan projek boleh:

  - Semak semula dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Semua projek**. 
  - Kemas kini atribut perakaunan untuk projek dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Semua projek** > **Sediakan** > **Tunjukkan perakaunan lalai**.  
  - Menyemak semula atribut projek operasi seperti tarikh mula dan akhir yang dianggarkan dengan memilih ID projek dalam aplikasi Finance and Operations yang membuka rekod projek yang berkaitan dalam Dataverse.

Projek dikaitkan dengan kontrak projek melalui entiti **Baris kontrak projek**.

Baris kontrak projek dalam Dataverse mencipta peraturan pengebilan kontrak projek dalam aplikasi Finance and Operations menggunakan peta jadual **Baris kontrak projek (salesorderdetails)**. Kaedah pengebilan mentakrifkan jenis peraturan pengebilan kontrak projek dalam aplikasi Finance and Operations:

  - Baris kontrak projek dengan kaedah pengebilan masa dan bahan mencipta peraturan pengebilan masa dan jenis bahan.
  - Baris kontrak kaedah pengebilan harga tetap mencipta peraturan pengebilan pencapaian.

Baris kontrak projek boleh disemak semula dengan akauntan projek dalam aplikasi Finance and Operations dengan pergi ke **Pengurusan dan perakaunan projek** > **Kontrak projek** > **Sediakan** > **Tunjukkan perakaunan lalai** dan menyemak semula butiran pada tab **Baris kontrak**. Akauntan juga boleh menetapkan dimensi kewangan untuk baris kontrak kaedah pengebilan harga tetap pada tab ini.

## <a name="billing-milestones"></a>Pencapaian pengebilan

Baris kontrak projek yang menggunakan kaedah pengebilan harga tetap diinvois melalui pencapaian pengebilan. Pencapaian pengebilan disegerakkan ke transaksi projek pada akaun dalam aplikasi Finance and Operations dengan menggunakan peta jadual **Pencapaian baris kontrak integrasi Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrasi pencapaian pengebilan](./media/2Milestones.jpg)

Akauntan boleh menyemak semula transaksi pada akaun dan melaraskan atribut perakaunan untuk transaksi itu dengan pergi ke **Pengurusan dan perakaunan projek** > **Kontrak projek** > **Kekalkan** > **Transaksi pada akaun** atau **Pengurusan dan perakaunan projek** > **Semua projek** > **Kekalkan** > **Transaksi pada akaun**.

Apabila pertama kali anda mencipta pencapaian pengebilan untuk baris kontrak projek yang diberikan, sistem secara automatik mencipta projek anggaran hasil tetap untuk projek yang berkaitan dengan baris kontrak ini. Projek anggaran hasil harga tetap boleh disemak semula dengan pergi ke **Pengurusan dan perakaunan projek** > **Projek anggaran hasil harga tetap**.

### <a name="project-tasks"></a>Tugas projek

Tugas projek disegerakkan ke aplikasi Finance and Operations melalui peta jadual **Tugas projek (msdyn\_projecttasks)** untuk tujuan rujukan sahaja. Mencipta, mengemas kini dan memadam operasi tidak disokong melalui aplikasi Finance and Operations.

  ![Integrasi tugas projek](./media/3Tasks.jpg)

## <a name="project-resources"></a>Sumber projek

Entiti **Peranan sumber projek** disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual **Peranan sumber projek untuk semua syarikat (bookableresourcecategories)** untuk tujuan rujukan sahaja. Oleh kerana peranan sumber dalam Dataverse bukan khusus syarikat, sistem secara automatik mencipta rekod peranan sumber khusus syarikat yang berkaitan dalam aplikasi Finance and Operations secara automatik untuk entiti sah termasuk dalam skop integrasi dwi tulis.

![Integrasi peranan sumber](./media/5Resources.jpg)

Sumber projek dalam Project Operations dikekalkan dalam Dataverse dan tidak disegerakkan ke aplikasi Finance and Operations.

### <a name="transaction-categories"></a>Kategori transaksi

Kategori transaksi dikekalkan dalam Dataverse dan disegerakkan ke aplikasi Finance and Operations menggunakan peta jadual **Kategori transaksi projek (msdyn\_transactioncategories)**. Selepas rekod kategori transaksi disegerakkan, sistem secara automatik mencipta empat rekod kategori dikongsi. Setiap rekod yang berkaitan dengan jenis transaksi dalam aplikasi Finance and Operations dan pautkannya ke rekod kategori transaksi.

![Integrasi kategori transaksi](./media/4TransactionCategories.jpg)

Menggunakan kategori transaksi untuk anggaran dan aktual memerlukan akauntan projek atau pentadbir sistem untuk mencipta kategori projek yang berkaitan dalam setiap entiti sah. Untuk maklumat lanjut, lihat [Konfigurasikan kategori projek](../project-accounting/configure-project-categories.md).
