---
title: Корректировки цены и скидки
description: В этой статье представлена информация о корректировках цен и скидок в Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240950"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="ed3ff-103">Корректировки цены и скидки</span><span class="sxs-lookup"><span data-stu-id="ed3ff-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed3ff-104">В этой статье представлена информация о корректировках цен и скидок в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ed3ff-105">В Commerce можно вносить корректировки цен на продукты, а также настраивать скидки, которые будут применяться к номенклатуре строки или проводке в POS, в заказе на продажу центра обработки вызовов или в заказе через Интернет.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="ed3ff-106">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="ed3ff-107">Как для корректировок цен, так и для скидок вы можете определить однократные дату начала и дату окончания или период повторения, код скидки и несколько дополнительных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="ed3ff-108">Корректировки цен и скидки применяются к продукции, вариантам или категориям.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="ed3ff-109">Если к продукту применяется более одной скидки, клиент мог получить или одну из скидок, или совмещенную скидку, в зависимости от конфигурации скидки.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="ed3ff-110">Commerce автоматически применяет скидку или сочетания скидок, которые обеспечивают самую лучшую цену для клиента.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="ed3ff-111">Когда вы настраиваете корректировку цены или скидку, обязательно убедитесь, что группы цены назначены правильным каналам, каталогам, назначениям или программам лояльности, к которым вы хотите применить скидку.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="ed3ff-112">Кроме того, если требуется автоматически создать код скидки, можно настроить номерные серии на странице **Параметры Commerce** перед определением новой корректировки цены или скидки.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="ed3ff-113">Можно удалить корректировку цен или скидку.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="ed3ff-114">Однако статистическая информация при этом будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="ed3ff-115">Типы скидок</span><span class="sxs-lookup"><span data-stu-id="ed3ff-115">Types of discounts</span></span>

<span data-ttu-id="ed3ff-116">Доступно много типов скидок:</span><span class="sxs-lookup"><span data-stu-id="ed3ff-116">There are many types of discounts:</span></span>

- <span data-ttu-id="ed3ff-117">**Простая скидка** — один процент или сумма.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="ed3ff-118">**Скидка за количество** — скидка, которая применяется при покупке двух и более продуктов.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="ed3ff-119">**Скидка за комплект** — скидка, которая применяется при покупке конкретного набора продуктов.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="ed3ff-120">**Скидка за пороговое значение** — скидка, которая применяется, когда общая сумма проводки больше указанного значения.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="ed3ff-121">**Скидки на основе платежных средств** — скидка, которая применяется, когда итог проводки превышает указанную сумму, и для оплаты используется определенный тип платежа (например, наличные деньги, кредитная или дебетовая карта).</span><span class="sxs-lookup"><span data-stu-id="ed3ff-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="ed3ff-122">**Скидка на доставку** — скидка, которая применяется, когда общая сумма проводки превышает указанную сумму и конкретный способ поставки (например, поставка через два дня или на следующий день) используется для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="ed3ff-123">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="ed3ff-124">Ценовые группы можно затем связать с каналами, каталогами, назначениями и программами лояльности.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="ed3ff-125">Скидка на комплект и скидка по порогу имеют свойства с именами "Учитывать не подлежащие скидке продукты" и "Учитывать не подлежащие скидке продукты при расчете порога", соответственно.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="ed3ff-126">Если эти свойства включены, номенклатура, на которую не распространяется скидка, все еще может помочь квалифицировать проводку для скидки, но неподходящий номенклатура не получит скидку.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="ed3ff-127">Например, если вы создаете скидку на комплект с двумя строками, A и B, где клиент должен получить скидку 10% на оба товара, но у товара А отмечена конфигурация "Запретить все скидки", то при этом, как правило, товар А не включается в скидку.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="ed3ff-128">Однако если свойство "Учитывать не подлежащие скидке продукты" включено, то товар А может быть использован для получения права на скидку, но скидка в размере 10% будет применяться только к товару B. Аналогичная логика применима к пороговой скидке.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="ed3ff-129">Однако свойство "Учитывать не подлежащие скидке продукты при расчете порога" имеет дополнительную возможность по сравнению со свойством "Учитывать не подлежащие скидке продукты" скидок на комплект.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="ed3ff-130">Если пороговая скидка включена, и если есть товар, который имеет существующую скидку, которая не позволит товару получить какие-либо другие скидки, то цена, уплаченная за этот товар, будет учитываться при расчете порога, но этот товар не получит дополнительную скидку.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
