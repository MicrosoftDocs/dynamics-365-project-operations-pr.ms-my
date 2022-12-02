---
title: Konsep utama dalam subkontrak
description: Artikel ini menerangkan beberapa konsep utama yang digunakan pada subkontrak dalam Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9577169f12198222e647ed07ae8a1b6c55da4323
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522760"
---
# <a name="key-concepts-in-subcontracting"></a>Konsep utama dalam subkontrak


_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

Artikel ini menerangkan beberapa konsep utama yang harus anda ketahui sebelum anda mula menggunakan fungsi subkontrak dalam Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unit kontrak pada subkontrak

Unit kontrak mewakili bahagian atau amalan yang memiliki pelaksanaan projek akhir. Unit kontrak juga merupakan bahagian yang mengikat kontrak dengan vendor.

## <a name="purchase-currency"></a>Mata wang pembelian

Dalam Project Operations, mata wang pembelian ialah mata wang yang digunakan dalam mencipta subkontrak. Ia juga merupakan mata wang yang direkodkan dalam kos subkontraktor untuk projek. Mata wang pembelian boleh berbeza daripada mata wang projek, dan mata wang projek, seterusnya, boleh berbeza daripada mata wang jualan.

## <a name="billing-methods-on-subcontract-lines"></a>Kaedah pengebilan pada baris subkontrak

Untuk projek, biasanya terdapat model kontrak berdasarkan penggunaan dan yuran tetap. Project Operations menyokong kaedah pengebilan ini dalam konteks jualan dan pembelian. Untuk pembelian, kaedah pengebilan berfungsi dengan cara berikut:

- **Masa dan Bahan** – Apabila baris subkontrak menggunakan kaedah pengebilan **Masa dan Bahan**, kos masa direkodkan pada projek semasa subkontraktor mengusahakan projek itu dan merekodkan masa. Transaksi kos daripada subkontraktor ini kemudian dipadankan dengan item baris pada invois vendor. Dalam model ini, pengurus projek yang menggunakan Project Operations boleh memadankan dan mengesahkan baris invois vendor dengan waktu subkontraktor yang direkodkan dan diluluskan. Setelah pengesahan selesai, aktual kos sebelumnya yang direkodkan selepas kelulusan diterbalikkan, dan aktual kos baru berdasarkan invois vendor dicipta pada projek.
- **Harga Tetap** – Dalam model kontrak yuran tetap ini, invois vendor adalah berdasarkan pencapaian tetap. Walau bagaimanapun, sumber subkontraktor juga boleh melaporkan masa. Masa tersebut kemudiannya disemak dan diluluskan oleh pengurus projek. Apabila ia diluluskan, Project Operations mencipta aktual kos sementara pada projek tersebut. Selepas vendor menghantar invois untuk pencapaian, pengurus projek boleh memadankan aktual kos yang telah direkodkan sebelumnya dengan pencapaian tersebut. Apabila pengesahan selesai, aktual kos akan diterbalikkan, dan kos berdasarkan pencapaian direkodkan.

## <a name="project-price-lists-on-subcontracts"></a>Senarai harga projek pada subkontrak

Senarai harga projek ialah senarai harga yang digunakan untuk menyediakan harga pembelian untuk masa, perbelanjaan, dan komponen lain yang berkaitan dengan projek. Boleh ada beberapa senarai harga, setiap satunya boleh mempunyai subkontrak berkuat kuasa tarikh ia sendiri dalam Project Operations. Project Operations tidak menyokong tarikh berkuat kuasa yang bertindih pada senarai harga projek untuk subkontrak.

## <a name="transaction-classes-on-subcontracts"></a>Kelas transaksi pada subkontrak

Project Operations menyokong empat jenis kelas transaksi:

- Masa
- Perbelanjaan
- Bahan
- Yuran

Kos pembelian boleh dianggarkan dan dikenakan hanya pada kelas transaksi **Masa**, **Perbelanjaan**, dan **Bahan**. **Yuran** ialah kelas transaksi hasil sahaja dan tidak tersedia dalam kandungan pembelian.

## <a name="purchase-pricing-dimensions"></a>Dimensi penentuan harga pembelian

Dimensi penentuan harga membolehkan anda menentukan atribut yang digunakan untuk penyediaan harga pembelian dan penetapan lalai pada transaksi masa. Berkaitan dengan pembelian, Project Operations hanya menyokong set dimensi tetap untuk penyediaan dan penetapan lalai harga pembelian. Bagi penyediaan dan penetapan lalai harga pembelian pada baris subkontrak dan transaksi masa subkontrak, atributnya ialah **Peranan** dan **Sumber Boleh Ditempah**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
