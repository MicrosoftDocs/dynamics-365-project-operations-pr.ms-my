---
title: Betulkan perakaunan dalam draf cadangan invois projek
description: Topik ini menerangkan cara untuk melaraskan maklumat berkaitan perakaunan dalam draf cadangan invois.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999327"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Betulkan perakaunan dalam draf cadangan invois projek

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

*Butiran operasi* untuk invois projek diselenggarakan oleh pengurus projek dalam invois proforma. Butiran ini termasuk keputusan mengenai jam, perbelanjaan, bahan atau pencapaian yang mesti diinvois, kadar dan aplikasi amaun pendahuluan dan penahan. Selepas anda mengesahkan invois proforma asal, anda boleh melaraskan butiran operasi dengan mencipta dan mengesahkan [invois proforma pembetulan](../proforma-invoicing/corrective-invoices.md).

*Butiran perakaunan* untuk invois projek diselenggarakan dalam dokumen invois bersemuka dengan pelanggan. Butiran ini termasuk pengiraan cukai jualan dan dimensi kewangan yang digunakan pada invois. Topik ini memberikan butiran mengenai cara butiran perakaunan ini boleh dilaraskan dalam draf cadangan invois projek.

## <a name="adjust-sales-tax"></a>Laraskan cukai jualan

Kumpulan cukai jualan pengebilan dan kumpulan cukai jualan item lalai boleh dilaraskan secara langsung dalam dokumen cadangan invois. Untuk melaraskan kumpulan-kumpulan ini, pilih **Edit** dan kemudian, pada setiap baris cadangan invois projek, masukkan nilai baharu dalam medan **Kumpulan cukai jualan** atau **Kumpulan cukai jualan item**.

## <a name="adjust-financial-dimensions"></a>Laraskan dimensi kewangan

Dimensi kewangan tidak boleh diedit secara langsung dalam baris cadangan invois projek. Sebaliknya, ikuti langkah ini untuk melaraskan dimensi kewangan dalam cadangan invois projek.

1. Pada cadangan invois projek, pilih **Padam semua** untuk mengalih keluar baris cadangan invois projek.

    > [!NOTE]
    > Butang **Padam semua** tersedia hanya selepas pentadbir sistem mendayakan **Padamkan baris cadangan invois apabila menggunakan ciri Project Operations untuk senario bukan distok/berdasarkan sumber** dalam ruang kerja **Pengurusan ciri**.

2. Laraskan dimensi kewangan:

    - **Transaksi dalam akaun (pencapaian pengebilan):** Pergi ke **Semua projek** \> **Urus** \> **Transaksi dalam akaun** dan pilih pencapaian yang memerlukan pelarasan. Kemudian, pada tab **Dimensi kewangan**, kemas kini nilai seperti yang diperlukan.
    - **Masa, perbelanjaan dan transaksi masa:** Pada halaman **Transaksi projek yang disiarkan**, pilih **Laraskan perakaunan** untuk mengemas kini dimensi kewangan.

3. Selepas anda menyelesaikan pelarasan nilai dimensi kewangan, pergi ke **Pengurusan dan perakaunan projek** \> **Berkala** \> **Integrasi Project Operations** dan pilih **Import daripada jadual pemeringkatan** untuk menjalankan proses berkala. Proses tersebut menggunakan nilai dimensi kewangan yang dikemas kini untuk mencipta semula baris cadangan invois projek. Nilai yang dikemas kini kemudian digunakan dalam sublejar projek dan lejar umum apabila invois projek disiarkan.
