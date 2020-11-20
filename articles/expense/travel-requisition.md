---
title: Permintaan perjalanan
description: Topik ini menyediakan maklumat tentang permintaan perjalanan.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123749"
---
# <a name="travel-requisitions"></a>Permintaan perjalanan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Permintaan perjalanan menyenaraikan perbelanjaan yang akan terlibat untuk tujuan perjalanan. Permintaan perjalanan diserahkan untuk ulasan dan boleh digunakan untuk membenarkan perbelanjaan.

Anda mungkin diperlukan untuk menyerahkan permintaan perjalanan sebelum anda menanggung sebarang perbelanjaan yang dicaj kepada organisasi. Keperluan ini digunakan, tanpa mengira sama ada anda caj perbelanjaan kepada kad kredit korporat, membelanjakan tunai yang anda terima daripada pendahuluan tunai, atau menanggung perbelanjaan secara saku yang akan dibayar balik oleh organisasi.

Permintaan perjalanan dan polisi boleh digunakan untuk membantu menguruskan perbelanjaan organisasi. Contohnya, jika organisasi anda mengusahakan projek harga tetap yang memerlukan perjalanan, perbelanjaan perjalanan ahli pasukan projek mesti sesuai dalam belanjawan projek. Dengan memerlukan perbelanjaan perjalanan diluluskan sebelum ditanggung, organisasi boleh membantu memastikan projek tersebut kekal dalam dalam belanjawan.

## <a name="configuration"></a>Konfigurasi 

Permintaan perjalanan boleh dikonfigurasikan sebagai "mandatori" dengan mendayakan parameter "Pra pengesahan perjalanan adalah mandatori" dalam Parameter Pengurusan Perbelanjaan. 

## <a name="create-and-submit-a-travel-requisition"></a>Cipta dan serahkan permintaan perjalanan

1. Pergi ke **Perbelanjaan saya: Permintaan Perjalanan**, dan pilih **Permintaan perjalanan baharu**.
2. Masukkan tujuan dan destinasi untuk permintaan.
3. Dalam medan  **Perihalan perjalanan**, masukkan sebarang maklumat tambahan. 
4. Untuk setiap perbelanjaan yang dijangka, seperti Penerbangan, hidangan atau sewaan kereta, cipta item baris perbelanjaan. Masukkan anggaran tarikh, jumlah anggaran, dan mata wang untuk setiap perbelanjaan. 
5. Apabila anda telah selesai menambah anggaran perbelanjaan, pilih **Simpan**.
6. Apabila anda bersedia untuk menyerahkan permintaan perjalanan, pilih **Aliran kerja** > **Serahkan**.

Anda boleh melihat permintaan perjalanan anda yang diluluskan di bawah **Perbelanjaan Saya: Permintaan Perjalanan**. 

## <a name="view-available-travel-requisitions"></a>Lihat permintaan perjalanan yang tersedia

Anda boleh melihat semua permintaan perjalanan anda yang diluluskan di bawah **Perbelanjaan Saya: Permintaan Perjalanan**.

## <a name="approve-travel-requisitions"></a>Luluskan permintaan perjalanan

Pilih permintaan perjalanan yang anda mahu luluskan, dan kemudian pilih **Aliran kerja** > **Luluskan**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Serahkan laporan perbelanjaan menggunakan permintaan perjalanan anda yang diluluskan

1. Cipta laporan perbelanjaan baharu dan dalam pengepala laporan perbelanjaan, dan daripada senarai permintaan perjalanan yang diluluskan, pilih **Peta kepada Permintaan perjalanan**.
2. Medan **Jumlah permintaan perjalanan** dikemas kini secara automatik dalam pengepala laporan perbelanjaan.
3. Tambah setiap perbelanjaan yang dikenakan untuk perjalanan. Jika medan **Pra dibenarkan** didayakan, jumlah rekonsiliasi dan jumlah yang dibenarkan untuk kategori perbelanjaan khusus akan dikemas kini.

> [!NOTE]
> Apabila anda memetakan laporan perbelanjaan kepada permintaan perjalanan yang diluluskan, jumlah transaksi tidak boleh lebih besar daripada jumlah yang dibenarkan. 
