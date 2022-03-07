---
title: Rancang kerja anda dalam Microsoft Project dengan tambahan Project Service
description: Topik ini memberikan maklumat tentang cara untuk menggunakan tambahan Microsoft Project untuk Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 471d3c421cd9dc39a5864e37ef762b5d08e59762
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285539"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Rancang kerja anda dalam Microsoft Project dengan tambahan Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] memudahkan anda membuat perancangan projek anda, termasuk anggaran. Anda boleh mentakrifkan kerja supaya nilai kos, usaha dan jualan jelas seperti cadangan akhir diserahkan.  

Anda boleh memasang [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] dan melakukan kerja perancangan anda dalam persekitaran [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang biasa. Gunakan keupayaan perancangan dan pengurusan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yang kukuh dan kemudian kemas kini rancangan projek anda dalam Project Service Automation.  

> [!IMPORTANT]
> - Untuk menggunakan pengurusan dokumen SharePoint bagi menyimpan fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], pentadbir [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] anda perlu menghidupkan pengurusan dokumen. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] adalah satu-satunya yang serasi dengan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Muat turun dan pasang tambahan  
 Pastikan maklumat daftar masuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda tersedia. Anda akan memerlukan maklumat ini untuk menyambung daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Daripada Pusat Muat Turun, muat turun tambahan untuk versi Project Service anda yang disokong, sama ada [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) atau [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Pilih pautan muat turun.  

3.  Apabila muat turun selesai, pilih **Ya** untuk memasang tambahan.  

## <a name="configure-the-add-in"></a>Konfigurasikan tambahan  

1. Buka [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan pilih tab **Project Service**.  

2. Pilih **Connect**.  

3. Masukkan maklumat daftar masuk anda dan kemudian pilih **Daftar Masuk**.  

   Anda boleh mula menggunakan tambahan sekarang.  

## <a name="read-from-a-template"></a>Baca daripada templat  
 Baca daripada templat yang anda cipta dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] disalin ke dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] untuk memulakan perancangan projek anda. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Cipta templat projek (Project Service Automation)](../psa/create-project-template.md)  

1.  Daripada tab **Project Service**, pilih **Baca** > **Templat Projek bagi Project Service Automation**.  

2.  Pilih templat projek daripada senarai dan kemudian pilih **Buka**.  

    > [!NOTE]
    >  Secara lalai, tugas yang disalin daripada templat ke dalam Projek ditetapkan seperti yang dijadualkan secara manual.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Untukkan peranan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada sumber projek  

1.  Buka projek dan pilih reben **Tugas**.  

2. Pilih menu **Carta Gantt** dan kemudian pilih **Helaian Sumber**.  

3. Pada Helaian Sumber, pilih menu juntai bawah **Peranan Sumber Project Service** dan pilih peranan Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Tetapkan sumber untuk projek anda  

1.  Daripada tab Project Service, pilih baris dan pilih **Cari Sumber**.  

2.  Pada skrin **Tempah Sumber**, pilih sumber yang anda mahu gunakan untuk projek.  

3.  Pilih **Tempah** dan kemudian pilih **OK**.  

## <a name="publish-your-project"></a>Terbitkan projek anda  
Apabila perancangan projek anda selesai, langkah seterusnya adalah untuk mengimport dan menerbitkan projek ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projek akan mengimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Proses penjanaan harga dan pasukan diguna pakai. Buka projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk melihat bahawa pasukan, anggaran projek dan struktur pecahan kerja telah dijanakan. Jadual berikut menunjukkan tempat untuk mencari hasil.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Carta Gantt**   | Mengimport ke dalam skrin **Struktur Pecahan Kerja** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Lembaran Sumber** |   Mengimport ke dalam skrin **Ahli Pasukan Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] .   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gunakan Penggunaan**    |    Import ke dalam skrin **Anggaran Projek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Untuk mengimport dan menerbitkan projek anda**  
1. Pada tab **Project Service**, pergi ke **Terbitkan** > **Projek Project Service Automation Baharu**.  

