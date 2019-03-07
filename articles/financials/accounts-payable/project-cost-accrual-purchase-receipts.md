---
title: Начисление затрат по проекту по приходам покупки
description: В этой теме описывается, как начисленные затраты по проекту по приходам покупки можно отслеживать в Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc822652abbba68f094fe5b8a65f796165a92c4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "340438"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="ccb6c-103">Начисление затрат по проекту по приходам покупки</span><span class="sxs-lookup"><span data-stu-id="ccb6c-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccb6c-104">В этой теме описывается, как начисленные затраты по проекту по приходам покупки можно отслеживать в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="ccb6c-105">Накладные по проекту часто поступают позже, чем доставляются товары и услуги, что может оказать значительное влияние на ключевые индикаторы производительности (KPI) проекта.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="ccb6c-106">Важно иметь возможность отслеживать эти проводки в финансовых и проектных отчетах.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="ccb6c-107">Этот иллюстрирует следующий пример сценария.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="ccb6c-108">Компания Contoso Consulting запустила новый проекта развертывания в облаке.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="ccb6c-109">Создается заказ на покупку для приобретения компьютера для проекта.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="ccb6c-110">Компьютер будет стоить 1500 долларов США, а услуги по установке будут стоить 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="ccb6c-111">Поставщик доставил и установил компьютер, но накладная еще не поступила в компанию Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="ccb6c-112">Руководитель проекта хотел бы видеть начисление затрат на проект в сумме 1650 долларов до поступления накладной.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="ccb6c-113">Эти затраты должны также отражаться в финансовых отчетах компании на конец месяца.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="ccb6c-114">Для целей отчетности начисленные расходы должны записываться как на финансовом уровне, так и на уровне проекта.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="ccb6c-115">В Finance and Operations финансовое обновление прихода продуктов можно отслеживать для номенклатур и категорий закупок.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="ccb6c-116">Для номенклатур на странице **Параметры модуля расчетов с поставщиками** выберите параметр **Разноска поступления продуктов в ГК**.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="ccb6c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="ccb6c-118">Для категорий закупок на странице закупаемой продукции на **Правило политики категории** выберите политики **Покупка**, затем выберите **Начислить расходы на покупку при оприходовании** для каждой категории закупок.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="ccb6c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="ccb6c-120">Счета **Расходы по закупкам, не выставлены накладные** и **Покупка, начисление** в **Настройка разноски** будут использоваться при разноске ваучеров, связанных с приходом продуктов.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="ccb6c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="ccb6c-122">Используя этот же сценарий, посмотрим, как разноска поступления продуктов повлияет на сведения в главной книге и сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="ccb6c-123">**Шаг 1.** Создание и подтверждение нового заказ на покупку для проекта, чтобы записать покупку компьютера за 1500 долларов США и услуг по установке за 150 долларов США.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="ccb6c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="ccb6c-125">При подтверждении заказа на покупку создаются проводки для подтвержденных затрат по проекту.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="ccb6c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="ccb6c-127">Проводки для подтвержденных затрат будут иметь в поле **Источник проводки** значение **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="ccb6c-128">Создание и подтверждения заказа на покупку не создает проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="ccb6c-129">**Шаг 2.** Товары и услуги доставляются, и зарегистрируется приход продуктов.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="ccb6c-130">Разноска прихода продуктов создаст и разнесет ваучер в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="ccb6c-131">Ваучер дебетует счет расходов по закупкам, по которым не выставлены накладные, и кредитует счет начислений покупки.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="ccb6c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ccb6c-133">Разноска прихода продуктов будет использовать настройку разноски для категории закупки и продуктов, а не настройку разноски для категорий проекта.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="ccb6c-134">Чтобы правильно отразить финансовое влияние начислений за покупку, необходимо скорректировать эту настройку.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="ccb6c-135">Имеется возможность сопоставить категории закупаемой продукции с категориями проекта на странице **Категория закупаемой продукции**.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="ccb6c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="ccb6c-137">**Шаг 3.** Создание черновика накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="ccb6c-138">В Finance and Operations разноска прихода продуктов не влияет на сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="ccb6c-139">Для обхода этой проблемы можно создать черновик накладной поставщика сразу после разноски прихода покупки.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="ccb6c-140">Откройте страницу **Заказ на покупку** &gt; **вкладку "Накладная"** &gt; **Создать** &gt; **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="ccb6c-141">При этом создается документ ожидающей обработки накладной, который обновляет сведения о проекте.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="ccb6c-142">Создание черновика накладной поставщика приведет к созданию ожидающих проводок по проекту.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="ccb6c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="ccb6c-144">На странице **Подтвержденные затраты** записи, созданные на шаге 1, будут закрыты, и будут созданы новые записи для отражения подтверждения затрат, вызванных ожидающей накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="ccb6c-145">В поле **Источник проводки** для подтвержденных затрат будет указано **Накладная поставщика**.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="ccb6c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="ccb6c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="ccb6c-147">Накладная поставщика останется в состоянии ожидания, пока не поступит фактическая накладная поставщика.</span><span class="sxs-lookup"><span data-stu-id="ccb6c-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



