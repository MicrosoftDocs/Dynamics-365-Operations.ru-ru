---
title: "Мониторинг точности прогноза"
description: "Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Finance and Operations, и поясняет, как просмотреть значения точности."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f54251b6f6937c59293bd44a0fc27272ffd3d55
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="monitor-forecast-accuracy"></a>Мониторинг точности прогноза

[!include [banner](../includes/banner.md)]

Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 for Finance and Operations, и поясняет, как просмотреть значения точности.

Finance and Operations вычисляет следующие типы точности прогноза.

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

**Примечание.** Если используется служба Microsoft Azure Machine Learning прогнозирования спроса Dynamics 365 for Finance and Operations, вычисления точности внутренней модели основываются на тестовом наборе данных. Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


<a name="additional-resources"></a>Дополнительные ресурсы
--------

[Авторизация скорректированного прогноза](authorize-adjusted-forecast.md)

[Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса](remove-historical-outliers-calculating-demand-forecast.md)




