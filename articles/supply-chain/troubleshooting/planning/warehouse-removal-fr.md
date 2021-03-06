---
title: Аналитику прогноза спроса склада нельзя удалить из строк прогноза
description: Аналитику прогноза спроса склада нельзя удалить из строк прогноза.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026850"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Аналитику прогноза спроса склада нельзя удалить из строк прогноза

Номер статьи базы знаний: 4614408

## <a name="symptoms"></a>Симптомы

Эта проблема возникает, когда аналитика **Склад** не назначена на вкладке **Аналитики прогноза** на странице **Параметры прогнозирования спроса**. Тем не менее столбец **Склад** отображается на странице **Прогноз спроса** (**Сводное планирование \> Прогнозирование \> Сущность прогнозирования вручную \> Строк прогноза спроса**).

## <a name="resolution"></a>Приказ

Настройки на вкладке **Аналитики прогноза** на странице **Параметры прогнозирования спроса** не влияют на страницу **Прогноз спроса**. Они управляют базовым прогнозом, который создается и отображается в скорректированном прогнозе спроса. Однако они не управляют аналитиками, которые необходимы для "реального" прогноза спроса. Путем авторизации записей, которые отображаются на странице **Скорректированный прогноз спроса**, можно преобразовать их в "фактические" прогнозные записи для прогнозной модели. Эта модель может затем использоваться для сводного планирования.

На странице **Прогноз спроса** аналитики для "реального" прогноза, которые отображаются в строках прогноза спроса, являются частью складских аналитик. (Это напоминает поведение строк заказа на продажу.) Если ваша система не настроена на использование **Склада** в качестве обязательной складской аналитики, можно настроить страницу, чтобы скрыть столбец.
