---
title: Удаление решений оркестрации приложений с двойной записью
description: В этой статье описан порядок удаления решений оркестрации приложений с двойной записью.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870384"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Удаление решений оркестрации приложений с двойной записью

[!include [banner](../../includes/banner.md)]

В этой статье описан порядок удаления решений оркестрации приложений с двойной записью.

Некоторые клиенты непреднамеренно устанавливают пакет оркестрации приложений с двойной записью, который устанавливает несколько решений в их среду Microsoft Dataverse. Установка лишних решений в пакете может привести к неожиданным и нежелательным проблемам.

Чтобы устранить проблемы, связанные с установкой пакета оркестрации приложений с двойной записью, удалите нежелательные решения с двойной записью в следующем порядке:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (при наличии)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Чтобы удалить это решение, необходимо открыть запрос в службу поддержки Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Если установлены решения субъектов и глобальной адресной книги, удалите решения в следующем порядке:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Субъект
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
