---
title: Модуль адреса доставки
description: В этом разделе описываются модуль адреса доставки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "4415399"
---
# <a name="shipping-address-module"></a><span data-ttu-id="51835-103">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="51835-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51835-104">В этом разделе описываются модуль адреса доставки, а также описывается, как настраивать его в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51835-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="51835-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="51835-105">Overview</span></span>

<span data-ttu-id="51835-106">Модуль адреса доставки позволяет клиентам добавлять или выбирать адрес доставки для заказа во время потока оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="51835-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="51835-107">Если клиент вошел в систему, отображаются все адреса, ранее сохраненные для этого клиента, и клиент может выбрать один из этих адресов.</span><span class="sxs-lookup"><span data-stu-id="51835-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="51835-108">Клиент также может добавить новый адрес.</span><span class="sxs-lookup"><span data-stu-id="51835-108">The customer can also add a new address.</span></span> <span data-ttu-id="51835-109">Модуль адреса доставки используется для всех номенклатур в заказе, для которых требуется доставка.</span><span class="sxs-lookup"><span data-stu-id="51835-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="51835-110">Форматы адресов отгрузки можно определить в Commerce headquarters для каждой страны или региона, а затем в модуле адреса отгрузки будут использоваться правила для определенных стран и регионов.</span><span class="sxs-lookup"><span data-stu-id="51835-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="51835-111">Когда клиенты вводят адрес доставки во время потока оформления заказа, они имеют возможность сохранить адрес как основной адрес.</span><span class="sxs-lookup"><span data-stu-id="51835-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="51835-112">Этот параметр отображается только в том случае, если клиент вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="51835-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="51835-113">Хотя модуль адреса доставки не обеспечивает проверку адресов, эта функция может быть реализована посредством настройки.</span><span class="sxs-lookup"><span data-stu-id="51835-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="51835-114">На следующем рисунке показан пример нового модуля адреса доставки на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="51835-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Пример модуля адреса доставки на странице оформления заказа](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="51835-116">Свойства модуля</span><span class="sxs-lookup"><span data-stu-id="51835-116">Module properties</span></span>

| <span data-ttu-id="51835-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="51835-117">Property name</span></span> | <span data-ttu-id="51835-118">Значения</span><span class="sxs-lookup"><span data-stu-id="51835-118">Values</span></span> | <span data-ttu-id="51835-119">описание</span><span class="sxs-lookup"><span data-stu-id="51835-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="51835-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51835-120">Heading</span></span> | <span data-ttu-id="51835-121">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="51835-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="51835-122">Необязательный заголовок для модуля адреса доставки.</span><span class="sxs-lookup"><span data-stu-id="51835-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="51835-123">Показать тип адрес</span><span class="sxs-lookup"><span data-stu-id="51835-123">Show address type</span></span> | <span data-ttu-id="51835-124">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="51835-124">**True** or **False**</span></span> | <span data-ttu-id="51835-125">Если для этого дополнительного свойства установлено значение **Истина**, будет показан тип адреса, например, **домашний** или **Рабочий**.</span><span class="sxs-lookup"><span data-stu-id="51835-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="51835-126">Если тип адреса не указан, адрес будет автоматически сохранен как **Тип**=**другой**.</span><span class="sxs-lookup"><span data-stu-id="51835-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="51835-127">Добавление модуля адреса доставки на страницу оформления заказа и задание необходимых свойств</span><span class="sxs-lookup"><span data-stu-id="51835-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="51835-128">Модуль адреса доставки может быть добавлен только в модуль оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="51835-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="51835-129">Дополнительные сведения о настройке модуля адреса доставки и его добавлении к странице оформления заказа см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="51835-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51835-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51835-130">Additional resources</span></span>

[<span data-ttu-id="51835-131">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="51835-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="51835-132">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="51835-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="51835-133">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="51835-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="51835-134">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="51835-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="51835-135">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="51835-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="51835-136">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="51835-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="51835-137">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="51835-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="51835-138">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="51835-138">Gift card module</span></span>](add-giftcard.md)
