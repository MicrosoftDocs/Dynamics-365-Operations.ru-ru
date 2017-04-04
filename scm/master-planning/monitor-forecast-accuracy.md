---
title: "Монитор прогноз точности"
description: "В этой статье описываются типы прогнозных точностью вычисляет Microsoft Dynamics 365 для операций и объясняется, как можно просмотреть значения точности."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Монитор прогноз точности

В этой статье описываются типы прогнозных точностью вычисляет Microsoft Dynamics 365 для операций и объясняется, как можно просмотреть значения точности.

Dynamics 365 для операций рассчитывает точность прогноза следующих типов:

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

**Примечание:** при использовании Dynamics 365 для прогнозирования службы Microsoft Azure машинного обучения спроса операции, расчет внутренней модели точностью основан на проверки набора данных. Чтобы указать размер набора данных для тестирования, установите **проверки\_УСТАНОВИТЬ\_размер\_ПРОЦЕНТОВ** параметра в **спрос прогнозирование параметры** страницы. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


<a name="see-also"></a>См. также
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


