---
title: Kemas kini atribut pasang masuk untuk memasukkan dimensi penetapan harga baharu
description: Topik ini memberikan maklumat mengenai mengemas kini atribut pasang masuk untuk dimensi penetapan.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147079"
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

 ![Tangkapan skrin pepohon carian](media/PRT-1.png)

3. Selepas pasang masuk ditemui, pilihnya dan klik **Pilih pada Borang Utama**.

4. Pilih langkah pasang masuk untuk dikemas kini, klik kanan dan kemudian pilih **Kemas Kini**.

 ![Tangkapan skrin bagi pasang masuk yang akan dikemas kini](media/PRT-2.png)
 
5. Dalam tetingkap kemas kini, klik elsis (**...**) dalam atribut penapisan.

 ![Tangkapan skrin kemas kini langkah sedia ada maklumat konfigurasi](media/PRT-3.png)
 
6. Pilih kotak semak atribut penetapan harga.

 ![Tangkapan skrin yang ditunjukkan pilihan kotak semak untuk atribut penetapan](media/PRT-4.png)

7. Klik **OK** untuk menutup halaman dan kemudian pilih **Kemas Kini Langkah**.

 ![Skrin menunjukkan butang “Langkah Kemas Kini”](media/PRT-5.png)
 
8. Ulang proses ini untuk pasang masuk kedua, **PreOperationQuoteLineDetail - Kemas Kini msdyn_quotelinetransaction**.

9. Tutup alat pendaftaran pasang masuk.



[!INCLUDE[footer-include](../includes/footer-banner.md)]