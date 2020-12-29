---
title: Обработка и печать счетов-фактур
description: В этом разделе приводятся сведения о работе со счетами-фактурами по накладным.
author: anasyash
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: 14692681eafe9120ba7689d8dc9fc1475ffa4578
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408557"
---
# <a name="invoice-factures-processing-and-printing"></a><span data-ttu-id="bb5d7-103">Обработка и печать счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="bb5d7-103">Invoice factures processing and printing</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bb5d7-104">Счет-фактура по накладной — это документ, который удостоверяет фактическую отгрузку товаров или услуг и их стоимость.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-104">An invoice-facture is a document that certifies the actual shipment of goods or services, and their cost.</span></span> <span data-ttu-id="bb5d7-105">Счет-фактура по накладной создается (отправляется) продавцом (подрядчиком или исполнителем) покупателю (клиенту) после того, как покупатель принял все товары или услуги.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-105">An invoice-facture is issued (sent) by the seller (contractor or performer) to the buyer (customer) after the buyer has accepted all the goods or services.</span></span> <span data-ttu-id="bb5d7-106">Счет-фактура по накладной имеет две цели.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-106">An invoice-facture has two purposes.</span></span> 

- <span data-ttu-id="bb5d7-107">Подтверждение того, что заказ или работа выполнены</span><span class="sxs-lookup"><span data-stu-id="bb5d7-107">Confirmation that the order or work has been completed</span></span>
- <span data-ttu-id="bb5d7-108">Подтверждение суммы оплаченного налога на добавленную стоимость (НДС), чтобы сумма эта сумма могла быть кредитована позже</span><span class="sxs-lookup"><span data-stu-id="bb5d7-108">Confirmation of the amount of value-added tax (VAT) that was paid, so that the amount can be credited later</span></span>

<span data-ttu-id="bb5d7-109">Счет-фактура по накладной может быть обработан следующими способами:</span><span class="sxs-lookup"><span data-stu-id="bb5d7-109">An invoice-facture can be processed in the following ways:</span></span>

- <span data-ttu-id="bb5d7-110">На основе заказа на покупку или заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="bb5d7-110">Based on a purchase order or sales order</span></span>
- <span data-ttu-id="bb5d7-111">На основе разнесенной накладной поставщика или клиента</span><span class="sxs-lookup"><span data-stu-id="bb5d7-111">Based on a posted vendor or customer invoice</span></span>
- <span data-ttu-id="bb5d7-112">На основе поступления приобретенного продукта</span><span class="sxs-lookup"><span data-stu-id="bb5d7-112">Based on a purchase product receipt</span></span>
- <span data-ttu-id="bb5d7-113">На основе отборочной накладной продажи</span><span class="sxs-lookup"><span data-stu-id="bb5d7-113">Based on a sales packing slip</span></span>
- <span data-ttu-id="bb5d7-114">На основе накладной с произвольным текстом по продаже</span><span class="sxs-lookup"><span data-stu-id="bb5d7-114">Based on a sales free-text invoice</span></span>

## <a name="setup"></a><span data-ttu-id="bb5d7-115">Настройка</span><span class="sxs-lookup"><span data-stu-id="bb5d7-115">Setup</span></span>

### <a name="set-up-a-number-sequence-for-factures"></a><span data-ttu-id="bb5d7-116">Настройка номерной серии для счетов-фактур</span><span class="sxs-lookup"><span data-stu-id="bb5d7-116">Set up a number sequence for factures</span></span>

1. <span data-ttu-id="bb5d7-117">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-117">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="bb5d7-118">На вкладке **Номерные серии** выберите код номерной серии для ссылки на счет-фактуру, затем назначьте номерную серию в поле **Код номерной серии**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-118">On the **Number sequences** tab, select a number sequence code for the facture reference, and then assign the number sequence in the **Number sequence code** field.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-119">Убедитесь, что выбранная номерная серия для счетов-фактур непрерывна (выбран флаг **Непрерывно** на вкладке **Общие**).</span><span class="sxs-lookup"><span data-stu-id="bb5d7-119">Verify that the selected number sequence for factures is continuous (the **Continuous** flag on the **General** FastTab is selected).</span></span> 

