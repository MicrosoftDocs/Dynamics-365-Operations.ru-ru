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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f13ea1f9acd48cc1e7dce794369e89901bdb582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976342"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="3860a-103">Проводка, связанная с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="3860a-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3860a-104">Эта процедура содержит указания по обработке гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="3860a-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="3860a-105">Прежде чем выполнять эту процедуру, необходимо выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="3860a-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="3860a-106">Настроить банковские услуги и профили разноски для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="3860a-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="3860a-107">Создать соглашение о банковских услугах для гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="3860a-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="3860a-108">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="3860a-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="3860a-109">Создание заказа на продажу с гарантийным письмом</span><span class="sxs-lookup"><span data-stu-id="3860a-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="3860a-110">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="3860a-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3860a-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="3860a-111">Click New.</span></span>
3. <span data-ttu-id="3860a-112">В поле "Счет клиента" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="3860a-113">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="3860a-113">Expand the General section.</span></span>
5. <span data-ttu-id="3860a-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="3860a-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3860a-116">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="3860a-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3860a-118">В поле "Тип банковского документа" выберите "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="3860a-119">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="3860a-119">Click OK.</span></span>
11. <span data-ttu-id="3860a-120">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="3860a-121">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="3860a-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="3860a-122">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="3860a-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="3860a-123">Перейдите на вкладку "Поставка".</span><span class="sxs-lookup"><span data-stu-id="3860a-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="3860a-124">Примечание. Выберите "Контроль даты поставки = Нет"</span><span class="sxs-lookup"><span data-stu-id="3860a-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="3860a-125">В поле "Запрошенная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="3860a-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="3860a-126">В поле "Подтвержденная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="3860a-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="3860a-127">Обработка запроса гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="3860a-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="3860a-128">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="3860a-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="3860a-129">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="3860a-130">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="3860a-131">Щелкните "Запрос", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3860a-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="3860a-132">В поле "Тип" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="3860a-133">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3860a-134">В поле "Значение" введите число.</span><span class="sxs-lookup"><span data-stu-id="3860a-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="3860a-135">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="3860a-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="3860a-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-136">Click OK.</span></span>
10. <span data-ttu-id="3860a-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3860a-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="3860a-138">Обработка отправки гарантийного письмо в банк</span><span class="sxs-lookup"><span data-stu-id="3860a-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="3860a-139">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="3860a-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="3860a-140">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3860a-141">Щелкните "Отправить в банк", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="3860a-142">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="3860a-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3860a-144">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="3860a-145">Обработка получения гарантийного письма от банка</span><span class="sxs-lookup"><span data-stu-id="3860a-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="3860a-146">Щелкните "Получить от банка", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="3860a-147">В поле "Код банка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3860a-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="3860a-148">Проверьте значения в рассчитываемых полях "Маржа" и "Расход".</span><span class="sxs-lookup"><span data-stu-id="3860a-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="3860a-149">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-149">Click OK.</span></span>
4. <span data-ttu-id="3860a-150">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="3860a-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="3860a-151">Подтвердите запись "Получить от банка".</span><span class="sxs-lookup"><span data-stu-id="3860a-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="3860a-152">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="3860a-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="3860a-153">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="3860a-153">Click Lines.</span></span>
    * <span data-ttu-id="3860a-154">Проверьте разноску записей журнала.</span><span class="sxs-lookup"><span data-stu-id="3860a-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="3860a-155">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3860a-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="3860a-156">Обработка передачи гарантийное письмо бенефициару</span><span class="sxs-lookup"><span data-stu-id="3860a-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="3860a-157">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="3860a-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3860a-158">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3860a-159">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="3860a-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="3860a-160">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="3860a-161">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="3860a-162">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="3860a-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-163">Click OK.</span></span>
8. <span data-ttu-id="3860a-164">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="3860a-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="3860a-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="3860a-166">Щелкните "Передать бенефициару", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="3860a-167">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-167">Click OK.</span></span>
12. <span data-ttu-id="3860a-168">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="3860a-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="3860a-169">Проверка запись "Передать бенефициару".</span><span class="sxs-lookup"><span data-stu-id="3860a-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="3860a-170">Обработка увеличения стоимости гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="3860a-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="3860a-171">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="3860a-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3860a-172">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3860a-173">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="3860a-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="3860a-174">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="3860a-175">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="3860a-176">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3860a-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="3860a-177">В поле "Добавляемая стоимость" введите число.</span><span class="sxs-lookup"><span data-stu-id="3860a-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="3860a-178">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-178">Click OK.</span></span>
9. <span data-ttu-id="3860a-179">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="3860a-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="3860a-180">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="3860a-181">Щелкните "Увеличить значение", чтобы открыть раскрывающуюся форму диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3860a-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="3860a-182">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-182">Click OK.</span></span>
13. <span data-ttu-id="3860a-183">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="3860a-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="3860a-184">Проверьте запись "Увеличить значение".</span><span class="sxs-lookup"><span data-stu-id="3860a-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="3860a-185">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3860a-186">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="3860a-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="3860a-187">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="3860a-187">Click Lines.</span></span>
    * <span data-ttu-id="3860a-188">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="3860a-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="3860a-189">Обработка ликвидации гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="3860a-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="3860a-190">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="3860a-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3860a-191">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3860a-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3860a-192">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="3860a-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="3860a-193">Щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="3860a-194">В области действий щелкните "Гарантийное письмо".</span><span class="sxs-lookup"><span data-stu-id="3860a-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="3860a-195">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="3860a-196">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-196">Click OK.</span></span>
8. <span data-ttu-id="3860a-197">Перейдите в раздел "Управление банком и кассовыми операциями" > "Гарантийные письма" > "Гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="3860a-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="3860a-198">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="3860a-199">Щелкните "Ликвидировать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3860a-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="3860a-200">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3860a-200">Click OK.</span></span>
12. <span data-ttu-id="3860a-201">Разверните раздел "Действия".</span><span class="sxs-lookup"><span data-stu-id="3860a-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="3860a-202">Проверьте запись "Ликвидировать".</span><span class="sxs-lookup"><span data-stu-id="3860a-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="3860a-203">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3860a-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="3860a-204">Щелкните для перехода по ссылке в поле "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="3860a-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="3860a-205">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="3860a-205">Click Lines.</span></span>
    * <span data-ttu-id="3860a-206">Проверьте разнесенные записи журнала.</span><span class="sxs-lookup"><span data-stu-id="3860a-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="3860a-207">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3860a-207">Close the page.</span></span>

