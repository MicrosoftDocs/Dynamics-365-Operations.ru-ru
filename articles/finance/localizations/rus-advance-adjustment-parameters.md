---
title: Переоценка в иностранной валюте для подотчетных лиц (Россия)
description: В этой теме содержится информация о переоценке в иностранной валюте для подотчетных лиц в России.
author: ilkond
ms.date: 09/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Russia
ms.author: roschlom
ms.dyn365.ops.version: 8.0999999999999996
ms.search.validFrom: 2018-10-31
ms.openlocfilehash: 5152612b5c12f7920c005e609c4e85835d5ceaa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822737"
---
# <a name="revaluate-foreign-currency-for-advance-holders-russia"></a><span data-ttu-id="197d2-103">Переоценка в иностранной валюте для подотчетных лиц (Россия)</span><span class="sxs-lookup"><span data-stu-id="197d2-103">Revaluate foreign currency for advance holders (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="197d2-104">В этой теме содержится информация о переоценке в иностранной валюте для подотчетных лиц в России.</span><span class="sxs-lookup"><span data-stu-id="197d2-104">This topic provides information about foreign currency revaluation for advance holders in Russia.</span></span>

<span data-ttu-id="197d2-105">При сопоставлении авансовых платежей и авансовых отчетов, которые включают проводки в иностранных валютах, создаются проводки корректировки как продолжение авансового отчета на основе настроек на странице **Параметры авансовой разницы**.</span><span class="sxs-lookup"><span data-stu-id="197d2-105">When you settle advance payments and advance reports that include transactions that were done in foreign currencies, adjustment transactions are created as a continuation of the advance report, based on the setup on the **Advance adjustment parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="197d2-106">Для открытых авансовых проводок, которые были выписаны или получены в иностранной валюте, курсовую разницу больше не требуется рассчитывать в бухгалтерском учете.</span><span class="sxs-lookup"><span data-stu-id="197d2-106">For open advance transactions that are issued or received in foreign currencies, exchange adjustments no longer have to be calculated in business accounting.</span></span>

<span data-ttu-id="197d2-107">Выполните следующие действия, чтобы настроить параметры корректировки аванса для подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="197d2-107">Follow these steps to set up advance adjustment parameters for advance holders.</span></span>

1. <span data-ttu-id="197d2-108">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="197d2-108">Go to **General ledger** \> **Ledger setup** \> **Advance adjustment parameters**.</span></span>
2. <span data-ttu-id="197d2-109">На экспресс-вкладке **Закупки/подотчетные лица** в поле **Разноска ГК** выберите тип разноски ГК:</span><span class="sxs-lookup"><span data-stu-id="197d2-109">On the **Purchases/Advance holders** FastTab, in the **Ledger posting** field, select the type of ledger posting:</span></span>

    - <span data-ttu-id="197d2-110">**Счета-фактуры** — корректировка аванса, которая получается в результате сопоставления аванса и авансового отчета для подотчетного лица, должна быть продолжением авансового отчета.</span><span class="sxs-lookup"><span data-stu-id="197d2-110">**Invoice accounts** – The advance adjustment that is produced by the settlement of an advance and an advance report for the advance holder should be a continuation of the advance report.</span></span>
    - <span data-ttu-id="197d2-111">**Счет отклонения стоимости товара** — расчет должен обрабатываться на основе параметров счета для отклонения, и корректировка аванса не должна являться продолжением авансового отчета.</span><span class="sxs-lookup"><span data-stu-id="197d2-111">**Deviation from the cost price** – The calculation should be processed based on the account's settings for deviation, and the advance adjustment should not be a continuation of the advance report.</span></span> <span data-ttu-id="197d2-112">В зависимости от типа корректировки аванса используются конкретные счета ГК для корректировки авансовых платежей.</span><span class="sxs-lookup"><span data-stu-id="197d2-112">Depending on the type of advance adjustment, specific ledger accounts are used to adjust the advance payments.</span></span>

4. <span data-ttu-id="197d2-113">В поле **Реализованный убыток** выберите счет ГК для разноски убытка по валютному курсу для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="197d2-113">In the **Realized loss** field, select the ledger account to post an exchange rate loss for an employee to.</span></span>
5. <span data-ttu-id="197d2-114">В поле **Реализованная прибыль** выберите счет ГК для разноски прибыли по валютному курсу для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="197d2-114">In the **Realized gain** field, select the ledger account to post an exchange rate profit for an employee to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="197d2-115">Счета реализованного убытка и реализованной прибыли используются для корректировки авансовых платежей, только если запасы закрыты.</span><span class="sxs-lookup"><span data-stu-id="197d2-115">The realized loss and realized gain accounts are used to adjust advance payments only if the inventory is closed.</span></span>

