---
title: Синхронизация по требованию с механизмом ценообразования Supply Chain Management
description: В этом разделе описывается, как использовать механизм ценообразования в Microsoft Dynamics 365 Supply Chain Management из Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130661"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="91542-103">Синхронизация по требованию с механизмом ценообразования Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="91542-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="91542-104">Microsoft Dynamics 365 Supply Chain Management включает в себя механизм ценообразования, который обрабатывает торговые договора, прайс-листы, программы лояльности клиентов, рекламные акции и скидки.</span><span class="sxs-lookup"><span data-stu-id="91542-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="91542-105">Механизм ценообразования использует сложные правила для определения наилучшей цены для данного предложения или заказа.</span><span class="sxs-lookup"><span data-stu-id="91542-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="91542-106">При использовании двойной записи можно использовать как статическое ценообразование, так и механизм ценообразования из Dynamics 365 Supply Chain Management на страницах предложения и заказа в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="91542-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="91542-107">Использование механизма ценообразования из Supply Chain Management в Sales</span><span class="sxs-lookup"><span data-stu-id="91542-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="91542-108">В Sales выберите **Продажи \> Заказы**.</span><span class="sxs-lookup"><span data-stu-id="91542-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="91542-109">Выберите **Создать**, чтобы создать новый заказ, или выберите существующий заказ в списке **Мои заказы**.</span><span class="sxs-lookup"><span data-stu-id="91542-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="91542-110">Добавьте новую строку заказа.</span><span class="sxs-lookup"><span data-stu-id="91542-110">Add a new order line.</span></span>
4. <span data-ttu-id="91542-111">При создании нового заказа выберите **Рассчитать цену заказа** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="91542-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="91542-112">При обновлении существующего заказа выберите **Пересчитать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="91542-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="91542-113">Следующие столбцы автоматически заполняются:</span><span class="sxs-lookup"><span data-stu-id="91542-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="91542-114">Детальная сумма</span><span class="sxs-lookup"><span data-stu-id="91542-114">Detail Amount</span></span>
    + <span data-ttu-id="91542-115">% скидки</span><span class="sxs-lookup"><span data-stu-id="91542-115">Discount %</span></span>
    + <span data-ttu-id="91542-116">Скидка</span><span class="sxs-lookup"><span data-stu-id="91542-116">Discount</span></span>
    + <span data-ttu-id="91542-117">Сумма без фрахта</span><span class="sxs-lookup"><span data-stu-id="91542-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="91542-118">Сумма фрахта</span><span class="sxs-lookup"><span data-stu-id="91542-118">Freight Amount</span></span>
    + <span data-ttu-id="91542-119">Итоговый налог</span><span class="sxs-lookup"><span data-stu-id="91542-119">Total Tax</span></span>
    + <span data-ttu-id="91542-120">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="91542-120">Total Amount</span></span>
    
5. <span data-ttu-id="91542-121">Чтобы убедиться в том, что система учитывает торговые договора и договора продажи для расчета цены:</span><span class="sxs-lookup"><span data-stu-id="91542-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="91542-122">Перейдите в среду Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91542-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="91542-123">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="91542-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="91542-124">Перейдите на вкладку **Цены** на расположенной выше панели навигации.</span><span class="sxs-lookup"><span data-stu-id="91542-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="91542-125">На экспресс-вкладке **Оценка коммерческого договора** отметьте выбора параметра **Ручной ввод**.</span><span class="sxs-lookup"><span data-stu-id="91542-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="91542-126">Как это работает</span><span class="sxs-lookup"><span data-stu-id="91542-126">How it works</span></span>

<span data-ttu-id="91542-127">При выборе пункта **Рассчитать цену заказа** в Sales функция **Итоговые значения** на вкладке **Заказ на продажу \> Просмотр** в Supply Chain Management вызывается для связанного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="91542-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="91542-128">Значения в итоговой сумме заказа в Sales используются для заполнения соответствующих столбцов в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91542-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="91542-129">При расчете итога по заказу на продажу в Supply Chain Management в расчете оцениваются существующие торговые договоры и договоры продажи для клиента и продуктов, перечисленных в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="91542-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="91542-130">Эти сведения используются при расчете итоговых сумм.</span><span class="sxs-lookup"><span data-stu-id="91542-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="91542-131">При выборе пункта **Рассчитать цену заказа** Sales автоматически отражает все настройки, выполненные в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91542-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="91542-132">Ограничения</span><span class="sxs-lookup"><span data-stu-id="91542-132">Limitations</span></span>

<span data-ttu-id="91542-133">Когда столбцы в Sales заполнены, действуют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="91542-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="91542-134">Настройка накладных расходов и распределения расходов в Supply Chain Management не воспроизводится в Sales.</span><span class="sxs-lookup"><span data-stu-id="91542-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="91542-135">В ценах не учитывается специальная розничная цена, указанная в столбце **Канал розничной торговли** на странице строки заказа на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91542-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="91542-136">Скидки, которые определены в разделе **Управление торговыми скидками** Supply Chain Management не рассматриваются.</span><span class="sxs-lookup"><span data-stu-id="91542-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
