---
title: Kos untuk melengkapkan kaedah
description: Topik ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531502"
---
# <a name="cost-to-complete-methods"></a>Kos untuk melengkapkan kaedah

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini memberikan maklumat tentang kaedah yang digunakan untuk mengira kos untuk melengkapkan projek. Terdapat berbilang kaedah yang boleh anda gunakan untuk mengira kos untuk melengkapkan projek. 

Apabila anda mencipta anggaran untuk projek, pada halaman **Cipta anggaran**, dalam medan **Kos untuk melengkapkan kaedah**, anda boleh memilih salah satu daripada kos berikut untuk melengkapkan kaedah.

| Kos untuk melengkapkan kaedah    | Penerangan                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jumlah kos sebenar            | Masukkan kos anggaran secara manual dalam medan **Jumlah kos** atau **Jumlah kuantiti** menggunakan butang **Anggaran kos** pada **Halaman anggaran**. Sistem menolak kos sebenar daripada jumlah yang anda masukkan. Jumlah ini merupakan kos untuk melengkapkan projek. Kaedah ini tidak menggunakan anggaran perbelanjaan dan penugasan sumber yang dimasukkan dalam Project Operations dibina dalam Microsoft Dataverse. Jumlah kos atau jumlah kuantiti boleh dikemas kini secara manual seperti yang diperlukan.  |
| Jumlah ramalan sebenar        | Penugasan sumber dan anggaran perbelanjaan digunakan untuk menentukan jumlah amaun ramalan projek. Kos sebenar dibandingkan dengan ramalan ini untuk mengira kos untuk dilengkapkan.                                                                                                                                                                                                                                                                          |
| Seperti anggaran sebelumnya         | Kaedah anggaran sama yang digunakan dalam tempoh sebelumnya digunakan di sini. Kaedah ini memerlukan model ramalan jika tempoh sebelumnya memerlukan model ramalan.                                                                                                                                                                                                                                                                                                                           |
| Tetapkan kos untuk selesaikan kepada sifar | Lazimnya digunakan sebelum projek anggaran disingkirkan, kaedah ini sepadan dengan jumlah anggaran dengan transaksi sebenar yang disiarkan dan membersihkan lajur **Kos untuk melengkapkan**. Apabila selesai, hasilnya sentiasa 100 peratus. Untuk setiap baris kos yang anda cipta, kotak semak **Ramalan** telah dikosongkan dan jumlah anggaran disalin daripada anggaran kos sebelumnya. Penggunaan sebenar bagi tempoh anggaran ditolak daripada kos untuk selesaikan projek.              |
| Daripada templat kos           | Kos untuk melengkapkan kaedah yang disediakan dalam templat kos yang berkaitan dengan projek anggaran yang dipilih.                                                                                                                                                                                                                                                                                                                                                                          |