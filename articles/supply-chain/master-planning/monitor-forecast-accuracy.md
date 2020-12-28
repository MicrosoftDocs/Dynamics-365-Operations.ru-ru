---
title: Отслеживание точности прогноза
description: Эта тема описывает типы точности прогнозов, вычисляемые Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e5425e54f9e0093888f355a51064e7f0057976
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436267"
---
# <a name="monitor-forecast-accuracy"></a>Отслеживание точности прогноза

[!include [banner](../includes/banner.md)]

Эта тема описывает типы точности прогнозов, вычисляемые Microsoft Dynamics 365 Supply Chain Management, и поясняет, как просмотреть значения точности.

Supply Chain Management вычисляет следующие типы точности прогноза.

-   Историческая точность прогноза: путем сравнения исторического прогноза, используемого в сводном планировании, с историческим спросом. Для просмотра значений (абсолютных и процентных) исторической точности прогноза щелкните **Показать точность** на странице **Сведения о прогнозе спроса**.
-   Предполагаемая точность модели прогнозирования, которая используется для создания прогнозов. Процент точности можно посмотреть в разделе **Сведения о модели — MAPE** на странице **Сведения о прогнозе спроса**. 

> [!NOTE]
> Если используется служба прогнозирования спроса Microsoft Azure Machine Learning, вычисления точности внутренней модели основываются на тестовом наборе данных. Чтобы задать размер тестового набора данных, задайте параметр **TEST\_SET\_SIZE\_PERCENT** на странице **Параметры прогнозирования спроса**. Например, если задать значение равным **20**, последние 20 % исторических данных будут использоваться для вычисления точности внутренней модели.


<a name="additional-resources"></a>Дополнительные ресурсы
--------

[Авторизация скорректированного прогноза](authorize-adjusted-forecast.md)

[Удаление выбросов из исторических транзакционных данных при расчете прогноза спроса](remove-historical-outliers-calculating-demand-forecast.md)



