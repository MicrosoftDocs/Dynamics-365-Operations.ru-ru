---
title: Модуль подтверждения заказа
description: В этом разделе описываются модули подтверждения заказа, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "4415401"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="f2796-103">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="f2796-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2796-104">В этом разделе описываются модули подтверждения заказа, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2796-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2796-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f2796-105">Overview</span></span>

<span data-ttu-id="f2796-106">После размещения заказа можно использовать модуль подтверждения заказа для отображения подробных сведений подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="f2796-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="f2796-107">Здесь отображается код подтверждения заказа, контактная информация заказа и другие сведения о заказе, такие как купленные номенклатуры, вариантах самовывоза и методе отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f2796-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="f2796-108">Свойства модуля подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="f2796-108">Order confirmation module properties</span></span>

| <span data-ttu-id="f2796-109">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="f2796-109">Property name</span></span>  | <span data-ttu-id="f2796-110">Значения</span><span class="sxs-lookup"><span data-stu-id="f2796-110">Values</span></span> | <span data-ttu-id="f2796-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f2796-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f2796-112">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2796-112">Heading</span></span>        | <span data-ttu-id="f2796-113">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="f2796-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f2796-114">Модуль подтверждения заказа может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="f2796-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="f2796-115">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="f2796-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="f2796-116">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="f2796-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="f2796-117">Контактный номер</span><span class="sxs-lookup"><span data-stu-id="f2796-117">Contact number</span></span> | <span data-ttu-id="f2796-118">Текст</span><span class="sxs-lookup"><span data-stu-id="f2796-118">Text</span></span> | <span data-ttu-id="f2796-119">Для вопросов, касающихся заказов, может быть указан номер контакта.</span><span class="sxs-lookup"><span data-stu-id="f2796-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="f2796-120">Отображать сведения о временном интервале получения</span><span class="sxs-lookup"><span data-stu-id="f2796-120">Show pickup timeslot information</span></span> | <span data-ttu-id="f2796-121">Истина или ложь</span><span class="sxs-lookup"><span data-stu-id="f2796-121">True or False</span></span> | <span data-ttu-id="f2796-122">Это свойство доступно в версии Dynamics 365 Commerce 10.0.15 и выше.</span><span class="sxs-lookup"><span data-stu-id="f2796-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="f2796-123">Если значение равно "true", в нем отображаются сведения о временном интервале получения, если они предоставляются для номенклатуры самовывоза</span><span class="sxs-lookup"><span data-stu-id="f2796-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="f2796-124">Модули, которые могут использоваться на странице подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="f2796-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="f2796-125">При создании страницы подтверждения заказа в дополнение к модулю подтверждения заказа можно добавлять другие соответствующие модули.</span><span class="sxs-lookup"><span data-stu-id="f2796-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="f2796-126">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="f2796-126">Here are some examples:</span></span>

- <span data-ttu-id="f2796-127">**Модуль рекомендаций** — модуль рекомендаций можно добавить на страницу подтверждения заказа, чтобы предложить другие продукты для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="f2796-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="f2796-128">**Модули маркетинга** — любой модуль маркетинга можно добавить на страницу подтверждения заказа для отображения маркетингового содержимого.</span><span class="sxs-lookup"><span data-stu-id="f2796-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="f2796-129">Добавление модуля подтверждения заказа на страницу</span><span class="sxs-lookup"><span data-stu-id="f2796-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="f2796-130">Чтобы добавить модуль подтверждения заказа на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2796-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f2796-131">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="f2796-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f2796-132">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя **Шаблон подтверждения заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-133">В ячейке **Содержание** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f2796-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2796-134">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-135">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f2796-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2796-136">В диалоговом окне **Добавить модуль** выберите модуль **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-137">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть шаблон.</span><span class="sxs-lookup"><span data-stu-id="f2796-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="f2796-138">Модуль подтверждения заказа не должен обрабатываться, поскольку ему требуется контекст номера подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="f2796-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="f2796-139">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="f2796-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f2796-140">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="f2796-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f2796-141">В диалоговом окне **Выбор шаблона** выберите **Шаблон подтверждения заказа**.</span><span class="sxs-lookup"><span data-stu-id="f2796-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="f2796-142">В поле **Имя страницы** введите **Страница подтверждения заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-143">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f2796-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2796-144">В диалоговом окне **Добавить модуль** выберите модуль **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-145">На панели свойств для модуля подтверждения заказа выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="f2796-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="f2796-146">В поле **Текст заголовка** в диалоговом окне **Заголовок** введите текст заголовка **Подтверждение заказа**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2796-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2796-147">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="f2796-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f2796-148">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="f2796-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2796-149">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2796-149">Additional resources</span></span>

[<span data-ttu-id="f2796-150">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="f2796-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f2796-151">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="f2796-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f2796-152">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="f2796-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f2796-153">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="f2796-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f2796-154">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="f2796-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f2796-155">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="f2796-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f2796-156">Модуль сведений о самовывозе</span><span class="sxs-lookup"><span data-stu-id="f2796-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f2796-157">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="f2796-157">Gift card module</span></span>](add-giftcard.md)
