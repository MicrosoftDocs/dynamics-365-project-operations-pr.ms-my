---
title: Laporan perbelanjaan digambarkan semula
description: Topik ini memberikan maklumat mengenai pengalaman yang direka dan digambarkkan semula untuk entri laporan perbelanjaan.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122806"
---
# <a name="expense-reports-reimagined"></a>Laporan perbelanjaan digambarkan semula

Entri laporan perbelanjaan telah direka bentuk semula untuk memudahkan proses dan mengurangkan masa yang diperlukan untuk melengkapkan laporan. Berikut ialah komponen utama pengalaman perbelanjaan baharu:

- Ruang kerja pengurusan perbelanjaan baharu yang membolehkan anda mengakses perbelanjaan wakil anda.
- Satu pengalaman pemadanan penerimaan baharu untuk menunjukkan penerimaan peringkat pengepala yang lebih baik dan memudahkan proses melampirkan resit kepada baris perbelanjaan.
- Grid baca sahaja yang baharu membolehkan anda melihat lebih banyak baris perbelanjaan dan lajur data tambahan. Anda kini boleh melihat semua baris yang diperincikan dan terpisah, bersama dengan perbelanjaan ibu bapa mereka.
- Anak tetingkap dipermudah untuk perbelanjaan pengeditan.
- Mesej ralat, amaran dan dasar yang direka semula untuk menyediakan konteks yang betul dan pemahaman masalah dan cara menyelesaikannya. Kami telah mengalih keluar beberapa mesej yang muncul sebelum pengguna boleh melengkapkan tugas mereka dan menangani masalah tersebut.
- Halaman baharu untuk menentukan medan yang diperlukan, medan pilihan dan medan yang tidak disertakan. Halaman ini membantu mengurangkan bilangan medan yang mesti ditetapkan.
- Wajah dan rasa baharu untuk laporan perbelanjaan, supaya laporan tidak lagi kelihatan seolah-olah telah direka bentuk untuk persona perakaunan.

Untuk menghidupkan pengalaman baharu, gunakan ruang kerja **Pengurusan ciri** untuk menghidupkan ciri **Laporan perbelanjaan yang digambarkan semula**. Apabila anda menghidupkan ciri ini, tindakan berikut berlaku:

- Ruang kerja perbelanjaan sedia ada diganti dengan ruang kerja baharu.
- Item menu baharu untuk keterlihatan medan perbelanjaan ditambah.
- Tiada item menu sedia ada untuk laporan perbelanjaan (halaman semasa) atau medan laporan perbelanjaan dialih keluar.
- Aliran kerja dan sebarang kelulusan masih akan membawa anda ke halaman laporan perbelanjaan sedia ada.

## <a name="getting-started-video-for-new-users"></a>Video mari bermula untuk pengguna baharu

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Pengalaman perbelanjaan dalam video Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (ditunjukkan di atas) termasuk dalam senarai main [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) yang tersedia di YouTube.

## <a name="new-features"></a>Ciri-ciri baru

| Ciri baharu | Penerangan |
|---|----|
| Kebolehlihatan medan perbelanjaan | Halaman persediaan baharu membolehkan anda menentukan medan yang mana patut dinyahdayakan untuk organisasi, medan yang patut diperlukan dan medan yang disyorkan. |
| Medan diperlukan | Konfigurasi mudah baharu membolehkan anda membuat beberapa medan yang diperlukan tanpa perlu menggunakan rangka dasar. |
| Medan pilihan | Halaman kedua untuk medan pilihan ditambah. Dengan cara ini, pekerja tidak akan merasa seolah-olah mereka mesti menetapkan medan, tetapi medan masih boleh diakses dengan mudah. |
| Tambah resit yang tidak dilampirkan | Keupayaan untuk menambah resit yang tidak dilampirkan pada laporan perbelanjaan adalah lebih ketara daripada ruang kerja dan pada laporan perbelanjaan. |
| Pemesejan yang dipertingkatkan | Terdapat keterlihatan yang lebih baik dalam baris perbelanjaan yang mempunyai amaran atau ralat. |
| Pengurangan mesej dalam bar mesej| Bilangan mesej Infolog telah berkurangan dan usaha telah dibuat untuk mengelakkan mesej duplikasi daripada muncul dalam banyak kes. |
| Tindakan biasa yang dikumpulkan bersama | Antara muka dibersihkan dengan penambahan butang tindakan baru untuk kebanyakan tindakan peringkat baris umum dan penambahan butang elipsis (...) untuk pengepala dan tindakan lain yang kurang kerap. |
| Ruang kerja baharu untuk menambahkan keterlihatan | Sebuah ruang kerja baharu yang menyatukan ciri dan pautan yang membolehkan pengguna berpindah ke kawasan yang berbeza. |
| Tambah perbelanjaan dan resit sedia ada semasa penciptaan perbelanjaan | Apabila anda mencipta laporan perbelanjaan, anda boleh menambah semua atau perbelanjaan dan resit yang terpilih. |
| Kalkulator kadar tukaran | Kalkulator kadar tukaran ditambahkan yang membolehkan anda mengira kadar tukaran untuk transaksi berbilang mata wang saku. |
| Simpan dan tambah baris perbelanjaan baharu | Butang **Simpan** dan **Baharu** tersedia apabila perbelanjaan baharu dimasukkan, untuk membantu anda memasukkan baris perbelanjaan dengan cepat. |
| Keterlihatan yang lebih baik ke dalam baris yang diperincikan dan terpisah | Garis yang diperincikan dan terpisah ditambah secara langsung pada senarai perbelanjaan untuk meningkatkan keterlihatan dan membantu anda menentukan sama ada terdapat sebarang ralat dengan mudah. |
| Tunjuk resit semasa pemerincian | Resit boleh ditunjukkan semasa perincian. |

Keluaran awal tertumpu kepada senario entri perbelanjaan. Sebarang semakan laporan perbelanjaan atau senario kelulusan akan terus menggunakan halaman entri perbelanjaan yang sedia ada.

Ciri berikut ditunjukkan pada halaman sedia ada tetapi masih belum ditunjukkan pada halaman baharu. Ciri ini akan diperkenalkan semula dalam beberapa keluaran akan datang:

- Kelulusan
- Kelulusan akaun berbayar dan keupayaan untuk mengedit perakaunan
- Pelbagai titik entri
- Penyepaduan permintaan perjalanan
- Entiti data untuk keterlihatan medan perbelanjaan
- Entri untuk perbelanjaan per-diem
- Aliran kerja peringkat baris
- Sokongan pelulus interim
- Perincian lanjutan