3. <span data-ttu-id="bb5d7-120">Чтобы переопределить существующие группы номерных серий, выберите **Группа**, затем выберите **Создать**, чтобы создать группу номерных серий.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-120">To override existing number sequence groups, select **Group**, and then select **New** to create a number sequence group.</span></span> <span data-ttu-id="bb5d7-121">Затем в нижней части страницы определите номерную серию для счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-121">Then, in the lower part of the page, define the number sequence for facture.</span></span>

<span data-ttu-id="bb5d7-122">На странице **Все клиенты** можно переопределить группы номерных серий в поле **Номерная серия** на экспресс-вкладке **Накладные и поставка**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-122">On the **All customers** page, you can override number sequence groups in the **Number sequence** field on the **Invoice and delivery** FastTab.</span></span>

### <a name="set-up-a-tax-settlement-period"></a><span data-ttu-id="bb5d7-123">Настройка периода сопоставления для налогов</span><span class="sxs-lookup"><span data-stu-id="bb5d7-123">Set up a tax settlement period</span></span>

1. <span data-ttu-id="bb5d7-124">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Периоды сопоставления налогов**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-124">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="bb5d7-125">Убедитесь, что на экспресс-вкладке **Интервалы периода** включен требуемый период.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-125">On the **Period intervals** FastTab, verify that the required period is included.</span></span>

## <a name="process-and-print-invoice-factures-for-purchase-orders"></a><span data-ttu-id="bb5d7-126">Обработка и печать счетов-фактур по накладным для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="bb5d7-126">Process and print invoice-factures for purchase orders</span></span>
<span data-ttu-id="bb5d7-127">Покупка завершена, когда зарегистрированы накладная и счет-фактура.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-127">A purchase is completed when the invoice and facture are registered.</span></span> <span data-ttu-id="bb5d7-128">Обычно проводки создаются при регистрации накладной, затем создается счет-фактура, которая является основой для вычета НДС.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-128">Typically, transactions are created when the invoice is registered, and then the facture, which is the basis for VAT deduction, is created.</span></span>

### <a name="process-a-facture-without-posting-a-purchase-order-invoice"></a><span data-ttu-id="bb5d7-129">Обработка счета-фактуры без разноски накладной заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="bb5d7-129">Process a facture without posting a purchase order invoice</span></span>
<span data-ttu-id="bb5d7-130">Можно обработать счет-фактуру до разноски накладной.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-130">You can process a facture before an invoice is posted.</span></span> <span data-ttu-id="bb5d7-131">В этом случае накладная автоматически разносится при обработке счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-131">In this case, the invoice is automatically posted when the facture is processed.</span></span>

1. <span data-ttu-id="bb5d7-132">На странице **Все заказы на покупку** на панели операций на вкладке **Накладная** в группе **Создать** выберите **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-132">On the **All purchase orders** page, on the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Facture**.</span></span>
2. <span data-ttu-id="bb5d7-133">В верхней части страницы **Обновить счет-фактуру** задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="bb5d7-133">In the upper part of the **Update facture** page, set the following fields:</span></span>

  - <span data-ttu-id="bb5d7-134">**Счет-фактура** — введите номер счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-134">**Facture** – Enter the facture number.</span></span>
  - <span data-ttu-id="bb5d7-135">**Дата регистрации** — выберите дату регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-135">**Date of the registration** – Select the facture registration date.</span></span>
  - <span data-ttu-id="bb5d7-136">**Дата счета-фактуры** — выберите дату создания счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-136">**Facture date** – Select the facture creation date.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-137">Дата создания счета-фактуры совпадает с датой регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-137">The facture creation date is the same as the facture registration date.</span></span> <span data-ttu-id="bb5d7-138">Значение этого поля можно изменить только в том случае, если для параметра **Та же** установлено значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-138">You can change the value of this field only if you set the **Same as** option to **No**.</span></span>

