---
title: Perkara baharu Oktober 2022 - Pelaksanaan Project Operations lite
description: Artikel ini menyediakan maklumat tentang kemas kini kualiti yang tersedia dalam keluaran Microsoft lite keluaran Dynamics 365 Project Operations Oktober 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806763"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Perkara baharu Oktober 2022 - Pelaksanaan Project Operations lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Artikel ini digunakan pada komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Project Operations dalam persekitaran Dataverse versi 4.57.0.176

## <a name="features-included-in-this-release"></a>Ciri yang disertakan dalam keluaran ini

| Bahagian ciri | Nama ciri | Maklumat lanjut |
| --- | --- | --- |
| Perancangan dan Penjejakan Projek | **Penjadualan Luaran Operasi Projek**<br>Mod penjadualan luaran membolehkan pelanggan mencipta, mengemas kini dan memadam entiti yang berkaitan dengan struktur pecahan kerja (WBS) secara asli dengan menggunakan API asli Dataverse , tanpa had semasa yang dikuatkuasakan oleh Project for the Web. | [Penjadualan luaran](/dynamics365/project-operations/project-management/external-scheduling) |
| Pelaksanaan dan Konfigurasi | <p>**Benarkan pelanggan memilih jenis penggunaan**<br>Kemas kini dipacu produk (PDU) Operasi Projek digunakan untuk memasang penyelesaian dwi-tulis Operasi Projek secara automatik apabila penyelesaian teras dan orkestra dwi-tulis dipasang di persekitaran.</p><p>Ciri ini memperkenalkan parameter kelakuan **naik taraf Penyelesaian baru** dalam parameter Projek. Apabila parameter ini disetkan kepada **Lite sahaja**, PUD tidak lagi akan memasang penyelesaian dwi-tulis Operasi Projek secara automatik, walaupun penyelesaian teras dan orkestra dwi-tulis dipasang di persekitaran. Tingkah laku ini akan memberi manfaat kepada pelanggan yang merancang untuk menggunakan penyelesaian Dwi-tulis untuk mengintegrasikan pesanan jualan ke dalam aplikasi kewangan dan operasi, tetapi ingin menggunakan Operasi Projek dalam mod Lite (iaitu, tanpa penyepaduan ke dalam aplikasi kewangan dan operasi).</p> | |

## <a name="quality-updates"></a>Kemas kini kualiti

| Bahagian ciri | Nombor rujukan | Kemas kini kualiti |
| --- | --- | --- |
| Pengebilan dan Penentuan Harga | 2316317 | Sistem ini membolehkan invois dibuat yang tidak mempunyai transaksi yang boleh dikenakan bayaran. |
| Pengebilan dan Penentuan Harga | 2737300 | Sahkan ketersediaan medan Pelanggan sebelum borang diakses. |
| Pengebilan dan Penentuan Harga | 2744948 | Tambah semakan nol untuk kaedah Pengebilan. |
| Pengebilan dan Penentuan Harga | 2763515 | Ralat rujukan nol mengendalikan apabila kontrak jualan invois hilang. |
| Pengebilan dan Penentuan Harga | 2844301 | Penciptaan invois kumpulan gagal kerana ralat. |
| Pengebilan dan Penentuan Harga | 2845869 | Penyimpanan Perkhidmatan Organisasi yang tidak betul. |
| Pengebilan dan Penentuan Harga | 2853729 | Butiran peranan dan harga dikemas kini apabila jenis Pengebilan diubah suai. |
| Pengebilan dan Penentuan Harga | 2940350 | Apabila harga sebenar ditetapkan, hanya senarai harga aktif yang perlu dimasukkan secara automatik. |
| Pelaksanaan dan Konfigurasi | 3001206 | Entiti replaylogheader msdyn\_ menghalang peningkatan Organisasi Pelanggan. |
| Pengurusan Peluang | 2755582 | Pemegang pengecualian rujukan nol dalam Pembantu Peraturan Pengebilan Pisah. |
| Pengurusan Peluang | 2761477 | Apabila pengebilan berpecah digunakan, pemadaman peristiwa penting (header) meninggalkan tonggak anak yatim. |
| Pengurusan Peluang | 2767595 | Apabila rekod penggunaan bahan dibuka dalam bentuk utama, sumber Boleh Ditempah untuk rekod diubah kepada pengguna yang didaftar masuk pada masa ini. |
| Perancangan dan Penjejakan Projek | 2790384 | Masa keluar Pending OperationSet terlalu pendek. |
| Pengurusan Sumber | 2751560 | Unit Organisasi Pilihan yang Tidak Konsisten dalam Keperluan Sumber. |
| Pemberian subkontrak | 2907231 | Peringkat proses invois vendor tidak boleh maju. |
| Masa dan Perbelanjaan | 2867363 | Rekod tidak termasuk dalam pandangan Ketidakhadiran/Percutian untuk Kelulusan apabila mereka beratur untuk kelulusan. |
| Masa dan Perbelanjaan | 2894405 | TESA: Direktori POC yang tidak digunakan menyebabkan isu pematuhan. |
