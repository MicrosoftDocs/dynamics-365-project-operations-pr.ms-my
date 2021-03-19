---
title: Tutup sebut harga
description: Topik ini menyediakan maklumat tentang penutupan sebut harga dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277259"
---
# <a name="close-a-quote"></a>Tutup sebut harga

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Sebut harga projek boleh ditutup sebagai Menang atau Hilang. Oleh kerana fungsi Aktifkan dan Semak tidak disokong pada sebut harga dalam Microsoft Dynamics 365 Project Operations, anda boleh menutup sebut harga draf.

## <a name="close-a-quote-as-won"></a>Tutup sebut harga sebagai Menang

Menutup sebut harga projek sebagai Menang akan menetapkan status sebut harga kepada **Tutup** dan sebab status kepada **Menang**. Menutup sebut harga menjadikan ia baca sahaja dan mencipta draf kontrak projek dengan semua maklumat sebut harga. Oleh kerana sebut harga ditutup tidak boleh dibuka semula, sebelum anda tutup sebut harga, dialog pengesahan akan mengesahkan perubahan anda.

Kontrak projek yang dicipta daripada sebut harga projek juga akan tersedia dalam modul Pengurusan projek dan perakaunan Project Operations. Jika kontrak projek tidak dipetakan kepada projek pada sebarang baris, kontrak projek ini akan tersedia sebagai kontrak projek yang tidak aktif dan menjadi aktif sebaik sahaja projek dipetakan kepada sekurang-kurangnya satu daripada baris kontrak.

Jika sebut harga dilampirkan kepada peluang, sebarang sebut harga projek lain untuk peluang ditutup secara automatik sebagai hilang.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Kesan kewangan untuk menutup sebut harga sebagai Menang

Jika telah ada sebarang masa yang sebenar direkodkan pada projek semasa ia masih dilampirkan pada draf sebut harga, hanya kos masa atau perbelanjaan direkodkan. Selepas sebut harga ditutup sebagai Menang, aplikasi itu akan faktor semula kos dengan menterbalikkan kos sebenar yang lebih lama dan mencipta semula kos sebenar yang baharu. Aplikasi akan memproses kos sebenar berdasarkan kepada Kaedah pengebilan bagi baris kontrak projek berkaitan. Jika kos sebenar merujuk pada masa dan baris kontrak bahan, sistem akan secara automatik akan mencipta jualan sebenar yang belum dibilkan untuk apabila sebut harga ditutup dan kontrak projek dicipta. Jika kos sebenar merujuk kepada baris kontrak harga tetap, aplikasi akan berhenti untuk memproses semula kos sebenar berdasarkan peraturan pengebilan pecahan untuk pelanggan kontrak projek.

Semua aktual yang diproses semula boleh tersedia di dalam Modul pengurusan projek dan perakaunan bagi Akauntan projek menyemak, mengemas kini, dan siaran ke Lejar Umum. 

## <a name="close-a-quote-as-lost"></a>Tutup sebut harga sebagai Hilang

Menutup sebut harga projek sebagai Hilang akan menetapkan status sebut harga kepada **Tutup** dan sebab status kepada **Hilang**. Tutup sebut harga menjadikan ia baca sahaja. Oleh kerana sebut harga ditutup tidak boleh dibuka semula dan, sebelum anda tutup sebut harga, dialog pengesahan akan mengesahkan perubahan anda.

Jika projek sebut harga yang ditutup sebagai Hilang mempunyai projek yang dirujuk pada sebarang baris, projek tersebut juga ditandakan sebagai Tutup dan sebarang penempahan sumber dari hari ke hadapan dibatalkan.

> [!NOTE]
> Dalam Project Operations, menutup sebut harga sebagai Menang atau Hilang tidak akan memberi kesan bahawa status Peluang, yang akan kekal terbuka sehingga ia secara manual ditutup.


[!INCLUDE[footer-include](../includes/footer-banner.md)]