3. <span data-ttu-id="bb5d7-139">В нижней части страницы отметьте накладные, которые должны быть включены в обработку счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-139">In the lower part of the page, mark the invoices that should be included in the facture processing.</span></span>
4. <span data-ttu-id="bb5d7-140">На панели действий выберите **Разноска** \> **Обновление и печать**, чтобы разнести и распечатать счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-140">On the Action Pane, select **Posting** \> **Update and print** to post and print the facture.</span></span>
<span data-ttu-id="bb5d7-141">–или– Выберите **Разноска** \> **Обновление**, чтобы обновить счет-фактуру без вывода ее на печать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-141">–or– Select **Posting** \> **Update** to update the facture without printing it.</span></span>
<span data-ttu-id="bb5d7-142">–или– Выберите **Разноска** \> **Печать**, чтобы распечатать счет-фактуру без ее обновления.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-142">–or– Select **Posting** \> **Print** to print the facture without posting it.</span></span>
5. <span data-ttu-id="bb5d7-143">Чтобы просмотреть разнесенные счета-фактуры, на панели операций на вкладке **Накладная** в группе **Журналы** выберите **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-143">To review the posted facture, on the Action Pane, on the **Invoice** tab, in the **Journals** group, select **Facture**.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-144">Чтобы разнести счет-фактуру для нескольких заказов на покупку, на странице **Обновить счет-фактуру** выберите **Выбрать**, затем выберите заказы, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-144">To post a facture for several purchase orders, on the **Update facture** page, select **Select**, and then select the orders that should be processed.</span></span>

### <a name="process-a-facture-based-on-the-posted-purchase-order-invoice"></a><span data-ttu-id="bb5d7-145">Обработка счета-фактуры на основе разрешенной накладной заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="bb5d7-145">Process a facture based on the posted purchase order invoice</span></span>
<span data-ttu-id="bb5d7-146">Шаги этой процедуры в основном совпадают с шагами предыдущей процедуры, "Обработка счета-фактуры без разноски накладной заказа на покупку".</span><span class="sxs-lookup"><span data-stu-id="bb5d7-146">The steps in this procedure are basically the same as the steps in the previous procedure, Process a facture without posting a purchase order invoice.</span></span> <span data-ttu-id="bb5d7-147">Однако на шаге 1 выполняется разноска накладной из заказа на покупку обычным способом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-147">However, in step 1, you post the invoice from the purchase order in the standard way.</span></span>

### <a name="process-a-facture-based-on-the-product-receipt-of-a-purchase-order"></a><span data-ttu-id="bb5d7-148">Обработка счета-фактуры на основе поступления продуктов заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="bb5d7-148">Process a facture based on the product receipt of a purchase order</span></span>
<span data-ttu-id="bb5d7-149">Вы можете разнести счета-фактуры, основанные на поступлениях продуктов, которые содержат разные типы строк заказа.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-149">You can post factures that are based on product receipts that include different types of order lines.</span></span>

1. <span data-ttu-id="bb5d7-150">Выполните разноску поступления продуктов из заказа на покупку обычным способом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-150">Post the product receipt from the purchase order in the standard way.</span></span>
2. <span data-ttu-id="bb5d7-151">На странице **Заказ на покупку** на панели операций на вкладке **Накладная** в группе **Создать** выберите **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-151">On the **Purchase order** page, on the Action Pane, on the **Invoice** tab, in the\*\* Generate\*\* group, select **Facture**.</span></span>
3. <span data-ttu-id="bb5d7-152">В нижней части страницы пометьте накладную или накладные получения продуктов, которые должны быть включены, затем выберите **OK**, чтобы разнести счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-152">In the lower part of the page, mark the product receipt invoice or invoices that should be included, and then select **OK** to post the facture.</span></span>

## <a name="process-factures-from-the-purchase-invoice-journal"></a><span data-ttu-id="bb5d7-153">Обработка счетов-фактур из журнала накладных по покупке</span><span class="sxs-lookup"><span data-stu-id="bb5d7-153">Process factures from the purchase invoice journal</span></span>
<span data-ttu-id="bb5d7-154">Можно обрабатывать счета-фактуры покупок из списка всех разнесенных накладных.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-154">You can process purchase factures from the list of all posted invoices.</span></span>