6. <span data-ttu-id="197d2-116">В поле **Код расхода** выберите код расходов налоговой аналитики.</span><span class="sxs-lookup"><span data-stu-id="197d2-116">In the **Expense code** field, select a tax dimension expense code.</span></span>
7. <span data-ttu-id="197d2-117">В поле **Код выручки** выберите код выручки налоговой аналитики.</span><span class="sxs-lookup"><span data-stu-id="197d2-117">In the **Revenue code** field, select a tax dimension revenue code.</span></span>
8. <span data-ttu-id="197d2-118">В поле **Авансовая разница - расход** выберите счет ГК для разноски убытков корректировки аванса в налоговом учете.</span><span class="sxs-lookup"><span data-stu-id="197d2-118">In the **Advance adjustment - loss** field, select the ledger account to post an advance adjustment loss in tax accounting to.</span></span>
9. <span data-ttu-id="197d2-119">В поле **Авансовая разница - доход** выберите счет ГК для разноски дохода корректировки аванса в налоговом учете.</span><span class="sxs-lookup"><span data-stu-id="197d2-119">In the **Advance adjustment - profit** field, select the ledger account to post an advance adjustment profit in tax accounting to.</span></span>
10. <span data-ttu-id="197d2-120">В поле **Корр. счет для авансовой разницы** выберите корр. счет ГК для разноски дохода корректировки аванса в налоговом учете.</span><span class="sxs-lookup"><span data-stu-id="197d2-120">In the **Advance adjustment offset account** field, select the offset ledger account to post an advance adjustment in tax accounting to.</span></span>
11. <span data-ttu-id="197d2-121">Выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="197d2-121">Select **Save**.</span></span>

<span data-ttu-id="197d2-122">Выполните эти действия для расчета корректировки валютного курса для подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="197d2-122">Follow these steps to calculate the exchange rate adjustment for advance holders.</span></span>

1. <span data-ttu-id="197d2-123">Выберите **Расчеты с поставщиками** \> **Периодические задачи** \> **Подотчетные лица** \> **Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="197d2-123">Go to **Accounts payable** \> **Periodic tasks** \> **Advance holders** \> **Foreign currency revaluation**.</span></span>
2. <span data-ttu-id="197d2-124">Выберите **Переоценка в иностранной валюте**, чтобы открыть диалоговое окно **Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="197d2-124">Select **Foreign currency revaluation** to open the **Foreign currency revaluation** dialog box.</span></span>
3. <span data-ttu-id="197d2-125">В поле **Метод** выберите вариант **Стандартная**.</span><span class="sxs-lookup"><span data-stu-id="197d2-125">In the **Method** field, select **Standard**.</span></span>
4. <span data-ttu-id="197d2-126">В поле **Фиксированная дата** выберите дату, на которую должна быть выполнена проводка в главной книге.</span><span class="sxs-lookup"><span data-stu-id="197d2-126">In the **Considered date** field, select the date that the general ledger transaction should be made by.</span></span>
5. <span data-ttu-id="197d2-127">В поле **Дата курса** выберите дату, определяющую валютный курс, используемый для вычисления корректировки на курсовую разницу.</span><span class="sxs-lookup"><span data-stu-id="197d2-127">In the **Date of rate** field, select the date that determines the currency exchange rate that is used to compute the exchange rate adjustment.</span></span> <span data-ttu-id="197d2-128">Если оставить это поле пустым, используется курс, действовавший на дату, указанную в поле **Фиксированная дата**.</span><span class="sxs-lookup"><span data-stu-id="197d2-128">If you leave this field blank, the rate that is in effect on the date in the **Considered date** field is used.</span></span>
6. <span data-ttu-id="197d2-129">В поле **Описание** введите текст, который должен отображаться в проводке корректировки курсовой разницы.</span><span class="sxs-lookup"><span data-stu-id="197d2-129">In the **Description** field, enter the text that should appear in the exchange rate adjustment transaction.</span></span>
7. <span data-ttu-id="197d2-130">В поле **Использовать профиль разноски из** выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="197d2-130">In the **Use posting profile from** field, select one of the following values:</span></span>

    - <span data-ttu-id="197d2-131">**Разноска** — после выполнения операции переоценки счет задолженности для подотчетного лица выбирается из профиля разноски первичной операции.</span><span class="sxs-lookup"><span data-stu-id="197d2-131">**Posting** – When a revaluation operation is done, the debt account for an advance holder is selected from the posting profile of the primary operation.</span></span>
    - <span data-ttu-id="197d2-132">**Выбрать** — после выполнения операции переоценки счет задолженности для подотчетного лица выбирается из профиля разноски, который выбран в поле **Профиль разноски**.</span><span class="sxs-lookup"><span data-stu-id="197d2-132">**Select** – When a revaluation operation is done, the debt account for an advance holder is selected from the posting profile that is selected in the **Posting profile** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="197d2-133">Корректировка курсовой разницы выполняется для счета, который указан в выбранном профиле разноски.</span><span class="sxs-lookup"><span data-stu-id="197d2-133">The exchange rate adjustment is done for the account that is specified in the selected posting profile.</span></span> <span data-ttu-id="197d2-134">Она не делается для счета, определенного в первичной операции.</span><span class="sxs-lookup"><span data-stu-id="197d2-134">It isn't done for the account that is specific in the primary operation.</span></span>

