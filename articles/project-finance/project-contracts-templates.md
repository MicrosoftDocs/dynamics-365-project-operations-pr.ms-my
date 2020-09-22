---
title: Segerakkan kontrak projek dan projek secara terus daripada Project Service Automation kepada Finance and Operations
description: Topik ini menghuraikan templat dan tugas asas yang digunakan untuk menyegerakkan kontrak projek dan projek secara terus daripada Microsoft Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ms-MY
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753856"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Segerakkan kontrak projek dan projek secara terus daripada Project Service Automation kepada Finance and Operations

[!include[banner](../includes/banner.md)]

Topik ini menghuraikan templat dan tugas asas yang digunakan untuk menyegerakkan kontrak projek dan projek secara terus daripada Dynamics 365 Project Service Automation kepada Dynamics 365 Finance.

> [!NOTE] 
> Jika anda menggunakan Enterprise Edition 7.3.0, anda mesti memasang KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Aliran data untuk Project Service Automation kepada Finance

> [!NOTE]
> Sebelum anda menggunakan penyelesaian integrasi Project Service Automation kepada Finance, anda harus membiasakan diri dengan ciri integrasi Data Dynamics 365.

Penyelesaian integrasi Project Service Automation kepada Finance menggunakan ciri integrasi Data untuk menyegerakkan data merentasi tika Project Service Automation dan Finance. Templat integrasi yang tersedia dengan ciri integrasi Data mendayakan aliran data tentang kontrak projek, projek, baris kontrak projek dan pencapaian baris kontrak projek daripada Project Service Automation kepada Finance.

Ilustrasi berikut menunjukkan cara data disegerakkan antara Project Service Automation dan Finance.

