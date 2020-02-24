---
title: Корректировки розничных цен
description: Эта процедура содержит инструкции по созданию корректировки коммерческой цены.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd6459416ca42530401aa439b1b8511657bd9b36
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023787"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="52350-103">Корректировки розничных цен</span><span class="sxs-lookup"><span data-stu-id="52350-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="52350-104">Эта процедура содержит инструкции по созданию корректировки коммерческой цены.</span><span class="sxs-lookup"><span data-stu-id="52350-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="52350-105">Корректировка цены может задавать цену продажи номенклатуры напрямую или изменят базовую цену продажи и цену продажи из коммерческого соглашения.</span><span class="sxs-lookup"><span data-stu-id="52350-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="52350-106">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="52350-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="52350-107">Щелкните "Управление ценообразованием и скидками".</span><span class="sxs-lookup"><span data-stu-id="52350-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="52350-108">Щелкните вкладку "Корректировки цены".</span><span class="sxs-lookup"><span data-stu-id="52350-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="52350-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="52350-109">Click New.</span></span>
    * <span data-ttu-id="52350-110">Здесь можно создать все наиболее часто используемые правила цен и скидок, включая скидки, корректировки цен, журналы коммерческих соглашений и правил ценообразования категории.</span><span class="sxs-lookup"><span data-stu-id="52350-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="52350-111">Щелкните "Ценовая коррекция".</span><span class="sxs-lookup"><span data-stu-id="52350-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="52350-112">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="52350-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="52350-113">Разверните раздел "Строки".</span><span class="sxs-lookup"><span data-stu-id="52350-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="52350-114">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="52350-114">Click Add.</span></span>
    * <span data-ttu-id="52350-115">Например, введите в поле "Продукт" значение "81126".</span><span class="sxs-lookup"><span data-stu-id="52350-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="52350-116">Затем введите "10.0" в поле "Процент скидки".</span><span class="sxs-lookup"><span data-stu-id="52350-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="52350-117">Корректировка цены типа процента скидки уменьшает базовую цену продажи или цену продажи из коммерческого соглашения.</span><span class="sxs-lookup"><span data-stu-id="52350-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="52350-118">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="52350-118">Click Add.</span></span>
    * <span data-ttu-id="52350-119">Например, введите в поле "Продукт" значение "81125".</span><span class="sxs-lookup"><span data-stu-id="52350-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="52350-120">Затем выберите "Сумма скидки по оплате" в поле "Способ скидки".</span><span class="sxs-lookup"><span data-stu-id="52350-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="52350-121">Наконец, введите "5.0" в поле "Сумма скидки по оплате".</span><span class="sxs-lookup"><span data-stu-id="52350-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="52350-122">Тип скидки "Сумма скидки по оплате" представляет собой сумму, на которую уменьшается базовая цена или цена из коммерческого соглашения.</span><span class="sxs-lookup"><span data-stu-id="52350-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="52350-123">Щелкните "Ценовые группы".</span><span class="sxs-lookup"><span data-stu-id="52350-123">Click Price groups.</span></span>
    * <span data-ttu-id="52350-124">В поле "Группа цен" введите "RP-Houston".</span><span class="sxs-lookup"><span data-stu-id="52350-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="52350-125">Это свяжет корректировку цены с магазином в Хьюстоне.</span><span class="sxs-lookup"><span data-stu-id="52350-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="52350-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52350-126">Click Save.</span></span>
11. <span data-ttu-id="52350-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52350-127">Close the page.</span></span>
12. <span data-ttu-id="52350-128">В поле "Состояние" выберите "Включено".</span><span class="sxs-lookup"><span data-stu-id="52350-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="52350-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="52350-129">Click Save.</span></span>
14. <span data-ttu-id="52350-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="52350-130">Close the page.</span></span>
15. <span data-ttu-id="52350-131">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="52350-131">Refresh the page.</span></span>

