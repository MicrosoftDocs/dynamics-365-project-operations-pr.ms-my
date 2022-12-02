---
title: Gunakan Tambahan Project Service untuk merancang kerja anda dalam Microsoft Project | MicrosoftDocs
description: Artikel ini memberikan maklumat tentang cara untuk menambah, mengkonfigurasi dan menggunakan tambahan Microsoft Project untuk Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925545"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Gunakan tambahan Project Service Automation untuk merancang kerja anda dalam Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] memudahkan anda membuat perancangan projek anda, termasuk anggaran. Anda boleh mentakrifkan kerja supaya nilai kos, usaha dan jualan jelas seperti cadangan akhir diserahkan.  

 Anda kini boleh memasang [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] dan melakukan kerja perancangan anda dalam persekitaran [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang biasa. Gunakan keupayaan perancangan dan pengurusan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang kukuh dan kemudian kemas kini rancangan projek anda dalam Project Service Automation.  

> [!IMPORTANT]
> - Untuk menggunakan pengurusan dokumen SharePoint bagi menyimpan fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pentadbir [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda perlu menghidupkan pengurusan dokumen. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] adalah satu-satunya yang serasi dengan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Muat turun dan pasang tambahan  
 Pastikan maklumat daftar masuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda tersedia. Anda akan memerlukan maklumat ini untuk menyambung daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Daripada Pusat Muat Turun, muat turun tambahan untuk versi Project Service anda yang disokong, sama ada [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) atau [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klik pautan muat turun.  

3.  Apabila muat turun selesai, klik **Ya** untuk memasang tambahan.  

## <a name="configure-the-add-in"></a>Konfigurasikan tambahan  

1. Buka [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan klik tab **Project Service**.  

2. Klik **Sambung**.  

3. Masukkan maklumat daftar masuk anda dan kemudian klik **Daftar Masuk**.  

   Anda boleh mula menggunakan tambahan sekarang.  

## <a name="read-from-a-template"></a>Baca daripada templat  
 Baca daripada templat yang anda cipta dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] disalin ke dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] untuk memulakan perancangan projek anda. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Cipta templat projek (Project Service Automation)](../psa/create-project-template.md)  

1.  Daripada tab **Project Service**, klik **Baca** > **Templat Projek bagi Project Service Automation**.  

2.  Pilih templat projek daripada senarai dan kemudian klik **Buka**.  

    > [!NOTE]
    >  Secara lalai, tugas yang disalin daripada templat ke dalam Projek ditetapkan seperti yang dijadualkan secara manual.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Untukkan peranan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada sumber projek  

1.  Buka projek dan klik reben **Tugas**.  

2.  Klik menu **Carta Gantt** dan kemudian pilih **Helaian Sumber**.  

3.  Pada Helaian Sumber, klik menu juntai bawah **Peranan Sumber Project Service** dan pilih peranan Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Tetapkan sumber untuk projek anda  

1.  Daripada tab Project Service, pilih baris dan klik **Cari Sumber**.  

2.  Pada skrin **Tempah Sumber**, pilih sumber yang anda mahu gunakan untuk projek.  

3.  Klik **Tempah** dan kemudian klik **OK**.  

## <a name="publish-your-project"></a>Terbitkan projek anda  
Apabila perancangan projek anda selesai, langkah seterusnya adalah untuk mengimport dan menerbitkan projek ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projek akan mengimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Proses penjanaan harga dan pasukan diguna pakai. Buka projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk melihat bahawa pasukan, anggaran projek dan struktur pecahan kerja telah dijanakan. Jadual berikut menunjukkan tempat untuk mencari hasil:

| Project | Details |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Carta Gantt**   | Mengimport ke dalam skrin **Struktur Pecahan Kerja** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Lembaran Sumber** |   Mengimport ke dalam skrin **Ahli Pasukan Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] .   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gunakan Penggunaan**    |    Import ke dalam skrin **Anggaran Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Untuk mengimport dan menerbitkan projek anda**  
1. Daripada tab **Project Service**, klik **Terbitkan** > **Projek Project Service Automation Baharu**.  

2. Pada kotak dialog **Terbitkan pada projek baharu dalam Project Service**, masukkan **Nama Projek** dan pilih **Pelanggan**.  

3. Secara pilihan, semak **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek rancangan kepada Project Service Automation.  

4. Klik **Terbitkan**.  

   Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.  Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Edit projek yang telah diimport  
 Untuk membuat perubahan kepada rancangan projek yang diimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], anda mempunyai dua pilihan:  

- Buka fail induk dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Nyahpaut fail dan edit ia secara terus dalam Project Service. Secara lalai, projek yang telah dimuat naik daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dikunci dan hanya boleh diedit dalam Projek. Untuk mengedit fail dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], fail perlu dinyahpautkan.  

### <a name="edit-in-pn_microsoft_project"></a>Edit dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Daripada menu utama, klik **Project Service** > **Projek**.  

2. Daripada senarai projek, buka projek yang anda cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klik **Buka dalam MS Project** daripada reben. Ini akan membuka fail induk yang dipautkan dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Nyahpautkan fail dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Daripada menu utama, klik **Project Service** > **Projek**.  

