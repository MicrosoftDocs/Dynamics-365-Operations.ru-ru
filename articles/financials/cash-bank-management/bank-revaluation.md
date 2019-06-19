---
title: Банковская переоценка в иностранной валюте
description: В этом разделе представлен обзор процесса банковской переоценки в иностранной валюте. Сюда входят сведения о настройке, запуске процесса, расчете для процесса и реверсировании проводок переоценки.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 353153a3a5cbcb27749f21582fcf83ac4f3a8f36
ms.sourcegitcommit: 56ec43e459ba93f495bc76fed23d6737218ef37e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "1591768"
---
# <a name="bank-foreign-currency-revaluation"></a><span data-ttu-id="51cef-104">Банковская переоценка в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="51cef-104">Bank foreign currency revaluation</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="51cef-105">В этом разделе представлен обзор процесса банковской переоценки в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-105">This topic provides an overview of the process of bank foreign currency revaluation.</span></span> <span data-ttu-id="51cef-106">Объясняется, как настроить и запустить процесс, а также предоставляется информация о расчете для процесса.</span><span class="sxs-lookup"><span data-stu-id="51cef-106">It explains how to set up and run the process, and provides information about the calculation for the process.</span></span> <span data-ttu-id="51cef-107">Здесь также объясняется порядок сторнирования проводок переоценки в случае необходимости отмены.</span><span class="sxs-lookup"><span data-stu-id="51cef-107">It also explains how to reverse revaluation transactions, if reversal is required.</span></span>

<span data-ttu-id="51cef-108">Как часть конца периода, учетные соглашения требуют, чтобы сальдо банковских счетов в иностранных валютах были переоценены с использованием различных типов валютного курса (текущий, исторический, средний и т. п.).</span><span class="sxs-lookup"><span data-stu-id="51cef-108">As part of a period end, accounting conventions require that bank account balances in foreign currencies be revalued by using different exchange rate types (current, historical, average, and so on).</span></span> <span data-ttu-id="51cef-109">Функция банковской переоценки иностранной валюты может использоваться для переоценки одного или нескольких банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="51cef-109">The bank foreign currency revaluation feature can be used to revalue one or more bank accounts.</span></span> <span data-ttu-id="51cef-110">Эта функция также является глобальной функцией.</span><span class="sxs-lookup"><span data-stu-id="51cef-110">The feature is also a global feature.</span></span> <span data-ttu-id="51cef-111">Таким образом, с одной страницы можно выполнить банковскую переоценку во всех юридических лицах, к которым вы имеете доступ.</span><span class="sxs-lookup"><span data-stu-id="51cef-111">Therefore, from a single page, you can revalue banks across all the legal entities that you have access to.</span></span>

> [!NOTE]
> <span data-ttu-id="51cef-112">При выполнении переоценки будет произведена переоценка сальдо на каждом банковском счете, разнесенном в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-112">When you run the revaluation process, the balance in each bank account that is posted in a foreign currency will be revalued.</span></span> <span data-ttu-id="51cef-113">Проводки внереализационной прибыли и убытка, которые созданы во время процесса переоценки, произведены системой.</span><span class="sxs-lookup"><span data-stu-id="51cef-113">The unrealized gain or loss transactions that are created during the revaluation process are system-generated.</span></span> <span data-ttu-id="51cef-114">Две проводки могут быть созданы, одна для валюты учета и одна для валюты отчетности, если требуется валюта отчетности.</span><span class="sxs-lookup"><span data-stu-id="51cef-114">Two transactions might be created, one for the accounting currency and one for the reporting currency, if a reporting currency is relevant.</span></span> <span data-ttu-id="51cef-115">Каждая учетная запись будет разнесена во внереализационную прибыль или убыток и переоцениваемый счет ГК.</span><span class="sxs-lookup"><span data-stu-id="51cef-115">Each accounting entry will be posted to the unrealized gain or loss and the main account that is being revalued.</span></span>

## <a name="prepare-to-run-foreign-currency-revaluation"></a><span data-ttu-id="51cef-116">Подготовка выполнения переоценки в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="51cef-116">Prepare to run foreign currency revaluation</span></span>

<span data-ttu-id="51cef-117">Прежде чем вы выполнить процесс переоценки, требуется следующая настройка.</span><span class="sxs-lookup"><span data-stu-id="51cef-117">Before you run the revaluation process, the following setup is required.</span></span>

