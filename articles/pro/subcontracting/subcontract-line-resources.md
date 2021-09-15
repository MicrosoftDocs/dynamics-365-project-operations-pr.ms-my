---
title: Sumber baris subkontrak
description: Topik ini menerangkan cara menentukan sumber khusus yang disediakan oleh vendor untuk baris subkontrak tertentu untuk masa.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323382"
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
4. Pada halaman **Pencapaian Baris Subkontrak Baharu**, masukkan maklumat yang diperlukan dan kemudian pilih **Simpan dan Tutup**.

Jadual berikut menerangkan medan pada sumber baris subkontrak.

| Medan |  Penerangan |
| ----- | ------------ |
| Sumber Boleh Ditempah | Pilih sumber boleh ditempah jenis "Pekerja kontrak" yang anda mahu gunakan sebagai sumber pada baris subkontrak. Jika anda belum mencipta sumber boleh ditempah untuk pekerja kontrak lagi, biarkan medan ini kosong. Sumber boleh ditempah dicipta apabila anda menyimpan rekod.  |
| Kenalan | Jika medan **Sumber Boleh Diitempah** adalah kosong, anda boleh mencipta sumber baris subkontrak anda daripada kenalan yang sedia ada. Gunakan carian untuk melihat senarai kenalan aktif dalam sistem. Pilih kenalan untuk vendor subkontrak ini. Kenalan yang anda pilih disahkan apabila anda menyimpan rekod. Jika kenalan yang anda pilih bukan kenalan yang sah, rekod anda tidak akan disimpan. Jika tiada sumber boleh ditempah untuk kenalan yang dipilih, sistem mencipta sumber boleh ditempah untuk kenalan yang dipilih sebelum mencipta sumber baris subkontrak. |
| Pengguna | Jika medan **Sumber Boleh Diitempah** adalah kosong, anda boleh mencipta sumber baris subkontrak dengan memilih pengguna aktif. Gunakan carian untuk melihat senarai pengguna aktif dalam sistem. Jika tiada sumber boleh ditempah untuk pengguna yang dipilih, sistem mencipta sumber boleh ditempah untuk pengguna yang dipilih sebelum sumber baris subkontrak dicipta. |
| Tarikh Mula | Tarikh yang tugasan pekerja subkontrak akan bermula. Jika sumber ini ditempah untuk tempoh yang jatuh sebelum julat tarikh ini, amaran akan berlaku. |
| Tarikh Tamat | Tarikh yang tugasan pekerja subkontrak akan tamat. Jika sumber ini ditempah untuk tempoh yang jatuh selepas julat tarikh ini, amaran akan berlaku. |
| Usaha | Jumlah jam usaha yang akan digunakan oleh pekerja subkontrak pada baris subkontrak ini. Jika sumber ini ditempah melebihi usaha yang mereka diperuntukkan pada sub kontrak ini, amaran akan berlaku. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
