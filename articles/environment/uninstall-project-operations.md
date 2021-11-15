---
title: Nyahpasang Dynamics 365 Project Operations
description: Topik ini menyediakan maklumat mengenai cara menyahpasang Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: ms-MY
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783654"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Nyahpasang Dynamics 365 Project Operations 

_**Terpakai Kepada:** Project Operations untuk senario berasaskan sumber/bukan stok_

Untuk menyahpasang Dynamics 365 Project Operations, anda mesti ditugaskan peranan Pentadbir.

1. Pergi ke **Tetapan** > **Penyelesaian**.

    ![Halaman tetapan.](./media/uninstall-proj-ops-solutions.png)
  
2. Keluarkan penyelesaian mengikut turutan tepat yang disenaraikan dalam jadual berikut. 

    | Langkah | Nama penyelesaian                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 2 | ProjectOperations_Anchor                           | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 5 | ProjectService                                     | Tiada nota tambahan.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Tiada nota tambahan.                                                                         |
    | 7 | ProjectServiceCore                                 | Tiada nota tambahan.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 9 | FieldServiceCommon                                 | Diperlukan untuk dwitulis dengan Dynamics 365 Finance atau Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Diperlukan untuk dwitulis dengan Dynamics 365 Finance atau Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Diperlukan untuk Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 19 | Dynamics365Notes                                   | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 21 | DualWriteCore                                      | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 23 | Dynamics365AssetManagement                         | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 26 | HCMCommon                                          | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 28 | Pihak                                              | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 29 | Dynamics365Company                                 | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 30 | CurrencyExchangeRates                              | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
    | 31 | AssetCommon                                        | Jika tidak ditemui, langkau penyelesaian ini.                                                            |
