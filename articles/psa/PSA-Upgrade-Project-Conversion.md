---
title: Proses penukaran penjadualan projek Project Service Automation kepada Project Operations
description: Artikel ini memberikan gambaran keseluruhan perubahan ciri untuk Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proses penukaran penjadualan projek Project Service Automation kepada Project Operations

Selepas projek telah berjaya ditatar daripada Microsoft Dynamics 365 Project Service Automation 3.X kepada Dynamics 365 Project Operations Lite, mengedit tugas projek dalam struktur pecahan kerja grid tugas (WBS) adalah tidak mungkin. Pelanggan akan dapat menyemak WBS dalam grid penjejakan, iaitu medan baharu telah ditambahkan untuk menyediakan semua butiran yang berkaitan dengan tugas. Untuk projek yang pengeditan pada WBS diperlukan, anda boleh memilih untuk menukar projek yang layak kepada pengalaman penjadualan Project for the web baharu.

## <a name="project-conversion-process"></a>Proses penukaran projek

Untuk menukar projek, ikut langkah ini.

1. Buka halaman utama projek dan pilih **Tukar** pada Anak Tetingkap Tindakan.
1. Dalam kotak mesej pengesahan, pilih **OK** untuk memulakan penukaran projek. Tindakan berikut berlaku:

    1. Bar mesej yang muncul pada halaman utama projek menyatakan, "Jadual projek sedang ditukar. Anda tidak boleh membuat perubahan pada projek sehingga penukaran selesai."
    1. Anda dihalakan semula ke senarai projek.

    Selepas penukaran projek selesai, tindakan berikut berlaku:

    1. Pengurus projek yang diuntukkan menerima pemberitahuan di sebelah kanan aplikasi tersebut.
    1. Bar mesej yang menyatakan bahawa penukaran sedang berjalan dialih keluar.
    1. Tab **Jadual** menunjukkan pengalaman penjadualan baharu dengan Project for the web. Sebarang pengguna yang mempunyai lesen dan peranan keselamatan yang sesuai boleh mengedit WBS.
    1. Medan **Enjin penjadualan** dikemas kini kepada **Project for the web**.
    1. Butang **Tukar** dialih keluar daripada Anak Tetingkap Tindakan.

> [!IMPORTANT]
> Penukaran pukal projek tidak dibenarkan. Sebarang percubaan untuk mengemas kini jumlah besar projek pada masa yang sama akan mengalami pendikitan. Batasan ini membantu untuk memastikan prestasi tinggi bagi semua pelanggan.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tugas manual lwn. tugas automatik

Apabila persekitaran ditatar daripada Project Service Automation kepada Project Operations, semua tugas dalam WBS dianggap telah dijadualkan secara automatik. Konsep tugas dijadualkan secara manual tidak tersedia dalam Project for the web. Walau bagaimanapun, anda boleh mentakrifkan tingkah laku penjadualan yang dipilih untuk projek anda menggunakan tetapan [mod penjadualan](/project-management/scheduling-modes.md) apabila anda mencipta projek baharu.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operasi terhad untuk projek prapenukaran

Bahagian ini menggariskan perbezaan fungsi yang boleh anda jangkakan apabila projek belum ditukar.

### <a name="copy-project"></a>Salin projek

Operasi **Salin** disokong hanya pada projek yang ditukar. Projek yang ditatar tidak boleh disalin sebelum penukaran.

### <a name="move-project"></a>Alihkan projek

Perubahan pada tarikh mula projek tidak akan mengalihkan permulaan tugas secara berkadaran melainkan projek telah ditukar.

## <a name="frequently-asked-questions"></a>Soalan lazim

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Apakah perbezaan antara projek yang ditukar dengan projek baharu yang dicipta selepas tatar telah diselesaikan?

Bagi projek yang ditukar selepas persekitaran telah ditatar, bendera akan ditetapkan agar mengarahkan jadual untuk menghormati hanya kalendar projek. Tingkah laku ini sepadan dengan tingkah laku dalam Project Service Automation. Walau bagaimanapun, bendera tidak akan ditetapkan untuk projek baharu yang dicipta selepas tatar. Oleh itu, jadual akan menghormati waktu kerja sumber apabila diuntukkan untuk tugas.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Apakah yang perlu saya lakukan jika projek saya gagal untuk ditukar?

Jika projek anda gagal untuk ditukar, langkah pertama adalah untuk meyemak log ralat untuk mengenal pasti sebarang isu lazim yang berkaitan dengan WBS anda. Jika log tidak menunjukkan ralat khusus yang boleh anda ambil tindakan, hubungi Sokongan Pelanggan supaya kes anda boleh disemak dengan lebih lanjut.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Bagaimanakah penutupan perniagaan yang dikendalikan dalam Project for the web?

Project for the web tidak menghormati penutupan perniagaan yang perusahaan mentakrifkan pada peringkat organisasi. Walau bagaimanapun, ciri ini akan menghormati jenis hari cuti lain yang ditakrifkan dalam templat kerja yang diberikan.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Apakah batasan untuk Project for the web?

Lihat [Cipta struktur pecahan kerja: Batasan Projek](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Bolehkah saya menjangkakan perubahan pada anggaran kos dan jualan saya?

Dalam kes yang jarang berlaku, iaitu kontur tugas sumber telah dikira semula, atau jatuh pada sempadan tarikh yang berbeza daripada projek sumber, anda mungkin melihat perbezaan dalam anggaran jualan dan kos. Sebagai sebahagian daripada proses tatar, pelanggan dijangka untuk menguji set sampel wakil projek, supaya mereka dapat memahami sebarang perubahan jadual yang berpotensi.
