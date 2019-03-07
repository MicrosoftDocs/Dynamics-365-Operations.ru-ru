---
title: Электронная отчетность Сопоставление модели данных с выбранными источникам данных
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может сопоставить модель данных электронной отчетности с выбранными источниками данных Dynamics 365 for Finance and Operations, Enterprise edition.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "331560"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="3d8fd-103">Электронная отчетность Сопоставление модели данных с выбранными источникам данных</span><span class="sxs-lookup"><span data-stu-id="3d8fd-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d8fd-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может сопоставить модель данных электронной отчетности с выбранными источниками данных Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="3d8fd-105">Это сопоставление модели позднее будет использоваться в качестве источника данных в конфигурации формата, которая будет использоваться для управления документами электронных платежей.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="3d8fd-106">В этом примере вам предстоит сопоставить модель данных для компании-образца Litware, Inc. с источниками данных.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="3d8fd-107">Для выполнения этих шагов сначала необходимо выполнить шаги в процедуре "Выбор источников данных для сопоставления с моделью".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="3d8fd-108">Открытие дерева конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="3d8fd-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="3d8fd-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3d8fd-110">Щелкните "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="3d8fd-111">Выбор созданного сопоставления модели</span><span class="sxs-lookup"><span data-stu-id="3d8fd-111">Select created model mapping</span></span>
1. <span data-ttu-id="3d8fd-112">В дереве выберите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="3d8fd-113">Убедитесь, что предварительно была создана конфигурация модели "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="3d8fd-114">В противном случае остановитесь сейчас и вернитесь по завершении руководства по задаче "Создание новой конфигурации с моделью данных выбранного домена".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="3d8fd-115">Щелкните "Конструктор моделей".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-115">Click Model designer.</span></span>
3. <span data-ttu-id="3d8fd-116">Щелкните "Сопоставить модель с источником данных".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="3d8fd-117">Выберите запись "Сопоставление для кредитовых переводов".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="3d8fd-118">Сопоставление для кредитовых переводов</span><span class="sxs-lookup"><span data-stu-id="3d8fd-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="3d8fd-119">Связывание созданных источников данных с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="3d8fd-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="3d8fd-120">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-120">Click Designer.</span></span>
2. <span data-ttu-id="3d8fd-121">В дереве выберите "Дата и время обработки(ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="3d8fd-122">В дереве выберите "Дата обработки(ProcessingDateTime)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="3d8fd-123">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-123">Click Bind.</span></span>
5. <span data-ttu-id="3d8fd-124">В дереве выберите "Идентификатор платежного сообщения (MessageIdentification)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="3d8fd-125">В дереве разверните узел "Проводки".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="3d8fd-126">В дереве выберите «Проводки\Номер партии журнала(JournalNum)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="3d8fd-127">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-127">Click Bind.</span></span>
9. <span data-ttu-id="3d8fd-128">В дереве выберите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="3d8fd-129">В дереве выберите "Проводки".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="3d8fd-130">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-130">Click Bind.</span></span>
12. <span data-ttu-id="3d8fd-131">В дереве разверните узел "Платежи= Проводки".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="3d8fd-132">В дереве разверните узел "Платежи= Проводки\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="3d8fd-133">В дереве разверните узел "Платежи= Проводки\Кредитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="3d8fd-134">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="3d8fd-135">В дереве разверните узел "Проводки\vendBankAccountInTransactionCompany()".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="3d8fd-136">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Валюта(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="3d8fd-137">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-137">Click Bind.</span></span>
19. <span data-ttu-id="3d8fd-138">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Код IBAN(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="3d8fd-139">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="3d8fd-140">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-140">Click Bind.</span></span>
22. <span data-ttu-id="3d8fd-141">В дереве выберите "Платежи= Проводки\Кредитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="3d8fd-142">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Номер банковского счета(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="3d8fd-143">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-143">Click Bind.</span></span>
25. <span data-ttu-id="3d8fd-144">В дереве разверните узел "Платежи= Проводки\Кредитор\Агент".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="3d8fd-145">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="3d8fd-146">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="3d8fd-147">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-147">Click Bind.</span></span>
29. <span data-ttu-id="3d8fd-148">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Код банка(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="3d8fd-149">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Код банка(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="3d8fd-150">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-150">Click Bind.</span></span>
32. <span data-ttu-id="3d8fd-151">В дереве выберите "Платежи= Проводки\Кредитор\Агент\Код SWIFT(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="3d8fd-152">В дереве выберите "Проводки\vendBankAccountInTransactionCompany()\Код SWIFT(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="3d8fd-153">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-153">Click Bind.</span></span>
35. <span data-ttu-id="3d8fd-154">В дереве выберите "Платежи= Проводки\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="3d8fd-155">В дереве разверните узел "Проводки\findVendTable()".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="3d8fd-156">В дереве выберите "Transactions\findVendTable()\name()".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="3d8fd-157">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-157">Click Bind.</span></span>
39. <span data-ttu-id="3d8fd-158">В дереве выберите "Платежи= Проводки\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="3d8fd-159">В дереве разверните узел "Проводки\>Связи".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="3d8fd-160">В дереве разверните узел "Проводки\>Связи\Таблица валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="3d8fd-161">В дереве выберите "Проводки\>Связи\Таблица валюты(Currency)\Код валюты (CurrencyCodeISO)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="3d8fd-162">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-162">Click Bind.</span></span>
44. <span data-ttu-id="3d8fd-163">В дереве разверните узел "Платежи= Проводки\Дебитор".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="3d8fd-164">В дереве разверните узел "Платежи= Проводки\Дебитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="3d8fd-165">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Код валюты(Currency)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="3d8fd-166">В дереве выберите "Банковский счет(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="3d8fd-167">В дереве разверните узел "Банковский счет(BankAccount)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="3d8fd-168">В дереве выберите "Банковский счет(BankAccount)\Валюта(CurrencyCode)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="3d8fd-169">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-169">Click Bind.</span></span>
51. <span data-ttu-id="3d8fd-170">В дереве выберите "Банковский счет(BankAccount)\IBAN".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="3d8fd-171">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Код IBAN(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="3d8fd-172">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-172">Click Bind.</span></span>
54. <span data-ttu-id="3d8fd-173">В дереве выберите "Платежи= Проводки\Дебитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="3d8fd-174">В дереве выберите "Банковский счет(BankAccount)\Номер банковского счета(AccountNum)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="3d8fd-175">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-175">Click Bind.</span></span>
57. <span data-ttu-id="3d8fd-176">В дереве разверните узел "Платежи= Проводки\Дебитор\Агент".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="3d8fd-177">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="3d8fd-178">В дереве выберите "Банковский счет(BankAccount)\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="3d8fd-179">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-179">Click Bind.</span></span>
61. <span data-ttu-id="3d8fd-180">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Код банка(RoutingNumber)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="3d8fd-181">В дереве выберите "Банковский счет(BankAccount)\Код банка(RegistrationNum)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="3d8fd-182">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-182">Click Bind.</span></span>
64. <span data-ttu-id="3d8fd-183">В дереве выберите "Платежи= Проводки\Дебитор\Агент\Код SWIFT(SWIFT)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="3d8fd-184">В дереве выберите "Банковский счет(BankAccount)\Код SWIFT(SWIFTNo)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="3d8fd-185">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-185">Click Bind.</span></span>
67. <span data-ttu-id="3d8fd-186">В дереве выберите "Платежи= Проводки\Дебитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="3d8fd-187">В дереве выберите "Информация о компании(Company)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="3d8fd-188">В дереве разверните узел "Информация о компании(Company)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="3d8fd-189">В дереве выберите "Информация о компании(Company)\Имя".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="3d8fd-190">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-190">Click Bind.</span></span>
72. <span data-ttu-id="3d8fd-191">В дереве выберите "Платежи= Проводки\Описание".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="3d8fd-192">В дереве выберите "Платежи= Проводки\Описание(Txt)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="3d8fd-193">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-193">Click Bind.</span></span>
75. <span data-ttu-id="3d8fd-194">В дереве выберите "Платежи= Проводки\Сквозной идентификационный код(End2EndID)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="3d8fd-195">В дереве выберите "Проводки\$EndToEndID".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="3d8fd-196">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-196">Click Bind.</span></span>
78. <span data-ttu-id="3d8fd-197">В дереве выберите "Платежи= Проводки\Начальная сумма платежного поручения(InstructedAmount)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="3d8fd-198">В дереве выберите "Проводки\$Amount".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="3d8fd-199">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-199">Click Bind.</span></span>
81. <span data-ttu-id="3d8fd-200">В дереве выберите "Платежи= Проводки\Дата проводки(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="3d8fd-201">В дереве выберите "Проводки\Дата(TransDate)".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="3d8fd-202">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="3d8fd-203">Проверка созданного сопоставления</span><span class="sxs-lookup"><span data-stu-id="3d8fd-203">Validate created mapping</span></span>
1. <span data-ttu-id="3d8fd-204">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-204">Click Validate.</span></span>
    * <span data-ttu-id="3d8fd-205">Проверьте новое сопоставление, чтобы убедиться, что все привязки работают верно.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="3d8fd-206">Щелкните стрелку, чтобы развернуть или свернуть раздел "Список ошибок".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="3d8fd-207">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-207">Click Save.</span></span>
4. <span data-ttu-id="3d8fd-208">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-208">Close the page.</span></span>
5. <span data-ttu-id="3d8fd-209">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-209">Close the page.</span></span>
6. <span data-ttu-id="3d8fd-210">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="3d8fd-211">Изменение статуса текущей версии модели конфигурации</span><span class="sxs-lookup"><span data-stu-id="3d8fd-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="3d8fd-212">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-212">Click Change status.</span></span>
    * <span data-ttu-id="3d8fd-213">Измените статус созданной конфигурации модели с "Черновик" на "Завершено", чтобы сделать ее доступной для дизайна формата платежа.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="3d8fd-214">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-214">Click Complete.</span></span>
    * <span data-ttu-id="3d8fd-215">Выберите "Завершить".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-215">Select Complete.</span></span>  
3. <span data-ttu-id="3d8fd-216">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3d8fd-217">Например, "версия 1".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="3d8fd-218">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="3d8fd-218">Click OK.</span></span>
5. <span data-ttu-id="3d8fd-219">Выберите завершенную версию текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="3d8fd-220">Обратите внимание, что созданная конфигурация сохраняется как завершенная версия 1.</span><span class="sxs-lookup"><span data-stu-id="3d8fd-220">Note that the created configuration is saved as completed version 1.</span></span>  

