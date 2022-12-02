---
title: Urus bakal pelanggan
description: Artikel ini memberikan maklumat tentang mengurus bakal pelanggan berasaskan projek.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 080f53ee2f800b8433d055525852f5c2e21aab77
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920209"
---
# <a name="manage-leads"></a>Urus bakal pelanggan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Bakal pelanggan berasaskan projek boleh diuruskan dan layak dalam Project Operations. Proses pengurusan bakal pelanggan termasuk mewujudkan bakal pelanggan berasaskan kerja dan melayakkan bakal pelanggan itu. 

## <a name="project-sales-leads"></a>Bakal pelanggan jualan projek

Dalam bahagian **Jualan**, dalam anak tetingkap navigasi kiri, buka halaman senarai **Bakal Pelanggan** untuk melihat senarai semua rekod bakal pelanggan dalam sistem. Senarai bakal pelanggan ditunjukkan adalah berasaskan kerja dan jenis bakal pelanggan lain yang boleh dicipta jika anda juga mempunyai aplikasi Dynamics 365 Sales atau Dynamics 365 Field Service.

Anda boleh mencipta pandangan ditapis untuk hanya melihat bakal pelanggan berasaskan projek dengan mencipta penapis pada nilai **Jenis**. Contohnya, anda boleh memilih untuk menunjukkan hanya bakal pelanggan berasaskan kerja.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Cipta bakal pelanggan baharu untuk urusan berasaskan projek

Apabila bakal pelanggan berasaskan projek layak, peluang dan akaun dicipta. Peluang berasaskan projek adalah titik permulaan untuk aktiviti mengejar jualan dalam fasa Peluang. Peluang berasaskan projek mempunyai keupayaan unik yang diperlukan untuk menjual kerja projek. Keupayaan ini termasuk:

- Masa dan bahan serta kaedah Pengebilan Harga Tetap
- Senarai harga berbilang tarikh kuat kuasa untuk sumber manusia, perbelanjaan dan bahan yang dikenakan ke atas projek

Untuk bakal pelanggan yang layak mencipta peluang secara automatik, tetapkan atribut **Jenis** ke **Berasaskan kerja** apabila anda mencipta bakal pelanggan. Jika anda memilih jenis berbeza, bakal pelanggan tidak akan mencipta peluang berasaskan projek apabila ianya layak. Jika peluang berasaskan projek tidak dicipta, keupayaan projek tertentu tidak akan tersedia dalam proses jualan hiliran.

Jadual berikut termasuk maklumat medan yang penting untuk bakal pelanggan dan implikasi hiliran medan tersebut.
 
| **Medan** | **Lokasi** | **Perihalan** | **Kesan hiliran** |
| --- | --- | --- | --- |
| Topik | Tab umum | Medan teks ini hendaklah mengandungi description ringkas tentang urusan. | Topik bakal pelanggan akan lalai sebagai topik Peluang dan Nama Sebut Harga dan kontrak Projek. |
| Jenis | Tab umum | Medan set pilihan ini mempunyai pilihan berikut:</br>- -Berasaskan kerja (tersedia hanya apabila Project Operations dipasang)</br>- Berasaskan item (tersedia hanya apabila Project Operations and Sales dipasang)</br>- Berasaskan perkhidmatan penyelenggaraan (tersedia apabila Field Service dipasang) | Apabila nilai medan ini ditetapkan ke **Berasaskan kerja** pada bakal pelanggan, bakal pelanggan layak untuk mencipta peluang berasaskan Projek. Peluang berasaskan projek diperlukan untuk mendayakan semua sambungan dan kefungsian khusus projek dalam proses jualan hiliran untuk urusan ini. |
| Nama pertama | Tab umum | Nama pertama kenalan prospek | Apabila bakal pelanggan layak, akaun, kenalan dan peluang dicipta. Nama pertama kenalan adalah nilai yang ditetapkan di sini. |
| Nama keluarga | Tab umum | Nama akhir kenalan prospek | Apabila bakal pelanggan layak, akaun, kenalan dan peluang dicipta. Nama akhir kenalan adalah nilai yang ditetapkan di sini. |
| Syarikat | Tab umum | Nama syarikat pelanggan prospek | Apabila bakal pelanggan layak, akaun, kenalan dan peluang dicipta. Nama akaun yang mencipta nilai yang ditetapkan di sini. |
| Mata wang | Tab butiran | Mata wang pelanggan prospek | Apabila bakal pelanggan layak, akaun, kenalan dan peluang dicipta. Mata wang akaun dicipta adalah nilai yang ditetapkan di sini. |

## <a name="qualify-a-new-project-based-lead"></a>Layakkan bakal pelanggan berasaskan projek baharu

Bakal pelanggan yang mempunyai nilai **Jenis** ditetapkan ke **Berasaskan kerja** dipanggil bakal pelanggan berasaskan projek. Apabila bakal pelanggan berasaskan projek layak, berikut dicipta:

- Akaun yang menggunakan medan **Syarikat** daripada bakal pelanggan.
- Rekod kenalan yang berkaitan dengan akaun berasaskan pada nilai dalam medan **Nama Pertama** dan **Nama Akhir** pada bakal pelanggan.
- Peluang berasaskan projek yang mempunyai medan **Jenis** ditetapkan kepada **Berasaskan kerja**.

Untuk maklumat terperinci tentang bakal pelanggan yang layak, lihat [Pelanggan yang layak atau tukar](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Kelayakan bakal pelanggan dan maklumat entiti sah 

Apabila anda menjalankan Project Operations menggunakan mod pelaksanaan, Project Operations untuk senario berasaskan sumber/bukan stok, setiap pelanggan dan peluang akan memerlukan set medan **Syarikat Pemilik**. Syarikat pemilik adalah sebuah entiti sah dalam organisasi anda yang memiliki penghantaran projek. Setiap pelanggan atau akaun dengan jenis perhubungan pelanggan mesti mempunyai set nilai medan **Syarikat Pemilik** ditetapkan kepada entiti sah yang membuat kontrak dan berunding dengan pelanggan ini. Pelanggan hanya boleh berada dalam satu entiti sah.

Apabila bakal pelanggan layak, rekod pelanggan dan peluang yang dicipta akan mempunyai medan **Syarikat Pemilik** ditetapkan kepada rekod sumber boleh ditempah syarikat pengguna semasa.

Jika rekod sumber boleh ditempah pengguna semasa adalah kosong kemudian nilai medan **Syarikat Pemilik** pada rekod pengguna digunakan untuk melalaikan rekod pelanggan dan peluang.

## <a name="business-process-flow-for-project-based-deals"></a>Aliran proses perniagaan untuk urusan berasaskan projek

Aliran proses perniagaan berikut disokong untuk urusan berasaskan projek dalam Project Operations:

- Bakal pelanggan ke proses perniagaan Peluang
- Proses jualan Peluang

Bakal pelanggan ke proses perniagaan Peluang menyokong peringkat berikut:

| Nama peringkat | Entiti yang dipetakan | Fungsi |
| --- | --- | --- |
| Layakkan | Bakal Pelanggan | Layakkan bakal pelanggan untuk mencipta akaun, kenalan dan peluang. |
| Bangunkan | Peluang | Membangunkan peluang untuk menambah lebih banyak maklumat tentang kerja yang terlibat, pemegang amanah utama dan pertandingan. |
| Cadangkan | Peluang | Membangunkan cadangan dan mendapatkan kelulusan daripada pasukan semakan dalaman. |
| Tutup | Peluang | Memenangi peluang untuk menutup urusan. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]