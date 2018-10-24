--- 
title: "Электронная отчетность Проектирование моделей данных для конкретных доменов"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="e341b-103">Электронная отчетность Проектирование моделей данных для конкретных доменов</span><span class="sxs-lookup"><span data-stu-id="e341b-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e341b-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="e341b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e341b-105">Эта модель данных впоследствии будет использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="e341b-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="e341b-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="e341b-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="e341b-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="e341b-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="e341b-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="e341b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e341b-109">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e341b-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="e341b-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="e341b-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="e341b-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="e341b-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="e341b-112">Вам предстоит создать конфигурацию, которая содержит модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="e341b-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e341b-113">Эта модель данных будет впоследствии использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="e341b-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="e341b-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="e341b-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="e341b-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e341b-116">В поле "Имя" введите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="e341b-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="e341b-117">Платежи (упрощенная модель)</span><span class="sxs-lookup"><span data-stu-id="e341b-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="e341b-118">В поле "Описание" введите "Конфигурация модели платежа".</span><span class="sxs-lookup"><span data-stu-id="e341b-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="e341b-119">Конфигурация модели платежа</span><span class="sxs-lookup"><span data-stu-id="e341b-119">Payment model configuration</span></span>  
    * <span data-ttu-id="e341b-120">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="e341b-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e341b-121">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e341b-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e341b-122">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="e341b-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="e341b-123">Нажмите кнопку "Создать конфигурацию", чтобы завершить задачу создания конфигурации</span><span class="sxs-lookup"><span data-stu-id="e341b-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="e341b-124">Создание модели данных</span><span class="sxs-lookup"><span data-stu-id="e341b-124">Create a data model</span></span>
    * <span data-ttu-id="e341b-125">Вы создаете новую модель данных для выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e341b-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="e341b-126">Эта версия конфигурации будет иметь статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="e341b-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="e341b-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="e341b-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="e341b-128">Определение структуры субъекта, участвующего в процессе оплаты</span><span class="sxs-lookup"><span data-stu-id="e341b-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="e341b-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e341b-130">В поле "Имя" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="e341b-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="e341b-131">Субъект</span><span class="sxs-lookup"><span data-stu-id="e341b-131">Party</span></span>  
