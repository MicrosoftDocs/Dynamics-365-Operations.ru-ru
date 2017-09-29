---
title: "Определения отчетов в конструкторе финансовых отчетов"
description: "Эта статья содержит сведения об определениях отчетов. Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета. Определение отчета также предоставляет параметры и настройки для настройки отчета."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="102e4-105">Определения отчетов в конструкторе финансовых отчетов</span><span class="sxs-lookup"><span data-stu-id="102e4-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="102e4-106">Эта статья содержит сведения об определениях отчетов.</span><span class="sxs-lookup"><span data-stu-id="102e4-106">This article provides information about report definitions.</span></span> <span data-ttu-id="102e4-107">Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="102e4-108">Определение отчета также предоставляет параметры и настройки для настройки отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="102e4-109">Определение отчета — это компонент отчета (или строительный блок), который использует определение строки, определение столбца и необязательное определение дерева отчетности для создания отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="102e4-110">Определение отчета также обеспечивает параметры и настройки, которые можно использовать для настройки отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="102e4-111">После того как вы определяете определения строки и определения столбца, вы должны совместить их в определении отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="102e4-112">В этот момент, вы также определяете другие аспекты определений, такие как уровень детализации и дата отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="102e4-113">Вы можете после этого сохранить и создать отчет.</span><span class="sxs-lookup"><span data-stu-id="102e4-113">You can then save and generate a report.</span></span> <span data-ttu-id="102e4-114">Финансовая отчетность предлагает следующие уровни детализации:</span><span class="sxs-lookup"><span data-stu-id="102e4-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="102e4-115">Финансы</span><span class="sxs-lookup"><span data-stu-id="102e4-115">Financial</span></span>
-   <span data-ttu-id="102e4-116">Финансовый и Счет</span><span class="sxs-lookup"><span data-stu-id="102e4-116">Financial and Account</span></span>
-   <span data-ttu-id="102e4-117">Финансовый, счет и проводка</span><span class="sxs-lookup"><span data-stu-id="102e4-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="102e4-118">Однако, в зависимости от того,как данные хранятся в системе Microsoft Dynamics ERP,сведения проводки могут быть не доступны в отчетах.</span><span class="sxs-lookup"><span data-stu-id="102e4-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="102e4-119">Создание определения отчета</span><span class="sxs-lookup"><span data-stu-id="102e4-119">Create a report definition</span></span>
1.  <span data-ttu-id="102e4-120">В конструкторе отчетов в меню **Файл** щелкните **Создать**, а затем выберите **Определение отчета**.</span><span class="sxs-lookup"><span data-stu-id="102e4-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="102e4-121">Определите соответствующую информацию на вкладках **Отчет**, **Вывод и распределение**, **Заголовки и нижние колонтитулы** и **Настройки**.</span><span class="sxs-lookup"><span data-stu-id="102e4-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="102e4-122">Содержимое определения отчета</span><span class="sxs-lookup"><span data-stu-id="102e4-122">Contents of a report definition</span></span>
<span data-ttu-id="102e4-123">Следующая таблица описывает вкладки в определении отчета и как информация используется.</span><span class="sxs-lookup"><span data-stu-id="102e4-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="102e4-124">Табуляция</span><span class="sxs-lookup"><span data-stu-id="102e4-124">Tab</span></span></th>
<th><span data-ttu-id="102e4-125">Описание</span><span class="sxs-lookup"><span data-stu-id="102e4-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="102e4-126">Отчет</span><span class="sxs-lookup"><span data-stu-id="102e4-126">Report</span></span></td>
<td><span data-ttu-id="102e4-127">Создайте отчет, настройте отчет, или измените существующий отчет.</span><span class="sxs-lookup"><span data-stu-id="102e4-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="102e4-128">Вывод и распределение</span><span class="sxs-lookup"><span data-stu-id="102e4-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="102e4-129">Измените тип вывода и назначение отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="102e4-130">Заголовки и нижние колонтитулы</span><span class="sxs-lookup"><span data-stu-id="102e4-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="102e4-131">Определите и отформатируйте заголовки и нижние колонтитулы для отчета.</span><span class="sxs-lookup"><span data-stu-id="102e4-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="102e4-132">Например, вы можете добавить текст или изображения к заголовку или нижнему колонтитулу.</span><span class="sxs-lookup"><span data-stu-id="102e4-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="102e4-133">Финансовая отчетность поддерживает файлы BMP, JPG и PNG для изображений.</span><span class="sxs-lookup"><span data-stu-id="102e4-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="102e4-134">Вы можете также добавить коды autotext для того, чтобы вставить другую информацию, такую как название фирмы, имя отчета, или номер страницы.</span><span class="sxs-lookup"><span data-stu-id="102e4-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="102e4-135">Настройки</span><span class="sxs-lookup"><span data-stu-id="102e4-135">Settings</span></span></td>
<td><span data-ttu-id="102e4-136">Определите установки определения отчета, такие как следующие установки:</span><span class="sxs-lookup"><span data-stu-id="102e4-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="102e4-137">Форматирование и точность округления</span><span class="sxs-lookup"><span data-stu-id="102e4-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="102e4-138">Форматирование подробных отчетов</span><span class="sxs-lookup"><span data-stu-id="102e4-138">Format detail reports</span></span></li>
<li><span data-ttu-id="102e4-139">Формат деревьев отчетности</span><span class="sxs-lookup"><span data-stu-id="102e4-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="102e4-140">Создать отчет об исключениях</span><span class="sxs-lookup"><span data-stu-id="102e4-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="102e4-141">Указать Конвертацию валюты</span><span class="sxs-lookup"><span data-stu-id="102e4-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="102e4-142">промежуточный итог и фильтрация сведений счета</span><span class="sxs-lookup"><span data-stu-id="102e4-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="102e4-143">См. также</span><span class="sxs-lookup"><span data-stu-id="102e4-143">See also</span></span>
--------

[<span data-ttu-id="102e4-144">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="102e4-144">Financial reporting</span></span>](financial-reporting-intro.md)




