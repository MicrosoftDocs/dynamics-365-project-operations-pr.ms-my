---
title: Mencadangkan sumber projek
description: Topik ini memberikan maklumat tentang cadangan sumber projek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120194"
---
# <a name="propose-project-resources"></a>Mencadangkan sumber projek

Pengurus sumber boleh mencadangkan sumber kepada pengurus projek menggunakan permintaan sumber.

1. Daripada grid permintaan atau permintaan itu sendiri, pilih **Cari sumber.**
2. Pada halaman **Pembantu Jadual** , pilih sumber dan kemudian, dalam anak tetingkap **Cipta Tempahan Sumber** dalam medan status **Status Tempahan**, pilih **Tempah.**

    ![Sumber terpilih yang dicadangkan.](media/Resource-Management-image62.png)

Kemas kini status berikut berlaku:

- Pada halaman **Pembantu Jadual**, penunjuk status dikemas kini untuk menunjukkan bahawa penempahan dicadangkan, tidak ditempah cetak.

    ![Petunjuk status untuk tempahan yang dicadangkan pada halaman Pembantu Jadual](media/Resource-Management-image63.png)

- Pada permintaan sumber, status ditukar kepada **Keperluan Semakan Semula.**

    ![Status permintaan sumber ditukar kepada Keperluan Semakan Semula](media/Resource-Management-image64.png)

- Pada tab **Pasukan** projek, permintaan ahli pasukan generik **Status Permintaan** ditukar kepada **Keperluan Semakan Semula.**

    ![Status permintaan ahli pasukan generik ditukar kepada Keperluan Semakan Semula pada tab Pasukan.](media/Resource-Management-image48.png)

Pengurus projek boleh sama ada menerima atau menolak cadangan itu.

Apabila pengurus sumber memproses permintaan sumber, mereka boleh menggunakan sebarang pendekatan berikut:

- Mencadangkan berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk memenuhi jam yang diperlukan. Waktu yang dicadangkan kemudian berpecah antara sumber yang boleh memenuhi jam yang diperlukan. Dalam senario ini, jam tidak boleh bertindan.
- Mencadangkan lebih sedikit sumber daripada keperluan. Dalam senario ini, kapasiti sumber yang dicadangkan adalah kurang daripada jam yang diperlukan yang ditentukan oleh peminta. Oleh itu, apabila peminta menerima sumber yang dicadangkan, keperluan sumber yang tidak dipatuhi dicipta untuk menawan permintaan yang berbaki.
- Tempah berbilang sumber untuk memenuhi permintaan jika tiada sumber tunggal tersedia untuk menyelesaikan kerja.
- Menempah lebih sedikit sumber daripada keperluan. Dalam senario ini, masa yang ditempah adalah lebih sedikit daripada jam yang diperlukan. Sistem ini memberi panduan kepada anda untuk mencadangkan sumber dan bukannya penempahan, supaya peminta boleh mengesahkan dan menjejaki permintaan yang berbaki.

## <a name="billable-utilization"></a>Penggunaan boleh dibilkan

Sumber boleh mempunyai sasaran penggunaan boleh dibilkan. Penggunaan sasaran ini sama ada ditakrifkan sebagai atribut pada peranan lalai sumber atau ditetapkan pada rekod sumber boleh ditempah individu. Pengiraan penggunaan adalah berdasarkan masa sebenar bahawa sumber telah dilaporkan dengan menggunakan kemasukan penyertaan yang diluluskan.

Formula berikut digunakan untuk mengira penggunaan:

- Penggunaan boleh dibilkan = Jam sebenar ÷ Kapasiti sumber boleh dituntut.
- Penggunaan tidak boleh dibilkan = Masa sebenar dengan ID jenis bil = Tidak dikenakan caj, Pelengkap atau Tidak tersedia yang boleh ÷ Kapasiti sumber
- Dalaman = Masa sebenar dengan tiada kontrak jualan ÷ Kapasiti sumber
- Kapasiti sumber = Waktu kerja sumber – Keluar dari pejabat – Hari tidak bekerja

