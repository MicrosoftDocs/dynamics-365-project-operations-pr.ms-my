---
title: Peningkatan pertimbangan untuk struktur pecahan kerja
description: Topik ini memberikan maklumat mengenai menaik taraf struktur pecahan kerja daripada Project Service Automation 2.x ke 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753942"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Peningkatan pertimbangan untuk struktur pecahan kerja
Topik ini memberikan maklumat mengenai menaik taraf struktur pecahan kerja daripada Project Service Automation 2.x ke 3.x. Topik ini mentakrifkan keadaan sihat projek dalam Project Service Automation (PSA) yang diperlukan untuk naik taraf yang berjaya. Terdapat juga maklumat mengenai syarat menyekat umum yang akan menyebabkan peningkatan untuk gagal. Untuk mendapatkan maklumat lanjut tentang mentakrifkan tugas projek dan fungsi mereka dalam jadual projek, lihat [Jadual project](project-creating.md).

## <a name="key-entities"></a>Entiti utama
Untuk struktur pecahan kerja yang tepat yang sudah dimuatkan dengan sumber, entiti berikut diperlukan:

- [Projek](../developer/entities/msdyn_project.md)
- [Pasukan Projek](../developer/entities/msdyn_projectteam.md)
- [Tugas Projek](../developer/entities/msdyn_projecttask.md)
- [Penugasan Sumber](../developer/entities/msdyn_resourceassignment.md)
- [Kebergantungan Tugas Projek](../developer/entities/msdyn_projecttaskdependency.md)
- [Sumber Boleh Ditempah](../developer/entities/bookableresource.md)

Untuk mentakrifkan struktur pecahan kerja sumber yang dimuatkan, anda mesti melengkapkan langkah berikut:

1. Cipta projek baharu. Untuk maklumat lanjut mengenai cara untuk mencipta projek baharu, lihat [msdyn_project](../developer/entities/msdyn_project.md).
2. Cipta satu atau lebih tugas. Untuk maklumat lanjut mengenai cara untuk mencipta tugasan baharu, lihat [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Takrifkan kebergantungan tugas. Untuk mendapatkan maklumat lanjut, lihat [Kebergantungan Tugas Projek](../developer/entities/msdyn_projecttaskdependency.md).
4. Tugaskan ahli pasukan projek ke projek. Untuk mendapatkan maklumat lanjut, lihat [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Tugaskan ahli pasukan projek ke tugasan. Untuk mendapatkan maklumat lanjut, lihat [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Perhubungan pasukan projek

Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:
- Semua ahli pasukan projek mesti dikaitkan dengan sumber boleh ditempah.
- Semua ahli pasukan projek mesti dikaitkan dengan projek yang sama. 

## <a name="project-task-relationships"></a>Perhubungan tugas projek
Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:

- Sebarang tugas berkaitan mesti dikaitkan dengan projek yang sama.
- Setiap tugas baris mesti mempunyai tugas induk.
- Setiap tugas baris mesti mempunyai tugas projek.

### <a name="valid-conditions"></a>Syarat sah

- Semua tugas tempoh mesti lebih besar daripada atau sama dengan (>=) sejam dan kurang daripada 1,800,000 minit (1,250 hari).*
- Semua tugas mesti mempunyai tarikh mula tidak lebih awal daripada 01/01/2000.*
- Semua tugas mesti mempunyai tarikh mula tidak melebihi 17 tahun dari hari sekarang.*
- Semua tugas mesti mempunyai tarikh mula lebih awal atau sama dengan tarikh penamat mereka.
- Semua jenis transaksi pada pengelasan (Perbelanjaan, Bahan, Cukai dan Masa) mesti mempunyai nilai untuk **Unit Lalai** dan **Kumpulan Unit**.
- Format tarikh dengan huruf perlu dielakkan.

### <a name="potential-mitigation-steps"></a>Langkah pengurangan berpotensi
- Gunakan Carian Lanjutan untuk mengenal pasti tugas Projek yang tidak mengandungi ID Projek.
- Gunakan Carian Lanjutan untuk mengenal pasti tugas Projek apabila tempoh dijadualkan lebih besar daripada > 1,800,000.
- Sebelum membuat sebarang perubahan data, anda perlu menyiasat sebarang penyesuaian yang berkaitan dengan entiti yang mungkin telah menyebabkan data berada dalam keadaan buruk. Penyesuaian ini perlu ditangani sebelum meneruskan dengan sebarang kemas kini berkaitan dengan data.
- Untuk tugas yang dikenal pasti telah menjadi yatim, pertimbangkan untuk memadam tugas ini jika ia tidak diperlukan atau jika ia harus dikaitkan dengan projek induk yang betul.
- Untuk sebarang tugas yang tempohnya adalah lebih besar daripada 1,250 hari, pertimbangkan menambah pelbagai tugas untuk mewakili jumlah tempoh, jika boleh dilaksanakan.

> [!NOTE]
> Item yang direkodkan dengan asterisk (\*) mempunyai had yang disebabkan oleh hakikat bahawa pengurusan perhubungan pelanggan (CRM) menyokong hanya 7,320 pengembangan yang berulang. Anda mesti kekal di bawah had ini.

## <a name="resource-assignment-relationships"></a>Perhubungan Tugasan Sumber
Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:

- Semua Tugasan Sumber dalam struktur pecahan kerja mesti mempunyai kaitan dengan projek yang sama.
- Semua Tugasan Sumber dalam struktur pecahan kerja mesti mempunyai kaitan dengan ahli pasukan dalam projek yang sama.

### <a name="potential-mitigation-steps"></a>Langkah pengurangan berpotensi
- Kenal pasti semua tugas yang berada di luar keadaan yang diterangkan di atas.  
- Sebarang Tugasan Sumber yang tidak lagi sah perlu dipadamkan.

## <a name="project-task-dependency-relationships"></a>Perhubungan kebergantungan tugasan projek
Untuk memastikan peningkatan yang berjaya, perhubungan berikut mesti diselenggara dengan betul:

- Semua tugas projek kebergantungan mestilah berkaitan dengan projek yang sama.
- Satu tugas tidak boleh mempunyai kebergantungan yang sama yang dirujuk lebih daripada sekali.
