---
title: Gambaran keseluruhan pengiktirafan hasil
description: Topik ini memberikan maklumat tentang pengiktirafan hasil dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278879"
---
# <a name="revenue-recognition-overview"></a>Gambaran keseluruhan pengiktirafan hasil

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Dalam Dynamics 365 Project Operations, prinsip pengiktirafan hasil berbeza-beza berdasarkan pada kaedah pengebilan terpilih untuk projek atau bahagian projek. Topik ini memberikan maklumat tentang pengiktirafan hasil dalam Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaksi dikira menggunakan kaedah pengebilan masa dan bahan

- Kos dan pengiktirafan hasil disambungkan. Kos transaksi dan jualan yang belum dibilkan diposkan menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).
- Kos projek dan profil hasil menentukan sama ada transaksi jualan yang belum dibilkan disiarkan kepada lejar umum. Jika **Hasil akruan** dipilih, sistem menggunakan akaun **Nilai jualan WIP** dan **Nilai jualan hasi terakru** semasa penyiaran. Berikut ialah sebuah contoh bagi kaedah ini.  

  | Jenis transaksi | Debit/Kredit | Amaun |
  | --- | --- | --- |
  | Nilai Jualan WIP | Debit | 100 |
  | Hasil jualan hasi terakru | Kredit | 100 |

- Hasil diktiraf semasa penginvoisan. Sistem ini menggunakan akaun **Hasil Invois** semasa penyiaran. Berikut ialah sebuah contoh bagi kaedah ini.  

  | Jenis transaksi | Debit/Kredit | Amaun |
  | --- | --- | --- |
  | Baki pelanggan | Debit | 120 |
  | Cukai jualan boleh bayar | Kredit | 20 |
  | Hasil Diinvois | Kredit | 100 |

- Jika hasil terakru apabila jualan belum dibilkan disiarkan, sistem akan mengundurkan hasil terakru pada invois.

  | Jenis transaksi | Debit/Kredit | Amaun |
  | --- | --- | --- |
  | Nilai Jualan WIP | Kredit | 100 |
  | Hasil jualan hasi terakru | Debit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaksi dikira menggunakan kaedah pengebilan harga tetap

- Kos dan pengiktirafan hasil diasingkan. Kos transaksi diposkan menggunakan [Jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Transaksi jualan belum dibilkan tidak dicipta.
- Hasil boleh diiktiraf semasa penginvoisan jika kos projek dan profil hasil telah menetapkan **Prinsip digunakan untuk pengiraan penyiapan projek** kepada **Tiada WIP**. Hanya gunakan kaedah ini untuk projek jangka pendek yang mudah.
- Hasil boleh diiktiraf menggunakan anggaran hasil harga tetap, dengan sama ada kaedah **Kontrak siap** atau **Pengiktirafan hasil siap peratus**.

## <a name="additional-resources"></a>Sumber tambahan
[Konfigurasi perakaunan untuk artikel projek boleh dibil](../project-accounting/configure-accounting-billable-projects.md)

[Projek anggaran hasil harga tetap](rev-rec-percentage-completion-method.md)

[Uruskan anggaran hasil](rev-rec-completed-contract-method.md)

[Kos untuk melengkapkan kaedah](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]