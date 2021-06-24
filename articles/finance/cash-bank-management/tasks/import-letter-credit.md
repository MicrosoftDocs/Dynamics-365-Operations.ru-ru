---
title: Импортный аккредитив
description: Эта процедура содержит указания по импорту аккредитива.
author: kweekley
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 841b4b4bb3c2f98ac65491a21bb991945c9f4bc9
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193937"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="c829d-103">Импортный аккредитив</span><span class="sxs-lookup"><span data-stu-id="c829d-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c829d-104">Эта процедура содержит указания по импорту аккредитива.</span><span class="sxs-lookup"><span data-stu-id="c829d-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="c829d-105">Перед выполнением этой процедуры необходимо настроить следующее: банковские кредиты, профили разноски, договора о банковских кредитах и сведения о банковском счете поставщика.</span><span class="sxs-lookup"><span data-stu-id="c829d-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="c829d-106">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c829d-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="c829d-107">Создание заказа на покупку с аккредитивом</span><span class="sxs-lookup"><span data-stu-id="c829d-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="c829d-108">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="c829d-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c829d-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c829d-109">Click New.</span></span>
3. <span data-ttu-id="c829d-110">В поле "Счет поставщика" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="c829d-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="c829d-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c829d-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c829d-113">Разверните раздел "Общие".</span><span class="sxs-lookup"><span data-stu-id="c829d-113">Expand the General section.</span></span>
7. <span data-ttu-id="c829d-114">В поле "Сайт" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="c829d-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c829d-116">В поле "Склад" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="c829d-117">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c829d-118">В поле "Дата учета" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="c829d-119">В поле "Дата поставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="c829d-120">Примечание. В поле "Тип банковского документа" необходимо выбрать значение "Аккредитив".</span><span class="sxs-lookup"><span data-stu-id="c829d-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="c829d-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-121">Click OK.</span></span>
14. <span data-ttu-id="c829d-122">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="c829d-123">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c829d-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="c829d-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c829d-125">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="c829d-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="c829d-126">Перейдите на вкладку "Поставка".</span><span class="sxs-lookup"><span data-stu-id="c829d-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="c829d-127">В поле "Дата поставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="c829d-128">В поле "Подтвержденная дата доставки" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="c829d-129">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="c829d-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="c829d-130">Определите сведения аккредитива.</span><span class="sxs-lookup"><span data-stu-id="c829d-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="c829d-131">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c829d-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="c829d-132">Щелкните "Аккредитив / импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="c829d-133">В поле "Дата заявления" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="c829d-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="c829d-134">Убедитесь, что в поле "Банковский счет" имеется активный банковский счет по умолчанию, который основан на дате подачи заявления.</span><span class="sxs-lookup"><span data-stu-id="c829d-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="c829d-135">В поле "Номер банковского документа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="c829d-136">В поле "Дата прихода" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="c829d-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="c829d-137">Разверните раздел "Банковский документ".</span><span class="sxs-lookup"><span data-stu-id="c829d-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="c829d-138">В поле "Дата окончания срока действия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="c829d-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="c829d-139">Разверните раздел "Сведения о банке".</span><span class="sxs-lookup"><span data-stu-id="c829d-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="c829d-140">В поле "Авизующий банк" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="c829d-141">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="c829d-142">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c829d-142">Click Save.</span></span>
33. <span data-ttu-id="c829d-143">Щелкните "Извлечь отгрузки по заказу на покупку".</span><span class="sxs-lookup"><span data-stu-id="c829d-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="c829d-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-144">Close the page.</span></span>
35. <span data-ttu-id="c829d-145">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="c829d-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="c829d-146">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="c829d-146">Click Confirm.</span></span>
37. <span data-ttu-id="c829d-147">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c829d-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="c829d-148">Щелкните "Аккредитив / импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="c829d-149">Щелкните "Обработать".</span><span class="sxs-lookup"><span data-stu-id="c829d-149">Click Process.</span></span>
40. <span data-ttu-id="c829d-150">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="c829d-150">Click Confirm.</span></span>
    * <span data-ttu-id="c829d-151">Убедитесь, что сальдо кредита уменьшает сумму покупки.</span><span class="sxs-lookup"><span data-stu-id="c829d-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="c829d-152">В этом примере сумма покупки = 500,00, кредитный лимит = 10000,00, поэтому сальдо кредита = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="c829d-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="c829d-153">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-153">Close the page.</span></span>
