---
title: Модуль параметров доставки
description: В этом разделе описываются модули параметров поставки, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d0e5fa731d4b808cda9863074d17d1917410f399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213682"
---
# <a name="delivery-options-module"></a><span data-ttu-id="67a8a-103">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="67a8a-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67a8a-104">В этом разделе описываются модули параметров поставки, а также описывается, как настраивать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="67a8a-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="67a8a-105">Модули параметров поставки позволяют клиентам выбирать способ поставки, например, отгрузку или отправку для заказа в Интернете.</span><span class="sxs-lookup"><span data-stu-id="67a8a-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="67a8a-106">Адрес доставки требуется для определения режима доставки.</span><span class="sxs-lookup"><span data-stu-id="67a8a-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="67a8a-107">Если адрес доставки изменяется, необходимо снова извлечь варианты доставки.</span><span class="sxs-lookup"><span data-stu-id="67a8a-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="67a8a-108">Если заказ включает только номенклатуры, которые клиент заберет из магазина, этот модуль автоматически скрывается.</span><span class="sxs-lookup"><span data-stu-id="67a8a-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="67a8a-109">Сведения о настройке способов доставки см. в разделе [Настройка интернет-канала](channel-setup-online.md) и [Настройка способов поставки](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="67a8a-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="67a8a-110">Каждый способ поставки может иметь связанный расход.</span><span class="sxs-lookup"><span data-stu-id="67a8a-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="67a8a-111">Дополнительные сведения о настройке накладных расходов для интернет-магазина см. в разделе [Расширенные автоматические накладные расходы многоканального взаимодействия](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="67a8a-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="67a8a-112">В Commerce версии 10.0.13 модуль параметров доставки был обновлен для поддержки функций **накладные расходы в заголовке без пропорциональное распределение** и **отгрузка накладных расходов по строке**.</span><span class="sxs-lookup"><span data-stu-id="67a8a-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="67a8a-113">Если пропорциональное распределение отключено, ожидается, что workflow-процесс электронной коммерции не разрешит смешанный режим поставки для номенклатур в корзине (то есть, для отгрузки выбираются некоторые номенклатуры, но для отправки выбираются другие.)</span><span class="sxs-lookup"><span data-stu-id="67a8a-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="67a8a-114">Для функции **накладных расходов заголовка без пропорциональное распределение** требуется установить флажок **Включить согласованную обработку режима доставки в канале** в Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="67a8a-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="67a8a-115">Когда этот флаг включен, расходы на доставку применяются на уровне заголовка или на уровне строки, в зависимости от конфигурации в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="67a8a-115">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="67a8a-116">Тема "Fabrikam" поддерживает смешанный способ доставки, в которой некоторые номенклатуры выбираются для отгрузки, а другие выбираются для отправки.</span><span class="sxs-lookup"><span data-stu-id="67a8a-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="67a8a-117">В этом режиме расходы на доставку будут пропорционально распределены по всем номенклатурам, выбранным для способа доставки.</span><span class="sxs-lookup"><span data-stu-id="67a8a-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="67a8a-118">Для работы в смешанном режиме доставки необходимо сначала настроить функцию **накладных расходов заголовка с пропорциональным распределением** в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="67a8a-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="67a8a-119">Дополнительные сведения о данной конфигурации см. в разделе [Пропорциональное распределение накладных расходов из заголовка по соответствующим строкам продаж](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="67a8a-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="67a8a-120">Если расходы на доставку применяются к номенклатурам строки, они могут отображаться в строке корзины для каждой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="67a8a-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="67a8a-121">Для этой функциональности требуется **включить свойство Показать накладные расходы на отгрузку по номенклатуре строки** для модуля корзины и модуля оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="67a8a-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="67a8a-122">Дополнительные сведения см. в разделе [модуль корзины](add-cart-module.md) и [модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="67a8a-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="67a8a-123">На следующем рисунке показан пример модуля параметров поставки на странице оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="67a8a-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Пример модуля параметров доставки на странице оформления заказа](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="67a8a-125">Свойства модуля параметров доставки</span><span class="sxs-lookup"><span data-stu-id="67a8a-125">Delivery options module properties</span></span>

| <span data-ttu-id="67a8a-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="67a8a-126">Property</span></span> | <span data-ttu-id="67a8a-127">Значения</span><span class="sxs-lookup"><span data-stu-id="67a8a-127">Values</span></span> | <span data-ttu-id="67a8a-128">описание</span><span class="sxs-lookup"><span data-stu-id="67a8a-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="67a8a-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="67a8a-129">Heading</span></span> | <span data-ttu-id="67a8a-130">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="67a8a-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="67a8a-131">Необязательный заголовок для модуля параметров доставки.</span><span class="sxs-lookup"><span data-stu-id="67a8a-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="67a8a-132">Пользовательское имя класса CSS</span><span class="sxs-lookup"><span data-stu-id="67a8a-132">Custom CSS class name</span></span> | <span data-ttu-id="67a8a-133">Текст</span><span class="sxs-lookup"><span data-stu-id="67a8a-133">Text</span></span> | <span data-ttu-id="67a8a-134">Имя настраиваемого класса каскадных таблиц стилей (CSS), которое будет использоваться для преобразовать для просмотра данного модуля, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="67a8a-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="67a8a-135">Параметр фильтра способа доставки</span><span class="sxs-lookup"><span data-stu-id="67a8a-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="67a8a-136">**Не фильтровать** или **режимы, не связанные с отгрузкой**</span><span class="sxs-lookup"><span data-stu-id="67a8a-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="67a8a-137">Значение, указывающее, должен ли модуль параметров доставки отфильтровать все режимы доставки, не связанные с отгрузкой.</span><span class="sxs-lookup"><span data-stu-id="67a8a-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="67a8a-138">Добавление модуля параметров поставки на страницу оформления заказа и задание необходимых свойств</span><span class="sxs-lookup"><span data-stu-id="67a8a-138">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="67a8a-139">Модуль параметров поставки может быть добавлен только в модуль оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="67a8a-139">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="67a8a-140">Дополнительные сведения о настройке модуля параметров поставки и его добавлении к странице оформления заказа см. в разделе [Модуль оформления заказа](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="67a8a-140">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67a8a-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67a8a-141">Additional resources</span></span>

[<span data-ttu-id="67a8a-142">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="67a8a-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="67a8a-143">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="67a8a-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="67a8a-144">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="67a8a-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="67a8a-145">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="67a8a-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="67a8a-146">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="67a8a-146">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="67a8a-147">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="67a8a-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="67a8a-148">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="67a8a-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="67a8a-149">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="67a8a-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="67a8a-150">Расширенные автоматические накладные расходы многоканального взаимодействия</span><span class="sxs-lookup"><span data-stu-id="67a8a-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="67a8a-151">Пропорциональное распределение накладных расходов из заголовка по соответствующим строкам продаж</span><span class="sxs-lookup"><span data-stu-id="67a8a-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="67a8a-152">Настройка способов поставки</span><span class="sxs-lookup"><span data-stu-id="67a8a-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]