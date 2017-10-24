--- 
title: "Выбор определения модели данных при создании формата для электронной отчетности (ER)"
description: "Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру \"Электронная отчетность — Создание поставщика конфигурации и пометка его как активного\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 70d928b0f0807731a5f96ef5497fb6060fbfebf5
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a><span data-ttu-id="b70d4-103">Выбор определения модели данных при создании формата для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="b70d4-103">Select data model definition while creating format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b70d4-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="b70d4-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="b70d4-105">Эта процедура показывает, как можно выбрать корневой элемент модели в качестве определения модели данных для вставки конфигурации формата электронной отчетности, предназначенного для формирования электронных документов.</span><span class="sxs-lookup"><span data-stu-id="b70d4-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="b70d4-106">В этой процедуре вам предстоит добавить новую конфигурацию формата для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b70d4-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="b70d4-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="b70d4-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="b70d4-108">Действия можно выполнять с использованием любого набора данных,</span><span class="sxs-lookup"><span data-stu-id="b70d4-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="b70d4-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="b70d4-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b70d4-110">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="b70d4-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="b70d4-111">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и пометка его как активного".</span><span class="sxs-lookup"><span data-stu-id="b70d4-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="b70d4-112">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="b70d4-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="b70d4-113">Добавление новой конфигурации модели данных электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b70d4-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="b70d4-114">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="b70d4-115">Мы добавим новую конфигурацию модели электронной отчетности, содержащую модель данных, предназначенную для использования в качестве источника данных для формирования отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b70d4-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="b70d4-116">В поле "Имя" введите "Модель платежа (вымышленная)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="b70d4-117">Модель платежа (вымышленная)</span><span class="sxs-lookup"><span data-stu-id="b70d4-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="b70d4-118">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b70d4-118">Click Create configuration.</span></span>
4. <span data-ttu-id="b70d4-119">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b70d4-119">Click Designer.</span></span>
    * <span data-ttu-id="b70d4-120">Откройте конструктор электронной отчетности для задания структуры модели данных этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b70d4-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="b70d4-121">Предположим, что мы разрабатываем модель данных для бизнес-домена платежей, которая будет поддерживать два способа оплаты — кредитный перевод и прямое дебетование.</span><span class="sxs-lookup"><span data-stu-id="b70d4-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="b70d4-122">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="b70d4-123">В поле "Имя" введите "Платежи — кредитный перевод".</span><span class="sxs-lookup"><span data-stu-id="b70d4-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="b70d4-124">Платежи — кредитный перевод</span><span class="sxs-lookup"><span data-stu-id="b70d4-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="b70d4-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b70d4-125">Click Add.</span></span>
8. <span data-ttu-id="b70d4-126">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="b70d4-127">В поле "Новый узел как" введите "Корень модели".</span><span class="sxs-lookup"><span data-stu-id="b70d4-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="b70d4-128">В поле "Имя" введите "Платежи — прямое дебетование".</span><span class="sxs-lookup"><span data-stu-id="b70d4-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="b70d4-129">Платежи — прямое дебетование</span><span class="sxs-lookup"><span data-stu-id="b70d4-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="b70d4-130">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b70d4-130">Click Add.</span></span>
12. <span data-ttu-id="b70d4-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b70d4-131">Click Save.</span></span>
13. <span data-ttu-id="b70d4-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-132">Close the page.</span></span>
14. <span data-ttu-id="b70d4-133">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="b70d4-133">Click Change status.</span></span>
    * <span data-ttu-id="b70d4-134">Завершите черновую версию модели, чтобы сделать ее доступной в новых сопоставлениях модели и форматах.</span><span class="sxs-lookup"><span data-stu-id="b70d4-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="b70d4-135">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="b70d4-135">Click Complete.</span></span>
16. <span data-ttu-id="b70d4-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b70d4-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="b70d4-137">Начало ввода новой конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b70d4-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="b70d4-138">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b70d4-139">В поле "Создать" введите "Формат, основанный на модели данных Модель платежа (вымышленная)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="b70d4-140">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b70d4-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="b70d4-141">Обратите внимание, что все корневые элементы модели данных в настоящее время доступны для выбора в качестве определения модели данных.</span><span class="sxs-lookup"><span data-stu-id="b70d4-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="b70d4-142">Можно продолжать разрабатывать формат, используя любые из необходимых корневых элементов модели данных.</span><span class="sxs-lookup"><span data-stu-id="b70d4-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="b70d4-143">Отсутствие сопоставления модели для выбранного корневого элемента не мешает продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="b70d4-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="b70d4-145">Добавление новой конфигурации сопоставлений модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b70d4-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="b70d4-146">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b70d4-147">В поле "Создать" введите "Сопоставление модели, основанное на модели данных Модель платежа (вымышленная)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="b70d4-148">В поле "Имя" введите "Сопоставления модели платежей (вымышленной)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="b70d4-149">Сопоставления модели платежей (вымышленные)</span><span class="sxs-lookup"><span data-stu-id="b70d4-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="b70d4-150">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b70d4-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="b70d4-151">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b70d4-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="b70d4-152">Разработка сопоставлений модели электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b70d4-152">Design ER model mappings</span></span>
1. <span data-ttu-id="b70d4-153">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b70d4-153">Click Designer.</span></span>
    * <span data-ttu-id="b70d4-154">С помощью конструктора электронной отчетности задайте сопоставления модели для необходимых корневых элементов.</span><span class="sxs-lookup"><span data-stu-id="b70d4-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="b70d4-155">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="b70d4-155">Click Designer.</span></span>
    * <span data-ttu-id="b70d4-156">Смоделируйте установку выбранного сопоставления модели для корневого элемента выбранной модели.</span><span class="sxs-lookup"><span data-stu-id="b70d4-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="b70d4-157">В дереве выберите "Dynamics 365 for Operations\Записи таблицы".</span><span class="sxs-lookup"><span data-stu-id="b70d4-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="b70d4-158">Щелкните "Добавить корень".</span><span class="sxs-lookup"><span data-stu-id="b70d4-158">Click Add root.</span></span>
5. <span data-ttu-id="b70d4-159">В поле "Имя" введите "Книга учета".</span><span class="sxs-lookup"><span data-stu-id="b70d4-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="b70d4-160">В поле "Таблица" введите "LedgerJournalTrans".</span><span class="sxs-lookup"><span data-stu-id="b70d4-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="b70d4-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b70d4-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="b70d4-162">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b70d4-162">Click OK.</span></span>
8. <span data-ttu-id="b70d4-163">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b70d4-163">Click Save.</span></span>
9. <span data-ttu-id="b70d4-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-164">Close the page.</span></span>
10. <span data-ttu-id="b70d4-165">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="b70d4-166">Начало ввода другой конфигурации формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b70d4-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="b70d4-167">В дереве выберите "Модель платежа (вымышленная)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="b70d4-168">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b70d4-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="b70d4-169">В поле "Создать" введите "Формат, основанный на модели данных Модель платежа (вымышленная)".</span><span class="sxs-lookup"><span data-stu-id="b70d4-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="b70d4-170">В поле "Определение модели данных" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b70d4-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="b70d4-171">Обратите внимание, что теперь только один корневой элемент доступен для сопоставления с источниками данных приложения.</span><span class="sxs-lookup"><span data-stu-id="b70d4-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="b70d4-172">При создании хотя бы одного сопоставления модели только корневые элементы модели, сопоставленные источникам данных приложения, могут быть выбраны в качестве определения модели при добавлении формата электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b70d4-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="b70d4-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b70d4-173">Close the page.</span></span>

