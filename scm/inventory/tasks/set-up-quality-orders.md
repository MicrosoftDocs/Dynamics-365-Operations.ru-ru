---
title: "Настройка заказов на контроль качества"
description: "В этой процедуре показано, как включить процесс управления качеством, в котором входящие запасы должны проверяться сразу после регистрации прибытия."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: ru-ru
ms.lasthandoff: 09/12/2017

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="83abc-103">Настройка заказов на контроль качества</span><span class="sxs-lookup"><span data-stu-id="83abc-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83abc-104">В этой процедуре показано, как включить процесс управления качеством, в котором входящие запасы должны проверяться сразу после регистрации прибытия.</span><span class="sxs-lookup"><span data-stu-id="83abc-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="83abc-105">Эту процедуру обычно выполняет менеджер по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="83abc-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="83abc-106">Процесс включает создание группы контроля качества для определения номенклатур, которые будут использоваться для выборки, и группу проверки для группировки проверок, которые будут проходить номенклатуры в группе контроля качества.</span><span class="sxs-lookup"><span data-stu-id="83abc-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="83abc-107">Это руководство можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="83abc-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="83abc-108">Включение управления качеством</span><span class="sxs-lookup"><span data-stu-id="83abc-108">Enable quality management</span></span>
1. <span data-ttu-id="83abc-109">Перейдите в раздел "Управление запасами" > "Настройка" > "Параметры управления запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="83abc-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="83abc-110">Перейдите на вкладку "Управление качеством".</span><span class="sxs-lookup"><span data-stu-id="83abc-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="83abc-111">Установите параметр Используйте управление качеством как Да.</span><span class="sxs-lookup"><span data-stu-id="83abc-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="83abc-112">Щелкните "Настройка отчетов".</span><span class="sxs-lookup"><span data-stu-id="83abc-112">Click Report setup.</span></span>
    * <span data-ttu-id="83abc-113">В USMF настройка отчета для управления качеством уже определена.</span><span class="sxs-lookup"><span data-stu-id="83abc-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="83abc-114">Если это не было сделано, здесь необходимо добавить новые строки для различных типов отчетов и выбрать тип документа, который будет использоваться для каждого отчета.</span><span class="sxs-lookup"><span data-stu-id="83abc-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="83abc-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-115">Close the page.</span></span>
