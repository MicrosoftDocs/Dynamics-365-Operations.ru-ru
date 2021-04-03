---
title: Содержимое Power BI "Факт/Бюджет"
description: В этой теме описывается содержимое Power BI "Факт/Бюджет". В нем объясняется, как получить доступ к отчетам, и представляются сведения о модели данных.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568581"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="c6d8e-104">Содержимое Power BI "Факт/Бюджет"</span><span class="sxs-lookup"><span data-stu-id="c6d8e-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6d8e-105">В этой теме описывается содержимое **Факт/Бюджет** для Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="c6d8e-106">В нем описывается порядок доступа к отчетам Power BI и предоставляется информация о модели данных и объектах, которые использовались для построения пакета содержимого.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="c6d8e-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="c6d8e-107">Overview</span></span>

<span data-ttu-id="c6d8e-108">Содержимое Power BI **Факт/Бюджет** было создан по отдельным лицам, ответственным за мониторинг фактических показателей в сравнении с бюджетными в своей организации.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="c6d8e-109">Содержимое Power BI **Факт/бюджет** обеспечивает видимость расхождений бюджета.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="c6d8e-110">Можно проанализировать бюджет за текущий года по категории счета, коду бюджета, счету ГК, описаниям счета ГК или финансовому периоду, чтобы лучше понять причину любых расхождений.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="c6d8e-111">Доступ к содержимому Power BI</span><span class="sxs-lookup"><span data-stu-id="c6d8e-111">Accessing the Power BI content</span></span>
<span data-ttu-id="c6d8e-112">Отчеты из содержимого Power BI **Факт/Бюджет** отображаются в рабочих областях **Бюджет ГК и прогнозы** и **CFO**.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="c6d8e-113">Отчеты, включенные в содержимое Power BI</span><span class="sxs-lookup"><span data-stu-id="c6d8e-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="c6d8e-114">В следующей таблице приводятся подробные сведения о показателях, которые находятся на каждой странице отчета, в содержимом Power BI **Факт/Бюджет**.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="c6d8e-115">Отчет</span><span class="sxs-lookup"><span data-stu-id="c6d8e-115">Report</span></span>                      | <span data-ttu-id="c6d8e-116">Показатели</span><span class="sxs-lookup"><span data-stu-id="c6d8e-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d8e-117">Расходы — фактические и бюджетные</span><span class="sxs-lookup"><span data-stu-id="c6d8e-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="c6d8e-118">Итоговые расходы за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-118">Total expenses this year</span></span></li><li><span data-ttu-id="c6d8e-119">Итоговые расходы по бюджету за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="c6d8e-120">Выручка — фактическая и бюджетная</span><span class="sxs-lookup"><span data-stu-id="c6d8e-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="c6d8e-121">Итоговая выручка за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-121">Total revenue this year</span></span></li><li><span data-ttu-id="c6d8e-122">Итоговая выручка по бюджету за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="c6d8e-123">Расход</span><span class="sxs-lookup"><span data-stu-id="c6d8e-123">Expense</span></span>                     | <ul><li><span data-ttu-id="c6d8e-124">Итоговые расходы за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-124">Total expenses this year</span></span></li><li><span data-ttu-id="c6d8e-125">Цель для расходов в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="c6d8e-126">Реализация</span><span class="sxs-lookup"><span data-stu-id="c6d8e-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="c6d8e-127">Итоговая выручка за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-127">Total revenue this year</span></span></li><li><span data-ttu-id="c6d8e-128">Цель для выручки в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="c6d8e-129">Чистый доход</span><span class="sxs-lookup"><span data-stu-id="c6d8e-129">Net income</span></span>                  | <ul><li><span data-ttu-id="c6d8e-130">Чистый доход за этот год</span><span class="sxs-lookup"><span data-stu-id="c6d8e-130">Net income this year</span></span></li><li><span data-ttu-id="c6d8e-131">Цель для чистого дохода в зависимости от бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="c6d8e-132">Понимание модели данных и объектов</span><span class="sxs-lookup"><span data-stu-id="c6d8e-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="c6d8e-133">Объект</span><span class="sxs-lookup"><span data-stu-id="c6d8e-133">Entity</span></span>                    | <span data-ttu-id="c6d8e-134">Содержание</span><span class="sxs-lookup"><span data-stu-id="c6d8e-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6d8e-135">Действия ГК</span><span class="sxs-lookup"><span data-stu-id="c6d8e-135">General Ledger Activities</span></span> | <span data-ttu-id="c6d8e-136">Сумма проводки по КГ</span><span class="sxs-lookup"><span data-stu-id="c6d8e-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="c6d8e-137">Действия бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-137">Budget Activities</span></span>         | <span data-ttu-id="c6d8e-138">Суммы проводок для регистра бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="c6d8e-139">Счета ГК</span><span class="sxs-lookup"><span data-stu-id="c6d8e-139">Main Accounts</span></span>             | <span data-ttu-id="c6d8e-140">Счета ГК для фильтрации отчетов</span><span class="sxs-lookup"><span data-stu-id="c6d8e-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="c6d8e-141">Финансовые календари</span><span class="sxs-lookup"><span data-stu-id="c6d8e-141">Fiscal Calendars</span></span>          | <span data-ttu-id="c6d8e-142">Финансовые календари для фильтрации отчетов</span><span class="sxs-lookup"><span data-stu-id="c6d8e-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="c6d8e-143">Главные книги</span><span class="sxs-lookup"><span data-stu-id="c6d8e-143">Ledgers</span></span>                   | <span data-ttu-id="c6d8e-144">Книги, которые могут использоваться для фильтрации отчета по текущей книге</span><span class="sxs-lookup"><span data-stu-id="c6d8e-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="c6d8e-145">Коды бюджета</span><span class="sxs-lookup"><span data-stu-id="c6d8e-145">Budget Codes</span></span>              | <span data-ttu-id="c6d8e-146">Коды бюджета, по которым требуется фильтровать отчеты</span><span class="sxs-lookup"><span data-stu-id="c6d8e-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="c6d8e-147">Юридические лица</span><span class="sxs-lookup"><span data-stu-id="c6d8e-147">Legal Entities</span></span>            | <span data-ttu-id="c6d8e-148">Юридические лица, которые могут использоваться для фильтрации отчета по текущему юридическому лицу</span><span class="sxs-lookup"><span data-stu-id="c6d8e-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]