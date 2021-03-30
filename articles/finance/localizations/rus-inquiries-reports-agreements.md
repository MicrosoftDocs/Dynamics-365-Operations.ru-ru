---
title: Запросы и отчеты с договорами
description: В этом разделе представлены сведения о восстановлении ранее удержанных сумм НДС для основных средств.
author: v-nadyuz
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2a6bb87f6bc8da66cb93d7cfe69192dfa393e439
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239611"
---
# <a name="inquiries-and-reports-with-agreements"></a><span data-ttu-id="44e20-103">Запросы и отчеты с договорами</span><span class="sxs-lookup"><span data-stu-id="44e20-103">Inquiries and reports with agreements</span></span>
[!include [banner](../includes/banner.md)]


## <a name="viewing-agreement-amounts"></a><span data-ttu-id="44e20-104">Просмотр сумм договоров</span><span class="sxs-lookup"><span data-stu-id="44e20-104">Viewing agreement amounts</span></span>

### <a name="view-sales-agreement-amounts"></a><a name="sales-agreement-amounts"></a><span data-ttu-id="44e20-105">Просмотр сумм договоров продажи</span><span class="sxs-lookup"><span data-stu-id="44e20-105">View sales agreement amounts</span></span>

1. <span data-ttu-id="44e20-106">На странице **Договоры продажи** выберите договор, а затем на вкладке **Договор продажи** в разделе **Связанные сведения** выберите **Сумма договора**, чтобы открыть страницу **Проводки клиента**.</span><span class="sxs-lookup"><span data-stu-id="44e20-106">On the **Sales agreements** page, select an agreement, and then, on the **Sales agreement** tab, in the **Related information** section, select **Agreement amount** to open the **Customer transactions** page.</span></span>

    ![Страница проводок по клиенту](media/14_Customer_transactions.png)
   
2. <span data-ttu-id="44e20-108">В полях **Дата начала** и **Дата окончания** укажите период, для которого требуется проанализировать суммы договоров.</span><span class="sxs-lookup"><span data-stu-id="44e20-108">In the **Start date** and **End date** fields, specify the period that you want to analyze agreement amounts for.</span></span>
3. <span data-ttu-id="44e20-109">В нижней части страницы в разделе **Итоги** просмотрите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="44e20-109">In the lower part of the page, in the **Totals** section, review thefollowing information:</span></span>

     - <span data-ttu-id="44e20-110">В **Начальное сальдо** отображается сальдо на дату начала.</span><span class="sxs-lookup"><span data-stu-id="44e20-110">The **Start balance** field shows the balance on the start date.</span></span>
     - <span data-ttu-id="44e20-111">В **Конечное сальдо** отображается сальдо на дату окончания.</span><span class="sxs-lookup"><span data-stu-id="44e20-111">The **End balance** field shows the balance on the end date.</span></span>
     - <span data-ttu-id="44e20-112">В полях **Оборот по дебету** и **Оборот по кредиту** отображаются соответствующие суммы согласно соглашению за период.</span><span class="sxs-lookup"><span data-stu-id="44e20-112">The **Amount debited** and **Amount credited** fields show the corresponding amounts under the agreement for the period.</span></span>

4. <span data-ttu-id="44e20-113">В верхней и средней частях страницы проверьте проводки по контрагенту для задолженности, которая возникала, и возврат для этой задолженности:</span><span class="sxs-lookup"><span data-stu-id="44e20-113">In the upper and middle parts of the page, review the transactions on the counterparty for the debt that has occurred and for the repayment of that debt:</span></span>

    - <span data-ttu-id="44e20-114">В поле **Сумма** показана сумма проводки.</span><span class="sxs-lookup"><span data-stu-id="44e20-114">The **Amount** field shows the transaction amount.</span></span>
    - <span data-ttu-id="44e20-115">В поле **Сальдо** отображается сумма непоставленная сумма.</span><span class="sxs-lookup"><span data-stu-id="44e20-115">The **Balance** field shows the undelivered amount.</span></span>
    - <span data-ttu-id="44e20-116">В поле **Описание** показано описание проводки.</span><span class="sxs-lookup"><span data-stu-id="44e20-116">The **Description** field shows the transaction description.</span></span>

5. <span data-ttu-id="44e20-117">Выберите **Ваучер** для просмотра проводок ГК.</span><span class="sxs-lookup"><span data-stu-id="44e20-117">Select **Voucher** to view the ledger transactions.</span></span>

