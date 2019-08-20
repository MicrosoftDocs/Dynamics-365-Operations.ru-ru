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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839095"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="6fbdf-104">Финансовый отчет по отчету о прибылях</span><span class="sxs-lookup"><span data-stu-id="6fbdf-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fbdf-105">В этой статье описывается отчет по умолчанию для отчетов о прибыли.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="6fbdf-106">Здесь также описываются строительные блоки, связанные с этим отчетом.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="6fbdf-107">Отчет о прибылях по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="6fbdf-108">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-108">Default report</span></span>             | <span data-ttu-id="6fbdf-109">Что он делает</span><span class="sxs-lookup"><span data-stu-id="6fbdf-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbdf-110">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-110">Income Statement – Default</span></span> | <span data-ttu-id="6fbdf-111">Предоставляет просмотр доходности организации за текущий период и также с начала года.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="6fbdf-112">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="6fbdf-112">Building blocks</span></span>
<span data-ttu-id="6fbdf-113">Финансовый отчет по отчету о прибылях использует следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="6fbdf-114">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-114">Default report</span></span>             | <span data-ttu-id="6fbdf-115">Определение строки</span><span class="sxs-lookup"><span data-stu-id="6fbdf-115">Row definition</span></span>                     | <span data-ttu-id="6fbdf-116">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="6fbdf-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="6fbdf-117">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-117">Income Statement - Default</span></span> | <span data-ttu-id="6fbdf-118">Сводный отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="6fbdf-119">Периодически и с начала года — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6fbdf-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="6fbdf-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="6fbdf-120">Row definition</span></span>

<span data-ttu-id="6fbdf-121">Определение строки, Сводный отчет о доходах — по умолчанию, содержит раздел для каждой из частей традиционного отчета о доходах.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="6fbdf-122">Аналитика Категория счета ГК используется для того, чтобы построить это определение строки.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="6fbdf-123">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="6fbdf-124">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="6fbdf-124">Column Definition</span></span>

<span data-ttu-id="6fbdf-125">Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="6fbdf-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="6fbdf-126">**Периодически и с начала года — типы столбца по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="6fbdf-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="6fbdf-127">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="6fbdf-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6fbdf-128">**FD** — Финансовые данные на текущий период</span><span class="sxs-lookup"><span data-stu-id="6fbdf-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="6fbdf-129">**FD** — Финансовые данные с начала года</span><span class="sxs-lookup"><span data-stu-id="6fbdf-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="6fbdf-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6fbdf-130">Additional resources</span></span>
--------

[<span data-ttu-id="6fbdf-131">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="6fbdf-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="6fbdf-132">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="6fbdf-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="6fbdf-133">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="6fbdf-133">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



