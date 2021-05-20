---
title: Tentukan jenis pelaksanaan anda
description: Topik ini menyediakan maklumat untuk membantu anda menentukan jenis pelaksanaan Project Operations yang betul untuk syarikat anda.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948120"
---
# <a name="determine-your-deployment-type"></a>Tentukan jenis pelaksanaan anda

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

> [!IMPORTANT]
> Selepas anda membeli lesen, mulakan di sini untuk menentukan model pelaksanaan Dynamics 365 Project Operations menggunakan [Aliran pemasangan berpandu](https://aka.ms/provisionprojectoperations).
> Selepas anda selesai membuat persediaan terhadap aliran pemasangan Dipandu, anda akan dihalakan ke portal pengurusan yang betul untuk melengkapkan pemasangan anda. Lihat butiran pelaksanaan untuk melengkapkan pemasangan.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Pelanggan sedia ada Dynamics menggunakan Dynamics 365 Project Service Automation
Project Operations termasuk keupayaan yang dihantar dengan Project Service Automation. Laluan naik taraf akan dilepaskan untuk pelanggan dalam 2021 release wave 1.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Pelanggan sedia ada Dynamics 365 Finance menggunakan pengurusan dan perakaunan Project 

Pelanggan sedia ada Kewangan yang menggunakan fungsi Pengurusan projek dan perakaunan boleh terus menggunakannya seperti itu. Lihat [Project Operations untuk senario pesanan stok/pengeluaran](#pma).


## <a name="deployment-regions"></a>Rantau pelaksanaan
Untuk menentukan rantau yang menyokong pelaksanaan Project Operations, lihat [Ketersediaan geografi untuk laporan Dynamics 365 dan Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Pilih **Lihat Laporan,** dan kembangkan **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** untuk melihat rantau yang disokong.

## <a name="deployment-types"></a>Jenis pelaksanaan
Project Operations menyokong berbilang pilihan pelaksanaan untuk dipadankan dengan keperluan anda. Sama ada anda ialah pelanggan Dynamics 365 yang baharu atau sedia ada, Project Operations boleh menyokong keperluan anda.

[Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations) kami akan membantu anda menentukan pelaksanaan yang betul. Keputusan akan membimbing anda ke arah salah satu jenis pelaksanaan yang berikut:

- [Pelaksanaan ringan – tawaran sehingga penginvoisan proforma](#lite)
- [Project Operations untuk senario sumber/tidak distok](#integrated)
- [Project Operations untuk senario pesanan distok/pengeluaran](#pma)

Project Operations menyokong senario pesanan stok/pengeluaran dan senario yang berasaskan bukan stok/sumber dalam persekitaran yang sama melalui konfigurasi peringkat entiti yang sah. Contohnya, Contoso boleh menggunakan keupayaan pesanan stok/pengeluaran di fasiliti pembuatan AS mereka (Entiti sah = Contoso Manufacturing Amerika Syarikat). Contoso boleh menggunakan keupayaan berasaskan bukan stok/sumber di fasiliti Contoso Robotics Arms mereka di UK (Entiti sah = Contoso Robotics United Kingdom).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Pelaksanaan ringan - urusan untuk penginvoisan proforma

Pelaksanaan Lite termasuk keupayaan berikut:

- Proses jualan projek yang meluas pengalaman aplikasi Dynamics 365 Sales
- Perancangan projek menggunakan Microsoft Project untuk Web
- Penentuan harga berbilang dimensi
- Pengurusan sumber disatukan
- Penjejakan masa
- Perbelanjaan asas
- Penginvoisan proforma untuk semakan dan edit Pengurus projek 

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](lite-preview-subscription-sign-up.md) dan [Persekitaran baharu peruntukan](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations untuk senario sumber/tidak distok
Project Operations untuk senario sumber/bukan stok termasuk keupayaan berikut:
 
- Proses jualan projek yang meluaskan aplikasi Dynamics 365 Sales
- Perancangan projek menggunakan Microsoft Project untuk Web
- Penentuan harga berbilang dimensi
- Pengurusan sumber disatukan
- Penjejakan masa
- Perbelanjaan asas
- Perbelanjaan penuh
- Penerimaan Pengesahan Pengembalian Barang (OCR)
- Proforma dan penginvoisan menghadapi pelanggan 
- Pengiktirafan hasil untuk projek

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](resource-sign-up-preview-subscription.md) dan [Persekitaran baharu peruntukan](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations untuk senario pesanan distok/pengeluaran

- Perancangan projek menggunakan WBS
- Pengurusan sumber
- Penjejakan masa
- Perbelanjaan penuh
- Penerimaan Pengesahan Pengembalian Barang (OCR)
- Penginvoisan penuh
- Pengiktirafan hasil
- Pesanan pengeluaran
- Sokongan bahan stok dengan inventori

#### <a name="deployment-steps"></a>Langkah pelaksanaan
Tentukan model pelaksanaan Project Operations terbaik menggunakan [Soal selidik pelaksanaan](https://aka.ms/provisionprojectoperations).

Untuk pelaksanaan ini, lihat [Pendaftaran untuk langganan pratonton](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) dan [Persekitaran baharu peruntukan](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]