6. <span data-ttu-id="83abc-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="83abc-117">Создание проверки</span><span class="sxs-lookup"><span data-stu-id="83abc-117">Create a test</span></span>
1. <span data-ttu-id="83abc-118">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Проверки".</span><span class="sxs-lookup"><span data-stu-id="83abc-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="83abc-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-119">Click New.</span></span>
3. <span data-ttu-id="83abc-120">В поле "Проверка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="83abc-121">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83abc-122">В поле "Тип" выберите "Параметр".</span><span class="sxs-lookup"><span data-stu-id="83abc-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="83abc-123">В этом примере выберем "Параметр", который позволит назначить результаты проверки на основе предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="83abc-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="83abc-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-124">Click Save.</span></span>
7. <span data-ttu-id="83abc-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="83abc-126">Создание переменных проверки для определения способа записи результатов проверок</span><span class="sxs-lookup"><span data-stu-id="83abc-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="83abc-127">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Переменные проверки".</span><span class="sxs-lookup"><span data-stu-id="83abc-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="83abc-128">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-128">Click New.</span></span>
3. <span data-ttu-id="83abc-129">В поле "Переменная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="83abc-130">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83abc-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-131">Click Save.</span></span>
6. <span data-ttu-id="83abc-132">Щелкните "Результаты".</span><span class="sxs-lookup"><span data-stu-id="83abc-132">Click Outcomes.</span></span>
7. <span data-ttu-id="83abc-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-133">Click New.</span></span>
8. <span data-ttu-id="83abc-134">В поле "Результат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="83abc-135">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="83abc-136">В поле "Статус результата" выберите "Проверено".</span><span class="sxs-lookup"><span data-stu-id="83abc-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="83abc-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-137">Click Save.</span></span>
12. <span data-ttu-id="83abc-138">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-138">Click New.</span></span>
13. <span data-ttu-id="83abc-139">В поле "Результат" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="83abc-140">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="83abc-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-141">Click Save.</span></span>
16. <span data-ttu-id="83abc-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-142">Close the page.</span></span>
17. <span data-ttu-id="83abc-143">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="83abc-144">Настройка выборки номенклатур</span><span class="sxs-lookup"><span data-stu-id="83abc-144">Set up item sampling</span></span>
1. <span data-ttu-id="83abc-145">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Выборка номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="83abc-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="83abc-146">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-146">Click New.</span></span>
3. <span data-ttu-id="83abc-147">В поле "Выборка номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="83abc-148">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83abc-149">В поле "Значение" введите число.</span><span class="sxs-lookup"><span data-stu-id="83abc-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="83abc-150">Это значение относится к спецификации количества, выбранной в соседнем поле.</span><span class="sxs-lookup"><span data-stu-id="83abc-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="83abc-151">Разверните или сверните раздел "Процесс".</span><span class="sxs-lookup"><span data-stu-id="83abc-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="83abc-152">Установите или, если необходимо, снимите флажок "Полная блокировка".</span><span class="sxs-lookup"><span data-stu-id="83abc-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="83abc-153">Если этот флажок установлен, количество всего лота или строки заказа блокируется в случае, если проверка не пройдена.</span><span class="sxs-lookup"><span data-stu-id="83abc-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="83abc-154">В противном случае блокируются только номенклатуры в заказе для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="83abc-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="83abc-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-155">Click Save.</span></span>
9. <span data-ttu-id="83abc-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="83abc-157">Создание группы контроля качества</span><span class="sxs-lookup"><span data-stu-id="83abc-157">Create a quality group</span></span>
1. <span data-ttu-id="83abc-158">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Группы контроля качества".</span><span class="sxs-lookup"><span data-stu-id="83abc-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="83abc-159">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-159">Click New.</span></span>
3. <span data-ttu-id="83abc-160">В поле "Группа контроля качества" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="83abc-161">Используйте описательное имя, которое поможет узнать, какой тип номенклатур содержится в группе (критерии отбора).</span><span class="sxs-lookup"><span data-stu-id="83abc-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="83abc-162">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83abc-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-163">Click Save.</span></span>
6. <span data-ttu-id="83abc-164">Нажмите кнопку Добавление номенклатур.</span><span class="sxs-lookup"><span data-stu-id="83abc-164">Click Add items.</span></span>
7. <span data-ttu-id="83abc-165">Выберите строку "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="83abc-165">Select the Item number row</span></span>
    * <span data-ttu-id="83abc-166">В этом примере фильтрация выполняется на основании кода номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="83abc-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="83abc-167">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="83abc-168">Например, введите "T*", чтобы отфильтровать коды номенклатуры, начинающиеся с "T".</span><span class="sxs-lookup"><span data-stu-id="83abc-168">For example, type T* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="83abc-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="83abc-169">Click OK.</span></span>
