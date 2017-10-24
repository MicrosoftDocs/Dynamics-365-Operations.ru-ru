---
title: "Финансовые отчеты по балансовому отчету"
description: "В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="853f5-104">Финансовые отчеты по балансовому отчету</span><span class="sxs-lookup"><span data-stu-id="853f5-104">Balance sheet financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="853f5-105">В этой статье описываются отчеты по умолчанию для балансовых отчетов.</span><span class="sxs-lookup"><span data-stu-id="853f5-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="853f5-106">Здесь также описываются строительные блоки, связанные с этими отчетами.</span><span class="sxs-lookup"><span data-stu-id="853f5-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="853f5-107">Отчеты по балансовому отчету по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="853f5-108">Есть два отчета по балансовому отчету по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="853f5-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="853f5-109">На одном отчете, разделы составлены друг над другом</span><span class="sxs-lookup"><span data-stu-id="853f5-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="853f5-110">На другом отчете, разделы расположены рядом по сторонам друг от друга.</span><span class="sxs-lookup"><span data-stu-id="853f5-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="853f5-111">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-111">Default report</span></span>                       | <span data-ttu-id="853f5-112">Что он делает</span><span class="sxs-lookup"><span data-stu-id="853f5-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="853f5-113">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="853f5-114">Предоставляет Просмотр финансового положения организации за год.</span><span class="sxs-lookup"><span data-stu-id="853f5-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="853f5-115">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="853f5-116">Предоставляет Просмотр финансового положения организации за год.</span><span class="sxs-lookup"><span data-stu-id="853f5-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="853f5-117">Сравнение основных средств, задолженности и собственного капитала акционеров.</span><span class="sxs-lookup"><span data-stu-id="853f5-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="853f5-118">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="853f5-118">Building blocks</span></span>
<span data-ttu-id="853f5-119">Финансовые отчеты по балансовому отчету ведомости используют следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="853f5-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="853f5-120">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-120">Default report</span></span>                       | <span data-ttu-id="853f5-121">Определение строки</span><span class="sxs-lookup"><span data-stu-id="853f5-121">Row definition</span></span>                       | <span data-ttu-id="853f5-122">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="853f5-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="853f5-123">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="853f5-124">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="853f5-125">С начала года и отклонение — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="853f5-126">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="853f5-127">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="853f5-128">Столбец С начала года — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="853f5-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="853f5-129">Определение строки</span><span class="sxs-lookup"><span data-stu-id="853f5-129">Row definition</span></span>

<span data-ttu-id="853f5-130">Определения строки для обоих балансовых отчетов содержит разделы для каждой части традиционного балансового отчета.</span><span class="sxs-lookup"><span data-stu-id="853f5-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="853f5-131">Отчет бок о бок включает перенос столбца так, что задолженность и собственный капитал владельца находятся рядом с активами.</span><span class="sxs-lookup"><span data-stu-id="853f5-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="853f5-132">Аналитика Категория счета ГК используется для того, чтобы построить оба определения строки.</span><span class="sxs-lookup"><span data-stu-id="853f5-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="853f5-133">Поэтому, кто угодно может создать отчеты, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="853f5-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="853f5-134">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="853f5-134">Column definition</span></span>

<span data-ttu-id="853f5-135">Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="853f5-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="853f5-136">**С начала года и отклонение — типы столбца по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="853f5-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="853f5-137">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="853f5-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="853f5-138">**FD** — Финансовые данные с начала года на текущий год</span><span class="sxs-lookup"><span data-stu-id="853f5-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="853f5-139">**FD** — Финансовые данные с начала года за прошлый год</span><span class="sxs-lookup"><span data-stu-id="853f5-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="853f5-140">**CALC** — Отклонение от вычитания прошлого года из этого года</span><span class="sxs-lookup"><span data-stu-id="853f5-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="853f5-141">**Столбец С начала года — по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="853f5-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="853f5-142">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="853f5-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="853f5-143">**FD** — Финансовые данные с начала года на текущий год</span><span class="sxs-lookup"><span data-stu-id="853f5-143">**FD** – Year-to-date financial data for the current year</span></span>

 

<a name="see-also"></a><span data-ttu-id="853f5-144">См. также</span><span class="sxs-lookup"><span data-stu-id="853f5-144">See also</span></span>
--------

[<span data-ttu-id="853f5-145">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="853f5-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="853f5-146">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="853f5-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="853f5-147">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="853f5-147">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




