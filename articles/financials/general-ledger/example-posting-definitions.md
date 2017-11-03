---
title: "Определения разносок"
description: "В этой статье приводятся примеры, которые показывают, как используются определения разноски для бюджетных обязательств по заказу на покупку и ассигнований бюджета."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1bbd9230219f11407bc7afbd59670c6287b77c02
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definition-examples"></a><span data-ttu-id="ed9e1-103">Примеры определений разноски</span><span class="sxs-lookup"><span data-stu-id="ed9e1-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ed9e1-104">В этой статье приводятся примеры, которые показывают, как используются определения разноски для бюджетных обязательств по заказу на покупку и ассигнований бюджета.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="ed9e1-105">Перед прочтением этой темы необходимо ознакомиться с определениями разноски и определениями разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="ed9e1-106">Информацию см. в разделе [Определения разносок](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="ed9e1-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="ed9e1-107">Следующие примеры можно настроить на странице **Определения разносок**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="ed9e1-108">Каждый пример содержит перечисленные ниже разделы:</span><span class="sxs-lookup"><span data-stu-id="ed9e1-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="ed9e1-109">Определение разноски - Критерии соответствия</span><span class="sxs-lookup"><span data-stu-id="ed9e1-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="ed9e1-110">Определение разноски - Созданные записи</span><span class="sxs-lookup"><span data-stu-id="ed9e1-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="ed9e1-111">Проводки со счетами, значениями аналитик и суммами</span><span class="sxs-lookup"><span data-stu-id="ed9e1-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="ed9e1-112">Записи в книге учета, созданные из определения разноски</span><span class="sxs-lookup"><span data-stu-id="ed9e1-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed9e1-113">Если между счетами и значениями аналитик на панели **Критерий соответствия** для определения разноски и счетами и значениями аналитик в проводке обнаруживается соответствие, в книге учета создаются записи с учетом панели **Созданные записи** для определения разноски.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="ed9e1-114">Для связывания определения разноски с проводками конкретного типа используйте страницу **Определения разноски проводок**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="ed9e1-115">После связывания определения разноски с типом проводок и установки флажка **Использовать определения разносок** на странице **Параметры главной книги** все проводки выбранного типа должны использовать определения разноски.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="ed9e1-116">Пример: Бюджетные обязательства по заказу на покупку</span><span class="sxs-lookup"><span data-stu-id="ed9e1-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="ed9e1-117">Если установкой флажка **Включить обработку бюджетного обязательства** на странице **Параметры главной книги** разрешена обработка бюджетных обязательств, при регистрации бюджетных обязательств в главной книге по всем счетам, подлежащим резервированию, должны использоваться определения разноски.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="ed9e1-118">В большинстве случаев в балансовом отчете резервируются все расходные счета.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="ed9e1-119">Определения разноски для бюджетных обязательств для модуля **Покупка** настраиваются на странице **Определения разносок**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ed9e1-120">Затем в области **Покупка** страницы **Определения разноски проводок** можно выбрать тип проводки **Заказ на покупку** для связывания определения разноски с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="ed9e1-121">Все проводки ваучера для бюджетных обязательств по заказу на покупку должны быть сбалансированы (т. е. дебет должен быть равен кредиту) в каждой уникальной аналитике ваучера.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ed9e1-122">Определение разноски - Критерии соответствия</span><span class="sxs-lookup"><span data-stu-id="ed9e1-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ed9e1-123">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-123">Account structure</span></span>       | <span data-ttu-id="ed9e1-124">Сопоставлять номер счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-124">Match account number</span></span> | <span data-ttu-id="ed9e1-125">Приоритет</span><span class="sxs-lookup"><span data-stu-id="ed9e1-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ed9e1-126">Структура счета - Прибыли и убытки</span><span class="sxs-lookup"><span data-stu-id="ed9e1-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ed9e1-127">1</span><span class="sxs-lookup"><span data-stu-id="ed9e1-127">1</span></span>        |

