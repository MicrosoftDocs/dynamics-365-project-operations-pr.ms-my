---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 26, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Project Service Automation Keluaran Kemas kini 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143569"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, Keluaran Kemas kini 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Keluaran Kemas kini Project Service Automation 26, V3. Versi ini mempunyai nombor binaan V3.10.44.59 dan secara amnya tersedia melalui kemas kini dengan sendiri pada Disember 2020.

## <a name="update-release-26"></a>Keluaran Kemas kini 26

### <a name="bug-fixes"></a>Pembetulan pepijat

**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- Pengguna boleh mengubah tugas pada entri masa yang telah diluluskan/diserahkan.
- Ralat "Rujukan Objek Tidak Ditetapkan" apabila menyimpan entri masa.
- Import entri masa daripada tugasan sumber menghasilkan entri masa dengan nilai DateTime yang salah.
- Apabila Project Service Automation dan aplikasi Field Service dipasang, butang **Baharu** dipaparkan dua kali pada bar perintah untuk entri masa dalam aplikasi Field Service.
- Kemas kini sel **Benarkan Unit** dan **Kumpulan Unit** kini berfungsi pada grid **Anggaran Perbelanjaan**.
- Borang **Kemas kini Edit Entri Masa** termasuk **Garis masa**.
- Kelulusan masa untuk entri masa bukan projek menyekat sistem ketika mencari peranan pelulus projek.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- Pengesahan yang ditambah dalam pasang masuk **PostProjectCreate** untuk menyemak keperluan utama sebelum mencipta satu.
- Borang cipta cepat **Ahli Pasukan Projek** memberikan pengecualian rujukan nol jika medan dialih keluar daripada borang.
- Menjana keperluan selama 12 jam lebih daripada 1 tahun akan gagal.
- Pengecualian rujukan nol mesej ralat yang dipertingkatkan semasa penciptaan keperluan sumber.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Pengesahan yang dipertingkatkan untuk menangani pengecualian rujukan nol yang dijana dalam pasang masuk **PreProjectUpdate**.
- Projek yang diterbitkan oleh tambahan Microsoft Project memadam tugasan yang tidak ditugaskan.
- Menambah pengesahan baharu apabila rujukan projek tugas tidak sah disebabkan pengecualian rujukan nol dalam pasang masuk **PreValidateProjectTaskUpdate**.
- Grid ahli pasukan tidak menunjukkan tugasan yang berbeza pada rekod ahli pasukan.
- Menambah pengesahan baharu dan mesej ralat disebabkan pengecualian rujukan nol dalam pasang masuk **PreProjectTaskDelete**.

**Sales**

Isu berikut telah dibaiki:

- Apabila memilih baris berdasarkan projek dalam sebut harga atau kontrak, butang **Cadangan** sepatutnya hanya boleh dilihat apabila memilih baris berdasarkan produk yang dikaitkan dengan produk sedia ada.
- Pisahkan kelayakan **Create_Product** daripada kelayakan **Create_ProjectContract**.
- Memadamkan baris invois menyebabkan kegagalan rujukan nol pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]