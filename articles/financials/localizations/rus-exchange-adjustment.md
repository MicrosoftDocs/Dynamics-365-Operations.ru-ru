---
title: Курсовая разница
description: В данном разделе содержится информация об учете банковской курсовой разницы для России.
author: anasyash
manager: kfend
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 37b97345626c8ff54fcc794ec65169b205585c62
ms.sourcegitcommit: ac02d2aa289d9c26321509b3ee1deffbc0f77c96
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886856"
---
# <a name="exchange-adjustment"></a><span data-ttu-id="f3e54-103">Курсовая разница</span><span class="sxs-lookup"><span data-stu-id="f3e54-103">Exchange adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3e54-104">На дату составления отчета должен использоваться валютный курс Центрального Банка России для переоценки сальдо денежных средств на банковском счете в иностранной валюте, чтобы оно правильно отображало значение сальдо денежных средств в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="f3e54-104">On the reporting date, the Central Bank of Russia's exchange rate must be used to revalue the cash balance on a foreign currency bank account so that it correctly represents the cash balance value in the accounting currency.</span></span> <span data-ttu-id="f3e54-105">Разница валютного курса из переоценки валютного банковского счета — это разница между суммой наличных денежных средств, в валюте учета, на банковском счету на дату платежа (или дату отчета предыдущего отчетного периода) и суммой наличных денежных средств, в валюте учета, банковского счету на дату отчетности.</span><span class="sxs-lookup"><span data-stu-id="f3e54-105">The exchange rate difference from the revaluation of the currency bank account is the difference between the value, in the accounting currency, of cash in the bank account on the date of the payment (or on the reporting date of the previous reporting period) and the value, in the accounting currency, of the cash in the bank account on the reporting date.</span></span>

## <a name="accounting-of-exchange-rate-differences"></a><span data-ttu-id="f3e54-106">Учет разницы валютного курса</span><span class="sxs-lookup"><span data-stu-id="f3e54-106">Accounting of exchange rate differences</span></span>
<span data-ttu-id="f3e54-107">В целях учета разница валютного курса обычно записывается в виде других доходов и расходов на счет ГК, например **счет ГК 91 — Прочие доходы и расходы**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-107">For accounting purposes, exchange rate differences are typically recorded as other income and expenses in the ledger account, such as **ledger account 91 - Other income and expenses**.</span></span> <span data-ttu-id="f3e54-108">В целях учета подоходного налога разница валютного курса учитывается как неоперационный доход и расходы.</span><span class="sxs-lookup"><span data-stu-id="f3e54-108">For the purpose of income tax accounting, exchange rate differences are considered non-operational income and expenses.</span></span>
<span data-ttu-id="f3e54-109">Разница валютного курса для банковского счета в валюте может быть положительной (при увеличении валютного курса) или отрицательной (когда валютный курс уменьшается).</span><span class="sxs-lookup"><span data-stu-id="f3e54-109">The exchange rate difference on the currency bank account can be either positive (when the currency exchange rate increases) or negative (when the currency exchange rate decreases).</span></span> <span data-ttu-id="f3e54-110">В следующей таблице показаны примеры проводок главной книги для положительных и отрицательных значений разницы валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-110">The following table shows examples of ledger transactions for positive and negative exchange rate differences.</span></span>

| <span data-ttu-id="f3e54-111">Проводка ГК</span><span class="sxs-lookup"><span data-stu-id="f3e54-111">Ledger transaction</span></span>                                            | <span data-ttu-id="f3e54-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f3e54-112">Description</span></span>                       |
|---------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="f3e54-113">Дебет 91 (нереализованная убыток) Кредит 52 (валютные банковские счета)</span><span class="sxs-lookup"><span data-stu-id="f3e54-113">Debit 91 (unrealized loss) Credit 52 (currency bank accounts)</span></span> | <span data-ttu-id="f3e54-114">Отрицательная курсовая разница</span><span class="sxs-lookup"><span data-stu-id="f3e54-114">Negative exchange rate difference</span></span> |
| <span data-ttu-id="f3e54-115">Дебет 52 (валютные банковские счета) Кредит 91 (нереализованная прибыль)</span><span class="sxs-lookup"><span data-stu-id="f3e54-115">Debit 52 (currency bank accounts) Credit 91 (unrealized gain)</span></span> | <span data-ttu-id="f3e54-116">Положительная курсовая разница</span><span class="sxs-lookup"><span data-stu-id="f3e54-116">Positive exchange rate difference</span></span> |

