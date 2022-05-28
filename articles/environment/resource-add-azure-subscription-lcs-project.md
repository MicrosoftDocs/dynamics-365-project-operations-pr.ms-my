---
title: Tambah langganan Azure untuk projek LCS
description: Topik ini memberikan maklumat mengenai cara untuk menyambungkan langganan Azure anda ke projek LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 839c510838b0bccb718b8ca8a4f71a1c46e7ea3f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595923"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tambah langganan Azure untuk projek LCS

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Persekitaran berhos awan mesti dilaksanakan dengan menggunakan langganan Azure yang sedia ada. Topik ini menjelaskan cara untuk menyambungkan langganan Azure sedia ada anda ke projek LCS. 

## <a name="grant-admin-consent"></a>Berikan persetujuan pentadbir

1. Dalam projek LCS anda, dalam bahagian **persekitaran**, pilih tetapan **Microsoft Azure**.

![Tetapan Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Pada halaman **tetapan projek**, pada tab **penyambung Azure**, pilih **Benarkan**. Ini membolehkan persekitaran digunakan untuk projek ini.

![Penyambung Azure.](./media/2AzureConnectors.png)

3. Pilih semula **Benarkan** untuk memberikan kebenaran pentadbir.

![Berikan Persetujuan Pentadbir.](./media/3GrantAdminConsent.png)

4. Menerima permintaan keizinan.

![Terima Permintaan Kebenaran.](./media/4AcceptPermissionRequest.png)

Pengesahan kini selesai. 

![Pengesahan Berjaya.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Berikan akses Perkhidmatan Pelaksanaan Dynamics kepada langganan Azure anda

1. Pergi ke pengebilan [Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) dan pilih langganan anda. Perkhidmatan Pelaksanaan Dynamics perlu mengakses langganan ini untuk dapat menggunakan persekitaran.

![Butiran Langganan Azure.](./media/6AzureSubscription.png)

2. Pilih **kawalan capaian (IAM)** dalam anak tetingkap navigasi dan kemudian pilih **Tambah tugasan peranan**.
3. Dalam gelangsar di sebelah kanan, pilih **Peranan penyumbang** dan dalam senarai yang disediakan, cari dan pilih **Perkhidmatan Pelaksanaan Dynamics**. 
4. Pilih **Simpan**.

![Akses Langganan.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Tambah penyambung langganan ke projek LCS

1. Dalam projek LCS anda, pada halaman tetapan **Microsoft Azure**, pilih **Tambah** untuk menambah penyambung baharu.
2. Masukkan ID langganan Azure anda. Anda boleh mencari ID langganan Azure anda dalam [Portal Azure](https://ms.portal.azure.com/), di bawah  **Tetapan**  di sebelah kiri bawah skrin.
3. Dalam **Konfigurasi untuk menggunakan medan Pengurus Sumber Azure**, pilih **Ya**.
4. Pastikan Langganan Azure AAD Domain Penyewa yang sepadan dengan domain-memiliki langganan Azure yang anda gunakan dan pilih **Seterusnya**.
5. Pada skrin **Persediaan Microsoft Azure**, pilih **Seterusnya** untuk mengesahkannya. Jika anda menerima ralat pada skrin ini, kembali ke bahagian [Berikan akses kepada Perkhidmatan Pelaksanaan Dynamics kepada Langganan Azure](#provide) dalam topik ini dan pastikan anda telah melengkapkan semua langkah tersebut.
6. Muat turun Sijil Pengurusan Azure ke folder tempatan pada komputer anda. Minta pentadbir langganan Azure anda untuk memuat naik sijil ke Portal Pengurusan Azure dengan memilih langganan dan pergi ke **Tetapan** > **Sijil Pengurusan**. Sijil ini mendayakan LCS untuk berkomunikasi dengan Azure bagi pihak anda. Anda boleh melangkau langkah ini jika pengguna anda mempunyai akses kepada langganan.
7. Pilih  **Seterusnya**.
8. Pilih rantau Azure untuk menggunakan dan pilih pusat data yang berdekatan dengan tempat anda merancang untuk menggunakan sistem ini.
9.  Pilih  **Connect**.

Anda telah berjaya menyambungkan langganan Azure anda. Anda kini boleh menggunakan Dynamics 365 Finance persekitaran yang dihoskan awan.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
