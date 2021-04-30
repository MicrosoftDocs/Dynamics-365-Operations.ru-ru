---
title: Налоговые регистры для задолженности расчетов с поставщиками и списание задолженностей
description: В этом разделе приводятся сведения о налоговые регистры для задолженности расчетов с поставщиками и списание задолженностей.
author: anasyash
ms.date: 04/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f7d5542455f3e7218d6d2bcad587c9d1f8606cf3
ms.sourcegitcommit: 8d637c0d3a038a2422dd5cc51a81bb33d0385476
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2021
ms.locfileid: "5871119"
---
# <a name="accounts-payable-debt-tax-registers-and-debt-write-offs"></a><span data-ttu-id="e2bef-103">Налоговые регистры для задолженности расчетов с поставщиками и списание задолженностей</span><span class="sxs-lookup"><span data-stu-id="e2bef-103">Accounts payable debt tax registers and debt write-offs</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e2bef-104">В этом разделе приводятся сведения о сомнительных долгах для расчетов с поставщиками, списании задолженностей для них, и следующие налоговые регистры:</span><span class="sxs-lookup"><span data-stu-id="e2bef-104">This topic provides information about accounts payable bad debts, write-offs for them, and the following tax registers:</span></span>
-   <span data-ttu-id="e2bef-105">Кред. задолженность - инвентаризация</span><span class="sxs-lookup"><span data-stu-id="e2bef-105">Accounts payable inventory act</span></span>
-   <span data-ttu-id="e2bef-106">Движение модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="e2bef-106">Accounts payable movement</span></span>

<span data-ttu-id="e2bef-107">Расчеты с поставщиками формируются на основе неоплаченных накладных для покупок товаров и услуг, а при авансовых платежах, полученных от клиентов.</span><span class="sxs-lookup"><span data-stu-id="e2bef-107">Accounts payable are formed based on outstanding invoices for purchases of goods and services, and on advance payments that are received from customers.</span></span>

<span data-ttu-id="e2bef-108">Суммы по расчетам с поставщиками, списанные в связи с истечением периода ограничения, считаются доходами от неосновной деятельности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-108">Accounts payable amounts that are written off because of expiration of the limitation period are considered non-operating income.</span></span>

## <a name="setup"></a><span data-ttu-id="e2bef-109">Настройка</span><span class="sxs-lookup"><span data-stu-id="e2bef-109">Setup</span></span>

### <a name="set-up-accounts-payable-parameters"></a><span data-ttu-id="e2bef-110">Настройте параметры "Расчетов с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="e2bef-110">Set up Accounts payable parameters</span></span>