2. Daripada senarai projek, buka projek yang anda cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klik **Nyahpaut daripada MS Project** daripada reben.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Muat naik fail Projek ke SharePoint atau Kumpulan Office  
 Anda boleh memuat naik fail Projek anda ke SharePoint dan menemuinya di bawah Dokumen Berkaitan untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda.  Anda perlu meminta pentadbir anda mengkonfigurasikan pengurusan dokumen SharePoint dan menghidupkannya untuk entiti Projek. 

 Anda juga boleh memuat naik fail Projek anda kepada [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jika anda telah menyediakan Kumpulan Office.

### <a name="upload-a-file-for-sharepoint"></a>Muat naik fail untuk SharePoint  

1. Daripada menu utama, klik **Project Service** > **Muat Naik**.  

2. Pilih **Ke Dokumen Projek Project Service Automation**.  

3. Pada dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **Ya** atau **Tidak**.  

   - Jika anda klik **Ya**, anda akan dapat memilih butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, melancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.  

   - Jika anda klik **Tidak**, pautan untuk butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.  

4. Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.  

### <a name="upload-a-file-for-office-groups"></a>Muat naik fail untuk Kumpulan Office  

1. Daripada menu utama, klik **Project Service** > **Muat Naik**.  

2. Pilih **Ke Dokumen Projek Project Service Automation**.  

3. Pada dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **Ya** atau **Tidak**.  

   - Jika anda klik **Ya**, anda akan dapat memilih butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, melancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.  

   - Jika anda klik **Tidak**, pautan untuk butang **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.  

4. Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.  

## <a name="publish--your-project-as-a-template"></a>Terbitkan projek anda sebagai templat  
 Anda boleh menyimpan projek anda dan menggunakannya semula dengan menyimpannya sebagai templat projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Templat projek ialah rancangan projek yang boleh digunakan semula dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Cipta templat projek (Project Service Automation)](../psa/create-project-template.md)  

1. Daripada tab **Project Service**, klik **Terbitkan** > **Templat Projek bagi Project Service Automation Baharu**.  

2. Pada kotak dialog **Terbitkan ke projek baharu dalam templat Project Service**, masukkan **Nama templat projek**.  

3. Secara pilihan, semak **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Klik **Terbitkan**.  

Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam templat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.  Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Baca jadual yang dimuatkan sumber

Apabila membaca projek daripada Project Service Automation, kalendar sumber tidak disegerakkan dengan klien desktop. Jika terdapat perbezaan dalam tempoh, usaha atau tamat tugas, ia mungkin kerana sumber dan klien desktop tidak mempunyai kalendar templat waktu kerja yang sama yang digunakan pada projek.


## <a name="data-synchronization"></a>Penyegerakan Data

Jadual berikut menggariskan cara data disegerakkan antara Project Service Automation dengan tambahan desktop Microsoft Project.

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Tugas Projek | Tarikh Siap | ● | - |
| Tugas Projek | Anggaran Usaha | ● | - |
| Tugas Projek | ID Klien MS Project | ● | - |
| Tugas Projek | Tugas Induk | ● | - |
| Tugas Projek | Project | ● | - |
| Tugas Projek | Tugas projek | ● | - |
| Tugas Projek | Nama Tugas Projek | ● | - |
| Tugas Projek | Unit sumber (Ditamatkan dalam v3.0) | ● | - |
| Tugas Projek | Tempoh Dijadualkan | ● | - |
| Tugas Projek | Tarikh Mula | ● | - |
| Tugas Projek | ID WBS | ● | - |

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Ahli Pasukan | ID Klien MS Project | ● | - |
| Ahli Pasukan | Nama Kedudukan | ● | - |
| Ahli Pasukan | projek | ● | ● |
| Ahli Pasukan | Pasukan Projek | ● | ● |
| Ahli Pasukan | Unit Sumber | - | ● |
| Ahli Pasukan | Peranan | - | ● |
| Ahli Pasukan | Waktu Bekerja | Tidak disegerakkan | Tidak disegerakkan |

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Tugasan Sumber | Dari Tarikh | ● | - |
| Tugasan Sumber | Jam | ● | - |
| Tugasan Sumber | ID Klien MS Project | ● | - |
| Tugasan Sumber | Kerja Dirancang | ● | - |
| Tugasan Sumber | Project | ● | - |
| Tugasan Sumber | Pasukan Projek | ● | - |
| Tugasan Sumber | Tugasan Sumber | ● | - |
| Tugasan Sumber | Tugas | ● | - |
| Tugasan Sumber | Hingga Tarikh | ● | - |

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Kebergantungan Tugas Projek | Kebergantungan Tugas Projek | ● | - |
| Kebergantungan Tugas Projek | Jenis Pautan | ● | - |
| Kebergantungan Tugas Projek | Tugas Pendahulu | ● | - |
| Kebergantungan Tugas Projek | Project | ● | - |
| Kebergantungan Tugas Projek | Tugas Pengganti | ● | - |

### <a name="see-also"></a>Lihat Juga  
 [Panduan Pengurus Projek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
