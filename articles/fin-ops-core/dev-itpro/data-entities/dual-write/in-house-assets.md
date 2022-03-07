---
title: Внутренние активы для обслуживания
description: В этом разделе описывается, как можно использовать Microsoft Dynamics 365 Field Service для обслуживания как клиентских активов, так и внутренних активов.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748601"
---
# <a name="in-house-assets-for-servicing"></a>Внутренние активы для обслуживания

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service разработано для обслуживания активов клиентов. Управление активами для Dynamics 365 Supply Chain Management предназначено для ведения внутренних активов. Интеграция этих двух приложений позволяет использовать Field Service для обслуживания как активов клиентов, так и внутренних активов. Имеется также возможность классифицировать активы на основе функционального местоположения или иерархии и отслеживать обслуживание на подробном уровне.

Дополнительные сведения см. в разделе [Интеграция Dynamics 365 Field Service и Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Шаблоны

Внутренние активы включают коллекцию сопоставлений основных таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]