### <a name="view-purchase-agreement-amounts"></a><span data-ttu-id="44e20-118">Просмотр сумм договоров покупки</span><span class="sxs-lookup"><span data-stu-id="44e20-118">View purchase agreement amounts</span></span>

1. <span data-ttu-id="44e20-119">На странице **Договоры покупки** выберите договор, а затем на вкладке **Договор покупки** в разделе **Связанные сведения** выберите **Сумма договора**, чтобы открыть страницу **Проводки по поставщику**.</span><span class="sxs-lookup"><span data-stu-id="44e20-119">On the **Purchase agreements** page, select an agreement, and then, on the **Purchase agreement** tab, in the **Related information** section, select **Agreement amount** to open the **Vendor transactions** page.</span></span>

    ![Страница проводок по поставщику](media/15_Vendor_transactions.png)

2. <span data-ttu-id="44e20-121">Просмотрите суммы, как описано в предыдущем разделе данной темы, [Просмотр сумм договоров продажи](#sales-agreement-amounts).</span><span class="sxs-lookup"><span data-stu-id="44e20-121">Review the amounts as described in the previous section of this topic, [View sales agreement amounts](#sales-agreement-amounts).</span></span>

## <a name="viewing-orders-and-invoices-that-are-linked-to-the-agreement"></a><span data-ttu-id="44e20-122">Просмотр заказов и накладных, связанных с этим договором</span><span class="sxs-lookup"><span data-stu-id="44e20-122">Viewing orders and invoices that are linked to the agreement</span></span>

### <a name="view-sales-orders-and-service-invoices-that-are-linked-to-sales-agreements"></a><span data-ttu-id="44e20-123">Просмотр заказов на продажу и накладных на обслуживание, связанных с договором продажи</span><span class="sxs-lookup"><span data-stu-id="44e20-123">View sales orders and service invoices that are linked to sales agreements</span></span>

1. <span data-ttu-id="44e20-124">На странице **Договоры продажи** выберите договор.</span><span class="sxs-lookup"><span data-stu-id="44e20-124">On the **Sales agreements** page, select an agreement.</span></span>
2. <span data-ttu-id="44e20-125">На вкладке **Договор о покупке** в разделе **Связанные сведения** выполните любое из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="44e20-125">On the **Sales agreement** tab, in the **Related information** section, follow any of these steps:</span></span>

    - <span data-ttu-id="44e20-126">Выберите **Связанные заказы на продажу** для просмотра сведений о заказах на продажу, связанных с договором продажи.</span><span class="sxs-lookup"><span data-stu-id="44e20-126">Select **Linked sales orders** to view the details of the sales orders that are linked to the sales agreement.</span></span>
    - <span data-ttu-id="44e20-127">Выберите **Связанные накладные на услуги** для просмотра сведений о накладных с произвольным текстом, связанных с договором продажи.</span><span class="sxs-lookup"><span data-stu-id="44e20-127">Select **Linked services invoices** to view the details of the free text invoices that are linked to the sales agreement.</span></span>
    - <span data-ttu-id="44e20-128">Выберите **Несвязанные заказы** для просмотра сведений о заказах на продажу, **не связанных** с договором продажи.</span><span class="sxs-lookup"><span data-stu-id="44e20-128">Select **Nonlinked sales orders** to view the details of the sales orders that are **not** linked to the sales agreement.</span></span>
    - <span data-ttu-id="44e20-129">Выберите **Несвязанные накладные на услуги** для просмотра сведений о накладных с произвольным текстом, **не связанных** с договором продажи.</span><span class="sxs-lookup"><span data-stu-id="44e20-129">Select **Nonlinked services invoices** to view the details of the free text invoices that are **not** linked to the sales agreement.</span></span>

### <a name="view-purchase-orders-that-are-linked-to-purchase-agreements"></a><span data-ttu-id="44e20-130">Просмотр заказов на покупку, связанных с договорами покупки</span><span class="sxs-lookup"><span data-stu-id="44e20-130">View purchase orders that are linked to purchase agreements</span></span>

1. <span data-ttu-id="44e20-131">На странице **Договоры покупки** выберите договор.</span><span class="sxs-lookup"><span data-stu-id="44e20-131">On the **Purchase agreements** page, select an agreement.</span></span>
2. <span data-ttu-id="44e20-132">На вкладке **Договор покупки** в разделе **Связанные сведения** выполните любое из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="44e20-132">On the **Purchase agreement** tab, in the **Related information** section, follow any of these steps:</span></span>

    - <span data-ttu-id="44e20-133">Выберите **Связанные покупки** для просмотра сведений о заказах на покупку, связанных с договором покупки.</span><span class="sxs-lookup"><span data-stu-id="44e20-133">Select **Linked purchases** to view the details of the purchase orders that are linked to the purchase agreement.</span></span>
    - <span data-ttu-id="44e20-134">Выберите **Несвязанные покупки** для просмотра сведений о заказах на покупку, **не** связанных с договором покупки.</span><span class="sxs-lookup"><span data-stu-id="44e20-134">Select **Nonlinked purchases** to view the details of the purchase orders that are **not** linked to the purchase agreement.</span></span>

## <a name="generating-an-act-of-adjustment"></a><span data-ttu-id="44e20-135">Создание акта сверки взаимных расчетов</span><span class="sxs-lookup"><span data-stu-id="44e20-135">Generating an Act of adjustment</span></span>

<span data-ttu-id="44e20-136">Акт сверки взаимных расчетов — это документ, который используется для анализа сопоставлений с контрагентом (клиентом или поставщиком).</span><span class="sxs-lookup"><span data-stu-id="44e20-136">An Act of adjustment is a document that is used to analyze settlements with the counterparty (customer or vendor).</span></span> <span data-ttu-id="44e20-137">Стороны, которые участвуют в договоре, соглашаются о повторении документа и его уровне детализации.</span><span class="sxs-lookup"><span data-stu-id="44e20-137">The parties that are involved agree on the recurrence of the document and its level of detail.</span></span> <span data-ttu-id="44e20-138">Документ содержит информацию о расчетах с клиентами или расчетах с поставщиками в начале и конце периода, о накладных, которые были выпущены или получены, о произведенных платежах и о проводках взаимозачета, которые разносятся в течение отчетного периода.</span><span class="sxs-lookup"><span data-stu-id="44e20-138">The document contains information about accounts receivable or accounts payable at the beginning and end of the period, invoices that are issued or received, payments that are made, and netting transactions that are posted during the reporting period.</span></span> <span data-ttu-id="44e20-139">Акт сверки взаимных расчетов может создаваться в контексте накладных или договоров, либо для клиента или поставщика в целом.</span><span class="sxs-lookup"><span data-stu-id="44e20-139">An Act of adjustment can be generated in the context of invoices or agreements, or for the customer or vendor as a whole.</span></span>

> [!NOTE]
> <span data-ttu-id="44e20-140">Сопоставление является единственной основой для определения срока погашения задолженности, а также для определения налога на добавленную стоимость (НДС), базы налога для подоходного налога и других сведений.</span><span class="sxs-lookup"><span data-stu-id="44e20-140">The settlement is the only basis for determining the timeliness of debt repayment, and for determining value-added tax (VAT), the tax base for income tax, and other details.</span></span> <span data-ttu-id="44e20-141">Таким образом, акт сверки взаимных расчетов отражает документы погашения задолженности в контексте документов, формирующих задолженность.</span><span class="sxs-lookup"><span data-stu-id="44e20-141">Therefore, an Act of adjustment reflects the documents of debt repayment in the context of the documents that form the debt.</span></span>

<span data-ttu-id="44e20-142">При формировании акта сверки взаимных расчетов, если клиент одновременно является поставщиком, оценивается общая задолженность контрагента.</span><span class="sxs-lookup"><span data-stu-id="44e20-142">When generate an Act of adjustment, if the customer is a vendor at the same time, the total debt of the counterparty is estimated.</span></span>

<span data-ttu-id="44e20-143">Акт сверки взаимных расчетов содержит следующие данные в контексте клиента или поставщика, а также их договоров:</span><span class="sxs-lookup"><span data-stu-id="44e20-143">An Act of adjustment contains the following data in the context of the customer or vendor and its agreements:</span></span>

   - <span data-ttu-id="44e20-144">Развернутое общее сальдо контрагента (договор) в начале и конце периода.</span><span class="sxs-lookup"><span data-stu-id="44e20-144">The expanded total balance on the counterparty (agreement) at the beginning and the end of the period.</span></span> <span data-ttu-id="44e20-145">Расширенное итоговое сальдо — это сальдо накладных или кредит-нот, а также сальдо по авансовым платежам или возмещениям.</span><span class="sxs-lookup"><span data-stu-id="44e20-145">The expanded total balance is the balance of invoices or credit notes, and the balance on advances or refunds.</span></span>
   - <span data-ttu-id="44e20-146">Сведения о неоплаченных накладных предыдущего периода (кредиторские и дебиторские задолженности), их оплата и их смещение (сопоставление) в текущем периоде.</span><span class="sxs-lookup"><span data-stu-id="44e20-146">Information about unpaid invoices of the previous period (payables or receivables), their payment, and their offset (settlement) in the current period.</span></span>
   - <span data-ttu-id="44e20-147">Сведения о полученных или отправленных накладных или кредит-нотах для изучаемого периода вместе со сведениями об оплате и взаимозачете (сопоставление).</span><span class="sxs-lookup"><span data-stu-id="44e20-147">Information about received or shipped invoices or credit notes for the period that is under review, together with information about their payment and netting (settlement).</span></span>
   - <span data-ttu-id="44e20-148">Сведения об авансах или возврате (несопоставленные платежи за текущий период).</span><span class="sxs-lookup"><span data-stu-id="44e20-148">Information about advances or refunds (unsettled payments of the current period).</span></span>
   - <span data-ttu-id="44e20-149">Сведения об авансах или возврате за прошлые периоды (несопоставленные платежи за прошлые периоды).</span><span class="sxs-lookup"><span data-stu-id="44e20-149">Information about advances or refunds of past periods (unsettled payments of past periods).</span></span>

### <a name="generate-an-act-of-adjustment-for-a-customer"></a><a name="generate-act-adjustment-customer"></a><span data-ttu-id="44e20-150">Создание акта сверки взаимных расчетов с клиентом</span><span class="sxs-lookup"><span data-stu-id="44e20-150">Generate an Act of adjustment for a customer</span></span>

1.  <span data-ttu-id="44e20-151">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Акт сверки взаимных расчетов**.</span><span class="sxs-lookup"><span data-stu-id="44e20-151">Go to **Accounts receivable** \> **Inquiries and reports** \> **Act of adjustment**.</span></span>

2.  <span data-ttu-id="44e20-152">В разделе **Контрагент** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="44e20-152">In the **Counteragent** section, specify the following details:</span></span>

    - <span data-ttu-id="44e20-153">В поле **Счет клиента** выберите клиента, для которого требуется создать акт сверки взаимных расчетов.</span><span class="sxs-lookup"><span data-stu-id="44e20-153">In the **Customer account** field, select the customer to generate the Act of adjustment for.</span></span>
    - <span data-ttu-id="44e20-154">Если контрагентом является одновременно клиент и поставщик, установите для параметра **Контрагент** значение **Да**, чтобы создать разделы для клиента и для связанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="44e20-154">If the counterparty is both a customer and a vendor at the same time, set the **Counteragent** parameter to **Yes** to create sections for both the customer and the associated vendor.</span></span>
    - <span data-ttu-id="44e20-155">В поле **Код интервала дат** выберите код для отчетного периода.</span><span class="sxs-lookup"><span data-stu-id="44e20-155">In the **Date interval code** field, select the code for the reporting period.</span></span>
    - <span data-ttu-id="44e20-156">В полях **Дата от** и **Дата до** выберите начальную и конечную даты отчетного периода.</span><span class="sxs-lookup"><span data-stu-id="44e20-156">In the **From date** and **To date** fields, select the start and end dates of the reporting period.</span></span>

3.  <span data-ttu-id="44e20-157">В разделе **Валюта** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="44e20-157">In the **Currency** section, specify the following details:</span></span>

    - <span data-ttu-id="44e20-158">В поле **Тип валюты** выберите тип валюты проводки: **Валюта учета**, **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="44e20-158">In the **Currency type** field, select the type of the transaction currency: **Accounting currency** or **Indicated currency**.</span></span>
    - <span data-ttu-id="44e20-159">В поле **Валюта** выберите валюту проводки.</span><span class="sxs-lookup"><span data-stu-id="44e20-159">In the **Currency** field, select the transaction currency.</span></span> <span data-ttu-id="44e20-160">Это поле доступно только если в поле **Тип валюты** выбрано значение **Указанная валюта**.</span><span class="sxs-lookup"><span data-stu-id="44e20-160">This field is available only if you select **Indicated currency** in the **Currency type** field.</span></span>

4.  <span data-ttu-id="44e20-161">В разделе **Настройка** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="44e20-161">In the **Setup** section, specify the following details:</span></span>

    - <span data-ttu-id="44e20-162">Установите для параметра **По данным контрагента** значение **Да**, если требуется, чтобы данные автоматически вводились в раздел, который должен быть заполнен контрагентом.</span><span class="sxs-lookup"><span data-stu-id="44e20-162">Set the **By data of counteragent** option to **Yes** if you want data to be automatically entered in the section that is intended to be filled in by the counterparty.</span></span>
    - <span data-ttu-id="44e20-163">Установите для параметра **Удалять нулевые сальдо** значение **Да**, чтобы исключить из отчета строки сальдо накладной с нулевым сальдо (0) или сальдо, равным сумме накладной.</span><span class="sxs-lookup"><span data-stu-id="44e20-163">Set the **Delete zero balance** option to **Yes** to exclude invoice balance lines from the report if they have a balance of 0 (zero) or a balance that equals the amount of the invoice.</span></span>
    - <span data-ttu-id="44e20-164">Установите для параметра **Договор** значение **Да**, чтобы создать акт сверки взаимных расчетов в контексте договоров.</span><span class="sxs-lookup"><span data-stu-id="44e20-164">Set the **Agreements** option to **Yes** to generate the Act of adjustment in the context of agreements.</span></span>
    - <span data-ttu-id="44e20-165">Установите для параметра **Документ** значение **Да**, чтобы создать акт сверки взаимных расчетов в контексте документов, формирующих задолженность.</span><span class="sxs-lookup"><span data-stu-id="44e20-165">Set the **Documents** option to **Yes** to generate the Act of adjustment in the context of documents that form debt.</span></span>

5. <span data-ttu-id="44e20-166">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="44e20-166">Select **OK**.</span></span>

    ![Страница акта сверки взаимных расчетов](media/16_Act_of_adjustment_(customers).png)

    > [!NOTE]
    > <span data-ttu-id="44e20-168">Для просмотра проводок клиента, которые создали строку, выберите строку, а затем на панели операций выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="44e20-168">To view the customer transactions that have generated a line, select the line, and then, on the Action Pane, select **Transactions**.</span></span> 
    >
    > <span data-ttu-id="44e20-169">Щелкните **Выбрать** для изменения параметров отчета.</span><span class="sxs-lookup"><span data-stu-id="44e20-169">To change the report parameters, on the Action Pane, select **Select**.</span></span>
    >
    > <span data-ttu-id="44e20-170">Щелкните **Печать** для печати отчета.</span><span class="sxs-lookup"><span data-stu-id="44e20-170">To print the report, on the Action Pane, select **Print**.</span></span>

![Проводки клиента, создавшие строку](media/17_Act_of_adjustment.png)

### <a name="generate-an-act-of-adjustment-for-a-vendor"></a><span data-ttu-id="44e20-172">Создание акта сверки взаимных расчетов с поставщиком</span><span class="sxs-lookup"><span data-stu-id="44e20-172">Generate an Act of adjustment for a vendor</span></span>

1. <span data-ttu-id="44e20-173">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Акт сверки взаимных расчетов**.</span><span class="sxs-lookup"><span data-stu-id="44e20-173">Go to **Accounts receivable** \> **Inquiries and reports** \> **Act of adjustment**.</span></span>
2. <span data-ttu-id="44e20-174">В разделе **Контрагент** в поле **Счет поставщика** выберите поставщика, для которого требуется создать акт сверки взаимных расчетов.</span><span class="sxs-lookup"><span data-stu-id="44e20-174">In the **Counteragent** section, in the **Vendor account** field, select the vendor to generate the Act of adjustment for.</span></span>
3. <span data-ttu-id="44e20-175">Укажите другие сведения, как описано в предыдущем разделе данной темы, [Создание акта сверки взаимных расчетов с клиентом](#generate-act-adjustment-customer), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="44e20-175">Specify other details as described in the previous section of this topic, [Generate an Act of adjustment for a customer](#generate-act-adjustment-customer), and then select **OK**.</span></span> <span data-ttu-id="44e20-176">После создания отчета можно также просмотреть проводки поставщика, изменить параметры отчета и напечатать отчет.</span><span class="sxs-lookup"><span data-stu-id="44e20-176">After generate the report, you can also view vendor transactions, change the report parameters, and print the report.</span></span>

<span data-ttu-id="44e20-177">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="44e20-177">Find more details in the following topics:</span></span>

- [<span data-ttu-id="44e20-178">Договоры</span><span class="sxs-lookup"><span data-stu-id="44e20-178">Agreements</span></span>](rus-agreements.md)
- [<span data-ttu-id="44e20-179">Настройка и создание договоров</span><span class="sxs-lookup"><span data-stu-id="44e20-179">Set up and create agreements</span></span>](rus-set-up-and-create-agreements.md)
- [<span data-ttu-id="44e20-180">Регистрация проводок со ссылками на договоры</span><span class="sxs-lookup"><span data-stu-id="44e20-180">Register transactions with reference to agreements</span></span>](rus-register-transactions-with-reference-to-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]