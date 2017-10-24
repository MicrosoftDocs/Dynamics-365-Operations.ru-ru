--- 
title: "Определение сопоставления моделей и выбор источников данных для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может выбрать источники данных для модели данных электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 512e24b5d0e20f00890e2a9abfe45b660a913913
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="2fadc-103">Определение сопоставления моделей и выбор источников данных для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="2fadc-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2fadc-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может выбрать источники данных для модели данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="2fadc-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="2fadc-105">Источники данных будут привязаны к отдельным компонентам выбранной модели данных во время разработки, и будут обеспечивать заполнение этой модели данных бизнес-данными во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2fadc-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="2fadc-106">В этом примере вам предстоит выбрать источники данных для существующей модели данных, созданной для компании-образца Litware, Inc. Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание новой модели данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="2fadc-107">Открытие дерева "Конфигурация электронной отчетности"</span><span class="sxs-lookup"><span data-stu-id="2fadc-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="2fadc-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="2fadc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2fadc-109">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="2fadc-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="2fadc-110">Вставка нового сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="2fadc-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="2fadc-111">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="2fadc-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="2fadc-112">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="2fadc-112">Click Designer.</span></span>
3. <span data-ttu-id="2fadc-113">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="2fadc-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2fadc-114">Click New.</span></span>
    * <span data-ttu-id="2fadc-115">В результате будет создана новая запись, обеспечивающая сопоставление модели данных с источниками данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="2fadc-116">В этом примере вам предстоит сопоставить модель данных с источниками данных для желаемого типа платежа: кредитовый перевод.</span><span class="sxs-lookup"><span data-stu-id="2fadc-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="2fadc-117">Для конкретной модели данных можно создать несколько сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="2fadc-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="2fadc-118">Например, можно создать сопоставление для различных типов платежей, например для прямого дебета или кредитовых переводов.</span><span class="sxs-lookup"><span data-stu-id="2fadc-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="2fadc-119">В этом примере вам предстоит создать сопоставление для кредитовых переводов.</span><span class="sxs-lookup"><span data-stu-id="2fadc-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="2fadc-120">В поле "Имя" введите "Сопоставление для кредитных переводов".</span><span class="sxs-lookup"><span data-stu-id="2fadc-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="2fadc-121">Сопоставление для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="2fadc-121">CT mapping</span></span>  
6. <span data-ttu-id="2fadc-122">В поле "Описание" введите "Модель платежа с сопоставлением для кредитовых переводов".</span><span class="sxs-lookup"><span data-stu-id="2fadc-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="2fadc-123">Модель платежа с сопоставлением для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="2fadc-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="2fadc-124">В поле "Определение" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="2fadc-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="2fadc-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="2fadc-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="2fadc-126">Разрешить изменения определения.</span><span class="sxs-lookup"><span data-stu-id="2fadc-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="2fadc-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2fadc-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="2fadc-128">Определение необходимых источников данных для текущего сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="2fadc-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="2fadc-129">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="2fadc-129">Click Designer.</span></span>
2. <span data-ttu-id="2fadc-130">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="2fadc-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="2fadc-131">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="2fadc-131">Click Add root.</span></span>
    * <span data-ttu-id="2fadc-132">Введите этот источник данных для доступа к проводкам по платежам.</span><span class="sxs-lookup"><span data-stu-id="2fadc-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="2fadc-133">В поле "Имя" введите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="2fadc-134">Транзакции</span><span class="sxs-lookup"><span data-stu-id="2fadc-134">Transactions</span></span>  
5. <span data-ttu-id="2fadc-135">В поле "Метка" введите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="2fadc-136">Транзакции</span><span class="sxs-lookup"><span data-stu-id="2fadc-136">Transactions</span></span>  
6. <span data-ttu-id="2fadc-137">В поле "Справка" введите "Строки журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="2fadc-138">Строки журнала ГК</span><span class="sxs-lookup"><span data-stu-id="2fadc-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="2fadc-139">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="2fadc-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="2fadc-140">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="2fadc-140">Select Yes.</span></span>  
8. <span data-ttu-id="2fadc-141">В поле "Таблица" введите "LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="2fadc-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="2fadc-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="2fadc-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="2fadc-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-143">Click OK.</span></span>
    * <span data-ttu-id="2fadc-144">Выберите таблицу LedgerJournalTrans в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="2fadc-145">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="2fadc-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="2fadc-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="2fadc-146">Click Add.</span></span>
    * <span data-ttu-id="2fadc-147">Щелкните "Добавить", чтобы добавить новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="2fadc-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="2fadc-148">В поле "Имя" введите "$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="2fadc-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="2fadc-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="2fadc-149">$EndToEndID</span></span>  
