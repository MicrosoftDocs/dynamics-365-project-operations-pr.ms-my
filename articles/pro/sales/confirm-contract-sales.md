---
title: Sahkan kontrak projek
description: Topik ini menyediakan maklumat tentang cara mengesahkan kontrak dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081348"
---
# <a name="confirm-a-project-contract"></a>Sahkan kontrak projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Kontrak projek dalam Dynamics 365 Project Operations boleh menjadi aktif dengan sebab **Disahkan** , atau ditutup dengan sebab **Hilang**. Apabila anda mengesahkan kontrak projek, kemas kini status daripada **Draf** kepada **Aktif** dan sebab status **Disahkan**. Kontrak aktif atau tertutup tidak boleh diedit atau dibuka semula. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Kesan kewangan kerana mengesahkan kontrak projek

Selepas kontrak projek disahkan, aplikasi mengira semula kos dengan menterbalikkan aktual kos yang lama dan mencipta semula aktual kos yang baharu. Aktual kos baharu kemudian diproses berdasarkan kepada kaedah pengebilan bagi baris kontrak projek berkaitan. Jika aktual kos merujuk kepada baris kontrak Masa dan Bahan, aplikasi secara automatik mencipta semula aktual jualan yang belum dibilkan yang serupa. Jika aktual kos merujuk kepada baris kontrak Harga Tetap, aplikasi berhenti memproses semula aktual kos.

Had tidak melebihi, persediaan boleh dituntut dan penetapan harga dan kos berdasarkan sebenar dinilai dan kemudian dikemas kini sebagai sebahagian daripada proses pengesahan.

## <a name="close-a-project-contract-as-lost"></a>Tutup kontrak projek sebagai hilang

Apabila anda menutup kontrak projek sebagai hilang, status kontrak dikemas kini kepada **Ditutup** dan sebab status **Hilang**. Kontrak projek menjadi baca sahaja. Dialog pengesahan diberikan sebelum perubahan selesai kerana anda tidak boleh membuka semula kontrak projek yang ditutup.

Jika kontrak projek yang ditutup sebagai hilang merujuk kepada projek pada barisnya, projek itu juga ditandakan sebagai ditutup. Sebarang tempahan sumber dari hari tersebut ke hadapan dibatalkan. Sebarang aktual jualan yang tidak dibilkan pada kontrak projek yang belum ada pada invois akan diterbalikkan.

> [!NOTE]
> Dalam Dynamics 365 Project Operations, menutup kontrak projek sebagai hilang tidak akan memberi kesan kepada peluang yang berkaitan. Peluang akan kekal terbuka dan mesti ditutup secara manual.
