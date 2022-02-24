---
title: Terima item pada pesanan pembelian daripada keperluan item
description: Topik ini menerangkan cara untuk menerima item pada pesanan pembelian daripada keperluan item.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081395"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Terima item pada pesanan pembelian daripada keperluan item

[!include [banner](../../includes/banner.md)]

Topik ini menerangkan cara untuk menerima item pada pesanan pembelian daripada keperluan item.

Dengan menggunakan keperluan item berbanding transaksi item, anda boleh merancang untuk penghantaran hanya sebelum item itu sebenarnya digunakan, cipta pesanan pembelian, termasuk item dalam rangka kerja perjanjian perdagangan dan termasuk keperluan item dalam perancangan pengeluaran. 

Tugas ini menggunakan set data USSI.

1. Dalam anak tetingkap navigasi, pergi ke **Modul > Pengurusan dan perakaunan projek > Projek > Semua projek**.
2. Dalam senarai, pilih pautan dalam baris yang dikehendaki.
3. Pada Anak Tetingkap Tindakan, pilih **Pelan**.
4. Pilih **Keperluan item**.
5. Pilih **Baharu**.
6. Dalam baris baharu, masukkan atau pilih nilai dalam medan **Nombor item**.
7. Dalam medan **Kuantiti**, masukkan nombor.
8. Pilih **Simpan**.
9. Pada Anak Tetingkap Tindakan, pilih **Urus**.
10. Pilih **Fungsi**.
11. Pilih **Cipta pesanan pembelian**.
12. Pilih kotak semak **Masukkan semua**.
13. Dalam medan **Akaun vendor**, masukkan atau pilih nilai.
14. Pilih **OK**.
15. Dalam anak tetingkap navigasi, pergi ke **Modul > Akaun belum dibayar > Pesanan pembelian > Semua pesanan pembelian**.
16. Dalam senarai, pilih pautan dalam baris yang dikehendaki.
17. Pada Anak Tetingkap Tindakan, pilih **Beli**.
18. Pilih **Sahkan**.
19. Pada Anak Tetingkap Tindakan, pilih **Terima**.
20. Pilih **Resit produk**.
21. Dalam medan **Resit produk**, taipkan nilai.
22. Pilih **OK**.

