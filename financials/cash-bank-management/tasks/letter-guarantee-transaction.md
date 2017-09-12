--- 
title: "Проводка, связанная с гарантийным письмом"
description: "Эта процедура содержит указания по обработке гарантийного письма."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 21895bcda8f0fe46e9b7c4b2189ca8b13e0dc012
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="c7e9b-103">Проводка, связанная с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="c7e9b-103">Letter of guarantee transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7e9b-104">Эта процедура содержит указания по обработке гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="c7e9b-105">Прежде чем выполнять эту процедуру, необходимо выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="c7e9b-106">Настроить банковские услуги и профили разноски для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="c7e9b-107">Создать соглашение о банковских услугах для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="c7e9b-108">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="c7e9b-109">Создание заказа на продажу с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="c7e9b-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="c7e9b-110">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c7e9b-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-111">Click New.</span></span>
3. <span data-ttu-id="c7e9b-112">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="c7e9b-113">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-113">Expand the General section.</span></span>
5. <span data-ttu-id="c7e9b-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="c7e9b-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c7e9b-116">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="c7e9b-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c7e9b-118">В поле "Тип банковского документа" выберите "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="c7e9b-119">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-119">Click OK.</span></span>
11. <span data-ttu-id="c7e9b-120">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="c7e9b-121">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="c7e9b-122">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="c7e9b-123">Перейдите на вкладку "Поставка".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="c7e9b-124">Примечание. Выберите "Контроль даты поставки = Нет"</span><span class="sxs-lookup"><span data-stu-id="c7e9b-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="c7e9b-125">В поле "Запрошенная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="c7e9b-126">В поле "Подтвержденная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="c7e9b-127">Обработка запроса гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="c7e9b-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="c7e9b-128">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="c7e9b-129">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="c7e9b-130">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="c7e9b-131">Щелкните "Запрос", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="c7e9b-132">В поле "Тип" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="c7e9b-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c7e9b-134">В поле "Значение" введите число.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="c7e9b-135">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="c7e9b-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-136">Click OK.</span></span>
10. <span data-ttu-id="c7e9b-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="c7e9b-138">Обработка отправки гарантийного письмо в банк</span><span class="sxs-lookup"><span data-stu-id="c7e9b-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="c7e9b-139">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="c7e9b-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c7e9b-141">Щелкните "Отправить в банк", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="c7e9b-142">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="c7e9b-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c7e9b-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="c7e9b-145">Обработка получения гарантийного письма от банка</span><span class="sxs-lookup"><span data-stu-id="c7e9b-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="c7e9b-146">Щелкните "Получить от банка", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="c7e9b-147">В поле "Код банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="c7e9b-148">Проверьте значения в рассчитываемых полях "Маржа" и "Расход".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="c7e9b-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-149">Click OK.</span></span>
4. <span data-ttu-id="c7e9b-150">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="c7e9b-151">Подтвердите запись "Получить от банка".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="c7e9b-152">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="c7e9b-153">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-153">Click Lines.</span></span>
    * <span data-ttu-id="c7e9b-154">Проверьте разноску записей журнала.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="c7e9b-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="c7e9b-156">Обработка передачи гарантийное письмо бенефициару</span><span class="sxs-lookup"><span data-stu-id="c7e9b-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="c7e9b-157">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c7e9b-158">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c7e9b-159">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c7e9b-160">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c7e9b-161">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c7e9b-162">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="c7e9b-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-163">Click OK.</span></span>
8. <span data-ttu-id="c7e9b-164">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="c7e9b-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c7e9b-166">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="c7e9b-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-167">Click OK.</span></span>
12. <span data-ttu-id="c7e9b-168">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="c7e9b-169">Проверка запись "Передать бенефициару".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="c7e9b-170">Обработка увеличения стоимости гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="c7e9b-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="c7e9b-171">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c7e9b-172">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c7e9b-173">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c7e9b-174">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c7e9b-175">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c7e9b-176">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="c7e9b-177">В поле "Добавляемая стоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="c7e9b-178">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-178">Click OK.</span></span>
9. <span data-ttu-id="c7e9b-179">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="c7e9b-180">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c7e9b-181">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="c7e9b-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-182">Click OK.</span></span>
13. <span data-ttu-id="c7e9b-183">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="c7e9b-184">Проверьте запись "Увеличить значение".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="c7e9b-185">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c7e9b-186">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="c7e9b-187">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-187">Click Lines.</span></span>
    * <span data-ttu-id="c7e9b-188">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="c7e9b-189">Обработка ликвидации гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="c7e9b-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="c7e9b-190">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c7e9b-191">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c7e9b-192">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c7e9b-193">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c7e9b-194">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c7e9b-195">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="c7e9b-196">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-196">Click OK.</span></span>
8. <span data-ttu-id="c7e9b-197">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="c7e9b-198">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c7e9b-199">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="c7e9b-200">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-200">Click OK.</span></span>
12. <span data-ttu-id="c7e9b-201">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="c7e9b-202">Проверьте запись "Ликвидировать".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="c7e9b-203">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c7e9b-204">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="c7e9b-205">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="c7e9b-205">Click Lines.</span></span>
    * <span data-ttu-id="c7e9b-206">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="c7e9b-207">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c7e9b-207">Close the page.</span></span>