- <span data-ttu-id="51cef-118">На странице **Книга учета** определите тип обменного курса.</span><span class="sxs-lookup"><span data-stu-id="51cef-118">On the **Ledger** page, specify the exchange rate type.</span></span> <span data-ttu-id="51cef-119">Если тип валютного курса не указан для счета ГК, этот тип валютного курса используется во время переоценки в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-119">If an exchange rate type isn't defined on the main account, this exchange rate type is used during foreign currency revaluation.</span></span>
- <span data-ttu-id="51cef-120">На странице **Книга учета**, определите реализованная прибыль, реализованный убыток, внереализационная прибыль, и внереализационный убыток для переоценки в валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-120">On the **Ledger** page, specify the realized gain, realized loss, unrealized gain, and unrealized loss accounts for currency revaluation.</span></span> <span data-ttu-id="51cef-121">Счета реализованной прибыли и реализованных убытков используются при сопоставлении проводок расчетов с клиентами и расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="51cef-121">Realized gain and realized loss accounts are used when Accounts receivable and Accounts payable transactions are settled.</span></span> <span data-ttu-id="51cef-122">Счета нереализованной прибыли и нереализованных убытков используются для переоценки открытых проводок и главных счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="51cef-122">Unrealized gain and unrealized loss accounts are used to revalue open transactions and general ledger main accounts.</span></span>
- <span data-ttu-id="51cef-123">На странице **Счета валютной переоценки** выберите различные счета валютной переоценки для каждой валюты и компании.</span><span class="sxs-lookup"><span data-stu-id="51cef-123">On the **Currency revaluation accounts** page, select different currency revaluation accounts for each currency and company.</span></span> <span data-ttu-id="51cef-124">Если никакой счета не определены, используются счета со страницы **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="51cef-124">If no accounts are defined, the accounts from the **Ledger** page are used.</span></span>

## <a name="enable-foreign-currency-revaluation"></a><span data-ttu-id="51cef-125">Включение переоценки в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="51cef-125">Enable foreign currency revaluation</span></span>

<span data-ttu-id="51cef-126">Перед обработкой переоценки в иностранной валюте необходимо включить функцию банковской переоценки иностранной валюты.</span><span class="sxs-lookup"><span data-stu-id="51cef-126">You must turn on the bank foreign currency revaluation feature before you can process foreign currency revaluations.</span></span>

1. <span data-ttu-id="51cef-127">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="51cef-127">Go to **Cash and bank management \> Setup \> Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="51cef-128">На вкладке **Общие** в области **Переоценка в иностранной валюте**, установите для параметра **Включить банковскую переоценку** значение **Да**, чтобы включить функцию для текущего юридического лица.</span><span class="sxs-lookup"><span data-stu-id="51cef-128">On the **General** tab, under **Foreign currency revaluation**, set the **Enable bank revaluation** option to **Yes** to turn on the feature for the current legal entity.</span></span> 
3. <span data-ttu-id="51cef-129">На вкладке **Номерные серии** добавьте номерную серию для переоценки в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-129">On the **Number sequences** tab, add a number sequence for foreign currency revaluation.</span></span>
4. <span data-ttu-id="51cef-130">Обновите обозреватель, чтобы увидеть пункт **Переоценка в иностранной валюте** в разделе **Периодические задачи** страницы области.</span><span class="sxs-lookup"><span data-stu-id="51cef-130">Refresh the browser to see **Foreign currency revaluation** in the **Periodic tasks** section of the area page.</span></span>

<span data-ttu-id="51cef-131">Необходимо включить функцию для каждого юридического лица, в котором будет использоваться переоценка в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-131">You must turn on the feature for every legal entity that will use foreign currency revaluation.</span></span> <span data-ttu-id="51cef-132">Если вы назначены роли системного администратора или диспетчера функций, вы можете исключить этот шаг, включив функцию с именем **Включить банковскую переоценку без параметра** в рабочей области **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="51cef-132">If you are assigned to the System Administrator role or Feature Manager role, you can eliminate this step by enabling the feature named **Enable bank revaluation without a parameter** in the **Feature management** workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="51cef-133">Если юридическое лицо использует русский, венгерский или польский код страны/региона, уже можно выполнять банковскую переоценку в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-133">If your legal entity uses a Russian, Polish, or Hungarian country/region code, you can already do bank foreign currency revaluation.</span></span> <span data-ttu-id="51cef-134">Будет нельзя использовать переоценку в иностранной валюте, которая используется в других странах или регионах.</span><span class="sxs-lookup"><span data-stu-id="51cef-134">You won't be able to use the foreign currency revaluation that is used by other countries or regions.</span></span>