13. <span data-ttu-id="2fadc-150">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="2fadc-150">Click Edit formula.</span></span>
14. <span data-ttu-id="2fadc-151">В дереве выберите "Строка\ОБЪЕДИНИТЬ".</span><span class="sxs-lookup"><span data-stu-id="2fadc-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="2fadc-152">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="2fadc-152">Click Add function.</span></span>
16. <span data-ttu-id="2fadc-153">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="2fadc-154">В дереве выберите "Проводки\Операция".</span><span class="sxs-lookup"><span data-stu-id="2fadc-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="2fadc-155">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-155">Click Add data source.</span></span>
19. <span data-ttu-id="2fadc-156">В поле "Формула" введите "CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="2fadc-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="2fadc-157">Введите [ , “-“, ] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="2fadc-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="2fadc-158">В дереве выберите "Строка\ТЕКСТ".</span><span class="sxs-lookup"><span data-stu-id="2fadc-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="2fadc-159">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="2fadc-159">Click Add function.</span></span>
22. <span data-ttu-id="2fadc-160">В дереве выберите "Проводки\Код записи(RecId)".</span><span class="sxs-lookup"><span data-stu-id="2fadc-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="2fadc-161">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-161">Click Add data source.</span></span>
24. <span data-ttu-id="2fadc-162">В поле "Формула" введите "в "CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="2fadc-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="2fadc-163">Введите [))] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="2fadc-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="2fadc-164">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2fadc-164">Click Save.</span></span>
    * <span data-ttu-id="2fadc-165">Убедитесь, что при создании формулы ошибок не обнаружено.</span><span class="sxs-lookup"><span data-stu-id="2fadc-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="2fadc-166">См. вкладку "ОШИБКИ" под элементом управления редактора формул.</span><span class="sxs-lookup"><span data-stu-id="2fadc-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="2fadc-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-167">Close the page.</span></span>
27. <span data-ttu-id="2fadc-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-168">Click OK.</span></span>
    * <span data-ttu-id="2fadc-169">Добавьте вычисляемое поле в этот источник данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="2fadc-170">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="2fadc-170">Click Add.</span></span>
    * <span data-ttu-id="2fadc-171">Щелкните "Добавить", чтобы добавить новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="2fadc-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="2fadc-172">В поле "Имя" введите "$Amount".</span><span class="sxs-lookup"><span data-stu-id="2fadc-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="2fadc-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="2fadc-173">$Amount</span></span>  
30. <span data-ttu-id="2fadc-174">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="2fadc-174">Click Edit formula.</span></span>
31. <span data-ttu-id="2fadc-175">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="2fadc-176">В дереве выберите "Проводки\Дебит(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="2fadc-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="2fadc-177">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-177">Click Add data source.</span></span>
34. <span data-ttu-id="2fadc-178">В поле "Формула" введите "Transactions.AmountCurDebit - ".</span><span class="sxs-lookup"><span data-stu-id="2fadc-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="2fadc-179">Введите [ - ] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="2fadc-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="2fadc-180">В дереве выберите "Проводки\Кредит(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="2fadc-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="2fadc-181">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="2fadc-181">Click Add data source.</span></span>
37. <span data-ttu-id="2fadc-182">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2fadc-182">Click Save.</span></span>
38. <span data-ttu-id="2fadc-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-183">Close the page.</span></span>
39. <span data-ttu-id="2fadc-184">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-184">Click OK.</span></span>
    * <span data-ttu-id="2fadc-185">Вычисляемое поле $Amount будет добавлено в выбранный источник данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="2fadc-186">В дереве выберите "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="2fadc-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="2fadc-187">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="2fadc-188">В дереве разверните или сверните "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="2fadc-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="2fadc-189">В дереве разверните или сверните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="2fadc-190">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="2fadc-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="2fadc-191">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="2fadc-191">Click Add root.</span></span>
    * <span data-ttu-id="2fadc-192">Введите этот источник данных для доступа к сведениям о банковском счете компании.</span><span class="sxs-lookup"><span data-stu-id="2fadc-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="2fadc-193">В поле "Имя" введите "BankAccount".</span><span class="sxs-lookup"><span data-stu-id="2fadc-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="2fadc-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="2fadc-194">BankAccount</span></span>  
