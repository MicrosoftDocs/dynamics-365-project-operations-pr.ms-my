---
title: Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu
description: Topik ini memberikan maklumat mengenai mengemas kini atribut pasang masuk untuk dimensi penetapan.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988797"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jika anda tidak menggunakan ciri Pesanan Harga Project Service Automation (PSA) dan Pengkontrakan, anda boleh melangkau topik ini.

Topik ini menganggap bahawa anda telah melengkapkan prosedur dalam topik, [Cipta medan dan entiti tersuai](create-custom-fields-entities.md), [Tambah medan tersuai kepada persediaan harga dan entiti transaksi](field-references.md) dan [Sediakan medan tersuai sebagai dimensi penetapan harga](set-up-pricing-dimensions.md). Jika anda belum menyelesaikan prosedur tersebut, kembali dan lengkapkan mereka dan kemudian kembali ke topik ini.

Apabila butiran baris sebut harga dicipta pada halaman baris **Baris Sebut Harga** untuk baris sebut harga projek, sistem mencipta dua baris anggaran dalam latar belakang -- satu baris untuk bahagian kos anggaran dan satu untuk jualan pihak. Ini adalah sama untuk baris kontrak projek.

Apabila anda membuat perubahan pada kuantiti atau medan pada bahagian kos, perubahan tersebut akan disebarkan ke bahagian jualan. Ini mungkin kerana pasang berikut yang mesti didaftarkan semula selepas perubahan dimensi penetapan harga.

- PreOperationContractLineDetailUpdate- Kemas Kini **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Kemas Kini **msdyn_quotelinetransaction**.

Langkah berikut menerangkan tentang proses pendaftaran pasang masuk.

1. Buka **PluginRegistrationTool** dan sambung kepada tika dalam talian anda.
2. Klik **Cari** dan cari untuk pasang masuk dikemas kini.

 ![Tangkapan skrin pohon carian.](media/PRT-1.png)

3. Selepas pasang masuk ditemui, pilihnya dan klik **Pilih pada Borang Utama**.

4. Pilih langkah pasang masuk untuk dikemas kini, klik kanan dan kemudian pilih **Kemas Kini**.

 ![Tangkapan skrin pasang masuk yang akan dikemas kini.](media/PRT-2.png)
 
5. Dalam tetingkap kemas kini, klik elsis (**...**) dalam atribut penapisan.

 ![Tangkapan skrin Kemas kini maklumat konfigurasi langkah sedia ada.](media/PRT-3.png)
 
6. Pilih kotak semak atribut penetapan harga.

 ![Tangkapan skrin menunjukkan pemilihan kotak semak untuk atribut penentuan harga.](media/PRT-4.png)

7. Klik **OK** untuk menutup halaman dan kemudian pilih **Kemas Kini Langkah**.

 ![Tangkapan skrin yang menunjukkan butang "Kemas kini Langkah".](media/PRT-5.png)
 
8. Ulang proses ini untuk pasang masuk kedua, **PreOperationQuoteLineDetail - Kemas Kini msdyn_quotelinetransaction**.

9. Tutup alat pendaftaran pasang masuk.



[!INCLUDE[footer-include](../includes/footer-banner.md)]