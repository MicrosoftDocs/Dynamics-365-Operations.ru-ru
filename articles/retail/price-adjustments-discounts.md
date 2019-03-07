---
title: Корректировки цены и скидки
description: В этой статье представлена информация о корректировках цен и скидок в Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "350972"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="3b19c-103">Корректировки цены и скидки</span><span class="sxs-lookup"><span data-stu-id="3b19c-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b19c-104">В этой статье представлена информация о корректировках цен и скидок в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3b19c-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="3b19c-105">В Dynamics 365 for Retail можно вносить корректировки цен на продукты, а также настраивать скидки, которые будут применяться к номенклатуре строки или проводке в POS, в заказе на продажу центра обработки вызовов или в заказе через Интернет.</span><span class="sxs-lookup"><span data-stu-id="3b19c-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="3b19c-106">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="3b19c-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="3b19c-107">Как для корректировок цен, так и для скидок вы можете определить однократные дату начала и дату окончания или период повторения, код скидки и несколько дополнительных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="3b19c-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="3b19c-108">Корректировки цен и скидки применяются к продукции, вариантам или категориям.</span><span class="sxs-lookup"><span data-stu-id="3b19c-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="3b19c-109">Если к продукту применяется более одной скидки, клиент мог получить или одну из скидок, или совмещенную скидку, в зависимости от конфигурации скидки.</span><span class="sxs-lookup"><span data-stu-id="3b19c-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="3b19c-110">Dynamics 365 for Retail автоматически применяет скидку или сочетания скидок, которые обеспечивают самую лучшую цену для клиента.</span><span class="sxs-lookup"><span data-stu-id="3b19c-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="3b19c-111">Когда вы настраиваете корректировку цены или скидку, обязательно убедитесь, что группы цены назначены правильным каналам, каталогам, назначениям или программам лояльности, к которым вы хотите применить скидку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="3b19c-112">Кроме того, если требуется автоматически создать код скидки, можно настроить номерные серии на странице **Параметры розничной торговли** перед определением новой корректировки цены или скидки.</span><span class="sxs-lookup"><span data-stu-id="3b19c-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="3b19c-113">Можно удалить корректировку цен или скидку.</span><span class="sxs-lookup"><span data-stu-id="3b19c-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="3b19c-114">Однако статистическая информация при этом будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="3b19c-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="3b19c-115">Типы скидок</span><span class="sxs-lookup"><span data-stu-id="3b19c-115">Types of discounts</span></span>

<span data-ttu-id="3b19c-116">Доступно четыре типа розничных скидок:</span><span class="sxs-lookup"><span data-stu-id="3b19c-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="3b19c-117">**Простая скидка** — один процент или сумма.</span><span class="sxs-lookup"><span data-stu-id="3b19c-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="3b19c-118">**Скидка за количество** — скидка, которая применяется при покупке двух и более продуктов.</span><span class="sxs-lookup"><span data-stu-id="3b19c-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="3b19c-119">**Скидка за комплект** — скидка, которая применяется при покупке конкретного набора продуктов.</span><span class="sxs-lookup"><span data-stu-id="3b19c-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="3b19c-120">**Скидка за пороговое значение** — скидка, которая применяется, когда общая сумма проводки больше указанного значения.</span><span class="sxs-lookup"><span data-stu-id="3b19c-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="3b19c-121">Корректировки цен и скидки можно связать с ценовыми группами.</span><span class="sxs-lookup"><span data-stu-id="3b19c-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="3b19c-122">Ценовые группы можно затем связать с каналами, каталогами, назначениями и программами лояльности.</span><span class="sxs-lookup"><span data-stu-id="3b19c-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
