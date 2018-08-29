--- 
title: "Определение сопоставлений моделей электронной отчетности и выбор источников данных для них"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2beda3555274fee3f17ad13c54c6823307216385
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="45502-103">Определение сопоставлений моделей электронной отчетности и выбор источников данных для них</span><span class="sxs-lookup"><span data-stu-id="45502-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45502-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может выбрать источники данных для модели данных электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="45502-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="45502-105">Источники данных будут привязаны к отдельным компонентам выбранной модели данных во время разработки, и будут обеспечивать заполнение этой модели данных бизнес-данными во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="45502-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="45502-106">В этом примере вам предстоит выбрать источники данных для существующей модели данных, созданной для компании-образца Litware, Inc. Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание новой модели данных".</span><span class="sxs-lookup"><span data-stu-id="45502-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="45502-107">Открытие дерева "Конфигурация электронной отчетности"</span><span class="sxs-lookup"><span data-stu-id="45502-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="45502-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="45502-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="45502-109">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="45502-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="45502-110">Вставка нового сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="45502-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="45502-111">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="45502-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="45502-112">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="45502-112">Click Designer.</span></span>
3. <span data-ttu-id="45502-113">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="45502-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="45502-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="45502-114">Click New.</span></span>
    * <span data-ttu-id="45502-115">В результате будет создана новая запись, обеспечивающая сопоставление модели данных с источниками данных.</span><span class="sxs-lookup"><span data-stu-id="45502-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="45502-116">В этом примере вам предстоит сопоставить модель данных с источниками данных для желаемого типа платежа: кредитовый перевод.</span><span class="sxs-lookup"><span data-stu-id="45502-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="45502-117">Для конкретной модели данных можно создать несколько сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="45502-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="45502-118">Например, можно создать сопоставление для различных типов платежей, например для прямого дебета или кредитовых переводов.</span><span class="sxs-lookup"><span data-stu-id="45502-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="45502-119">В этом примере вам предстоит создать сопоставление для кредитовых переводов.</span><span class="sxs-lookup"><span data-stu-id="45502-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="45502-120">В поле "Имя" введите "Сопоставление для кредитных переводов".</span><span class="sxs-lookup"><span data-stu-id="45502-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="45502-121">Сопоставление для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="45502-121">CT mapping</span></span>  
6. <span data-ttu-id="45502-122">В поле "Описание" введите "Модель платежа с сопоставлением для кредитовых переводов".</span><span class="sxs-lookup"><span data-stu-id="45502-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="45502-123">Модель платежа с сопоставлением для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="45502-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="45502-124">В поле "Определение" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="45502-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="45502-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="45502-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="45502-126">Разрешить изменения определения.</span><span class="sxs-lookup"><span data-stu-id="45502-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="45502-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="45502-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="45502-128">Определение необходимых источников данных для текущего сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="45502-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="45502-129">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="45502-129">Click Designer.</span></span>
2. <span data-ttu-id="45502-130">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="45502-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="45502-131">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="45502-131">Click Add root.</span></span>
    * <span data-ttu-id="45502-132">Введите этот источник данных для доступа к проводкам по платежам.</span><span class="sxs-lookup"><span data-stu-id="45502-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="45502-133">В поле "Имя" введите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="45502-134">Транзакции</span><span class="sxs-lookup"><span data-stu-id="45502-134">Transactions</span></span>  
5. <span data-ttu-id="45502-135">В поле "Метка" введите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="45502-136">Транзакции</span><span class="sxs-lookup"><span data-stu-id="45502-136">Transactions</span></span>  
6. <span data-ttu-id="45502-137">В поле "Справка" введите "Строки журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="45502-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="45502-138">Строки журнала ГК</span><span class="sxs-lookup"><span data-stu-id="45502-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="45502-139">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="45502-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="45502-140">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="45502-140">Select Yes.</span></span>  
8. <span data-ttu-id="45502-141">В поле "Таблица" введите "LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="45502-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="45502-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="45502-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="45502-143">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-143">Click OK.</span></span>
    * <span data-ttu-id="45502-144">Выберите таблицу LedgerJournalTrans в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="45502-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="45502-145">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="45502-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="45502-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45502-146">Click Add.</span></span>
    * <span data-ttu-id="45502-147">Щелкните "Добавить", чтобы добавить новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="45502-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="45502-148">В поле "Имя" введите "$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="45502-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="45502-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="45502-149">$EndToEndID</span></span>  
