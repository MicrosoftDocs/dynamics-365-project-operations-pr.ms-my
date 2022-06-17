---
title: Prestasi API jadual Projek
description: Artikel ini memberikan maklumat tentang penanda aras prestasi API jadual Projek dan mengenal pasti amalan terbaik untuk kegunaan optimum.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911193"
---
# <a name="project-schedule-api-performance"></a>Prestasi API jadual Projek

_**Digunakan Untuk:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Lite - urusan untuk penginvoisan proforma, Project for the web_

Artikel ini memberikan maklumat tentang penanda aras prestasi antara muka pengaturcaraan aplikasi jadual Projek (API) dan mengenal pasti amalan terbaik untuk mengoptimumkan penggunaan.

## <a name="project-scheduling-service"></a>Perkhidmatan Penjadualan Projek
Perkhidmatan Penjadualan Projek ialah perkhidmatan berbilang penyewa yang berjalan dalam Microsoft Azure. Ia direka bentuk untuk meningkatkan interaksi dengan menyediakan pengalaman pantas dan bendalir apabila pengguna mengusahakan projek. Penambahbaikan ini dicapai dengan menerima permintaan perubahan, memproses perubahan itu, kemudian mengembalikan hasil dengan serta-merta. Perkhidmatan berlanjutan kepada Dataverse secara tidak segerak dan tidak menyekat pengguna daripada melakukan operasi lain.

API jadual Projek bergantung pada Perkhidmatan Penjadualan Projek untuk menjalankan permintaan yang diterangkan dengan lebih terperinci dalam bahagian kemudian artikel ini.

API jadual Projek direka bentuk untuk berfungsi dengan entiti struktur pecahan kerja (WBS) berikut:

  - Project
  - Tugas Projek
  - Kebergantungan Tugas Projek
  - Ahli Pasukan Projek
  - Tugasan Sumber
  
Medan di luar kotak dan medan tersuai disokong. Melainkan dinyatakan sebaliknya, semua operasi biasa disokong, seperti cipta, kemas kini dan padam. Untuk mendapatkan maklumat lanjut, lihat [Gunakan API jadual Projek untuk melakukan operasi dan entiti penjadualan](schedule-api-preview.md).

Sebagai sebahagian daripada API jadual Projek, corak unit kerja telah ditambah. Corak ini dikenali sebagai OperationSet dan ia boleh digunakan apabila beberapa permintaan mesti diproses dalam satu transaksi.

Ilustrasi berikut menunjukkan aliran yang akan rakan kongsi alami apabila ciri ini digunakan.

![Dataverse dan aliran perkhidmatan penjadualan projek.](./media/dataverse-project-scheduling-service-flow.png)

**Langkah 1**: Klien membuat panggilan API kepada titik tamat Protokol Data Terbuka (OData) dalam Dataverse untuk mencipta OperationSet.

**Langkah 2**: Selepas OperationSet baharu dicipta, nilai **OperationSetId** akan dikembalikan.

**Langkah 3**: Klien menggunakan nilai **OperationSetId** untuk membuat permintaan API jadual Projek yang lain. Hasilnya ialah permintaan cipta, kemas kini atau padam pada entiti penjadualan. Apabila permintaan ini dibuat, pengesahan metadata sudah selesai. Jika pengesahan gagal, permintaan ditamatkan dan ralat dikembalikan.

**Langkah 4a–4c**: Langkah ini mewakili fasa TERIMA. Klien menghubungi API **ExecuteOperationSetV1**, yang menghantar semua perubahan kepada Perkhidmatan Penjadualan Projek dalam satu kelompok. Perkhidmatan Penjadualan Projek menjalankan pengesahan sendiri pada permintaan dalam kelompok. Sebarang kegagalan pengesahan membuat asal kelompok dan mengembalikan pengecualian kepada pemanggil. Jika kelompok berjaya diterima oleh Perkhidmatan Penjadualan Projek, status OperationSet dikemas kini untuk menunjukkan hakikat bahawa OperationSet sedang diproses oleh Perkhidmatan Penjadualan Projek.

**Langkah 5**: Langkah ini mewakili fasa BERTERUSAN. Perkhidmatan Penjadualan Projek menulis kelompok secara tidak segerak kepada Dataverse dalam transaksi. Jika operasi tulis berjaya, OperationSet ditanda sebagai **Selesai**. Sebarang ralat membatalkan transaksi dan kelompok dan OperationSet ditanda sebagai **Gagal**.

