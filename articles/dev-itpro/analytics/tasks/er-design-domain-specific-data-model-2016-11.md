--- 
title: "Проектирование моделей данных для конкретных доменов"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.openlocfilehash: c59bdea789c4eafd2443a5d1cf802768259858c6
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="design-domain-specific-data-models"></a><span data-ttu-id="35224-103">Проектирование моделей данных для конкретных доменов</span><span class="sxs-lookup"><span data-stu-id="35224-103">Design domain-specific data models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35224-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="35224-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="35224-105">Эта модель данных впоследствии будет использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="35224-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="35224-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="35224-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="35224-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="35224-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="35224-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="35224-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="35224-109">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="35224-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="35224-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="35224-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="35224-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="35224-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="35224-112">Вам предстоит создать конфигурацию, которая содержит модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="35224-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="35224-113">Эта модель данных будет впоследствии использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="35224-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="35224-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="35224-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="35224-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="35224-116">В поле "Имя" введите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="35224-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="35224-117">Платежи (упрощенная модель)</span><span class="sxs-lookup"><span data-stu-id="35224-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="35224-118">В поле "Описание" введите "Конфигурация модели платежа".</span><span class="sxs-lookup"><span data-stu-id="35224-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="35224-119">Конфигурация модели платежа</span><span class="sxs-lookup"><span data-stu-id="35224-119">Payment model configuration</span></span>  
    * <span data-ttu-id="35224-120">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="35224-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="35224-121">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="35224-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="35224-122">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="35224-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="35224-123">Нажмите кнопку "Создать конфигурацию", чтобы завершить задачу создания конфигурации</span><span class="sxs-lookup"><span data-stu-id="35224-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="35224-124">Создание модели данных</span><span class="sxs-lookup"><span data-stu-id="35224-124">Create a data model</span></span>
    * <span data-ttu-id="35224-125">Вы создаете новую модель данных для выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="35224-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="35224-126">Эта версия конфигурации будет иметь статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="35224-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="35224-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="35224-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="35224-128">Определение структуры субъекта, участвующего в процессе оплаты</span><span class="sxs-lookup"><span data-stu-id="35224-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="35224-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="35224-130">В поле "Имя" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="35224-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="35224-131">Субъект</span><span class="sxs-lookup"><span data-stu-id="35224-131">Party</span></span>  