Anda boleh mencari pandangan **Penggunaan Sumber** dalam anak tetingkap **Sumber**.

![Pandangan Penggunaan sumber](media/Resource-Management-image65.png)

Setiap sel dalam grid mewakili peratusan penggunaan boleh dibilkan bagi sumber dalam tempoh, seperti hari, minggu atau bulan. Formula berikut digunakan untuk mewarnakan sel:

- **Hijau:** Penggunaan boleh dibilkan \>= Penggunaan sasaran sumber
- **Kuning:** Penggunaan sasaran – 20 \<= Penggunaan boleh dibilkan \< Penggunaan sasaran
- **Merah:** Penggunaan boleh dibilkan \< Penggunaan sasaran – 20

Oleh kerana pandangan **Penggunaan Sumber** adalah berdasarkan Papan Jadual, anda boleh menggunakan keupayaan penapisan Papan Jadual untuk menapis hasil anda.

Grid memerlukan anda menetapkan penggunaan sasaran pada sama ada peranan atau sumber individu. Untuk melakukan persediaan ini, pergi ke **Peranan** \> **Peranan sumber**.

Selain itu, peranan lalai mesti ditugaskan kepada setiap sumber boleh ditempah. Pergi ke **Sumber** \> **Sumber**. Pada tab **Project Service** sahkan peranan sumber ditakrifkan dan medan **Adalah Lalai** untuk ia disetkan kepada **Ya.** Anda boleh menambah peranan tambahan di mana **Adalah Lalai = No**. Peranan di mana **Adalah Lalai = Ya** digunakan untuk menilai penggunaan sumber terhadap sasaran untuk peranan tersebut.

![Peranan lalai ditetapkan](media/Resource-Management-image67.png)

Pada tab **Project Service**, anda juga boleh menetapkan penggunaan sasaran individu untuk sumber. Pengiraan penggunaan ini kemudian menggunakan penggunaan sasaran yang akan menilai sasaran sumber bukan sasaran peranan lalai sumber.

Penggunaan ditunjukkan untuk sumber hanya jika sumber tersebut telah diluluskan dan masa boleh dikenakan dalam tempoh yang ditunjukkan dalam grid.

## <a name="resource-availability"></a>Ketersediaan sumber

Adalah penting bahawa pengurus sumber boleh melihat ketersediaan sumber dan kemas kini tempahan. Dalam sesetengah kes, tidak ada permintaan formal (permintaan sumber), tetapi pengurus sumber mesti bertindak balas kepada permintaan yang tidak dirancang yang datang melalui saluran seperti e-mel, panggilan telefon atau mesej segera. Pengurus sumber menggunakan Papan Jadual untuk mengemas kini sumber dan penempahan.

Waktu kerja sumber digunakan sebagai asas untuk mengira ketersediaan sumber. Tempahan sumber mengambil kapasiti sumber.

![Papan Jadual](media/Resource-Management-image68.png)

Papan Jadual menggunakan warna dan pembayangan untuk menunjukkan penempahan, ketersediaan dan pilihan berlebihan dan juga status tempahan. Tetapan dalam tetapan Papan Jadual membolehkan anda menunjukkan petunjuk.

Jika anak panah tunjuk sebelah kanan muncul di sebelah sumber boleh ditempah individu pada Papan Jadual, sumber itu dapat dikembangkan untuk menunjukkan butiran kerja yang digunakan oleh sumber tersebut.

![Sumber boleh ditempah dikembangkan ke Papan Jadual](media/Resource-Management-image69.png)

Kerana Dynamics 365 Project Service Automation menggunakan enjin Universal Resource Scheduling, jika anda juga telah Dynamics 365 Field Service dipasang, anda boleh melihat butiran daripada penempahan sumber untuk projek, pesanan kerja dan sebarang entiti lain yang anda telah melanjutkan penjadualan.

![Butiran terperinci mengenai tempahan sumber untuk projek dan pesanan kerja](media/Resource-Management-image70.png)

Untuk melihat lebih banyak butiran mengenai sumber individu, klik kanan padanya untuk membuka kad sumber.

![Kad Sumber](media/Resource-Management-image71.png)