1. <span data-ttu-id="e2bef-111">Перейдите в раздел **Расчеты с поставщиками** > **Настройка** > **Параметры расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-111">Go to **Accounts payable** > **Setup** > **Accounts payable parameters**.</span></span>
2. <span data-ttu-id="e2bef-112">На вкладке **Главная книга и налог** на экспресс-вкладке **Кредиторская задолженность** в поле **Код дохода** укажите код дохода, который необходимо назначить проводкам для списания сомнительной задолженности по расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e2bef-112">On the **Ledger and sales tax** tab, on the **Creditor debts** FastTab, in the **Income code** field, specify the income code to assign to transactions for writing off bad accounts payable debt.</span></span>
3. <span data-ttu-id="e2bef-113">В поле **счет ГК** укажите счет для доходов от неосновной деятельности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-113">In the **Main account** field, specify an account for non-operating income.</span></span>

    ![Параметры модуля ""Расчеты с поставщиками", вкладка "Главная книга и налог"](media/1-AP_tax.png)

4. <span data-ttu-id="e2bef-115">На вкладке **Номерные серии** в поле **Код номерной серии** выберите код номерной серии для ссылки **Ваучер ГК для амортизации задолженностей**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-115">On the **Number sequences** tab, in the **Number sequence code** field, select the number sequence code for the **Ledger voucher for debts amortization** reference.</span></span>

### <a name="set-up-the-debt-interval-for-hopeless-debts"></a><span data-ttu-id="e2bef-116">Настройка интервала задолженности для безнадежных долгов</span><span class="sxs-lookup"><span data-stu-id="e2bef-116">Set up the debt interval for hopeless debts</span></span>

1. <span data-ttu-id="e2bef-117">Перейти к **Расчеты с поставщиками** > **Настройка** > **Интервал задолженности**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-117">Go to **Accounts payable** > **Setup** > **Debt interval**.</span></span>
2. <span data-ttu-id="e2bef-118">В поле **С** введите нижний предел интервала задолженности, в днях.</span><span class="sxs-lookup"><span data-stu-id="e2bef-118">In the **From** field, enter the lower limit of the debt interval, in days.</span></span> <span data-ttu-id="e2bef-119">Например, введите **240**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-119">For example, enter **240**.</span></span>
3. <span data-ttu-id="e2bef-120">В поле **По** введите верхний предел интервала задолженности, в днях.</span><span class="sxs-lookup"><span data-stu-id="e2bef-120">In the **By** field, enter the upper limit of the debt interval, in days.</span></span> <span data-ttu-id="e2bef-121">Например, введите **0**, если верхний предел отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e2bef-121">For example, enter **0** if there is no upper limit.</span></span>
4. <span data-ttu-id="e2bef-122">В поле **Описание** введите подробное описание интервала задолженности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-122">In the **Description** field, enter a detailed description of the debt interval.</span></span>

    ![Интервалы кредиторской задолженности](media/2-AP_tax.png)

## <a name="tax-registers"></a><span data-ttu-id="e2bef-124">Регистры налогового учета</span><span class="sxs-lookup"><span data-stu-id="e2bef-124">Tax registers</span></span>

<span data-ttu-id="e2bef-125">Необходимо создать и настроить налоговые регистры.</span><span class="sxs-lookup"><span data-stu-id="e2bef-125">You must create and set up tax registers.</span></span> <span data-ttu-id="e2bef-126">Дополнительные сведения см. в "Регистры налога на прибыль".</span><span class="sxs-lookup"><span data-stu-id="e2bef-126">For more information, see Profit tax registers.</span></span> <span data-ttu-id="e2bef-127">В следующих разделах приведены дополнительные сведения о каждом из налоговых регистров.</span><span class="sxs-lookup"><span data-stu-id="e2bef-127">The following sections provide more information about each tax register.</span></span>

### <a name="accounts-payable-inventory-act-tax-register"></a><span data-ttu-id="e2bef-128">Налоговый регистр акта учета запасов для расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="e2bef-128">Accounts payable inventory act tax register</span></span>

<span data-ttu-id="e2bef-129">Налоговый регистр **акта запасов для расчетов с поставщиками** основан на запасах счетов по состоянию на дату отчета.</span><span class="sxs-lookup"><span data-stu-id="e2bef-129">The **Accounts payable inventory act** tax register is based on the inventory of accounts as of the reporting date.</span></span> <span data-ttu-id="e2bef-130">Он отражает существование сумм расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e2bef-130">It reflects the existence of accounts payable amounts.</span></span>

<span data-ttu-id="e2bef-131">Регистр требуется для учета доходов от неосновной деятельности и расходов для отчетного (налогового) периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-131">The register is required to account for non-operating income and expenses for the reporting (tax) period.</span></span>

   ![Страница акта учета запасов для расчетов с поставщиками](media/3-AP_tax.png)

<span data-ttu-id="e2bef-133">Строки регистра также отображают следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="e2bef-133">The register lines show the following information:</span></span>

- <span data-ttu-id="e2bef-134">**Объект учета**: номер накладной поставщика или номер полученного авансового платежа клиента.</span><span class="sxs-lookup"><span data-stu-id="e2bef-134">**Accounting object**: The number of the vendor invoice or the number of the customer advance payment that was received.</span></span>
- <span data-ttu-id="e2bef-135">**Дата проводки**: дата накладной или авансового платежа.</span><span class="sxs-lookup"><span data-stu-id="e2bef-135">**Transaction date**: The date of the invoice or advance payment.</span></span>
- <span data-ttu-id="e2bef-136">**Крайний срок**: дата выполнения платежа в соответствии с условиями оплаты.</span><span class="sxs-lookup"><span data-stu-id="e2bef-136">**Deadline**: The payment due date according to the payment terms.</span></span>
- <span data-ttu-id="e2bef-137">**Задолженность**: неоплаченная сумма по накладной или авансовый платеж, который был получен на дату запасов, если период распределения по срокам оплаты находится в пределах интервала задолженности, настроенного ранее.</span><span class="sxs-lookup"><span data-stu-id="e2bef-137">**Debt**: The outstanding amount of the invoice or advance payment that was received on the date of inventory, if the aging period of the debts is within the debt interval limits that you configured earlier.</span></span>
- <span data-ttu-id="e2bef-138">**Сумма НДС для задолженности**: сумма налога на добавленную стоимость (НДС) по неоплаченным расчетам с поставщиками на дату запасов.</span><span class="sxs-lookup"><span data-stu-id="e2bef-138">**Debt VAT amount**: The amount of value-added tax (VAT) on outstanding accounts payable on the date of inventory.</span></span>
- <span data-ttu-id="e2bef-139">**Закрытая сумма**: общая сумма расчетов с поставщиками, которая была списана в течение отчетного (налогового) периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-139">**Closed amount**: The total amount of accounts payable that were written off during the reporting (tax) period.</span></span>
- <span data-ttu-id="e2bef-140">**Закрытая сумма НДС**: общая сумма НДС для расчетов с поставщиками, которая была списана в течение отчетного (налогового) периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-140">**Closed VAT amount**: The total amount of VAT on accounts payable that were written off during the reporting (tax) period.</span></span>
- <span data-ttu-id="e2bef-141">**Не подтвержденная задолженность**: введите сумму неподтвержденной задолженности по поставщику.</span><span class="sxs-lookup"><span data-stu-id="e2bef-141">**Non-confirmed debt**: Enter the amount of unconfirmed debt by vendor.</span></span>

### <a name="accounts-payable-movement-tax-register"></a><span data-ttu-id="e2bef-142">Налоговый регистр движения средств при расчетах с поставщиками</span><span class="sxs-lookup"><span data-stu-id="e2bef-142">Accounts payable movement tax register</span></span>

<span data-ttu-id="e2bef-143">Налоговый регистр **Движение средств при расчетах с поставщиками** сформирован для суммирования информации об операциях по движению средств при расчетах с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e2bef-143">The **Accounts payable movement** tax register is formed to summarize information about operations on the movement of accounts payable.</span></span>

<span data-ttu-id="e2bef-144">В регистр вносятся записи о всех вхождениях расчетов с поставщиками, и все возвраты денежных средств (полные или частичные) и их списание по налогоплательщику между началом налогового периода и датой отчетности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-144">Entries are made in the register for all occurrences of accounts payable, and all repayments (full or partial) and write-offs of them by the taxpayer, between the beginning of the tax period and the reporting date.</span></span>

<span data-ttu-id="e2bef-145">Этот регистр не соответствует суммам расчетов с поставщиками налогоплательщика в бюджетах других уровней.</span><span class="sxs-lookup"><span data-stu-id="e2bef-145">This register doesn't reflect the amounts of the taxpayer's accounts payable to the budgets of different levels.</span></span>

<span data-ttu-id="e2bef-146">В целях отчетности записи по проводкам в иностранной валюте также создаются для каждого факта о переоценке задолженности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-146">For reporting purposes, records on transactions in foreign currency are also made for each fact about the revaluation of debt.</span></span>

   ![Страница Движение средств при расчете с поставщиками](media/4-AP_tax.png)

<span data-ttu-id="e2bef-148">Строки регистра также отображают следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="e2bef-148">The register lines show the following information:</span></span>

- <span data-ttu-id="e2bef-149">**Объект учета**: номер накладной поставщика или номер полученного авансового платежа клиента.</span><span class="sxs-lookup"><span data-stu-id="e2bef-149">**Accounting object**: The number of the vendor invoice or the number of the customer advance payment that was received.</span></span>
- <span data-ttu-id="e2bef-150">**Дата проводки**: дата накладной или авансового платежа.</span><span class="sxs-lookup"><span data-stu-id="e2bef-150">**Transaction date**: The date of the invoice or advance payment.</span></span>
- <span data-ttu-id="e2bef-151">**Описание проводки**: описание документа.</span><span class="sxs-lookup"><span data-stu-id="e2bef-151">**Transaction description**: A description of the document.</span></span>
- <span data-ttu-id="e2bef-152">**Крайний срок**: дата выполнения платежа в соответствии с условиями оплаты.</span><span class="sxs-lookup"><span data-stu-id="e2bef-152">**Deadline**: The payment due date according to the payment terms.</span></span>
- <span data-ttu-id="e2bef-153">**Порядок учета**: условия оплаты накладной.</span><span class="sxs-lookup"><span data-stu-id="e2bef-153">**Accounting order**: The invoice payment terms.</span></span>
- <span data-ttu-id="e2bef-154">**Задолженность**: неоплаченная сумма по накладной или авансовый платеж, который был получен на дату запасов, если период распределения по срокам оплаты находится в пределах интервала задолженности, настроенного ранее.</span><span class="sxs-lookup"><span data-stu-id="e2bef-154">**Debt**: The outstanding amount of the invoice or advance payment that was received on the date of inventory, if the aging period of the debts is within the debt interval limits that you configured earlier.</span></span>
- <span data-ttu-id="e2bef-155">**Сумма НДС для задолженности**: сумма НДС по неоплаченным расчетам с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e2bef-155">**Debt VAT amount**: The amount of VAT on outstanding accounts payable.</span></span>
- <span data-ttu-id="e2bef-156">**Дата закрытия**: дата закрытия накладной, списания или проводки платежа.</span><span class="sxs-lookup"><span data-stu-id="e2bef-156">**Close date**: The closing date of the invoice, write-off, or payment transaction.</span></span>
- <span data-ttu-id="e2bef-157">**Причина закрытия**: описание проводки для списания или выплаты задолженности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-157">**Close reason**: A description of the transaction for writing off or paying the debt.</span></span>
- <span data-ttu-id="e2bef-158">**Сумма закрытия**: общая сумма списанных расчетов с поставщиками для отчетного (налогового) периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-158">**Close amount**: The total amount of written-off accounts payable for the reporting (tax) period.</span></span>
- <span data-ttu-id="e2bef-159">**Закрытая сумма НДС**: общая сумма НДС для расчетов с поставщиками, которая была списана для отчетного (налогового) периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-159">**Closed VAT amount**: The total amount of VAT on accounts payable that were written off for the reporting (tax) period.</span></span>
- <span data-ttu-id="e2bef-160">**Сумма непогашенной задолженности**: общая сумма неоплаченных расчетов с поставщиками после движения средств.</span><span class="sxs-lookup"><span data-stu-id="e2bef-160">**Unsettled debt amount**: The total amount of outstanding accounts payable after the movement.</span></span>
- <span data-ttu-id="e2bef-161">**Сумма НДС по непогашенной задолженности**: общая сумма НДС по неоплаченным расчетам с поставщиками после движения средств.</span><span class="sxs-lookup"><span data-stu-id="e2bef-161">**Unsettled debt amount VAT**: The total amount of VAT on outstanding accounts payable after the movement.</span></span>

## <a name="write-off-hopeless-debts"></a><span data-ttu-id="e2bef-162">Списание безнадежных задолженностей</span><span class="sxs-lookup"><span data-stu-id="e2bef-162">Write off hopeless debts</span></span>

<span data-ttu-id="e2bef-163">Прежде чем можно будет списать безнадежные задолженности, необходимо создать журнал регистров для того же периода, что и списание, и рассчитать регистры.</span><span class="sxs-lookup"><span data-stu-id="e2bef-163">Before you can write off hopeless debts, you must create a register journal for the same period as the write-off and calculate the registers.</span></span>

<span data-ttu-id="e2bef-164">В журнале следует утвердить регистр **акт учета запасов для расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-164">In the journal, you should approve the **Accounts payable inventory act** register.</span></span>

> [!NOTE]
> <span data-ttu-id="e2bef-165">Не утверждайте регистр **Движение средств при расчете с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-165">Don't approve the **Accounts payable movement** register.</span></span>

### <a name="recognize-and-write-off-hopeless-debt"></a><span data-ttu-id="e2bef-166">Распознавание и списание безнадежной задолженности</span><span class="sxs-lookup"><span data-stu-id="e2bef-166">Recognize and write off hopeless debt</span></span>

1. <span data-ttu-id="e2bef-167">Расчет и утверждение журнала налоговых регистров для предыдущего периода.</span><span class="sxs-lookup"><span data-stu-id="e2bef-167">Calculate and approve the tax register journal for the previous period.</span></span> <span data-ttu-id="e2bef-168">Дополнительные сведения см. в "Регистры налога на прибыль".</span><span class="sxs-lookup"><span data-stu-id="e2bef-168">For more information, see Profit tax registers.</span></span>
2. <span data-ttu-id="e2bef-169">Переход к **Расчеты с поставщиками** > **Периодические задачи** > **Амортизация** > **Амортизация кредиторской задолженности**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-169">Go to **Accounts payable** > **Periodic tasks** > **Amortization** > **Trade liabilities amortization**.</span></span>
3. <span data-ttu-id="e2bef-170">В поле **Дата расчета** выберите дату, которая указывает необходимый расчетный период.</span><span class="sxs-lookup"><span data-stu-id="e2bef-170">In the **Calculation date** field, select a date that indicates the required calculation period.</span></span>

    <span data-ttu-id="e2bef-171">На странице отображаются задолженности, срок действия которых истек на указанную дату отчета:</span><span class="sxs-lookup"><span data-stu-id="e2bef-171">The page shows the debts that have expired as of the indicated reporting date:</span></span>

    -   <span data-ttu-id="e2bef-172">На вкладке **Клиенты** отображается список предоплат клиентов.</span><span class="sxs-lookup"><span data-stu-id="e2bef-172">The **Customers** tab shows the list of customer prepayments.</span></span>
    -   <span data-ttu-id="e2bef-173">На вкладке **Поставщики** отображается список накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="e2bef-173">The **Vendors** tab shows the list of vendor invoices.</span></span>

4. <span data-ttu-id="e2bef-174">Для просмотра исходных проводок клиента или поставщика выберите **проводки** на соответствующей вкладке.</span><span class="sxs-lookup"><span data-stu-id="e2bef-174">To review the original customer or vendor transactions, select **Transactions** on the appropriate tab.</span></span>
5. <span data-ttu-id="e2bef-175">Выбор долгов для списания.</span><span class="sxs-lookup"><span data-stu-id="e2bef-175">Select the debts to write off.</span></span> <span data-ttu-id="e2bef-176">В поле **Итого** в разделе **Отмечено** отображается общая сумма проводок, помеченных для дебета.</span><span class="sxs-lookup"><span data-stu-id="e2bef-176">The **Total** field in the **Marked** section shows the total amount of the transactions that have been marked for debiting.</span></span>

    ![Страница журнала отмены задолженностей кредиторов, Поле "Итого"](media/5-AP_tax.png)

6. <span data-ttu-id="e2bef-178">На панели операций выберите **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-178">On the Action Pane, select **Update**.</span></span> <span data-ttu-id="e2bef-179">Помеченные проводки больше не отображаются.</span><span class="sxs-lookup"><span data-stu-id="e2bef-179">The marked transactions are no longer shown.</span></span> <span data-ttu-id="e2bef-180">В разделе **Списано** суммы увеличиваются до значения, которое отображалось в поле **Итого** в разделе **Отмечено** до того, как было выбрано **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-180">In the **Written off** section, the amounts are increased to the value that appeared in the **Total** field in the **Marked** section before you selected **Update**.</span></span> <span data-ttu-id="e2bef-181">Создаются проводки для клиентов/поставщиков.</span><span class="sxs-lookup"><span data-stu-id="e2bef-181">Transactions for customers/vendors are created.</span></span> <span data-ttu-id="e2bef-182">Кроме того, в главной книге создаются проводки для списания каждой задолженности.</span><span class="sxs-lookup"><span data-stu-id="e2bef-182">Additionally, transactions for writing off each debt are created in the general ledger.</span></span> <span data-ttu-id="e2bef-183">Дата операций списания соответствует дате, выбранной в поле **Дата расчета**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-183">The date of the write-off operations corresponds to the date that you selected in the **Calculation date** field.</span></span>

    ![Страница журнала отмены задолженностей кредиторов, Поле "Дата расчета"](media/6-AP_tax.png)

### <a name="cancel-the-write-off-of-hopeless-debt"></a><span data-ttu-id="e2bef-185">Отмена списания безнадежной задолженности</span><span class="sxs-lookup"><span data-stu-id="e2bef-185">Cancel the write-off of hopeless debt</span></span>

<span data-ttu-id="e2bef-186">Чтобы отменить списание безнадежной задолженности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2bef-186">To cancel the write-off of hopeless debts, follow these steps.</span></span>

1. <span data-ttu-id="e2bef-187">Переход к **Расчеты с поставщиками** > **Периодические задачи** > **Амортизация** > **Отмена амортизации кредиторской задолженности**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-187">Go to **Accounts payable** > **Periodic tasks** > **Amortization** > **Trade liabilities amortization cancellation**.</span></span>
2. <span data-ttu-id="e2bef-188">В поле **Дата расчета** выберите дату, которая указывает необходимый расчетный период.</span><span class="sxs-lookup"><span data-stu-id="e2bef-188">In the **Calculation date** field, select a date that indicates the required calculation period.</span></span>

    <span data-ttu-id="e2bef-189">На странице отображаются списанные задолженности, срок действия которых истек на указанную дату отчета:</span><span class="sxs-lookup"><span data-stu-id="e2bef-189">The page shows the written-off debts that have expired as of the indicated reporting date:</span></span>

    - <span data-ttu-id="e2bef-190">На вкладке **Клиенты** отображается список списанных предоплат клиентов.</span><span class="sxs-lookup"><span data-stu-id="e2bef-190">The **Customers** tab shows the list of written-off customer prepayments.</span></span>
    - <span data-ttu-id="e2bef-191">На вкладке **Поставщики** отображается список списанных накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="e2bef-191">The **Vendors** tab shows the list of written-off vendor invoices.</span></span>

3. <span data-ttu-id="e2bef-192">Для просмотра исходных проводок клиента или поставщика выберите **проводки** на соответствующей вкладке.</span><span class="sxs-lookup"><span data-stu-id="e2bef-192">To review the original customer or vendor transactions, select **Transactions** on the appropriate tab.</span></span>
4. <span data-ttu-id="e2bef-193">Выбрать списанные задолженности для отмены.</span><span class="sxs-lookup"><span data-stu-id="e2bef-193">Select the written-off debts to cancel.</span></span> <span data-ttu-id="e2bef-194">В поле **Итого** в разделе **Отмечено** отображается общая сумма проводок, помеченных для дебета.</span><span class="sxs-lookup"><span data-stu-id="e2bef-194">The **Total** field in the **Marked** section shows the total amount of the transactions that have been marked for debiting.</span></span>

    ![Страница журнала отмены амортизации кредиторской задолженности](media/7-AP_tax.png)

5. <span data-ttu-id="e2bef-196">На панели операций выберите **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-196">On the Action Pane, select **Update**.</span></span> <span data-ttu-id="e2bef-197">Помеченные проводки больше не отображаются.</span><span class="sxs-lookup"><span data-stu-id="e2bef-197">The marked transactions are no longer shown.</span></span> <span data-ttu-id="e2bef-198">В разделе **Списано** суммы уменьшаются до значения, которое отображалось в поле **Итого** в разделе **Отмечено** до того, как было выбрано **Обновление**.</span><span class="sxs-lookup"><span data-stu-id="e2bef-198">In the **Written off** section, the amounts are decreased to the value that appeared in the **Total** field in the **Marked** section before you selected **Update**.</span></span> <span data-ttu-id="e2bef-199">Создаются проводки, отменяющие списание расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e2bef-199">Transactions that cancel the write-off of accounts payable are generated.</span></span>
