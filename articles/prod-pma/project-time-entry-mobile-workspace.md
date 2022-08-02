---
title: Ruang kerja entri masa Projek
description: Artikel ini menyediakan maklumat tentang ruang kerja mudah alih masukan masa Projek. Ruang kerja ini membolehkan pengguna memasukkan dan menjimatkan masa terhadap projek dengan menggunakan peranti mudah alih mereka.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 50388bd024fdf2de0d28e49ef07a01b03c6b88f0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029679"
---
# <a name="project-time-entry-mobile-workspace"></a>Ruang kerja entri masa Projek

[!include [banner](../includes/banner.md)]

Artikel ini menyediakan maklumat tentang **ruang kerja mudah alih masukan** masa Projek. Ruang kerja ini membolehkan pengguna memasukkan dan menjimatkan masa terhadap projek dengan menggunakan peranti mudah alih mereka.

Ruang kerja mudah alih ini bertujuan untuk digunakan bersama dengan aplikasi mudah alih Dynamics 365 Unified Ops. 

## <a name="overview"></a>Ikhtisar
Sebagai sebahagian daripada kerja harian mereka, sumber projek sentiasa berada di tapak atau perjalanan. **Ruang kerja kemasukan masa projek** akan membolehkan pengguna memasukkan masa yang boleh dibilkan atau tidak boleh dibilkan terhadap projek pada peranti mudah alih pilihan mereka. Oleh itu, sumber projek boleh merekodkan penyertaan masa pada bila-bila masa dan di mana jua. Mereka juga boleh melihat penyertaan masa yang sudah direkodkan. 

Secara khusus, dalam ruang kerja mudah alih **entri masa Projek**, pengguna boleh melakukan tugas ini:

-   Untuk sebarang tarikh yang dipilih, masukkan bilangan jam yang anda belanjakan untuk tugas tertentu.
-   Cari mengikut nama projek atau pelanggan untuk mencari projek untuk masukkan masa.
-   Tentukan kategori dan aktiviti untuk masa yang anda belanjakan.
-   Rekod masa sebagai boleh dibilkan atau tidak dapat dibil bagi projek.
-   Secara pilihan masukkan sebarang komen luaran atau dalaman untuk jam tersebut.

## <a name="prerequisites"></a>Prasyarat
Prasyarat berbeza, berdasarkan versi Microsoft Dynamics 365 yang telah digunakan untuk organisasi anda.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prasyarat jika anda menggunakan Dynamics 365 Finance
Jika kewangan telah digunakan untuk organisasi anda, pentadbir sistem mesti menerbitkan ruang kerja mudah alih **entri masa Projek**. Untuk arahan, lihat [Terbitkan ruang kerja mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Prasyarat jika anda menggunakan versi 1611 dengan kemas kini Platform 3 atau kemudian
Jika versi 1611 dengan kemas kini Platform 3 atau lebih baharu digunakan untuk organisasi anda, pentadbir sistem mesti melengkapkan prasyarat berikut. 

<table>
<thead>
<tr class="header">
<th>Prasyarat</th>
<th>Peranan</th>
<th>Penerangan</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Melaksanakan KB 4018050.</td>
<td>Pentadbir sistem</td>
<td>KB 4018050 ialah kemas kini X++ atau hotfix metadata yang mengandungi ruang kerja mudah alih <strong>entri masa Projek</strong>. Untuk melaksanakan KB 4018050, pentadbir sistem anda mesti mengikut langkah ini.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Muat turun hotfix metadata daripada Microsoft Dynamics Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Pasang hotfix metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cipta pakej boleh dilaksanakan</a> yang mengandungi model <strong>ApplicationSuite</strong> dan <strong>ProjectMobile</strong>, dan kemudian muat naik pakej boleh dilaksanakan to LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Gunakan pakej boleh dilaksanakan</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Terbitkan ruang kerja mudah alih <strong>Entri masa projek</strong>.</td>
<td>Pentadbir sistem</td>
<td>Liht <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Terbitkan ruang kerja mudah alih</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Muat turun dan pasang tambahan aplikasi mudah alih

Muat turun dan pasang aplikasi mudah alih kewangan dan operasi:

-   [Untuk telefon Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Untuk iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Daftar masuk ke aplikasi mudah alih
1.  Mulakan peranti mudah alih anda.
2.  Masukkan URL Dynamics 365.
3.  Kali pertama anda mendaftar masuk, anda akan diprom untuk nama pengguna dan kata laluan anda. Masukkan kelayakan anda.
4.  Selepas anda mendaftar masuk, ruang kerja yang tersedia untuk syarikat anda ditunjukkan. Ambil perhatian bahawa jika pentadbir sistem anda menerbitkan ruang kerja baharu kemudian, anda perlu menyegarkan semula senarai ruang kerja mudah alih.

[![Tarik untuk segar semula.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Isikan masa dengan menggunakan ruang kerja mudah alih entri masa Projek
1.  Pada peranti mudah alih anda, pilih ruang kerja **entri masa Projek**.
2.  Pilih **Entri masa**. Tarikh kalendar untuk minggu semasa ditunjukkan.
3.  Untuk tarikh yang dipilih, pilih **Tindakan** &gt; **Entri baharu**.
4.  Masukkan jumlah jam untuk merakam.
5.  Pilih projek untuk entri masa. Senarai menunjukkan projek yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk mendapatkan maklumat lanjut, lihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Jika projek anda tiada dalam senarai, pilih **Cari**. Cari mengikut nama atau bertukar kepada carian mengikut nama projek atau pelanggan.
7.  Pilih kategori. Senarai menunjukkan kategori yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk mendapatkan maklumat lanjut, lihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Jika kategori anda tiada dalam senarai, pilih **Cari**. Cari mengikut kategori atau tukar ke carian mengikut nama kategori.
9.  Pilih aktiviti. Senarai menunjukkan aktiviti yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk mendapatkan maklumat lanjut, lihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Jika aktiviti anda tiada dalam senarai, pilih **Cari**. Cari mengikut nombor aktiviti atau bertukar kepada carian oleh tujuan.

11. Pilih sifat garis.
12. Pilihan: Secara pilihan masukkan sebarang komen luaran dan dalaman.
13. Pilih **Selesai**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]