## <a name="process-foreign-currency-revaluation"></a><span data-ttu-id="51cef-135">Обработка переоценки в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="51cef-135">Process foreign currency revaluation</span></span>

<span data-ttu-id="51cef-136">После завершения настройки используйте страницу **Переоценка в иностранной валюте** в разделе управления банком и кассовыми операциями, чтобы переоценить сальдо одного или нескольких банковских счетов во всех юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="51cef-136">After the setup is completed, use the **Foreign currency revaluation** page in Cash and bank management to revalue the balances of one or more bank accounts across all legal entities.</span></span> <span data-ttu-id="51cef-137">Вы можете выполнить процесс в реальном времени или можно запланировать его выполнение с использованием пакета.</span><span class="sxs-lookup"><span data-stu-id="51cef-137">You can run the process in real time, or you can schedule it to run by using a batch.</span></span>

<span data-ttu-id="51cef-138">На странице **Переоценка в иностранной валюте** отображается журнал каждого процесса переоценки.</span><span class="sxs-lookup"><span data-stu-id="51cef-138">The **Foreign currency revaluation** page shows the history of each revaluation process.</span></span> <span data-ttu-id="51cef-139">Он показывает, когда процесс был выполнен и какие критерии были определены, и предоставляет ссылку на ваучер, созданный для переоценки.</span><span class="sxs-lookup"><span data-stu-id="51cef-139">It shows when the process was run and what criteria were defined, and provides a link to the voucher that was created for the revaluation.</span></span> <span data-ttu-id="51cef-140">Он также показывает, была ли сторнирована предыдущая переоценка.</span><span class="sxs-lookup"><span data-stu-id="51cef-140">It also shows whether a previous revaluation was reversed.</span></span> <span data-ttu-id="51cef-141">Чтобы запустить процесс переоценки, выберите **Переоценка в иностранной валюте** в области действий, чтобы открыть диалоговое окно **Банк - Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="51cef-141">To run the revaluation process, select **Foreign currency revaluation** on the Action Pane to open the **Bank - foreign currency revaluation** dialog box.</span></span>

<span data-ttu-id="51cef-142">Поле **Дата переоценки** определяет дату отсечки для расчета сальдо в иностранной валюте, которое будет переоцениваться.</span><span class="sxs-lookup"><span data-stu-id="51cef-142">The **Revaluation date** field defines the cutoff date for calculating the foreign currency balance that will be revalued.</span></span> <span data-ttu-id="51cef-143">Сумма по всем банковским проводкам, произведенным вплоть до этой даты, переоценивается.</span><span class="sxs-lookup"><span data-stu-id="51cef-143">The sum of all bank transactions that occurred up through this date is revalued.</span></span>

<span data-ttu-id="51cef-144">Поле **Дата валютного курса** определяет дату валютного курса, который будет использоваться для переоценки сальдо.</span><span class="sxs-lookup"><span data-stu-id="51cef-144">The **Exchange rate date** field defines the date of the exchange rate that will be used to revalue the currency balances.</span></span> <span data-ttu-id="51cef-145">Например, вы можете переоценить сальдо по состоянию на 31 января, но использовать валютный курс, который определен для 1 февраля.</span><span class="sxs-lookup"><span data-stu-id="51cef-145">For example, you can revalue the balances as of January 31 but use the exchange rate that is defined for February 1.</span></span>

<span data-ttu-id="51cef-146">Процесс переоценки может выполняться для одного или нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="51cef-146">The revaluation process can be run for one or more legal entities.</span></span> <span data-ttu-id="51cef-147">Поиск показывает только юридические лица, к которым имеется доступ.</span><span class="sxs-lookup"><span data-stu-id="51cef-147">The lookup shows only the legal entities that you have access to.</span></span> <span data-ttu-id="51cef-148">Выберите юридические лица, для которых вы хотите выбрать банковские счета, для которые требуется переоценка в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-148">Select the legal entities for which you want to select the bank accounts that are eligible for foreign currency revaluation.</span></span> <span data-ttu-id="51cef-149">В сетке будут отображаться все банковские счета для этих юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="51cef-149">All the bank accounts for those legal entities will be shown in the grid.</span></span>