## <a name="setup"></a><span data-ttu-id="f3e54-117">Настройка</span><span class="sxs-lookup"><span data-stu-id="f3e54-117">Setup</span></span>

### <a name="set-up-ledger-accounts-for-currency-bank-account-revaluation"></a><span data-ttu-id="f3e54-118">Настройка счетов книги учета для переоценки валютных банковских счетов</span><span class="sxs-lookup"><span data-stu-id="f3e54-118">Set up ledger accounts for currency bank account revaluation</span></span>

1. <span data-ttu-id="f3e54-119">Откройте **Главная книга** \> **Валюты** \> **Параметры валюты**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-119">Go to **General ledger** \> **Currencies** \> **Currency parameters**.</span></span>
2. <span data-ttu-id="f3e54-120">В левой части страницы **Счета валютной переоценки** в поле **Юридические лица** выберите компанию.</span><span class="sxs-lookup"><span data-stu-id="f3e54-120">On the left side of the **Currency revaluation accounts** page, in the **Legal entities** field, select a company.</span></span>
3. <span data-ttu-id="f3e54-121">Выберите валюту проводки, затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-121">Select the transaction currency, and then select **Edit**.</span></span>
4. <span data-ttu-id="f3e54-122">Для параметра **Активация параметров** задайте значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-122">Set the **Activate parameters** option to **Yes**.</span></span>
5. <span data-ttu-id="f3e54-123">На экспресс-вкладке **Общие** в сетке в поле **Разноска** выберите **Нереализованная прибыль**, затем в поле **Счет ГК** выберите счет книги учета для разноски прибыли от валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-123">On the **General** FastTab, in the grid, in the **Posting** field, select **Unrealized gain**, and then, in the **Main account** field, select the ledger account to post the exchange rate gain to.</span></span>
6. <span data-ttu-id="f3e54-124">В поле **Разноска** выберите **Нереализованные убытки**, затем в поле **Счет ГК** выберите счет книги учета для разноски убытка от валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-124">In the **Posting** field, select **Unrealized loss**, and then, in the **Main account** field, select the ledger account to post exchange rate loss to.</span></span>
7. <span data-ttu-id="f3e54-125">В поле **Код дохода** выберите код дохода/расхода для целей налогового учета, соответствующий прибыли от валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-125">In the **Income code** field, select the income/expense code for tax accounting purposes that corresponds to the exchange rate gain.</span></span>
8. <span data-ttu-id="f3e54-126">В поле **Код расхода** выберите код дохода/расхода для целей налогового учета, соответствующий убытку от валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-126">In the **Expense code** field, select the income/expense code for tax accounting purchases that corresponds to the exchange rate loss.</span></span>
9. <span data-ttu-id="f3e54-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-127">Select **Save**.</span></span>

### <a name="set-up-a-number-sequence"></a><span data-ttu-id="f3e54-128">Настройка номерной серии</span><span class="sxs-lookup"><span data-stu-id="f3e54-128">Set up a number sequence</span></span>

1. <span data-ttu-id="f3e54-129">Перейдите в раздел **Управление банком и кассовыми операциями** \> **Настройка** \> **Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-129">Go to **Cash and bank management** \> **Setup** \> **Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="f3e54-130">На вкладке **Номерные серии** в поле **Код номерной серии** выберите код номерной серии для ссылки **Банк - Учет курсовой разницы**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-130">On the **Number sequences** tab, in the **Number sequence code** field, select a number sequence code for the **Bank – Exchange adjustment** reference.</span></span>

