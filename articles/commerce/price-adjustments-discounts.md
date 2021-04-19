---
title: Корректировки цены и скидки
description: В этой статье представлена информация о корректировках цен и скидок в Dynamics 365 Commerce.
author: scott-tucker
ms.date: 11/16/2020
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
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802799"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="8356b-103">Корректировки цены и скидки</span><span class="sxs-lookup"><span data-stu-id="8356b-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8356b-104">В этой статье представлена информация о корректировках цен и скидок в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8356b-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8356b-105">В Commerce можно вносить корректировки цен на продукты, а также настраивать скидки, которые будут применяться к номенклатуре строки или проводке в POS, в заказе на продажу центра обработки вызовов или в заказе через Интернет.</span><span class="sxs-lookup"><span data-stu-id="8356b-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="8356b-106">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="8356b-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="8356b-107">Как для корректировок цен, так и для скидок вы можете определить однократные дату начала и дату окончания или период повторения, код скидки и несколько дополнительных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8356b-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="8356b-108">Корректировки цен и скидки применяются к продукции, вариантам или категориям.</span><span class="sxs-lookup"><span data-stu-id="8356b-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="8356b-109">Если к продукту применяется более одной скидки, клиент мог получить или одну из скидок, или совмещенную скидку, в зависимости от конфигурации скидки.</span><span class="sxs-lookup"><span data-stu-id="8356b-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="8356b-110">Commerce автоматически применяет скидку или сочетания скидок, которые обеспечивают самую лучшую цену для клиента.</span><span class="sxs-lookup"><span data-stu-id="8356b-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="8356b-111">Когда вы настраиваете корректировку цены или скидку, обязательно убедитесь, что группы цены назначены правильным каналам, каталогам, назначениям или программам лояльности, к которым вы хотите применить скидку.</span><span class="sxs-lookup"><span data-stu-id="8356b-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="8356b-112">Кроме того, если требуется автоматически создать код скидки, можно настроить номерные серии на странице **Параметры Commerce** перед определением новой корректировки цены или скидки.</span><span class="sxs-lookup"><span data-stu-id="8356b-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="8356b-113">Можно удалить корректировку цен или скидку.</span><span class="sxs-lookup"><span data-stu-id="8356b-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="8356b-114">Однако статистическая информация при этом будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="8356b-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="8356b-115">Типы скидок</span><span class="sxs-lookup"><span data-stu-id="8356b-115">Types of discounts</span></span>

<span data-ttu-id="8356b-116">Доступно много типов скидок:</span><span class="sxs-lookup"><span data-stu-id="8356b-116">There are many types of discounts:</span></span>

- <span data-ttu-id="8356b-117">**Простая скидка** — один процент или сумма.</span><span class="sxs-lookup"><span data-stu-id="8356b-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="8356b-118">**Скидка за количество** — скидка, которая применяется при покупке двух и более продуктов.</span><span class="sxs-lookup"><span data-stu-id="8356b-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="8356b-119">**Скидка за комплект** — скидка, которая применяется при покупке конкретного набора продуктов.</span><span class="sxs-lookup"><span data-stu-id="8356b-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="8356b-120">**Скидка за пороговое значение** — скидка, которая применяется, когда общая сумма проводки больше указанного значения.</span><span class="sxs-lookup"><span data-stu-id="8356b-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="8356b-121">**Скидки на основе платежных средств** — скидка, которая применяется, когда итог проводки превышает указанную сумму, и для оплаты используется определенный тип платежа (например, наличные деньги, кредитная или дебетовая карта).</span><span class="sxs-lookup"><span data-stu-id="8356b-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="8356b-122">**Скидка на доставку** — скидка, которая применяется, когда общая сумма проводки превышает указанную сумму и конкретный способ поставки (например, поставка через два дня или на следующий день) используется для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="8356b-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="8356b-123">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="8356b-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="8356b-124">Ценовые группы можно затем связать с каналами, каталогами, назначениями и программами лояльности.</span><span class="sxs-lookup"><span data-stu-id="8356b-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]