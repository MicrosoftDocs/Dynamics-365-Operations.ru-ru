---
title: Электронная отчетность Проектирование моделей данных для конкретных доменов
description: В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d66cc69da08478ceb931fab594da51bafcacc38
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185091"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="5da3c-103">Электронная отчетность Проектирование моделей данных для конкретных доменов</span><span class="sxs-lookup"><span data-stu-id="5da3c-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5da3c-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="5da3c-105">Эта модель данных впоследствии будет использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="5da3c-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="5da3c-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="5da3c-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="5da3c-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="5da3c-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="5da3c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="5da3c-109">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5da3c-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="5da3c-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="5da3c-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="5da3c-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="5da3c-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="5da3c-112">Вам предстоит создать конфигурацию, которая содержит модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="5da3c-113">Эта модель данных будет впоследствии использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="5da3c-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="5da3c-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="5da3c-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="5da3c-116">В поле "Имя" введите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="5da3c-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="5da3c-117">Платежи (упрощенная модель)</span><span class="sxs-lookup"><span data-stu-id="5da3c-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="5da3c-118">В поле "Описание" введите "Конфигурация модели платежа".</span><span class="sxs-lookup"><span data-stu-id="5da3c-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="5da3c-119">Конфигурация модели платежа</span><span class="sxs-lookup"><span data-stu-id="5da3c-119">Payment model configuration</span></span>  
    * <span data-ttu-id="5da3c-120">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="5da3c-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5da3c-121">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5da3c-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5da3c-122">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="5da3c-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="5da3c-123">Нажмите кнопку "Создать конфигурацию", чтобы завершить задачу создания конфигурации</span><span class="sxs-lookup"><span data-stu-id="5da3c-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="5da3c-124">Создание модели данных</span><span class="sxs-lookup"><span data-stu-id="5da3c-124">Create a data model</span></span>
    * <span data-ttu-id="5da3c-125">Вы создаете новую модель данных для выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5da3c-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="5da3c-126">Эта версия конфигурации будет иметь статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="5da3c-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="5da3c-127">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="5da3c-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="5da3c-128">Определение структуры субъекта, участвующего в процессе оплаты</span><span class="sxs-lookup"><span data-stu-id="5da3c-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="5da3c-129">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5da3c-130">В поле "Имя" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="5da3c-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="5da3c-131">Субъект</span><span class="sxs-lookup"><span data-stu-id="5da3c-131">Party</span></span>  
