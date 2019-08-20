---
title: Проводка, связанная с гарантийным письмом
description: Эта процедура содержит указания по обработке гарантийного письма.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff105bdefff2ea93c853d590c77391653f50a4dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842001"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="30a26-103">Проводка, связанная с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="30a26-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30a26-104">Эта процедура содержит указания по обработке гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="30a26-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="30a26-105">Прежде чем выполнять эту процедуру, необходимо выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="30a26-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="30a26-106">Настроить банковские услуги и профили разноски для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="30a26-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="30a26-107">Создать соглашение о банковских услугах для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="30a26-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="30a26-108">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="30a26-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="30a26-109">Создание заказа на продажу с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="30a26-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="30a26-110">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="30a26-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="30a26-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="30a26-111">Click New.</span></span>
3. <span data-ttu-id="30a26-112">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="30a26-113">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="30a26-113">Expand the General section.</span></span>
5. <span data-ttu-id="30a26-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="30a26-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="30a26-116">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="30a26-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="30a26-118">В поле "Тип банковского документа" выберите "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="30a26-119">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="30a26-119">Click OK.</span></span>
11. <span data-ttu-id="30a26-120">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="30a26-121">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="30a26-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="30a26-122">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="30a26-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="30a26-123">Перейдите на вкладку "Поставка".</span><span class="sxs-lookup"><span data-stu-id="30a26-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="30a26-124">Примечание. Выберите "Контроль даты поставки = Нет"</span><span class="sxs-lookup"><span data-stu-id="30a26-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="30a26-125">В поле "Запрошенная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="30a26-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="30a26-126">В поле "Подтвержденная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="30a26-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="30a26-127">Обработка запроса гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="30a26-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="30a26-128">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="30a26-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="30a26-129">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="30a26-130">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="30a26-131">Щелкните "Запрос", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="30a26-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="30a26-132">В поле "Тип" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="30a26-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="30a26-134">В поле "Значение" введите число.</span><span class="sxs-lookup"><span data-stu-id="30a26-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="30a26-135">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="30a26-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="30a26-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-136">Click OK.</span></span>
10. <span data-ttu-id="30a26-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="30a26-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="30a26-138">Обработка отправки гарантийного письмо в банк</span><span class="sxs-lookup"><span data-stu-id="30a26-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="30a26-139">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="30a26-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="30a26-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="30a26-141">Щелкните "Отправить в банк", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="30a26-142">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="30a26-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="30a26-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="30a26-145">Обработка получения гарантийного письма от банка</span><span class="sxs-lookup"><span data-stu-id="30a26-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="30a26-146">Щелкните "Получить от банка", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="30a26-147">В поле "Код банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="30a26-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="30a26-148">Проверьте значения в рассчитываемых полях "Маржа" и "Расход".</span><span class="sxs-lookup"><span data-stu-id="30a26-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="30a26-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-149">Click OK.</span></span>
4. <span data-ttu-id="30a26-150">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="30a26-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="30a26-151">Подтвердите запись "Получить от банка".</span><span class="sxs-lookup"><span data-stu-id="30a26-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="30a26-152">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="30a26-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="30a26-153">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="30a26-153">Click Lines.</span></span>
    * <span data-ttu-id="30a26-154">Проверьте разноску записей журнала.</span><span class="sxs-lookup"><span data-stu-id="30a26-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="30a26-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="30a26-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="30a26-156">Обработка передачи гарантийное письмо бенефициару</span><span class="sxs-lookup"><span data-stu-id="30a26-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="30a26-157">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="30a26-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="30a26-158">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="30a26-159">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="30a26-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="30a26-160">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="30a26-161">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="30a26-162">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="30a26-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-163">Click OK.</span></span>
8. <span data-ttu-id="30a26-164">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="30a26-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="30a26-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="30a26-166">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="30a26-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-167">Click OK.</span></span>
12. <span data-ttu-id="30a26-168">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="30a26-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="30a26-169">Проверка запись "Передать бенефициару".</span><span class="sxs-lookup"><span data-stu-id="30a26-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="30a26-170">Обработка увеличения стоимости гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="30a26-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="30a26-171">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="30a26-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="30a26-172">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="30a26-173">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="30a26-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="30a26-174">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="30a26-175">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="30a26-176">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="30a26-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="30a26-177">В поле "Добавляемая стоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="30a26-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="30a26-178">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-178">Click OK.</span></span>
9. <span data-ttu-id="30a26-179">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="30a26-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="30a26-180">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="30a26-181">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="30a26-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="30a26-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-182">Click OK.</span></span>
13. <span data-ttu-id="30a26-183">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="30a26-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="30a26-184">Проверьте запись "Увеличить значение".</span><span class="sxs-lookup"><span data-stu-id="30a26-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="30a26-185">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="30a26-186">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="30a26-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="30a26-187">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="30a26-187">Click Lines.</span></span>
    * <span data-ttu-id="30a26-188">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="30a26-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="30a26-189">Обработка ликвидации гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="30a26-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="30a26-190">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="30a26-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="30a26-191">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="30a26-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="30a26-192">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="30a26-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="30a26-193">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="30a26-194">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="30a26-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="30a26-195">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="30a26-196">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-196">Click OK.</span></span>
8. <span data-ttu-id="30a26-197">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="30a26-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="30a26-198">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="30a26-199">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="30a26-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="30a26-200">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="30a26-200">Click OK.</span></span>
12. <span data-ttu-id="30a26-201">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="30a26-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="30a26-202">Проверьте запись "Ликвидировать".</span><span class="sxs-lookup"><span data-stu-id="30a26-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="30a26-203">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="30a26-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="30a26-204">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="30a26-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="30a26-205">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="30a26-205">Click Lines.</span></span>
    * <span data-ttu-id="30a26-206">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="30a26-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="30a26-207">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="30a26-207">Close the page.</span></span>