13. <span data-ttu-id="45502-150">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="45502-150">Click Edit formula.</span></span>
14. <span data-ttu-id="45502-151">В дереве выберите "Строка\ОБЪЕДИНИТЬ".</span><span class="sxs-lookup"><span data-stu-id="45502-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="45502-152">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="45502-152">Click Add function.</span></span>
16. <span data-ttu-id="45502-153">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="45502-154">В дереве выберите "Проводки\Операция".</span><span class="sxs-lookup"><span data-stu-id="45502-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="45502-155">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="45502-155">Click Add data source.</span></span>
19. <span data-ttu-id="45502-156">В поле "Формула" введите "CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="45502-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="45502-157">Введите [ , “-“, ] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="45502-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="45502-158">В дереве выберите "Строка\ТЕКСТ".</span><span class="sxs-lookup"><span data-stu-id="45502-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="45502-159">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="45502-159">Click Add function.</span></span>
22. <span data-ttu-id="45502-160">В дереве выберите "Проводки\Код записи(RecId)".</span><span class="sxs-lookup"><span data-stu-id="45502-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="45502-161">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="45502-161">Click Add data source.</span></span>
24. <span data-ttu-id="45502-162">В поле "Формула" введите "в "CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="45502-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="45502-163">Введите [))] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="45502-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="45502-164">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="45502-164">Click Save.</span></span>
    * <span data-ttu-id="45502-165">Убедитесь, что при создании формулы ошибок не обнаружено.</span><span class="sxs-lookup"><span data-stu-id="45502-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="45502-166">См. вкладку "ОШИБКИ" под элементом управления редактора формул.</span><span class="sxs-lookup"><span data-stu-id="45502-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="45502-167">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-167">Close the page.</span></span>
27. <span data-ttu-id="45502-168">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-168">Click OK.</span></span>
    * <span data-ttu-id="45502-169">Добавьте вычисляемое поле в этот источник данных.</span><span class="sxs-lookup"><span data-stu-id="45502-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="45502-170">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="45502-170">Click Add.</span></span>
    * <span data-ttu-id="45502-171">Щелкните "Добавить", чтобы добавить новое вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="45502-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="45502-172">В поле "Имя" введите "$Amount".</span><span class="sxs-lookup"><span data-stu-id="45502-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="45502-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="45502-173">$Amount</span></span>  
30. <span data-ttu-id="45502-174">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="45502-174">Click Edit formula.</span></span>
31. <span data-ttu-id="45502-175">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="45502-176">В дереве выберите "Проводки\Дебит(AmountCurDebit)".</span><span class="sxs-lookup"><span data-stu-id="45502-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="45502-177">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="45502-177">Click Add data source.</span></span>
34. <span data-ttu-id="45502-178">В поле "Формула" введите "Transactions.AmountCurDebit - ".</span><span class="sxs-lookup"><span data-stu-id="45502-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="45502-179">Введите [ - ] в конце формулы.</span><span class="sxs-lookup"><span data-stu-id="45502-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="45502-180">В дереве выберите "Проводки\Кредит(AmountCurCredit)".</span><span class="sxs-lookup"><span data-stu-id="45502-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="45502-181">Щелкните "Добавить источник данных".</span><span class="sxs-lookup"><span data-stu-id="45502-181">Click Add data source.</span></span>
37. <span data-ttu-id="45502-182">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="45502-182">Click Save.</span></span>
38. <span data-ttu-id="45502-183">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-183">Close the page.</span></span>
39. <span data-ttu-id="45502-184">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-184">Click OK.</span></span>
    * <span data-ttu-id="45502-185">Вычисляемое поле $Amount будет добавлено в выбранный источник данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="45502-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="45502-186">В дереве выберите "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="45502-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="45502-187">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="45502-188">В дереве разверните или сверните "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="45502-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="45502-189">В дереве разверните или сверните "Проводки".</span><span class="sxs-lookup"><span data-stu-id="45502-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="45502-190">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="45502-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="45502-191">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="45502-191">Click Add root.</span></span>
    * <span data-ttu-id="45502-192">Введите этот источник данных для доступа к сведениям о банковском счете компании.</span><span class="sxs-lookup"><span data-stu-id="45502-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="45502-193">В поле "Имя" введите "BankAccount".</span><span class="sxs-lookup"><span data-stu-id="45502-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="45502-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="45502-194">BankAccount</span></span>  
