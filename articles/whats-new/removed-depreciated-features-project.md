---
title: Ciri dialih keluar atau ditamatkan dalam Dynamics 365 Project Operations
description: Artikel ini menerangkan ciri yang telah dialih keluar atau yang dirancang untuk pengalihan keluar daripada Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028340"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Ciri dialih keluar atau ditamatkan dalam Dynamics 365 Project Operations

_**Digunakan pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma dan Project Operations untuk senario berasaskan stok/pengeluaran_

Artikel ini menerangkan ciri yang telah dialih keluar atau yang dirancang untuk pengalihan keluar daripada Dynamics 365 Project Operations.

- Ciri *dialih keluar* tidak lagi tersedia dalam produk.
- CIri *ditamatkan* bukan dalam pembangunan aktif dan mungkin akan dialih keluar dalam kemas kini yang akan datang.

Senarai ini bertujuan untuk membantu anda mempertimbangkan pengalihan keluar dan penamatan ini untuk perancangan anda sendiri.

> [!NOTE]
> Maklumat terperinci tentang objek dalam aplikasi kewangan dan operasi boleh didapati dalam [**Laporan rujukan teknikal**](/dynamics/s-e/global/axtechrefrep_61). Anda boleh membandingkan versi berbeza bagi laporan ini untuk mengetahui tentang objek yang telah berubah atau dialih keluar dalam setiap versi aplikasi kewangan dan operasi.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Ciri dialih keluar atau ditamatkan dalam Project Operations keluaran Mac 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameter "Sentiasa cipta urus niaga pelarasan" pengurusan projek dan perakaunan

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Urus niaga pelarasan diperlukan untuk tujuan audit. Selepas penamatan, parameter ini akan disembunyikan. Sistem akan sentiasa mencipta urus niaga pelarasan, sama seperti biasa apabila parameter ditetapkan kepada **Ya**. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Project Operations untuk senario pesanan pengeluaran/stok |
| **Status** | Ditamatkan: Pada 1 Mac 2023, kami akan menyembunyikan parameter dan mengubah tingkah laku sistem supaya urus niaga pelarasan sentiasa dicipta. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parameter "Gunakan tarikh pelarasan sebagai tarikh projek baharu" pengurusan projek dan perakaunan

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Parameter ini pada asalnya digunakan untuk membenarkan pelarasan apabila tempoh fiskal ditutup. Walau bagaimanapun, parameter ini tidak diperlukan lagi, kerana tarikh perakaunan urus niaga boleh ditukar kepada tarikh pertama tempoh terbuka, jika dikonfigurasikan. Tarikh projek tidak boleh ditukar kerana tarikh itu mewakili tarikh apabila urus niaga berlaku. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Project Operations untuk senario pesanan pengeluaran/stok |
| **Status** | Ditamatkan: Pada 1 Mac 2023, kami akan menyembunyikan parameter dan mengubah tingkah laku sistem supaya tarikh projek tidak akan ditukar semasa pelarasan. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Aliran kerja permintaan sumber dalam Project Operations untuk senario berasaskan stok/pengeluaran

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana penggunaan rendah dan had jumlah urus niaga. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Project Operations untuk senario pesanan pengeluaran/stok |
| **Status** | Ditamatkan: Pada 1 Mac 2023, kami akan menyahdayakan pilihan untuk meminta sumber bagi projek menggunakan aliran kerja. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Halaman cadangan invois projek tanpa pandangan Pengepala dan Baris

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana peningkatan pada halaman yang diperkenalkan bersama dengan kekunci ciri **Gunakan cadangan invois Projek dan borang jurnal invois dengan pandangan Pengepala dan Baris**. |
| **Digantikan dengan ciri lain?** | Ya |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Project Operations untuk senario pengeluaran/stok; Project Operations untuk senario sumber/ bukan stok |
| **Status** | Ditamatkan: Pada 1 Mac 2023, kami akan mematikan halaman (legasi) awal dan menghidupkan kekunci ciri **Gunakan cadangan invois Projek dan borang jurnal invois dengan pandangan Pengepala dan Baris** secara lalai. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Ciri dialih keluar atau ditamatkan dalam Project Operations keluaran Disember 2021

### <a name="collaboration-workspaces"></a>Ruang kerja kerjasama

[Cipta atau pautkan pada ruang kerja kerjasama (Projek)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana penggunaan rendah. Pelanggan yang menggunakan Project Operations untuk senario sumber/bukan stok boleh memanfaatkan [Kerjasama dengan Kumpulan Pejabat](../project-management/collaboration-groups.md). |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan  |
| **Pilihan pelaksanaan** | Project Operations untuk senario pesanan pengeluaran/stok |
| **Status** | Ditamatkan: Pada 1 Disember 2022, kami merancang untuk tidak lagi menyokong ruang kerja Kerjasama. |
