---
title: Cipta invois proforma manual - ringan
description: Topik ini menyediakan maklumat tentang mencipta invois proforma manual dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176397"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Cipta invois proforma manual - ringan

_**Gunakan Kepada:** Pelaksanaan ringan - urusan dengan invois proforma_

Dalam Dynamics 365 Project Operations, invois proforma boleh dicipta secara manual apabila diperlukan. Anda boleh mencipta invois proforma secara manual daripada halaman senarai **Kontrak Projek** atau daripada halaman butiran **Kontrak Projek**.

##  <a name="project-contracts-list-page"></a>Halaman senarai Kontrak Projek

Daripada halaman senarai **Kontrak Projek**, pilih satu atau lebih kontrak projek dan cipta invois untuk semua rekod yang dipilih.

Sistem menyemak untuk melihat kontrak projek yang dipilih yang mempunyai tunggakan **Bersedia untuk Invois** bertarikh sebelum tarikh hari ini. Daripada kontrak tersebut, sistem mencipta invois proforma draf. Jika kontrak projek mempunyai berbilang pelanggan, mungkin terdapat satu invois yang dicipta bagi setiap pelanggan dan berbilang invois bagi setiap kontrak projek.

Semua invois projek yang dicipta tersedia pada halaman **Invois** dalam bahagian **Pengebilan** bagi kawasan **Jualan**.

## <a name="project-contract-details-page"></a>Halaman butiran Kontrak Projek

Invois proforma juga boleh dicipta daripada halaman butiran **Kontrak Projek**, yang mencipta invois untuk kontrak projek khusus tersebut. Sistem mengesahkan bahawa kontrak projek mempunyai tunggakan **Bersedia untuk Invois** yang bertarikh sebelum tarikh hari ini. Daripada kontrak ini, sistem mencipta invois proforma draf berdasarkan bilangan pelanggan pada setiap baris kontrak.

Apabila terdapat invois proforma tunggal yang dicipta, halaman **Invois** dibuka. Jika terdapat berbilang invois yang dicipta untuk kontrak projek tersebut, maka halaman senarai **Invois** dibuka untuk menunjukkan semua invois yang dicipta.
