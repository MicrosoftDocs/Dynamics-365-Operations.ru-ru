---
title: Электронная отчетность Проектирование моделей данных для конкретных доменов
description: В этой теме описывается, как создать новую конфигурацию электронной отчетности (ER), которая содержит модель данных для электронных платежных документов.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eb2c6e5b5f186fb6db7c32a9982807274e5ea1b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092699"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="b9ed6-103">Электронная отчетность Проектирование моделей данных для конкретных доменов</span><span class="sxs-lookup"><span data-stu-id="b9ed6-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9ed6-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности, содержащую модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b9ed6-105">Эта модель данных впоследствии будет использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="b9ed6-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="b9ed6-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="b9ed6-108">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="b9ed6-109">Выберите поставщика конфигурации для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="b9ed6-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Электронная отчетность — создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="b9ed6-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="b9ed6-112">Вам предстоит создать конфигурацию, которая содержит модель данных для электронных платежных документов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b9ed6-113">Эта модель данных будет впоследствии использоваться в качестве источника данных при создании формата для платежных документов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b9ed6-114">Создать новой конфигурации модели данных</span><span class="sxs-lookup"><span data-stu-id="b9ed6-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="b9ed6-115">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b9ed6-116">В поле "Имя" введите "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="b9ed6-117">В поле "Описание" введите "Конфигурация модели платежа".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="b9ed6-118">Активный поставщик конфигурации вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="b9ed6-119">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="b9ed6-120">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="b9ed6-121">Нажмите кнопку "Создать конфигурацию", чтобы завершить задачу создания конфигурации</span><span class="sxs-lookup"><span data-stu-id="b9ed6-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="b9ed6-122">Создание модели данных</span><span class="sxs-lookup"><span data-stu-id="b9ed6-122">Create a data model</span></span>
<span data-ttu-id="b9ed6-123">Вы создаете новую модель данных для выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="b9ed6-124">Эта версия конфигурации будет иметь статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="b9ed6-125">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="b9ed6-126">Определение структуры субъекта, участвующего в процессе оплаты</span><span class="sxs-lookup"><span data-stu-id="b9ed6-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="b9ed6-127">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b9ed6-128">В поле "Имя" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="b9ed6-129">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-129">Click Add.</span></span>
4. <span data-ttu-id="b9ed6-130">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b9ed6-131">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="b9ed6-132">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="b9ed6-133">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-133">Click Add.</span></span>
8. <span data-ttu-id="b9ed6-134">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="b9ed6-135">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="b9ed6-136">Определение структуры банка для этой модели</span><span class="sxs-lookup"><span data-stu-id="b9ed6-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="b9ed6-137">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b9ed6-138">В поле "Имя" введите "Агент".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="b9ed6-139">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b9ed6-140">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-140">Click Add.</span></span>
5. <span data-ttu-id="b9ed6-141">В поле "Описание" введите "Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="b9ed6-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="b9ed6-142">Финансовое учреждение (например, банк), обслуживающее счет субъекта (дебитор/кредитор).</span><span class="sxs-lookup"><span data-stu-id="b9ed6-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="b9ed6-143">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b9ed6-144">В поле "Имя" введите "Имя".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="b9ed6-145">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b9ed6-146">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-146">Click Add.</span></span>
10. <span data-ttu-id="b9ed6-147">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b9ed6-148">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="b9ed6-149">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-149">Click Add.</span></span>
13. <span data-ttu-id="b9ed6-150">В поле "Описание" введите "Банковский идентификационный код".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="b9ed6-151">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b9ed6-152">В поле "Имя" введите "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="b9ed6-153">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-153">Click Add.</span></span>
17. <span data-ttu-id="b9ed6-154">В поле "Описание" введите "Внутренний номер".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="b9ed6-155">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="b9ed6-156">Определение структуры счета для этой модели</span><span class="sxs-lookup"><span data-stu-id="b9ed6-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="b9ed6-157">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b9ed6-158">В поле "Имя" введите "Счет".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="b9ed6-159">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b9ed6-160">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-160">Click Add.</span></span>
5. <span data-ttu-id="b9ed6-161">В поле "Описание" введите "Идентификация счета субъекта в финансовом учреждении (например, банк)".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="b9ed6-162">Идентификация счета субъекта в финансовом учреждении (например, банк).</span><span class="sxs-lookup"><span data-stu-id="b9ed6-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="b9ed6-163">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b9ed6-164">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="b9ed6-165">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b9ed6-166">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-166">Click Add.</span></span>
10. <span data-ttu-id="b9ed6-167">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="b9ed6-168">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b9ed6-169">В поле "Имя" введите "Номер".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="b9ed6-170">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-170">Click Add.</span></span>
14. <span data-ttu-id="b9ed6-171">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b9ed6-172">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="b9ed6-173">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-173">Click Add.</span></span>
17. <span data-ttu-id="b9ed6-174">В поле "Описание" введите "Международный номер банковского счета".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="b9ed6-175">Определение структуры платежного сообщения для типа платежа "кредитный перевод"</span><span class="sxs-lookup"><span data-stu-id="b9ed6-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="b9ed6-176">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b9ed6-177">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="b9ed6-178">В поле "Имя" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="b9ed6-179">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-179">Click Add.</span></span>
5. <span data-ttu-id="b9ed6-180">В поле "Поиск" введите "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="b9ed6-181">Щелкните "Найти предыдущий".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-181">Click Find previous.</span></span>
7. <span data-ttu-id="b9ed6-182">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b9ed6-183">В поле "Имя" введите "MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="b9ed6-184">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-184">Click Add.</span></span>
10. <span data-ttu-id="b9ed6-185">В поле "Описание" введите "Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="b9ed6-186">Ссылка точка-точка, присваиваемая субъектом-поручителем (и отправляемая следующему субъекту) для идентификации сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="b9ed6-187">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b9ed6-188">В поле "Имя" введите "ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="b9ed6-189">В поле "Тип элемента" выберите "Дата и время".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="b9ed6-190">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-190">Click Add.</span></span>
15. <span data-ttu-id="b9ed6-191">В поле "Описание" введите "Дата и время создания платежного сообщения".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="b9ed6-192">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="b9ed6-193">Определите структуру проводки по оплате для этой модели.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="b9ed6-194">В поле "Имя" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="b9ed6-195">В поле "Тип элемента" выберите "Список записей".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="b9ed6-196">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-196">Click Add.</span></span>
20. <span data-ttu-id="b9ed6-197">В поле "Описание" введите "Платежные строки текущего сообщения".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="b9ed6-198">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b9ed6-199">В поле "Имя" введите "Кредитор".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="b9ed6-200">В поле "Тип элемента" выберите "Запись".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="b9ed6-201">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-201">Click Add.</span></span>
25. <span data-ttu-id="b9ed6-202">В поле "Описание" введите "Субъект, которому причитается некоторая сумма денег".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="b9ed6-203">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="b9ed6-204">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="b9ed6-205">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-205">Click Find next.</span></span>
29. <span data-ttu-id="b9ed6-206">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-206">Click OK.</span></span>
30. <span data-ttu-id="b9ed6-207">В поле "Поиск" введите "Платежи".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="b9ed6-208">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-208">Click Find next.</span></span>
32. <span data-ttu-id="b9ed6-209">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="b9ed6-210">В поле "Имя" введите "Дебитор".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="b9ed6-211">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-211">Click Add.</span></span>
35. <span data-ttu-id="b9ed6-212">В поле "Описание" введите "Субъект, который должен некоторую сумму денег (конечному) кредитору".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="b9ed6-213">Щелкните "Переключить ссылку номенклатуры".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="b9ed6-214">В поле "Поиск" введите "Субъект".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="b9ed6-215">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-215">Click Find next.</span></span>
39. <span data-ttu-id="b9ed6-216">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-216">Click OK.</span></span>
40. <span data-ttu-id="b9ed6-217">Нажмите кнопку "Найти далее".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-217">Click Find next.</span></span>
41. <span data-ttu-id="b9ed6-218">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b9ed6-219">В поле "Имя" введите "Описание".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="b9ed6-220">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="b9ed6-221">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-221">Click Add.</span></span>
45. <span data-ttu-id="b9ed6-222">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b9ed6-223">В поле "Имя" введите "Валюта".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="b9ed6-224">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-224">Click Add.</span></span>
48. <span data-ttu-id="b9ed6-225">В поле "Описание" введите "Код валюты".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="b9ed6-226">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="b9ed6-227">В поле "Имя" введите "TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="b9ed6-228">В поле "Тип элемента" выберите "Дата".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="b9ed6-229">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-229">Click Add.</span></span>
53. <span data-ttu-id="b9ed6-230">В поле "Описание" введите "Дата проводки".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="b9ed6-231">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="b9ed6-232">В поле "Имя" введите "InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="b9ed6-233">В поле "Тип элемента" выберите "Вещественный".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="b9ed6-234">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-234">Click Add.</span></span>
58. <span data-ttu-id="b9ed6-235">В поле "Описание" введите "Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b9ed6-236">Сумма должна быть выражена в валюте, указанной инициирующим субъектом".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="b9ed6-237">Денежная сумма, которая будет переведена со счета дебитора на счет кредитора, до вычета накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b9ed6-238">Сумма должна быть выражена в валюте, указанной инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="b9ed6-239">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b9ed6-240">В поле "Имя" введите "End2EndID".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="b9ed6-241">В поле "Тип элемента" выберите "Строка".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b9ed6-242">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-242">Click Add.</span></span>
63. <span data-ttu-id="b9ed6-243">В поле "Описание" введите "Уникальный код, назначенный инициирующим субъектом.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="b9ed6-244">Этот идентификатор передается в неизменном виде по всей цепочке обработки платежа".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="b9ed6-245">В поле "Имя" введите "PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="b9ed6-246">Имя PaymentModel соответствует предопределенным интерфейсам форм платежей.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="b9ed6-247">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b9ed6-247">Click Save.</span></span>
66. <span data-ttu-id="b9ed6-248">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-248">Close the page.</span></span>

