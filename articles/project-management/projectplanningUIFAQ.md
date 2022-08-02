---
title: Selesaikan masalah kerja dalam grid Tugas
description: Artikel ini menyediakan maklumat penyelesaian masalah yang diperlukan semasa bekerja dalam grid Tugas.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188243"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Selesaikan masalah kerja dalam grid Tugas 


_**Digunakan Untuk:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Lite - urusan untuk penginvoisan proforma, Project for the web_

Grid Tugas yang digunakan oleh Dynamics 365 Project Operations adalah iframe yang dihoskan dalam Microsoft Dataverse. Hasil daripada penggunaan ini, keperluan khusus mesti dipenuhi untuk memastikan pengesahan, dan kebenaran berfungsi dengan betul. Artikel ini menggariskan isu umum yang boleh memberi kesan kepada keupayaan untuk menjadikan grid atau menguruskan tugas dalam struktur pecahan kerja (WBS).

Isu lazim termasuk:

- Tab **Tugas** pada grid Tugas adalah kosong.
- Apabila membuka projek, projek tidak dimuatkan dan antara muka pengguna (UI) tersekat pada spinner.
- Pentadbiran kelayakan untuk **Project for the Web**.
- Perubahan tidak disimpan apabila anda mencipta, mengemas kini atau memadam tugas.

## <a name="issue-the-task-tab-is-empty"></a>Isu: Tab tugas adalah kosong

### <a name="mitigation-1-enable-cookies"></a>Pengurangan 1: Dayakan kuki

Project Operations memerlukan kuki pihak ketiga didayakan untuk memaparkan struktur pecahan kerja. Apabila kuki pihak ketiga tidak didayakan, selain daripada melihat tugas, anda akan melihat halaman kosong apabila anda memilih **tab Tugas** pada **halaman Projek**.

Untuk penyemak imbas Microsoft Edge atau Google Chrome, prosedur berikut menggariskan cara mengemas kini tetapan penyemak imbas anda untuk mendayakan kuki pihak ketiga.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Buka penyemak imbas Microsoft Edge anda.
2. Di penjuru sebelah kanan bahagian atas, pilih **elipsis** (...), dan kemudian pilih **Tetapan**.
3. Di bawah **Keizinan kuki dan tapak**, pilih **Kuki dan data tapak**.
4. Matikan **Sekat kuki pihak ketiga**.
5. Segar semula pelayar anda. 

#### <a name="google-chrome"></a>Google Chrome

1. Buka penyemak imbas Chrome anda.
2. Di penjuru sebelah kanan bahagian atas, pilih tiga titik menegak (...), dan kemudian pilih **Tetapan**.
3. Di bawah **Privasi dan keselamatan**, pilih **Kuki dan data tapak lain**.
4. Pilih **Benarkan semua kuki**.
5. Segar semula pelayar anda. 

> [!NOTE]
> Jika anda menyekat kuki pihak ketiga, semua kuki dan data tapak daripada tapak lain akan disekat, sekalipun tapak itu dibenarkan pada senarai pengecualian anda.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Pengurangan 2: Sahkan titik tamat PEX telah dikonfigurasikan dengan betul

Project Operations memerlukan parameter projek merujuk Titik Tamat PEX. Titik tamat ini diperlukan untuk berkomunikasi dengan perkhidmatan yang digunakan untuk memaparkan struktur pecahan kerja. Jika parameter tidak didayakan, anda akan menerima ralat, "Parameter projek tidak sah". Untuk mengemas kini titik tamat PEX, lengkapkan langkah berikut.

1. Tambah medan **Titik Tamat PEX** pada halaman **Parameter Projek**.
2. Kenal pasti jenis produk yang anda gunakan. Nilai ini digunakan apabila Titik tamat PEX ditetapkan. Selepas pengambilan, jenis produk sudah ditentukan dalam Titik tamat PEX. Simpan nilai itu.
3. Kemas kini medan dengan nilai berikut: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Jadual berikut menyediakan parameter jenis yang sepatutnya digunakan berdasarkan pada jenis produk.

      | **Jenis produk**                     | **Parameter Jenis** |
      |--------------------------------------|--------------------|
      | Project for the Web pada org Lalai   | jenis=0             |
      | Project for the Web pada org bernama CDS | jenis=1             |
      | Project Operations                   | jenis=2             |

4. Alih keluar medan daripada halaman **Parameter Projek**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigasi 3: log masuk ke project.microsoft.com

Dalam pelayar anda, buka tab baharu, pergi ke project.microsoft.com dan log masuk dengan peranan pengguna yang anda gunakan untuk mencapai Project Operations. Adalah penting bahawa hanya satu pengguna yang akan log masuk ke produk Microsoft dalam penyemak imbas. Mesej ralat "login.microsoftonline.com enggan menyambung" paling kerap berlaku apabila lebih daripada satu pengguna log masuk, seperti yang ditunjukkan dalam ilustrasi berikut.

