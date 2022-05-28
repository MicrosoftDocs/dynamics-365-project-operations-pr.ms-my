---
title: Atur letak aplikasi Project Operations Dataverse secara manual dengan sokongan dwi tulis
description: Topik ini menerangkan cara untuk mengatur letak aplikasi Project Operations Dataverse secara manual supaya ia menyokong dwi tulis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591231"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Atur letak aplikasi Project Operations Dataverse secara manual dengan sokongan dwi tulis

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Topik ini menerangkan cara untuk mengatur letak Microsoft Dynamics 365 Project Operations dalam Microsoft Dataverse secara manual supaya ia menyokong dwi tulis. Project Operations mengesan konfigurasi persekitaran dan menambahkan sokongan tambahan untuk dwi tulis jika prasyarat dipenuhi.

Semasa pelaksanaan melalui Microsoft Dynamics Lifecycle Services (LCS), jika anda telah mengikuti arahan dalam topik ini, anda boleh melangkau pelaksanaan integrasi Microsoft Power Platform (sebelum ini dikenali sebagai persekitaran Common Data Service).

Proses pelaksanaan Project Operations dalam Dataverse supaya ia menyokong dwi tulis mempunyai empat langkah utama:

1. [Cipta persekitaran baharu dalam Dataverse yang menyokong dwi tulis](#create).
2. [Tambah prasyarat dwi tulis pada persekitaran](#prerequisites).
3. [Tambah aplikasi Project Operations Dataverse](#dataverse).
4. [Pautkan persekitaran anda](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Cipta persekitaran baharu dalam Dataverse yang menyokong dwi tulis

Untuk melengkapkan prosedur ini, anda mesti mendaftar masuk sebagai pentadbir.

1. Buka [Pusat pentadbir Power Platform](https://admin.powerplatform.com) dan daftar masuk sebagai pentadbir.
2. Cipta persekitaran baharu dan namakannya.
3. Pilih jenis persekitaran. Jika anda telah mendaftar untuk tawaran percubaan, pilih **Percubaan (berdasarkan langganan)**.
4. Sahkan rantau pelaksanaan.
5. Dayakan opsyen **Cipta pangkalan data untuk persekitaran ini**. 
6. Sahkan bahasa, dan kemudian sahkan bahawa mata wang sepadan dengan mata wang untuk aplikasi Kewangan dan Operasi anda.
7. Dayakan opsyen **Aplikasi Dynamics 365** dan sahkan bahawa medan **Laksanakan secara automatik aplikasi ini** ditetapkan kepada **Tiada**.
8. Tambah kumpulan keselamatan, jika kumpulan keselamatan ini diperlukan.
9. Pilih **Simpan** untuk mencipta persekitaran.
10. Tunggu sehingga pelaksanaan selesai dan persekitaran mencapai keadaan **Sedia**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Tambah prasyarat dwi tulis pada persekitaran

Sokongan dwi tulis termasuk medan tambahan yang ditambahkan pada entiti utama seperti entiti **Syarikat**. Jika anda menambahkan sokongan dwi tulis pada persekitaran sedia ada, anda mungkin perlu mengemas kini data untuk mendayakan sokongan tersebut. Untuk maklumat mengenai cara untuk butstrap data, lihat [Butstrap data syarikat](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Untuk maklumat lanjut mengenai dwi tulis, lihat [Keperluan sistem dwi tulis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Lengkapkan prosedur ini untuk menambahkan prasyarat dwi tulis pada persekitaran anda.

1. Buka persekitaran yang baharu anda cipta dan kemudian pergi ke **Sumber** \> **Aplikasi Dynamics 365**.
2. Pilih **Penyelesaian teras dwi tulis** dalam senarai aplikasi dan memasangnya.
3. Tunggu sehingga pemasangan selesai. Kemudian pilih **Penyelesaian pengorkestraan aplikasi dwi tulis** dalam senarai aplikasi dan memasangnya.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Tambah aplikasi Project Operations Dataverse

Anda boleh melengkapkan prosedur ini hanya jika anda melengkapkan prosedur sebelumnya sebelum anda memasang Project Operations. Semasa pemasangan, sistem menganalisis konfigurasi persekitaran dan menambahkan sokongan untuk dwi tulis jika ia diperlukan.

1. Buka persekitaran yang anda cipta lebih awal dan kemudian pergi ke **Sumber** \> **Aplikasi Dynamics 365**.
2. Pilih **Microsoft Dynamics 365 Project Operations** dalam senarai aplikasi dan memasangnya.

## <a name="link-your-environments"></a><a name="link"></a>Pautkan persekitaran anda

Dataverse Selepas persekitaran digunakan, anda boleh menyediakan pautan dalam apl Kewangan dan Operasi anda. Ikut langkah dalam [Gunakan wizard dwi tulis untuk memautkan persekitaran anda](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
