---
title: Perkara baharu atau diubah dalam Keluaran Kemas kini Project Service Automation 22, V3
description: Topik ini menyenaraikan ciri dan pembetulan yang tersedia dalam Keluaran Kemas kini Project Service Automation 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150994"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, Keluaran Kemas kini 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Kami dengan sukacitanya mengumumkan kemas kini terbaharu untuk aplikasi Project Service Automation untuk Dynamics 365. Keluaran ini menyertakan beberapa penambahbaikan penting kepada kualiti, prestasi dan kebolehgunaan. Keluaran ini serasi dengan Dynamics 365 9.x. Untuk mengemas kini kepada keluaran ini, lawati halaman penyelesaian Pusat Pentadbir untuk Dynamics 365 online untuk memasang kemas kini. Untuk maklumat lanjut, lihat [Pasang, kemas kini atau alih keluar penyelesaian yang diutamakan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Topik ini menyenaraikan ciri dan pembetulan yang baharu atau diubah untuk Project Service Automation V3, Keluaran Kemas kini 22. Versi ini mempunyai nombor binaan V 3.10.33.48 dan secara amnya boleh didapati melalui kemas kini sendiri pada Jun 2020.

## <a name="update-release-22"></a>Keluaran Kemas kini 22

### <a name="bug-fixes"></a>Pembetulan pepijat



**Masa dan Perbelanjaan**

Isu berikut telah dibaiki:

- **Entri masa** tidak ditambah secara automatik dalam Entri masa selepas import.
- Pemilih tarikh grid **Entri masa** tidak mengenali tetapan serantau pengguna.

**Pengurusan Sumber**

Isu berikut telah dibaiki:

- Dalam mod manual, perubahan pada kontur **Tugasan Sumber** tidak dikenali semasa menjana **Keperluan Sumber**.
- **Permintaan Sumber** tidak menyokong status permintaan tersuai.

**Pengurusan Projek**

Isu berikut telah dibaiki:

- Menggunakan klik dua kali pada EstimateGridControl tidak akan menghuraikan nombor format Belanda dengan betul.
- Masa yang diberikan tidak dikemas kini dengan betul apabila tugasan ditukar menggunakan tambahan klien desktop Microsoft Project.
- Grid Penjejakan dan Anggaran Projek memaparkan kod mata wang penjualan yang salah apabila mata wang kontrak berbeza daripada mata wang pelanggan dan organisasi dikonfigurasikan untuk memaparkan kod mata wang dan bukan simbol mata wang.
- Tarikh tamat ahli Pasukan akan menambah satu hari jika jadual waktu kerja adalah 24 jam sehari.
- Pada Jadual Projek, menambahkan Kategori Transaksi kepada tugas tidak mencetuskan simpan automatik.
- Kesalahan berikut ditunjukkan apabila menambahkan ahli pasukan pada Templat Projek: "Keperluan sumber tidak boleh dikaitkan dengan templat projek". 
- Skrip peraturan reben "msdyn.Approval.CanApproveOrReject" memaparkan ralat masa tamat.

**Sales**

Isu berikut telah dibaiki:

- Mesej ralat pengesahan tidak dipaparkan apabila Senarai Harga Kos dipilih dalam carian Senarai Harga pada borang/entiti 'Senarai Harga Projek Sebut Harga Baharu'.
- Menutup sebut harga sebagai dimenangi tidak menavigasi ke kontrak yang dicipta jika BPF yang dilampirkan pada sebut harga berada dalam peringkat akhir.
- Membalikkan **Jualan yang Belum Dibilkan** dikaitkan dengan kos asal apabila entri masa dipanggil semula.
- Selepas memilih butang **Sahkan**, status invois tidak berubah kepada **Disahkan** melainkan invois disegar semula.


[!INCLUDE[footer-include](../includes/footer-banner.md)]