1. <span data-ttu-id="bb5d7-155">Перейдите в раздел **Расчеты с поставщиками** \> **Запросы и отчеты** \> **Накладная** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-155">Go to **Accounts payable** \> **Inquiries and reports** \> **Invoice** \> **Invoice journal**.</span></span>
2. <span data-ttu-id="bb5d7-156">Выберите разнесенную накладную для обновления счета-фактуры, затем на вкладке **Обзор** выберите **Создать счет-фактуру** > **Обновления счета-фактуры**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-156">Select the posted invoice to update the facture for, and then, on the **Overview** tab, select **Create facture** > **Update facture**.</span></span>
3. <span data-ttu-id="bb5d7-157">В верхней части страницы **Обновить счет-фактуру** на вкладке **Обзор** в поле **Счет-фактура** введите номер счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-157">In the upper part of the **Update facture** page, on the **Overview** tab, in the **Facture** field, enter the facture number.</span></span>
4. <span data-ttu-id="bb5d7-158">В поле **Дата регистрации** введите дату регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-158">In the **Date of the registration** field, select the facture registration date.</span></span>
5. <span data-ttu-id="bb5d7-159">В поле **Дата фактуры** выберите дату создания счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-159">In the **Facture date** field, select the facture creation date.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-160">Дата создания счета-фактуры совпадает с датой регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-160">The facture creation date is the same as the facture registration date.</span></span> <span data-ttu-id="bb5d7-161">Значение этого поля можно изменить только в том случае, если для параметра "Та же" установлено значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="bb5d7-161">You can change the value of this field only if you set the Same as option to No.</span></span>

6. <span data-ttu-id="bb5d7-162">В нижней части страницы на вкладке **Накладная** выберите накладные для счета-фактуры с помощью флажка **В фактуру**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-162">In the lower part of the page, on the **Invoice** tab, select the **To facture** check box for the invoice or invoices for the facture.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-163">Если для строки накладной не следует создавать счет-фактуру, снимите флажок **В фактуру** для этой строки на вкладке **Строки накладной**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-163">If you don't want to create a facture for an invoice line, clear the **To facture** check box for that line on the **Invoice lines** tab.</span></span>

7. <span data-ttu-id="bb5d7-164">На панели действий выберите **Разноска** \> **Обновление и печать**, чтобы разнести и распечатать счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-164">On the Action Pane, select **Posting** \> **Update and print** to post and print the facture.</span></span>
<span data-ttu-id="bb5d7-165">–или– Выберите **Разноска** \> **Обновление**, чтобы обновить счет-фактуру без вывода ее на печать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-165">–or– Select **Posting** \> **Update** to update the facture without printing it.</span></span>
<span data-ttu-id="bb5d7-166">–или– Выберите **Разноска** \> **Печать**, чтобы распечатать счет-фактуру без ее обновления.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-166">–or– Select **Posting** \> **Print** to print the facture without posting it.</span></span>

8. <span data-ttu-id="bb5d7-167">Можно просмотреть фактуру, созданную путем выбора счета-фактуры, на вкладке **Обзор** страницы **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-167">You can view the facture that is created by selecting Facture on the **Overview** tab of the **Invoice journal** page.</span></span>

## <a name="view-factures-in-the-purchase-facture-journal"></a><span data-ttu-id="bb5d7-168">Просмотр счетов-фактур в журнале счетов-фактур покупок</span><span class="sxs-lookup"><span data-stu-id="bb5d7-168">View factures in the purchase facture journal</span></span>
<span data-ttu-id="bb5d7-169">Просмотреть и распечатать счета-фактуры можно на странице **Журнал счетов-фактур** (**Расчеты с поставщиками** \> **Запросы и отчеты** \> **Счет-фактура**).</span><span class="sxs-lookup"><span data-stu-id="bb5d7-169">You can view and print factures on the **Facture journal** page (**Accounts payable** \> **Inquiries and reports** \> **Facture**).</span></span> <span data-ttu-id="bb5d7-170">Выберите счет-фактуру, затем на панели операций выберите **Печать** \> **Оригинал** для печати исходного счета-фактуры, выберите **Печать** \> **Копия** для печати копии или выберите **Удалить** для удаления счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-170">Select the facture, and then, on the Action Pane, select **Print** \> **Original** to print the original facture select **Print** \> **Copy** to print a copy, or select **Delete** to delete the facture.</span></span>

<span data-ttu-id="bb5d7-171">В верхней части страницы отображаются сведения о сведениях о счете-фактуре.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-171">The upper part of the page shows information about the facture information.</span></span> <span data-ttu-id="bb5d7-172">Эти сведения включают номер счета-фактуры, дату регистрации, дату счета-фактуры, сумму (включая и исключая налог), сумму налога, валюту и счет по накладной.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-172">This information includes the facture number, date of the registration, facture date, amount (including and excluding tax), sales tax amount, currency, and invoice account.</span></span>