3. <span data-ttu-id="e341b-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-132">Click Add.</span></span>
4. <span data-ttu-id="e341b-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e341b-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="e341b-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="e341b-135">Наименование</span><span class="sxs-lookup"><span data-stu-id="e341b-135">Name</span></span>  
6. <span data-ttu-id="e341b-136">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e341b-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="e341b-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-137">Click Add.</span></span>
8. <span data-ttu-id="e341b-138">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="e341b-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e341b-139">Субъект</span><span class="sxs-lookup"><span data-stu-id="e341b-139">Party</span></span>  
9. <span data-ttu-id="e341b-140">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="e341b-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="e341b-141">Определение структуры банка для этой модели</span><span class="sxs-lookup"><span data-stu-id="e341b-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="e341b-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e341b-143">В поле "Имя" введите "Агент".</span><span class="sxs-lookup"><span data-stu-id="e341b-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="e341b-144">Агент</span><span class="sxs-lookup"><span data-stu-id="e341b-144">Agent</span></span>  
3. <span data-ttu-id="e341b-145">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="e341b-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e341b-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-146">Click Add.</span></span>
5. <span data-ttu-id="e341b-147">В поле "Описание" введите "Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="e341b-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="e341b-148">Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="e341b-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="e341b-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e341b-150">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="e341b-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="e341b-151">Наименование</span><span class="sxs-lookup"><span data-stu-id="e341b-151">Name</span></span>  
8. <span data-ttu-id="e341b-152">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e341b-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e341b-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-153">Click Add.</span></span>
10. <span data-ttu-id="e341b-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="e341b-155">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="e341b-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="e341b-156">SWIFT-код</span><span class="sxs-lookup"><span data-stu-id="e341b-156">SWIFT</span></span>  
12. <span data-ttu-id="e341b-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-157">Click Add.</span></span>
13. <span data-ttu-id="e341b-158">В поле "Описание" введите "Банковский идентификационный код".</span><span class="sxs-lookup"><span data-stu-id="e341b-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="e341b-159">Банковский идентификационный код</span><span class="sxs-lookup"><span data-stu-id="e341b-159">Bank identification code</span></span>  
14. <span data-ttu-id="e341b-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e341b-161">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="e341b-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="e341b-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="e341b-162">RoutingNumber</span></span>  
16. <span data-ttu-id="e341b-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-163">Click Add.</span></span>
17. <span data-ttu-id="e341b-164">В поле "Описание" введите "Внутренний номер".</span><span class="sxs-lookup"><span data-stu-id="e341b-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="e341b-165">Номер маршрута</span><span class="sxs-lookup"><span data-stu-id="e341b-165">Routing number</span></span>  
18. <span data-ttu-id="e341b-166">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="e341b-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="e341b-167">Определение структуры счета для этой модели</span><span class="sxs-lookup"><span data-stu-id="e341b-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="e341b-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e341b-169">В поле "Имя" введите "Счет".</span><span class="sxs-lookup"><span data-stu-id="e341b-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="e341b-170">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="e341b-170">Account</span></span>  
3. <span data-ttu-id="e341b-171">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="e341b-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e341b-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-172">Click Add.</span></span>
5. <span data-ttu-id="e341b-173">В поле "Описание" введите "Идентификация счета субъекта в финансовом учреждении (например, банк)".</span><span class="sxs-lookup"><span data-stu-id="e341b-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="e341b-174">Идентификация счета субъекта в финансовом учреждении (например, банк).</span><span class="sxs-lookup"><span data-stu-id="e341b-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="e341b-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e341b-176">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="e341b-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="e341b-177">Валютное</span><span class="sxs-lookup"><span data-stu-id="e341b-177">Currency</span></span>  
8. <span data-ttu-id="e341b-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e341b-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e341b-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-179">Click Add.</span></span>
10. <span data-ttu-id="e341b-180">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="e341b-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="e341b-181">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="e341b-181">Currency code</span></span>  
11. <span data-ttu-id="e341b-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e341b-183">В поле "Имя" введите "Номер".</span><span class="sxs-lookup"><span data-stu-id="e341b-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="e341b-184">Число</span><span class="sxs-lookup"><span data-stu-id="e341b-184">Number</span></span>  
13. <span data-ttu-id="e341b-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-185">Click Add.</span></span>
14. <span data-ttu-id="e341b-186">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e341b-187">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="e341b-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="e341b-188">номер IBAN</span><span class="sxs-lookup"><span data-stu-id="e341b-188">IBAN</span></span>  
16. <span data-ttu-id="e341b-189">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-189">Click Add.</span></span>
17. <span data-ttu-id="e341b-190">В поле "Описание" введите "Международный номер банковского счета".</span><span class="sxs-lookup"><span data-stu-id="e341b-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="e341b-191">Международный номер банковского счета</span><span class="sxs-lookup"><span data-stu-id="e341b-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="e341b-192">Определение структуры платежного сообщения для типа платежа "кредитный перевод"</span><span class="sxs-lookup"><span data-stu-id="e341b-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="e341b-193">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e341b-194">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="e341b-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="e341b-195">В поле "Имя" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="e341b-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e341b-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e341b-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="e341b-197">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-197">Click Add.</span></span>
5. <span data-ttu-id="e341b-198">В поле "Поиск" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="e341b-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e341b-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e341b-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="e341b-200">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="e341b-200">Click Find previous.</span></span>
7. <span data-ttu-id="e341b-201">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e341b-202">В поле "Имя" введите "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="e341b-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="e341b-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="e341b-203">MessageIdentification</span></span>  
9. <span data-ttu-id="e341b-204">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-204">Click Add.</span></span>
10. <span data-ttu-id="e341b-205">В поле "Описание" введите "Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения".</span><span class="sxs-lookup"><span data-stu-id="e341b-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="e341b-206">Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения.</span><span class="sxs-lookup"><span data-stu-id="e341b-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="e341b-207">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e341b-208">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="e341b-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="e341b-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="e341b-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="e341b-210">В поле "Тип элемента" выберите "Дата и время".</span><span class="sxs-lookup"><span data-stu-id="e341b-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="e341b-211">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-211">Click Add.</span></span>
15. <span data-ttu-id="e341b-212">В поле "Описание" введите "Дата и время создания платежного сообщения".</span><span class="sxs-lookup"><span data-stu-id="e341b-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="e341b-213">Дата и время создания платежного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e341b-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="e341b-214">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="e341b-215">Определите структуру проводки по оплате для этой модели.</span><span class="sxs-lookup"><span data-stu-id="e341b-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="e341b-216">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="e341b-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="e341b-217">Оплаты</span><span class="sxs-lookup"><span data-stu-id="e341b-217">Payments</span></span>  
18. <span data-ttu-id="e341b-218">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="e341b-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="e341b-219">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-219">Click Add.</span></span>
20. <span data-ttu-id="e341b-220">В поле "Описание" введите "Платежные строки текущего сообщения".</span><span class="sxs-lookup"><span data-stu-id="e341b-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="e341b-221">Платежные строки текущего сообщения</span><span class="sxs-lookup"><span data-stu-id="e341b-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="e341b-222">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e341b-223">В поле "Имя" введите "Кредитор".</span><span class="sxs-lookup"><span data-stu-id="e341b-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="e341b-224">Кредитор</span><span class="sxs-lookup"><span data-stu-id="e341b-224">Creditor</span></span>  
23. <span data-ttu-id="e341b-225">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="e341b-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="e341b-226">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-226">Click Add.</span></span>
25. <span data-ttu-id="e341b-227">В поле "Описание" введите "Субъект, которому причитается некоторая сумма денег".</span><span class="sxs-lookup"><span data-stu-id="e341b-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="e341b-228">Субъект, которому выплачивается денежная сумма.</span><span class="sxs-lookup"><span data-stu-id="e341b-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="e341b-229">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="e341b-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="e341b-230">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="e341b-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e341b-231">Субъект</span><span class="sxs-lookup"><span data-stu-id="e341b-231">Party</span></span>  
28. <span data-ttu-id="e341b-232">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="e341b-232">Click Find next.</span></span>
29. <span data-ttu-id="e341b-233">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e341b-233">Click OK.</span></span>
30. <span data-ttu-id="e341b-234">В поле "Поиск" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="e341b-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="e341b-235">Оплаты</span><span class="sxs-lookup"><span data-stu-id="e341b-235">Payments</span></span>  
31. <span data-ttu-id="e341b-236">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="e341b-236">Click Find next.</span></span>
32. <span data-ttu-id="e341b-237">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="e341b-238">В поле "Имя" введите "Дебитор".</span><span class="sxs-lookup"><span data-stu-id="e341b-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="e341b-239">Дебитор</span><span class="sxs-lookup"><span data-stu-id="e341b-239">Debtor</span></span>  
34. <span data-ttu-id="e341b-240">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-240">Click Add.</span></span>
35. <span data-ttu-id="e341b-241">В поле "Описание" введите "Субъект, который должен некоторую сумму денег (конечному) кредитору".</span><span class="sxs-lookup"><span data-stu-id="e341b-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="e341b-242">Субъект, должный денежную сумму (основному) кредитору.</span><span class="sxs-lookup"><span data-stu-id="e341b-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="e341b-243">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="e341b-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="e341b-244">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="e341b-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="e341b-245">Субъект</span><span class="sxs-lookup"><span data-stu-id="e341b-245">Party</span></span>  
38. <span data-ttu-id="e341b-246">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="e341b-246">Click Find next.</span></span>
39. <span data-ttu-id="e341b-247">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e341b-247">Click OK.</span></span>
40. <span data-ttu-id="e341b-248">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="e341b-248">Click Find next.</span></span>
41. <span data-ttu-id="e341b-249">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="e341b-250">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="e341b-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="e341b-251">описание</span><span class="sxs-lookup"><span data-stu-id="e341b-251">Description</span></span>  
43. <span data-ttu-id="e341b-252">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e341b-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="e341b-253">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-253">Click Add.</span></span>
45. <span data-ttu-id="e341b-254">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="e341b-255">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="e341b-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="e341b-256">Валютное</span><span class="sxs-lookup"><span data-stu-id="e341b-256">Currency</span></span>  
47. <span data-ttu-id="e341b-257">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-257">Click Add.</span></span>
48. <span data-ttu-id="e341b-258">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="e341b-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="e341b-259">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="e341b-259">Currency code</span></span>  
49. <span data-ttu-id="e341b-260">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="e341b-261">В поле "Имя" введите "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="e341b-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="e341b-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="e341b-262">TransactionDate</span></span>  
51. <span data-ttu-id="e341b-263">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="e341b-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="e341b-264">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-264">Click Add.</span></span>
53. <span data-ttu-id="e341b-265">В поле "Описание" введите "Дата проводки".</span><span class="sxs-lookup"><span data-stu-id="e341b-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="e341b-266">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="e341b-266">Transaction date</span></span>  
54. <span data-ttu-id="e341b-267">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="e341b-268">В поле "Имя" введите "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="e341b-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="e341b-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="e341b-269">InstructedAmount</span></span>  
56. <span data-ttu-id="e341b-270">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="e341b-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="e341b-271">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-271">Click Add.</span></span>
58. <span data-ttu-id="e341b-272">В поле "Описание" введите "Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="e341b-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e341b-273">Сумма должна быть выражена в валюте, указанной инициирующим субъектом".</span><span class="sxs-lookup"><span data-stu-id="e341b-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="e341b-274">Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="e341b-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e341b-275">Сумма должна быть выражена в валюте, указанной инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="e341b-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="e341b-276">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e341b-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="e341b-277">В поле "Имя" введите "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="e341b-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="e341b-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="e341b-278">End2EndID</span></span>  
61. <span data-ttu-id="e341b-279">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="e341b-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="e341b-280">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="e341b-280">Click Add.</span></span>
63. <span data-ttu-id="e341b-281">В поле "Описание" введите "Уникальный код, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="e341b-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="e341b-282">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа".</span><span class="sxs-lookup"><span data-stu-id="e341b-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="e341b-283">Уникальный идентификатор, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="e341b-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="e341b-284">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="e341b-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="e341b-285">В поле "Имя" введите "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="e341b-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="e341b-286">Имя PaymentModel соответствует предопределенным интерфейсам форм платежей.</span><span class="sxs-lookup"><span data-stu-id="e341b-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="e341b-287">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e341b-287">Click Save.</span></span>
66. <span data-ttu-id="e341b-288">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e341b-288">Close the page.</span></span>


