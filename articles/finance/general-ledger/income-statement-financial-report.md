---
title: Финансовый отчет по отчету о прибылях
description: В этой статье описывается отчет по умолчанию для отчетов о прибыли. Здесь также описываются строительные блоки, связанные с этим отчетом.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1852eac49b4a26e0680d7a918d2a6d8af37031
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838845"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="e012a-104">Финансовый отчет по отчету о прибылях</span><span class="sxs-lookup"><span data-stu-id="e012a-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e012a-105">В этой статье описывается отчет по умолчанию для отчетов о прибыли.</span><span class="sxs-lookup"><span data-stu-id="e012a-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="e012a-106">Здесь также описываются строительные блоки, связанные с этим отчетом.</span><span class="sxs-lookup"><span data-stu-id="e012a-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="e012a-107">Отчет о прибылях по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="e012a-108">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-108">Default report</span></span>             | <span data-ttu-id="e012a-109">Что он делает</span><span class="sxs-lookup"><span data-stu-id="e012a-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e012a-110">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-110">Income Statement – Default</span></span> | <span data-ttu-id="e012a-111">Предоставляет просмотр доходности организации за текущий период и также с начала года.</span><span class="sxs-lookup"><span data-stu-id="e012a-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="e012a-112">Строительные блоки</span><span class="sxs-lookup"><span data-stu-id="e012a-112">Building blocks</span></span>
<span data-ttu-id="e012a-113">Финансовый отчет по отчету о прибылях использует следующие строительные блоки.</span><span class="sxs-lookup"><span data-stu-id="e012a-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="e012a-114">Отчет по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-114">Default report</span></span>             | <span data-ttu-id="e012a-115">Определение строки</span><span class="sxs-lookup"><span data-stu-id="e012a-115">Row definition</span></span>                     | <span data-ttu-id="e012a-116">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="e012a-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="e012a-117">Отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-117">Income Statement - Default</span></span> | <span data-ttu-id="e012a-118">Сводный отчет о доходах — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="e012a-119">Периодически и с начала года — по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e012a-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="e012a-120">Определение строки</span><span class="sxs-lookup"><span data-stu-id="e012a-120">Row definition</span></span>

<span data-ttu-id="e012a-121">Определение строки, Сводный отчет о доходах — по умолчанию, содержит раздел для каждой из частей традиционного отчета о доходах.</span><span class="sxs-lookup"><span data-stu-id="e012a-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="e012a-122">Аналитика Категория счета ГК используется для того, чтобы построить это определение строки.</span><span class="sxs-lookup"><span data-stu-id="e012a-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="e012a-123">Поэтому, кто угодно может создать отчет, не делая изменений.</span><span class="sxs-lookup"><span data-stu-id="e012a-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="e012a-124">Определение столбца</span><span class="sxs-lookup"><span data-stu-id="e012a-124">Column Definition</span></span>

<span data-ttu-id="e012a-125">Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.</span><span class="sxs-lookup"><span data-stu-id="e012a-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="e012a-126">**Периодически и с начала года — типы столбца по умолчанию:**</span><span class="sxs-lookup"><span data-stu-id="e012a-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="e012a-127">**DESC** – Описание из определения строки</span><span class="sxs-lookup"><span data-stu-id="e012a-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e012a-128">**FD** — Финансовые данные на текущий период</span><span class="sxs-lookup"><span data-stu-id="e012a-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="e012a-129">**FD** — Финансовые данные с начала года</span><span class="sxs-lookup"><span data-stu-id="e012a-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="e012a-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e012a-130">Additional resources</span></span>
--------

[<span data-ttu-id="e012a-131">Обзор финансовой отчетности</span><span class="sxs-lookup"><span data-stu-id="e012a-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="e012a-132">Просмотр финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="e012a-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="e012a-133">Блог финансовой отчетности Dynamics</span><span class="sxs-lookup"><span data-stu-id="e012a-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]