<span data-ttu-id="bb5d7-173">В нижней части страницы отображаются сведения о строках накладной на двух вкладках:</span><span class="sxs-lookup"><span data-stu-id="bb5d7-173">The lower part of the page shows information about the invoice lines on two tabs:</span></span>
-   <span data-ttu-id="bb5d7-174">**Обзор** — на этой вкладке отображается код номенклатуры, наименование продукта, количество единицы измерения цены, сумма в валюте проводки, цена и сумма налога по строке.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-174">**Overview** – This tab shows the item code, product name, price unit quantity, amount in the transaction currency, price, and sales tax amount per line.</span></span>
-   <span data-ttu-id="bb5d7-175">**Аналитики продукта** — на этой вкладке отображаются аналитики сайта, склада и продукта.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-175">**Product dimensions** – This tab shows the site, warehouse, and product dimensions.</span></span>

## <a name="process-and-print-invoice-factures-for-sales-orders"></a><span data-ttu-id="bb5d7-176">Обработка и печать счетов-фактур по накладным для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="bb5d7-176">Process and print invoice-factures for sales orders</span></span>
<span data-ttu-id="bb5d7-177">При регистрации накладной создаются проводки, затем создается счет-фактура.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-177">When an invoice is registered, transactions are created, and then the facture is generated.</span></span> <span data-ttu-id="bb5d7-178">Этот процесс завершает продажу.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-178">This process completes the sale.</span></span>

### <a name="process-a-facture-without-posting-the-invoice-for-a-sales-order"></a><span data-ttu-id="bb5d7-179">Обработка счета-фактуры без разноски накладной для заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="bb5d7-179">Process a facture without posting the invoice for a sales order</span></span>
<span data-ttu-id="bb5d7-180">Можно обработать счет-фактуру без разноски накладной.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-180">You can process a facture without posting an invoice.</span></span> <span data-ttu-id="bb5d7-181">В этом случае накладная автоматически разносится при обработке счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-181">In this case, the invoice is automatically posted when the facture is processed.</span></span>

1. <span data-ttu-id="bb5d7-182">На странице **Все заказы на продажу** на панели операций на вкладке **Накладная** в группе **Создать** выберите **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-182">On the **All sales orders** page, on the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Facture**.</span></span>
2. <span data-ttu-id="bb5d7-183">В верхней части страницы **Обновить счет-фактуру** задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="bb5d7-183">In the upper part of the **Update facture** page, set the following fields:</span></span>

  - <span data-ttu-id="bb5d7-184">**Дата регистрации** — выберите дату регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-184">**Date of the registration** – Select the facture registration date.</span></span>
  - <span data-ttu-id="bb5d7-185">**Дата счета-фактуры** — выберите дату создания счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-185">**Facture date** – Select the facture creation date.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bb5d7-186">Дата создания счета-фактуры совпадает с датой регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-186">The facture creation date is the same as the facture registration date.</span></span> <span data-ttu-id="bb5d7-187">Значение этого поля можно изменить только в том случае, если для параметра **Та же** установлено значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-187">You can change the value of this field only if you set the **Same as** option to **No**.</span></span>

  - <span data-ttu-id="bb5d7-188">**Группа номерных серий** — выберите группу номерных серий, чтобы назначать разным клиентам или поставщикам различные номерные серии.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-188">**Number sequence group** – Select the number sequence group to allocate different number sequences to different customers or vendors.</span></span>
  
  > [!NOTE]
  > <span data-ttu-id="bb5d7-189">Ссылка используется при применении альтернативной нумерации документов для счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-189">The reference is used if alternative document numbering is applied for the facture.</span></span>

  - <span data-ttu-id="bb5d7-190">**Счет-фактура** — (необязательно) выберите свободный номер счета-фактуры, если ранее был удален счет-фактура.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-190">**Facture** – (Optional) Select the free facture number if you previously deleted a facture.</span></span> <span data-ttu-id="bb5d7-191">Если свободный номер счета-фактуры не выбран, для нового счета-фактуры будет назначен самый низкий свободный номер счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-191">If you don't select the free facture number, the lowest free facture number will be assigned to the new facture.</span></span> <span data-ttu-id="bb5d7-192">Это поведение является стандартным для непрерывной нумерации номерных серий.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-192">This behavior is standard for continuous numbering of number sequences.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bb5d7-193">Если вы ранее не удаляли счета-фактуры, поле счета-фактуры нельзя редактировать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-193">If you didn't previously delete any factures, the Facture field isn't editable.</span></span>
  