42. <span data-ttu-id="c829d-154">В поле "Цена за единицу" введите число.</span><span class="sxs-lookup"><span data-stu-id="c829d-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="c829d-155">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c829d-155">Click Save.</span></span>
44. <span data-ttu-id="c829d-156">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="c829d-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="c829d-157">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="c829d-157">Click Confirm.</span></span>
    * <span data-ttu-id="c829d-158">Измените аккредитив в соответствии с изменением в цене за единицу.</span><span class="sxs-lookup"><span data-stu-id="c829d-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="c829d-159">В области действий щелкните "Управлять".</span><span class="sxs-lookup"><span data-stu-id="c829d-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="c829d-160">Щелкните "Аккредитив / импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="c829d-161">Измените аккредитив в соответствии с изменением в цене единицы покупки.</span><span class="sxs-lookup"><span data-stu-id="c829d-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="c829d-162">Щелкните "Обработать".</span><span class="sxs-lookup"><span data-stu-id="c829d-162">Click Process.</span></span>
49. <span data-ttu-id="c829d-163">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="c829d-163">Click Amend.</span></span>
50. <span data-ttu-id="c829d-164">Щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="c829d-164">Click Remove.</span></span>
51. <span data-ttu-id="c829d-165">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="c829d-165">Click Yes.</span></span>
52. <span data-ttu-id="c829d-166">Щелкните "Извлечь отгрузки по заказу на покупку".</span><span class="sxs-lookup"><span data-stu-id="c829d-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="c829d-167">Щелкните "Обработать".</span><span class="sxs-lookup"><span data-stu-id="c829d-167">Click Process.</span></span>
54. <span data-ttu-id="c829d-168">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="c829d-168">Click Confirm.</span></span>
    * <span data-ttu-id="c829d-169">Убедитесь, что сальдо кредита уменьшает сумму покупки.</span><span class="sxs-lookup"><span data-stu-id="c829d-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="c829d-170">В этом примере измененная сумма покупки = 600,00, кредитный лимит = 10000,00, поэтому сальдо кредита = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="c829d-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="c829d-171">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="c829d-172">Разноска отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="c829d-172">Post Packing slip</span></span>
1. <span data-ttu-id="c829d-173">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="c829d-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="c829d-174">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="c829d-174">Click Product receipt.</span></span>
3. <span data-ttu-id="c829d-175">В поле PurchParmTable_Num введите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="c829d-176">Выберите номер отгрузки, созданной со ссылкой на аккредитив.</span><span class="sxs-lookup"><span data-stu-id="c829d-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="c829d-177">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c829d-178">В поле "Дата поступления продуктов" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="c829d-179">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-179">Click OK.</span></span>
7. <span data-ttu-id="c829d-180">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-180">Close the page.</span></span>
8. <span data-ttu-id="c829d-181">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="c829d-182">Проверка статуса импортного аккредитива</span><span class="sxs-lookup"><span data-stu-id="c829d-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="c829d-183">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="c829d-184">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c829d-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c829d-185">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c829d-186">Проверьте статус импортного аккредитива.</span><span class="sxs-lookup"><span data-stu-id="c829d-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="c829d-187">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-187">Close the page.</span></span>
5. <span data-ttu-id="c829d-188">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="c829d-189">Разноска накладной по покупке</span><span class="sxs-lookup"><span data-stu-id="c829d-189">Post purchase invoice</span></span>
1. <span data-ttu-id="c829d-190">Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="c829d-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="c829d-191">Выберите заказ на покупку, который был создан с аккредитивом.</span><span class="sxs-lookup"><span data-stu-id="c829d-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="c829d-192">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c829d-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c829d-193">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c829d-194">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="c829d-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="c829d-195">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="c829d-195">Click Invoice.</span></span>
6. <span data-ttu-id="c829d-196">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="c829d-197">В поле "Номер отгрузки" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="c829d-198">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c829d-199">В поле "Дата накладной" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="c829d-200">Щелкните "Обновить статус сопоставления".</span><span class="sxs-lookup"><span data-stu-id="c829d-200">Click Update match status.</span></span>
11. <span data-ttu-id="c829d-201">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="c829d-201">Click Post.</span></span>
12. <span data-ttu-id="c829d-202">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-202">Close the page.</span></span>
13. <span data-ttu-id="c829d-203">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-and-printing"></a><span data-ttu-id="c829d-204">Проверка и печать статуса импортного аккредитива</span><span class="sxs-lookup"><span data-stu-id="c829d-204">Verify Import letter of credit status and printing</span></span>

