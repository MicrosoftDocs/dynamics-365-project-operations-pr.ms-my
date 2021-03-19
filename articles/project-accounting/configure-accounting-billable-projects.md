---
title: Konfigurasi perakaunan untuk projek boleh dibil
description: Topik ini menyediakan maklumat tentang pilihan perakaunan untuk projek boleh dibilkan.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4398ef44d4211a2921270bebe38fc92f18503854
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287654"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurasi perakaunan untuk projek boleh dibil

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Dynamics 365 Project Operations menyokong pelbagai pilihan perakaunan untuk projek boleh dibilkan yang merangkumi masa dan bahan serta transaksi harga tetap.

- **Transaksi masa dan bahan** : Transaksi ini diinvoiskan semasa kerja sedang berjalan berdasarkan penggunaan jam, perbelanjaan, barangan atau yuran pada projek. Kos transaksi boleh dipadankan dengan hasil pada setiap transaksi dan projek diinvoiskan apabila kerja berjalan. Hasil projek boleh juga diakrukan pada masa transaksi berlaku. Semasa penginvoisan, hasil dikenal pasti dan jika berkenaan, pendapatan terakru dibalikkan.
- **Transaksi harga tetap**: Transaksi ini diinvoiskan mengikut jadual pengebilan yang berdasarkan kontrak projek. Hasil bagi transaksi harga tetap boleh dikenal pasti pada penginvoisan atau dikira dan disiarkan secara berkala, mengikut kaedah **Kontrak selesai** atau **Peratusan selesai**.

Projek dianggap boleh dibilkan apabila ia dikaitkan dengan satu atau lebih baris kontrak. Baris kontrak projek mentakrifkan sendiri kaedah pengebilan dan jenis transaksi yang dibenarkan.

Sebagai contoh, Fabrikam Robotics telah memenangi kontrak projek dengan Adatum Corporation untuk pengoptimuman peralatan. Adatum akan membayar jumlah tetap $10,000 USD untuk menampung perbelanjaan projek yang ditanggung. Ini ialah kaedah pengebilan harga tetap. Masa dan yuran projek akan dibilkan bagi setiap penggunaan. Ini ialah kaedah pengebilan masa dan bahan. Semua kerja akan dijejak di bawah satu projek yang dinamakan, pengoptimuman peralatan Adatum.

Seorang ahli pasukan projek menyerahkan lapan jam kerja dalam projek pengoptimuman peralatan Adatum. Apabila pengurus projek meluluskan masa ini, sistem menggunakan kaedah pengebilan masa dan bahan untuk mencipta transaksi aktual, invois dan akaun. Transaksi ini tidak akan dimasukkan dalam pengiraan anggaran hasil harga tetap.

Satu lagi ahli pasukan projek menyerahkan perbelanjaan perjalanan untuk $2000.00 USD terhadap projek pengoptimuman peralatan Adatum. Apabila pengurus projek meluluskan serahan ini, sistem menggunakan kaedah pengebilan harga tetap untuk mencipta transaksi aktual dan akaun untuk perbelanjaan projek ini. Pelanggan tidak akan diinvoiskan berdasarkan transaksi ini. Sebaliknya, mereka akan diinvois dengan menggunakan peristiwa pengebilan yang dikonfigurasikan secara berasingan. Transaksi perbelanjaan ini, bersama dengan anggaran perbelanjaan, akan dimasukkan dalam pengiraan anggaran hasil harga tetap.

Prinsip perakaunan untuk transaksi projek ditakrifkan dalam profil kos dan hasil projek. Bagi setiap transaksi projek, sistem menentukan profil kos dan hasil projek yang sesuai dengan menggunakan peraturan profil kos dan hasil projek yang telah dikonfigurasikan.

## <a name="define-project-cost-and-revenue-profiles"></a>Tentukan profil kos dan hasil projek 

Profil kos dan hasil projek menentukan peraturan perakaunan untuk transaksi projek. Profil ini dikonfigurasikan dalam Pengurusan projek dan perakaunan. 

Lengkapkan langkah berikut untuk mencipta profil kos dan hasil projek baharu. 

