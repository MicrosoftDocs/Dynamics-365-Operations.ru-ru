---
title: Синхронизация с ядром ценообразования Dynamics 365 Supply Chain Management по запросу
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
ms.openlocfilehash: 740ae20704abd9c59f64c2c7622fa96d65dccb1d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997154"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="9fee0-103">Синхронизация с ядром ценообразования Dynamics 365 Supply Chain Management по запросу</span><span class="sxs-lookup"><span data-stu-id="9fee0-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="9fee0-104">Microsoft Dynamics 365 Supply Chain Management включает в себя механизм ценообразования, который обрабатывает торговые договора, прайс-листы, программы лояльности клиентов, рекламные акции и скидки.</span><span class="sxs-lookup"><span data-stu-id="9fee0-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="9fee0-105">Механизм ценообразования использует сложные правила для определения наилучшей цены для данного предложения или заказа.</span><span class="sxs-lookup"><span data-stu-id="9fee0-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="9fee0-106">При использовании двойной записи можно использовать как статическое ценообразование, так и механизм ценообразования из Dynamics 365 Supply Chain Management на страницах предложения и заказа в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9fee0-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="9fee0-107">Использование механизма ценообразования из Supply Chain Management в Sales</span><span class="sxs-lookup"><span data-stu-id="9fee0-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="9fee0-108">В Sales выберите **Продажи \> Заказы**.</span><span class="sxs-lookup"><span data-stu-id="9fee0-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="9fee0-109">Выберите **Создать** , чтобы создать новый заказ, или выберите существующий заказ в списке **Мои заказы**.</span><span class="sxs-lookup"><span data-stu-id="9fee0-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="9fee0-110">Добавьте новую строку заказа.</span><span class="sxs-lookup"><span data-stu-id="9fee0-110">Add a new order line.</span></span>
4. <span data-ttu-id="9fee0-111">При создании нового заказа выберите **Рассчитать цену заказа** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="9fee0-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="9fee0-112">При обновлении существующего заказа выберите **Пересчитать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="9fee0-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="9fee0-113">Следующие поля автоматически заполняются:</span><span class="sxs-lookup"><span data-stu-id="9fee0-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="9fee0-114">Детальная сумма</span><span class="sxs-lookup"><span data-stu-id="9fee0-114">Detail Amount</span></span>
    + <span data-ttu-id="9fee0-115">% скидки</span><span class="sxs-lookup"><span data-stu-id="9fee0-115">Discount %</span></span>
    + <span data-ttu-id="9fee0-116">Скидка</span><span class="sxs-lookup"><span data-stu-id="9fee0-116">Discount</span></span>
    + <span data-ttu-id="9fee0-117">Сумма без фрахта</span><span class="sxs-lookup"><span data-stu-id="9fee0-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="9fee0-118">Сумма фрахта</span><span class="sxs-lookup"><span data-stu-id="9fee0-118">Freight Amount</span></span>
    + <span data-ttu-id="9fee0-119">Итоговый налог</span><span class="sxs-lookup"><span data-stu-id="9fee0-119">Total Tax</span></span>
    + <span data-ttu-id="9fee0-120">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="9fee0-120">Total Amount</span></span>
    
5. <span data-ttu-id="9fee0-121">Чтобы убедиться в том, что система учитывает торговые договора и договора продажи для расчета цены:</span><span class="sxs-lookup"><span data-stu-id="9fee0-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="9fee0-122">Перейдите в среду Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9fee0-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="9fee0-123">Перейдите в раздел **Расчеты с клиентами \> Настройка \> Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="9fee0-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="9fee0-124">Перейдите на вкладку **Цены** на расположенной выше панели навигации.</span><span class="sxs-lookup"><span data-stu-id="9fee0-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="9fee0-125">На экспресс-вкладке **Оценка коммерческого договора** отметьте выбора параметра **Ручной ввод**.</span><span class="sxs-lookup"><span data-stu-id="9fee0-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="9fee0-126">Как это работает</span><span class="sxs-lookup"><span data-stu-id="9fee0-126">How it works</span></span>

<span data-ttu-id="9fee0-127">При выборе пункта **Рассчитать цену заказа** в Sales функция **Итоговые значения** на вкладке **Заказ на продажу \> Просмотр** в Supply Chain Management вызывается для связанного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="9fee0-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="9fee0-128">Значения в итоговой сумме заказа в Sales используются для заполнения соответствующих полей в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9fee0-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="9fee0-129">При расчете итога по заказу на продажу в Supply Chain Management в расчете оцениваются существующие торговые договоры и договоры продажи для клиента и продуктов, перечисленных в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="9fee0-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="9fee0-130">Эти сведения используются при расчете итоговых сумм.</span><span class="sxs-lookup"><span data-stu-id="9fee0-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="9fee0-131">При выборе пункта **Рассчитать цену заказа** Sales автоматически отражает все настройки, выполненные в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9fee0-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="9fee0-132">Ограничения</span><span class="sxs-lookup"><span data-stu-id="9fee0-132">Limitations</span></span>

<span data-ttu-id="9fee0-133">Когда поля в Sales заполнены, действуют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="9fee0-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="9fee0-134">Настройка накладных расходов и распределения расходов в Supply Chain Management не воспроизводится в Sales.</span><span class="sxs-lookup"><span data-stu-id="9fee0-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="9fee0-135">В ценах не учитывается специальная розничная цена, указанная в поле **Канал розничной торговли** на странице строки заказа на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9fee0-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="9fee0-136">Скидки, которые определены в разделе **Управление торговыми скидками** Supply Chain Management не рассматриваются.</span><span class="sxs-lookup"><span data-stu-id="9fee0-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