## <a name="performance-methodology"></a>Metodologi prestasi
Masa pelaksanaan ditakrifkan sebagai masa daripada panggilan kepada API **ExecuteOperationSetV1** sehingga Perkhidmatan Penjadualan Projek telah selesai menulis kepada Dataverse. Semua operasi menjalankan gabungan 2,200 kali dan ukuran masa pelaksanaan P99 dilaporkan. Operasi rekod tunggal dan pukal diukur.

Untuk operasi rekod tunggal, OperationSet mengandungi satu permintaan. Untuk operasi pukal, ia mengandungi 20, 50 atau 100 permintaan. Setiap saiz pukal dilaporkan secara berasingan.

Operasi ini berjalan pada pelaksanaan ringan Project Operations UR 15 di Amerika Utara.

## <a name="results"></a>Keputusan
### <a name="create-operations"></a>Cipta operasi
#### <a name="single-record-create-operations"></a>Operasi mencipta rekod tunggal
Jadual berikut menunjukkan masa pelaksanaan bagi penciptaan rekod tunggal. Masa adalah dalam saat.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekod</th>
    <th class="tg-0lax" colspan="2">Masa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ahli pasukan</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Kebergantungan</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operasi mencipta pukal
Jadual berikut menunjukkan masa pelaksanaan bagi penciptaan banyak rekod. Secara khusus, Microsoft mengukur masa pelaksanaan untuk penciptaan 20, 50, dan 100 rekod dalam OperationSet tunggal. Masa adalah dalam saat.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Jenis&nbsp;&nbsp;&nbsp;rekod</th>
    <th class="tg-0lax" colspan="6">Masa</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekod</th>
    <th class="tg-0lax" colspan="2">50 rekod</th>
    <th class="tg-0lax" colspan="2">100 rekod</th>
  </tr>
  <tr>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Kebergantungan</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operasi mencipta pukal pada entiti **Projek** dan **Ahli Pasukan** tidak termasuk dalam jadual ini, kerana masa jalanan untuk operasi tersebut menyerupai masa jalanan apabila API untuk mencipta rekod tunggal dipanggil beberapa kali. API ini akan berjalan dalam Dataverse dengan serta-merta.

Ilustrasi berikut menunjukkan plot masa pelaksanaan untuk entiti **Tugas**, **Tugasan**, dan **Kebergantungan** apabila 20, 50, dan 100 rekod dicipta dan semua medan yang disokong digunakan.

