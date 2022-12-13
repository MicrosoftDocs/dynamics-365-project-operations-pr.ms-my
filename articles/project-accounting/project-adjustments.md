---
title: Pelarasan projek
description: Artikel ini menyediakan maklumat mengenai pelarasan projek.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788371"
---
# <a name="project-adjustments"></a>Pelarasan projek

_**Digunakan Pada:** Project Operations untuk senario distok/berasaskan pengeluaran_

## <a name="adjustments-overview"></a>Gambaran keseluruhan pelarasan

Anda boleh mengkonfigurasikan Microsoft Dynamics 365 Project Operations supaya pengguna boleh membuat perubahan pada transaksi yang disiarkan. Anda boleh melaraskan transaksi projek secara individu, atau anda boleh memilih berbilang transaksi pada satu masa dalam senarai semua transaksi projek. Pelarasan projek digunakan, sebagai contoh, untuk mengemas kini status yang boleh dibilkan secara besar-besaran, mengira semula kos selepas perubahan konfigurasi atau mengemas kini sumber pembiayaan.

Pengguna boleh mengakses fungsi pelarasan projek dengan beberapa cara:

- Dengan halaman **Laraskan transaksi** yang boleh diakses daripada **Pengurusan Projek dan Persediaan perakaunan** \> **·**.
- Dengan menggunakan **butang Pelarasan** pada **halaman Transaksi projek yang disiarkan yang boleh diakses daripada** Pengurusan Projek dan **Transaksi** \> **perakaunan**.
- Dengan menggunakan **butang Pelarasan** pada **halaman Transaksi** projek yang disiarkan dalam konteks projek. Halaman ini boleh diakses dari **Pengurusan Projek dan perakaunan** \> **Semua projek**.

Untuk membenarkan pelarasan, anda mesti mendayakan satu atau lebih status transaksi daripada **Pengurusan Projek dan perakaunan Pengurusan Projek dan paramater** \> **perakaunan** pada **tab Umum** di bawah seksyen **Benarkan pelarasan status** transaksi. Contoh status transaksi termasuk transaksi yang disiarkan, transaksi invois atau transaksi yang dihapuskan. Sebarang status transaksi yang ditetapkan kepada **Tidak** akan mempunyai transaksi dalam status tersebut yang tidak akan muncul dalam proses pelarasan sebagai boleh dipilih untuk pelarasan.

Pilihan konfigurasi yang dinamakan **Sentiasa buat transaksi** pelarasan kini tersedia dalam parameter pengurusan Projek dan perakaunan. Anda boleh menyahdayakan pilihan ini untuk mengemas kini transaksi asal dan bukannya membuat transaksi baharu semasa pelarasan dalam subset senario. Telah diumumkan bahawa parameter ini akan ditamatkan pada 1 Mac 2023. Selepas 1 Mac 2023, sistem akan sentiasa berkelakuan seolah-olah pilihan diaktifkan.

## <a name="adjustments-process-flow"></a>Aliran proses pelarasan

Langkah-langkah berikut menunjukkan aliran biasa untuk pelarasan pemprosesan.

1.  **Buka halaman Pelarasan** projek.
2. Pilih **Pilih** untuk mencari transaksi yang memenuhi kriteria jangkaan untuk pelarasan.
3. Dalam senarai urus niaga, pilih semua transaksi atau subset transaksi untuk pelarasan.
4. Pilih **Laraskan** dan ubah suai atribut pada baris. Secara alternatif, jika nilai ditentukan secara manual semasa entri transaksi, anda boleh memilih untuk memasukkan nilai sistem lalai.
5. Senarai transaksi dikembalikan dan tanda semak muncul dalam **lajur Pelarasan** belum selesai untuk menunjukkan tempat perubahan dibuat. Sebarang pelarasan yang mempunyai perubahan belum selesai ditunjukkan pada separuh bawah halaman. Di sana, anda boleh membuat perubahan terperinci tambahan melebihi apa yang ditunjukkan pada halaman sebelumnya.
6. Pilih **Siarkan** untuk menyiarkan transaksi pelarasan.

Bergantung pada konfigurasi, urus niaga baru biasanya dibuat untuk pelarasan.

-  **Medan Status** Invois bagi transaksi asal disetkan kepada **Dilaraskan**.
- Transaksi pembalikan dicipta untuk menterbalikkan transaksi asal dan **medan Status** disetkan kepada **Diselaraskan**.
- Urus niaga baru dicipta yang mempunyai perubahan yang dibuat semasa proses pelarasan.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Memilih berbilang transaksi projek yang disiarkan pada satu masa untuk pelarasan dan nota kredit

