---
title: Gunakan Project Operations Lite
description: Artikel ini memberikan maklumat tentang cara memasang pelaksanaan Project Operations lite - urusan untuk penginvoisan proforma.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810990"
---
# <a name="deploy-project-operations-lite"></a>Gunakan Project Operations Lite

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_



Project Operations menyokong berbilang model pelaksanaan. Untuk menentukan model pelaksanaan terbaik, lihat [Jenis pelaksanaan](determine-deployment-type.md).


> [!IMPORTANT]
> Pelaksanaan ini, pelaksanaan Lite – urusan untuk penginvoisan proforma, keputusan dalam **Dataverse satu-satunya pelaksanaan Project Operations**.

- [Pasang Project Operations ke dalam persekitaran Dataverse baharu](#new)
- [Pasang ke dalam persekitaran Dataverse sedia ada](#existing)
- [Pasang ke persekitaran sedia ada Dataverse yang mempunyai komponen tulis dua](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Pasang Project Operations Lite ke persekitaran baharu Dataverse 

1. Sebagai [Pentadbir Global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cipta persekitaran Dataverse baharu dalam [pusat pentadbir PowerPlatform](https://admin.powerplatform.com). Pastikan bahawa **Cipta pangkalan data untuk persekitaran ini** dan **Aplikasi Dynamics 365** didayakan. Untuk mendapatkan maklumat lanjut, lihat [Cipta dan urus persekitaran dalam pusat pentadbir Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Pilih **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Pasang Project Operations Lite ke persekitaran yang sedia ada Dataverse  
1. Sebagai [Pentadbir global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cari persekitaran dalam [Pusat pentadbir Power Platform](https://admin.powerplatform.com) di tempat anda mahu memasang Project Operations.
1. Pasang **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365. Untuk mendapatkan maklumat lanjut, lihat [Urus aplikasi Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Pasang Project Operations Lite ke persekitaran sedia ada di mana penyelesaian Dwitulis sudah ada Dataverse 

Jika anda ingin terus menjalankan Operasi Projek dalam mod Penggunaan Lite, anda harus mengikuti langkah-langkah berikut:

1. Sebagai [Pentadbir global atau Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lesen Project Operations, cari persekitaran dalam [Pusat pentadbir Power Platform](https://admin.powerplatform.com) di tempat anda mahu memasang Project Operations.
1. Pasang **Microsoft Dynamics 365 Project Operations** daripada senarai pelaksanaan aplikasi Dynamics 365. Untuk mendapatkan maklumat lanjut, lihat [Urus aplikasi Dynamics 365](/power-platform/admin/manage-apps).
1. Oleh sebab persekitaran anda mempunyai Dwi tulis komponen yang membantu penyepaduan kepada aplikasi kewangan dan operasi dipasang, pemasangan Project Operations juga akan memasang keupayaan dan sambungan yang diperlukan untuk menyepadukan data berkaitan Projek ke aplikasi kewangan dan operasi. Oleh kerana anda ingin menjalankan Operasi Projek dalam penggunaan Lite, komponen integrasi ini harus dikeluarkan kerana ia akan membuat sekatan dan overhed untuk senario penggunaan Lite. Nyahpasang penyelesaian **Dynamics 365 Project Operations Secara manual Dwi Tulis dan** Peta **Dynamics 365 Project Operations Entiti Tulis** Dwi untuk mengalih keluar komponen ini.
1. Pergi ke **Operasi Projek -> Tetapan -> Parameter**.  **Buka halaman butiran Parameter** Projek dan setkan **medan Kelakuan** Naik Taraf Penyelesaian kepada **Lite Sahaja**. Ini memastikan bahawa sebarang peningkatan Operasi Projek seterusnya tidak akan mengembalikan komponen integrasi ke dalam Operasi Projek.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
