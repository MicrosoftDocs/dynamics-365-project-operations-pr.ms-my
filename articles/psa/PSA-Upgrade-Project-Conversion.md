---
title: Project Service Automation to Project Operations proses penjadualan projek
description: Artikel ini menyediakan gambaran keseluruhan perubahan ciri untuk Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642580"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation to Project Operations proses penjadualan projek

Selepas projek berjaya dinaik taraf daripada Microsoft Dynamics 365 Project Service Automation 3.X kepada Dynamics 365 Project Operations Lite, mengedit tugas projek dalam struktur pembahagian kerja grid tugas (WBS) tidak mungkin. Pelanggan akan dapat menyemak WBS dalam grid penjejakan di mana medan baru telah ditambah untuk menyediakan semua butiran yang berkaitan dengan tugas tersebut. Untuk projek di mana pengeditan kepada WBS diperlukan, anda boleh menukar projek yang layak secara terpilih kepada Projek baru untuk pengalaman penjadualan web.

## <a name="project-conversion-process"></a>Proses penukaran projek

Untuk menukar projek, ikuti langkah ini.

1. Buka halaman utama projek dan pilih **Tukar** pada Anak Tetingkap Tindakan.
1. Dalam kotak mesej pengesahan, pilih **OK** untuk memulakan penukaran projek. Tindakan berikut berlaku:

    1. Bar mesej yang muncul di halaman utama projek menyatakan, "Jadual projek sedang ditukar. Anda tidak boleh membuat perubahan pada projek sehingga penukaran selesai.
    1. Anda diubah hala ke senarai projek.

    Selepas penukaran projek selesai, tindakan berikut berlaku:

    1. Pengurus projek yang ditugaskan menerima pemberitahuan di sebelah kanan permohonan.
    1. Bar mesej yang menyatakan bahawa penukaran sedang berjalan dialih keluar.
    1. Tab **Jadual** menunjukkan pengalaman penjadualan baru dengan Project for the web. Mana-mana pengguna yang mempunyai lesen dan peranan keselamatan yang sesuai boleh mengedit WBS.
    1. Medan **enjin** penjadualan dikemas kini kepada **Project for the web**.
    1. Butang **Tukar** dialih keluar daripada Anak Tetingkap Tindakan.

> [!IMPORTANT]
> Penukaran pukal projek tidak dibenarkan. Sebarang percubaan untuk mengemas kini jumlah projek yang besar pada masa yang sama akan dicairkan. Batasan ini membantu memastikan prestasi tinggi untuk semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual berbanding tugas automatik

Apabila persekitaran dinaik taraf daripada Automasi Perkhidmatan Projek kepada Operasi Projek, semua tugas dalam WBS dianggap dijadualkan secara automatik. Konsep tugas berjadual secara manual tidak tersedia dalam Project for the web. Walau bagaimanapun, anda boleh menentukan kelakuan penjadualan yang diutamakan untuk projek anda menggunakan [seting mod](/project-management/scheduling-modes.md) penjadualan apabila anda mencipta projek baru.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi terhad untuk projek pra-penukaran

Bahagian ini menggariskan perbezaan fungsi yang boleh anda jangkakan apabila projek belum ditukar.

### <a name="copy-project"></a>Salin projek

Operasi **Salin** hanya disokong pada projek yang ditukar. Projek yang dinaik taraf tidak boleh disalin sebelum penukaran.

### <a name="move-project"></a>Alihkan projek

Perubahan pada tarikh mula projek tidak akan secara berkadaran mengalihkan permulaan tugas melainkan projek telah ditukar.

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apakah perbezaan antara projek yang ditukar dan projek baru yang diwujudkan selepas naik taraf selesai?

Bagi projek yang ditukar selepas persekitaran dinaik taraf, bendera akan ditetapkan yang mengarahkan jadual untuk menghormati kalendar projek sahaja. Kelakuan ini sepadan dengan kelakuan dalam Automasi Perkhidmatan Projek. Walau bagaimanapun, bendera tidak akan ditetapkan untuk projek baharu yang dicipta selepas naik taraf. Oleh itu, jadual akan menghormati waktu kerja sumber apabila mereka ditugaskan untuk tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apa yang perlu saya lakukan jika projek saya gagal ditukar?

Jika projek anda gagal ditukar, langkah pertama ialah menyemak log ralat untuk mengenal pasti sebarang isu biasa yang berkaitan dengan WBS anda. Jika log tidak menunjukkan ralat tertentu yang boleh anda ambil tindakan, hubungi Sokongan Pelanggan supaya kes anda boleh disemak dengan lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimanakah penutupan perniagaan dikendalikan dalam Project for the web?

Projek untuk web tidak menghormati penutupan perniagaan yang ditakrifkan oleh perusahaan di peringkat organisasi. Walau bagaimanapun, ia akan menghormati jenis hari cuti lain yang ditakrifkan dalam templat jam kerja tertentu.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apakah had Projek untuk web?

Lihat [Cipta struktur pecahan kerja: Pengehadan](/project-management/create-wbs#project-limitations.md) Projek.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Bolehkah saya menjangkakan perubahan pada anggaran kos dan jualan saya?

Dalam kes yang jarang berlaku di mana kontur tugasan sumber dikira semula, atau di mana ia jatuh pada sempadan tarikh yang berbeza daripada projek sumber, anda mungkin melihat perbezaan dalam anggaran jualan dan kos. Sebagai sebahagian daripada proses naik taraf, pelanggan dijangka menguji set sampel projek wakil, supaya mereka dapat memahami sebarang perubahan jadual yang berpotensi.
