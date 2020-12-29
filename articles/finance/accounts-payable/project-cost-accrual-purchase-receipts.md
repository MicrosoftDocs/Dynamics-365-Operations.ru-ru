---
title: Начисление затрат по проекту по приходам покупки
description: В этой теме описывается, как начисленные затраты по проекту по приходам покупки можно отслеживать в Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a930b4921a29d5ce561ce0e958733f0c3261b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447158"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="9fa89-103">Начисление затрат по проекту по приходам покупки</span><span class="sxs-lookup"><span data-stu-id="9fa89-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fa89-104">В этой теме описывается, как начисленные затраты по проекту по приходам покупки можно отслеживать в Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9fa89-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="9fa89-105">Накладные по проекту часто поступают позже, чем доставляются товары и услуги, что может оказать значительное влияние на ключевые индикаторы производительности (KPI) проекта.</span><span class="sxs-lookup"><span data-stu-id="9fa89-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="9fa89-106">Важно иметь возможность отслеживать эти проводки в финансовых и проектных отчетах.</span><span class="sxs-lookup"><span data-stu-id="9fa89-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="9fa89-107">Этот иллюстрирует следующий пример сценария.</span><span class="sxs-lookup"><span data-stu-id="9fa89-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="9fa89-108">Компания Contoso Consulting запустила новый проекта развертывания в облаке.</span><span class="sxs-lookup"><span data-stu-id="9fa89-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="9fa89-109">Создается заказ на покупку для приобретения компьютера для проекта.</span><span class="sxs-lookup"><span data-stu-id="9fa89-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="9fa89-110">Компьютер будет стоить 1500 долларов США, а услуги по установке будут стоить 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="9fa89-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="9fa89-111">Поставщик доставил и установил компьютер, но накладная еще не поступила в компанию Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="9fa89-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="9fa89-112">Руководитель проекта хотел бы видеть начисление затрат на проект в сумме 1650 долларов до поступления накладной.</span><span class="sxs-lookup"><span data-stu-id="9fa89-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="9fa89-113">Эти затраты должны также отражаться в финансовых отчетах компании на конец месяца.</span><span class="sxs-lookup"><span data-stu-id="9fa89-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="9fa89-114">Для целей отчетности начисленные расходы должны записываться как на финансовом уровне, так и на уровне проекта.</span><span class="sxs-lookup"><span data-stu-id="9fa89-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="9fa89-115">Финансовое обновление прихода продуктов можно отслеживать для номенклатур и категорий закупок.</span><span class="sxs-lookup"><span data-stu-id="9fa89-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="9fa89-116">Для номенклатур на странице **Параметры модуля расчетов с поставщиками** выберите параметр **Разноска поступления продуктов в ГК**.</span><span class="sxs-lookup"><span data-stu-id="9fa89-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="9fa89-117">[![Страница "Параметры модуля расчетов с поставщиками"](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="9fa89-118">Для категорий закупок на странице закупаемой продукции на **Правило политики категории** выберите политики **Покупка**, затем выберите **Начислить расходы на покупку при оприходовании** для каждой категории закупок.</span><span class="sxs-lookup"><span data-stu-id="9fa89-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="9fa89-119">[![Страница "Правило политики категории"](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="9fa89-120">Счета **Расходы по закупкам, не выставлены накладные** и **Покупка, начисление** в **Настройка разноски** будут использоваться при разноске ваучеров, связанных с приходом продуктов.</span><span class="sxs-lookup"><span data-stu-id="9fa89-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="9fa89-121">Используя этот же сценарий, посмотрим, как разноска поступления продуктов повлияет на сведения в главной книге и сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="9fa89-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="9fa89-122">**Шаг 1.** Создание и подтверждение нового заказ на покупку для проекта, чтобы записать покупку компьютера за 1500 долларов США и услуг по установке за 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="9fa89-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="9fa89-123">[![Создание нового заказа на покупку](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="9fa89-124">При подтверждении заказа на покупку создаются проводки для подтвержденных затрат по проекту.</span><span class="sxs-lookup"><span data-stu-id="9fa89-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="9fa89-125">[![Созданные проводки](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="9fa89-126">Проводки для подтвержденных затрат будут иметь в поле **Источник проводки** значение **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="9fa89-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="9fa89-127">Создание и подтверждения заказа на покупку не создает проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="9fa89-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="9fa89-128">**Шаг 2.** Товары и услуги доставляются, и зарегистрируется приход продуктов.</span><span class="sxs-lookup"><span data-stu-id="9fa89-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="9fa89-129">Разноска прихода продуктов создаст и разнесет ваучер в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="9fa89-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="9fa89-130">Ваучер дебетует счет расходов по закупкам, по которым не выставлены накладные, и кредитует счет начислений покупки.</span><span class="sxs-lookup"><span data-stu-id="9fa89-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="9fa89-131">[![Проводки ваучера](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9fa89-132">Разноска прихода продуктов будет использовать настройку разноски для категории закупки и продуктов, а не настройку разноски для категорий проекта.</span><span class="sxs-lookup"><span data-stu-id="9fa89-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="9fa89-133">Чтобы правильно отразить финансовое влияние начислений за покупку, необходимо скорректировать эту настройку.</span><span class="sxs-lookup"><span data-stu-id="9fa89-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="9fa89-134">Имеется возможность сопоставить категории закупаемой продукции с категориями проекта на странице **Категория закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="9fa89-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="9fa89-135">[![Страница "Категория закупаемой продукции"](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="9fa89-136">**Шаг 3.** Создание черновика накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="9fa89-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="9fa89-137">Разноска прихода продуктов не влияет на сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="9fa89-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="9fa89-138">Для обхода этой проблемы можно создать черновик накладной поставщика сразу после разноски прихода покупки.</span><span class="sxs-lookup"><span data-stu-id="9fa89-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="9fa89-139">Откройте страницу **Заказ на покупку** &gt; **вкладку "Накладная"** &gt; **Создать** &gt; **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="9fa89-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="9fa89-140">При этом создается документ ожидающей обработки накладной, который обновляет сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="9fa89-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="9fa89-141">Создание черновика накладной поставщика приведет к созданию ожидающих проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="9fa89-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="9fa89-142">[![Ожидающие проводки по проекту](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="9fa89-143">На странице **Подтвержденные затраты** записи, созданные на шаге 1, будут закрыты, и будут созданы новые записи для отражения подтверждения затрат, вызванных ожидающей накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="9fa89-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="9fa89-144">В поле **Источник проводки** для подтвержденных затрат будет указано **Накладная поставщика**.</span><span class="sxs-lookup"><span data-stu-id="9fa89-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="9fa89-145">[![Страница "Подтвержденные затраты"](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="9fa89-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="9fa89-146">Накладная поставщика останется в состоянии ожидания, пока не поступит фактическая накладная поставщика.</span><span class="sxs-lookup"><span data-stu-id="9fa89-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



