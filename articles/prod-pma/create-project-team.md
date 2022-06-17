---
title: Cipta pasukan projek
description: Artikel ini menyediakan maklumat tentang cara mencipta dan mengurus pasukan projek.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9df8b3ee9b42a33c6031c78ff3673cad47bfe6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927339"
---
# <a name="create-a-project-team"></a>Cipta pasukan projek

[!include [banner](../includes/banner.md)]

Untuk menggunakan peranan yang sebelum ini disediakan dalam projek, pengurus projek mesti kaitkan peranan dengan projek. Berbilang peranan boleh ditugaskan untuk projek. Untuk mengelakkan kekeliruan, peranan ini dilabelkan secara automatik semasa penempahan. Contohnya, jika pengurus projek memerlukan tiga jurutera perisian, tiga peranan jurutera Perisian yang mempunyai **jurutera perisian 1**, **perisian Jurutera 2**, dan **jurutera perisian 3** sebagai label mereka dijana secara automatik. Jika ciri peranan sebelum ini telah ditetapkan untuk peranan, ia akan digunakan sebagai penapis semasa mencari sumber. Ciri tambahan boleh ditambah apabila diperlukan untuk sempurnakan lagi carian.

Tetapan pandangan juga boleh disesuaikan untuk memberi pandangan yang lebih baik tentang ketersediaan sumber. Terdapat pilihan untuk menunjukkan ketersediaan setiap jam, harian, mingguan, bulanan, suku tahunan, dan tahunan. Terdapat juga pilihan untuk menunjukkan kapasiti pada sumber yang tersedia dan yang selebihnya. Pilihan ini berguna untuk pengurusan masa, apabila anda menganggarkan masa tersedia untuk aktiviti atau ketersediaan sumber.

Pengurus projek boleh memilih peranan pada halaman dan kemudian, jika terdapat sumber tersedia yang sesuai dengan keperluan, pilih untuk menguntukkan sumber untuk memenuhi peranan. Ambil perhatian bahawa sumber tidak perlu diperuntukkan pada masa ini dalam peringkat perancangan. Apabila anda mencipta WBS, anda boleh menggantikan peranan dengan sumber diperlukan untuk projek. Jika peranan digantikan dengan sumber diperlukan dalam WBS, persediaan sumber secara automatik mengemas kini senarai pasukan dan penjadualan projek.

[![Senarai pasukan projek yang merangkumi kedua-dua peranan dan sumber sebenar.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Pengurus projek mempunyai pelbagai pilihan untuk menempah sumber untuk projek, seperti **Baki kapasiti**, **Kapasiti penuh**, **Peratusan kapasiti** dan **Tentukan jam**. Pilihan penempahan ini boleh dibatalkan pada bila-bila masa jika tugasan sumber berubah. Dua jenis penempahan disokong:

- **Tempah Keras** – Tempahan sumber telah diluluskan dan disahkan untuk bekerja pada perikatan untuk tempoh yang ditetapkan.
- **Tempah sementara** – Tempahan sumber telah secara sementara ditetapkan untuk bekerja pada perikatan untuk tempoh yang ditetapkan.

Prosedur berikut menjelaskan cara mencipta pasukan projek.

## <a name="create-a-project-team"></a>Cipta pasukan projek

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

## <a name="monitor-project-teams"></a>Pantau pasukan projek
1. Pada halaman **Semua projek**, pilih paut **Projek ID** untuk projek **Naik taraf XYZ Fasa 2**.
2. Pada Fasttab **Pasukan dan penjadualan projek**, mengesahkan bahawa sumber projek yang disenaraikan adalah betul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]