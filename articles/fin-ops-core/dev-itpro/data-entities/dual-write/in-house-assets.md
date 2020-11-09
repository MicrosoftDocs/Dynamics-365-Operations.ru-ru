---
title: Внутренние активы для обслуживания
description: В этом разделе описывается, как можно использовать Microsoft Dynamics 365 Field Service для обслуживания как клиентских активов, так и внутренних активов.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0e87a3d645c19fab3bb0560ba5114d193e2d0be7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997178"
---
# <a name="in-house-assets-for-servicing"></a>Внутренние активы для обслуживания

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service разработано для обслуживания активов клиентов. Управление активами для Dynamics 365 Supply Chain Management предназначено для ведения внутренних активов. Интеграция этих двух приложений позволяет использовать Field Service для обслуживания как активов клиентов, так и внутренних активов. Имеется также возможность классифицировать активы на основе функционального местоположения или иерархии и отслеживать обслуживание на подробном уровне.

Дополнительные сведения см. в разделе [Интеграция Dynamics 365 Field Service и Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Шаблоны

Внутренние активы включают коллекцию сопоставлений основных объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

| Приложения Finance and Operations | Приложения на основе модели в Dynamics 365 | описание |
|-----------------------------|-----------------------------------|-------------|
| Модели жизненного цикла актива в управлении активами | msdyn\_assetlifecyclemodels | |
| Состояния жизненного цикла актива в управлении активами | msdyn\_assetlifecyclestates | |
| Активы управления активами | msdyn\_customerassets | |
| Типы активов управления активами | msdyn\_customerassetcategories | |
| Модели жизненного цикла функционального местоположения управления активами | msdyn\_functionallocationlifecyclemodels | |
| Состояния жизненного цикла функционального местоположения управления активами | msdyn\_functionallocationlifecyclestates | |
| Функциональные местоположения управления активами | msdyn\_functionallocations | |
| Типы функциональных местоположений управления активами | msdyn\_functionallocationtypes | |
| Производители управления активами | msdyn\_manufacturers | |
| Модели управление активами | msdyn\_models | |
| Гарантия управления активами | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
