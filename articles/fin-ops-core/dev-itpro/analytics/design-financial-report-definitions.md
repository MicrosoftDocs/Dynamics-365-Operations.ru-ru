---
title: Определения отчетов в конструкторе финансовых отчетов
description: Эта статья содержит сведения об определениях отчетов. Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета. Определение отчета также предоставляет параметры и настройки для настройки отчета.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174152"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="04ee1-105">Определения отчетов в конструкторе финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="04ee1-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04ee1-106">Эта статья содержит сведения об определениях отчетов.</span><span class="sxs-lookup"><span data-stu-id="04ee1-106">This article provides information about report definitions.</span></span> <span data-ttu-id="04ee1-107">Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="04ee1-108">Определение отчета также предоставляет параметры и настройки для настройки отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="04ee1-109">Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="04ee1-110">Определение отчета также содержит дополнительные параметры для настройки отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="04ee1-111">После задания определений строк и столбцов их нужно объединить в определении отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="04ee1-112">В этот момент, вы также определяете другие аспекты определений, такие как уровень детализации и дата отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="04ee1-113">Вы можете после этого сохранить и создать отчет.</span><span class="sxs-lookup"><span data-stu-id="04ee1-113">You can then save and generate a report.</span></span> <span data-ttu-id="04ee1-114">Финансовая отчетность предлагает следующие уровни детализации:</span><span class="sxs-lookup"><span data-stu-id="04ee1-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="04ee1-115">Финансы</span><span class="sxs-lookup"><span data-stu-id="04ee1-115">Financial</span></span>
- <span data-ttu-id="04ee1-116">Финансовый и Счет</span><span class="sxs-lookup"><span data-stu-id="04ee1-116">Financial and Account</span></span>
- <span data-ttu-id="04ee1-117">Финансовый, счет и проводка</span><span class="sxs-lookup"><span data-stu-id="04ee1-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="04ee1-118">Но в зависимости от способа хранения в данных в ERP-системе Microsoft Dynamics сведения о транзакциях могут быть недоступны для отчетов.</span><span class="sxs-lookup"><span data-stu-id="04ee1-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="04ee1-119">Создание определения отчета</span><span class="sxs-lookup"><span data-stu-id="04ee1-119">Create a report definition</span></span>
1. <span data-ttu-id="04ee1-120">В конструкторе отчетов в меню **Файл** щелкните **Создать**, а затем выберите **Определение отчета**.</span><span class="sxs-lookup"><span data-stu-id="04ee1-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="04ee1-121">Определите соответствующую информацию на вкладках **Отчет**, **Вывод и распределение**, **Заголовки и нижние колонтитулы** и **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="04ee1-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="04ee1-122">Содержимое определения отчета</span><span class="sxs-lookup"><span data-stu-id="04ee1-122">Contents of a report definition</span></span>
<span data-ttu-id="04ee1-123">В следующей таблице описаны вкладки определения отчета и применение этих данных.</span><span class="sxs-lookup"><span data-stu-id="04ee1-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="04ee1-124">Вкладка</span><span class="sxs-lookup"><span data-stu-id="04ee1-124">Tab</span></span></th>
<th><span data-ttu-id="04ee1-125">Описание</span><span class="sxs-lookup"><span data-stu-id="04ee1-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="04ee1-126">Отчет</span><span class="sxs-lookup"><span data-stu-id="04ee1-126">Report</span></span></td>
<td><span data-ttu-id="04ee1-127">Эта вкладка используется для создания и настройки отчета или его изменения.</span><span class="sxs-lookup"><span data-stu-id="04ee1-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ee1-128">Вывод и распространение</span><span class="sxs-lookup"><span data-stu-id="04ee1-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="04ee1-129">Изменение типа выходных данных и места вывода отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ee1-130">Колонтитулы</span><span class="sxs-lookup"><span data-stu-id="04ee1-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="04ee1-131">Определение и форматирование колонтитулов отчета.</span><span class="sxs-lookup"><span data-stu-id="04ee1-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="04ee1-132">Например, вы можете добавить текст или изображения к заголовку или нижнему колонтитулу.</span><span class="sxs-lookup"><span data-stu-id="04ee1-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="04ee1-133">Финансовая отчетность поддерживает файлы BMP, JPG и PNG для изображений.</span><span class="sxs-lookup"><span data-stu-id="04ee1-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="04ee1-134">Вы можете также добавить коды autotext для того, чтобы вставить другую информацию, такую как название фирмы, имя отчета, или номер страницы.</span><span class="sxs-lookup"><span data-stu-id="04ee1-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="04ee1-135">Параметры</span><span class="sxs-lookup"><span data-stu-id="04ee1-135">Settings</span></span></td>
<td><span data-ttu-id="04ee1-136">Укажите настройки определения отчета, например следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="04ee1-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="04ee1-137">Форматирование и округление сумм</span><span class="sxs-lookup"><span data-stu-id="04ee1-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="04ee1-138">Форматирование подробных отчетов</span><span class="sxs-lookup"><span data-stu-id="04ee1-138">Format detail reports</span></span></li>
<li><span data-ttu-id="04ee1-139">Форматирование аналитических структур</span><span class="sxs-lookup"><span data-stu-id="04ee1-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="04ee1-140">Создать отчет об исключениях</span><span class="sxs-lookup"><span data-stu-id="04ee1-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="04ee1-141">Задание пересчета валюты</span><span class="sxs-lookup"><span data-stu-id="04ee1-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="04ee1-142">Получение промежуточных итогов по счетам и фильтрация сведений о счетах</span><span class="sxs-lookup"><span data-stu-id="04ee1-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="04ee1-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04ee1-143">Additional resources</span></span>

[<span data-ttu-id="04ee1-144">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="04ee1-144">Financial reporting</span></span>](financial-reporting-intro.md)
