---
title: Kaedah peruntukan tempahan
description: Topik ini menyediakan maklumat tentang cara kaedah peruntukan penempahan berfungsi dalam Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081178"
---
# <a name="booking-allocation-methods"></a>Kaedah peruntukan tempahan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Apabila anda menambah ahli pasukan secara terus kepada projek pada tab **Pasukan** , atau tempah sumber pada projek atau keperluan dari papan Jadualm terdapat beberapa kaedah peruntukan tempahan berbeza yang anda boleh gunakan. Topik ini menerangkan cara setiap fungsi kaedah, dan kaedah yang mana membawa kepada sumber tempah berlebihan

## <a name="booking-allocation-methods"></a>Kaedah peruntukan tempahan

Terdapat enam kaedah peruntukan penempahan yang boleh anda gunakan:

- [Kapasiti penuh](#full)
- [Baki kapasiti](#remaining)
- [Kapasiti peratusan](#percentage)
- [Jam diagihkan dengan sekata](#evenly)
- [Jam muatan hadapan](#front)
- [Tiada](#none)

### <a name="full-capacity"></a><a name="full"></a>Kapasiti penuh 
Kaedah Kapasiti Penuh menempah kapasiti penuh sumber utnuk tarikh dari dan sehingga khusus. Contohnya, jika kalendar sumber ditetapkan untuk bekerja lapan jam setiap hari, lima hari dalam semingu, menetapkan tarikh mula dan tamat yang merangkumi lima hari bekerja akan menempah sumber selama 40 jam. Tempahan dilakukan tanpa mengambil kira baki kapasiti sumber. Jika sumber telah ditempah pada projek lain semasa tempah tersebut, 40 jam ditempah sebagai jam tambahan, yang berpotensi membawa kepada tempah berlebihan.

### <a name="remaining-capacity"></a><a name="remaining"></a>Baki kapasiti
Kedah Baki Kapasiti hanya tersedia apabila anda tempah secara terus kepada projek menggunakan papan Jadual. Kaedah ini menempah kapasiti tersedia sumber dalam julat tarikh yang dinyatakan. Contohnya, jika sumber mempunyai kapasiti 40 jam setiap minggu dan telah ditempah 10 jam, tempahan untuk minggu sama menyebabkan tempahan baki 30 jam kapasiti untuk minggu tersebut.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapasiti peratusan
Kaedah Kapasiti Peratusan menempah sumber untuk peratusan kapasiti bagi tarikh dari dan sehingga yang dinyatakan. Contohnya, jika kalendar sumber ditetapkan untuk bekerja lapan jam setiap hari, lima hari dalam semingu, menetapkan tarikh mula dan tamat yang merangkumi lima hari bekerja pada kapasiti 50% akan menempah sumber untuk 20 jam. Tempahan individu setiap hari diagihkan sama rata dalam semua tempoh, empat jam setiap hari dalam contoh ini. Tempahan dilakukan tanpa mengambil kira baki kapasiti sumber. Jika sumber telah ditempah pada projek lain semasa tempah tersebut, 20 jam ditempah sebagai jam tambahan, yang berpotensi membawa kepada tempah berlebihan.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Jam diagihkan dengan sekata
Kaedah Mengagih Jam Sama Rata menempah sumber untuk jumlah jam tertentu, mengagihkan masa tersebut secara sama rata setiap hari selama tempoh tarikh dari dan tarikh hingga khusus. Contohnya, jika and menempah sumber untuk 20 jam selama tempoh lima hari, kaedah ini mengagihkan 20 jam secara sama rata kepada empat jam setiap hari. Tempahan dilakukan tanpa mengambil kira baki kapasiti sumber. Jika sumber telah ditempah pada projek lain semasa tempah tersebut, 20 jam ditempah sebagai jam tambahan, yang berpotensi membawa kepada tempah berlebihan.

### <a name="front-load-hours"></a><a name="front"></a>Jam muatan hadapan
Kaedah Muat Jam Hadapan menempah sumber untuk jumlah jam tertentu, memuat hadapan jam setiap hari selama tempoh tarikh dari dan tarikh hingga khusus. Muatan depan menggunakan kapasiti tersedia sumber dalam susunan "pertama masuk pertama digunakan". Contohnya, jika jadual kerja sumber adalah lapan jam setiap hari, limat hari setiap minggu, dan ia tiada tempahan semasa, menempah sumber untuk 20 jam selama tempoh lima hari bekerja menghasilkan corak tempahan harian berikut: 

|                           |    Hari 1    |    Hari 2    |    Hari 3    |    Hari 4    |    Hari 5    |    Jumlah    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Tempahan sedia ada**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Tempahan baharu**          |    8        |    8        |    4        |    0        |    0        |    20       |

Kaedah muatan hadapan mengambil kira tempahan sedia ada dan kapasiti tersedia. Contohnya, jika sumber yang sama sudah mempunyai 20 jam tempahan dalam minggu kerja, tempahan baharu menggunakan baki kapasiri seperti berikut:

|                     | Hari 1 | Hari 2 | Hari 3 | Hari 4 | Hari 5 | Jumlah |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Tempahan sedia ada** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Tempahan baharu**       | 0     | 0     | 4     | 8     | 8     | 20    |

Kerana tempahan sedia ada dipertimbangkan, anda mungkin menerima mesej ralat jika sumber tidak mempunyai baki kapasiti yang boleh diserap melalui tempahan. Dengan kaedah ini, anda tidak boleh terlebih tempah.

### <a name="none"></a><a name="none"></a>Tiada
Kaedah Tiada hanya tersedia apabila anda menempah dari tab **Pasukan** dalam projek. Kaedah ini menambah sumber sebagai ahli pasukan pada projek, tetapi tidak mencipta sebarang tempahan yang menyerap kapasiti sumber. Kaedah ini digunakan apabila ahli pasukan pengurus projek ditambah semasa projek dicipta. Pengguna pengurus projek yang mencipta projek ditambah secara lalai kepada projek, supaya rekod entiti projek mempunyai pemilik dan terdapat seorang pelulus pada projek. Disebabkan pengguna ini tidak mempunyai sebarang tempahan, jika anda mahu menempah sumber, anda boleh sama da memadam dan kemudian menambah semula mereka menggunakan kaedah peruntukan berbeza, atau menambah sumber pada tugas dan kemudian menggunakan **Lanjutkan Tempahan** pada tab **Penyesuaian** untuk mencipta tempahan untuk tugasan.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Kaedah peruntukan yang menyebabkan terlebih tempahan
Ringkasnya, kaedah peruntukan yang berikut menyebabkan terlebih tempahan jika sumber sudah komited dalam projek lain (atau untuk susunan kerja lain atau entiti boleh jadual):

- Kapasiti Penuh
- Kapasiti Peratusan
- Jam Diagihkan dengan Sekata

Semasa menggunakan salah satu daripada tiga kaedah peruntukan ini, anda tidak akan diberi amaran bahawa sumber telah terlebih tempah. Untuk membetulkan tempahan berlebihan, anda perlu menggunakan papan Jadual.
