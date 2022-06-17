---
title: Betulkan perakaunan dalam draf cadangan invois projek
description: Artikel ini menerangkan cara melaraskan maklumat berkaitan perakaunan pada draf cadangan invois.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921221"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Betulkan perakaunan dalam draf cadangan invois projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

*Butiran operasi* untuk invois projek diselenggarakan oleh pengurus projek dalam invois proforma. Butiran ini termasuk keputusan mengenai jam, perbelanjaan, bahan atau pencapaian yang mesti diinvois, kadar dan aplikasi amaun pendahuluan dan penahan. Selepas anda mengesahkan invois proforma asal, anda boleh melaraskan butiran operasi dengan mencipta dan mengesahkan [invois proforma pembetulan](../proforma-invoicing/corrective-invoices.md).

*Butiran perakaunan* untuk invois projek diselenggarakan dalam dokumen invois bersemuka dengan pelanggan. Butiran ini termasuk pengiraan cukai jualan dan dimensi kewangan yang digunakan pada invois. Artikel ini memberikan butiran tentang cara butiran perakaunan ini boleh dilaraskan pada draf cadangan invois projek.

## <a name="adjust-sales-tax"></a>Laraskan cukai jualan

Kumpulan cukai jualan pengebilan dan kumpulan cukai jualan item lalai boleh dilaraskan secara langsung dalam dokumen cadangan invois. Untuk melaraskan kumpulan-kumpulan ini, pilih **Edit** dan kemudian, pada setiap baris cadangan invois projek, masukkan nilai baharu dalam medan **Kumpulan cukai jualan** atau **Kumpulan cukai jualan item**.

## <a name="adjust-financial-dimensions"></a>Laraskan dimensi kewangan

### <a name="header-dimensions"></a>Dimensi tajuk

Secara lalai, dimensi kewangan invois diperolehi daripada rekod transaksi projek yang belum dibilkan yang sedang diinvois. Walau bagaimanapun, tetapan sistem membolehkan anda menggunakan dimensi kewangan pada tajuk cadangan invois projek untuk menghantar baki pelanggan. Untuk mendayakan kefungsian ini, pilih **Benarkan kemas kini kepada dimensi projek untuk akaun belum terima** pada **tab Kewangan** bagi **halaman Pengurusan Projek dan parameter** perakaunan.

Dimensi kewangan pada pengepala invois boleh diedit sebelum invois disiarkan. **Pada halaman Cadangan** invois Projek, tukar kepada **pandangan Pengepala**, kemudian edit nilai pada **tab Dimensi** kewangan.

Pandangan **Pengepala** tersedia hanya selepas pentadbir sistem mendayakan **borang Gunakan cadangan invois Projek dan jurnal invois dengan ciri pandangan** Pengepala dan Baris dalam **ruang kerja pengurusan** Ciri. Ciri ini memerlukan kemas kini Kewangan 10.0.25 atau lebih baru.

### <a name="line-dimensions"></a>Dimensi garisan

Dimensi kewangan tidak boleh diedit secara langsung dalam baris cadangan invois projek. Sebaliknya, ikuti langkah ini untuk melaraskan dimensi kewangan dalam cadangan invois projek.

1. Pada cadangan invois projek, pilih **Padam semua** untuk mengalih keluar baris cadangan invois projek.

    Butang **Padam semua** tersedia hanya selepas pentadbir sistem mendayakan **Padamkan baris cadangan invois apabila menggunakan ciri Project Operations untuk senario bukan distok/berdasarkan sumber** dalam ruang kerja **Pengurusan ciri**.

2. Laraskan dimensi kewangan:

    - **Transaksi dalam akaun (pencapaian pengebilan):** Pergi ke **Semua projek** \> **Urus** \> **Transaksi dalam akaun** dan pilih pencapaian yang memerlukan pelarasan. Kemudian, pada tab **Dimensi kewangan**, kemas kini nilai seperti yang diperlukan.
    - **Masa, perbelanjaan dan transaksi masa:** Pada halaman **Transaksi projek yang disiarkan**, pilih **Laraskan perakaunan** untuk mengemas kini dimensi kewangan.

3. Selepas anda menyelesaikan pelarasan nilai dimensi kewangan, pergi ke **Pengurusan dan perakaunan projek** \> **Berkala** \> **Integrasi Project Operations** dan pilih **Import daripada jadual pemeringkatan** untuk menjalankan proses berkala. Proses tersebut menggunakan nilai dimensi kewangan yang dikemas kini untuk mencipta semula baris cadangan invois projek. Nilai yang dikemas kini kemudian digunakan dalam sublejar projek dan lejar umum apabila invois projek disiarkan.
