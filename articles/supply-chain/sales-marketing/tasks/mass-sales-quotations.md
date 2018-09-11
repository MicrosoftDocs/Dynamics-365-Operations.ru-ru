--- 
title: "Создать предложения по продажам"
description: "Эта процедура демонстрирует, как эффективно создавать предложения, предлагающие набор продуктов или услуг, которые должны быть отправлены нескольким клиентам."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fe2d4cff512c32069f6aef3134e604b0ce6e47cc
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="3fb32-103">Создать предложения по продажам</span><span class="sxs-lookup"><span data-stu-id="3fb32-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3fb32-104">Эта процедура демонстрирует, как эффективно создавать предложения, предлагающие набор продуктов или услуг, которые должны быть отправлены нескольким клиентам.</span><span class="sxs-lookup"><span data-stu-id="3fb32-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="3fb32-105">Это массовое создание предложений основано на шаблонах предложений.</span><span class="sxs-lookup"><span data-stu-id="3fb32-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="3fb32-106">Эту процедуру можно выполнить со своими данными или с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="3fb32-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="3fb32-107">Создание шаблона предложений</span><span class="sxs-lookup"><span data-stu-id="3fb32-107">Create a quotation template</span></span>
1. <span data-ttu-id="3fb32-108">Перейдите в раздел "Продажи и маркетинг" > "Настройка" > "Предложения" > "Группы шаблонов".</span><span class="sxs-lookup"><span data-stu-id="3fb32-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="3fb32-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3fb32-109">Click New.</span></span>
3. <span data-ttu-id="3fb32-110">В поле "Код группы" введите код.</span><span class="sxs-lookup"><span data-stu-id="3fb32-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="3fb32-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3fb32-112">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3fb32-112">Click Save.</span></span>
6. <span data-ttu-id="3fb32-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-113">Close the page.</span></span>
7. <span data-ttu-id="3fb32-114">Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".</span><span class="sxs-lookup"><span data-stu-id="3fb32-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="3fb32-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3fb32-115">Click New.</span></span>
9. <span data-ttu-id="3fb32-116">В поле "Тип счета" выберите "Клиент".</span><span class="sxs-lookup"><span data-stu-id="3fb32-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="3fb32-117">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="3fb32-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3fb32-118">Click OK.</span></span>
    * <span data-ttu-id="3fb32-119">Чтобы предложение стало шаблоном, требуется выполнить этап настройки в заголовке предложения.</span><span class="sxs-lookup"><span data-stu-id="3fb32-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="3fb32-120">Это необходимо сделать перед добавлением строк в предложение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="3fb32-121">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="3fb32-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="3fb32-122">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="3fb32-122">Click Change view.</span></span>
