---
title: Ciri yang dialih keluar atau ditamatkan dalam Dynamics 365 Project Operations
description: Topik ini menerangkan ciri-ciri yang telah dikeluarkan, atau yang dirancang untuk penyingkiran dari Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601581"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Ciri yang dialih keluar atau ditamatkan dalam Dynamics 365 Project Operations

_**Digunakan pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma dan Project Operations untuk senario berasaskan stok/pengeluaran_

Topik ini menerangkan ciri-ciri yang telah dikeluarkan, atau yang dirancang untuk penyingkiran dari Dynamics 365 Project Operations.

- Ciri *dialih keluar* tidak lagi tersedia dalam produk.
- CIri *ditamatkan* bukan dalam pembangunan aktif dan mungkin akan dialih keluar dalam kemas kini yang akan datang.

Senarai ini bertujuan untuk membantu anda mempertimbangkan pengalihan keluar dan penamatan ini untuk perancangan anda sendiri.

> [!NOTE]
> Maklumat terperinci tentang objek dalam aplikasi Kewangan dan Operasi boleh didapati dalam [**laporan rujukan Teknikal**](/dynamics/s-e/global/axtechrefrep_61). Anda boleh membandingkan versi berbeza laporan ini untuk mengetahui tentang objek yang telah berubah atau telah dialih keluar dalam setiap versi aplikasi Kewangan dan Operasi.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Ciri-ciri yang dialih keluar atau ditamatkan dalam keluaran Operasi Projek Mac 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Pengurusan projek dan perakaunan "Sentiasa buat transaksi pelarasan" parameter

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Urus niaga pelarasan diperlukan untuk tujuan audit. Selepas penamatan, parameter ini akan disembunyikan. Sistem ini akan sentiasa membuat transaksi pelarasan, sama seperti yang berlaku pada masa ini apabila parameter ditetapkan kepada **Ya**. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Operasi Projek untuk senario pengeluaran/stok |
| **Status** | Ditamatkan: Menjelang 1 Mac 2023, kami akan menyembunyikan parameter dan mengubah tingkah laku sistem supaya transaksi pelarasan sentiasa dibuat. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Pengurusan projek dan perakaunan "Gunakan tarikh pelarasan sebagai tarikh projek baru" parameter

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Parameter ini pada asalnya digunakan untuk membenarkan pelarasan apabila tempoh fiskal ditutup. Walau bagaimanapun, ia tidak lagi diperlukan, kerana tarikh perakaunan transaksi boleh diubah kepada tarikh pertama tempoh terbuka, jika ia dikonfigurasikan. Tarikh projek tidak boleh diubah, kerana ia mewakili tarikh transaksi berlaku. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Operasi Projek untuk senario pengeluaran/stok |
| **Status** | Ditamatkan: Menjelang 1 Mac 2023, kami akan menyembunyikan parameter dan mengubah tingkah laku sistem supaya tarikh projek tidak pernah diubah pada pelarasan. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Aliran kerja permintaan sumber dalam Operasi Projek untuk senario berasaskan stok/pengeluaran

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana had penggunaan dan jumlah transaksi yang rendah. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Operasi Projek untuk senario pengeluaran/stok |
| **Status** | Ditamatkan: Menjelang 1 Mac 2023, kami akan menyahdayakan pilihan untuk meminta sumber untuk projek dengan menggunakan aliran kerja. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Halaman cadangan invois projek tanpa pandangan Pengepala dan Baris

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana penambahbaikan pada halaman yang diperkenalkan bersama-sama dengan **cadangan invois Gunakan Projek dan borang jurnal invois dengan kekunci ciri Pandangan** Pengepala dan Garis. |
| **Digantikan dengan ciri lain?** | Ya |
| **Kawasan produk terjejas** | Permohonan |
| **Pilihan pelaksanaan** | Operasi Projek untuk senario pengeluaran/stok; Operasi Projek untuk senario sumber/ bukan stok |
| **Status** | Ditamatkan: Menjelang 1 Mac 2023, kami akan mematikan halaman (legasi) yang lebih awal dan menghidupkan **borang Gunakan cadangan invois Projek dan jurnal invois dengan kekunci ciri paparan** Pengepala dan Baris secara lalai. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Ciri-ciri yang dialih keluar atau ditamatkan dalam keluaran Operasi Projek Disember 2021

### <a name="collaboration-workspaces"></a>Ruang kerja kerjasama

[Mencipta atau memaut ke ruang kerja kerjasama (Projek)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Sebab untuk penamatan/pengalihan keluar** | Ditamatkan kerana penggunaan yang rendah. Pelanggan yang menggunakan Project Operations untuk senario sumber/bukan stok boleh memanfaatkan [Kerjasama dengan Kumpulan](../project-management/collaboration-groups.md) Office. |
| **Digantikan dengan ciri lain?** | No |
| **Kawasan produk terjejas** | Permohonan  |
| **Pilihan pelaksanaan** | Operasi Projek untuk senario pengeluaran/stok |
| **Status** | Ditamatkan: Menjelang 1 Disember 2022, kami merancang untuk tidak lagi menyokong ruang kerja Kerjasama. |
