---
title: Kos untuk melengkapkan kaedah
description: Artikel ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920301"
---
# <a name="cost-to-complete-methods"></a>Kos untuk melengkapkan kaedah

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Artikel ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek. Terdapat berbilang kaedah yang boleh anda gunakan untuk mengira kos untuk melengkapkan projek. 

Apabila anda mencipta anggaran untuk projek, pada halaman **Cipta anggaran**, dalam medan **Kos untuk melengkapkan kaedah**, anda boleh memilih salah satu daripada kos berikut untuk melengkapkan kaedah.

| Kos untuk melengkapkan kaedah    | Penerangan                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jumlah kos sebenar            | Masukkan kos anggaran secara manual dalam medan **Jumlah kos** atau **Jumlah kuantiti** menggunakan butang **Anggaran kos** pada **Halaman anggaran**. Sistem menolak kos sebenar daripada jumlah yang anda masukkan. Jumlah ini merupakan kos untuk melengkapkan projek. Kaedah ini tidak menggunakan anggaran perbelanjaan dan penugasan sumber yang dimasukkan dalam Project Operations dibina dalam Microsoft Dataverse. Jumlah kos atau jumlah kuantiti boleh dikemas kini secara manual seperti yang diperlukan.  |
| Jumlah ramalan sebenar        | Penugasan sumber dan anggaran perbelanjaan digunakan untuk menentukan jumlah amaun ramalan projek. Kos sebenar dibandingkan dengan ramalan ini untuk mengira kos untuk dilengkapkan.                                                                                                                                                                                                                                                                          |
| Seperti anggaran sebelumnya         | Kaedah anggaran sama yang digunakan dalam tempoh sebelumnya digunakan di sini. Kaedah ini memerlukan model ramalan jika tempoh sebelumnya memerlukan model ramalan.                                                                                                                                                                                                                                                                                                                           |
| Tetapkan kos untuk selesaikan kepada sifar | Lazimnya digunakan sebelum projek anggaran disingkirkan, kaedah ini sepadan dengan jumlah anggaran dengan transaksi sebenar yang disiarkan dan membersihkan lajur **Kos untuk melengkapkan**. Apabila selesai, hasilnya sentiasa 100 peratus. Untuk setiap baris kos yang anda cipta, kotak semak **Ramalan** telah dikosongkan dan jumlah anggaran disalin daripada anggaran kos sebelumnya. Penggunaan sebenar bagi tempoh anggaran ditolak daripada kos untuk selesaikan projek.              |
| Daripada templat kos           | Kos untuk melengkapkan kaedah yang disediakan dalam templat kos yang berkaitan dengan projek anggaran yang dipilih.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]