8. <span data-ttu-id="197d2-135">Поле **Аналитика** определяет способ создания аналитики в проводке корректировки валютного курса.</span><span class="sxs-lookup"><span data-stu-id="197d2-135">The **Dimension** field determines how the dimension is generated in the exchange rate adjustment transaction.</span></span> <span data-ttu-id="197d2-136">Выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="197d2-136">Select one of the following values:</span></span>

    - <span data-ttu-id="197d2-137">**Нет** — аналитика отсутствует в записи для прогноза корректировки валютного курса.</span><span class="sxs-lookup"><span data-stu-id="197d2-137">**No** – The dimension is absent in the entry for the exchange rate adjustment forecast.</span></span>
    - <span data-ttu-id="197d2-138">**Разноска** — аналитика наследуется из проводок для подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="197d2-138">**Posting** – The dimension is inherited from the transactions for an advance holder.</span></span>
    - <span data-ttu-id="197d2-139">**Таблица** — в проводке для прогноза корректировки валютного курса аналитика наследуется из карты подотчетного лица, если только эта аналитика не назначена для налогового учета.</span><span class="sxs-lookup"><span data-stu-id="197d2-139">**Table** – In the transaction for the exchange rate adjustment forecast, the dimension is inherited from the advance holder card, unless the dimension is designated for tax accounting.</span></span>

9. <span data-ttu-id="197d2-140">На экспресс-вкладке **Включаемые записи** можно определить дополнительную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="197d2-140">On the **Records to include** FastTab, you can define additional filtering.</span></span>
10. <span data-ttu-id="197d2-141">Выберите **OK** для вычисления корректировки валютных курсов.</span><span class="sxs-lookup"><span data-stu-id="197d2-141">Select **OK** to calculate the exchange rates adjustment.</span></span>

<span data-ttu-id="197d2-142">После завершения расчета создается новая строка для корректировки курсовой разницы на странице **Переоценка в иностранной валюте** в соответствии с критериями, которые указаны.</span><span class="sxs-lookup"><span data-stu-id="197d2-142">After the calculation is completed, a new line for the exchange adjustment is generated on the **Foreign currency revaluation** page, based on the criteria that you specified.</span></span> <span data-ttu-id="197d2-143">Теперь имеется возможность выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="197d2-143">You can now perform the following actions:</span></span>

- <span data-ttu-id="197d2-144">Выберите **Ваучер**, чтобы открыть страницу **Проводки ваучера**, где можно просмотреть проводки, которые были выполнены в главной книге.</span><span class="sxs-lookup"><span data-stu-id="197d2-144">Select **Voucher** to open the **Voucher transactions** page, where you can review the transactions that were completed for the general ledger.</span></span>
- <span data-ttu-id="197d2-145">Выберите **Проводки**, чтобы открыть страницу **Проводки по подотчетным лицам**, где можно просмотреть проводки, которые были выполнены для подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="197d2-145">Select **Transactions** to open the **Advance holder transactions** page, where you can review the transactions that were completed for the advance holder.</span></span>
- <span data-ttu-id="197d2-146">Выберите **Проверено**, чтобы пометить выбранную строку как проверенную.</span><span class="sxs-lookup"><span data-stu-id="197d2-146">Select **Reviewed** to mark the selected line as reviewed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]