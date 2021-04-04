---
title: Электронная отчетность Сопоставление модели данных с выбранными источникам данных
description: В этой теме описывается сопоставление модели данных электронной отчетности (ER) с выбранными источниками данных Microsoft Dynamics 365 Finance.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b6f5e3b64e7d000feb7fa1ff84edd2e20891bb7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570670"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="c3859-103">Электронная отчетность Сопоставление модели данных с выбранными источникам данных</span><span class="sxs-lookup"><span data-stu-id="c3859-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3859-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может сопоставить модель данных электронной отчетности с выбранными источниками данных.</span><span class="sxs-lookup"><span data-stu-id="c3859-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="c3859-105">Это сопоставление модели позднее будет использоваться в качестве источника данных в конфигурации формата, которая будет использоваться для управления документами электронных платежей.</span><span class="sxs-lookup"><span data-stu-id="c3859-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="c3859-106">В этом примере вам предстоит сопоставить модель данных для компании-образца Litware, Inc. с источниками данных.</span><span class="sxs-lookup"><span data-stu-id="c3859-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="c3859-107">Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Выбор источников данных для сопоставления с моделью".</span><span class="sxs-lookup"><span data-stu-id="c3859-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="c3859-108">Открытие дерева конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="c3859-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="c3859-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="c3859-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c3859-110">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="c3859-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="c3859-111">Выбор созданного сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="c3859-111">Select created model mapping</span></span>
1. <span data-ttu-id="c3859-112">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="c3859-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="c3859-113">Убедитесь, что предварительно была создана конфигурация модели "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="c3859-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="c3859-114">В противном случае остановитесь сейчас и вернитесь по завершении руководства по задаче "Создание новой конфигурации с моделью данных выбранного домена".</span><span class="sxs-lookup"><span data-stu-id="c3859-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="c3859-115">Щелкните "Конструктор моделей".</span><span class="sxs-lookup"><span data-stu-id="c3859-115">Click Model designer.</span></span>
3. <span data-ttu-id="c3859-116">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="c3859-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="c3859-117">Выберите запись "Сопоставление для кредитовых переводов".</span><span class="sxs-lookup"><span data-stu-id="c3859-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="c3859-118">Сопоставление для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="c3859-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="c3859-119">Связывание созданных источников данных с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="c3859-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="c3859-120">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="c3859-120">Click Designer.</span></span>
2. <span data-ttu-id="c3859-121">В дереве выберите "Дата и время обработки(ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="c3859-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="c3859-122">В дереве выберите "Дата обработки(ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="c3859-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="c3859-123">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-123">Click Bind.</span></span>
5. <span data-ttu-id="c3859-124">В дереве выберите "Идентификатор платежного сообщения (MessageIdentification)".</span><span class="sxs-lookup"><span data-stu-id="c3859-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="c3859-125">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="c3859-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="c3859-126">В дереве выберите «Проводки\Номер партии журнала(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="c3859-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="c3859-127">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-127">Click Bind.</span></span>
9. <span data-ttu-id="c3859-128">В дереве выберите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="c3859-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="c3859-129">В дереве выберите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="c3859-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="c3859-130">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-130">Click Bind.</span></span>
12. <span data-ttu-id="c3859-131">В дереве разверните узел "Платежи= Проводки".</span><span class="sxs-lookup"><span data-stu-id="c3859-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="c3859-132">В дереве разверните узел "Платежи= Проводки\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="c3859-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="c3859-133">В дереве разверните узел "Платежи= Проводки\Кредитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="c3859-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="c3859-134">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="c3859-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="c3859-135">В дереве разверните узел "Проводки\vendBankAccountInTransactionCompany()".</span><span class="sxs-lookup"><span data-stu-id="c3859-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="c3859-136">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Валюта(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="c3859-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="c3859-137">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-137">Click Bind.</span></span>
19. <span data-ttu-id="c3859-138">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Код IBAN(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="c3859-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="c3859-139">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".</span><span class="sxs-lookup"><span data-stu-id="c3859-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="c3859-140">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-140">Click Bind.</span></span>
22. <span data-ttu-id="c3859-141">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="c3859-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="c3859-142">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Номер банковского счета(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="c3859-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="c3859-143">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-143">Click Bind.</span></span>
25. <span data-ttu-id="c3859-144">В дереве разверните узел "Платежи= Проводки\Кредитор\Агент".</span><span class="sxs-lookup"><span data-stu-id="c3859-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="c3859-145">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="c3859-146">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="c3859-147">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-147">Click Bind.</span></span>
29. <span data-ttu-id="c3859-148">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Код банка(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="c3859-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="c3859-149">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Код банка(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="c3859-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="c3859-150">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-150">Click Bind.</span></span>
32. <span data-ttu-id="c3859-151">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Код SWIFT(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="c3859-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="c3859-152">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Код SWIFT(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="c3859-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="c3859-153">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-153">Click Bind.</span></span>
35. <span data-ttu-id="c3859-154">В дереве выберите "Платежи= Проводки\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="c3859-155">В дереве разверните узел "Проводки\findVendTable()".</span><span class="sxs-lookup"><span data-stu-id="c3859-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="c3859-156">В дереве выберите "Transactions\findVendTable()\name()".</span><span class="sxs-lookup"><span data-stu-id="c3859-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="c3859-157">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-157">Click Bind.</span></span>
39. <span data-ttu-id="c3859-158">В дереве выберите "Платежи= Проводки\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="c3859-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="c3859-159">В дереве разверните узел "Проводки\>Связи".</span><span class="sxs-lookup"><span data-stu-id="c3859-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="c3859-160">В дереве разверните узел "Проводки\>Связи\Таблица валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="c3859-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="c3859-161">В дереве выберите "Проводки\>Связи\Таблица валюты(Currency)\Код валюты (CurrencyCodeISO)".</span><span class="sxs-lookup"><span data-stu-id="c3859-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="c3859-162">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-162">Click Bind.</span></span>
44. <span data-ttu-id="c3859-163">В дереве разверните узел "Платежи= Проводки\Дебитор".</span><span class="sxs-lookup"><span data-stu-id="c3859-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="c3859-164">В дереве разверните узел "Платежи= Проводки\Дебитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="c3859-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="c3859-165">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="c3859-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="c3859-166">В дереве выберите "Банковский счет(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="c3859-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="c3859-167">В дереве разверните узел "Банковский счет(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="c3859-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="c3859-168">В дереве выберите "Банковский счет(BankAccount)\Валюта(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="c3859-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="c3859-169">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-169">Click Bind.</span></span>
51. <span data-ttu-id="c3859-170">В дереве выберите "Банковский счет(BankAccount)\IBAN".</span><span class="sxs-lookup"><span data-stu-id="c3859-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="c3859-171">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Код IBAN(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="c3859-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="c3859-172">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-172">Click Bind.</span></span>
54. <span data-ttu-id="c3859-173">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="c3859-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="c3859-174">В дереве выберите "Банковский счет(BankAccount)\Номер банковского счета(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="c3859-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="c3859-175">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-175">Click Bind.</span></span>
57. <span data-ttu-id="c3859-176">В дереве разверните узел "Платежи= Проводки\Дебитор\Агент".</span><span class="sxs-lookup"><span data-stu-id="c3859-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="c3859-177">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="c3859-178">В дереве выберите "Банковский счет(BankAccount)\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="c3859-179">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-179">Click Bind.</span></span>
61. <span data-ttu-id="c3859-180">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Код банка(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="c3859-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="c3859-181">В дереве выберите "Банковский счет(BankAccount)\Код банка(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="c3859-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="c3859-182">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-182">Click Bind.</span></span>
64. <span data-ttu-id="c3859-183">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Код SWIFT(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="c3859-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="c3859-184">В дереве выберите "Банковский счет(BankAccount)\Код SWIFT(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="c3859-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="c3859-185">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-185">Click Bind.</span></span>
67. <span data-ttu-id="c3859-186">В дереве выберите "Платежи= Проводки\Дебитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="c3859-187">В дереве выберите "Информация о компании(Company)".</span><span class="sxs-lookup"><span data-stu-id="c3859-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="c3859-188">В дереве разверните узел "Информация о компании(Company)".</span><span class="sxs-lookup"><span data-stu-id="c3859-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="c3859-189">В дереве выберите "Информация о компании(Company)\Имя".</span><span class="sxs-lookup"><span data-stu-id="c3859-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="c3859-190">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-190">Click Bind.</span></span>
72. <span data-ttu-id="c3859-191">В дереве выберите "Платежи= Проводки\Описание".</span><span class="sxs-lookup"><span data-stu-id="c3859-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="c3859-192">В дереве выберите "Платежи= Проводки\Описание(Txt)".</span><span class="sxs-lookup"><span data-stu-id="c3859-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="c3859-193">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-193">Click Bind.</span></span>
75. <span data-ttu-id="c3859-194">В дереве выберите "Платежи= Проводки\Сквозной идентификационный код(End2EndID)".</span><span class="sxs-lookup"><span data-stu-id="c3859-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="c3859-195">В дереве выберите "Проводки\$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="c3859-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="c3859-196">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-196">Click Bind.</span></span>
78. <span data-ttu-id="c3859-197">В дереве выберите "Платежи= Проводки\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="c3859-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="c3859-198">В дереве выберите "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="c3859-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="c3859-199">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-199">Click Bind.</span></span>
81. <span data-ttu-id="c3859-200">В дереве выберите "Платежи= Проводки\Дата проводки(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="c3859-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="c3859-201">В дереве выберите "Проводки\Дата(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="c3859-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="c3859-202">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="c3859-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="c3859-203">Проверка созданного сопоставления</span><span class="sxs-lookup"><span data-stu-id="c3859-203">Validate created mapping</span></span>
1. <span data-ttu-id="c3859-204">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="c3859-204">Click Validate.</span></span>
    * <span data-ttu-id="c3859-205">Проверьте новое сопоставление, чтобы убедиться, что все привязки работают верно.</span><span class="sxs-lookup"><span data-stu-id="c3859-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="c3859-206">Щелкните стрелку, чтобы развернуть или свернуть раздел "Список ошибок".</span><span class="sxs-lookup"><span data-stu-id="c3859-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="c3859-207">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c3859-207">Click Save.</span></span>
4. <span data-ttu-id="c3859-208">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c3859-208">Close the page.</span></span>
5. <span data-ttu-id="c3859-209">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c3859-209">Close the page.</span></span>
6. <span data-ttu-id="c3859-210">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c3859-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="c3859-211">Изменение статуса текущей версии модели конфигурации</span><span class="sxs-lookup"><span data-stu-id="c3859-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="c3859-212">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="c3859-212">Click Change status.</span></span>
    * <span data-ttu-id="c3859-213">Измените статус созданной конфигурации модели с "Черновик" на "Завершено", чтобы сделать ее доступной для дизайна формата платежа.</span><span class="sxs-lookup"><span data-stu-id="c3859-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="c3859-214">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="c3859-214">Click Complete.</span></span>
    * <span data-ttu-id="c3859-215">Выберите "Завершить".</span><span class="sxs-lookup"><span data-stu-id="c3859-215">Select Complete.</span></span>  
3. <span data-ttu-id="c3859-216">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c3859-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c3859-217">Например, "версия 1".</span><span class="sxs-lookup"><span data-stu-id="c3859-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="c3859-218">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c3859-218">Click OK.</span></span>
5. <span data-ttu-id="c3859-219">Выберите завершенную версию текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c3859-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="c3859-220">Обратите внимание, что созданная конфигурация сохраняется как завершенная версия 1.</span><span class="sxs-lookup"><span data-stu-id="c3859-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]