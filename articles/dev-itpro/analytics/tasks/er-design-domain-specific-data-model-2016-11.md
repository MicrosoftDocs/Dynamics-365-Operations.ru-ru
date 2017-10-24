--- 
title: "Разработка модели данных конкретного домена для электронной отчетности (ER)"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fadc5bc54654faf9e91e0831bdd0ff087cea3164
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="edd15-103">Разработка модели данных конкретного домена для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="edd15-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edd15-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="edd15-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="edd15-105">Эта модель данных впоследствии будет использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="edd15-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="edd15-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="edd15-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="edd15-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="edd15-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="edd15-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="edd15-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="edd15-109">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="edd15-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="edd15-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="edd15-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="edd15-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="edd15-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="edd15-112">Вам предстоит создать конфигурацию, которая содержит модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="edd15-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="edd15-113">Эта модель данных будет впоследствии использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="edd15-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="edd15-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="edd15-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="edd15-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="edd15-116">В поле "Имя" введите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="edd15-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="edd15-117">Платежи (упрощенная модель)</span><span class="sxs-lookup"><span data-stu-id="edd15-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="edd15-118">В поле "Описание" введите "Конфигурация модели платежа".</span><span class="sxs-lookup"><span data-stu-id="edd15-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="edd15-119">Конфигурация модели платежа</span><span class="sxs-lookup"><span data-stu-id="edd15-119">Payment model configuration</span></span>  
    * <span data-ttu-id="edd15-120">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="edd15-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="edd15-121">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="edd15-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="edd15-122">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="edd15-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="edd15-123">Нажмите кнопку "Создать конфигурацию", чтобы завершить задачу создания конфигурации</span><span class="sxs-lookup"><span data-stu-id="edd15-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="edd15-124">Создание модели данных</span><span class="sxs-lookup"><span data-stu-id="edd15-124">Create a data model</span></span>
    * <span data-ttu-id="edd15-125">Вы создаете новую модель данных для выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="edd15-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="edd15-126">Эта версия конфигурации будет иметь статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="edd15-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="edd15-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="edd15-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="edd15-128">Определение структуры субъекта, участвующего в процессе оплаты</span><span class="sxs-lookup"><span data-stu-id="edd15-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="edd15-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="edd15-130">В поле "Имя" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="edd15-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="edd15-131">Субъект</span><span class="sxs-lookup"><span data-stu-id="edd15-131">Party</span></span>  
