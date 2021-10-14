---
title: Отслеживание точности прогноза
description: Эта тема описывает типы точности прогнозов, вычисляемые Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4246a277aa5d88193c18336cb1de69916ec2a3c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565791"
---
# <a name="monitor-forecast-accuracy"></a>Отслеживание точности прогноза

[!include [banner](../includes/banner.md)]

Эта тема описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.

Supply Chain Management вычисляет следующие типы точности прогноза.

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

> [!NOTE]
> Если используется служба прогнозирования спроса Microsoft Azure Machine Learning, вычисления точности внутренней модели основываются на тестовом наборе данных. Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


## <a name="additional-resources"></a>Дополнительные ресурсы

[Авторизация скорректированного прогноза](authorize-adjusted-forecast.md)

[Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]