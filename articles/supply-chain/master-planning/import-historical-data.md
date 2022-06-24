---
title: Импорт исторических данных для прогнозов спроса
description: Чтобы получить точные прогнозы спроса, требуются исторические данные по спросу на номенклатуру или ключу распределения номенклатуры. В этой статье объясняется, как использовать объекты данных для импорта исторических данных о спросе из любой системы, чтобы получить более данные для прогноза спроса за больший исторический период.
author: t-benebo
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36ea72322c31f7e0ea3377b474cd148d78bdd3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877605"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Импорт исторических данных для прогнозов спроса

[!include [banner](../includes/banner.md)]

Для обеспечения точности прогнозов спроса необходимо иметь максимальный объем исторических данных по спросу, который можно получить для номенклатуры или ключа распределения номенклатуры. Если исторические данные по спросу еще не импортированы, используйте информационный объект **Исторический внешний спрос** (ReqDemPlanHistoricalExternalDemandEntity) в Dynamics 365 Supply Chain Management, чтобы импортировать его.

В рабочей области **Управление данными** можно просмотреть обзор всех полей объекта.

1. Откройте рабочую область **Управление данными**.
2. Выберите плитку **Информационные объекты**.
3. Найдите в списке объект **Исторический внешний спрос**.
4. Выберите **Целевые поля**. Следующие поля объекта являются обязательными: сайт (**DeliveringSiteId**), дата (**DemandDate**), количество (**DemandQuantity**) и номер номенклатуры (**ItemNumber**) или ключ распределения номенклатуры (**ProductAllocationKeyId**).

Чтобы использовать информационный объект, необходим файл Microsoft Excel или файл значений с разделителями-запятыми (CSV), содержащий исторические данные о спросе. В следующем примере показано, как импортировать данные из CSV-файла.

Дополнительные сведения о том, как импортировать данные, в том числе о порядке очистки данных после импорта, см. в теме [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) и связанных с ней статьях.

См. также [Создание статистического базового прогноза](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]