<span data-ttu-id="ed9e1-128">*Пустое значение в поле **Сопоставлять номер счета** означает, что все соответствующие счета в определенной структуре счета являются частью правила соответствия.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ed9e1-129">Определение разноски - Созданные записи</span><span class="sxs-lookup"><span data-stu-id="ed9e1-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ed9e1-130">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-130">Account structure</span></span> | <span data-ttu-id="ed9e1-131">Созданный номер счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-131">Generated account number</span></span>                    | <span data-ttu-id="ed9e1-132">Созданный дебет/кредит</span><span class="sxs-lookup"><span data-stu-id="ed9e1-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="ed9e1-133">Сальдо</span><span class="sxs-lookup"><span data-stu-id="ed9e1-133">Balance</span></span>           | <span data-ttu-id="ed9e1-134">300143 - -(Счет бюджетных обязательств)</span><span class="sxs-lookup"><span data-stu-id="ed9e1-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="ed9e1-135">Одинаковые</span><span class="sxs-lookup"><span data-stu-id="ed9e1-135">Same</span></span>                   |
| <span data-ttu-id="ed9e1-136">Сальдо</span><span class="sxs-lookup"><span data-stu-id="ed9e1-136">Balance</span></span>           | <span data-ttu-id="ed9e1-137">300144 - -(Резерв для счета бюджетных обязательств)</span><span class="sxs-lookup"><span data-stu-id="ed9e1-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="ed9e1-138">Балансирование</span><span class="sxs-lookup"><span data-stu-id="ed9e1-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ed9e1-139">Проводки со счетами, значениями аналитик и суммами</span><span class="sxs-lookup"><span data-stu-id="ed9e1-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ed9e1-140">Счета и значения аналитики извлекаются из распределений по бухгалтерским счетам, указанных для строки заказа на покупку, или из счетов и аналитик, созданных автоматически с учетом значений по умолчанию для поставщиков, номенклатур, категорий и шаблонов аналитик.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="ed9e1-141">Счет + аналитики</span><span class="sxs-lookup"><span data-stu-id="ed9e1-141">Account + dimensions</span></span>           | <span data-ttu-id="ed9e1-142">по дебету</span><span class="sxs-lookup"><span data-stu-id="ed9e1-142">Debit</span></span>  | <span data-ttu-id="ed9e1-143">по кредиту</span><span class="sxs-lookup"><span data-stu-id="ed9e1-143">Credit</span></span> | <span data-ttu-id="ed9e1-144">Комментарий</span><span class="sxs-lookup"><span data-stu-id="ed9e1-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed9e1-145">606400-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed9e1-146">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ed9e1-147">Записи в книге учета, созданные из определения разноски</span><span class="sxs-lookup"><span data-stu-id="ed9e1-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed9e1-148">Созданные записи книги учета формируются для регистрации бюджетных обязательств.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="ed9e1-149">Счет + аналитики</span><span class="sxs-lookup"><span data-stu-id="ed9e1-149">Account + dimensions</span></span>           | <span data-ttu-id="ed9e1-150">по дебету</span><span class="sxs-lookup"><span data-stu-id="ed9e1-150">Debit</span></span>  | <span data-ttu-id="ed9e1-151">по кредиту</span><span class="sxs-lookup"><span data-stu-id="ed9e1-151">Credit</span></span> | <span data-ttu-id="ed9e1-152">Комментарий</span><span class="sxs-lookup"><span data-stu-id="ed9e1-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed9e1-153">300143-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed9e1-154">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-154">250.00</span></span> |        |         |
| <span data-ttu-id="ed9e1-155">300144-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ed9e1-156">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-156">250.00</span></span> |         |

<span data-ttu-id="ed9e1-157">В этом примере критериям определения разноски соответствует любой счет в составе модуля "Структура счета - Прибыли и убытки".</span><span class="sxs-lookup"><span data-stu-id="ed9e1-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ed9e1-158">Поэтому при оценке модуля "606500-OU\_1-OU\_3566-Обучение" созданные записи формируются для счетов, указанных на панели **Созданные записи** для определения разноски.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="ed9e1-159">Пример: Ассигнования бюджета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-159">Example: Budget appropriations</span></span>
<span data-ttu-id="ed9e1-160">Если установкой флажка **Включить ассигнование бюджета** на странице **Параметры главной книги** включено ассигнование бюджета, при регистрации записей регистра бюджета в главной книге должны использоваться определения разноски.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="ed9e1-161">Если конфигурация бюджетного контроля активна и включена, определения разноски и определения разноски проводок можно использовать для поддержки регистрации в главной книге записей ассигнований, пересмотров, передач, проектов, основных средств и прогнозов предложения и спроса.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="ed9e1-162">Чтобы настроить определения разноски для записей регистра бюджета с типом **Исходный бюджет** и включенным режимом ассигнования, выберите модуль **Бюджет** на странице **Определения разносок**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="ed9e1-163">Затем в области **Бюджет** на странице **Определения разноски проводок** можно использовать коды бюджета, чтобы связать определение разноски с записями регистра бюджета, имеющими тип бюджета **Исходный бюджет**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="ed9e1-164">Если ассигнования бюджета и определения разноски включены, записи регистра бюджета регистрируются для контроля бюджета и в главной книге.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="ed9e1-165">Определение разноски - Критерии соответствия</span><span class="sxs-lookup"><span data-stu-id="ed9e1-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="ed9e1-166">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-166">Account structure</span></span>       | <span data-ttu-id="ed9e1-167">Сопоставлять номер счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-167">Match account number</span></span> | <span data-ttu-id="ed9e1-168">Приоритет</span><span class="sxs-lookup"><span data-stu-id="ed9e1-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="ed9e1-169">Структура счета - Прибыли и убытки</span><span class="sxs-lookup"><span data-stu-id="ed9e1-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="ed9e1-170">1</span><span class="sxs-lookup"><span data-stu-id="ed9e1-170">1</span></span>        |

