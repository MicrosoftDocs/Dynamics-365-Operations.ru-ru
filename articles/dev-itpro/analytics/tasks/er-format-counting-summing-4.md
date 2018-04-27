--- 
title: "Выполнения формата для подсчета и суммирования"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e3569e48bcc063b2423a60038732e8e53dbea2cb
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a><span data-ttu-id="1bf68-103">Выполнения формата для подсчета и суммирования</span><span class="sxs-lookup"><span data-stu-id="1bf68-103">Run the format to do counting and summing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bf68-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1bf68-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="1bf68-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="1bf68-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1bf68-106">Для выполнения этих шагов необходимо сначала выполнить шаги из процедуры "Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 3. Использование вычислений для создания выходных данных)".</span><span class="sxs-lookup"><span data-stu-id="1bf68-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="1bf68-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="1bf68-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="1bf68-108">Проверьте эту конфигурацию для создания отчетов "Интрастат"</span><span class="sxs-lookup"><span data-stu-id="1bf68-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="1bf68-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="1bf68-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1bf68-110">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="1bf68-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1bf68-111">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="1bf68-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="1bf68-112">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="1bf68-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="1bf68-113">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="1bf68-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="1bf68-114">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="1bf68-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="1bf68-115">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="1bf68-115">Click User parameters.</span></span>
8. <span data-ttu-id="1bf68-116">Выберите "Да" в поле "Запустить настройки".</span><span class="sxs-lookup"><span data-stu-id="1bf68-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="1bf68-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bf68-117">Click OK.</span></span>
10. <span data-ttu-id="1bf68-118">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="1bf68-118">Click Edit.</span></span>
11. <span data-ttu-id="1bf68-119">Выберите "Да" в поле "Запустить черновик".</span><span class="sxs-lookup"><span data-stu-id="1bf68-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="1bf68-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1bf68-120">Click Save.</span></span>
13. <span data-ttu-id="1bf68-121">Перейдите в раздел "Налог" > "Настройка" > "Внешняя торговля" > "Параметры внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="1bf68-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="1bf68-122">Разверните раздел "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="1bf68-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="1bf68-123">Выберите конфигурацию "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="1bf68-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="1bf68-124">Выберите конфигурацию "Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="1bf68-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="1bf68-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="1bf68-125">Click Save.</span></span>
18. <span data-ttu-id="1bf68-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1bf68-126">Close the page.</span></span>
19. <span data-ttu-id="1bf68-127">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="1bf68-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="1bf68-128">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="1bf68-128">Click Output.</span></span>
21. <span data-ttu-id="1bf68-129">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="1bf68-129">Click Report.</span></span>
    * <span data-ttu-id="1bf68-130">Запустите процесс создания отчета Интрастат.</span><span class="sxs-lookup"><span data-stu-id="1bf68-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="1bf68-131">В поле "Начальная дата" установите для даты значение "01.01.2000".</span><span class="sxs-lookup"><span data-stu-id="1bf68-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="1bf68-132">Определите начальную и конечную даты отчетного периода, который включает существующие даты в проводках формы.</span><span class="sxs-lookup"><span data-stu-id="1bf68-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="1bf68-133">В поле "Конечная дата" установите для даты значение "31.12.2022".</span><span class="sxs-lookup"><span data-stu-id="1bf68-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="1bf68-134">Определите начальную и конечную даты отчетного периода, который включает существующие даты в проводках формы.</span><span class="sxs-lookup"><span data-stu-id="1bf68-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="1bf68-135">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="1bf68-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="1bf68-136">Выберите значение "Да" в поле "Создать файл".</span><span class="sxs-lookup"><span data-stu-id="1bf68-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="1bf68-137">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bf68-137">Click OK.</span></span>
    * <span data-ttu-id="1bf68-138">Просмотрите созданные выходные данные со сводными строками в конце.</span><span class="sxs-lookup"><span data-stu-id="1bf68-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="1bf68-139">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="1bf68-139">Click New.</span></span>