<span data-ttu-id="51cef-150">Задайте для параметра **Просмотр перед разноской** значение **Да**, если вы хотите просматривать результаты переоценки перед их разноской.</span><span class="sxs-lookup"><span data-stu-id="51cef-150">Set the **Preview before posting** option to **Yes** if you want to review the results of the revaluation before you post it.</span></span> <span data-ttu-id="51cef-151">Переоценка в иностранной валюте имеет просмотр, который может быть разнесен.</span><span class="sxs-lookup"><span data-stu-id="51cef-151">The foreign currency revaluation has a preview that can be posted.</span></span> <span data-ttu-id="51cef-152">Не нужно снова запускать процесс переоценки.</span><span class="sxs-lookup"><span data-stu-id="51cef-152">You don't have to run the revaluation process again.</span></span> <span data-ttu-id="51cef-153">Можно экспортировать результаты предварительного просмотра в Microsoft Excel, чтобы сохранить историю того, как эти суммы были рассчитаны.</span><span class="sxs-lookup"><span data-stu-id="51cef-153">You can export the results in the preview to Microsoft Excel to keep a history of how the amounts were calculated.</span></span> <span data-ttu-id="51cef-154">Вы не можете использовать пакетную обработку, если необходимо предварительно просматривать результаты переоценки.</span><span class="sxs-lookup"><span data-stu-id="51cef-154">You can't use batch processing if you want to preview the results of the revaluation.</span></span>

<span data-ttu-id="51cef-155">Выберите **ОК** для выполнения переоценки в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="51cef-155">Select **OK** to process the foreign currency revaluation.</span></span> <span data-ttu-id="51cef-156">Запись создается для отслеживания истории каждого выполнения.</span><span class="sxs-lookup"><span data-stu-id="51cef-156">A record is created to track the history of each run.</span></span> <span data-ttu-id="51cef-157">Отдельная запись создается для каждого юридического лица и слоя разноски.</span><span class="sxs-lookup"><span data-stu-id="51cef-157">A separate record is created for each legal entity and posting layer.</span></span>

## <a name="calculate-unrealized-gainloss"></a><span data-ttu-id="51cef-158">Расчет внереализационной прибыли/убытка</span><span class="sxs-lookup"><span data-stu-id="51cef-158">Calculate unrealized gain/loss</span></span>

<span data-ttu-id="51cef-159">В окне управление банком и кассовыми операциями валюта банка рассматривается как основная валюта и не переоценивается.</span><span class="sxs-lookup"><span data-stu-id="51cef-159">In Cash and bank management, the bank currency is considered to be the base currency and it is not revalued.</span></span> <span data-ttu-id="51cef-160">Сальдо банковского счета в валюте учета переоценивается с использованием валютных курсов между валютой банка и валютой учета на дату **Дата валютного курса**.</span><span class="sxs-lookup"><span data-stu-id="51cef-160">The balance of the bank account in the accounting currency is revalued using the exchange rates between the bank currency and the accounting currency on the **Exchange rate date**.</span></span> <span data-ttu-id="51cef-161">Сальдо банковского счета в валюте отчетности также переоценивается с использованием валютных курсов между валютой банка и валютой отчетности на дату **Дата валютного курса**.</span><span class="sxs-lookup"><span data-stu-id="51cef-161">The balance of the bank account in the reporting currency is also revalued using the exchange rates between the bank currency and the reporting currency on the **Exchange rate date**.</span></span>

<span data-ttu-id="51cef-162">Создается проводка для разницы между сальдо банковского счета и новое сальдо, которое вычисляется для валюты учета.</span><span class="sxs-lookup"><span data-stu-id="51cef-162">A transaction is created for the difference between the balance of the bank account and the new balance that is calculated for the accounting currency.</span></span> <span data-ttu-id="51cef-163">Создается другая проводка для разницы между сальдо банковского счета и новое сальдо, которое вычисляется для валюты отчетности.</span><span class="sxs-lookup"><span data-stu-id="51cef-163">Another transaction is created for the difference between the balance of the bank account and the new balance that is calculated for the reporting currency.</span></span> <span data-ttu-id="51cef-164">Записи для этих проводок помечаются как выверенные.</span><span class="sxs-lookup"><span data-stu-id="51cef-164">The entries for these transactions are marked as reconciled.</span></span> 

