---
title: Model keselamatan
description: Topik ini memberikan maklumat tentang model keselamatan dalam Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642914"
---
# <a name="security-model"></a>Model Keselamatan

_**Gunakan Pada:** Project Operations untuk senario berasaskan sumber/bukan stok, pelaksanaan Ringan - urusan untuk penginvoisan proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations mengandungi model keselamatan unik yang membenarkan model keselamatan perniagaan berdasarkan peranan yang bekerjasama dengan Kumpulan Microsoft Office. 


## <a name="security-roles"></a>Peranan keselamatan
Project Operations keupayaan bahagian depan termasuk peranan berikut:

| Peranan                          | Penerangan                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Pengurus amalan              | Menyokong pelaporan merentas projek.                                                                                                            | Unit perniagaan              |
| Pelulus projek              | Meluluskan masa dan perbelanjaan terhadap projek.                                                                                                                              | Unit perniagaan |
| Pentadbir pengebilan projek | Cipta cadangan invois.                                                                                                                                                 | Unit perniagaan |
| Pengurus projek               | Cipta pelan projek dan sumber permintaan.                                                                                                                              | Unit perniagaan |
| Sumber projek              | Ahli pasukan yang boleh menempah dan melaporkan masa.                                                                                                          | Unit perniagaan|
| Resource manager              | Semua fungsi pengurusan sumber, seperti memenuhi permintaan sumber dan penempahan, diasingkan untuk menyokong konfigurasi Pengurus projek hibrid + Resource manager dan peranan Resource manager tunggal dan berpusat. | Unit perniagaan |


Microsoft Project untuk Web termasuk peranan berikut:

| Peranan           | Penerangan                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Pengguna projek   | Kerjasama pengguna Projek yang mampu mencipta projek mereka sendiri dan pandangan sebarang projek yang dikongsi dengan mereka. | Pengguna   |
| Sistem projek | Peranan yang digunakan untuk konteks aplikasi. Pelanggan tidak sepatutnya menggunakan peranan sistem ini.                                    | Global |

## <a name="security-enforcement"></a>Penguatkuasaan keselamatan
Tindakan yang dilakukan pada peringkat projek dilaksanakan dalam konteks pengguna log masuk. Ini bermaksud untuk mencipta, membuka, atau memadam projek, pengguna perlu mempunyai akses tersedia dalam CDS. Akses dalam CDS mungkin diberikan melalui sebarang mekanisma yang mungkin disertakan dalam platform. Contohnya, pengguna dengan skop yang lebih besar boleh mengakses projek atau jika tindakan perkongsian projek eksplisit telah dilaksanakan yang memberikan akses kepada pengguna.

Ia adalah penting untuk mempertimbangkan ini apabila mencipta projek dalam Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Kerjasama kumpulan moden dengan Project Operations
Projek untuk Web dan Project Operations menyokong kumpulan moden untuk kerjasama. Pengguna yang ditambah ke projek melalui kumpulan dapat mengedit pelan projek.

Projek untuk Web menambah pengguna kepada kumpulan secara automatik semasa penugasan.

Kumpulan membenarkan keizinan projek dan artifak kerjasama sokongan untuk dilakukan secara bekerjasama. Diagram berikut menggambarkan peristiwa dan perubahan keadaan yang berlaku semasa proses tugasan kumpulan.

Project Operations tidak mencipta kumpulan melalui tindakan tersirat dan hanya berbuat demikian melalui tindakan yang jelas dalam kumpulan yang mendesak.

Ahli kumpulan carian dalam dialog **Pengurusan kumpulan**, adalah terhad kepada mereka yang ditetapkan sebagai sebahagian daripada kumpulan keselamatan persekitaran. Untuk mendapatkan maklumat lanjut, lihat [Kawal akses pengguna kepada persekitaran: kumpulan keselamatan dan lesen](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Mod kumpulan](./media/groupsmode.png)

1. Projek dicipta dan dimiliki oleh Pengguna yang mencipta.
2. Pemilik projek dikemas kini kepada pasukan.
3. Pasukan pemilik dipetakan ke Kumpulan Pejabat yang ditentukan atau dicipta.
4. Pemilik asal projek ditambah ke Kumpulan Pejabat.

## <a name="deployment-recommendation"></a>Pengesyoran pelaksanaan
Sebagai model kerjasama Kumpulan pejabat yang berkembang, kefungsian akan ditambah untuk memberikan kawalan lebih terperinci mengikut masa. Pelanggan yang melaksanakan Project Operations hari ini digalakkan untuk fokus pada model keselamatan tradisional Microsoft Dynamics 365.

Untuk mendapatkan maklumat lanjut, lihat [Keselamatan dalam Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations dan keselamatan Microsoft Dynamics 365 Finance
Project Operations termasuk peranan berikut:

- Pengurus projek
- Akauntan projek

Untuk mendapatkan maklumat lanjut tentang keselamatan dalam Kewangan, lihat [Keselamatan berasaskan peranan](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