28. <span data-ttu-id="1bf68-140">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1bf68-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="1bf68-141">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="1bf68-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="1bf68-142">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1bf68-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="1bf68-143">В поле "Товар" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1bf68-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="1bf68-144">Задайте вес равным "10".</span><span class="sxs-lookup"><span data-stu-id="1bf68-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="1bf68-145">Задайте сумму накладной "10000".</span><span class="sxs-lookup"><span data-stu-id="1bf68-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="1bf68-146">Задайте статистическую сумму "10000".</span><span class="sxs-lookup"><span data-stu-id="1bf68-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="1bf68-147">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="1bf68-147">Click Output.</span></span>
36. <span data-ttu-id="1bf68-148">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="1bf68-148">Click Report.</span></span>
37. <span data-ttu-id="1bf68-149">В поле "Направление" выберите "Поступление".</span><span class="sxs-lookup"><span data-stu-id="1bf68-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="1bf68-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bf68-150">Click OK.</span></span>
    * <span data-ttu-id="1bf68-151">Просмотрите созданные выходные данные со сводными строками в конце.</span><span class="sxs-lookup"><span data-stu-id="1bf68-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="1bf68-152">Обратите внимание, что имеются изменения по сравнению с первым прогоном.</span><span class="sxs-lookup"><span data-stu-id="1bf68-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="1bf68-153">Запустите эту конфигурацию в режиме отладки, чтобы проверить собранные данные инвентаризации и суммирования</span><span class="sxs-lookup"><span data-stu-id="1bf68-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="1bf68-154">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="1bf68-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1bf68-155">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="1bf68-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="1bf68-156">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="1bf68-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="1bf68-157">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="1bf68-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="1bf68-158">В области действий щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="1bf68-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="1bf68-159">Щелкните "Параметры пользователя".</span><span class="sxs-lookup"><span data-stu-id="1bf68-159">Click User parameters.</span></span>
7. <span data-ttu-id="1bf68-160">Выберите "Да" в поле "Запустить в режиме отладки".</span><span class="sxs-lookup"><span data-stu-id="1bf68-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="1bf68-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bf68-161">Click OK.</span></span>
9. <span data-ttu-id="1bf68-162">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1bf68-162">Close the page.</span></span>
10. <span data-ttu-id="1bf68-163">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="1bf68-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="1bf68-164">Щелкните "Вывести".</span><span class="sxs-lookup"><span data-stu-id="1bf68-164">Click Output.</span></span>
12. <span data-ttu-id="1bf68-165">Щелкните "Отчет".</span><span class="sxs-lookup"><span data-stu-id="1bf68-165">Click Report.</span></span>
13. <span data-ttu-id="1bf68-166">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="1bf68-166">Click OK.</span></span>
14. <span data-ttu-id="1bf68-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1bf68-167">Close the page.</span></span>
15. <span data-ttu-id="1bf68-168">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="1bf68-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="1bf68-169">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="1bf68-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="1bf68-170">В дереве разверните узел "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="1bf68-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="1bf68-171">В дереве выберите "Модель Интрастат\Интрастат (DE)\Интрастат (DE) с инвентаризацией и суммированием".</span><span class="sxs-lookup"><span data-stu-id="1bf68-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="1bf68-172">Щелкните "Журналы отладки".</span><span class="sxs-lookup"><span data-stu-id="1bf68-172">Click Debug logs.</span></span>
    * <span data-ttu-id="1bf68-173">Обратите внимание, что запись журнала отладки была создана для процесса выполнения выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1bf68-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="1bf68-174">Щелкните "Привязать".</span><span class="sxs-lookup"><span data-stu-id="1bf68-174">Click Attach.</span></span>
21. <span data-ttu-id="1bf68-175">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="1bf68-175">Click Open.</span></span>
    * <span data-ttu-id="1bf68-176">Просмотрите созданный XML-файл, который содержит сведения об инвентаризации и суммировании, которые были собраны во время выполнения выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1bf68-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