1. Pergi ke **Pengurusan dan perakaunan projek** > **Persediaan** > **Penyiaran** > **Profil kos dan hasil projek**. 
2. Pilih **Baharu** untuk mencipta profil kos dan hasil projek baharu.
3. Dalam medan **Nama**, masukkan nama dan perihalan ringkas bagi profil.
4. Dalam medan **Kaedah pengebilan**, pilih **Masa dan bahan** atau **Harga tetap**.
5. Kembangkan FastTab **Lejar**. Medan pada tab ini mentakrifkan prinsip perakaunan yang digunakan apabila transaksi projek dijurnalkan dengan menggunakan jurnal integrasi Project Operations dan kemudian diinvois melalui Cadangan invois projek.
6. Pilih maklumat yang sesuai dalam medan berikut pada FastTab **Lejar**:

    - **Siarkan kos – jam**:

       - *Tiada Lejar*: Kos untuk transaksi masa tidak akan disiarkan pada Lejar apabila jurnal integrasi Project Operations disiarkan. Walau bagaimanapun, pihak akauntan boleh menyiarkan kos menggunakan fungsi Siarkan kos pada masa yang lain.
       - **Baki akaun** : Kos untuk transaksi masa akan didebitkan pada jenis akaun Lejar, *Nilai WIP - Kos* dan dikreditkan pada *Akaun peruntukan gaji* dalam persediaan penyiaran Lejar. Pihak akauntan akan menggunakan fungsi Siarkan kos untuk memindahkan kos ini daripada Akaun baki kepada Akaun untung rugi secara berkala.
       - **Untung rugi**: Apabila menyiarkan jurnal integrasi Project Operations, kos transaksi masa akan didebitkan pada jenis akaun Lejar *Kos* dan dikreditkan pada *Akaun peruntukan gaji* yang ditentukan pada tab **Kos** pada halaman **Persediaan penyiaran lejar** ( **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Penyiaran** \> **Persediaan penyiaran lejar**). Ini ialah persediaan yang paling biasa untuk transaksi masa dan bahan.
        - *Jangan sekali-kali Ledger*: Kos untuk transaksi masa tidak akan disiarkan pada Lejar.

    - **Siarkan kos – perbelanjaan**:

         - **Baki akaun**: Apabila menyiarkan jurnal integrasi Project Operations, kos transaksi perbelanjaan akan didebitkan pada jenis akaun Lejar *WIP - Nilai kos* seperti yang ditentukan pada tab **Kos** pada halaman **Persediaan penyiaran lejar** dan dikreditkan pada akaun ofset pada garisan jurnal. Akaun ofset lalai untuk perbelanjaan ditakrifkan dalam **Pengurusan dan perakaunan projek** > **Persediaan** \> **Penyiaran** \> **Akaun ofset lalai untuk perbelanjaan**. Pihak akauntan akan menggunakan fungsi **Siarkan kos** untuk memindahkan kos ini daripada akaun baki kepada akaun untung rugi secara berkala.
        - **Untung rugi**: Apabila menyiarkan jurnal integrasi Project Operations, kos transaksi perbelanjaan akan didebitkan pada jenis akaun Lejar *Kos* seperti yang ditentukan pada tab **Kos** pada halaman **Persediaan penyiaran lejar** dan dikreditkan pada akaun ofset pada garisan jurnal. Akaun ofset lalai untuk perbelanjaan ditakrifkan dalam **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Penyiaran** \> **Akaun ofset lalai untuk perbelanjaan**.
       
    - **Pada penginvoisan akaun**:

        - **Baki akaun**: Apabila menyiarkan cadangan Invois projek, transaksi dalam akaun (peristiwa pengebilan) akan dikreditkan pada jenis akaun Lejar *WIP diinvoiskan - pada akaun* seperti yang ditentukan pada tab **Hasil** pada halaman **Persediaan penyiaran lejar** dan didebitkan pada Akaun baki klien.
         - **Untung rugi**: Apabila menyiarkan cadangan Invois projek, transaksi dalam akaun (peristiwa pengebilan) akan dikreditkan pada jenis akaun Lejar *Hasil diinvoiskan - pada akaun* seperti yang ditentukan pada tab **Hasil** pada halaman **Persediaan penyiaran lejar** dan didebitkan pada Akaun baki klien. Akaun baki pelanggan ditakrifkan dalam **Akaun belum terima** \> **Persediaan** \> **Profil penyiaran pelanggan**.

   Apabila anda mentakrifkan profil penyiaran untuk Kaedah pengebilan masa dan bahan, anda mempunyai pilihan untuk mengakru hasil bagi setiap jenis transaksi (jam, perbelanjaan dan yuran). Jika pilihan **Hasil terakru** ditetapkan kepada **Ya**, transaksi jualan yang tidak dibilkan dalam jurnal integrasi Project Operations akan direkodkan pada lejar am. Nilai jualan didebitkan pada **WIP - akaun nilai jualan** dan dikreditkan pada **Hasil terakru - nilai jualan** yang ditetapkan pada halaman **Persediaan penyiaran lejar**, pada tab **Hasil**. 
  
  > [!NOTE]
  > Pilihan, **Hasil terakru** hanya tersedia apabila transaksi masing-masing jenis **Kos** disiarkan pada akaun untung rugi.
    