3. <span data-ttu-id="bb5d7-194">В нижней части страницы отметьте накладную или накладные, которые должны быть включены в обработку счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-194">In the lower part of the page, mark the invoice or invoices that should be included in the facture processing.</span></span>
4. <span data-ttu-id="bb5d7-195">На панели действий выберите **Разноска** \> **Обновление и печать**, чтобы разнести и распечатать счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-195">On the Action Pane, select **Posting** \> **Update and print** to post and print the facture.</span></span>
<span data-ttu-id="bb5d7-196">–или– Выберите **Разноска** \> **Обновление**, чтобы обновить счет-фактуру без вывода ее на печать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-196">–or– Select **Posting** \> **Update** to update the facture without printing it.</span></span>
<span data-ttu-id="bb5d7-197">–или– Выберите **Разноска** \> **Печать**, чтобы распечатать счет-фактуру без ее обновления.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-197">–or– Select **Posting** \> **Print** to print the facture without posting it.</span></span>

5. <span data-ttu-id="bb5d7-198">Можно просмотреть разнесенные счета-фактуры, выбрав **Счет-фактура** в **Группа журналов** на вкладке **Накладная** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-198">You can review the posted facture by selecting **Facture** in the **Journals group** on the **Invoice** tab of the Action Pane.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-199">Чтобы разнести счет-фактуру для нескольких заказов на продажу, на странице **Обновить счет-фактуру** выберите **Выбрать**, затем выберите заказы, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-199">To post a facture for several sales orders, on the **Update facture** page, select **Select**, and then select the orders that should be processed.</span></span>

### <a name="process-a-facture-based-on-a-posted-invoice-for-a-sales-order"></a><span data-ttu-id="bb5d7-200">Обработка счета-фактуры на основе разрешенной накладной заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="bb5d7-200">Process a facture based on a posted invoice for a sales order</span></span>
<span data-ttu-id="bb5d7-201">Шаги этой процедуры в основном совпадают с шагами предыдущей процедуры, "Обработка счета-фактуры без разноски накладной для заказа на продажу".</span><span class="sxs-lookup"><span data-stu-id="bb5d7-201">The steps in this procedure are basically the same as the steps in the previous procedure, Process a facture without posting the invoice for a sales order.</span></span> <span data-ttu-id="bb5d7-202">Однако на шаге 1 выполняется разноска накладной из заказа на продажу обычным способом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-202">However, in step 1, you post the invoice from the sales order in the standard way.</span></span>

### <a name="process-a-facture-based-on-packing-slips-for-sales-orders"></a><span data-ttu-id="bb5d7-203">Обработка счета-фактуры на основе отборочных накладных для заказов на продажу</span><span class="sxs-lookup"><span data-stu-id="bb5d7-203">Process a facture based on packing slips for sales orders</span></span>
<span data-ttu-id="bb5d7-204">Вы можете разнести счета-фактуры, основанные на отборочных накладных, которые содержат разные типы строк заказа.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-204">You can post factures that are based on packing slips that include different types of order lines.</span></span>

1. <span data-ttu-id="bb5d7-205">Выполните разноску отборочной накладной из заказа на продажу стандартным способом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-205">Post the packing slip from the sales order in the standard way.</span></span>
2. <span data-ttu-id="bb5d7-206">На странице **Заказ на продажу** на панели операций на вкладке **Накладная** в группе **Создать** выберите **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-206">On the **Sales order** page, on the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Facture**.</span></span>
3. <span data-ttu-id="bb5d7-207">В нижней части страницы пометьте накладную или накладные отборочной накладной, которые должны быть включены, затем выберите **OK**, чтобы разнести счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-207">In the lower part of the page, mark the packing slip invoice or invoices that should be included, and then select **OK** to post the facture.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-208">Основанные на категориях строки заказа на продажу содержат номер грузовой таможенной декларации (ГТД) и страну или регион происхождения.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-208">Sales order lines that are based on categories contain the customs cargo declaration (GTD) number, and the country or region of origin.</span></span> <span data-ttu-id="bb5d7-209">Эти сведения переносятся в журнал фактур при обновлении счета-фактуры для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-209">These details are transferred to the facture journal when you update a facture for a sales order.</span></span>
> <span data-ttu-id="bb5d7-210">В результате разноски счета-фактуры система обрабатывает накладную и разносит счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-210">As a result of facture posting, the system processes the invoice and posts the facture.</span></span>

