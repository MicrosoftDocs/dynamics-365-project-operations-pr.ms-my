---
title: Sumber baris subkontrak
description: Topik ini menerangkan cara menentukan sumber khusus yang disediakan oleh vendor untuk baris subkontrak tertentu untuk masa.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558468"
---
# <a name="subcontract-line-resources"></a>Sumber baris subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, vendor boleh menentukan sumber yang akan digunakan untuk membekalkan kapasiti sumber yang dibeli pada baris subkontrak untuk masa.

## <a name="create-subcontract-line-resources"></a>Cipta sumber baris subkontrak

Untuk mencipta sumber baris subkontrak, lengkapkan langkah berikut.

1. Pada anak tetingkap navigasi, pilih **Subkontrak** dan buka subkontrak yang ingin anda usahakan.
2. Buka baris subkontrak untuk masa yang anda mahu tentukan sumber vendor.
3. Pada tab **Sumber Baris Subkontrak**, dalam subgrid, pilih **+ Sumber Baris Subkontrak Baharu**.
4. Pada halaman **Sumber Baris Subkontrak Baharu**, masukkan maklumat yang diperlukan dan kemudian pilih **Simpan dan Tutup**.

Jadual berikut menerangkan medan pada sumber baris subkontrak.

| Medan | Penerangan | Kesan kefungsian |
| ----- | ----------- | ----------------- |
| Sumber Boleh Ditempah | Pilih sumber boleh ditempah bagi jenis **Pekerja kontrak** yang anda ingin gunakan sebagai sumber pada baris subkontrak.| Jika anda belum mencipta sumber boleh ditempah untuk pekerja kontrak, biarkan medan ini kosong. Sumber boleh ditempah akan dicipta apabila anda menyimpan rekod.  |
| Kenalan | Anda boleh mencipta sumber baris subkontrak anda daripada kenalan sedia ada. Gunakan carian untuk melihat senarai kenalan aktif dalam sistem. Pilih kenalan untuk vendor subkontrak ini. Jika kenalan yang anda pilih bukan kenalan yang sah untuk vendor pada subkontrak, rekod sumber baris subkontrak tidak akan disimpan.| Jika tiada sumber boleh ditempah untuk kenalan yang dipilih, sistem mencipta sumber boleh ditempah untuk kenalan yang dipilih sebelum mencipta sumber baris subkontrak. |
| Pengguna | Anda boleh mencipta sumber baris subkontrak dengan memilih pengguna aktif. Gunakan carian untuk melihat senarai pengguna aktif dalam sistem.| Jika tiada sumber boleh ditempah untuk pengguna yang dipilih, sistem mencipta sumber boleh ditempah untuk pengguna yang dipilih sebelum sumber baris subkontrak dicipta. |
| Tarikh Mula | Tarikh yang tugasan pekerja subkontrak akan bermula.| Jika sumber ini ditempah untuk tempoh yang jatuh sebelum julat tarikh ini, amaran akan berlaku. |
| Tarikh Tamat | Tarikh yang tugasan pekerja subkontrak akan tamat.| Jika sumber ini ditempah untuk tempoh yang jatuh selepas julat tarikh ini, amaran akan berlaku. |
| Usaha | Jumlah bilangan bagi jam usaha yang akan dihabiskan oleh pekerja kontrak pada baris subkontrak ini.| Jika sumber ini ditempah di luar usaha yang diperuntukkan ke atas subkontrak ini, amaran akan berlaku. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
