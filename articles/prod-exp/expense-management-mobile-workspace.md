---
title: Ruang kerja mudah alih Pengurusan perbelanjaan
description: Topik ini menyediakan maklumat tentang ruang kerja mudah alih pengurusan Perbelanjaan. Ruang kerja ini membolehkan pengguna mengambil dan memuat naik resit supaya ianya boleh melampirkannya ke laporan perbelanjaan kemudian. Pengguna juga boleh mencipta baris perbelanjaan dengan pantas menggunakan resit yang dilampirkan dan menguruskan laporan perbelanjaan mereka.
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d5309b55ed146d21d7a42e0b40add9ee346d48aa
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682813"
---
# <a name="expense-management-mobile-workspace"></a>Ruang kerja mudah alih Pengurusan perbelanjaan

Topik ini menyediakan maklumat tentang ruang kerja mudah alih **Pengurusan perbelanjaan**. Ruang kerja ini membolehkan pengguna mengambil dan memuat naik resit supaya ianya boleh melampirkannya ke laporan perbelanjaan kemudian. Pengguna juga boleh mencipta baris perbelanjaan dengan pantas menggunakan resit yang dilampirkan dan menguruskan laporan perbelanjaan mereka. Selain itu, pelulus boleh menggunakan ruang kerja mudah alih **Pengurusan perbelanjaan** untuk melihat laporan perbelanjaan yang ditugaskan kepadanya dan sama ada melulus atau menolak laporan perbelanjaan itu.


Ruang kerja mudah alih ini bertujuan untuk digunakan bersama dengan aplikasi mudah alih Dynamics 365 Unified Ops.


## <a name="overview"></a>Gambaran keseluruhan

Banyak organisasi memerlukan salinan resit yang dilampirkan kepada laporan perbelanjaan berkaitan pelancongan atau berkaitan perniagaan yang diserahkan oleh pekerja untuk bayaran ganti. Ruang kerja mudah alih **Pengurusan perbelanjaan** membolehkan pengguna mencipta baris perbelanjaan baharu dengan pantas pada peranti pilihannya menggunakan gambar resit yang dilampirkan. Sebagai alternatif, pengguna boleh mengambil gambar resit dan kemudian melampirkannya kepada laporan perbelanjaan kemudian. Pekerja juga boleh mencipta dan menguruskan laporan perbelanjaan mereka dan kemudian menyerahkannya untuk kelulusan dan pembayaran balik menggunakan peranti mudah alih mereka.


Secara khususnya, ruang kerja mudah alih **Pengurusan perbelanjaan** membolehkan pengguna melakukan tugas ini:

- Ambil gambar resit, dan muat naik ke Dynamics 365 Finance. Anda kemudiannya boleh melampirkan foto itu ke dalam laporan perbelanjaan.
- Memuat naik fail sebagai resit ditangkap. Anda kemudiannya boleh melampirkan fail itu ke dalam laporan perbelanjaan kemudian.
- Cipta baris perbelanjaan baharu dengan menggunakan resit yang dilampirkan. Anda kemudian boleh menambah item baris ke laporan perbelanjaan kemudian dan menyerahkannya untuk kelulusan dan pembayaran balik.

Anda juga boleh menggunakan ciri ini:

- Cipta laporan perbelanjaan baharu.
- Lampirkan transaksi kad kredit dan perbelanjaan lain yang dicipta sebelum ini dengan laporan perbelanjaan.
- Cipta perbelanjaan baharu untuk laporan perbelanjaan.
- Lampirkan resit ke sebarang perbelanjaan untuk laporan perbelanjaan sama ada dengan mengambil gambar resit atau dengan memuat naik fail sebagai resit ditangkap.
- Bergantung kepada polisi perbelanjaan syarikat, tambah senarai tetamu kepada perbelanjaan.
- Bergantung kepada polisi perbelanjaan syarikat, perincikan perbelanjaan.
- Serahkan laporan perbelanjaan untuk kelulusan dan pembayaran balik.
- Lulus atau tolak Laporan perbelanjaan yang ditugaskan kepada anda sebagai pelulus.

