---
title: Kemas kini atribut pasang masuk dengan dimensi penentuan harga baharu
description: Topik ini memberikan maklumat tentang cara mengemas kini atribut pasang masuk untuk dimensi penentuan harga.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643229"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Kemas kini atribut pasang masuk dengan dimensi penentuan harga baharu

Topik ini memberikan maklumat tentang cara mengemas kini atribut pasang masuk untuk dimensi penentuan harga.

> [!NOTE]
> Topik ini hanya digunakan untuk sebut harga dan ciri kontrak dalam Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Prasyarat
Sebelum anda melengkapkan langkah dalam topik ini, anda mesti melengkapkan prosedur dalam topik berikut:

  - [Cipta medan dan entiti tersuai](create-custom-fields-entities-pricing-dimensions.md) 
  - [Tambah medan tersuai kepada persediaan harga dan entiti transaksi ](add-custom-fields-price-setup-transactional-entities.md)
  - [Sediakan medan tersuai sebagai dimensi penentuan harga](set-up-custom-fields-pricing-dimensions.md). 
  
Jika anda belum melengkapkan prosedur tersebut, lengkapkannya dan kemudian kembali ke topik ini.

## <a name="register-a-plug-in"></a>Daftarkan pasang masuk
Apabila butiran baris sebut harga dicipta pada halaman **Baris Sebut Harga** untuk baris sebut harga projek, sistem mencipta dua baris anggaran. Satu baris adalah untuk bahagian kos anggaran dan baris lain untuk bahagian jualan. Ini adalah sama untuk baris kontrak projek.

Apabila anda membuat perubahan pada kuantiti atau medan pada bahagian kos, perubahan tersebut juga dibuat pada bahagian jualan. Ini berlaku kerana pasang masuk PreOperation pada Quotelinedetail dan entiti butiran baris kontrak menghubungkan atribut tertentu pada bahagian kos kepada bahagian jualan transaksi. Jika anda memerlukan perubahan yang dibuat pada nilai dimensi penentuan harga pada bahagian jualan juga dibuat pada bahagian kos, pasang masuk berikut mesti didaftarkan semula selepas membuat perubahan pada dimensi penentuan harga.

Ini ialah pasang masuk untuk dikemas kini dan didaftar semula:

- PreOperationContractLineDetailUpdate - **Kemas kini msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Kemas kini msdyn_quotelinetransaction**

Lengkapkan langkah berikut untuk mengemas kini dan mendaftar semula pasang masuk.

1. Buka **PluginRegistrationTool** dan sambung ke persekitaran Project Operations Dataverse anda.
2. Pilih **Cari** dan taip beberapa huruf pertama bagi pasang masuk yang akan dikemas kini.
3. Selepas pasang masuk ditemui, pilihnya dan pilih **Pilih pada Borang Utama**.
4. Pilih langkah **Kemas kini msdyn_orderlinetransaction**, klik kanan dan kemudian pilih **Kemas kini**.
5. Dalam halaman dialog **Kemas kini**, pilih elipsis (**...**) dalam atribut penapisan.
6. Tetingkap atribut penapisan dibuka dan menyediakan senarai semua atribut dalam entiti dan dimensi penentuan harga. Pilih kotak semak untuk atribut dimensi penentuan harga.
7. Pilih **OK** untuk menutup halaman dan kemudian pilih **Kemas Kini Langkah**.
8. Ulangan langkah 2-7 untuk pasang masuk kedua, **PreOperationQuoteLineDetail**. Untuk pasang masuk ini, anda perlu mengemas kini langkah **Update of msdyn_quotelinetransaction**.
9. Tutup **PluginRegistrationTool**.