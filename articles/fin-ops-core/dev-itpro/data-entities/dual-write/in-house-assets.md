---
title: Внутренние активы для обслуживания
description: В этом разделе описывается, как можно использовать Microsoft Dynamics 365 Field Service для обслуживания как клиентских, так и внутренних активов.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 9ba92b9bf0e35aa812fc7077d998c8779ebe622e
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542351"
---
# <a name="in-house-assets-for-servicing"></a>Внутренние активы для обслуживания

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service разработано для обслуживания активов клиентов. Управление активами для Dynamics 365 Supply Chain Management предназначено для ведения внутренних активов. Интеграция этих двух приложений позволяет использовать Field Service для обслуживания как активов клиентов, так и внутренних активов. Имеется также возможность классифицировать активы на основе функционального местоположения или иерархии и отслеживать обслуживание на подробном уровне.

Дополнительные сведения см. в разделе [Интеграция Dynamics 365 Field Service и Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Шаблоны

Внутренние активы включают коллекцию сопоставлений основных таблиц, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.

| Приложения Finance and Operations | Приложения для взаимодействия с клиентами | описание |
|-----------------------------|-----------------------------------|-------------|
[Модели жизненного цикла актива в управлении активами](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Состояния жизненного цикла актива в управлении активами](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Типы активов управления активами](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Активы управления активами](mapping-reference.md#125) | msdyn_customerassets | |
[Модели жизненного цикла функционального местоположения управления активами](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Состояния жизненного цикла функционального местоположения управления активами](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Типы функциональных местоположений управления активами](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Функциональные местоположения управления активами](mapping-reference.md#136) | msdyn_functionallocations | |
[Производители управления активами](mapping-reference.md#153) | msdyn_manufacturers | |
[Модели управление активами](mapping-reference.md#154) | msdyn_models | |
[Гарантия управления активами](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