3. <span data-ttu-id="edd15-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-132">Click Add.</span></span>
4. <span data-ttu-id="edd15-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="edd15-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="edd15-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="edd15-135">Наименование</span><span class="sxs-lookup"><span data-stu-id="edd15-135">Name</span></span>  
6. <span data-ttu-id="edd15-136">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="edd15-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="edd15-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-137">Click Add.</span></span>
8. <span data-ttu-id="edd15-138">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="edd15-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="edd15-139">Субъект</span><span class="sxs-lookup"><span data-stu-id="edd15-139">Party</span></span>  
9. <span data-ttu-id="edd15-140">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="edd15-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="edd15-141">Определение структуры банка для этой модели</span><span class="sxs-lookup"><span data-stu-id="edd15-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="edd15-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="edd15-143">В поле "Имя" введите "Агент".</span><span class="sxs-lookup"><span data-stu-id="edd15-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="edd15-144">Агент</span><span class="sxs-lookup"><span data-stu-id="edd15-144">Agent</span></span>  
3. <span data-ttu-id="edd15-145">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="edd15-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="edd15-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-146">Click Add.</span></span>
5. <span data-ttu-id="edd15-147">В поле "Описание" введите "Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="edd15-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="edd15-148">Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="edd15-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="edd15-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="edd15-150">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="edd15-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="edd15-151">Наименование</span><span class="sxs-lookup"><span data-stu-id="edd15-151">Name</span></span>  
8. <span data-ttu-id="edd15-152">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="edd15-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="edd15-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-153">Click Add.</span></span>
10. <span data-ttu-id="edd15-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="edd15-155">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="edd15-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="edd15-156">SWIFT-код</span><span class="sxs-lookup"><span data-stu-id="edd15-156">SWIFT</span></span>  
12. <span data-ttu-id="edd15-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-157">Click Add.</span></span>
13. <span data-ttu-id="edd15-158">В поле "Описание" введите "Банковский идентификационный код".</span><span class="sxs-lookup"><span data-stu-id="edd15-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="edd15-159">Банковский идентификационный код</span><span class="sxs-lookup"><span data-stu-id="edd15-159">Bank identification code</span></span>  
14. <span data-ttu-id="edd15-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="edd15-161">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="edd15-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="edd15-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="edd15-162">RoutingNumber</span></span>  
16. <span data-ttu-id="edd15-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-163">Click Add.</span></span>
17. <span data-ttu-id="edd15-164">В поле "Описание" введите "Внутренний номер".</span><span class="sxs-lookup"><span data-stu-id="edd15-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="edd15-165">Номер маршрута</span><span class="sxs-lookup"><span data-stu-id="edd15-165">Routing number</span></span>  
18. <span data-ttu-id="edd15-166">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="edd15-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="edd15-167">Определение структуры счета для этой модели</span><span class="sxs-lookup"><span data-stu-id="edd15-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="edd15-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="edd15-169">В поле "Имя" введите "Счет".</span><span class="sxs-lookup"><span data-stu-id="edd15-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="edd15-170">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="edd15-170">Account</span></span>  
3. <span data-ttu-id="edd15-171">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="edd15-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="edd15-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-172">Click Add.</span></span>
5. <span data-ttu-id="edd15-173">В поле "Описание" введите "Идентификация счета субъекта в финансовом учреждении (например, банк)".</span><span class="sxs-lookup"><span data-stu-id="edd15-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="edd15-174">Идентификация счета субъекта в финансовом учреждении (например, банк).</span><span class="sxs-lookup"><span data-stu-id="edd15-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="edd15-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="edd15-176">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="edd15-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="edd15-177">Валютное</span><span class="sxs-lookup"><span data-stu-id="edd15-177">Currency</span></span>  
8. <span data-ttu-id="edd15-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="edd15-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="edd15-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-179">Click Add.</span></span>
10. <span data-ttu-id="edd15-180">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="edd15-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="edd15-181">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="edd15-181">Currency code</span></span>  
11. <span data-ttu-id="edd15-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="edd15-183">В поле "Имя" введите "Номер".</span><span class="sxs-lookup"><span data-stu-id="edd15-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="edd15-184">Число</span><span class="sxs-lookup"><span data-stu-id="edd15-184">Number</span></span>  
13. <span data-ttu-id="edd15-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-185">Click Add.</span></span>
14. <span data-ttu-id="edd15-186">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="edd15-187">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="edd15-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="edd15-188">номер IBAN</span><span class="sxs-lookup"><span data-stu-id="edd15-188">IBAN</span></span>  
16. <span data-ttu-id="edd15-189">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-189">Click Add.</span></span>
17. <span data-ttu-id="edd15-190">В поле "Описание" введите "Международный номер банковского счета".</span><span class="sxs-lookup"><span data-stu-id="edd15-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="edd15-191">Международный номер банковского счета</span><span class="sxs-lookup"><span data-stu-id="edd15-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="edd15-192">Определение структуры платежного сообщения для типа платежа "кредитный перевод"</span><span class="sxs-lookup"><span data-stu-id="edd15-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="edd15-193">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="edd15-194">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="edd15-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="edd15-195">В поле "Имя" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="edd15-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="edd15-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="edd15-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="edd15-197">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-197">Click Add.</span></span>
5. <span data-ttu-id="edd15-198">В поле "Поиск" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="edd15-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="edd15-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="edd15-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="edd15-200">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="edd15-200">Click Find previous.</span></span>
7. <span data-ttu-id="edd15-201">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="edd15-202">В поле "Имя" введите "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="edd15-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="edd15-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="edd15-203">MessageIdentification</span></span>  
9. <span data-ttu-id="edd15-204">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-204">Click Add.</span></span>
10. <span data-ttu-id="edd15-205">В поле "Описание" введите "Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения".</span><span class="sxs-lookup"><span data-stu-id="edd15-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="edd15-206">Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения.</span><span class="sxs-lookup"><span data-stu-id="edd15-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="edd15-207">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="edd15-208">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="edd15-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="edd15-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="edd15-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="edd15-210">В поле "Тип элемента" выберите "Дата и время".</span><span class="sxs-lookup"><span data-stu-id="edd15-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="edd15-211">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-211">Click Add.</span></span>
15. <span data-ttu-id="edd15-212">В поле "Описание" введите "Дата и время создания платежного сообщения".</span><span class="sxs-lookup"><span data-stu-id="edd15-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="edd15-213">Дата и время создания платежного сообщения.</span><span class="sxs-lookup"><span data-stu-id="edd15-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="edd15-214">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="edd15-215">Определите структуру проводки по оплате для этой модели.</span><span class="sxs-lookup"><span data-stu-id="edd15-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="edd15-216">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="edd15-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="edd15-217">Оплаты</span><span class="sxs-lookup"><span data-stu-id="edd15-217">Payments</span></span>  
18. <span data-ttu-id="edd15-218">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="edd15-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="edd15-219">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-219">Click Add.</span></span>
20. <span data-ttu-id="edd15-220">В поле "Описание" введите "Платежные строки текущего сообщения".</span><span class="sxs-lookup"><span data-stu-id="edd15-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="edd15-221">Платежные строки текущего сообщения</span><span class="sxs-lookup"><span data-stu-id="edd15-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="edd15-222">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="edd15-223">В поле "Имя" введите "Кредитор".</span><span class="sxs-lookup"><span data-stu-id="edd15-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="edd15-224">Кредитор</span><span class="sxs-lookup"><span data-stu-id="edd15-224">Creditor</span></span>  
23. <span data-ttu-id="edd15-225">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="edd15-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="edd15-226">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-226">Click Add.</span></span>
25. <span data-ttu-id="edd15-227">В поле "Описание" введите "Субъект, которому причитается некоторая сумма денег".</span><span class="sxs-lookup"><span data-stu-id="edd15-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="edd15-228">Субъект, которому выплачивается денежная сумма.</span><span class="sxs-lookup"><span data-stu-id="edd15-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="edd15-229">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="edd15-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="edd15-230">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="edd15-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="edd15-231">Субъект</span><span class="sxs-lookup"><span data-stu-id="edd15-231">Party</span></span>  
28. <span data-ttu-id="edd15-232">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="edd15-232">Click Find next.</span></span>
29. <span data-ttu-id="edd15-233">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="edd15-233">Click OK.</span></span>
30. <span data-ttu-id="edd15-234">В поле "Поиск" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="edd15-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="edd15-235">Оплаты</span><span class="sxs-lookup"><span data-stu-id="edd15-235">Payments</span></span>  
31. <span data-ttu-id="edd15-236">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="edd15-236">Click Find next.</span></span>
32. <span data-ttu-id="edd15-237">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="edd15-238">В поле "Имя" введите "Дебитор".</span><span class="sxs-lookup"><span data-stu-id="edd15-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="edd15-239">Дебитор</span><span class="sxs-lookup"><span data-stu-id="edd15-239">Debtor</span></span>  
34. <span data-ttu-id="edd15-240">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-240">Click Add.</span></span>
35. <span data-ttu-id="edd15-241">В поле "Описание" введите "Субъект, который должен некоторую сумму денег (конечному) кредитору".</span><span class="sxs-lookup"><span data-stu-id="edd15-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="edd15-242">Субъект, должный денежную сумму (основному) кредитору.</span><span class="sxs-lookup"><span data-stu-id="edd15-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="edd15-243">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="edd15-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="edd15-244">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="edd15-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="edd15-245">Субъект</span><span class="sxs-lookup"><span data-stu-id="edd15-245">Party</span></span>  
38. <span data-ttu-id="edd15-246">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="edd15-246">Click Find next.</span></span>
39. <span data-ttu-id="edd15-247">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="edd15-247">Click OK.</span></span>
40. <span data-ttu-id="edd15-248">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="edd15-248">Click Find next.</span></span>
41. <span data-ttu-id="edd15-249">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="edd15-250">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="edd15-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="edd15-251">описание</span><span class="sxs-lookup"><span data-stu-id="edd15-251">Description</span></span>  
43. <span data-ttu-id="edd15-252">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="edd15-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="edd15-253">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-253">Click Add.</span></span>
45. <span data-ttu-id="edd15-254">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="edd15-255">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="edd15-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="edd15-256">Валютное</span><span class="sxs-lookup"><span data-stu-id="edd15-256">Currency</span></span>  
47. <span data-ttu-id="edd15-257">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-257">Click Add.</span></span>
48. <span data-ttu-id="edd15-258">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="edd15-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="edd15-259">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="edd15-259">Currency code</span></span>  
49. <span data-ttu-id="edd15-260">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="edd15-261">В поле "Имя" введите "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="edd15-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="edd15-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="edd15-262">TransactionDate</span></span>  
51. <span data-ttu-id="edd15-263">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="edd15-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="edd15-264">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-264">Click Add.</span></span>
53. <span data-ttu-id="edd15-265">В поле "Описание" введите "Дата проводки".</span><span class="sxs-lookup"><span data-stu-id="edd15-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="edd15-266">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="edd15-266">Transaction date</span></span>  
54. <span data-ttu-id="edd15-267">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="edd15-268">В поле "Имя" введите "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="edd15-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="edd15-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="edd15-269">InstructedAmount</span></span>  
56. <span data-ttu-id="edd15-270">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="edd15-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="edd15-271">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-271">Click Add.</span></span>
58. <span data-ttu-id="edd15-272">В поле "Описание" введите "Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="edd15-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="edd15-273">Сумма должна быть выражена в валюте, указанной инициирующим субъектом".</span><span class="sxs-lookup"><span data-stu-id="edd15-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="edd15-274">Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="edd15-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="edd15-275">Сумма должна быть выражена в валюте, указанной инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="edd15-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="edd15-276">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="edd15-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="edd15-277">В поле "Имя" введите "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="edd15-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="edd15-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="edd15-278">End2EndID</span></span>  
61. <span data-ttu-id="edd15-279">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="edd15-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="edd15-280">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="edd15-280">Click Add.</span></span>
63. <span data-ttu-id="edd15-281">В поле "Описание" введите "Уникальный код, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="edd15-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="edd15-282">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа".</span><span class="sxs-lookup"><span data-stu-id="edd15-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="edd15-283">Уникальный идентификатор, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="edd15-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="edd15-284">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="edd15-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="edd15-285">В поле "Имя" введите "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="edd15-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="edd15-286">Имя PaymentModel соответствует предопределенным интерфейсам форм платежей.</span><span class="sxs-lookup"><span data-stu-id="edd15-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="edd15-287">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="edd15-287">Click Save.</span></span>
66. <span data-ttu-id="edd15-288">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="edd15-288">Close the page.</span></span>

