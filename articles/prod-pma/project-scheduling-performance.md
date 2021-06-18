---
title: Prestasi penjadualan sumber projek
description: Topik ini memberikan maklumat mengenai cara untuk menambah baik prestasi penjadualan sumber untuk sebilangan besar projek.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010032"
---
# <a name="project-resource-scheduling-performance"></a>Prestasi penjadualan sumber projek

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Isu prestasi yang berkaitan dengan penjadualan sumber boleh berlaku apabila bilangan projek mencapai ke dalam ribuan. Untuk meningkatkan prestasi penjadualan sumber, ciri tersedia membenarkan pengguna untuk mengurangkan masa yang diperlukan untuk melancarkan borang ketersediaan sumber. Khususnya, ini akan mengalih keluar proses penyegerakan gulungan kapasiti sumber dan menggunakan jadual **SumberProjekRes** untuk mempercepat carian sumber. Ambil perhatian jadual **ResRollup** tidak akan digunakan lagi.

> [!IMPORTANT]
> Jika terdapat kebergantungan pada sama ada proses penyegerakan gulungan kapasiti sumber atau jadual **SumberProjekRes**, jangan gunakan ciri ini.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Dayakan peningkatan prestasi penjadualan sumber
Untuk mendayakan peningkatan prestasi penjadualan sumber, lengkapkan langkah berikut.

1. Pergi ke **Pengurusan ciri** > **Semua**, dan dalam senarai ciri, cari **Dayakan ciri peningkatan prestasi penjadualan sumber projek**.
2. Pilih **Dayakan sekarang**.

> [!NOTE]
> Jika anda tidak dapat mencari ciri dalam senarai, pilih **Semak untuk kemas kini** untuk segar semula senarai.

3. Segar semula pelayar anda, dan kemudian pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Sumber projek** > **Segerakkan kapasiti kalendar sumber merentasi semua syarikat**.
4. Tetapkan **Alih keluar rekod kapasiti sedia ada** kepada **Ya** untuk mengalih keluar data sebelumnya. Jika anda mahu menjana data tambahan, tetapkan ia kepada **Tidak**.
5. Dalam medan **Kod tempoh**, pilih tempoh data yang sepatutnya dijana. Jika anda memilih kod tempoh, tarikh mula dan tamat tidak perlu ditakrifkan.
6. Jika anda membiarkan medan **Kod tempoh** kosong, pilih tarikh mula dan tamat khusus untuk menjana data.
7. Pilih **OK**.

 > [!NOTE]
 > Ini akan mengedarkan data umum untuk jadual **KapasitiKalendarRes** merentasi semua syarikat dalam persekitaran anda, jadi kerja kelompok hanya perlu berjalan dalam satu entiti yang sah. Data dalam kerja kelompok ini diperlukan untuk mengira kapasiti sumber melalui kalendar berkaitan.

8. Pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Sumber projek** > **Isikan sumber projek merentasi semua syarikat** dan kemudian pilih **OK**. Ini adalah skrip naik taraf data untuk data umum dalam **ResProjectResource**, **ResCalendarDateTimeRange**, dan jadual **ResEffectiveDateTimeRange**. Nilai untuk medan **PSAPRojSchedRole.RootActivity** juga dikemas kini. Jika ini tidak berjalan, anda akan menerima amaran apabila anda cuba untuk melaksanakan operasi penjadualan sumber.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Matikan peningkatan prestasi penjadualan sumber

1. Pergi ke **Pengurusan ciri** > **Semua**  dan carian untuk **Dayakan ciri peningkatan prestasi penjadualan sumber projek**.
2. Pilih ciri dan kemudian pilih butang **Nyahdaya**.
3. Segar semula pelayar anda.
4. Pergi ke **Pengurusan dan perakaunan projek** > **Berkala** > **Penyegerakan kapasiti** > **Segerakkan gulungan kapasiti sumber**.
5. Pada halaman **Penyegerakan gulungan kapasiti**, tetapkan **Alih keluar rekod kapasiti sedia ada** kepada **Ya** untuk mengalih keluar data sebelumnya. Jika anda mahu menjana data tambahan, tetapkan ia kepada **Tidak**.
6. Dalam medan **Kod tempoh**, pilih tempoh data yang sepatutnya dijana. Jika anda memilih kod tempoh, tarikh mula dan tamat tidak perlu ditakrifkan.
7. Jika anda membiarkan medan **Kod tempoh** kosong, pilih tarikh mula dan tamat khusus untuk menjana data.
8. Pilih **OK**.

> [!NOTE]
> Ini akan mengedarkan data umum untuk jadual **ResRollup** merentasi semua syarikat dalam persekitaran anda, jadi kerja kelompok hanya perlu berjalan dalam satu entiti yang sah. Kerja kelompok ini diperlukan untuk semua pandangan **Ketersediaan Sumber**. Jika kerja kelompok ini tidak berjalan, data **ResRollup** akan dijana pada bila-bila masa, yang boleh mengambil masa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]