Ciri baharu yang diperkenalkan dalam keluaran 10.0.30 membolehkan pemilihan berbilang transaksi untuk pelarasan pada satu masa daripada **halaman Transaksi** projek yang disiarkan.

Sebelum anda boleh menggunakan ciri ini, ia mesti didayakan dalam sistem anda. Pentadbir boleh menggunakan **ruang kerja pengurusan** ciri untuk menyemak status ciri dan mendayakannya jika diperlukan.  **Dalam ruang kerja pengurusan** ciri, cari dan pilih Transaksi projek yang disiarkan berbilang pilihan untuk pelarasan dan nota **kredit, kemudian pilih** **Dayakan sekarang**.

Ciri ini mendayakan kefungsian utama berikut:

- Ia boleh diakses dari halaman transaksi yang disiarkan dalam projek dengan menggunakan butang Pelarasan **sedia ada** .
- Ia membolehkan kawalan pilih berbilang baris pada **halaman Transaksi** projek yang disiarkan. Anda boleh menggunakan penapis pada halaman senarai dan pilih rekod anda sebelum anda memulakan pelarasan.
- Ia melumpuhkan **butang Pelarasan** jika sebarang transaksi tunggal tidak dapat diselaraskan, atau jika anda memilih gabungan nota kredit dan jurnal bersama-sama dan bukannya secara individu.
- Oleh sebab penambahan kawalan pilih berbilang baris, **pautan Kos** komited dalam reben tidak lagi dinyahdayakan jika berbilang baris dipilih.
- Ia menambah mesej amaran berikut: "Anda telah memilih lebih daripada (nombor terpilih) rekod untuk pelarasan. Meneruskan tindakan ini mungkin mengambil sedikit masa. Adakah anda pasti ingin meneruskan tindakan ini?

Ciri ini juga mengalih keluar langkah 2 daripada aliran proses yang diterangkan sebelum ini dalam artikel ini. Oleh itu, sebarang transaksi yang dipilih sebelum **halaman Laraskan transaksi dibuka akan dimasukkan ke dalam senarai transaksi** untuk pelarasan. Anda tidak perlu menggunakan **butang Pilih** untuk mencarinya.

> [!NOTE] 
> Walaupun ciri ini dinyahdayakan, anda masih boleh memilih berbilang rekod untuk pelarasan. Walau bagaimanapun, hanya satu rekod akan kekal dipilih *dan kotak dialog Pilih transaksi* akan **muncul serta-merta** selepas anda memilih untuk membuka pelarasan.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Status transaksi pelarasan yang boleh didayakan atau dinyahdayakan untuk pelarasan

Status berikut boleh didayakan atau dinyahdayakan pada **tab** Umum **halaman parameter** pengurusan dan perakaunan Projek:

- Disiarkan
- Cadangan Invois
- Diinvois
- Anggaran
- Dihapuskan
- Baki permulaan (jam)

## <a name="adjustment-parameters"></a>Parameter pelarasan

Parameter ini disenaraikan pada halaman parameter **pengurusan dan perakaunan Projek pada**  **tab Umum** di bawah **kumpulan Pelarasan** dan akan mengubah suai tingkah laku untuk cara pelarasan diproses. 

| Nama parameter | Description |
|----------------|-------------
| Sentiasa buat transaksi pelarasan | Jika parameter ini didayakan, proses pelarasan akan sentiasa mencipta transaksi pembalikan baharu dan transaksi pelarasan baharu apabila terdapat kesan kewangan atau pelaporan. Jika parameter dinyahdayakan, proses pelarasan akan mengemas kini transaksi asal dan bukannya mencipta pembalikan dan transaksi baru untuk senario seperti kemas kini teks transaksi. |
| Medan Autokemas kini | Jika parameter ini didayakan, sistem akan mengira semula harga kos dan harga jualan. |
| Gunakan tarikh pelarasan sebagai projek baru | Parameter ini digunakan untuk memindahkan transaksi ke tempoh fiskal masa depan sebelum sistem menyokong fungsi ini. Kami tidak mengesyorkan agar anda menggunakannya, kerana ia mengubah tarikh perniagaan transaksi dan akan ditamatkan dalam keluaran akan datang. |
| Benarkan aktiviti tertutup | Biasanya, urus niaga tidak boleh dibuat untuk aktiviti tertutup. Jika parameter ini didayakan, kelakuan itu terlalu besar. Oleh itu, pelarasan boleh dibuat untuk aktiviti tertutup. |
