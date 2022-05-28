---
title: Jadual Perbelanjaan pertanyaan Anugerah Persekutuan
description: Topik ini menyediakan maklumat mengenai Jadual Perbelanjaan pertanyaan Anugerah Persekutuan.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b88c97f3dcb1020ccf17788256990485580f6964
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684469"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Jadual Perbelanjaan pertanyaan Anugerah Persekutuan

[!include [banner](../includes/banner.md)]

Menurut pejabat Pengurusan dan Pekeliling Belanjawan A-133, agensi yang menerima dana persekutuan adalah tertakluk kepada keperluan audit, yang juga dikenali sebagai audit tunggal. Proses audit digunakan untuk melaporkan hasil dan perbelanjaan pemberian persekutuan pada asas yang berulang. Sebahagian daripada laporan audit tunggal termasuk Jadual Perbelanjaan Anugerah Persekutuan (SEFA).

Jadual Perbelanjaan pertanyaan Anugerah Persekutuan termasuk tajuk dan nombor Katalog Bantuan Domestik Persekutuan (CFDA), nombor pemberian, tahun pemberian, nama agensi persekutuan yang menyediakan dana dan nama entiti serah semua. Pertanyaan adalah untuk tempoh tertentu. Lazimnya, tempoh tersebut adalah sama dengan tempoh penyata kewangan yang merupakan tahun fiskal.

Pertanyaan termasuk pemberian yang mempunyai tarikh unjuran dalam julat tarikh yang dipilih. Lajur **Agensi penerima** bagi pertanyaan menunjukkan pelanggan pemberian atau, untuk pemberian serah semua, agensi penerima. Untuk pemberian serah semua, lajur **Agensi serah semua** menunjukkan pelanggan pemberian. Jika pemberian bukan pemberian serah semua, lajur **Agensi serah semua** adalah kosong.

## <a name="set-up-the-cfda-clusters"></a>Sediakan kelompok CFDA

Anda mesti sediakan kelompok CFDA yang boleh dikaitkan dengan nombor CFDA dalam Jadual Perbelanjaan pertanyaan Anugerah Persekutuan.

1. Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Pemberian \> Katalog kelompok Bantuan Domestik Persekutuan**.
2. Pilih **Baharu** untuk mencipta kelompok CFDA.
3. Masukkan nama kelompok.
4. Pilih **Simpan** untuk menyimpan perubahan anda.

## <a name="set-up-cfda-numbers"></a>Sediakan nombor CFDA

Anda mesti sediakan nombor CFDA yang boleh ditambah untuk memberikan dan termasuk dalam pertanyaan Jadual Perbelanjaan Anugerah Persekutuan.

1. Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Geran \> Katalog nombor Bantuan Domestik Persekutuan**.
2. Pilih **Baharu** untuk mencipta nombor CFDA.
3. Dalam lajur **Nombor**, masukkan nombor CFDA.
4. Tekan kekunci **Tab**.
5. Dalam lajur **Description**, masukkan tajuk CFDA.
6. Tekan kekunci **Tab**.
7. Pilihan: Dalam medan **Kelompok program**, tambah kelompok CFDA yang sesuai.
8. Pilih **Simpan** untuk menyimpan perubahan anda.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Menyediakan geran untuk melapor untuk Jadual Perbelanjaan pertanyaan Anugerah Persekutuan

1. Pergi ke **Pengurusan dan perakaunan projek \> Geran \> Geran**, dan pilih geran sedia ada.
2. Pada FastTab **Persediaan**, dalam medan **Katalog Bantuan Domestik Persekutuan**, tugaskan nombor CFDA. Nombor CFDA pada geran menentukan kelompok CFDA untuk pelaporan.
3. Pada FastTab **Maklumat kenalan**, masukkan maklumat pemberi dengan mengikut langkah berikut:

    1. Dalam medan **Berikan pelanggan**, masukkan pelanggan yang bertanggungjawab untuk geran tersebut. Untuk geran sedia ada, maklumat ini mungkin telah dimasukkan.
    2. Menunjukkan sama ada pemberian pelanggan adalah pemberi dana. Jika pemberian pelanggan adalah pemberi dana, biarkan kotak semak **Serah semua** kosong. Jika pelanggan lain adalah pemberi dana, dan pelanggan pemberian bertanggungjawab untuk berbelanja dan menjejaki wang, pilih kotak semak **Serah semua**.

4. Jika anda memilih kotak semak **Serah semua** dalam langkah sebelumnya, dalam medan **Agensi pemberi**, masukkan pelanggan yang menyediakan pemberian tersebut. Agensi penerima dan pelanggan pemberian tidak boleh menjadi pelanggan yang sama.

Berikut ialah contoh pemberian serah semua:

Kerajaan persekutuan telah membiayai projek infrastruktur untuk keadaan. Kerajaan persekutuan memberikan wang kepada keadaan untuk berbelanja. Dalam hal ini, kerajaan persekutuan ialah agensi penerima, dan keadaan ini ialah pelanggan pemberian.

> [!NOTE] 
> Apabila anda terlebih dahulu menghidupkan ciri, nombor CFDA awal akan dimasukkan dengan menggunakan nombor sedia ada pada pemberian.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Kecualikan pemberian daripada pelaporan SEFA berdasarkan jenis pemberian

1. Pergi ke **Pengurusan dan perakaunan projek \> Persediaan \> Pemberian \> Jenis pemberian**.
2. Pada FastTab **Maklumat lalai**, pilih kotak semak **Kecualikan daripada Jadual Perbelanjaan Anugerah Persekutuan**.
3. Pilih **Simpan** untuk menyimpan perubahan anda.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Jalankan Jadual Perbelanjaan pertanyaan Anugerah Persekutuan

1. Pergi ke **Pengurusan dan perakaunan projek \> Pertanyaan dan laporan \> Pertanyaan pemberian \> Jadual Perbelanjaan Anugerah Persekutuan**.
2. Dalam bahagian **Parameter**, ikuti langkah ini:

    1. Dalam medan **Selang tarikh**, pilih kod untuk selang tarikh. Sebagai alternatif, pada medan **Daripada tarikh** dan **Hingga Tarikh**, takrifkan selang tarikh.
    2. Pilihan: Untuk memasukkan hanya transaksi yang dibilkan sebagai pendapatan dalam pertanyaan, tetapkan pilihan **Termasuk hasil dibilkan sahaja** kepada **Ya**.

## <a name="columns"></a>Lajur

Jadual Perbelanjaan pertanyaan Anugerah Persekutuan termasuk lajur berikut:

- Katalog nama kelompok Bantuan Domestik Persekutuan
- Agensi pemberi
- Agensi serah semua
- Nama pemberian
- ID pemberian
- ID aplikasi pemberian
- Katalog Bantuan Domestik Persekutuan
- Resit
- Perbelanjaan


[!INCLUDE[footer-include](../includes/footer-banner.md)]