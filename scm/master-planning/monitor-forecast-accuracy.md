---
title: "Мониторинг точности прогноза"
description: "Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Operations, и поясняет, как просмотреть значения точности."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Мониторинг точности прогноза

[!include[banner](../includes/banner.md)]


Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Operations, и поясняет, как просмотреть значения точности.

Dynamics 365 for Operations вычисляет следующие типы точности прогноза.

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

**Примечание.** Если используется служба Microsoft Azure Machine Learning прогнозирования спроса Dynamics 365 for Operations, вычисления точности внутренней модели основываются на тестовом наборе данных. Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


<a name="see-also"></a>См. также
--------

[Авторизация скорректированного прогноза](authorize-adjusted-forecast.md)

[Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса](remove-historical-outliers-calculating-demand-forecast.md)




