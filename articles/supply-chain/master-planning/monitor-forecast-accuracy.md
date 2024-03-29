---
title: Мониторинг точности прогноза
description: Эта статья описывает типы точности прогнозов, вычисляемые Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76248d87533fd233b255060aa278c76e13719700
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740748"
---
# <a name="monitor-forecast-accuracy"></a>Мониторинг точности прогноза

[!include [banner](../includes/banner.md)]

Эта статья описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.

Supply Chain Management вычисляет следующие типы точности прогноза.

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

> [!NOTE]
> Если используется служба прогнозирования спроса Microsoft Azure Machine Learning, вычисления точности внутренней модели основываются на тестовом наборе данных. Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


## <a name="additional-resources"></a>Дополнительные ресурсы

- [Авторизация скорректированного прогноза](authorize-adjusted-forecast.md)
- [Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]