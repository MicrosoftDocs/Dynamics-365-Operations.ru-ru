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
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="32243-103">Аналитику прогноза спроса склада нельзя удалить из строк прогноза</span><span class="sxs-lookup"><span data-stu-id="32243-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="32243-104">Номер статьи базы знаний: 4614408</span><span class="sxs-lookup"><span data-stu-id="32243-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="32243-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="32243-105">Symptoms</span></span>

<span data-ttu-id="32243-106">Эта проблема возникает, когда аналитика **Склад** не назначена на вкладке **Аналитики прогноза** на странице **Параметры прогнозирования спроса**.</span><span class="sxs-lookup"><span data-stu-id="32243-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="32243-107">Тем не менее столбец **Склад** отображается на странице **Прогноз спроса** (**Сводное планирование \> Прогнозирование \> Сущность прогнозирования вручную \> Строк прогноза спроса**).</span><span class="sxs-lookup"><span data-stu-id="32243-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="32243-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="32243-108">Resolution</span></span>

<span data-ttu-id="32243-109">Настройки на вкладке **Аналитики прогноза** на странице **Параметры прогнозирования спроса** не влияют на страницу **Прогноз спроса**.</span><span class="sxs-lookup"><span data-stu-id="32243-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="32243-110">Они управляют базовым прогнозом, который создается и отображается в скорректированном прогнозе спроса.</span><span class="sxs-lookup"><span data-stu-id="32243-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="32243-111">Однако они не управляют аналитиками, которые необходимы для "реального" прогноза спроса.</span><span class="sxs-lookup"><span data-stu-id="32243-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="32243-112">Путем авторизации записей, которые отображаются на странице **Скорректированный прогноз спроса**, можно преобразовать их в "фактические" прогнозные записи для прогнозной модели.</span><span class="sxs-lookup"><span data-stu-id="32243-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="32243-113">Эта модель может затем использоваться для сводного планирования.</span><span class="sxs-lookup"><span data-stu-id="32243-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="32243-114">На странице **Прогноз спроса** аналитики для "реального" прогноза, которые отображаются в строках прогноза спроса, являются частью складских аналитик.</span><span class="sxs-lookup"><span data-stu-id="32243-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="32243-115">(Это напоминает поведение строк заказа на продажу.) Если ваша система не настроена на использование **Склада** в качестве обязательной складской аналитики, можно настроить страницу, чтобы скрыть столбец.</span><span class="sxs-lookup"><span data-stu-id="32243-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