10. <span data-ttu-id="83abc-170">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="83abc-170">Click OK.</span></span>
11. <span data-ttu-id="83abc-171">Щелкните "Группы контроля качества номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="83abc-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="83abc-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-172">Close the page.</span></span>
13. <span data-ttu-id="83abc-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="83abc-174">Создание проверочной группы</span><span class="sxs-lookup"><span data-stu-id="83abc-174">Create a test group</span></span>
1. <span data-ttu-id="83abc-175">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Группы проверки".</span><span class="sxs-lookup"><span data-stu-id="83abc-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="83abc-176">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-176">Click New.</span></span>
3. <span data-ttu-id="83abc-177">В поле "Группа проверки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="83abc-178">Присвойте группе проверки имя, которое поможет запомнить, какие типы проверки выполняются и с какой группой контроля она должна быть связана.</span><span class="sxs-lookup"><span data-stu-id="83abc-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="83abc-179">Например, если она должна использоваться с группой контроля качества, в которой выбираются номенклатуры, начинающиеся с "Т", ее можно назвать "Проверки номенклатур Т".</span><span class="sxs-lookup"><span data-stu-id="83abc-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="83abc-180">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="83abc-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="83abc-181">В поле "Выборка номенклатуры" выберите строку выборки номенклатуры, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="83abc-182">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="83abc-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="83abc-183">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="83abc-183">Click Add.</span></span>
8. <span data-ttu-id="83abc-184">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="83abc-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="83abc-185">В поле "Проверка" выберите проверку, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="83abc-186">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="83abc-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="83abc-187">Перейдите на вкладку Тест.</span><span class="sxs-lookup"><span data-stu-id="83abc-187">Click the Test tab.</span></span>
12. <span data-ttu-id="83abc-188">В поле "Переменная" выберите переменную проверки, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="83abc-189">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="83abc-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="83abc-190">В поле "Результат по умолчанию" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="83abc-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="83abc-191">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="83abc-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="83abc-192">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-192">Click Save.</span></span>
17. <span data-ttu-id="83abc-193">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="83abc-194">Определение времени создания заказов для контроля качества</span><span class="sxs-lookup"><span data-stu-id="83abc-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="83abc-195">Перейдите в раздел "Управление запасами" > "Настройка" > "Контроль качества" > "Сопоставления контроля качества".</span><span class="sxs-lookup"><span data-stu-id="83abc-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="83abc-196">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="83abc-196">Click New.</span></span>
3. <span data-ttu-id="83abc-197">В поле "Тип ссылки" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="83abc-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="83abc-198">В поле "Код номенклатуры" выберите "Группа".</span><span class="sxs-lookup"><span data-stu-id="83abc-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="83abc-199">В этом примере выберем значение "Группа" и используем группу контроля качества, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="83abc-200">Также можно установить значение "Таблица", чтобы указать номенклатуры вручную, или выбрать значение "Все", чтобы добавить все номенклатуры к заказу для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="83abc-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="83abc-201">В поле "Номенклатура" выберите группу контроля качества, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="83abc-202">Параметры, доступные в поле "Номенклатура", зависят от значения, указанного в поле "Код номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="83abc-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="83abc-203">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="83abc-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="83abc-204">Разверните или сверните раздел "Процесс".</span><span class="sxs-lookup"><span data-stu-id="83abc-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="83abc-205">В поле "Тип события" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="83abc-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="83abc-206">Это событие, которое запускает проверку.</span><span class="sxs-lookup"><span data-stu-id="83abc-206">This is the event that triggers the test.</span></span> <span data-ttu-id="83abc-207">Доступные параметры зависят от процесса, выбранного в поле "Тип ссылки".</span><span class="sxs-lookup"><span data-stu-id="83abc-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="83abc-208">В поле "Выполнение" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="83abc-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="83abc-209">Разверните или сверните раздел "Процесс контроля качества".</span><span class="sxs-lookup"><span data-stu-id="83abc-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="83abc-210">В поле "Блокировка событий" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="83abc-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="83abc-211">В этом поле отображается список процессов, которые можно заблокировать, если заказ для контроля качества все еще открыт.</span><span class="sxs-lookup"><span data-stu-id="83abc-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="83abc-212">Параметры зависят от значения, выбранного в поле "Тип события".</span><span class="sxs-lookup"><span data-stu-id="83abc-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="83abc-213">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="83abc-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="83abc-214">Это будет зависеть от предыдущих выбранных значений.</span><span class="sxs-lookup"><span data-stu-id="83abc-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="83abc-215">Укажите, следует ли блокировать следующие процессы, если имеются открытые заказы для контроля качества, связанные со строкой документа-источника.</span><span class="sxs-lookup"><span data-stu-id="83abc-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="83abc-216">Разверните или сверните раздел "Спецификации".</span><span class="sxs-lookup"><span data-stu-id="83abc-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="83abc-217">В поле "Группа проверки" выберите группу проверки, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="83abc-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="83abc-218">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="83abc-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="83abc-219">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="83abc-219">Click Save.</span></span>
17. <span data-ttu-id="83abc-220">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="83abc-220">Close the page.</span></span>

