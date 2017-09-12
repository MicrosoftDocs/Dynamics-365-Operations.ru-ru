--- 
title: "Экспорт аккредитива"
description: "Эта процедура содержит указания по обработке экспортного аккредитива."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 07fef304361fa0008f57425ff27596e4e382072a
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="76789-103">Экспорт аккредитива</span><span class="sxs-lookup"><span data-stu-id="76789-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76789-104">Эта процедура содержит указания по обработке экспортного аккредитива.</span><span class="sxs-lookup"><span data-stu-id="76789-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="76789-105">Аккредитив — это соглашение, выданное банком, в котором банк соглашается обеспечить платеж от имени покупателя, если будут выполнены условия соглашения между покупателем и продавцом.</span><span class="sxs-lookup"><span data-stu-id="76789-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="76789-106">Выполните процедуры "Настройка банковских услуг и профилей разноски" и "Создание соглашения о банковских услугах для аккредитива" перед выполнением этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="76789-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="76789-107">Для успешного выполнения этой процедуры необходимо выбрать демонстрационную компанию USMF.</span><span class="sxs-lookup"><span data-stu-id="76789-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="76789-108">Создание заказа на продажу для аккредитива</span><span class="sxs-lookup"><span data-stu-id="76789-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="76789-109">Перейдите в раздел "Расчеты с клиентами" > "Заказы" > "Все заказы на продажу".</span><span class="sxs-lookup"><span data-stu-id="76789-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="76789-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76789-110">Click New.</span></span>
3. <span data-ttu-id="76789-111">В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="76789-112">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="76789-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="76789-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="76789-114">Разверните или сверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="76789-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="76789-115">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="76789-116">Выберите место, где хранится номенклатура, подлежащая выдаче.</span><span class="sxs-lookup"><span data-stu-id="76789-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="76789-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="76789-118">В поле "Склад" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="76789-119">Выберите склад, где хранится номенклатура, подлежащая выдаче.</span><span class="sxs-lookup"><span data-stu-id="76789-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="76789-120">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="76789-121">Примечание. В поле "Тип банковского документа" необходимо выбрать значение "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="76789-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="76789-122">В поле "Тип банковского документа" выберите "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="76789-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="76789-123">Разверните или сверните раздел "Поставка".</span><span class="sxs-lookup"><span data-stu-id="76789-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="76789-124">Выберите "Контроль даты поставки = Нет"</span><span class="sxs-lookup"><span data-stu-id="76789-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="76789-125">В поле "Запрошенная дата прихода" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="76789-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-126">Click OK.</span></span>
15. <span data-ttu-id="76789-127">В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="76789-128">Выберите обязательную номенклатуру для выдачи/продажи.</span><span class="sxs-lookup"><span data-stu-id="76789-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="76789-129">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="76789-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="76789-130">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="76789-131">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="76789-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="76789-132">Разверните или сверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="76789-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="76789-133">Перейдите на вкладку "Поставка".</span><span class="sxs-lookup"><span data-stu-id="76789-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="76789-134">В поле "Запрошенная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="76789-135">В поле "Подтвержденная дата отгрузки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="76789-136">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="76789-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="76789-137">Щелкните "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="76789-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="76789-138">В поле "Номер банковского документа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="76789-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="76789-139">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="76789-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="76789-140">Разверните или сверните раздел "Сведения о банке".</span><span class="sxs-lookup"><span data-stu-id="76789-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="76789-141">В поле "Выставляющий банк" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="76789-142">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="76789-143">В поле "Авизующий банк" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="76789-144">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="76789-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="76789-145">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="76789-146">Щелкните "Извлечь отгрузки по заказу на продажу".</span><span class="sxs-lookup"><span data-stu-id="76789-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="76789-147">Щелкните "Выдать банковский документ".</span><span class="sxs-lookup"><span data-stu-id="76789-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="76789-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="76789-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="76789-149">Разноска отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="76789-149">Post Packing slip</span></span>
1. <span data-ttu-id="76789-150">В области действий щелкните "Комплектация и упаковка".</span><span class="sxs-lookup"><span data-stu-id="76789-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="76789-151">Щелкните "Разноска отборочной накладной".</span><span class="sxs-lookup"><span data-stu-id="76789-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="76789-152">Разверните или сверните раздел "Параметры".</span><span class="sxs-lookup"><span data-stu-id="76789-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="76789-153">В поле "Количество" выберите значение "Все".</span><span class="sxs-lookup"><span data-stu-id="76789-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="76789-154">Разверните или сверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="76789-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="76789-155">В поле "Дата отборочной накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="76789-156">Выберите номер отгрузки.</span><span class="sxs-lookup"><span data-stu-id="76789-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="76789-157">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="76789-158">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-158">Click OK.</span></span>
10. <span data-ttu-id="76789-159">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="76789-160">Разноска накладной по продаже</span><span class="sxs-lookup"><span data-stu-id="76789-160">Post sales invoice</span></span>
1. <span data-ttu-id="76789-161">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="76789-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="76789-162">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="76789-162">Click Invoice.</span></span>
3. <span data-ttu-id="76789-163">Разверните или сверните раздел "Обзор".</span><span class="sxs-lookup"><span data-stu-id="76789-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="76789-164">Выберите номер отгрузки.</span><span class="sxs-lookup"><span data-stu-id="76789-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="76789-165">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="76789-166">Разверните или сверните раздел "Настройка".</span><span class="sxs-lookup"><span data-stu-id="76789-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="76789-167">В поле "Дата накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="76789-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-168">Click OK.</span></span>
9. <span data-ttu-id="76789-169">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="76789-170">Состояние "Отправлено" документа отгрузки</span><span class="sxs-lookup"><span data-stu-id="76789-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="76789-171">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="76789-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="76789-172">Щелкните "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="76789-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="76789-173">Разверните или сверните раздел "Строки".</span><span class="sxs-lookup"><span data-stu-id="76789-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="76789-174">Примечание. В поле "Документ отправлен" должно быть установлено значение "Да".</span><span class="sxs-lookup"><span data-stu-id="76789-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="76789-175">Проверка экспортного аккредитива</span><span class="sxs-lookup"><span data-stu-id="76789-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="76789-176">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Экспортный аккредитив и импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="76789-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="76789-177">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="76789-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="76789-178">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="76789-179">Убедитесь, что экспортный аккредитив имеет статус отгрузки "Отгружено".</span><span class="sxs-lookup"><span data-stu-id="76789-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="76789-180">Клиентский платеж</span><span class="sxs-lookup"><span data-stu-id="76789-180">Customer payment</span></span>
1. <span data-ttu-id="76789-181">Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="76789-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="76789-182">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="76789-182">Click New.</span></span>
3. <span data-ttu-id="76789-183">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="76789-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="76789-184">В поле "Имя" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="76789-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="76789-185">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="76789-186">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="76789-186">Click Lines.</span></span>
7. <span data-ttu-id="76789-187">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="76789-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="76789-188">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="76789-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="76789-189">Щелкните "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="76789-189">Click Settlement.</span></span>
10. <span data-ttu-id="76789-190">Установите флажок в заголовке "Итоговые значения".</span><span class="sxs-lookup"><span data-stu-id="76789-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="76789-191">Примечание. Установите для поля "Показать" значение "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="76789-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="76789-192">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="76789-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="76789-193">Установите или снимите флажок "Пометка".</span><span class="sxs-lookup"><span data-stu-id="76789-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="76789-194">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="76789-194">Click OK.</span></span>
14. <span data-ttu-id="76789-195">Перейдите на вкладку Платеж.</span><span class="sxs-lookup"><span data-stu-id="76789-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="76789-196">Проверка номера банковского документа и номера отгрузки</span><span class="sxs-lookup"><span data-stu-id="76789-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="76789-197">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="76789-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="76789-198">Проверка экспортного аккредитива после платежа</span><span class="sxs-lookup"><span data-stu-id="76789-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="76789-199">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Экспортный аккредитив и импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="76789-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="76789-200">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="76789-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="76789-201">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="76789-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="76789-202">Проверьте, что "Статус отгрузки = Платеж получен" и "Сальдо = 0.00".</span><span class="sxs-lookup"><span data-stu-id="76789-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