47. <span data-ttu-id="45502-195">В поле "Метка" введите "Банковский счет".</span><span class="sxs-lookup"><span data-stu-id="45502-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="45502-196">Банковский счет</span><span class="sxs-lookup"><span data-stu-id="45502-196">Bank Account</span></span>  
48. <span data-ttu-id="45502-197">В поле "Справка" введите "Банковский счет".</span><span class="sxs-lookup"><span data-stu-id="45502-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="45502-198">Банковский счет</span><span class="sxs-lookup"><span data-stu-id="45502-198">Bank Account</span></span>  
49. <span data-ttu-id="45502-199">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="45502-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="45502-200">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="45502-200">Select Yes.</span></span>  
50. <span data-ttu-id="45502-201">В поле "Таблица" введите "BankAccountTable".</span><span class="sxs-lookup"><span data-stu-id="45502-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="45502-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="45502-202">BankAccountTable</span></span>  
51. <span data-ttu-id="45502-203">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-203">Click OK.</span></span>
    * <span data-ttu-id="45502-204">Выберите таблицу BankAccountTable в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="45502-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="45502-205">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="45502-205">Click Add root.</span></span>
    * <span data-ttu-id="45502-206">Введите этот источник данных для доступа к реквизитам компании.</span><span class="sxs-lookup"><span data-stu-id="45502-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="45502-207">В поле "Имя" введите "Компания".</span><span class="sxs-lookup"><span data-stu-id="45502-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="45502-208">Организация</span><span class="sxs-lookup"><span data-stu-id="45502-208">Company</span></span>  
54. <span data-ttu-id="45502-209">В поле "Метка" введите значение.</span><span class="sxs-lookup"><span data-stu-id="45502-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="45502-210">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="45502-210">Company information</span></span>  
55. <span data-ttu-id="45502-211">В поле "Справка" введите "Информация о компании".</span><span class="sxs-lookup"><span data-stu-id="45502-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="45502-212">Информация о компании</span><span class="sxs-lookup"><span data-stu-id="45502-212">Company information</span></span>  
56. <span data-ttu-id="45502-213">Выберите "Да" в поле "Запросить запрос".</span><span class="sxs-lookup"><span data-stu-id="45502-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="45502-214">Выберите "Да".</span><span class="sxs-lookup"><span data-stu-id="45502-214">Select Yes.</span></span>  
57. <span data-ttu-id="45502-215">В поле "Таблица" введите "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="45502-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="45502-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="45502-216">CompanyInfo</span></span>  
58. <span data-ttu-id="45502-217">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-217">Click OK.</span></span>
    * <span data-ttu-id="45502-218">Выберите таблицу CompanyInfo в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="45502-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="45502-219">В дереве выберите "Функции\Вычисляемое поле".</span><span class="sxs-lookup"><span data-stu-id="45502-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="45502-220">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="45502-220">Click Add root.</span></span>
    * <span data-ttu-id="45502-221">Вставьте вычисляемое поле как новый источник данных.</span><span class="sxs-lookup"><span data-stu-id="45502-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="45502-222">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="45502-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="45502-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="45502-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="45502-224">В поле "Метка" введите "Дата и время обработки".</span><span class="sxs-lookup"><span data-stu-id="45502-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="45502-225">Дата и время обработки</span><span class="sxs-lookup"><span data-stu-id="45502-225">Processing date & time</span></span>  
63. <span data-ttu-id="45502-226">Щелкните "Изменить формулу".</span><span class="sxs-lookup"><span data-stu-id="45502-226">Click Edit formula.</span></span>
64. <span data-ttu-id="45502-227">В дереве выберите "Date/time\SESSIONNOW".</span><span class="sxs-lookup"><span data-stu-id="45502-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="45502-228">Щелкните "Добавить функцию".</span><span class="sxs-lookup"><span data-stu-id="45502-228">Click Add function.</span></span>
66. <span data-ttu-id="45502-229">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="45502-229">Click Save.</span></span>
67. <span data-ttu-id="45502-230">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-230">Close the page.</span></span>
68. <span data-ttu-id="45502-231">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="45502-231">Click OK.</span></span>
    * <span data-ttu-id="45502-232">Добавьте вычисляемое поле ProcessingDateTime в качестве источника данных для текущей модели данных.</span><span class="sxs-lookup"><span data-stu-id="45502-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="45502-233">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="45502-233">Click Save.</span></span>
70. <span data-ttu-id="45502-234">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-234">Close the page.</span></span>
71. <span data-ttu-id="45502-235">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-235">Close the page.</span></span>
72. <span data-ttu-id="45502-236">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="45502-236">Close the page.</span></span>


