---
title: Pemulihan VAT dalam Pengurusan perbelanjaan
description: Topik ini menerangkan cara untuk menerima bayaran balik pada transaksi cukai (VAT) nilai ditambah yang layak.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081096"
---
# <a name="vat-recovery-in-expense-management"></a>Pemulihan VAT dalam Pengurusan perbelanjaan

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menerima bayaran balik bagi transaksi cukai (VAT) nilai ditambah yang layak, syarikat atau organisasi mesti mengenal pasti, mengumpul, mengesahkan, dan menyerahkan maklumat yang tepat. Proses ini termasuk berbilang tugas dan, bergantung pada saiz syarikat anda, boleh termasuk beberapa pekerja atau peranan.

Untuk memulihkan VAT dalam modul **Pengurusan perbelanjaan**, prasyarat berikut mesti dilengkapkan:

- Kod cukai mesti dicipta untuk negara/rantau yang diperuntukkan kepada kategori perbelanjaan.
- Kumpulan cukai jualan mesti dicipta untuk setiap kod cukai.
- Item kod cukai jualan mesti dicipta untuk setiap kumpulan cukai jualan.

Selepas prasyarat dilengkapkan, langkah berikut mesti dilengkapkan untuk meminta bayaran balik untuk transaksi VAT.

1. Pada laporan perbelanjaan, masukkan maklumat cukai tentang transaksi kad kredit untuk mengenal pasti bayaran balik VAT yang layak.
2. Sahkan bahawa semua maklumat cukai lengkap, dan kemudian siaran laporan perbelanjaan.
3. Memproses perbelanjaan yang layak untuk pemulihan VAT antarabangsa.
4. Hantar data pemulihan VAT kepada vendor pihak ketiga untuk memfailkan pulangan pemulihan antarabangsa.
5. Memproses perbelanjaan untuk pemulihan VAT domestik.

Seksyen berikut memberikan contoh yang menunjukkan cara pekerja Ariffin melengkapkan setiap langkah.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Masukkan maklumat cukai tentang transaksi kad kredit untuk mengenal pasti bayaran balik VAT yang layak

Siah, wakil jualan Ariffin yang berpangkalan di Amerika Syarikat, baru-baru ini kembali daripada perjalanan jualan ke United Kingdom. Semasa perjalanan, Siah menanggung perbelanjaan kad kredit peribadi untuk makanan. Siah kini perlu mencipta laporan perbelanjaan untuk menyelesaikan perbelanjaan.

Apabila Siah memasukkan maklumat pada laporan perbelanjaan, dia memilih **United Kingdom** dalam medan **Negara/rantau** pada halaman **Edit laporan perbelanjaan**. Senarai kumpulan cukai jualan kemudiannya ditapis supaya menunjukkan hanya kumpulan yang diguna pakai di United Kingdom. Siah memilih **United Kingdom 001** kumpulan cukai jualan dan kemudian memilih **Makanan** item kumpulan cukai jualan. Seterusnya, Siah menambah transaksi baharu untuk penginapan. Kerana hanya ada satu kumpulan cukai jualan dan satu item kumpulan cukai jualan untuk penginapan di United Kingdom, maklumat ini secara automatik diisi dalam laporan perbelanjaan Siah.

Setiap dasar Ariffin, semua perbelanjaan mesti mempunyai resit pemadanan. Oleh itu, apabila Siah menyimpan laporan perbelanjaan, dia menerima mesej yang menyatakan bahawa dia mesti melampirkan resit untuk setiap transaksi yang dia senaraikan dalam laporan perbelanjaannya. Siah mengesahkan bahawa dia telah melampirkan imej digital setiap resit transaksi ke laporan perbelanjaannya dan kemudian menyerahkan laporan untuk kelulusan. Dia kemudian menghantar resit kertas kepada pasukan pemprosesan pejabat sokongan. Pasukan ini akan menghantar data pemulihan VAT kepada vendor pihak ketiga yang menfailkan pulangan pemulihan VAT antarabangsa untuk Ariffin.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Sahkan maklumat cukai dan siaran laporan perbelanjaan