### <a name="process-a-facture-based-on-recurring-invoices"></a><span data-ttu-id="bb5d7-211">Обработка счета-фактуры на основе периодических накладных</span><span class="sxs-lookup"><span data-stu-id="bb5d7-211">Process a facture based on recurring invoices</span></span>
<span data-ttu-id="bb5d7-212">Для выполнения периодического создания счета-фактуры выберите **Расчеты с клиентами** \> **Накладные** \> **Пакетное выставление накладных** \> **Счет-фактура**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-212">To run periodic facture creation, go to **Accounts receivable** \> **Invoices** \> **Batch invoicing** \> **Facture**.</span></span>

### <a name="process-invoice-factures-for-a-free-text-invoice"></a><span data-ttu-id="bb5d7-213">Обработка счетов-фактур по накладным для накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="bb5d7-213">Process invoice-factures for a free text invoice</span></span>

1. <span data-ttu-id="bb5d7-214">Перейдите в раздел **Расчеты с клиентами** \> **Накладные** \> **Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-214">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="bb5d7-215">Выберите **Создать**, чтобы создать накладную с произвольным текстом, затем введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-215">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="bb5d7-216">Выберите **Разнести**, чтобы выполнить разноску накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-216">Select **Post** to post the free text invoice.</span></span>
4. <span data-ttu-id="bb5d7-217">На панели операций на вкладке **Накладная** в группе **Разнести** выберите **Обновить счет-фактуру**, чтобы создать счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-217">On the Action Pane, on the **Invoice** tab, in the **Post** group, select **Update facture** to create the facture.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-218">Можно обработать счет-фактуру без разноски накладной с произвольным текстом.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-218">You can process a facture without posting a free text invoice.</span></span> <span data-ttu-id="bb5d7-219">В этом случае накладная автоматически разносится при обработке счета-фактуры.\*\*</span><span class="sxs-lookup"><span data-stu-id="bb5d7-219">In this case, the invoice is automatically posted when the facture is processed.\*\*</span></span>

### <a name="process-invoice-factures-from-sales-invoice-journal"></a><span data-ttu-id="bb5d7-220">Обработка счетов-фактур по накладным из журнала накладных по продаже</span><span class="sxs-lookup"><span data-stu-id="bb5d7-220">Process invoice-factures from sales invoice journal</span></span>
<span data-ttu-id="bb5d7-221">Можно обрабатывать счета-фактуры продажи из списка всех разнесенных накладных.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-221">You can process sales factures from the list of all posted invoices.</span></span>

1. <span data-ttu-id="bb5d7-222">Перейдите в раздел **Расчеты с клиентами** \> **Запросы и отчеты** \> **Накладные** \> **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-222">Go to **Accounts receivable** \> **Inquiries and reports** \> **Invoices** \> **Invoice journal**.</span></span>
2. <span data-ttu-id="bb5d7-223">Выберите накладную, связанную со счетом фактурой, который необходимо обновить, затем на панели операций на вкладке **Накладная** выберите **Создать счет-фактуру** \> **Обновление счета-фактуры**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-223">Select the invoice that is associated with the facture that must be updated, and then, on the Action Pane, on the **Invoice** tab, select **Create facture** \> **Update facture**.</span></span>
3. <span data-ttu-id="bb5d7-224">В поле **Группа номерных серий** выберите группу номерных серий, чтобы назначать разным клиентам или поставщикам различные номерные серии.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-224">In the **Number sequence group** field, select the number sequence group to allocate different number sequences to different customers or vendors.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-225">Ссылка используется при применении альтернативной нумерации документов для счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-225">The reference is used if an alternative document numbering is applied for the facture.</span></span>

4. <span data-ttu-id="bb5d7-226">В поле **Дата регистрации** введите дату регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-226">In the **Date of the registration** field, select the facture registration date.</span></span>
5. <span data-ttu-id="bb5d7-227">В поле **Дата фактуры** выберите дату создания счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-227">In the **Facture date** field, select the facture creation date.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-228">Дата создания счета-фактуры совпадает с датой регистрации счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-228">The facture creation date is the same as the facture registration date.</span></span> <span data-ttu-id="bb5d7-229">Значение этого поля можно изменить только в том случае, если для параметра **Та же** установлено значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-229">You can change the value of this field only if you set the **Same as** option to **No**.</span></span>

