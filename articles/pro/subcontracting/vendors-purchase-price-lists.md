---
title: Pengurusan vendor dan senarai harga pembelian dalam Project Operations
description: Topik ini memberikan maklumat yang akan membantu anda mencipta dan mengekalkan data vendor dan senarai harga pembelian untuk subkontrak.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994152"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Pengurusan vendor dan senarai harga pembelian dalam Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

## <a name="vendors-in-project-operations"></a>Penjual dalam Project Operations

Dalam Microsoft Dynamics 365 Project Operations, akaun vendor mempunyai jenis hubungan **Vendor** atau **Pembekal**. Anda hanya boleh memilih rekod akaun yang mempunyai salah satu jenis hubungan ini sebagai vendor pada subkontrak.

Anda boleh mengaitkan satu atau lebih senarai harga pembelian dengan rekod vendor. Walau bagaimanapun, setiap senarai harga pembelian yang dikaitkan dengan rekod vendor harus mempunyai kuat kuasa tarikh yang berbeza. Project Operations tidak menyokong kuat kuasa tarikh yang bertindih untuk senarai harga pembelian.

Secara lalai, medan dan konsep berikut pada rekod vendor digunakan untuk sebarang subkontrak yang dicipta untuk vendor:

- Terma pembayaran
- Kenalan bil kepada
- Kenalan utama

    > [!NOTE]
    > Secara lalai, kenalan utama vendor digunakan sebagai pengurus akaun vendor subkontrak.

- Mata wang
- Senarai harga pembelian semasa

## <a name="purchase-price-lists-in-project-operations"></a>Senarai harga pembelian dalam Project Operations

Senarai harga yang medan **Konteks** ditetapkan kepada **Pembelian** dianggap senarai harga pembelian. Senarai harga pembelian boleh ditakrifkan untuk mewakili katalog harga pembelian untuk masa, perbelanjaan, dan bahan. Senarai harga pembelian menyerupai senarai harga kos dan jualan dalam Project Operations. Konsep berikut digunakan pada senarai harga pembelian dengan cara yang sama ia digunakan pada senarai harga kos dan penjualan:

- **Kuat kuasa tarikh** – Senarai harga pembelian mempunyai kuat kuasa tarikh. Kuat kuasa tarikh ditunjukkan oleh medan tarikh mula dan tarikh akhir pada setiap senarai harga. Masa antara tarikh mula dan tarikh akhir ialah tempoh kuat kuasa tarikh.
- **Mata wang** – Mata wang pada tajuk senarai harga digunakan sebagai mata wang yang dinyatakan bagi harga pembelian untuk buruh, kategori perbelanjaan, dan produk dalam katalog.
- **Unit masa lalai** – Unit masa lalai menyatakan harga buruh untuk pembelian. Medan unit masa pada senarai harga hanya digunakan untuk memberikan nilai lalai. Nilai tersebut boleh diubah pada baris harga peranan individu.

Senarai harga pembelian boleh dilampirkan pada rekod vendor sebagai perkaitan yang dikenali sebagai senarai harga projek. Senarai harga ini digunakan untuk memasukkan harga lalai pada baris subkontrak. Secara lalai, apabila beberapa senarai harga pembelian dilampirkan pada rekod vendor, senarai harga terkini digunakan untuk subkontrak yang dicipta untuk vendor. Hanya senarai harga yang medan **Konteks** ditetapkan kepada **Pembelian** boleh dilampirkan pada rekod vendor.

### <a name="subcontract-specific-purchase-price-lists"></a>Senarai harga pembelian khusus subkontrak

Senarai harga pembelian boleh juga dilampirkan pada subkontrak sebagai perkaitan yang dikenali sebagai senarai harga projek. Senarai harga ini digunakan untuk memasukkan harga lalai pada baris subkontrak. Secara lalai, apabila beberapa senarai harga pembelian dilampirkan pada subkontrak, setiap satunya mesti mempunyai kuat kuasa tarikh yang berbeza. Project Operations tidak menyokong senarai harga pembelian yang mempunyai kuat kuasa tarikh yang bertindih. Hanya senarai harga yang medan **Konteks** ditetapkan kepada **Pembelian** boleh dilampirkan pada subkontrak.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