<span data-ttu-id="ed9e1-171">*Пустое значение в поле **Сопоставлять номер счета** означает, что все соответствующие счета в определенной структуре счета являются частью правила соответствия.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="ed9e1-172">Определение разноски - Созданные записи</span><span class="sxs-lookup"><span data-stu-id="ed9e1-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="ed9e1-173">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-173">Account structure</span></span> | <span data-ttu-id="ed9e1-174">Созданный номер счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-174">Generated account number</span></span>              | <span data-ttu-id="ed9e1-175">Созданный дебет/кредит</span><span class="sxs-lookup"><span data-stu-id="ed9e1-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="ed9e1-176">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-176">Account structure</span></span> | <span data-ttu-id="ed9e1-177">300145 - -(Счет ожидаемой выручки)</span><span class="sxs-lookup"><span data-stu-id="ed9e1-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="ed9e1-178">Одинаковые</span><span class="sxs-lookup"><span data-stu-id="ed9e1-178">Same</span></span>                   |
| <span data-ttu-id="ed9e1-179">Структура счета</span><span class="sxs-lookup"><span data-stu-id="ed9e1-179">Account structure</span></span> | <span data-ttu-id="ed9e1-180">300146 - -(Счет ассигнования)</span><span class="sxs-lookup"><span data-stu-id="ed9e1-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="ed9e1-181">Балансирование</span><span class="sxs-lookup"><span data-stu-id="ed9e1-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="ed9e1-182">Проводки со счетами, значениями аналитик и суммами</span><span class="sxs-lookup"><span data-stu-id="ed9e1-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="ed9e1-183">Счета, значения аналитик и суммы для записи по бюджетному счету вводятся на странице **Запись бюджетного регистра**.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="ed9e1-184">Счет + аналитики</span><span class="sxs-lookup"><span data-stu-id="ed9e1-184">Account + dimensions</span></span>           | <span data-ttu-id="ed9e1-185">по дебету</span><span class="sxs-lookup"><span data-stu-id="ed9e1-185">Debit</span></span> | <span data-ttu-id="ed9e1-186">по кредиту</span><span class="sxs-lookup"><span data-stu-id="ed9e1-186">Credit</span></span> | <span data-ttu-id="ed9e1-187">Комментарий</span><span class="sxs-lookup"><span data-stu-id="ed9e1-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="ed9e1-188">606400-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="ed9e1-189">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="ed9e1-190">Записи в книге учета, созданные из определения разноски</span><span class="sxs-lookup"><span data-stu-id="ed9e1-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="ed9e1-191">Созданные записи книги учета формируются для регистрации исходного бюджета в каждой аналитике.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="ed9e1-192">Счет + аналитики</span><span class="sxs-lookup"><span data-stu-id="ed9e1-192">Account + dimensions</span></span>           | <span data-ttu-id="ed9e1-193">по дебету</span><span class="sxs-lookup"><span data-stu-id="ed9e1-193">Debit</span></span>  | <span data-ttu-id="ed9e1-194">по кредиту</span><span class="sxs-lookup"><span data-stu-id="ed9e1-194">Credit</span></span> | <span data-ttu-id="ed9e1-195">Комментарий</span><span class="sxs-lookup"><span data-stu-id="ed9e1-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="ed9e1-196">300145-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="ed9e1-197">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-197">250.00</span></span> |         |
| <span data-ttu-id="ed9e1-198">300146-OU\_1-OU\_3566-Обучение</span><span class="sxs-lookup"><span data-stu-id="ed9e1-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="ed9e1-199">250.00</span><span class="sxs-lookup"><span data-stu-id="ed9e1-199">250.00</span></span> |        |         |

<span data-ttu-id="ed9e1-200">В этом примере критериям определения разноски соответствует любой счет в составе модуля "Структура счета - Прибыли и убытки".</span><span class="sxs-lookup"><span data-stu-id="ed9e1-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="ed9e1-201">Поэтому при оценке модуля "606400-OU\_1-OU\_3566-Обучение" формируются созданные записи книги учета.</span><span class="sxs-lookup"><span data-stu-id="ed9e1-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






