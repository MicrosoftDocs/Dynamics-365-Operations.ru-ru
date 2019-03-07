---
title: Финансовый отчет по отчету о прибылях
description: В этой статье описывается отчет по умолчанию для отчетов о прибыли. Здесь также описываются строительные блоки, связанные с этим отчетом.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9105e1de86ed2834b04f75c7d08c4021402bcfda
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "364013"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="e4ce0-104">Финансовый отчет по отчету о прибылях</span><span class="sxs-lookup"><span data-stu-id="e4ce0-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4ce0-105">В этой статье описывается отчет по умолчанию для отчетов о прибыли.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="e4ce0-106">Здесь также описываются строительные блоки, связанные с этим отчетом.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="e4ce0-107">Отчет о прибылях по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="e4ce0-108">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-108">Default report</span></span>             | <span data-ttu-id="e4ce0-109">Что он делает</span><span class="sxs-lookup"><span data-stu-id="e4ce0-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ce0-110">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-110">Income Statement – Default</span></span> | <span data-ttu-id="e4ce0-111">Предоставляет просмотр доходности организации за текущий период и также с начала года.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="e4ce0-112">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="e4ce0-112">Building blocks</span></span>
<span data-ttu-id="e4ce0-113">Финансовый отчет по отчету о прибылях использует следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="e4ce0-114">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-114">Default report</span></span>             | <span data-ttu-id="e4ce0-115">Определение строки</span><span class="sxs-lookup"><span data-stu-id="e4ce0-115">Row definition</span></span>                     | <span data-ttu-id="e4ce0-116">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="e4ce0-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="e4ce0-117">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-117">Income Statement - Default</span></span> | <span data-ttu-id="e4ce0-118">Сводный отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="e4ce0-119">Периодически и с начала года — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4ce0-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="e4ce0-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="e4ce0-120">Row definition</span></span>

<span data-ttu-id="e4ce0-121">Определение строки, Сводный отчет о доходах — по умолчанию, содержит раздел для каждой из частей традиционного отчета о доходах.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="e4ce0-122">Аналитика Категория счета ГК используется для того, чтобы построить это определение строки.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="e4ce0-123">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="e4ce0-124">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="e4ce0-124">Column Definition</span></span>

<span data-ttu-id="e4ce0-125">Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="e4ce0-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="e4ce0-126">**Периодически и с начала года — типы столбца по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="e4ce0-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="e4ce0-127">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="e4ce0-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e4ce0-128">**FD** — Финансовые данные на текущий период</span><span class="sxs-lookup"><span data-stu-id="e4ce0-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="e4ce0-129">**FD** — Финансовые данные с начала года</span><span class="sxs-lookup"><span data-stu-id="e4ce0-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="e4ce0-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e4ce0-130">Additional resources</span></span>
--------

[<span data-ttu-id="e4ce0-131">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="e4ce0-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="e4ce0-132">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="e4ce0-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="e4ce0-133">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="e4ce0-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