## <a name="calculate-the-exchange-rate-difference-for-a-bank-account"></a><span data-ttu-id="f3e54-131">Расчет разницы по валютному курсу для банковского счета</span><span class="sxs-lookup"><span data-stu-id="f3e54-131">Calculate the exchange rate difference for a bank account</span></span>
<span data-ttu-id="f3e54-132">Для выполнения переоценки на дату отчетности используется страница **Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-132">To do revaluation on the reporting date, use the **Foreign currency revaluation** page.</span></span>

1. <span data-ttu-id="f3e54-133">Выберите **Управление банком и кассовыми операциями** \> **Периодические задачи** \> **Переоценка в иностранной валюте — Банк**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-133">Go to **Cash and bank management** \> **Periodic tasks** \> **Foreign currency revaluation – Bank**.</span></span>
2. <span data-ttu-id="f3e54-134">На странице **Переоценка в иностранной валюте** в поле **На дату** выберите дату переоценки.</span><span class="sxs-lookup"><span data-stu-id="f3e54-134">On the **Foreign currency revaluation** page, in the **On date** field, select the revaluation date.</span></span>
3. <span data-ttu-id="f3e54-135">В полях **Из валюты** и **В валюту** задайте диапазон кодов валюты, для которых необходимо выполнить переоценку.</span><span class="sxs-lookup"><span data-stu-id="f3e54-135">In the **From currency** and **To currency** fields, define the range of currency codes that should be revalued.</span></span>
4. <span data-ttu-id="f3e54-136">Выберите **фильтр**, чтобы настроить дополнительные критерии фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f3e54-136">Select **Filter** to set up additional criteria for filtering.</span></span> <span data-ttu-id="f3e54-137">Например, выберите конкретный валютный банковский счет для переоценки.</span><span class="sxs-lookup"><span data-stu-id="f3e54-137">For example, select a specific currency bank account to revalue.</span></span>
5. <span data-ttu-id="f3e54-138">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-138">Select **OK**.</span></span> <span data-ttu-id="f3e54-139">Рассчитывается курсовая разница для выбранной даты.</span><span class="sxs-lookup"><span data-stu-id="f3e54-139">The exchange difference for the selected date is calculated.</span></span> <span data-ttu-id="f3e54-140">Будет выведено сообщение с указанием даты и суммы проводки валютного курса.</span><span class="sxs-lookup"><span data-stu-id="f3e54-140">You receive a message that indicates the date and amount of the exchange rate transaction.</span></span>

## <a name="view-exchange-adjustment-transactions"></a><span data-ttu-id="f3e54-141">Просмотр проводок по курсовым разницам</span><span class="sxs-lookup"><span data-stu-id="f3e54-141">View exchange adjustment transactions</span></span>
<span data-ttu-id="f3e54-142">Можно просмотреть разнесенные проводки курсовой разницы на странице **Банковские проводки**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-142">You can review the posted exchange adjustment transactions on the **Bank transactions** page.</span></span>

1. <span data-ttu-id="f3e54-143">Перейдите в раздел **Управление банком и кассовыми операциями** \> **Банковские счета** \> **Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-143">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="f3e54-144">Выберите банковский счет, затем выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-144">Select the bank account, and then select **Transactions**.</span></span>
3. <span data-ttu-id="f3e54-145">На странице **Банковские проводки** просмотрите проводки, которые были разнесены из-за переоценки.</span><span class="sxs-lookup"><span data-stu-id="f3e54-145">On the **Bank transactions** page, review the transactions that were posted because of the revaluation.</span></span> <span data-ttu-id="f3e54-146">В поле **Тип проводки книги учета** для этих проводок устанавливается значение **Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-146">The **Ledger transaction type** field for these transactions is set to **Foreign currency revaluation**.</span></span>

> [!NOTE]
> <span data-ttu-id="f3e54-147">Если столбец **Тип проводки книги учета** не отображается, щелкните правой кнопкой мыши в любом месте в строке сетки, отображающем имена столбцов, выберите **Добавить столбцы**, затем выберите **Тип проводки книги учета**, затем выберите **Вставить**.</span><span class="sxs-lookup"><span data-stu-id="f3e54-147">If the **Ledger transaction type** column isn't visible, right-click anywhere in the grid row that shows the column names, select **Add columns**, select **Ledger transaction type** and then select **Insert**.</span></span>