2. Dalam kotak dialog **Terbitkan pada projek baharu dalam Project Service**, masukkan **Nama Projek** dan pilih **Pelanggan**.  

3. Secara pilihan, pilih **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek rancangan kepada Project Service Automation.  

4. Pilih **Terbitkan**.  

   Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.  Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Edit projek yang telah diimport  
 Untuk membuat perubahan kepada rancangan projek yang diimport ke dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], anda mempunyai dua pilihan:  

- Buka fail induk dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Nyahpaut fail dan edit ia secara terus dalam Project Service. Secara lalai, projek yang telah dimuat naik daripada [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dikunci dan hanya boleh diedit dalam Projek. Untuk mengedit fail dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], fail perlu dinyahpautkan.  

### <a name="edit-in-pn_microsoft_project"></a>Edit dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Pada menu utama, pergi ke **Project Service** > **Projek**.  

2. Daripada senarai projek, buka projek yang anda telah cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Pilih **Buka dalam MS Project** daripada reben. Ini akan membuka fail induk yang dipautkan dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Nyahpautkan fail dan edit ia dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Pada menu utama, pergi ke **Project Service** > **Projek**.  

2. Daripada senarai projek, buka projek yang anda telah cipta dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Pilih **Nyahpaut daripada MS Project** daripada reben.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Muat naik fail Projek ke SharePoint atau Kumpulan Office  
 Anda boleh memuat naik fail Projek anda ke SharePoint dan menemuinya di bawah Dokumen Berkaitan untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] anda.  Anda perlu meminta pentadbir anda mengkonfigurasikan pengurusan dokumen SharePoint dan menghidupkannya untuk entiti Projek. 

 Anda juga boleh memuat naik fail Projek anda kepada [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jika anda telah menyediakan Kumpulan Office.

### <a name="upload-a-file-for-sharepoint"></a>Muat naik fail untuk SharePoint  

1. Pada menu utama, pergi ke **Project Service** > **Muat naik**.  

2. Pilih **Ke Dokumen Projek Project Service Automation**.  

3. Dalam kotak dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **Ya** atau **Tidak**.  

   - Jika anda pilih **Ya**, anda akan dapat memilih **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, lancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.  

   - Jika anda memilih **Tidak**, pautan untuk **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.  

4. Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.  

### <a name="upload-a-file-for-office-groups"></a>Muat naik fail untuk Kumpulan Office  

1. Pada menu utama, pergi ke **Project Service** > **Muat naik**.  

2. Pilih **Ke Dokumen Projek Project Service Automation**.  

3. Dalam kotak dialog **Dayakan Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, pilih **Ya** atau **Tidak**.  

   - Jika anda pilih **Ya**, anda akan dapat memilih **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dalam Project Service Automation, lancarkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuatkan fail Projek daripada pustaka dokumen SharePoint.  

   - Jika anda memilih **Tidak**, pautan untuk **Buka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan berfungsi.  

4. Fail [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] boleh ditemui dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **Dokumen** untuk projek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tertentu.  

## <a name="publish--your-project-as-a-template"></a>Terbitkan projek anda sebagai templat  
 Anda boleh menyimpan projek anda dan menggunakannya semula dengan menyimpannya sebagai templat projek dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Templat projek ialah rancangan projek yang boleh digunakan semula dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Untuk maklumat lanjut, lihat [Cipta templat projek (Project Service Automation)](../psa/create-project-template.md). 

1. Pada tab **Project Service**, pergi ke **Terbitkan** > **Templat Projek Project Service Automation Baharu**.  

2. Dalam kotak dialog **Terbitkan ke projek baharu dalam templat Project Service**, masukkan **Nama templat projek**.  

3. Secara pilihan, pilih **Pautkan rancangan projek kepada Project Service Automation** untuk memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Pilih **Terbitkan**.  

Memautkan fail Projek kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadikan fail Projek sebagai fail induk dan menetapkan struktur pecahan kerja dalam templat [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kepada baca sahaja.  Untuk membuat perubahan kepada rancangan projek, anda perlu membuatnya dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan menerbitkannya sebagai kemas kini untuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Baca jadual yang dimuatkan sumber

Apabila membaca projek daripada Project Service Automation, kalendar sumber tidak disegerakkan dengan klien desktop. Jika terdapat perbezaan dalam tempoh, usaha atau tamat tugas, ia mungkin kerana sumber dan klien desktop tidak mempunyai kalendar templat waktu kerja yang sama yang digunakan pada projek.


## <a name="data-synchronization"></a>Penyegerakan data
Jadual dalam bahagian ini memberikan maklumat tentang penyegerakan data entiti antara Project Service Automation dan tambahan desktop Projek Microsoft.

### <a name="project-task-entity-table"></a>Jadual entiti Tugas Projek
Jadual berikut menggariskan cara data entiti Tugas Projek disegerakkan antara Project Service Automation dengan tambahan desktop Microsoft Project.

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Tugas Projek | Tarikh Siap | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Anggaran Usaha | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | ID Klien MS Project | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Tugas Induk | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Project | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Tugas projek | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Nama Tugas Projek | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Unit sumber (Ditamatkan dalam v3.0) | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Tempoh Dijadualkan | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | Tarikh Mula | Disegerakkan | Tidak disegerakkan |
| Tugas Projek | ID WBS | Disegerakkan | Tidak disegerakkan |

### <a name="team-member-entity-table"></a>Jadual entiti Ahli Pasukan
Jadual berikut menggariskan cara data entiti Ahli Pasukan disegerakkan antara Project Service Automation dan Micros

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Ahli Pasukan | ID Klien MS Project | Disegerakkan | Tidak disegerakkan |
| Ahli Pasukan | Nama Kedudukan | Disegerakkan | Tidak disegerakkan |
| Ahli Pasukan | projek | Disegerakkan | Disegerakkan |
| Ahli Pasukan | Pasukan Projek | Disegerakkan | Disegerakkan |
| Ahli Pasukan | Unit Sumber | Tidak disegerakkan | Disegerakkan |
| Ahli Pasukan | Peranan | Tidak disegerakkan | Disegerakkan |
| Ahli Pasukan | Waktu Bekerja | Tidak disegerakkan | Tidak disegerakkan |

### <a name="resource-assignment-entity-table"></a>Jadual entiti Tugasan Sumber
Jadual berikut menggariskan cara data entiti Tugasan Sumber disegerakkan antara Project Service Automation dan Micros

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Tugasan Sumber | Dari Tarikh | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Jam | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | ID Klien MS Project | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Kerja Dirancang | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Project | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Pasukan Projek | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Tugasan Sumber | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Tugas | Disegerakkan | Tidak disegerakkan |
| Tugasan Sumber | Hingga Tarikh | Disegerakkan | Tidak disegerakkan |

### <a name="project-task-dependencies-entity-table"></a>Jadual entiti Kebergantungan Tugas Projek
Jadual berikut menggariskan cara data entiti Kebergantungan Tugasan Sumber disegerakkan antara Project Service Automation dan Micros

| **Entiti** | **Medan** | **Microsoft Project ke Project Service Automation** | **Project Service Automation ke Microsoft Project** |
| --- | --- | --- | --- |
| Kebergantungan Tugas Projek | Kebergantungan Tugas Projek | Disegerakkan | Tidak disegerakkan |
| Kebergantungan Tugas Projek | Jenis Pautan | Disegerakkan | Tidak disegerakkan |
| Kebergantungan Tugas Projek | Tugas Pendahulu | Disegerakkan | Tidak disegerakkan |
| Kebergantungan Tugas Projek | Project | Disegerakkan | Tidak disegerakkan |
| Kebergantungan Tugas Projek | Tugas Pengganti | Disegerakkan | Tidak disegerakkan |

### <a name="additional-resources"></a>Sumber tambahan
 [Panduan Pengurus Projek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]