14. <span data-ttu-id="3fb32-123">Щелкните Вид заголовка.</span><span class="sxs-lookup"><span data-stu-id="3fb32-123">Click Header view.</span></span>
15. <span data-ttu-id="3fb32-124">Разверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="3fb32-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="3fb32-125">В поле "Код группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="3fb32-126">В поле "Имя шаблона" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="3fb32-127">Выберите значение "Да" в поле "Активно".</span><span class="sxs-lookup"><span data-stu-id="3fb32-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="3fb32-128">Только активные шаблоны можно использовать при применении шаблона в новом предложении по продаже.</span><span class="sxs-lookup"><span data-stu-id="3fb32-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="3fb32-129">В области действий щелкните "Параметры".</span><span class="sxs-lookup"><span data-stu-id="3fb32-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="3fb32-130">Щелкните "Изменить режим просмотра".</span><span class="sxs-lookup"><span data-stu-id="3fb32-130">Click Change view.</span></span>
21. <span data-ttu-id="3fb32-131">Щелкните Линейное представление.</span><span class="sxs-lookup"><span data-stu-id="3fb32-131">Click Line view.</span></span>
22. <span data-ttu-id="3fb32-132">В поле "Номенклатура" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="3fb32-133">В поле "Номенклатура" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="3fb32-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-134">Close the page.</span></span>
25. <span data-ttu-id="3fb32-135">В поле "Процент скидки" введите число.</span><span class="sxs-lookup"><span data-stu-id="3fb32-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="3fb32-136">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="3fb32-136">Click Add line.</span></span>
27. <span data-ttu-id="3fb32-137">В поле "Номенклатура" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="3fb32-138">В поле "Номенклатура" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="3fb32-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-139">Close the page.</span></span>
30. <span data-ttu-id="3fb32-140">В поле "Цена за единицу" введите новую цену или измените текущую.</span><span class="sxs-lookup"><span data-stu-id="3fb32-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="3fb32-141">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="3fb32-141">Click Add line.</span></span>
32. <span data-ttu-id="3fb32-142">В поле "Номенклатура" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="3fb32-143">В поле "Номенклатура" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="3fb32-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-144">Close the page.</span></span>
35. <span data-ttu-id="3fb32-145">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="3fb32-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="3fb32-146">В поле "Скидка" введите число.</span><span class="sxs-lookup"><span data-stu-id="3fb32-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="3fb32-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3fb32-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="3fb32-148">Применение шаблона для создания одного предложения</span><span class="sxs-lookup"><span data-stu-id="3fb32-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="3fb32-149">Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".</span><span class="sxs-lookup"><span data-stu-id="3fb32-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3fb32-150">Обратите внимание, что предложение, только что созданное, отмечено как шаблон.</span><span class="sxs-lookup"><span data-stu-id="3fb32-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="3fb32-151">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3fb32-151">Click New.</span></span>
3. <span data-ttu-id="3fb32-152">В поле "Тип счета" выберите "Клиент".</span><span class="sxs-lookup"><span data-stu-id="3fb32-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="3fb32-153">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="3fb32-154">Разверните раздел "Шаблон".</span><span class="sxs-lookup"><span data-stu-id="3fb32-154">Expand the Template section.</span></span>
6. <span data-ttu-id="3fb32-155">В поле "Код группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="3fb32-156">В поле "Имя шаблона" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="3fb32-157">В поле "Способ расчета" выберите "Основано на значениях шаблона".</span><span class="sxs-lookup"><span data-stu-id="3fb32-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="3fb32-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3fb32-158">Click OK.</span></span>
    * <span data-ttu-id="3fb32-159">Теперь новое предложение создано на основе данных и условий шаблона.</span><span class="sxs-lookup"><span data-stu-id="3fb32-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="3fb32-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-160">Close the page.</span></span>
11. <span data-ttu-id="3fb32-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3fb32-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="3fb32-162">Применение шаблона для массового создания предложений</span><span class="sxs-lookup"><span data-stu-id="3fb32-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="3fb32-163">Перейдите в раздел "Продажи и маркетинг" > "Предложения по продажам" > "Обновление предложения" > "Массовое создание предложений".</span><span class="sxs-lookup"><span data-stu-id="3fb32-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="3fb32-164">В поле "Тип счета" выберите "Клиент".</span><span class="sxs-lookup"><span data-stu-id="3fb32-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="3fb32-165">В поле "Код группы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="3fb32-166">В поле "Имя шаблона" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3fb32-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="3fb32-167">В поле "Способ расчета" выберите "Основано на значениях шаблона".</span><span class="sxs-lookup"><span data-stu-id="3fb32-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="3fb32-168">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="3fb32-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="3fb32-169">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="3fb32-169">Click Filter.</span></span>
8. <span data-ttu-id="3fb32-170">В поле "Критерии" установите фильтр для покрытия диапазон клиентов, которых требуется включить в это массовое создание предложения.</span><span class="sxs-lookup"><span data-stu-id="3fb32-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="3fb32-171">Используйте следующий формат "Customer1..CustomerN".</span><span class="sxs-lookup"><span data-stu-id="3fb32-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="3fb32-172">Например, можно установить фильтр для: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="3fb32-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="3fb32-173">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3fb32-173">Click OK.</span></span>
10. <span data-ttu-id="3fb32-174">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3fb32-174">Click OK.</span></span>
11. <span data-ttu-id="3fb32-175">Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".</span><span class="sxs-lookup"><span data-stu-id="3fb32-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="3fb32-176">Убедитесь, что предложения были созданы для всех клиентов, указанных в процедуре массового обновления, как основанные на выбранном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="3fb32-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