7. Kembangkan FastTab **Anggaran**. Medan pada tab ini mentakrifkan tetapan pengiraan untuk anggaran hasil harga tetap. Medan pada tab ini hanya digunakan pada Profil kos dan hasil projek dengan kaedah pengebilan **Harga tetap**.
8. Pilih maklumat yang sesuai dalam medan berikut pada FastTab **Anggaran**:

    - **Prinsip yang digunakan untuk pengiraan penyiapan projek**:

        - **Kontrak yang telah selesai**: Pemadanan kos dan pengiktirafan hasil tidak berlaku sehingga projek tamat. Kos ditunjukkan sebagai WIP dalam baki sehingga projek selesai.
        - **Peratusan selesai**: Hasil terakru dikira dan disiarkan pada lejar pada setiap tempoh berdasarkan peratusan penyiapan projek. Terdapat beberapa kaedah yang tersedia untuk mengira peratusan siap. Kaedah ini boleh dibuat secara automatik berdasarkan konfigurasi, atau manual.
        - **Tiada WIP**: Persediaan ini digunakan untuk projek harga tetap dengan jangka masa yang singkat dan apabila invois dan kos berlaku dalam tempoh yang sama. Dalam kes ini, nilai medan **Penginvoisan pada akaun** pada FastTab **Lejar** ditetapkan secara automatik kepada **Untung rugi** untuk memastikan hasil dikenal pasti semasa penginvoisan. Proses anggaran Hasil tidak akan digunakan untuk profil kos dan hasil projek.

    - **Prinsip yang sepadan**: Medan ini menentukan cara nilai jualan yang dikira (hasil yang terakru) akan disiarkan pada lejar.

        - Dengan menggunakan prinsip **Nilai jualan**, sistem ini akan mengira nilai jualan dengan memadankan kos dan hasil dan kemudian menyiarkannya sebagai jumlah tunggal.
        - Dengan menggunakan prinsip **Pengeluaran dan hasil**, sistem akan membahagikan nilai jualan kepada dalam kos yang terealisasi dan keuntungan yang dikira. Ini disiarkan secara berasingan.

    - **Templat kos**: Membolehkan transaksi projek dihimpun berdasarkan jenis transaksi dan kategori projek serta mentakrifkan peraturan pengiraan peratusan siap untuk kumpulan ini.
    - **Kod tempoh**: Mentakrifkan kekerapan yang anggaran hasil dikira dengannya untuk Profil kos dan hasil projek yang diberikan.
    - **Kategori untuk anggaran**: Digunakan untuk nilai jualan (hasil terakru) yang disiarkan pada Transaksi projek. Pertama, konfigurasikan kategori projek khusus untuk jenis transaksi **Yuran** dan kemudian tetapkan bendera, **Anggarkan** untuk kategori projek ini. Seterusnya, bergantung pada prinsip pemadanan yang dipilih, pilih kategori projek ini dalam nilai **Jualan** atau medan **Keuntungan** dalam Profil kos dan hasil projek.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Contoh konfigurasi untuk Profil kos dan hasil projek

