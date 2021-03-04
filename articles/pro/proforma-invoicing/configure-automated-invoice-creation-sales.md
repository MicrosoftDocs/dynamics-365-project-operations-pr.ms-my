---
title: Konfigurasi penciptaan invois automatik - ringan
description: Topik ini menyediakan maklumat tentang mengkonfigurasi penciptaan automatik invois proforma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176577"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Konfigurasi penciptaan invois automatik - ringan
 
_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Anda boleh mengkonfigurasikan penciptaan invois automatik dalam Dynamics 365 Project Operations. Sistem mencipta invois draf proforma berdasarkan jadual invois untuk setiap kontrak projek dan baris kontrak. Jadual invois dikonfigurasikan pada peringkat baris kontrak. Setiap baris pada kontrak boleh mempunyai jadual invois yang berbeza, atau jadual invois yang sama boleh dimasukkan pada setiap baris kontrak.

Apabila anda mencipta invois, sistem sentiasa mencipta sekurang-kurangnya satu invois bagi setiap kontrak projek. Dalam sesetengah kes, mungkin terdapat berbilang invois yang dicipta.

Contohnya, jika kontrak mempunyai berbilang pelanggan, bilangan invois yang sama akan dicipta sebagai bilangan pelanggan yang mempunyai transaksi boleh dibilkan ke invois pada kontrak projek tersebut.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Memahami cara transaksi dimasukkan pada invois 

Kadang kala, setiap baris kontrak berasaskan projek menentukan jadual invois yang berasingan. Sebagai contoh, perkhidmatan pelaksanaan untuk kontrak Adatum mempunyai baris kontrak berikut:

- Kerja prototaip iaitu harga tetap dengan dua pencapaian yang dicipta secara manual.
- Kerja pelaksanaan yang termasuk Masa dan akan dibilkan dua minggu sekali pada hari Isnin.
- Perbelanjaan ditanggung yang perlu dibilkan setiap bulan pada hari Isnin pertama setiap bulan.

Jadual invois ditakrifkan pada setiap dua item baris ini ini kelihatan seperti jadual berikut:

| Baris kontrak | Tarikh jalanan invois | Tarikh penggalan transaksi | Tarikh pencapaian | Jumlah pencapaian |
| --- | --- | --- | --- | --- |
| Kerja prototaip | 5 Oktober, Isnin | - | 5 Oktober, Isnin | 5000 USD |
| - | 3 November, Selasa | - | 3 November, Selasa | 12,000 USD |
| Kerja pelaksanaan | 5 Oktober, Isnin | 4 Oktober, Ahad | - | - |
| - | 19 Oktober, Isnin | 18 Oktober, Ahad | - | - |
| - | 2 November, Isnin | 1 November, Ahad | - | - |
| - | 16 November, Isnin | 15 November, Ahad | - | - |
| Perbelanjaan yang ditanggung | 5 Oktober, Isnin | 4 Oktober, Ahad | - | - |
| - | 2 November, Isnin | 1 November, Ahad | - | - |

Dalam contoh ini apabila penginvoisan automatik berjalan pada:

- **4 Oktober atau pada sebarang tarikh sebelum**: Tiada invois dijana untuk kontrak ini kerana jadual **Jadual Invois** untuk setiap baris kontrak ini tidak memanggil 4 Oktober, Ahad sebagai tarikh jalanan invois.
- **5 Oktober Isnin**: Satu invois dijana untuk:

    - Kerja prototaip yang termasuk pencapaian, jika ia ditandakan sebagai **Sedia untuk Invois**.
    - Kerja pelaksanaan yang merangkumi semua transaksi Masa yang dicipta sebelum tarikh tamat transaksi pada 4 Oktober, Ahad, yang ditandakan sebagai **Sedia untuk Invois**.
    - Perbelanjaan yang ditanggung yang merangkumi semua transaksi Perbelanjaan yang dicipta sebelum tarikh tamat transaksi pada 4 Oktober, Ahad, yang ditandakan sebagai **Sedia untuk Invois**.
  
