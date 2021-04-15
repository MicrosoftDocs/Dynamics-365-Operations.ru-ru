---
title: Модуль адреса доставки
description: В этом разделе описываются модуль адреса доставки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795437"
---
# <a name="shipping-address-module"></a><span data-ttu-id="5e7db-103">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="5e7db-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e7db-104">В этом разделе описываются модуль адреса доставки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e7db-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5e7db-105">Модуль адреса доставки позволяет клиентам добавлять или выбирать адрес доставки для заказа во время потока оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="5e7db-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="5e7db-106">Если клиент вошел в систему, отображаются все адреса, ранее сохраненные для этого клиента, и клиент может выбрать один из этих адресов.</span><span class="sxs-lookup"><span data-stu-id="5e7db-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="5e7db-107">Клиент также может добавить новый адрес.</span><span class="sxs-lookup"><span data-stu-id="5e7db-107">The customer can also add a new address.</span></span> <span data-ttu-id="5e7db-108">Модуль адреса доставки используется для всех номенклатур в заказе, для которых требуется доставка.</span><span class="sxs-lookup"><span data-stu-id="5e7db-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="5e7db-109">Форматы адресов отгрузки можно определить в Commerce headquarters для каждой страны или региона, а затем в модуле адреса отгрузки будут использоваться правила для определенных стран и регионов.</span><span class="sxs-lookup"><span data-stu-id="5e7db-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="5e7db-110">Когда клиенты вводят адрес доставки во время потока оформления заказа, они имеют возможность сохранить адрес как основной адрес.</span><span class="sxs-lookup"><span data-stu-id="5e7db-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="5e7db-111">Этот параметр отображается только в том случае, если клиент вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="5e7db-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="5e7db-112">Хотя модуль адреса доставки не обеспечивает проверку адресов, эта функция может быть реализована посредством настройки.</span><span class="sxs-lookup"><span data-stu-id="5e7db-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="5e7db-113">На следующем рисунке показан пример нового модуля адреса доставки на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="5e7db-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Пример модуля адреса доставки на странице оформления заказа](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="5e7db-115">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="5e7db-115">Module properties</span></span>

| <span data-ttu-id="5e7db-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="5e7db-116">Property name</span></span> | <span data-ttu-id="5e7db-117">Значения</span><span class="sxs-lookup"><span data-stu-id="5e7db-117">Values</span></span> | <span data-ttu-id="5e7db-118">описание</span><span class="sxs-lookup"><span data-stu-id="5e7db-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5e7db-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5e7db-119">Heading</span></span> | <span data-ttu-id="5e7db-120">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="5e7db-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5e7db-121">Необязательный заголовок для модуля адреса доставки.</span><span class="sxs-lookup"><span data-stu-id="5e7db-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="5e7db-122">Показать тип адрес</span><span class="sxs-lookup"><span data-stu-id="5e7db-122">Show address type</span></span> | <span data-ttu-id="5e7db-123">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5e7db-123">**True** or **False**</span></span> | <span data-ttu-id="5e7db-124">Если для этого дополнительного свойства установлено значение **Истина**, будет показан тип адреса, например, **домашний** или **Рабочий**.</span><span class="sxs-lookup"><span data-stu-id="5e7db-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="5e7db-125">Если тип адреса не указан, адрес будет автоматически сохранен как **Тип**=**другой**.</span><span class="sxs-lookup"><span data-stu-id="5e7db-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="5e7db-126">Включить автоматическое предложение</span><span class="sxs-lookup"><span data-stu-id="5e7db-126">Enable auto suggestion</span></span>| <span data-ttu-id="5e7db-127">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5e7db-127">**True** or **False**</span></span> | <span data-ttu-id="5e7db-128">Если для этого дополнительного свойства установлено значение **True**, будут предоставлены автоматические варианты адресов.</span><span class="sxs-lookup"><span data-stu-id="5e7db-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="5e7db-129">Эти предложения основаны на Картах Bing.</span><span class="sxs-lookup"><span data-stu-id="5e7db-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="5e7db-130">Сведения о том, как настроить интеграцию Карт Bing для вашего сайта, см. в разделе [модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5e7db-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="5e7db-131">Эта функция доступна в Commerce версии 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="5e7db-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="5e7db-132">Параметры автоматического предложения</span><span class="sxs-lookup"><span data-stu-id="5e7db-132">Auto suggest options</span></span>| <span data-ttu-id="5e7db-133">Номер</span><span class="sxs-lookup"><span data-stu-id="5e7db-133">A number</span></span>| <span data-ttu-id="5e7db-134">Если включены автоматические предложения адресов, можно указать дополнительные параметры, такие как максимальное число предлагаемых вариантов.</span><span class="sxs-lookup"><span data-stu-id="5e7db-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="5e7db-135">Добавление модуля адреса доставки на страницу оформления заказа и задание необходимых свойств</span><span class="sxs-lookup"><span data-stu-id="5e7db-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="5e7db-136">Модуль адреса доставки может быть добавлен только в модуль оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="5e7db-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="5e7db-137">Дополнительные сведения о настройке модуля адреса доставки и его добавлении к странице оформления заказа см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5e7db-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e7db-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5e7db-138">Additional resources</span></span>

[<span data-ttu-id="5e7db-139">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="5e7db-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5e7db-140">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="5e7db-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5e7db-141">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="5e7db-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5e7db-142">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="5e7db-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5e7db-143">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="5e7db-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="5e7db-144">Информационный модуль отправки</span><span class="sxs-lookup"><span data-stu-id="5e7db-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="5e7db-145">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="5e7db-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5e7db-146">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="5e7db-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="5e7db-147">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="5e7db-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]