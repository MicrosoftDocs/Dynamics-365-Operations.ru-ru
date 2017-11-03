---
title: "Рабочая область управления банками"
description: "В этой теме содержится информация о рабочей области управления банками. В этой рабочей области отображаются сведения, которые связаны с банковскими счетами компании, представление сводки и страница аналитики. Представление сводки показывает сводные плитки, сведения о банковском счете, диаграмму сальдо и связанные данные. Страницы аналитики использует возможности Microsoft Power BI для отображения визуальных объектов, которые относятся к сальдо банковского счета."
author: saraschi2
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5d9f9aab56441a7ecd2407b5571de77ece2ab3f
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---
# <a name="bank-management-workspace"></a><span data-ttu-id="32dbc-106">Рабочая область управления банками</span><span class="sxs-lookup"><span data-stu-id="32dbc-106">Bank management workspace</span></span>

<span data-ttu-id="32dbc-107">Рабочая область **Управление банками** содержит сведения, которые связаны с банковскими счетами компании.</span><span class="sxs-lookup"><span data-stu-id="32dbc-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="32dbc-108">Эта рабочая область содержит представление **Сводка** и страницу **Аналитика**.</span><span class="sxs-lookup"><span data-stu-id="32dbc-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="32dbc-109">Представление **Сводка** показывает сводные плитки, сведения о банковском счете, диаграмму сальдо и связанные данные.</span><span class="sxs-lookup"><span data-stu-id="32dbc-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="32dbc-110">Страница **Аналитика** использует возможности Microsoft Power BI для отображения визуальных объектов, которые относятся к сальдо банковского счета.</span><span class="sxs-lookup"><span data-stu-id="32dbc-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="32dbc-111">Представление "Сводка"</span><span class="sxs-lookup"><span data-stu-id="32dbc-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="32dbc-112">Сводка</span><span class="sxs-lookup"><span data-stu-id="32dbc-112">Summary</span></span>

<span data-ttu-id="32dbc-113">Плитки в разделе **Сводка** дают общий обзор банковских счетов и обеспечивают быстрый доступ к страницам, которые чаще всего используются.</span><span class="sxs-lookup"><span data-stu-id="32dbc-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="32dbc-114">Сведения о банковской выверке относятся только к функциям расширенной банковской выверки.</span><span class="sxs-lookup"><span data-stu-id="32dbc-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="32dbc-115">Сведения включается только для тех банковских счетов, для которых параметр **Расширенная банковская выверка** задан как **Да** на странице **Банковский счет**.</span><span class="sxs-lookup"><span data-stu-id="32dbc-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="32dbc-116">В разделе **Сводка** можно импортировать электронные банковские файлы для банковских счетов во всех юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="32dbc-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="32dbc-117">Банковские счета</span><span class="sxs-lookup"><span data-stu-id="32dbc-117">Bank accounts</span></span>

<span data-ttu-id="32dbc-118">Каждый банковский счет юридического лица представлен карточкой в разделе **Банковский счет**.</span><span class="sxs-lookup"><span data-stu-id="32dbc-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="32dbc-119">Отображается текущее сальдо и можно выполнить детализацию до проводок, которые составляют эту сумму в итоговом сальдо.</span><span class="sxs-lookup"><span data-stu-id="32dbc-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="32dbc-120">Сумма **Проводка по промежуточному счету** также позволяет детализировать до проводок, которые составляют эту сводную сумму.</span><span class="sxs-lookup"><span data-stu-id="32dbc-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="32dbc-121">Проводки по промежуточному счету — это ожидающие проводки, которые были разнесены с помощью функций промежуточной проводки, но еще не были очищены.</span><span class="sxs-lookup"><span data-stu-id="32dbc-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="32dbc-122">Сумма **Ожидающее сальдо** — это текущее сальдо за вычетом промежуточных или ожидающих проводок.</span><span class="sxs-lookup"><span data-stu-id="32dbc-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="32dbc-123">Карта также показывает последнюю выверку банковского счета.</span><span class="sxs-lookup"><span data-stu-id="32dbc-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="32dbc-124">Эта информация отображается, только если расширенная банковская выверка включена для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="32dbc-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="32dbc-125">Баланс</span><span class="sxs-lookup"><span data-stu-id="32dbc-125">Balance</span></span>

<span data-ttu-id="32dbc-126">Диаграмма **Сальдо** отображает либо исторические сведения по сальдо для банковского счета, выбранного в разделе **Банковские счета**, либо сводку по историческим сведениям по сальдо для всех банковских счетов юридического лица.</span><span class="sxs-lookup"><span data-stu-id="32dbc-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="32dbc-127">Эта информация доступна для различных периодов: текущая неделя, текущий месяц, текущий год, последние пять лет и все периоды (полная история банковского счета).</span><span class="sxs-lookup"><span data-stu-id="32dbc-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="32dbc-128">При просмотре диаграммы **Сальдо** для одного банковского счета исторические данные по сальдо отображаются в валюте банковского счета.</span><span class="sxs-lookup"><span data-stu-id="32dbc-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="32dbc-129">При просмотре диаграммы для всех банковских счетов юридического лица исторические данные по сальдо отображаются в валюте учета.</span><span class="sxs-lookup"><span data-stu-id="32dbc-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="32dbc-130">Сведения о последнем обновлении данных отображаются в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="32dbc-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="32dbc-131">Можно обновить данные по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="32dbc-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="32dbc-132">Связанные сведения</span><span class="sxs-lookup"><span data-stu-id="32dbc-132">Related information</span></span>

<span data-ttu-id="32dbc-133">В разделе **Связанные сведения** можно открыть страницу **Общий журнал**, чтобы выполнить банковские переводы.</span><span class="sxs-lookup"><span data-stu-id="32dbc-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="32dbc-134">Можно также быстро открыть страницы **Банковские проводки** и **Проводки по промежуточному счету**.</span><span class="sxs-lookup"><span data-stu-id="32dbc-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="32dbc-135">Представление аналитики</span><span class="sxs-lookup"><span data-stu-id="32dbc-135">Analytics view</span></span>

<span data-ttu-id="32dbc-136">На странице **Аналитика** содержатся важные показатели банковских счетов в текущей компании.</span><span class="sxs-lookup"><span data-stu-id="32dbc-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="32dbc-137">На странице доступны следующие возможности визуализации.</span><span class="sxs-lookup"><span data-stu-id="32dbc-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="32dbc-138">Обще банковское сальдо в валюте системы</span><span class="sxs-lookup"><span data-stu-id="32dbc-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="32dbc-139">Сальдо по юридическому лицу</span><span class="sxs-lookup"><span data-stu-id="32dbc-139">Balance by legal entity</span></span>
-   <span data-ttu-id="32dbc-140">Фактическое и прогнозируемое сальдо на сегодня в валюте банковского счета</span><span class="sxs-lookup"><span data-stu-id="32dbc-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="32dbc-141">Сальдо по банковскому счету</span><span class="sxs-lookup"><span data-stu-id="32dbc-141">Balance by bank account</span></span>
-   <span data-ttu-id="32dbc-142">Сальдо по валютам</span><span class="sxs-lookup"><span data-stu-id="32dbc-142">Balance by currency</span></span>

<span data-ttu-id="32dbc-143">Можно просмотреть аналитики банка для всех компаний в рабочей области **Обзор кассы — все компании**.</span><span class="sxs-lookup"><span data-stu-id="32dbc-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>