[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Templat dan tugas

Untuk mengakses templat yang tersedia, dalam pusat pentadbiran Microsoft Power Apps, pilih **Projek** dan kemudian, di sudut kanan atas, pilih **Projek baharu** untuk memilih templat awam.

Templat dan tugas asas yang berikut digunakan untuk menyegerakkan kontrak projek dan projek daripada Project Service Automation kepada Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Berintegrasi dengan Dynamics 365 Project Service Automation v2.x
- **Nama templat dalam integrasi Data:** Projek dan kontrak (PSA kepada Fin dan Ops)
- **Nama tugas dalam projek:**

    - Kontrak projek PSA kepada Fin dan Ops
    - Projek PSA kepada Fin dan Ops
    - Baris kontrak projek PSA kepada Fin dan Ops
    - Pencapaian baris kontrak projek PSA kepada Fin dan Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Berintegrasi dengan Dynamics 365 Project Service Automation v3.x
Terdapat perubahan skema dalam Project Service Automation yang memberi kesan kepada templat pencapaian baris kontrak projek dan penggunaan versi V2 templat diperlukan untuk mengintegrasikan Project Service Automation v3.x dengan Dynamics 365.

- **Nama templat dalam integrasi Data:** Projek dan Kontrak (PSA 3.x kepada Fin dan Ops) - v2
- **Nama tugas dalam projek:**

    - Kontrak projek PSA kepada Fin dan Ops
    - Projek PSA kepada Fin dan Ops
    - Baris kontrak projek PSA kepada Fin dan Ops
    - Pencapaian baris kontrak projek PSA kepada Fin dan Ops

Selepas penyegerakan kontrak projek dan projek boleh berlaku, anda mesti menyegerakkan akaun.

## <a name="entity-set"></a>Set entiti

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Pesanan                           | Entiti integrasi untuk kontrak projek                |
| Projek                         | Entiti integrasi untuk projek                         |
| Baris pesanan                      | Entiti integrasi untuk baris kontrak projek           |
| Pencapaian baris kontrak projek | Entiti integrasi untuk pencapaian baris kontrak projek |

## <a name="entity-flow"></a>Aliran entiti

Kontrak projek diuruskan dalam Project Service Automation dan disegerakkan kepada Finance sebagai kontrak projek. Sebagai sebahagian daripada templat integrasi, anda boleh menetapkan sumber integrasi dalam Finance untuk kontrak projek.

Projek masa dan bahan serta projek harga Tetap diuruskan dalam Project Service Automation dan disegerakkan kepada Finance sebagai projek. Sebagai sebahagian daripada integrasi templat, anda boleh menetapkan sumber integrasi dalam Finance untuk projek.

Baris kontrak projek diuruskan dalam Project Service Automation dan disegerakkan kepada Finance sebagai peraturan pengebilan kontrak projek. Jika kaedah pengebilan berbeza daripada jenis projek lalai, penyegerakan mengemas kini jenis projek untuk projek baris kontrak dan kumpulan projek.

Pencapaian baris kontrak projek diuruskan dalam Project Service Automation dan disegerakkan kepada Finance sebagai pencapaian peraturan pengebilan kontrak projek.

## <a name="project-service-automation-to-finance-integration-solution"></a>Penyelesaian integrasi Project Service Automation kepada Finance

Medan **ID kontrak projek** tersedia di halaman **Kontrak projek**. Medan ini telah menghasilkan kunci unik dan natural untuk menyokong integrasi.

Apabila kontrak projek baharu dicipta, jika nilai **ID kontrak projek** tidak wujud, ia dijana secara automatik dengan menggunakan jujukan nombor. Nilai ini terdiri daripada **ORD** diikuti oleh jujukan nombor yang menaik dan kemudian akhiran enam aksara. Berikut ialah contoh: **ORD-01022-Z4M9Q0**.

Medan **Nombor Projek** tersedia di halaman **Projek**. Medan ini telah menghasilkan kunci unik dan natural untuk menyokong integrasi.

Apabila projek baharu dicipta, jika nilai **Nombor Projek** tidak wujud, ia dijana secara automatik dengan menggunakan jujukan nombor. Nilai ini terdiri daripada **PRJ** diikuti oleh jujukan nombor yang menaik dan kemudian akhiran enam aksara. Berikut ialah contoh: **PRJ-01049-CCNID0**.

Apabila penyelesaian integrasi Project Service Automation kepada Finance digunakan, skrip naik taraf menetapkan medan **ID kontrak projek** untuk kontrak projek sedia ada dan medan **Nombor Projek** untuk projek sedia ada dalam Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Persediaan prasyarat dan pemetaan

- Selepas penyegerakan kontrak projek dan projek boleh berlaku, anda mesti menyegerakkan akaun.
- Dalam set sambungan anda, tambahkan pemetaan medan kunci integrasi untuk **msdyn\_organizationalunits** pada **msdyn\_nama \[Name\]**. Anda mungkin perlu menambahkan terlebih dahulu projek pada set sambungan. Untuk maklumat lanjut, lihat [Integrasikan data ke dalam Common Data Service untuk Aplikasi](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Dalam set sambungan anda, tambahkan pemetaan medan kunci integrasi untuk **msdyn\_projects** pada **msdynce\_projectnumber \[Project Number\]**. Anda mungkin perlu menambahkan terlebih dahulu projek pada set sambungan. Untuk maklumat lanjut, lihat [Integrasikan data ke dalam Common Data Service untuk Aplikasi](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** untuk kontrak projek dan projek boleh dikemas kini kepada nilai yang berbeza atau dialih keluar daripada pemetaan. Nilai templat lalai ialah **Project Service Automation**.
- Pemetaan **PaymentTerms** mesti dikemas kini supaya ia menunjukkan terma pembayaran yang sah dalam Finance. Anda juga boleh mengalih keluar pemetaan daripada tugas projek. Peta nilai lalai mempunyai nilai lain untuk data demo. Jadual yang berikut menunjukkan nilai dalam Project Service Automation.

    | Nilai | Penerangan   |
    |-------|---------------|
    | 1     | Bersih 30        |
    | 2     | 2% 10, Bersih 30 |
    | 3     | Bersih 45        |
    | 4     | Bersih 60        |

## <a name="power-query"></a>Pertanyaan Kuasa

Anda mesti menggunakan Microsoft Power Query untuk Excel bagi menapis data jika syarat yang berikut dipenuhi:

- Anda mempunyai pesanan jualan dalam Dynamics 365 Sales.
- Anda mempunyai berbilang unit organisasi dalam Project Service Automation dan unit organisasi ini akan dipetakan kepada berbilang entiti sah dalam Finance.

Jika anda mesti menggunakan Power Query, ikut garis panduan ini:

- Templat Projek dan kontrak (PSA kepada Fin dan Ops) mempunyai penapis lalai yang mengandungi hanya pesanan jualan jenis **Item kerja (msdyn\_ordertype = 192350001)**. Penapis ini membantu menjamin bahawa kontrak projek tidak dicipta untuk pesanan jualan dalam Finance. Jika anda mencipta templat anda sendiri, anda mesti menambahkan penapis ini.
- Anda mesti mencipta penapis Power Query yang mengandungi hanya organisasi kontrak yang perlu disegerakkan kepada entiti sah bagi set sambungan integrasi. Contohnya, kontrak projek yang anda miliki dengan unit organisasi kontrak Contoso US perlu disegerakkan kepada entiti sah USSI tetapi kontrak projek yang anda miliki dengan unit organisasi kontrak Contoso Global perlu disegerakkan kepada entiti sah USMF. Jika anda tidak menambahkan penapis ini pada pemetaan tugas anda, semua kontrak projek akan disegerakkan kepada entiti sah yang ditakrifkan untuk set sambungan, tanpa mengira unit organisasi kontrak.

## <a name="template-mapping-in-data-integration"></a>Pemetaan tempat dalam integrasi Data

> [!NOTE] 
> Medan **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** dan **AddressZipCode** tidak disertakan dalam pemetaan lalai untuk kontrak projek. Anda boleh menambahkan pemetaan jika anda memerlukan data ini disegerakkan untuk kontrak projek.
>
> Medan **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** dan **ProjectType** tidak disertakan dalam pemetaan lalai untuk projek. Anda boleh menambahkan pemetaan jika anda memerlukan data ini disegerakkan untuk projek.

Ilustrasi yang berikut menunjukkan contoh pemetaan tugas templat dalam integrasi Data. Pemetaan menunjukkan maklumat medan yang akan disegerakkan daripada Project Service Automation kepada Finance.

[![Pemetaan templat](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Pemetaan templat](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Pemetaan templat](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Pemetaan templat](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Pemetaan pencapaian baris kontrak projek dalam templat Projek dan Kontrak (PSA 3.x kepada Dynamics) - v2:

[![Pemetaan templat](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