![Pilih halaman daftar masuk akaun yang menunjukkan bahawa dua pengguna log masuk.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Isu: projek tidak dimuatkan dan UI tersekat pada spinner

Untuk tujuan pengesahan, pop timbul mesti didayakan untuk grid Tugas untuk dimuatkan. Jika pop timbul tidak didayakan, skrin akan tersekat pada pemuatan spinner. Grafik berikut menunjukkan URL dengan label pop timbul yang disekat dalam bar alamat, yang mengakibatkan pemintal tersekat ketika cuba memuatkan halaman. 

   ![Spinner yang tersekat dan pop timbul disekat.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Pengurangan 1: Dayakan pop timbul

Apabila projek anda tersekat pada spinner, berkemungkinan pop timbul tidak didayakan.

#### <a name="microsoft-edge"></a>Microsoft Edge

Terdapat dua cara untuk mendayakan pop timbul dalam pelayar Edge anda.

1. Dalam pelayar Edge anda, pilih pemberitahuan di kanan atas pelayar.
2. Pilih **Sentiasa benarkan pop timbul dan hala semula daripada** persekitaran Dataverse khusus.
 
     ![Tetingkap pop timbul yang disekat.](media/enablepopups.png)

Selain itu, anda juga boleh melengkapkan langkah berikut:

1. Buka penyemak imbas Microsoft Edge anda.
2. Di sudut kanan atas, pilih **elipsis** (...), dan kemudian pilih **Tetapan** > **Keizinan tapak** > **Pop timbul dan hala semula**.
3. Matikan togol **Pop timbul dan hala semula** untuk menyekat pop timbul atau hidupkan togol untuk membenarkan pop timbul pada peranti anda.
4. Selepas anda mendayakan pop timbul, segar semula pelayar anda. 

#### <a name="google-chrome"></a>Google Chrome
1. Buka penyemak imbas Chrome anda.
2. Navigasi ke halaman pop timbul disekat.
3. Dalam bar alamat, pilih **Pop timbul disekat**.
4. Pilih pautan untuk pop timbul yang anda mahu lihat.
5. Selepas anda mendayakan pop timbul, segar semula pelayar anda. 

> [!NOTE]
> Untuk sentiasa melihat pop timbul bagi tapak, pilih **Sentiasa benarkan pop timbul dan hala semula daripada [tapak]** dan kemudian pilih **Selesai**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Isu 3: Pentadbiran kelayakan untuk Project for the Web

Project Operations bergantung pada perkhidmatan penjadualan luaran. Perkhidmatan ini memerlukan pengguna mempunyai beberapa peranan yang diberikan yang membolehkan mereka membaca dan menulis kepada entiti yang berkaitan dengan WBS. Entiti ini termasuklah tugas projek, tugasan sumber dan kebersandaran tugas. Jika pengguna tidak dapat memaparkan WBS apabila mereka menavigasi ke **tab Tugas**, ia mungkin kerana **Project** for **Project Operations** belum didayakan. Pengguna mungkin menerima sama ada ralat peranan keselamatan atau ralat berkaitan dengan penafian akses.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Pengurangan 1: Sahkan peranan keselamatan pengguna aplikasi dan pengguna akhir

1. Pergi ke **Tetapan** > **Keselamatan** > **Pengguna** > **Pengguna Aplikasi**.  

   ![Pembaca aplikasi.](media/applicationuser.jpg)
   
2. Klik dua kali pada rekod pengguna aplikasi untuk mengesahkan:

     - Pengguna mempunyai capaian kepada projek. Anda boleh melakukan ini dengan mengesahkan bahawa pengguna mempunyai peranan keselamatan **Pengurus Projek**.
     - Pengguna aplikasi Microsoft Project wujud dan dikonfigurasikan dengan betul.
 
3. Jika pengguna ini tidak wujud, cipta rekod pengguna baharu. 
4. Pilih **Pengguna Baharu**, ubah borang entri ke **Pengguna Aplikasi** dan kemudian tambah **ID Aplikasi**.

   ![Butiran pengguna aplikasi.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Isu 4: Perubahan tidak disimpan apabila anda mencipta, mengemas kini atau memadam tugas

Apabila anda membuat satu atau lebih kemas kini ke WBS, perubahan gagal dan tidak disimpan. Ralat berlaku dalam grid jadual dengan mesej yang menyatakan, "Perubahan terkini yang anda buat tidak dapat disimpan".

### <a name="mitigation-1-validate-the-license-assignment"></a>Pengurangan 1: Sahkan penugasan lesen

1. Sahkan bahawa pengguna telah ditugaskan lesen yang betul dan perkhidmatan didayakan dalam rancangan perkhidmatan untuk butiran lesen.  
2. Sahkan bahawa pengguna boleh membuka **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Pengurangan 2: Konfigurasi pengesahan bagi pengguna aplikasi Project
1. Sahkan bahawa pengguna aplikasi Project telah dicipta.
2. Gunakan peranan keselamatan berikut kepada pengguna:
  
  - Pengguna atau Pengguna Asas Dataverse
  - Sistem Project Operations
  - Sistem Projek
  - Sistem Dwi tulis Project Operations. Peranan ini diperlukan untuk senario pelaksanaan berasaskan sumber/bukan stok bagi Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