## <a name="prerequisites"></a>Prasyarat
Prasyarat berbeza berdasarkan pada versi yang telah dilaksanakan untuk organisasi anda.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prasyarat jika anda menggunakan Dynamics 365 Finance 
Jika Kewangan telah dilaksanakan untuk organisasi anda, pentadbir sistem mesti menerbitkan ruang kerja mudah alih **Pengurusan perbelanjaan**. Untuk mendapatkan arahan, lihat [Terbitkan ruang kerja mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Prasyarat jika anda menggunakan versi 1611 dengan kemas kini platform 3 atau lebih baharu
Jika versi 1611 dengan kemas kini Platform 3 atau lebih baharu dilaksanakan untuk organisasi anda, pentadbir sistem mesti melengkapkan prasyarat berikut. 

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
<td>Melaksanakan KB 4019015.</td>
<td>Pentadbir sistem</td>
<td>KB 4019015 adalah kemas kini X++ atau hotfix metadata yang mengandungi ruang kerja mudah alih <strong>Pengurusan perbelanjaan</strong>. Untuk melaksanakan KB 4019015, pentadbir sistem anda mesti mengikut langkah ini.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Muat turun hotfix metadata daripada Microsoft Dynamics Lifecycle Services</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Pasang hotfix metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cipta pakej boleh dilaksanakan</a> yang mengandungi model <strong>ApplicationSuite</strong> dan <strong>ExpenseMobile</strong> dan kemudian muat naik pakej boleh dilaksanakan ke LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Gunakan pakej boleh dilaksanakan</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Terbitkan ruang kerja mudah alih <strong>Pengurusan perbelanjaan</strong>.</td>
<td>Pentadbir sistem</td>
<td>Liht <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Terbitkan ruang kerja mudah alih</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Muat turun dan pasang aplikasi mudah alih Dynamics 365 for Operations
Muat turun dan pasang aplikasi mudah alih Dynamics 365 Unified Ops:

- [Untuk telefon Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Untuk iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Daftar masuk ke aplikasi mudah alih
1. Mulakan peranti mudah alih anda.
2. Masukkan URL Dynamics 365.
4. Kali pertama anda mendaftar masuk, anda akan diprom untuk nama pengguna dan kata laluan anda. Masukkan kelayakan anda.
5. Selepas anda mendaftar masuk, ruang kerja yang tersedia untuk syarikat anda ditunjukkan. Ambil perhatian bahawa jika pentadbir sistem anda menerbitkan ruang kerja baharu kemudian, anda perlu menyegarkan semula senarai ruang kerja mudah alih.


[![Tarik untuk segar semula.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Tangkap resit menggunakan ruang kerja mudah alih pengurusan Perbelanjaan

1. Pada peranti mudah alih anda, buka ruang kerja **Pengurusan perbelanjaan**.
2. Pilih **Tangkap resit**.
3. Pilih **Ambil gambar** atau **Pilih imej**.
4. Ikuti salah satu langkah ini:

    - Jika anda memilih **Ambil gambar**, ikuti langkah ini:

        1. Anda dibawa ke kamera pada peranti mudah alih anda supaya anda boleh mengambil gambar resit itu. Apabila anda telah selesai mengambil gambar, pilih **OK** untuk menerima gambar.
        2. Pilihan: Masukkan nama untuk gambar dan masukkan sebarang nota.

    - Jika anda memilih **Pilih imej**, ikuti langkah ini:

        1. Pilih imej dalam senarai.
        2. Pilihan: Masukkan nama untuk imej dan masukkan sebarang nota.

5. Pilih **Selesai**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Masukan dengan pantas perbelanjaan menggunakan ruang kerja mudah alih pengurusan Perbelanjaan
1. Pada peranti mudah alih anda, buka ruang kerja **Pengurusan perbelanjaan**.
2. Pilih **Entri perbelanjaan pantas**.
3. Pilih kategori untuk perbelanjaan. Anda melihat senarai kategori perbelanjaan yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika kategori anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Carian mengikut kategori perbelanjaan atau tukar ke carian mengikut jenis perbelanjaan.
4. Masukkan tarikh transaksi perbelanjaan.
5. Pilihan: Masukkan peniaga untuk perbelanjaan.
6. Masukkan amaun perbelanjaan.
7. Pilih mata wang perbelanjaan. Anda melihat kod mata wang yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 400 mata wang dimuatkan tetapi pembangun boleh mengubah bilangan ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika mata wang anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Cari mengikut mata wang atau tukar ke carian mengikut nama.
8. Pilih **Ambil gambar** atau **Pilih imej**.
9. Ikuti salah satu langkah ini:

    - Jika anda memilih **Ambil gambar**, anda dibawa ke kamera pada peranti mudah alih anda supaya anda boleh mengambil gambar resit. Apabila anda telah selesai mengambil gambar, pilih **OK** untuk menerima gambar.
    - Jika anda memilih **Pilih imej**, pilih imej dalam senarai.

10. Pilih **Selesai**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Luluskan laporan perbelanjaan menggunakan ruang kerja mudah alih pengurusan Perbelanjaan (jika anda menggunakan kemas kini Julai 2017)
1. Pada peranti mudah alih anda, buka ruang kerja **Pengurusan perbelanjaan**.
2. **Kelulusan perbelanjaan** menunjukkan bilangan laporan perbelanjaan yang ditugaskan kepada anda untuk kelulusan. Nombor dikemas kini kira-kira setiap 30 minit. Pilih **Kelulusan Perbelanjaan**.

    Senarai laporan perbelanjaan yang ditugaskan kepada anda untuk kelulusan ditunjukkan.
    
3. Pilih laporan perbelanjaan untuk melihat butiran perbelanjaan untuknya.
4. Pilih perbelanjaan untuk melihat butiran perbelanjaan untuknya. Maklumat yang ditunjukkan untuk perbelanjaan termasuk sebarang resit, tetamu dan butiran perincian.
5. Kembali ke halaman **Laporan perbelanjaan**, pilih untuk melulus atau menolak laporan perbelanjaan.
6. Masukkan sebarang komen untuk tindakan kelulusan.
7. Pilih **Selesai**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Cipta laporan perbelanjaan baharu dan serahkannya untuk kelulusan dengan menggunakan ruang kerja mudah alih pengurusan Perbelanjaan (jika anda menggunakan kemas kini Julai 2017)
1. Pada peranti mudah alih anda, buka ruang kerja **Pengurusan perbelanjaan**.
2. Pilih **Entri perbelanjaan**.
3. Pilih **Laporan baharu** atau pilih laporan perbelanjaan sedia ada dalam senarai.
4. Untuk laporan perbelanjaan baharu, masukkan tujuan dan sebarang maklumat tambahan yang tersedia. Maklumat ini berbeza-beza bergantung pada cara pengurusan perbelanjaan dikonfigurasikan untuk syarikat anda.
5. Pilih **Selesai**.
6. Untuk menambah perbelanjaan sedia ada seperti transaksi kad kredit kepada laporan perbelanjaan, pilih **Lampirkan**.
7. Pilih satu atau lebih perbelanjaan dalam senarai.
8. Pilih **Selesai**.
9. Untuk menambahkan perbelanjaan baharu kepada laporan perbelanjaan, pilih **Perbelanjaan baharu**.
10. Pilih kategori untuk perbelanjaan. Anda melihat senarai kategori perbelanjaan yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika kategori anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Carian mengikut kategori perbelanjaan atau tukar ke carian mengikut jenis perbelanjaan.
11. Pilihan: Masukkan peniaga untuk perbelanjaan.
12. Masukkan tarikh transaksi perbelanjaan.
13. Masukkan amaun perbelanjaan.
14. Pilih mata wang perbelanjaan. Anda melihat kod mata wang yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 400 mata wang dimuatkan tetapi pembangun boleh mengubah bilangan ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika mata wang anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Cari mengikut mata wang atau tukar ke carian mengikut nama.
15. Pilih **Selesai**.
16. Untuk menambah lebih banyak butiran pada perbelanjaan, pilih **Tambah lebih butiran**. Medan yang tersedia bergantung kepada konfigurasi pengurusan perbelanjaan untuk syarikat anda.
17. Jika polisi syarikat memerlukan resit untuk perbelanjaan, pilih **Resit** dan kemudian ikuti langkah ini:

    1. Pilih **Tangkap resit** atau **lampirkan resit**.
    2. Ikuti salah satu langkah ini:

        - Jika anda memilih **Tangkap resit**, ikuti langkah ini:

            1. Pilih **Ambil gambar** atau **Pilih imej**.
            2. Ikuti salah satu langkah ini:

                - Jika anda memilih **Ambil gambar**, ikuti langkah ini:

                    1. Anda dibawa ke kamera pada peranti mudah alih anda supaya anda boleh mengambil gambar resit itu. Apabila anda telah selesai mengambil gambar, pilih **OK** untuk menerima gambar.
                    2. Pilihan: Masukkan nama untuk gambar dan masukkan sebarang nota.

                - Jika anda memilih **Pilih imej**, ikuti langkah ini:

                    1. Pilih imej dalam senarai.
                    2. Pilihan: Masukkan nama untuk imej dan masukkan sebarang nota.

            3.  Pilih **Selesai**.

        - Jika anda memilih **Lampirkan resit**, ikuti langkah ini:

            1.  Pilih satu atau lebih imej dalam senarai.
            2.  Pilih **Selesai**.

    3. Pilih butang **Kembali** untuk kembali ke butiran perbelanjaan..

18. Jika polisi syarikat memerlukan tetamu untuk perbelanjaan, pilih **Tetamu** dan kemudian ikuti langkah ini:

    1. Pilih **Tetamu**, **Tetamu terdahulu** atau **Rakan sekerja**.
    2. Ikuti salah satu langkah ini:

        - Jika anda memilih **Tetamu**, ikuti langkah ini:

            1. Masukkan nama tetamu.
            2. Pilihan: masukkan organisasi dan/atau negara tetamu.
            3. Pilihan: Masukkan gelaran tetamu.
            4. Pilih **Selesai**.

        - Jika anda memilih **Tetamu terdahulu**, ikuti langkah ini:

            1. Pilih satu atau lebih tetamu terdahulu dalam senarai. Anda lihat senarai tetamu terdahulu yang anda telah tambahkan kepada laporan perbelanjaan yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika tetamu terdahulu anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Cari mengikut nama atau bertukar kepada carian mengikut organisasi, negara atau gelaran.
            2. Pilih **Selesai**.

        - Jika anda memilih **Rakan sekerja**, ikuti langkah ini:

            1. Pilih satu atau lebih rakan sekerja dalam senarai. Anda lihat senarai rakan sekerja yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika rakan sekerja anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Carian mengikut nama atau bertukar kepada carian mengikut syarikat atau gelaran.
            2. Pilih **Selesai**.

    3. Pilih butang **Kembali** untuk kembali ke butiran perbelanjaan..

19. Jika polisi syarikat memerlukan perbelanjaan untuk diperincikan, pilih **Perincikan** dan kemudian ikuti langkah ini:

    1. Pilih tarikh pertama untuk perincian.
    2. Pilih **Tambah perincian**.
    3. Pilih subkategori untuk perincian perbelanjaan. Anda lihat senarai subkategori perbelanjaan yang dimuatkan ke dalam aplikasi anda untuk kegunaan luar talian. Secara lalai, 50 item dimuat, tetapi pembangun boleh mengubah nombor ini. Untuk maklumat lanjut, pembangun hendaklah melihat [Platform mudah alih](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Jika subkategori anda tiada dalam senarai, pilih **Carian** untuk melakukan carian dalam talian. Carian mengikut nama subkategori perbelanjaan.
    4. Masukkan amaun transaksi untuk perincian.
    5. Edit tarikh transaksi jika diperlukan.
    6. Pilih **Selesai**.
    7. Ulangi langkah sebelum ini hingga anda selesai menambah semua perincian untuk tarikh yang dipilih.
    8. Untuk hari tambahan, anda boleh memilih **Salin ke hari seterusnya** untuk menyalin perincian ke hari seterusnya. Sebagai alternatif, anda boleh memilih tarikh untuk diperincikan dan kemudian menambah perincian seperti yang anda lakukan untuk tarikh pertama.
    9. Selepas anda selesai memperincikan perbelanjaan, pilih butang **Kembali** untuk kembali ke butiran perbelanjaan.

20. Pilih butang **Kembali** untuk kembali ke halaman **Laporan perbelanjaan**.
21. Ulangi langkah sebelum ini hingga anda selesai menambah semua perbelanjaan.
22. Pilih **Serahkan**.
23. Masukkan sebarang komen untuk pelulus.
24. Pilih **Selesai**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]