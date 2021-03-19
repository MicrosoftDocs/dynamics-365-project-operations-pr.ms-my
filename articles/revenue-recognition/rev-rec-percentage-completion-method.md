---
title: Projek anggaran hasil harga tetap
description: Topik ini memberikan maklumat tentang hasil harga tetap dalam projek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278924"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projek anggaran hasil harga tetap 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Apabila anda mencipta baris kontrak projek dengan atribut berikut dalam Dynamics 365 Project Operations pada Microsoft Dataverse, sistem secara automatik mencipta projek anggaran hasil harga tetap. Maklumat dalam projek ini adalah berdasarkan perkara berikut:

  - Kaedah pengebilan harga tetap.
  - Projek yang berkaitan.
  - Sekurang-kurangnya satu pencapaian ditakrifkan pada tab **Jadual invois** pada halaman **Baris kontrak projek**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Semak projek anggaran hasil harga tetap
Untuk menyemak projek anggaran hasil harga tetap, lengkapkan langkah berikut:

1. Dalam persekitaran Dynamics 365 Finance, pergi ke **Pengurusan dan perakaunan projek** > **Projek** > **Projek anggaran hasil harga tetap**.
2. Pilih projek yang anda mahu lihat dan klik dua kali pada **ID projek anggaran** untuk membuka rekod dan menyemak butiran projek.
3. Kembangkan tab **Projek**. Anda akan melihat satu projek dalam grid **Projek yang dipilih**. Sistem ini menggunakan ini sebagai projek lalai kerana ia merupakan projek yang berkaitan dengan baris kontrak projek. 
4. Untuk mengubah perkaitan itu, pilih projek tambahan dan tambahkannya pada grid **Projek yang dipilih**. Jika berbilang projek dipilih dalam grid ini, peratusan penyelesaian projek dan anggaran hasil dikira bersama untuk semua projek yang dipilih.

  Kos projek, profil hasil, templat kos dan kod tempoh boleh ditetapkan secara manual. Jika ia tidak ditetapkan secara manual, nilai lalai semasa pengiraan anggaran pertama untuk projek menggunakan peraturan yang dikonfigurasikan untuk kos projek dan profil hasil.



[!INCLUDE[footer-include](../includes/footer-banner.md)]