- **Pada 6 Oktober atau pada sebarang tarikh sebelum 19 Oktober**: Tiada invois dijana untuk kontrak ini oleh kerana jadual **Jadual Invois** untuk setiap baris kontrak ini tidak memanggil 6 Oktober sebagai tarikh sebelum 19 Oktober sebagai tarikh jalanan invois.
- **19 Oktober, Isnin**: Satu invois dijana untuk kerja pelaksanaan yang merangkumi semua transaksi Masa yang dicipta sebelum tarikh tamat transaksi pada 18 Oktober, Ahad, yang ditandakan sebagai **Sedia untuk Invois**.
- **2 November Isnin**: Satu invois dijana untuk:

    - Kerja pelaksanaan yang merangkumi semua transaksi Masa yang dicipta sebelum tarikh tamat transaksi pada 1 November, Ahad, yang ditandakan sebagai **Sedia untuk Invois**.
    - Perbelanjaan yang ditanggung yang merangkumi semua transaksi Perbelanjaan yang dicipta sebelum tarikh tamat transaksi pada 1 November, Ahad, yang ditandakan sebagai **Sedia untuk Invois**.

- **3 November, Selasa**: Satu invois dijana untuk kerja prototaip yang termasuk pencapaian untuk 12000 USD, jika ia ditanda sebagai **Sedia untuk Invois**.

## <a name="configure-automatic-invoicing"></a>Konfigurasikan penginvoisan automatik

Lengkapkan langkah yang berikut untuk mengkonfigurasikan jalanan invois automatik.

1. Dalam **Operasi Projek**, pergi ke **Tetapan** > **Persediaan Invois Berulang**.
2. Cipta kerja kelompok dan namakannya **Operasi Projek Mencipta Invois**. Nama kerja kelompok mesti termasuk perkataan terma "cipta invois".
3. Dalam medan **Jenis Kerja**, pilih **Tiada**. Secara lalai, medan **Kekerapan Harian** dan **Adalah Aktif** ditetapkan kepada **Ya**.
4. Pilih **Jalankan Aliran Kerja**. Dalam kotak dialog **Cari Rekod**, anda akan melihat tiga aliran tugas:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Pilih **ProcessRunCaller**, kemudian pilih **Tambah**.
6. Dalam kotak dialog seterusnya, pilih **OK**. Aliran tugas **Tidur** diikuti dengan aliran tugas **Proses**. 

> [!NOTE]
> Anda juga boleh memilih **ProcessRunner** dalam langkah 5. Kemudian, apabila anda pilih **OK**, aliran tugas **Proses** diikuti oleh aliran kerja **Tidur**.

Aliran kerja **ProcessRunCaller** dan **ProcessRunner** mencipta invois. **ProcessRunCaller** memanggil **ProcessRunner**. **ProcessRunner** ialah aliran kerja yang sebenarnya mencipta invois. Aliran kerja merangkumi semua baris kontrak yang perlu dicipta invois, dan mencipta invois untuk baris tersebut. Untuk menentukan baris kontrak yang perlu dicipta invois, kerja dilihat pada tarikh jalanan invois untuk baris kontrak. Jika baris kontrak milik satu kontrak yang mempunyai tarikh jalanan invois sama, transaksi digabungkan ke dalam satu invois yang mempunyai dua baris invois. Jika tiada transaksi untuk mencipta invois, kerja melangkau mencipta invois.

Selepas **ProcessRunner** selesai berjalan, ia memanggil **ProcessRunCaller**, memberikan masa akhir, dan ditutup. **ProcessRunCaller** kemudian memulakan pemasa yang berjalan 24-jam dari tarikh akhir khusus. Pada penghujung pemasa, **ProcessRunCaller** ditutup.

Kerja proses kelompok untuk mencipta invois adalah kerja berulang. Jika proses kelompok ini berjalan banyak kali, berbilang tika kerja dicipta dan menyebabkan ralat. Maka, anda perlu memulakan proses kelompol hanya satu kali, dan kemudian mulakan semula jika ia berhenti berjalan.

> [!NOTE]
> Penginvoisan kelompok dalam Project Operations hanya berjalan untuk baris kontrak projek yang dikonfigurasikan oleh jadual invois. Baris kontrak dengan kaedah pengebilan harga tetap mesti mempunyai pencapaian yang dikonfigurasikan. Baris kontrak projek dengan kaedah pengebilan masa dan bahan akan memerlukan persediaan jadual invois berdasarkan tarikh.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]