3. <span data-ttu-id="35224-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-132">Click Add.</span></span>
4. <span data-ttu-id="35224-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="35224-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="35224-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="35224-135">Наименование</span><span class="sxs-lookup"><span data-stu-id="35224-135">Name</span></span>  
6. <span data-ttu-id="35224-136">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="35224-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="35224-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-137">Click Add.</span></span>
8. <span data-ttu-id="35224-138">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="35224-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="35224-139">Субъект</span><span class="sxs-lookup"><span data-stu-id="35224-139">Party</span></span>  
9. <span data-ttu-id="35224-140">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="35224-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="35224-141">Определение структуры банка для этой модели</span><span class="sxs-lookup"><span data-stu-id="35224-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="35224-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="35224-143">В поле "Имя" введите "Агент".</span><span class="sxs-lookup"><span data-stu-id="35224-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="35224-144">Агент</span><span class="sxs-lookup"><span data-stu-id="35224-144">Agent</span></span>  
3. <span data-ttu-id="35224-145">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="35224-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="35224-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-146">Click Add.</span></span>
5. <span data-ttu-id="35224-147">В поле "Описание" введите "Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="35224-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="35224-148">Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="35224-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="35224-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="35224-150">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="35224-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="35224-151">Наименование</span><span class="sxs-lookup"><span data-stu-id="35224-151">Name</span></span>  
8. <span data-ttu-id="35224-152">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="35224-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="35224-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-153">Click Add.</span></span>
10. <span data-ttu-id="35224-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="35224-155">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="35224-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="35224-156">SWIFT-код</span><span class="sxs-lookup"><span data-stu-id="35224-156">SWIFT</span></span>  
12. <span data-ttu-id="35224-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-157">Click Add.</span></span>
13. <span data-ttu-id="35224-158">В поле "Описание" введите "Банковский идентификационный код".</span><span class="sxs-lookup"><span data-stu-id="35224-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="35224-159">Банковский идентификационный код</span><span class="sxs-lookup"><span data-stu-id="35224-159">Bank identification code</span></span>  
14. <span data-ttu-id="35224-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="35224-161">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="35224-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="35224-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="35224-162">RoutingNumber</span></span>  
16. <span data-ttu-id="35224-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-163">Click Add.</span></span>
17. <span data-ttu-id="35224-164">В поле "Описание" введите "Внутренний номер".</span><span class="sxs-lookup"><span data-stu-id="35224-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="35224-165">Номер маршрута</span><span class="sxs-lookup"><span data-stu-id="35224-165">Routing number</span></span>  
18. <span data-ttu-id="35224-166">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="35224-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="35224-167">Определение структуры счета для этой модели</span><span class="sxs-lookup"><span data-stu-id="35224-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="35224-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="35224-169">В поле "Имя" введите "Счет".</span><span class="sxs-lookup"><span data-stu-id="35224-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="35224-170">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="35224-170">Account</span></span>  
3. <span data-ttu-id="35224-171">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="35224-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="35224-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-172">Click Add.</span></span>
5. <span data-ttu-id="35224-173">В поле "Описание" введите "Идентификация счета субъекта в финансовом учреждении (например, банк)".</span><span class="sxs-lookup"><span data-stu-id="35224-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="35224-174">Идентификация счета субъекта в финансовом учреждении (например, банк).</span><span class="sxs-lookup"><span data-stu-id="35224-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="35224-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="35224-176">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="35224-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="35224-177">Валютное</span><span class="sxs-lookup"><span data-stu-id="35224-177">Currency</span></span>  
8. <span data-ttu-id="35224-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="35224-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="35224-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-179">Click Add.</span></span>
10. <span data-ttu-id="35224-180">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="35224-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="35224-181">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="35224-181">Currency code</span></span>  
11. <span data-ttu-id="35224-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="35224-183">В поле "Имя" введите "Номер".</span><span class="sxs-lookup"><span data-stu-id="35224-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="35224-184">Число</span><span class="sxs-lookup"><span data-stu-id="35224-184">Number</span></span>  
13. <span data-ttu-id="35224-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-185">Click Add.</span></span>
14. <span data-ttu-id="35224-186">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="35224-187">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="35224-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="35224-188">номер IBAN</span><span class="sxs-lookup"><span data-stu-id="35224-188">IBAN</span></span>  
16. <span data-ttu-id="35224-189">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-189">Click Add.</span></span>
17. <span data-ttu-id="35224-190">В поле "Описание" введите "Международный номер банковского счета".</span><span class="sxs-lookup"><span data-stu-id="35224-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="35224-191">Международный номер банковского счета</span><span class="sxs-lookup"><span data-stu-id="35224-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="35224-192">Определение структуры платежного сообщения для типа платежа "кредитный перевод"</span><span class="sxs-lookup"><span data-stu-id="35224-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="35224-193">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="35224-194">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="35224-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="35224-195">В поле "Имя" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="35224-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="35224-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="35224-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="35224-197">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-197">Click Add.</span></span>
5. <span data-ttu-id="35224-198">В поле "Поиск" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="35224-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="35224-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="35224-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="35224-200">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="35224-200">Click Find previous.</span></span>
7. <span data-ttu-id="35224-201">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="35224-202">В поле "Имя" введите "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="35224-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="35224-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="35224-203">MessageIdentification</span></span>  
9. <span data-ttu-id="35224-204">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-204">Click Add.</span></span>
10. <span data-ttu-id="35224-205">В поле "Описание" введите "Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения".</span><span class="sxs-lookup"><span data-stu-id="35224-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="35224-206">Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения.</span><span class="sxs-lookup"><span data-stu-id="35224-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="35224-207">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="35224-208">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="35224-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="35224-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="35224-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="35224-210">В поле "Тип элемента" выберите "Дата и время".</span><span class="sxs-lookup"><span data-stu-id="35224-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="35224-211">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-211">Click Add.</span></span>
15. <span data-ttu-id="35224-212">В поле "Описание" введите "Дата и время создания платежного сообщения".</span><span class="sxs-lookup"><span data-stu-id="35224-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="35224-213">Дата и время создания платежного сообщения.</span><span class="sxs-lookup"><span data-stu-id="35224-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="35224-214">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="35224-215">Определите структуру проводки по оплате для этой модели.</span><span class="sxs-lookup"><span data-stu-id="35224-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="35224-216">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="35224-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="35224-217">Оплаты</span><span class="sxs-lookup"><span data-stu-id="35224-217">Payments</span></span>  
18. <span data-ttu-id="35224-218">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="35224-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="35224-219">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-219">Click Add.</span></span>
20. <span data-ttu-id="35224-220">В поле "Описание" введите "Платежные строки текущего сообщения".</span><span class="sxs-lookup"><span data-stu-id="35224-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="35224-221">Платежные строки текущего сообщения</span><span class="sxs-lookup"><span data-stu-id="35224-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="35224-222">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="35224-223">В поле "Имя" введите "Кредитор".</span><span class="sxs-lookup"><span data-stu-id="35224-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="35224-224">Кредитор</span><span class="sxs-lookup"><span data-stu-id="35224-224">Creditor</span></span>  
23. <span data-ttu-id="35224-225">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="35224-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="35224-226">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-226">Click Add.</span></span>
25. <span data-ttu-id="35224-227">В поле "Описание" введите "Субъект, которому причитается некоторая сумма денег".</span><span class="sxs-lookup"><span data-stu-id="35224-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="35224-228">Субъект, которому выплачивается денежная сумма.</span><span class="sxs-lookup"><span data-stu-id="35224-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="35224-229">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="35224-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="35224-230">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="35224-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="35224-231">Субъект</span><span class="sxs-lookup"><span data-stu-id="35224-231">Party</span></span>  
28. <span data-ttu-id="35224-232">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="35224-232">Click Find next.</span></span>
29. <span data-ttu-id="35224-233">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="35224-233">Click OK.</span></span>
30. <span data-ttu-id="35224-234">В поле "Поиск" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="35224-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="35224-235">Оплаты</span><span class="sxs-lookup"><span data-stu-id="35224-235">Payments</span></span>  
31. <span data-ttu-id="35224-236">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="35224-236">Click Find next.</span></span>
32. <span data-ttu-id="35224-237">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="35224-238">В поле "Имя" введите "Дебитор".</span><span class="sxs-lookup"><span data-stu-id="35224-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="35224-239">Дебитор</span><span class="sxs-lookup"><span data-stu-id="35224-239">Debtor</span></span>  
34. <span data-ttu-id="35224-240">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-240">Click Add.</span></span>
35. <span data-ttu-id="35224-241">В поле "Описание" введите "Субъект, который должен некоторую сумму денег (конечному) кредитору".</span><span class="sxs-lookup"><span data-stu-id="35224-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="35224-242">Субъект, должный денежную сумму (основному) кредитору.</span><span class="sxs-lookup"><span data-stu-id="35224-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="35224-243">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="35224-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="35224-244">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="35224-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="35224-245">Субъект</span><span class="sxs-lookup"><span data-stu-id="35224-245">Party</span></span>  
38. <span data-ttu-id="35224-246">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="35224-246">Click Find next.</span></span>
39. <span data-ttu-id="35224-247">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="35224-247">Click OK.</span></span>
40. <span data-ttu-id="35224-248">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="35224-248">Click Find next.</span></span>
41. <span data-ttu-id="35224-249">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="35224-250">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="35224-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="35224-251">описание</span><span class="sxs-lookup"><span data-stu-id="35224-251">Description</span></span>  
43. <span data-ttu-id="35224-252">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="35224-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="35224-253">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-253">Click Add.</span></span>
45. <span data-ttu-id="35224-254">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="35224-255">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="35224-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="35224-256">Валютное</span><span class="sxs-lookup"><span data-stu-id="35224-256">Currency</span></span>  
47. <span data-ttu-id="35224-257">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-257">Click Add.</span></span>
48. <span data-ttu-id="35224-258">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="35224-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="35224-259">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="35224-259">Currency code</span></span>  
49. <span data-ttu-id="35224-260">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="35224-261">В поле "Имя" введите "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="35224-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="35224-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="35224-262">TransactionDate</span></span>  
51. <span data-ttu-id="35224-263">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="35224-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="35224-264">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-264">Click Add.</span></span>
53. <span data-ttu-id="35224-265">В поле "Описание" введите "Дата проводки".</span><span class="sxs-lookup"><span data-stu-id="35224-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="35224-266">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="35224-266">Transaction date</span></span>  
54. <span data-ttu-id="35224-267">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="35224-268">В поле "Имя" введите "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="35224-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="35224-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="35224-269">InstructedAmount</span></span>  
56. <span data-ttu-id="35224-270">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="35224-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="35224-271">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-271">Click Add.</span></span>
58. <span data-ttu-id="35224-272">В поле "Описание" введите "Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="35224-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="35224-273">Сумма должна быть выражена в валюте, указанной инициирующим субъектом".</span><span class="sxs-lookup"><span data-stu-id="35224-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="35224-274">Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="35224-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="35224-275">Сумма должна быть выражена в валюте, указанной инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="35224-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="35224-276">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="35224-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="35224-277">В поле "Имя" введите "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="35224-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="35224-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="35224-278">End2EndID</span></span>  
61. <span data-ttu-id="35224-279">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="35224-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="35224-280">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="35224-280">Click Add.</span></span>
63. <span data-ttu-id="35224-281">В поле "Описание" введите "Уникальный код, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="35224-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="35224-282">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа".</span><span class="sxs-lookup"><span data-stu-id="35224-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="35224-283">Уникальный идентификатор, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="35224-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="35224-284">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="35224-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="35224-285">В поле "Имя" введите "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="35224-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="35224-286">Имя PaymentModel соответствует предопределенным интерфейсам форм платежей.</span><span class="sxs-lookup"><span data-stu-id="35224-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="35224-287">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="35224-287">Click Save.</span></span>
66. <span data-ttu-id="35224-288">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="35224-288">Close the page.</span></span>


