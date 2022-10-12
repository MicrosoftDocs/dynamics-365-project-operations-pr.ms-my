---
title: Perubahan ciri untuk Automasi Perkhidmatan Projek kepada Operasi Projek
description: Artikel ini menyediakan gambaran keseluruhan perubahan ciri untuk Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621337"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Perubahan ciri untuk Automasi Perkhidmatan Projek kepada Operasi Projek

Selepas projek berjaya dinaik taraf daripada Microsoft Dynamics 365 Project Service Automation 3.X kepada Dynamics 365 Project Operations Lite, tugas mengedit projek dalam struktur pembahagian kerja grid tugas (WBS) tidak mungkin. Pelanggan akan dapat menyemak WBS dalam grid penjejakan di mana medan baru telah ditambah untuk menyediakan semua butiran yang berkaitan dengan tugas. Untuk projek di mana pengeditan kepada WBS diperlukan, anda boleh menukar projek yang layak secara terpilih kepada Projek baru untuk pengalaman penjadualan web.

## <a name="project-conversion-process"></a>Proses penukaran projek

Untuk menukar projek, ikut langkah ini.

1. Buka halaman utama projek dan pilih **Tukar** pada Anak Tetingkap Tindakan.
1. Dalam kotak mesej pengesahan, pilih **OK** untuk memulakan penukaran projek. Tindakan berikut berlaku:

    1. Bar mesej yang muncul di halaman utama projek menyatakan, "Jadual projek sedang ditukar. Anda tidak boleh membuat perubahan pada projek sehingga penukaran selesai.
    1. Anda diubah hala ke senarai projek.

    Selepas penukaran projek selesai, tindakan berikut berlaku:

    1. Pengurus projek yang ditugaskan menerima pemberitahuan di sebelah kanan aplikasi.
    1. Bar mesej yang menyatakan bahawa penukaran sedang berjalan dialih keluar.
    1. Tab **Jadual** menunjukkan pengalaman penjadualan baru dengan Project for the web. Mana-mana pengguna yang mempunyai lesen dan peranan keselamatan yang sesuai boleh mengedit WBS.
    1. Medan **enjin** Penjadualan dikemas kini kepada **Project for the web**.
    1. Butang **Tukar** dialih keluar daripada Anak Tetingkap Tindakan.

> [!IMPORTANT]
> Penukaran projek secara pukal tidak dibenarkan. Sebarang percubaan untuk mengemas kini sejumlah besar projek pada masa yang sama akan dikurangkan. Batasan ini membantu memastikan prestasi tinggi untuk semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual berbanding tugas automatik

Apabila persekitaran dinaik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek, semua tugas dalam WBS dianggap dijadualkan secara automatik. Konsep tugas berjadual secara manual tidak tersedia dalam Project for the web. Walau bagaimanapun, anda boleh menentukan tingkah laku penjadualan pilihan untuk projek anda dengan menggunakan [tetapan mod](/project-management/scheduling-modes.md) penjadualan apabila anda mencipta projek baru.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi terhad untuk projek pra penukaran

Seksyen ini menggariskan perbezaan fungsian yang anda boleh jangkakan apabila projek belum ditukar.

### <a name="copy-project"></a>Salin projek

Operasi **Salin** hanya disokong pada projek yang ditukar. Projek dinaik taraf tidak boleh disalin sebelum penukaran.

### <a name="move-project"></a>Alih projek

Perubahan pada tarikh mula projek tidak akan secara berkadar mengalihkan permulaan tugas melainkan projek telah ditukar.

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apakah perbezaan antara projek yang ditukar dan projek baru yang diwujudkan selepas naik taraf selesai?

Bagi projek yang ditukar selepas persekitaran dinaik taraf, bendera akan ditetapkan yang mengarahkan jadual untuk menghormati kalendar projek sahaja. Tingkah laku ini sepadan dengan tingkah laku dalam Automasi Perkhidmatan Projek. Walau bagaimanapun, bendera tidak akan ditetapkan untuk projek baru yang dicipta selepas naik taraf. Oleh itu, jadual akan menghormati waktu kerja sumber apabila mereka ditugaskan untuk tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apakah yang perlu saya lakukan jika projek saya gagal ditukar?

Jika projek anda gagal ditukar, langkah pertama ialah menyemak semula log ralat untuk mengenal pasti sebarang isu biasa yang berkaitan dengan WBS anda. Jika log tidak menunjukkan ralat tertentu yang boleh anda ambil tindakan, hubungi Sokongan Pelanggan supaya kes anda boleh disemak lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimanakah penutupan perniagaan dikendalikan dalam Project untuk web?

Projek untuk web tidak menghormati penutupan perniagaan yang ditakrifkan oleh perusahaan di peringkat organisasi. Walau bagaimanapun, ia akan menghormati jenis hari lain yang ditakrifkan dalam templat jam kerja tertentu.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apakah had Projek untuk web?

Lihat [Mencipta struktur pecahan kerja: Batasan](/project-management/create-wbs#project-limitations.md) Projek.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Bolehkah saya menjangkakan perubahan pada anggaran kos dan jualan saya?

Dalam kes yang jarang berlaku di mana kontur tugasan sumber dikira semula, atau di mana ia jatuh pada sempadan tarikh yang berbeza daripada projek sumber, anda mungkin melihat perbezaan dalam anggaran jualan dan kos. Sebagai sebahagian daripada proses naik taraf, pelanggan dijangka menguji set sampel projek wakil, supaya mereka dapat memahami sebarang kemungkinan perubahan jadual.