<span data-ttu-id="51cef-165">Запись не создается для валюты учета, если валюта банка соответствует валюте учета.</span><span class="sxs-lookup"><span data-stu-id="51cef-165">No entry is made for the accounting currency if the bank currency matches the accounting currency.</span></span> <span data-ttu-id="51cef-166">Аналогично, запись не создается для валюты отчетности, если валюта банка соответствует валюте отчетности.</span><span class="sxs-lookup"><span data-stu-id="51cef-166">Likewise, no entry is made for the reporting currency if the bank currency matches the reporting currency.</span></span>

<span data-ttu-id="51cef-167">Проводка переоценки в иностранной валюте также делится на аналитики, которые найдены в банковских проводок.</span><span class="sxs-lookup"><span data-stu-id="51cef-167">The foreign currency revaluation transaction is also split across the dimensions that are found on the bank transactions.</span></span> <span data-ttu-id="51cef-168">Разбиение зависит от сальдо для каждой аналитики.</span><span class="sxs-lookup"><span data-stu-id="51cef-168">The split is based on the balance for each dimension.</span></span> <span data-ttu-id="51cef-169">Например, общее банковское сальдо равно 10 000, но сальдо для подразделения 001 равно 4 000, а сальдо для подразделения 002 равно 6 000.</span><span class="sxs-lookup"><span data-stu-id="51cef-169">For example, the total bank balance is 10,000, but the balance for business unit 001 is 4,000, whereas the balance for business unit 002 is 6,000.</span></span> <span data-ttu-id="51cef-170">В этом случае 40 процентов от суммы переоценки разносится на счет переоценки с подразделением 001 и 60 процентов разносится для счета переоценки с подразделением 002.</span><span class="sxs-lookup"><span data-stu-id="51cef-170">In this case, 40 percent of the revaluation amount is posted to the revaluation account that has business unit 001, and 60 percent is posted to the revaluation account that has business unit 002.</span></span> <span data-ttu-id="51cef-171">Если структуры счетов не включает подразделение, вся сумма разносится на счет переоценки.</span><span class="sxs-lookup"><span data-stu-id="51cef-171">If the account structure doesn't include a business unit, the full amount is posted to the revaluation account.</span></span>

## <a name="reverse-foreign-currency-revaluation"></a><span data-ttu-id="51cef-172">Реверсировать переоценку в иностранной валюте</span><span class="sxs-lookup"><span data-stu-id="51cef-172">Reverse foreign currency revaluation</span></span>

<span data-ttu-id="51cef-173">Если необходимо реверсировать проводку переоценки, выберите кнопку **Сторнировать проводку** на панели действий страницы **Переоценка в иностранной валюте**.</span><span class="sxs-lookup"><span data-stu-id="51cef-173">If you must reverse the revaluation transaction, select **Reverse transaction** on the Action Pane of the **Foreign currency revaluation** page.</span></span> <span data-ttu-id="51cef-174">Новая историческая запись переоценки в иностранной валюте создается для поддержания исторического аудиторского следа, когда выполняется или сторнируется переоценка.</span><span class="sxs-lookup"><span data-stu-id="51cef-174">A new foreign currency revaluation historical record is created to maintain the historical audit trail of when the revaluation occurred or was reversed.</span></span>

<span data-ttu-id="51cef-175">Чтобы отменить несколько переоценок, сначала необходимо реверсировать самую последнюю переоценку.</span><span class="sxs-lookup"><span data-stu-id="51cef-175">To reverse several revaluations, you must reverse the most current revaluation first.</span></span> <span data-ttu-id="51cef-176">Затем продолжайте реверсирование более старых переоценок по датам.</span><span class="sxs-lookup"><span data-stu-id="51cef-176">Then continue to reverse older revaluations in date order.</span></span> <span data-ttu-id="51cef-177">Затем можно обработать новые переоценки для периодов, которые были реверсированы.</span><span class="sxs-lookup"><span data-stu-id="51cef-177">You can then process new revaluations for the periods that you reversed.</span></span>