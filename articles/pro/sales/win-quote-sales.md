---
title: Tutup sebut harga - ringkas
description: Topik ini menyediakan maklumat tentang penutupan sebut harga dalam Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994147"
---
# <a name="close-a-quote---lite"></a>Tutup sebut harga - ringkas

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Sebut harga projek boleh ditutup sebagai Menang atau Hilang. Sebut harga draf boleh ditutup kerana operasi Aktifkan dan Semak Semula pada sebut harga tidak disokong dalam Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Tutup sebut harga sebagai Menang

Apabila anda menutup sebut harga projek sebagai Dimenangi, status ditetapkan ke Ditutup dan sebab status ialah Dimenangi. Menutup sebut harga menjadikan sebut harga projek baca sahaja dan mencipta draf kontrak projek yang mengandungi maklumat sebut harga. Oleh kerana sebut harga yang ditutup tidak boleh dibuka semula, dialog pengesahan akan mengesahkan perubahan anda.

Jika sebut harga dilampirkan kepada peluang, sebarang sebut harga projek lain untuk peluang ditutup secara automatik sebagai hilang.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Kesan kewangan untuk menutup sebut harga sebagai Menang

Jika terdapat mana-mana aktual untuk masa pada projek semasa masih dilampirkan ke draf sebut harga, hanya kos masa atau perbelanjaan direkodkan. Selepas sebut harga ditutup sebagai Menang, aplikasi itu akan faktor semula kos dengan menterbalikkan kos sebenar yang lebih lama dan mencipta semula kos sebenar yang baharu. Aplikasi akan memproses kos sebenar berdasarkan kepada Kaedah pengebilan bagi baris kontrak projek berkaitan. Jika kos aktual merujuk kepada masa dan baris kontrak bahan, aktual jualan yang belum dibil berkaitan akan dicipta untuk apabila sebut harga ditutup dan kontrak projek dicipta. Jika aktual kos merujuk kepada baris kontrak harga tetap, permohonan akan berhenti memproses semula aktual kos yang berdasarkan pada pecahan peraturan pengebilan untuk pelanggan kontrak projek.

## <a name="closing-a-quote-as-lost"></a>Menutup sebut harga sebagai hilang:

Apabila anda menutup sebut harga projek sebagai Kalah, status ditetapkan ke Ditutup dan sebab status ialah Kalah. Menutup sebut harga menjadikan sebut harga projek baca sahaja. Oleh kerana sebut harga ditutup tidak boleh dibuka semula dan, sebelum anda tutup sebut harga, dialog pengesahan akan mengesahkan perubahan anda.

Jika sebut harga projek ditutup sebagai Kalah merujuk kepada projek pada salah satu baris, projek itu juga ditandakan sebagai Ditutup. Sebarang tempahan sumber dari hari tersebut ke hadapan dibatalkan.

> [!NOTE]
> Dalam Project Operations, menutup sebut harga sebagai Menang atau Hilang tidak akan memberi kesan bahawa status Peluang, yang akan kekal terbuka sehingga ia secara manual ditutup.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]