---
title: Gambaran keseluruhan penginvoisan antara syarikat
description: Topik ini memberikan maklumat dan contoh tentang penginvoisan antara syarikat untuk projek.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595519"
---
# <a name="intercompany-invoicing-overview"></a>Gambaran keseluruhan penginvoisan antara syarikat

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Organisasi anda mungkin mempunyai berbilang divisyen, subsidiari dan entiti undang-undang lain yang memindahkan produk dan perkhidmatan kepada satu sama lain untuk projek. Entiti undang-undang yang menyediakan perkhidmatan atau produk tersebut dipanggil *entiti undang-undang yang memberi pinjaman*. Entiti undang-undang yang menerima perkhidmatan atau produk tersebut dipanggil *entiti undang-undang yang menerima pinjaman*.

Ilustrasi berikut menunjukkan senario biasa di mana dua entiti undang-undang, Contoso Robotics USA (entiti undang-undang yang menerima pinjaman) dan contoso Robotics UK (entiti undang-undang yang memberi pinjaman) berkongsi sumber untuk menyampaikan projek kepada pelanggan, kerja Adventure. Untuk senario ini, Contoso Robotics USA dikontrakkan untuk menyampaikan kerja kepada Adventure Works.

![Penginvoisan antara syarikat](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations menggunakan aliran berikut untuk memproses transaksi antara syarikat:

1. Sumber daripada entiti undang-undang yang memberi pinjaman merekod transaksi perbelanjaan atau masa antara syarikat mengikut masa tempahan dan perbelanjaan terhadap projek dalam entiti undang-undang yang menerima pinjaman.
2. Kos masa dan perbelanjaan direkodkan dalam syarikat yang memberi pinjaman dengan menggunakan senarai harga kos unit syarikat yang menerima pinjaman.
3. Transaksi jualan tidak dibilkan antara syarikat direkodkan dalam syarikat yang memberi pinjaman dengan menggunakan senarai harga kos unit syarikat yang menerima pinjaman.
4. Pendapatan yang tidak dibilkan direkodkan dalam syarikat yang menerima pinjaman menggunakan senarai harga jualan kontrak projek. Pelanggan boleh dibilkan apabila hasil tidak dibilkan direkodkan. Pelanggan tidak perlu menunggu sehingga pemprosesan invois antara syarikat selesai.
5. Invois pelanggan antara syarikat dibuat secara berkala dalam syarikat yang memberi pinjaman. Invois dicipta secara manual atau dengan menggunakan proses automatik berkala. Invois tunggal boleh dicipta untuk setiap entiti undang-undang yang memberi pinham atau invois berasingan boleh dicipta mengikut projek.
6. Apabila invois pelanggan antara syarikat disiarkan dalam entiti undang-undang yang memberi pinjaman, invois vendor yang belum selesai dibuat dalam entiti undang-undang yang menerima pinjaman. Kos dalam invois vendor yang belum selesai akan direkodkan kepada sublejar projek apabila invois disiarkan.

Gambar rajah berikut menunjukkan penginvoisan antara syarikat kerana ia berkaitan dengan peristiwa perakaunan dan penyiaran yang dijangka kepada lejar umum.

![Aliran antara syarikat](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Sumber tambahan

- [Konfigurasikan penginvoisan antara syarikat](configure-intercompany-invoicing.md)
- [Rekodkan transaksi antara syarikat](create-intercompany-transactions.md)
- [Cipta invois pelanggan dan vendor antara syarikat](create-intercompany-customer-vendor-invoices.md)
