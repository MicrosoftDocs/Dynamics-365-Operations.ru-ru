---
title: "Статусы запасов"
description: "Эта статья описывает, как можно использовать состояния запасов для классификации и отслеживания запасов."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b3ec66c805d028c20f3d3f95e7af9d78252828c7
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="inventory-statuses"></a>Статусы запасов

[!include[banner](../includes/banner.md)]


Эта статья описывает, как можно использовать состояния запасов для классификации и отслеживания запасов.

Статусы запасов можно использовать для классификации запасов. После этого можно инициировать соответствующие действия, такие как работа пополнения или размещения.

Вот несколько примеров того, как можно использовать статусы запасов:

-   Создание статусов запасов для запасов в наличии, входящих проводок и исходящих проводок.
-   Определение статуса запасов по умолчанию для складских проводок.
-   Изменение статуса запасов для номенклатур до прибытия, во время прибытия или при размещении номенклатур во время перемещения запасов.
-   Использование статуса запасов для ценообразования номенклатур при их возврате и планирования покрытия номенклатуры во время сводного планирования.

Статус запасов — это одна из аналитик в группе аналитик хранения. Статусы запасов можно классифицировать как "Доступно" или "Недоступно", и параметр **Блокировка запасов** можно использовать для блокировки номенклатур со статусом запасов "Недоступно". Номенклатуры со статусом "Заблокировано" считаются физическими запасами и не могут использоваться в производственном заказе, заказе на продажу, заказе на перемещение или исходящей проводке.

Можно использовать складские номенклатуры со статусами запасов "Доступно" или "Недоступно" для входящей работы. Например, можно создать статус "Доступно" с именем **Готово**, статус "Недоступно" с именем **Повреждено** и статус "Заблокировано" с именем **Заблокировано**. При создании заказа на покупку для полученных или возвращенных номенклатур, если номенклатуры повреждены или сломаны, вы можете изменить статус запасов для этих номенклатур на **Повреждено** в строке заказа на покупку. После получения этих номенклатур автоматически задается статус **Заблокировано**. Если вы просматриваете поврежденные номенклатуры с помощью мобильного устройства, Microsoft Dynamics 365 for Finance and Operations может использовать директивы местонахождений и шаблоны работ для отображения информации о соответствующем местонахождении или ряде местонахождений, в которых можно разместить эти номенклатуры. Для возвращенных номенклатур создается тип расхода **Резервирование** на странице **Складские проводки**.

Для исходящей работы используйте номенклатуры со статусом запасов "Доступно". Если имеются номенклатуры со статусом **Сломано** и для этих номенклатур выполняется сводное планирование, номенклатуры считаются отсутствующими и запасы автоматически пополняются.

После настройки статусов запасов можно установить статус запасов по умолчанию для сайта, номенклатуры и склада. Можно можете задать статус по умолчанию для заказов на продажу, перемещение и покупку. Статус по умолчанию для заказов на продажу и исходящего заказа на перемещение не может иметь значение **Да** для параметра **Блокировка запасов**. Статус запасов, унаследованный от параметров по умолчанию для сайта, склада, номенклатуры, заказа на покупку, заказа на перемещение или заказа на продажу, можно изменить на мобильном устройстве или в строке заказа на покупку, заказа на продажу или заказа на перемещение.

Чтобы запланировать покрытие номенклатур со статусом запасов "Доступно", выберите параметр **План покрытия по аналитикам** для аналитики хранения на странице **Группы аналитик хранения**. При открытии мастера **Покрытие номенклатуры** номенклатуры со статусом "Доступно" отображаются на странице **Статус**. Чтобы создать параметры покрытия для этих номенклатур, выберите код статуса запасов для доступных статусов запасов. В зависимости от параметров покрытия можно рассчитать потребности в номенклатуре и спрогнозировать предложение и спрос на доступные номенклатуры во время сводного планирования. Невозможно создать настройку покрытия номенклатуры со статусом запасов "Заблокировано". Либо используйте страницу **Покрытие номенклатуры** для создания или изменения параметров покрытия номенклатуры.