![Cipta graf masa pelaksanaan rekod.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operasi kemas kini
#### <a name="single-record-update-operations"></a>Operasi mengemas kini rekod tunggal
Jadual berikut menunjukkan masa pelaksanaan bagi kemas kini rekod tunggal. Masa adalah dalam saat.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekod</th>
    <th class="tg-0lax" colspan="2">Masa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Medan diperlukan </th>
    <th class="tg-0lax">Semua medan yang disokong</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ahli pasukan</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi kemas kini pada entiti **Tugasan Sumber** dan **Kebergantungan Tugas Projek** tidak disokong.

#### <a name="bulk-update-operations"></a>Operasi mengemas kini pukal
Jadual berikut menunjukkan masa pelaksanaan bagi kemas kini banyak rekod. Secara khusus, Microsoft mengukur masa pelaksanaan untuk kemas kini 20, 50, dan 100 rekod dalam OperationSet tunggal. Masa adalah dalam saat.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Jenis&nbsp;&nbsp;&nbsp;rekod</th>
    <th class="tg-0lax" colspan="6">Masa</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 rekod</th>
    <th class="tg-0lax" colspan="2">50 rekod</th>
    <th class="tg-0lax" colspan="2">100 rekod</th>
  </tr>
  <tr>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
    <th class="tg-0lax">Medan diperlukan</th>
    <th class="tg-0lax">Semua medan yang disokong</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ahli pasukan</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi kemas kini pada entiti **Tugasan Sumber** dan **Kebergantungan Tugas Projek** tidak disokong.

Ilustrasi berikut menunjukkan plot masa pelaksanaan untuk entiti Tugas dan Ahli Pasukan apabila 20, 50, dan 100 rekod dikemas kini dan semua medan yang disokong digunakan.

![Kemas kini graf masa pelaksanaan rekod.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operasi padam
#### <a name="single-record-delete-operations"></a>Operasi memadamkan rekod tunggal
Jadual berikut menunjukkan masa pelaksanaan bagi pemadaman rekod tunggal. Masa adalah dalam saat.

| Jenis rekod | Masa  |
|-------------|-------|
| Tugas        | 20.12 |
| Penugasan  | 10.86 |
| Ahli pasukan | 12.52 |
| Kebergantungan  | 20.89 |

> [!NOTE]
> Operasi padam pada entiti **Projek** tidak disokong.

#### <a name="bulk-delete-operations"></a>Operasi memadam secara pukal
Jadual berikut menunjukkan masa pelaksanaan bagi pemadaman banyak rekod. Secara khusus, Microsoft mengukur masa pelaksanaan untuk pemadaman 20, 50, dan 100 rekod dalam OperationSet tunggal. Masa adalah dalam saat.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekod</th>
    <th class="tg-0lax" colspan="3">Masa</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 rekod</th>
    <th class="tg-0lax">50 rekod</th>
    <th class="tg-0lax">100 rekod</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Ahli pasukan</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Kebergantungan</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi padam pada entiti **Projek** tidak disokong.

Ilustrasi berikut menunjukkan plot masa pelaksanaan untuk entiti **Tugas**, **Tugasan**, **Ahli Pasukan**, dan **Kebergantungan** apabila 20, 50, dan 100 rekod dipadam.

![Padamkan graf masa pelaksanaan rekod.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Pemerhatian
Bagi setiap operasi rekod, API **ExecuteOperationSet** mengambil masa kira-kira 800 milisaat untuk menghantar permintaan kepada Perkhidmatan Penjadualan Projek. Kemudian, Perkhidmatan Penjadualan Projek mengambil masa kira-kira lima saat untuk memproses muatan dan memanggil Dataverse. Baki masa pelaksanaan diluangkan untuk menjalankan logik perniagaan dan menulis data kepada pangkalan data dalam Dataverse.

Apabila 100 rekod dicipta, dikemas kini atau dipadamkan, API **ExecuteOperationSet** mengambil masa kira-kira tiga saat untuk menghantar permintaan kepada Perkhidmatan Penjadualan Projek. Kemudian, Perkhidmatan Penjadualan Projek mengambil masa kira-kira lima saat untuk memproses permintaan dan memanggil Dataverse. Operasi pukal mesti membayar **cukai Perkhidmatan Penjadualan Projek** sekali, untuk semua rekod dalam OperationSet. Oleh itu, operasi pukal mempunyai purata masa pelaksanaan yang jauh lebih rendah daripada operasi rekod tunggal.

## <a name="scenarios"></a>Senario
Jadual berikut menunjukkan masa pelaksanaan apabila API jadual Projek digunakan untuk mencapai senario tertentu. Masa adalah dalam saat.

| Senario                                                                   | Masa  |
|----------------------------------------------------------------------------|-------|
| Cipta projek yang mempunyai 40 tugas.                                      | 36.01 |
| Cipta projek yang mempunyai 40 tugas dan 20 kebergantungan.                  | 38.11 |
| Cipta projek yang mempunyai 40 tugas dan 30 tugasan.                   | 60.17 |
| Cipta projek yang mempunyai 40 tugas, 20 kebergantungan, dan 30 tugasan. | 60.27 |

## <a name="best-practices"></a>Amalan terbaik
Berdasarkan keputusan senario sebelum ini, API melakukan dengan lebih baik dalam keadaan berikut:

  - Kumpulan bersama-sama sebanyak operasi yang mungkin. Purata masa jalanan untuk operasi pukal adalah lebih baik daripada purata masa jalanan untuk operasi rekod tunggal. Apabila bilangan OperationSets yang digunakan lebih kecil, purata masa pelaksanaan akan lebih cepat.
  - Tetapkan atribut minimum yang diperlukan untuk mencapai senario anda sahaja. Memilih tentang jenis medan yang tidak diperlukan termasuk dalam permintaan OperationSet. Medan yang mengandungi kunci asing atau medan gulung atas akan mempengaruhi prestasi secara negatif.