6. <span data-ttu-id="bb5d7-230">В нижней части страницы на вкладке **Накладная** выберите накладные для счета-фактуры с помощью флажка **В фактуру**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-230">In the lower part of the page, on the **Invoice** tab, use the **To facture** check box to select the invoice or invoices for the facture.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d7-231">Если для строки накладной не следует создавать счет-фактуру, снимите флажок **В фактуру** для этой строки на вкладке **Строки накладной**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-231">If you don't want to create a facture for an invoice line, clear the **To facture** check box for the line on the **Invoice lines** tab.</span></span>

7.  <span data-ttu-id="bb5d7-232">На панели действий выберите **Разноска** \> **Обновление и печать**, чтобы обновить и распечатать счет-фактуру.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-232">On the Action Pane, select **Posting** \> **Update and print** to update and print the facture.</span></span>
<span data-ttu-id="bb5d7-233">–или– Выберите **Разноска** \> **Обновление**, чтобы обновить счет-фактуру без вывода ее на печать.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-233">–or– Select **Posting** \> **Update** to update the facture without printing it.</span></span>
<span data-ttu-id="bb5d7-234">–или– Выберите **Разноска** \> **Печать**, чтобы распечатать счет-фактуру без ее обновления.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-234">–or– Select **Posting** \> **Print** to print the facture without posting it.</span></span>

8.  <span data-ttu-id="bb5d7-235">Можно просмотреть фактуру, созданную путем выбора **Счет-фактура** на вкладке **Обзор** страницы **Журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-235">You can view the facture that is created by selecting **Facture** on the **Overview** tab of the **Invoice journal** page.</span></span>

### <a name="view-factures-in-the-sales-facture-journal"></a><span data-ttu-id="bb5d7-236">Просмотр счетов-фактур в журнале счетов-фактур продажи</span><span class="sxs-lookup"><span data-stu-id="bb5d7-236">View factures in the sales facture journal</span></span>
<span data-ttu-id="bb5d7-237">Просмотреть и распечатать все счета-фактуры можно на странице **Журнал счетов-фактур** (**Расчеты с клиентами** \> **Запросы и отчеты** \> **Счет-фактура**).</span><span class="sxs-lookup"><span data-stu-id="bb5d7-237">You can view and print all factures on the **Facture journal** page (**Accounts receivable** \> **Inquiries and reports** \> **Facture**).</span></span> <span data-ttu-id="bb5d7-238">Выберите счет-фактуру, затем на панели операций выберите **Печать** \> **Оригинал** для печати исходного счета-фактуры, выберите **Печать** \> **Копия** для печати копии или выберите **Удалить** для удаления счета-фактуры.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-238">Select the facture, and then, on the Action Pane, select **Print** \> **Original** to print original facture, select **Print** \> **Copy** to print a copy, or select **Delete** to delete the facture.</span></span>

<span data-ttu-id="bb5d7-239">В верхней части страницы отображаются сведения о счете-фактуре.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-239">The upper part of the page shows information about the facture.</span></span> <span data-ttu-id="bb5d7-240">Эти сведения включают номер счета-фактуры, дату регистрации, дату счета-фактуры, сумму (включая и исключая налог), сумму налога, валюту и счет по накладной.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-240">This information includes, the facture number, date of the registration, facture date, amount (including and excluding tax), tax amount, currency, and invoice account.</span></span>

<span data-ttu-id="bb5d7-241">В нижней части страницы отображаются сведения о строках накладной.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-241">The lower part of the page shows information about the invoice lines.</span></span> <span data-ttu-id="bb5d7-242">Эти сведения включают номер накладной, код номенклатуры, категорию, наименование продукта, цену, количество единиц, сумма в валюте проводки и цену.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-242">This information includes the invoice number, item code, category, product name, price, unit quantity, amount in the transaction currency, and price.</span></span> <span data-ttu-id="bb5d7-243">На вкладке **Обзор** отображается сумма налога по строкам, а на вкладке **Аналитики продукта** отображаются сведения об узле, складе и другой информации об аналитике продукта.</span><span class="sxs-lookup"><span data-stu-id="bb5d7-243">The **Overview** tab shows the sales tax amount per line, and the **Product dimensions** tab shows the site, warehouse, and other product dimension information.</span></span>