1. <span data-ttu-id="c829d-205">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="c829d-206">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c829d-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c829d-207">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c829d-208">Проверьте импортный аккредитив 2.</span><span class="sxs-lookup"><span data-stu-id="c829d-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="c829d-209">Проверка: Статус отгрузки = сведения об оприходованном банковском кредите</span><span class="sxs-lookup"><span data-stu-id="c829d-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="c829d-210">Щелкните "Вид".</span><span class="sxs-lookup"><span data-stu-id="c829d-210">Click View.</span></span>
5. <span data-ttu-id="c829d-211">Щелкните "Печать заявления".</span><span class="sxs-lookup"><span data-stu-id="c829d-211">Click Print application.</span></span>
6. <span data-ttu-id="c829d-212">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-212">Click OK.</span></span>
    * <span data-ttu-id="c829d-213">Проверьте, что аккредитив печатается.</span><span class="sxs-lookup"><span data-stu-id="c829d-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="c829d-214">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-214">Close the page.</span></span>
8. <span data-ttu-id="c829d-215">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-215">Close the page.</span></span>
9. <span data-ttu-id="c829d-216">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="c829d-217">Разноска журнала платежей поставщика для созданной накладной по покупке с аккредитивом</span><span class="sxs-lookup"><span data-stu-id="c829d-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="c829d-218">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="c829d-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c829d-219">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c829d-219">Click New.</span></span>
3. <span data-ttu-id="c829d-220">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="c829d-221">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c829d-222">Выберите Строки.</span><span class="sxs-lookup"><span data-stu-id="c829d-222">Click Lines.</span></span>
6. <span data-ttu-id="c829d-223">В поле "Дата" введите дату.</span><span class="sxs-lookup"><span data-stu-id="c829d-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="c829d-224">В поле "Счет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="c829d-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="c829d-225">Щелкните "Сопоставление проводок".</span><span class="sxs-lookup"><span data-stu-id="c829d-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="c829d-226">Развернуть раздел "Итоговые значения".</span><span class="sxs-lookup"><span data-stu-id="c829d-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="c829d-227">В поле "Показать" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="c829d-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="c829d-228">Убедитесь, что поля "Номер банковского документа" и "Номер отгрузки" были обновлены.</span><span class="sxs-lookup"><span data-stu-id="c829d-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="c829d-229">Установите флажок "Пометка".</span><span class="sxs-lookup"><span data-stu-id="c829d-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="c829d-230">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-230">Click OK.</span></span>
13. <span data-ttu-id="c829d-231">Перейдите на вкладку Платеж.</span><span class="sxs-lookup"><span data-stu-id="c829d-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="c829d-232">Убедитесь, что поля "Номер банковского документа" и "Номер отгрузки" были обновлены.</span><span class="sxs-lookup"><span data-stu-id="c829d-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="c829d-233">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="c829d-233">Click Post.</span></span>
15. <span data-ttu-id="c829d-234">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-234">Close the page.</span></span>
16. <span data-ttu-id="c829d-235">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="c829d-236">Проверка статуса импортного аккредитива после оплаты накладной</span><span class="sxs-lookup"><span data-stu-id="c829d-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="c829d-237">Перейдите в раздел "Управление банком и кассовыми операциями" > "Аккредитивы" > "Импортный аккредитив и импортное инкассо".</span><span class="sxs-lookup"><span data-stu-id="c829d-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="c829d-238">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="c829d-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c829d-239">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c829d-240">Проверьте статус импортного аккредитива.</span><span class="sxs-lookup"><span data-stu-id="c829d-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="c829d-241">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="c829d-242">Проверка лимита банковского кредита и отчета по использованию</span><span class="sxs-lookup"><span data-stu-id="c829d-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="c829d-243">Перейдите в раздел "Управление банком и кассовыми операциями" > "Запросы и отчеты" > "Аккредитивы или гарантийные письма" > "Отчет о банковских услугах и использовании".</span><span class="sxs-lookup"><span data-stu-id="c829d-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="c829d-244">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="c829d-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="c829d-245">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="c829d-245">Click Filter.</span></span>
    * <span data-ttu-id="c829d-246">Определите поле "Критерии", указав требуемый банковский счет.</span><span class="sxs-lookup"><span data-stu-id="c829d-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="c829d-247">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="c829d-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="c829d-248">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c829d-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c829d-249">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-249">Click OK.</span></span>
7. <span data-ttu-id="c829d-250">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c829d-250">Click OK.</span></span>
    * <span data-ttu-id="c829d-251">Проверьте отчет, в котором перечисляются проводки.</span><span class="sxs-lookup"><span data-stu-id="c829d-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="c829d-252">Проверьте, что в отчете есть проводки с номером банковского документа, кредитным лимитом, использованной суммой и суммой сальдо кредита.</span><span class="sxs-lookup"><span data-stu-id="c829d-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="c829d-253">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c829d-253">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]