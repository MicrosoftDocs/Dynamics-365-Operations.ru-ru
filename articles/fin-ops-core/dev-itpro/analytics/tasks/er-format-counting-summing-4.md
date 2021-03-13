---
title: Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 4. Выполнение формата)
description: В этой теме описывается, как настроить формат электронный отчетности для выполнения инвентаризации и суммирования на основе данных уже созданного текстового вывода. (Часть 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092955"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="438bd-104">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 4. Выполнение формата)</span><span class="sxs-lookup"><span data-stu-id="438bd-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="438bd-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="438bd-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="438bd-106">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="438bd-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="438bd-107">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)".</span><span class="sxs-lookup"><span data-stu-id="438bd-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="438bd-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="438bd-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="438bd-109">Проверьте эту конфигурацию для создания отчетов "Интрастат"</span><span class="sxs-lookup"><span data-stu-id="438bd-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="438bd-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="438bd-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="438bd-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="438bd-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="438bd-112">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="438bd-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="438bd-113">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="438bd-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="438bd-114">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="438bd-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="438bd-115">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="438bd-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="438bd-116">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="438bd-116">Click User parameters.</span></span>
8. <span data-ttu-id="438bd-117">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="438bd-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="438bd-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="438bd-118">Click OK.</span></span>
10. <span data-ttu-id="438bd-119">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="438bd-119">Click Edit.</span></span>
11. <span data-ttu-id="438bd-120">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="438bd-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="438bd-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="438bd-121">Click Save.</span></span>
13. <span data-ttu-id="438bd-122">Перейдите в раздел "Налог" > "Настройка" > "Внешняя торговля" > "Параметры внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="438bd-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="438bd-123">Разверните раздел "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="438bd-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="438bd-124">Выберите конфигурацию "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="438bd-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="438bd-125">Выберите конфигурацию "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="438bd-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="438bd-126">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="438bd-126">Click Save.</span></span>
18. <span data-ttu-id="438bd-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="438bd-127">Close the page.</span></span>
19. <span data-ttu-id="438bd-128">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="438bd-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="438bd-129">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="438bd-129">Click Output.</span></span>
21. <span data-ttu-id="438bd-130">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="438bd-130">Click Report.</span></span>
    * <span data-ttu-id="438bd-131">Запустите процесс создания отчета Интрастат.</span><span class="sxs-lookup"><span data-stu-id="438bd-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="438bd-132">В поле "Начальная дата" установите для даты значение "01.01.2000".</span><span class="sxs-lookup"><span data-stu-id="438bd-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="438bd-133">Определите начальную и конечную даты отчетного периода, который включает существующие даты в проводках формы.</span><span class="sxs-lookup"><span data-stu-id="438bd-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="438bd-134">В поле "Конечная дата" установите для даты значение "31.12.2022".</span><span class="sxs-lookup"><span data-stu-id="438bd-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="438bd-135">Определите начальную и конечную даты отчетного периода, который включает существующие даты в проводках формы.</span><span class="sxs-lookup"><span data-stu-id="438bd-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="438bd-136">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="438bd-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="438bd-137">Выберите значение "Да" в поле "Создать файл".</span><span class="sxs-lookup"><span data-stu-id="438bd-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="438bd-138">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="438bd-138">Click OK.</span></span>
    * <span data-ttu-id="438bd-139">Просмотрите созданные выходные данные со сводными строками в конце.</span><span class="sxs-lookup"><span data-stu-id="438bd-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="438bd-140">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="438bd-140">Click New.</span></span>
28. <span data-ttu-id="438bd-141">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="438bd-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="438bd-142">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="438bd-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="438bd-143">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="438bd-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="438bd-144">В поле "Товар" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="438bd-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="438bd-145">Задайте вес равным "10".</span><span class="sxs-lookup"><span data-stu-id="438bd-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="438bd-146">Задайте сумму накладной "10000".</span><span class="sxs-lookup"><span data-stu-id="438bd-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="438bd-147">Задайте статистическую сумму "10000".</span><span class="sxs-lookup"><span data-stu-id="438bd-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="438bd-148">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="438bd-148">Click Output.</span></span>
36. <span data-ttu-id="438bd-149">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="438bd-149">Click Report.</span></span>
37. <span data-ttu-id="438bd-150">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="438bd-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="438bd-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="438bd-151">Click OK.</span></span>
    * <span data-ttu-id="438bd-152">Просмотрите созданные выходные данные со сводными строками в конце.</span><span class="sxs-lookup"><span data-stu-id="438bd-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="438bd-153">Обратите внимание, что имеются изменения по сравнению с первым прогоном.</span><span class="sxs-lookup"><span data-stu-id="438bd-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="438bd-154">Запустите эту конфигурацию в режиме отладки, чтобы проверить собранные данные инвентаризации и суммирования</span><span class="sxs-lookup"><span data-stu-id="438bd-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="438bd-155">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="438bd-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="438bd-156">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="438bd-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="438bd-157">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="438bd-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="438bd-158">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="438bd-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="438bd-159">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="438bd-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="438bd-160">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="438bd-160">Click User parameters.</span></span>
7. <span data-ttu-id="438bd-161">Выберите "Да" в поле "Запустить в режиме отладки".</span><span class="sxs-lookup"><span data-stu-id="438bd-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="438bd-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="438bd-162">Click OK.</span></span>
9. <span data-ttu-id="438bd-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="438bd-163">Close the page.</span></span>
10. <span data-ttu-id="438bd-164">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="438bd-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="438bd-165">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="438bd-165">Click Output.</span></span>
12. <span data-ttu-id="438bd-166">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="438bd-166">Click Report.</span></span>
13. <span data-ttu-id="438bd-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="438bd-167">Click OK.</span></span>
14. <span data-ttu-id="438bd-168">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="438bd-168">Close the page.</span></span>
15. <span data-ttu-id="438bd-169">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="438bd-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="438bd-170">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="438bd-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="438bd-171">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="438bd-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="438bd-172">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="438bd-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="438bd-173">Щелкните "Журналы отладки".</span><span class="sxs-lookup"><span data-stu-id="438bd-173">Click Debug logs.</span></span>
    * <span data-ttu-id="438bd-174">Обратите внимание, что запись журнала отладки была создана для процесса выполнения выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="438bd-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="438bd-175">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="438bd-175">Click Attach.</span></span>
21. <span data-ttu-id="438bd-176">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="438bd-176">Click Open.</span></span>
    * <span data-ttu-id="438bd-177">Просмотрите созданный XML-файл, который содержит сведения об инвентаризации и суммировании, которые были собраны во время выполнения выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="438bd-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

