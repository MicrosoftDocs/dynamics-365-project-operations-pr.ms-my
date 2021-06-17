---
title: Sahkan kontrak projek
description: Topik ini menyediakan maklumat tentang cara mengesahkan kontrak dalam Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003687"
---
# <a name="confirm-a-project-contract"></a>Sahkan kontrak projek

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Kontrak projek dalam Dynamics 365 Project Operations boleh aktif dengan sebab **Disahkan** atau ditutup dengan sebab **Hilang**. Apabila anda mengesahkan kontrak projek, kemas kini status daripada **Draf** kepada **Aktif** dan sebab status **Disahkan**. Kontrak aktif atau tertutup tidak boleh diedit atau dibuka semula. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Kesan kewangan kerana mengesahkan kontrak projek

Selepas kontrak projek disahkan, aplikasi mengira semula kos dengan menterbalikkan aktual kos yang lama dan mencipta semula aktual kos yang baharu. Aktual kos baharu kemudian diproses berdasarkan kepada kaedah pengebilan bagi baris kontrak projek berkaitan. Jika aktual kos merujuk kepada baris kontrak Masa dan Bahan, aplikasi secara automatik mencipta semula aktual jualan yang belum dibilkan yang serupa. Jika aktual kos merujuk kepada baris kontrak Harga Tetap, aplikasi berhenti memproses semula aktual kos.

Had tidak melebihi, persediaan boleh dituntut dan penetapan harga dan kos berdasarkan sebenar dinilai dan kemudian dikemas kini sebagai sebahagian daripada proses pengesahan.

## <a name="close-a-project-contract-as-lost"></a>Tutup kontrak projek sebagai hilang

Apabila anda menutup kontrak projek sebagai hilang, status kontrak dikemas kini kepada **Ditutup** dan sebab status **Hilang**. Kontrak projek menjadi baca sahaja. Dialog pengesahan diberikan sebelum perubahan selesai kerana anda tidak boleh membuka semula kontrak projek yang ditutup.

Jika kontrak projek yang ditutup sebagai hilang merujuk kepada projek pada barisnya, projek itu juga ditandakan sebagai ditutup. Sebarang tempahan sumber dari hari tersebut ke hadapan dibatalkan. Sebarang aktual jualan yang tidak dibilkan pada kontrak projek yang belum ada pada invois akan diterbalikkan.

> [!NOTE]
> Dalam Dynamics 365 Project Operations, menutup kontrak projek sebagai hilang tidak akan memberi kesan kepada status peluang yang berkaitan. Peluang akan kekal terbuka dan mesti ditutup secara manual.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]