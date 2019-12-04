---
title: Финансовые отчеты по балансовому отчету
description: В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96552447182f3692a19d4cfd962afbcb28e5508
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771877"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="ab7cf-104">Финансовые отчеты по балансовому отчету</span><span class="sxs-lookup"><span data-stu-id="ab7cf-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab7cf-105">В этой статье описываются отчеты по умолчанию для балансовых отчетов.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="ab7cf-106">Здесь также описываются строительные блоки, связанные с этими отчетами.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="ab7cf-107">Отчеты по балансовому отчету по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="ab7cf-108">Есть два отчета по балансовому отчету по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="ab7cf-109">На одном отчете, разделы составлены друг над другом</span><span class="sxs-lookup"><span data-stu-id="ab7cf-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="ab7cf-110">На другом отчете, разделы расположены рядом по сторонам друг от друга.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="ab7cf-111">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-111">Default report</span></span>                       | <span data-ttu-id="ab7cf-112">Что он делает</span><span class="sxs-lookup"><span data-stu-id="ab7cf-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7cf-113">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="ab7cf-114">Предоставляет Просмотр финансового положения организации за год.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="ab7cf-115">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ab7cf-116">Предоставляет Просмотр финансового положения организации за год.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="ab7cf-117">Сравнение основных средств, задолженности и собственного капитала акционеров.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="ab7cf-118">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="ab7cf-118">Building blocks</span></span>
<span data-ttu-id="ab7cf-119">Финансовые отчеты по балансовому отчету ведомости используют следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="ab7cf-120">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-120">Default report</span></span>                       | <span data-ttu-id="ab7cf-121">Определение строки</span><span class="sxs-lookup"><span data-stu-id="ab7cf-121">Row definition</span></span>                       | <span data-ttu-id="ab7cf-122">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="ab7cf-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="ab7cf-123">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="ab7cf-124">Балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="ab7cf-125">С начала года и отклонение — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="ab7cf-126">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ab7cf-127">Сравнительный балансовый отчет — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="ab7cf-128">Столбец С начала года — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab7cf-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="ab7cf-129">Определение строки</span><span class="sxs-lookup"><span data-stu-id="ab7cf-129">Row definition</span></span>

<span data-ttu-id="ab7cf-130">Определения строки для обоих балансовых отчетов содержит разделы для каждой части традиционного балансового отчета.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="ab7cf-131">Отчет бок о бок включает перенос столбца так, что задолженность и собственный капитал владельца находятся рядом с активами.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="ab7cf-132">Аналитика Категория счета ГК используется для того, чтобы построить оба определения строки.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="ab7cf-133">Поэтому, кто угодно может создать отчеты, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="ab7cf-134">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="ab7cf-134">Column definition</span></span>

<span data-ttu-id="ab7cf-135">Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="ab7cf-136">**С начала года и отклонение — типы столбца по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="ab7cf-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="ab7cf-137">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="ab7cf-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ab7cf-138">**FD** — Финансовые данные с начала года на текущий год</span><span class="sxs-lookup"><span data-stu-id="ab7cf-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="ab7cf-139">**FD** — Финансовые данные с начала года за прошлый год</span><span class="sxs-lookup"><span data-stu-id="ab7cf-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="ab7cf-140">**CALC** — Отклонение от вычитания прошлого года из этого года</span><span class="sxs-lookup"><span data-stu-id="ab7cf-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="ab7cf-141">**Столбец С начала года — по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="ab7cf-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="ab7cf-142">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="ab7cf-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ab7cf-143">**FD** — Финансовые данные с начала года на текущий год</span><span class="sxs-lookup"><span data-stu-id="ab7cf-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="ab7cf-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ab7cf-144">Additional resources</span></span>
--------

[<span data-ttu-id="ab7cf-145">Обзор финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="ab7cf-145">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="ab7cf-146">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="ab7cf-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="ab7cf-147">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="ab7cf-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