47. <span data-ttu-id="2fadc-195">В поле "Метка" введите "Банковский счет".</span><span class="sxs-lookup"><span data-stu-id="2fadc-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="2fadc-196">Банковский счет</span><span class="sxs-lookup"><span data-stu-id="2fadc-196">Bank Account</span></span>  
48. <span data-ttu-id="2fadc-197">В поле "Справка" введите "Банковский счет".</span><span class="sxs-lookup"><span data-stu-id="2fadc-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="2fadc-198">Банковский счет</span><span class="sxs-lookup"><span data-stu-id="2fadc-198">Bank Account</span></span>  
49. <span data-ttu-id="2fadc-199">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="2fadc-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="2fadc-200">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="2fadc-200">Select Yes.</span></span>  
50. <span data-ttu-id="2fadc-201">В поле "Таблица" введите "BankAccountTable".</span><span class="sxs-lookup"><span data-stu-id="2fadc-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="2fadc-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="2fadc-202">BankAccountTable</span></span>  
51. <span data-ttu-id="2fadc-203">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-203">Click OK.</span></span>
    * <span data-ttu-id="2fadc-204">Выберите таблицу BankAccountTable в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="2fadc-205">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="2fadc-205">Click Add root.</span></span>
    * <span data-ttu-id="2fadc-206">Введите этот источник данных для доступа к реквизитам компании.</span><span class="sxs-lookup"><span data-stu-id="2fadc-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="2fadc-207">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="2fadc-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="2fadc-208">Организация</span><span class="sxs-lookup"><span data-stu-id="2fadc-208">Company</span></span>  
54. <span data-ttu-id="2fadc-209">В поле "Метка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2fadc-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="2fadc-210">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="2fadc-210">Company information</span></span>  
55. <span data-ttu-id="2fadc-211">В поле "Справка" введите "Информация о компании".</span><span class="sxs-lookup"><span data-stu-id="2fadc-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="2fadc-212">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="2fadc-212">Company information</span></span>  
56. <span data-ttu-id="2fadc-213">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="2fadc-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="2fadc-214">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="2fadc-214">Select Yes.</span></span>  
57. <span data-ttu-id="2fadc-215">В поле "Таблица" введите "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="2fadc-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="2fadc-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="2fadc-216">CompanyInfo</span></span>  
58. <span data-ttu-id="2fadc-217">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-217">Click OK.</span></span>
    * <span data-ttu-id="2fadc-218">Выберите таблицу CompanyInfo в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="2fadc-219">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="2fadc-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="2fadc-220">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="2fadc-220">Click Add root.</span></span>
    * <span data-ttu-id="2fadc-221">Вставьте вычисляемое поле как новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="2fadc-222">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="2fadc-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="2fadc-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="2fadc-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="2fadc-224">В поле "Метка" введите "Дата и время обработки".</span><span class="sxs-lookup"><span data-stu-id="2fadc-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="2fadc-225">Дата и время обработки</span><span class="sxs-lookup"><span data-stu-id="2fadc-225">Processing date & time</span></span>  
63. <span data-ttu-id="2fadc-226">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="2fadc-226">Click Edit formula.</span></span>
64. <span data-ttu-id="2fadc-227">В дереве выберите "Date/time\SESSIONNOW".</span><span class="sxs-lookup"><span data-stu-id="2fadc-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="2fadc-228">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="2fadc-228">Click Add function.</span></span>
66. <span data-ttu-id="2fadc-229">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2fadc-229">Click Save.</span></span>
67. <span data-ttu-id="2fadc-230">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-230">Close the page.</span></span>
68. <span data-ttu-id="2fadc-231">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="2fadc-231">Click OK.</span></span>
    * <span data-ttu-id="2fadc-232">Добавьте вычисляемое поле ProcessingDateTime в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="2fadc-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="2fadc-233">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2fadc-233">Click Save.</span></span>
70. <span data-ttu-id="2fadc-234">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-234">Close the page.</span></span>
71. <span data-ttu-id="2fadc-235">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-235">Close the page.</span></span>
72. <span data-ttu-id="2fadc-236">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2fadc-236">Close the page.</span></span>