Sebelum April, penyelaras Akaun belum bayar untuk Ariffin, boleh menyiarkan laporan perbelanjaan, dia mesti memasukkan sebarang maklumat cukai yang hilang daripadanya. Dia membuka halaman **Butiran laporan perbelanjaan** dan melihat laporan perbelanjaan diluluskan oleh Siah. April kemudian buka laporan perbelanjaan untuk melihat butiran transaksi. Dia melihat bahawa Siah tidak memasukkan item kumpulan cukai jualan untuk salah satu transaksi. Oleh kerana maklumat ini tidak diberikan, April tidak boleh menyiarkan laporan perbelanjaan. Oleh itu, dia melihat pada halaman **Konfigurasi cukai** dalam Pengurusan perbelanjaan, dan menemui item kumpulan cukai jualan yang sesuai untuk negara/rantau dan jenis transaksi. April kini boleh menyiarkan laporan perbelanjaan kepada lejar umum.

Apabila April menyiarkan laporan perbelanjaan, item kerja pemulihan VAT dicipta. Item kerja ini ditugaskan kepada ahli pasukan pemprosesan pejabat sokongan. April menerima mesej yang mengesahkan bahawa siaran berjaya. Mesej ini juga menyenaraikan bilangan transaksi VAT yang dikenal pasti untuk pemulihan.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Memproses perbelanjaan yang layak untuk pemulihan VAT antarabangsa

Arnie, ahli pasukan pemprosesan pejabat sokongan Ariffin, bertanggungjawab untuk mengesahkan bahawa semua maklumat yang diperlukan untuk pemulihan VAT dimasukkan dalam laporan perbelanjaan. Dia membuka halaman **Pemulihan cukai perbelanjaan** dan memilih laporan perbelanjaan yang Siah serahkan. Arnie kemudian mengesahkan bahawa semua resit yang diperlukan dilampirkan, dan kumpulan cukai jualan yang betul dan item kod cukai jualan dimasukkan.

Apabila Arnie menerima resit kertas daripada Siah, dia mengesahkannya daripada resit digital dan kemudian mengubah status laporan perbelanjaan kepada **Sedia untuk pemulihan**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Hantar data pemulihan VAT kepada vendor pihak ketiga

Apabila Arnie bersedia untuk menghantar data laporan perbelanjaan kepada vendor pihak ketiga yang akan memfailkan pulangan pemulihan VAT, dia membuka halaman **Pemulihan cukai perbelanjaan**. Dia menapis halaman supaya ia menunjukkan hanya laporan perbelanjaan yang ditandakan sebagai **Sedia untuk pemulihan**. Arnie kemudian pilih **Fail** &gt; **Eksport fail ke Excel**. Maklumat VAT daripada laporan perbelanjaan dieksport ke lembaran kerja Microsoft Excel. Arnie menyerahkan lembaran kerja ini kepada vendor pihak ketiga dan memasukkan mesej yang menyatakan resit kertas telah dihantar melalui kurier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Memproses perbelanjaan untuk pemulihan VAT domestik

Arnie mesti mengesahkan bahawa transaksi laporan perbelanjaan adalah layak untuk pemulihan VAT, dan resit digital dilampirkan pada laporan tersebut. Untuk mula memproses perbelanjaan yang layak untuk pemulihan domestik, Arnie membuka halaman **Pemulihan cukai perbelanjaan** dan memilih laporan perbelanjaan yang memerlukan pengesahan. Dia mengesahkan bahawa resit adalah atas nama syarikat dan bukannya pekerja. (Untuk pemulihan VAT, resit mestilah atas nama syarikat.) Arnie kemudian mengesahkan bahawa kumpulan cukai jualan yang betul dan item kod cukai jualan dimasukkan.

Apabila Arnie menerima resit kertas, dia mengubah status laporan perbelanjaan kepada **Sedia untuk pemulihan**. Dia kemudian boleh memfailkan pulangan dengan pihak berkuasa cukai yang berkenaan. Dalam kes ini, pihak berkuasa cukai yang berkenaan di Amerika Syarikat ialah Internal Revenue Service (IRS).