Masa dan bahan – tiada WIP

![Profil kos dan hasil: Masa dan bahan - tiada WIP](media/time-material-no-wip.png)

Masa dan bahan – WIP (hasil)

![Profil kos dan hasil: Masa dan bahan - WIP](media/time-material-with-wip.png)

Harga Tetap – Tiada WIP

![Profil kos dan hasil: Harga tetap - tiada WIP](media/fixed-price-no-wip.png)

Harga tetap – kontrak yang telah selesai

![Profil kos dan hasil: Harga tetap - kontrak yang telah selesai](media/fixed-price-completed-contract.png)

Harga Tetap – peratusan siap

![Profil kos dan hasil: Harga tetap - peratusan siap](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Contoh peristiwa perakaunan untuk contoh Profil kos dan hasil projek.

| Peristiwa Perakaunan                  | Masa dan Bahan - Tiada WIP                       | Masa dan Bahan - WIP                                                                                           | Harga tetap – tiada WIP                                            | Harga tetap – Kontrak yang telah selesai                                                                            | Harga Tetap – Peratusan siap                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Menjurnalkan masa transaksi    | Debit – Kos <br>Kredit –Peruntukan gaji          | Debit - Kos <br>Kredit –Peruntukan Gaji <br>Debit – nilai Jualan WIP <br>Kredit –Hasil Terakru Nilai Jualan                | Debit – Kos <br>Kredit –Peruntukan gaji                         | Debit – Kos <br>Kredit – Peruntukan gaji                                                                    | Debit – Kos <br>Kredit – Peruntukan gaji                       |
| Menjurnalkan transaksi perbelanjaan | Debit – Kos <br>Kredit – Akaun ofset untuk perbelanjaan | Debit – Kos <br>Kredit – Akaun ofset untuk perbelanjaan <br>Debit – nilai Jualan WIP <br>Kredit –Hasil Terakru Nilai Jualan      | Debit –Kos <br>Kredit – Akaun ofset untuk perbelanjaan                 | Debit – Kos<br> Kredit – Akaun ofset untuk perbelanjaan                                                            | Debit – Kos <br>Kredit – Akaun ofset untuk perbelanjaan               |
| Menginvois pelanggan                | Debit –Baki pelanggan <br>Kredit –Hasil diinvois | Debit – Baki pelanggan <br>Kredit – Hasil diinvois <br>Kredit – nilai Jualan WIP Debit – Hasil Terakru Nilai Jualan | Debit – Baki pelanggan <br>Kredit – Hasil diinvois - pada akaun | Debit –Baki pelanggan <br>Kredit – WIP – Diinvois pada akaun                                                  | Debit – Baki pelanggan <br>Kredit – WIP - Diinvois pada akaun    |
| Siarkan Anggaran Hasil             | Tidak berkenaan                                   | Tidak berkenaan                                                                                                    | Tidak Berkenaan                                                  | Debit – Nilai Kos WIP <br>Credit –Kos                                                                         | Debit - WIP - Nilai jualan <br>Kredit – Hasil terakru Nilai jualan |
| Singkirkan                         | Tidak berkenaan                                   | Tidak berkenaan                                                                                                    | Tidak Berkenaan                                                  | Kredit – Nilai Kos WIP <br>Debit – Kos <br>Kredit – Hasil Terakru - Nilai Jualan <br>Debit – WIP Diinvois pada akaun | Debit – WIP – Diinvois pada akaun <br>Kredit – Nilai Jualan WIP     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurasikan peraturan Profil kos dan hasil projek

Peraturan profil kos dan hasil projek menentukan Profil kos dan hasil projek yang mesti digunakan apabila memproses sebarang transaksi projek yang boleh dibilkan. Takrifkan peraturan dengan pergi ke **Pengurusan dan perakaunan projek** \> **Persediaan** \> **Penyiaran** \> **Peraturan profil kos dan hasil projek**.

Peraturan boleh ditakrifkan oleh kontrak projek, kumpulan projek atau oleh projek khusus. Sistem akan sentiasa memilih peraturan kebutiran tertinggi dahulu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]