---
title: Tentukan jenis pelaksanaan anda
description: Topik ini menyediakan maklumat untuk membantu anda menentukan jenis pelaksanaan Project Operations yang betul untuk syarikat anda.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081232"
---
# <a name="determine-your-deployment-type"></a>Tentukan jenis pelaksanaan anda

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

> [!IMPORTANT]
> Selepas anda membeli lesen, mulakan di sini untuk menentukan model pelaksanaan terbaik bagi Project Operations Dynamics 365 menggunakan [aliran pemasangan Dipandu](https://aka.ms/provisionprojectoperations).
> Selepas anda selesai membuat persediaan terhadap aliran pemasangan Dipandu, anda akan dihalakan ke portal pengurusan yang betul untuk melengkapkan pemasangan anda. Lihat butiran pelaksanaan untuk melengkapkan pemasangan.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Pelanggan sedia ada Dynamics menggunakan Dynamics 365 Project Service Automation
Project Operations termasuk keupayaan yang dihantar dengan Project Service Automation. Laluan naik taraf akan dilepaskan untuk pelanggan ini pada masa akan datang.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Pelanggan sedia ada Dynamics 365 Finance menggunakan pengurusan dan perakaunan Project 

Pelanggan Finance yang sedia ada yang menggunakan kefungsian Pengurusan dan perakaunan projek boleh terus menggunakan ini sebagaimana seadanya. Lihat [Project Operations untuk senario pesanan stok/pengeluaran](#pma).


## <a name="deployment-types"></a>Jenis pelaksanaan
Project Operations menyokong berbilang pilihan pelaksanaan untuk dipadankan dengan keperluan anda. Sama ada anda ialah pelanggan Dynamics 365 yang baharu atau sedia ada, Project Operations boleh menyokong keperluan anda.

[Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations) kami akan membantu anda menentukan pelaksanaan yang betul. Keputusan akan membimbing anda ke arah salah satu jenis pelaksanaan yang berikut:

- [Pelaksanaan ringan – tawaran sehingga penginvoisan proforma](#lite)
- [Project Operations untuk senario sumber/tidak distok](#integrated)
- [Project Operations untuk senario pesanan distok/pengeluaran](#pma)

Project Operations menyokong senario pesanan stok/pengeluaran dan senario yang berasaskan bukan stok/sumber dalam persekitaran yang sama melalui konfigurasi peringkat entiti yang sah. Sebagai contoh, Contoso boleh menggunakan keupayaan pesanan berstok/pengeluaran dalam kemudahan pengeluaran AS mereka (Entiti sah = Pengeluaran Amerika Syarikat Contoso). Contoso boleh menggunakan keupayaan tidak berstok/berasaskan sumber dalam kemudahan servis Lengan Robotik Contoso di UK (Entiti sah = Robotik United Kingdom Contoso).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Pelaksanaan ringan - urusan untuk penginvoisan proforma

Pelaksanaan Lite termasuk keupayaan berikut:

- Perancangan projek menggunakan Microsoft Project untuk Web
- Penentuan harga berbilang dimensi
- Pengurusan Sumber Disatukan
- Penjejakan Masa
- Perbelanjaan Asas
- Cadangan Invois

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](lite-preview-subscription-sign-up.md) dan [Persekitaran baharu peruntukan](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations untuk senario sumber/tidak distok
Project Operations untuk senario sumber/bukan stok termasuk keupayaan berikut:
  
- Perancangan projek menggunakan Microsoft Project untuk Web
- Penentuan harga berbilang dimensi
- Pengurusan Sumber Disatukan
- Penjejakan Masa
- Perbelanjaan Asas
- Perbelanjaan Penuh
- Penerimaan Pengesahan Pengembalian Barang (OCR)
- Penginvoisan Penuh
- Pengiktirafan Hasil

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](resource-sign-up-preview-subscription.md) dan [Persekitaran baharu peruntukan](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations untuk senario pesanan distok/pengeluaran

- Perancangan projek menggunakan WBS
- Pengurusan Sumber
- Penjejakan Masa
- Perbelanjaan Penuh
- Penerimaan Pengesahan Pengembalian Barang (OCR)
- Penginvoisan Penuh
- Pengiktirafan Hasil
- Pesanan Pengeluaran
- Sokongan bahan

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) dan [Persekitaran baharu peruntukan](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

