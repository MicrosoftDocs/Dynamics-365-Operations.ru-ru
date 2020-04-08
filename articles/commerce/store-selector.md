---
title: Модуль выбора магазина
description: В этом разделе описываются модуль выбора магазина, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157348"
---
# <a name="store-selector-module"></a><span data-ttu-id="49cd6-103">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="49cd6-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49cd6-104">В этом разделе описываются модуль выбора магазина, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49cd6-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49cd6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="49cd6-105">Overview</span></span>

<span data-ttu-id="49cd6-106">Модуль выбора магазина используется для сценария "купить в Интернете, забрать в магазине" (BOPIS).</span><span class="sxs-lookup"><span data-stu-id="49cd6-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="49cd6-107">В нем отображается список магазинов, в которых продукт доступен для получения, а также часы работы магазина и запасы товаров для каждого магазина.</span><span class="sxs-lookup"><span data-stu-id="49cd6-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="49cd6-108">Для модуля выбора магазина требуется контекст продукта и место поиска, чтобы найти магазины.</span><span class="sxs-lookup"><span data-stu-id="49cd6-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="49cd6-109">При отсутствии места поиска по умолчанию используется местонахождение браузера клиента, при условии, что клиент дает согласие.</span><span class="sxs-lookup"><span data-stu-id="49cd6-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="49cd6-110">В модуле имеется поле ввода, позволяющее клиенту ввести местонахождение (почтовый индекс или город и регион), чтобы найти ближайшие магазины.</span><span class="sxs-lookup"><span data-stu-id="49cd6-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="49cd6-111">Модуль выбора магазина встроен в интерфейс прикладного программирования (API) геокодирования карт Bing для преобразования местоположения, введенного клиентом, в широту и долготу.</span><span class="sxs-lookup"><span data-stu-id="49cd6-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="49cd6-112">Требуется ключ API карт Bing, который должен быть добавлен на страницу общих параметров Commerce в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49cd6-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="49cd6-113">Модуль выбора магазина можно добавить в модуль поля покупки на странице сведений о продукте (PDP), чтобы отображать магазины, в которых продукт доступен для получения.</span><span class="sxs-lookup"><span data-stu-id="49cd6-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="49cd6-114">Его также можно добавить в модуль корзины.</span><span class="sxs-lookup"><span data-stu-id="49cd6-114">It can also be added to a cart module.</span></span> <span data-ttu-id="49cd6-115">При добавлении в модуль корзины в модуле выбора магазина отображаются параметры получения для каждого элемента строки корзины.</span><span class="sxs-lookup"><span data-stu-id="49cd6-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="49cd6-116">Кроме того, с помощью пользовательского кода этот модуль можно добавить на другие страницы или модули через расширения и настройки.</span><span class="sxs-lookup"><span data-stu-id="49cd6-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="49cd6-117">Для работы сценария BOPIS следует настроить режим доставки продуктов "самовывоз клиентом".</span><span class="sxs-lookup"><span data-stu-id="49cd6-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="49cd6-118">В противном случае модуль не будет отображаться на соответствующих страницах.</span><span class="sxs-lookup"><span data-stu-id="49cd6-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="49cd6-119">Подробные сведения о настройке режима доставки см. в разделе [Настройка способов доставки](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="49cd6-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="49cd6-120">На следующем рисунке показан пример модуля выбора магазина, используемого на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="49cd6-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Пример модуля выбора магазина](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="49cd6-122">Использование модуля выбора магазина в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="49cd6-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="49cd6-123">Модуль выбора магазина можно использовать на странице сведений о продукте (PDP) для поиска ближайших магазинов, в которых продукт доступен для получения.</span><span class="sxs-lookup"><span data-stu-id="49cd6-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="49cd6-124">Модуль выбора магазина можно использовать на странице корзины для поиска ближайших магазинов, в которых продукт из корзины доступен для получения.</span><span class="sxs-lookup"><span data-stu-id="49cd6-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="49cd6-125">Свойства модуля выбора магазина</span><span class="sxs-lookup"><span data-stu-id="49cd6-125">Store selector module properties</span></span>

| <span data-ttu-id="49cd6-126">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="49cd6-126">Property name</span></span>             | <span data-ttu-id="49cd6-127">значение</span><span class="sxs-lookup"><span data-stu-id="49cd6-127">Value</span></span>                 | <span data-ttu-id="49cd6-128">описание</span><span class="sxs-lookup"><span data-stu-id="49cd6-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="49cd6-129">Радиус поиска</span><span class="sxs-lookup"><span data-stu-id="49cd6-129">Search radius</span></span> | <span data-ttu-id="49cd6-130">Номер</span><span class="sxs-lookup"><span data-stu-id="49cd6-130">Number</span></span> | <span data-ttu-id="49cd6-131">Определяет радиус поиска магазинов, в милях.</span><span class="sxs-lookup"><span data-stu-id="49cd6-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="49cd6-132">Если значение не указано, используется радиус поиска по умолчанию в 50 миль.</span><span class="sxs-lookup"><span data-stu-id="49cd6-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="49cd6-133">Условия обслуживания</span><span class="sxs-lookup"><span data-stu-id="49cd6-133">Terms of Service</span></span> | <span data-ttu-id="49cd6-134">URL</span><span class="sxs-lookup"><span data-stu-id="49cd6-134">URL</span></span>    |  <span data-ttu-id="49cd6-135">URL-адрес ссылки на условия предоставления услуг, которая должна быть указана для службы карт Bing.</span><span class="sxs-lookup"><span data-stu-id="49cd6-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="49cd6-136">Добавление модуля выбора магазина на страницу</span><span class="sxs-lookup"><span data-stu-id="49cd6-136">Add a store selector module to a page</span></span>

<span data-ttu-id="49cd6-137">Модуль выбора магазина требует наличия контекста продукта, поэтому он может использоваться только в моделях поля покупки и корзины.</span><span class="sxs-lookup"><span data-stu-id="49cd6-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="49cd6-138">Модули выбора магазина не работают за пределами этих модулей.</span><span class="sxs-lookup"><span data-stu-id="49cd6-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="49cd6-139">Сведения о порядке добавления модуля выбора магазина в модуль поля покупки можно найти в разделе [Модуль поля покупки](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="49cd6-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="49cd6-140">Сведения о порядке добавления модуля выбора магазина в модуль корзины можно найти в разделе [Модуль корзины](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="49cd6-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49cd6-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="49cd6-141">Additional resources</span></span>

[<span data-ttu-id="49cd6-142">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="49cd6-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="49cd6-143">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="49cd6-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="49cd6-144">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="49cd6-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="49cd6-145">Краткий обзор страницы сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="49cd6-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="49cd6-146">Краткий обзор корзины и оформления заказа</span><span class="sxs-lookup"><span data-stu-id="49cd6-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="49cd6-147">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="49cd6-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
