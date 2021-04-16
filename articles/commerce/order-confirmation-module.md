---
title: Модуль подтверждения заказа
description: В этом разделе описываются модули подтверждения заказа, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804585"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="a9a90-103">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="a9a90-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9a90-104">В этом разделе описываются модули подтверждения заказа, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9a90-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a9a90-105">После размещения заказа можно использовать модуль подтверждения заказа для отображения подробных сведений подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="a9a90-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="a9a90-106">Здесь отображается код подтверждения заказа, контактная информация заказа и другие сведения о заказе, такие как купленные номенклатуры, вариантах самовывоза и методе отгрузки.</span><span class="sxs-lookup"><span data-stu-id="a9a90-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="a9a90-107">Свойства модуля подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="a9a90-107">Order confirmation module properties</span></span>

| <span data-ttu-id="a9a90-108">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a9a90-108">Property name</span></span>  | <span data-ttu-id="a9a90-109">Значения</span><span class="sxs-lookup"><span data-stu-id="a9a90-109">Values</span></span> | <span data-ttu-id="a9a90-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a9a90-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="a9a90-111">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9a90-111">Heading</span></span>        | <span data-ttu-id="a9a90-112">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="a9a90-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a9a90-113">Модуль подтверждения заказа может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="a9a90-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="a9a90-114">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a9a90-115">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="a9a90-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a9a90-116">Контактный номер</span><span class="sxs-lookup"><span data-stu-id="a9a90-116">Contact number</span></span> | <span data-ttu-id="a9a90-117">Текст</span><span class="sxs-lookup"><span data-stu-id="a9a90-117">Text</span></span> | <span data-ttu-id="a9a90-118">Для вопросов, касающихся заказов, может быть указан номер контакта.</span><span class="sxs-lookup"><span data-stu-id="a9a90-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="a9a90-119">Отображать сведения о временном интервале получения</span><span class="sxs-lookup"><span data-stu-id="a9a90-119">Show pickup timeslot information</span></span> | <span data-ttu-id="a9a90-120">Истина или ложь</span><span class="sxs-lookup"><span data-stu-id="a9a90-120">True or False</span></span> | <span data-ttu-id="a9a90-121">Это свойство доступно в версии Dynamics 365 Commerce 10.0.15 и выше.</span><span class="sxs-lookup"><span data-stu-id="a9a90-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="a9a90-122">Если значение равно "true", в нем отображаются сведения о временном интервале получения, если они предоставляются для номенклатуры самовывоза</span><span class="sxs-lookup"><span data-stu-id="a9a90-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="a9a90-123">Модули, которые могут использоваться на странице подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="a9a90-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="a9a90-124">При создании страницы подтверждения заказа в дополнение к модулю подтверждения заказа можно добавлять другие соответствующие модули.</span><span class="sxs-lookup"><span data-stu-id="a9a90-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="a9a90-125">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="a9a90-125">Here are some examples:</span></span>

- <span data-ttu-id="a9a90-126">**Модуль рекомендаций** — модуль рекомендаций можно добавить на страницу подтверждения заказа, чтобы предложить другие продукты для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="a9a90-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="a9a90-127">**Модули маркетинга** — любой модуль маркетинга можно добавить на страницу подтверждения заказа для отображения маркетингового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a9a90-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="a9a90-128">Добавление модуля подтверждения заказа на страницу</span><span class="sxs-lookup"><span data-stu-id="a9a90-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="a9a90-129">Чтобы добавить модуль подтверждения заказа на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a9a90-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a9a90-130">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="a9a90-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a9a90-131">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя **Шаблон подтверждения заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-132">В ячейке **Содержание** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a9a90-133">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-134">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a9a90-135">В диалоговом окне **Добавить модуль** выберите модуль **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-136">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть шаблон.</span><span class="sxs-lookup"><span data-stu-id="a9a90-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="a9a90-137">Модуль подтверждения заказа не должен обрабатываться, поскольку ему требуется контекст номера подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="a9a90-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="a9a90-138">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="a9a90-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a9a90-139">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="a9a90-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="a9a90-140">В диалоговом окне **Выбор шаблона** выберите **Шаблон подтверждения заказа**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="a9a90-141">В поле **Имя страницы** введите **Страница подтверждения заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-142">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a9a90-143">В диалоговом окне **Добавить модуль** выберите модуль **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-144">На панели свойств для модуля подтверждения заказа выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="a9a90-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a9a90-145">В поле **Текст заголовка** в диалоговом окне **Заголовок** введите текст заголовка **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a9a90-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="a9a90-146">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="a9a90-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="a9a90-147">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="a9a90-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9a90-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a9a90-148">Additional resources</span></span>

[<span data-ttu-id="a9a90-149">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="a9a90-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a9a90-150">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="a9a90-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a9a90-151">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="a9a90-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a9a90-152">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="a9a90-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a9a90-153">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="a9a90-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a9a90-154">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="a9a90-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a9a90-155">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="a9a90-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a9a90-156">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="a9a90-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]