3. <span data-ttu-id="5da3c-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-132">Click Add.</span></span>
4. <span data-ttu-id="5da3c-133">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="5da3c-134">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="5da3c-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5da3c-135">Наименование</span><span class="sxs-lookup"><span data-stu-id="5da3c-135">Name</span></span>  
6. <span data-ttu-id="5da3c-136">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="5da3c-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="5da3c-137">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-137">Click Add.</span></span>
8. <span data-ttu-id="5da3c-138">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="5da3c-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5da3c-139">Субъект</span><span class="sxs-lookup"><span data-stu-id="5da3c-139">Party</span></span>  
9. <span data-ttu-id="5da3c-140">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="5da3c-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="5da3c-141">Определение структуры банка для этой модели</span><span class="sxs-lookup"><span data-stu-id="5da3c-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="5da3c-142">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5da3c-143">В поле "Имя" введите "Агент".</span><span class="sxs-lookup"><span data-stu-id="5da3c-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="5da3c-144">Агент</span><span class="sxs-lookup"><span data-stu-id="5da3c-144">Agent</span></span>  
3. <span data-ttu-id="5da3c-145">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="5da3c-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="5da3c-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-146">Click Add.</span></span>
5. <span data-ttu-id="5da3c-147">В поле "Описание" введите "Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="5da3c-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="5da3c-148">Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="5da3c-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="5da3c-149">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="5da3c-150">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="5da3c-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="5da3c-151">Наименование</span><span class="sxs-lookup"><span data-stu-id="5da3c-151">Name</span></span>  
8. <span data-ttu-id="5da3c-152">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="5da3c-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="5da3c-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-153">Click Add.</span></span>
10. <span data-ttu-id="5da3c-154">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="5da3c-155">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="5da3c-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="5da3c-156">SWIFT-код</span><span class="sxs-lookup"><span data-stu-id="5da3c-156">SWIFT</span></span>  
12. <span data-ttu-id="5da3c-157">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-157">Click Add.</span></span>
13. <span data-ttu-id="5da3c-158">В поле "Описание" введите "Банковский идентификационный код".</span><span class="sxs-lookup"><span data-stu-id="5da3c-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="5da3c-159">Банковский идентификационный код</span><span class="sxs-lookup"><span data-stu-id="5da3c-159">Bank identification code</span></span>  
14. <span data-ttu-id="5da3c-160">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="5da3c-161">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="5da3c-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="5da3c-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="5da3c-162">RoutingNumber</span></span>  
16. <span data-ttu-id="5da3c-163">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-163">Click Add.</span></span>
17. <span data-ttu-id="5da3c-164">В поле "Описание" введите "Внутренний номер".</span><span class="sxs-lookup"><span data-stu-id="5da3c-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="5da3c-165">Номер маршрута</span><span class="sxs-lookup"><span data-stu-id="5da3c-165">Routing number</span></span>  
18. <span data-ttu-id="5da3c-166">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="5da3c-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="5da3c-167">Определение структуры счета для этой модели</span><span class="sxs-lookup"><span data-stu-id="5da3c-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="5da3c-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5da3c-169">В поле "Имя" введите "Счет".</span><span class="sxs-lookup"><span data-stu-id="5da3c-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="5da3c-170">Учетная запись</span><span class="sxs-lookup"><span data-stu-id="5da3c-170">Account</span></span>  
3. <span data-ttu-id="5da3c-171">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="5da3c-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="5da3c-172">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-172">Click Add.</span></span>
5. <span data-ttu-id="5da3c-173">В поле "Описание" введите "Идентификация счета субъекта в финансовом учреждении (например, банк)".</span><span class="sxs-lookup"><span data-stu-id="5da3c-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="5da3c-174">Идентификация счета субъекта в финансовом учреждении (например, банк).</span><span class="sxs-lookup"><span data-stu-id="5da3c-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="5da3c-175">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="5da3c-176">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="5da3c-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5da3c-177">Валютное</span><span class="sxs-lookup"><span data-stu-id="5da3c-177">Currency</span></span>  
8. <span data-ttu-id="5da3c-178">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="5da3c-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="5da3c-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-179">Click Add.</span></span>
10. <span data-ttu-id="5da3c-180">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="5da3c-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="5da3c-181">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="5da3c-181">Currency code</span></span>  
11. <span data-ttu-id="5da3c-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5da3c-183">В поле "Имя" введите "Номер".</span><span class="sxs-lookup"><span data-stu-id="5da3c-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="5da3c-184">Число</span><span class="sxs-lookup"><span data-stu-id="5da3c-184">Number</span></span>  
13. <span data-ttu-id="5da3c-185">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-185">Click Add.</span></span>
14. <span data-ttu-id="5da3c-186">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="5da3c-187">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="5da3c-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="5da3c-188">номер IBAN</span><span class="sxs-lookup"><span data-stu-id="5da3c-188">IBAN</span></span>  
16. <span data-ttu-id="5da3c-189">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-189">Click Add.</span></span>
17. <span data-ttu-id="5da3c-190">В поле "Описание" введите "Международный номер банковского счета".</span><span class="sxs-lookup"><span data-stu-id="5da3c-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="5da3c-191">Международный номер банковского счета</span><span class="sxs-lookup"><span data-stu-id="5da3c-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="5da3c-192">Определение структуры платежного сообщения для типа платежа "кредитный перевод"</span><span class="sxs-lookup"><span data-stu-id="5da3c-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="5da3c-193">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="5da3c-194">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="5da3c-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="5da3c-195">В поле "Имя" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="5da3c-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="5da3c-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="5da3c-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="5da3c-197">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-197">Click Add.</span></span>
5. <span data-ttu-id="5da3c-198">В поле "Поиск" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="5da3c-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="5da3c-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="5da3c-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="5da3c-200">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="5da3c-200">Click Find previous.</span></span>
7. <span data-ttu-id="5da3c-201">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="5da3c-202">В поле "Имя" введите "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="5da3c-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="5da3c-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="5da3c-203">MessageIdentification</span></span>  
9. <span data-ttu-id="5da3c-204">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-204">Click Add.</span></span>
10. <span data-ttu-id="5da3c-205">В поле "Описание" введите "Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения".</span><span class="sxs-lookup"><span data-stu-id="5da3c-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="5da3c-206">Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения.</span><span class="sxs-lookup"><span data-stu-id="5da3c-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="5da3c-207">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5da3c-208">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="5da3c-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="5da3c-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="5da3c-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="5da3c-210">В поле "Тип элемента" выберите "Дата и время".</span><span class="sxs-lookup"><span data-stu-id="5da3c-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="5da3c-211">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-211">Click Add.</span></span>
15. <span data-ttu-id="5da3c-212">В поле "Описание" введите "Дата и время создания платежного сообщения".</span><span class="sxs-lookup"><span data-stu-id="5da3c-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="5da3c-213">Дата и время создания платежного сообщения.</span><span class="sxs-lookup"><span data-stu-id="5da3c-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="5da3c-214">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="5da3c-215">Определите структуру проводки по оплате для этой модели.</span><span class="sxs-lookup"><span data-stu-id="5da3c-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="5da3c-216">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="5da3c-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="5da3c-217">Оплаты</span><span class="sxs-lookup"><span data-stu-id="5da3c-217">Payments</span></span>  
18. <span data-ttu-id="5da3c-218">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="5da3c-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="5da3c-219">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-219">Click Add.</span></span>
20. <span data-ttu-id="5da3c-220">В поле "Описание" введите "Платежные строки текущего сообщения".</span><span class="sxs-lookup"><span data-stu-id="5da3c-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="5da3c-221">Платежные строки текущего сообщения</span><span class="sxs-lookup"><span data-stu-id="5da3c-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="5da3c-222">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="5da3c-223">В поле "Имя" введите "Кредитор".</span><span class="sxs-lookup"><span data-stu-id="5da3c-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="5da3c-224">Кредитор</span><span class="sxs-lookup"><span data-stu-id="5da3c-224">Creditor</span></span>  
23. <span data-ttu-id="5da3c-225">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="5da3c-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="5da3c-226">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-226">Click Add.</span></span>
25. <span data-ttu-id="5da3c-227">В поле "Описание" введите "Субъект, которому причитается некоторая сумма денег".</span><span class="sxs-lookup"><span data-stu-id="5da3c-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="5da3c-228">Субъект, которому выплачивается денежная сумма.</span><span class="sxs-lookup"><span data-stu-id="5da3c-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="5da3c-229">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="5da3c-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="5da3c-230">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="5da3c-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5da3c-231">Субъект</span><span class="sxs-lookup"><span data-stu-id="5da3c-231">Party</span></span>  
28. <span data-ttu-id="5da3c-232">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="5da3c-232">Click Find next.</span></span>
29. <span data-ttu-id="5da3c-233">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5da3c-233">Click OK.</span></span>
30. <span data-ttu-id="5da3c-234">В поле "Поиск" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="5da3c-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="5da3c-235">Оплаты</span><span class="sxs-lookup"><span data-stu-id="5da3c-235">Payments</span></span>  
31. <span data-ttu-id="5da3c-236">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="5da3c-236">Click Find next.</span></span>
32. <span data-ttu-id="5da3c-237">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="5da3c-238">В поле "Имя" введите "Дебитор".</span><span class="sxs-lookup"><span data-stu-id="5da3c-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="5da3c-239">Дебитор</span><span class="sxs-lookup"><span data-stu-id="5da3c-239">Debtor</span></span>  
34. <span data-ttu-id="5da3c-240">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-240">Click Add.</span></span>
35. <span data-ttu-id="5da3c-241">В поле "Описание" введите "Субъект, который должен некоторую сумму денег (конечному) кредитору".</span><span class="sxs-lookup"><span data-stu-id="5da3c-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="5da3c-242">Субъект, должный денежную сумму (основному) кредитору.</span><span class="sxs-lookup"><span data-stu-id="5da3c-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="5da3c-243">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="5da3c-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="5da3c-244">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="5da3c-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="5da3c-245">Субъект</span><span class="sxs-lookup"><span data-stu-id="5da3c-245">Party</span></span>  
38. <span data-ttu-id="5da3c-246">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="5da3c-246">Click Find next.</span></span>
39. <span data-ttu-id="5da3c-247">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5da3c-247">Click OK.</span></span>
40. <span data-ttu-id="5da3c-248">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="5da3c-248">Click Find next.</span></span>
41. <span data-ttu-id="5da3c-249">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="5da3c-250">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="5da3c-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="5da3c-251">описание</span><span class="sxs-lookup"><span data-stu-id="5da3c-251">Description</span></span>  
43. <span data-ttu-id="5da3c-252">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="5da3c-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="5da3c-253">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-253">Click Add.</span></span>
45. <span data-ttu-id="5da3c-254">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="5da3c-255">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="5da3c-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="5da3c-256">Валютное</span><span class="sxs-lookup"><span data-stu-id="5da3c-256">Currency</span></span>  
47. <span data-ttu-id="5da3c-257">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-257">Click Add.</span></span>
48. <span data-ttu-id="5da3c-258">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="5da3c-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="5da3c-259">Код Валюты</span><span class="sxs-lookup"><span data-stu-id="5da3c-259">Currency code</span></span>  
49. <span data-ttu-id="5da3c-260">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="5da3c-261">В поле "Имя" введите "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="5da3c-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="5da3c-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="5da3c-262">TransactionDate</span></span>  
51. <span data-ttu-id="5da3c-263">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="5da3c-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="5da3c-264">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-264">Click Add.</span></span>
53. <span data-ttu-id="5da3c-265">В поле "Описание" введите "Дата проводки".</span><span class="sxs-lookup"><span data-stu-id="5da3c-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="5da3c-266">Дата проводки</span><span class="sxs-lookup"><span data-stu-id="5da3c-266">Transaction date</span></span>  
54. <span data-ttu-id="5da3c-267">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="5da3c-268">В поле "Имя" введите "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="5da3c-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="5da3c-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="5da3c-269">InstructedAmount</span></span>  
56. <span data-ttu-id="5da3c-270">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="5da3c-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="5da3c-271">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-271">Click Add.</span></span>
58. <span data-ttu-id="5da3c-272">В поле "Описание" введите "Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="5da3c-273">Сумма должна быть выражена в валюте, указанной инициирующим субъектом".</span><span class="sxs-lookup"><span data-stu-id="5da3c-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="5da3c-274">Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="5da3c-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="5da3c-275">Сумма должна быть выражена в валюте, указанной инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="5da3c-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="5da3c-276">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5da3c-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="5da3c-277">В поле "Имя" введите "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="5da3c-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="5da3c-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="5da3c-278">End2EndID</span></span>  
61. <span data-ttu-id="5da3c-279">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="5da3c-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="5da3c-280">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="5da3c-280">Click Add.</span></span>
63. <span data-ttu-id="5da3c-281">В поле "Описание" введите "Уникальный код, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="5da3c-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="5da3c-282">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа".</span><span class="sxs-lookup"><span data-stu-id="5da3c-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="5da3c-283">Уникальный идентификатор, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="5da3c-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="5da3c-284">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="5da3c-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="5da3c-285">В поле "Имя" введите "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="5da3c-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="5da3c-286">Имя PaymentModel соответствует предопределенным интерфейсам форм платежей.</span><span class="sxs-lookup"><span data-stu-id="5da3c-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="5da3c-287">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5da3c-287">Click Save.</span></span>
66. <span data-ttu-id="5da3c-288">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5da3c-288">Close the page.</span></span>

