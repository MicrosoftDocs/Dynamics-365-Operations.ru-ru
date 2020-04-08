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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173185"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="6425f-103">Синхронизация с ядром ценообразования Dynamics 365 Supply Chain Management по запросу</span><span class="sxs-lookup"><span data-stu-id="6425f-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6425f-104">Microsoft Dynamics 365 Supply Chain Management включает в себя механизм ценообразования, который обрабатывает торговые договора, прайс-листы, программы лояльности клиентов, рекламные акции и скидки.</span><span class="sxs-lookup"><span data-stu-id="6425f-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="6425f-105">Механизм ценообразования использует сложные правила для определения наилучшей цены для данного предложения или заказа.</span><span class="sxs-lookup"><span data-stu-id="6425f-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="6425f-106">При использовании двойной записи можно использовать как статическое ценообразование, так и механизм ценообразования из Dynamics 365 Supply Chain Management на страницах предложения и заказа в Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6425f-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="6425f-107">Использование механизма ценообразования из Supply Chain Management в Sales</span><span class="sxs-lookup"><span data-stu-id="6425f-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="6425f-108">В Sales выберите **Продажи \> Заказы**.</span><span class="sxs-lookup"><span data-stu-id="6425f-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="6425f-109">Выберите **Создать**, чтобы создать новый заказ, или выберите существующий заказ в списке **Мои заказы**.</span><span class="sxs-lookup"><span data-stu-id="6425f-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="6425f-110">Добавьте новую строку заказа.</span><span class="sxs-lookup"><span data-stu-id="6425f-110">Add a new order line.</span></span>
4. <span data-ttu-id="6425f-111">При создании нового заказа выберите **Рассчитать цену заказа** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="6425f-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="6425f-112">При обновлении существующего заказа выберите **Пересчитать** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="6425f-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="6425f-113">Следующие поля автоматически заполняются:</span><span class="sxs-lookup"><span data-stu-id="6425f-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="6425f-114">Детальная сумма</span><span class="sxs-lookup"><span data-stu-id="6425f-114">Detail Amount</span></span>
    + <span data-ttu-id="6425f-115">% скидки</span><span class="sxs-lookup"><span data-stu-id="6425f-115">Discount %</span></span>
    + <span data-ttu-id="6425f-116">Скидка</span><span class="sxs-lookup"><span data-stu-id="6425f-116">Discount</span></span>
    + <span data-ttu-id="6425f-117">Сумма без фрахта</span><span class="sxs-lookup"><span data-stu-id="6425f-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="6425f-118">Сумма фрахта</span><span class="sxs-lookup"><span data-stu-id="6425f-118">Freight Amount</span></span>
    + <span data-ttu-id="6425f-119">Итоговый налог</span><span class="sxs-lookup"><span data-stu-id="6425f-119">Total Tax</span></span>
    + <span data-ttu-id="6425f-120">Итоговая сумма</span><span class="sxs-lookup"><span data-stu-id="6425f-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="6425f-121">Как это работает</span><span class="sxs-lookup"><span data-stu-id="6425f-121">How it works</span></span>

<span data-ttu-id="6425f-122">При выборе пункта **Рассчитать цену заказа** в Sales функция **Итоговые значения** на вкладке **Заказ на продажу \> Просмотр** в Supply Chain Management вызывается для связанного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="6425f-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="6425f-123">Значения в итоговой сумме заказа в Sales используются для заполнения соответствующих полей в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6425f-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="6425f-124">При расчете итога по заказу на продажу в Supply Chain Management в расчете оцениваются существующие торговые договоры и договоры продажи для клиента и продуктов, перечисленных в заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="6425f-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="6425f-125">Эти сведения используются при расчете итоговых сумм.</span><span class="sxs-lookup"><span data-stu-id="6425f-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="6425f-126">При выборе пункта **Рассчитать цену заказа** Sales автоматически отражает все настройки, выполненные в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6425f-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="6425f-127">Ограничения</span><span class="sxs-lookup"><span data-stu-id="6425f-127">Limitations</span></span>

<span data-ttu-id="6425f-128">Когда поля в Sales заполнены, действуют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="6425f-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="6425f-129">Настройка накладных расходов и распределения расходов в Supply Chain Management не воспроизводится в Sales.</span><span class="sxs-lookup"><span data-stu-id="6425f-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="6425f-130">В ценах не учитывается специальная розничная цена, указанная в поле **Канал розничной торговли** на странице строки заказа на продажу в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6425f-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="6425f-131">Скидки, которые определены в разделе **Управление торговыми скидками** Supply Chain Management не рассматриваются.</span><span class="sxs-lookup"><span data-stu-id="6425f-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
