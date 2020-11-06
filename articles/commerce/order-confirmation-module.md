---
title: Модуль сведений о заказе
description: В этом разделе описываются модули сведений о заказе, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015188"
---
# <a name="order-details-module"></a><span data-ttu-id="74f89-103">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="74f89-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74f89-104">В этом разделе описываются модули сведений о заказе, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74f89-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74f89-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="74f89-105">Overview</span></span>

<span data-ttu-id="74f89-106">После размещения заказа можно использовать модуль сведений о заказе для отображения подробных сведений подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="74f89-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="74f89-107">Здесь отображается код подтверждения заказа, контактная информация заказа и другие сведения о заказе, такие как купленные номенклатуры, сведения о платежах и методе отгрузки.</span><span class="sxs-lookup"><span data-stu-id="74f89-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="74f89-108">Свойства модуля сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="74f89-108">Order details module properties</span></span>

| <span data-ttu-id="74f89-109">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="74f89-109">Property name</span></span>  | <span data-ttu-id="74f89-110">Значения</span><span class="sxs-lookup"><span data-stu-id="74f89-110">Values</span></span> | <span data-ttu-id="74f89-111">описание</span><span class="sxs-lookup"><span data-stu-id="74f89-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="74f89-112">Заголовок</span><span class="sxs-lookup"><span data-stu-id="74f89-112">Heading</span></span>        | <span data-ttu-id="74f89-113">Текст заголовка и метка заголовка ( **H1** , **H2** , **H3** , **H4** , **H5** или **H6** )</span><span class="sxs-lookup"><span data-stu-id="74f89-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="74f89-114">Модуль сведений о заказе может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="74f89-114">The order details module can have a heading.</span></span> <span data-ttu-id="74f89-115">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="74f89-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="74f89-116">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="74f89-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="74f89-117">Контактный номер</span><span class="sxs-lookup"><span data-stu-id="74f89-117">Contact number</span></span> | <span data-ttu-id="74f89-118">Текст</span><span class="sxs-lookup"><span data-stu-id="74f89-118">Text</span></span> | <span data-ttu-id="74f89-119">Для вопросов, касающихся заказов, может быть указан номер контакта.</span><span class="sxs-lookup"><span data-stu-id="74f89-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="74f89-120">Модули, которые могут использоваться на странице сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="74f89-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="74f89-121">При создании страницы сведений о заказе в дополнение к модулю сведений о заказе можно добавлять другие соответствующие модули.</span><span class="sxs-lookup"><span data-stu-id="74f89-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="74f89-122">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="74f89-122">Here are some examples:</span></span>

- <span data-ttu-id="74f89-123">**Модуль рекомендаций** — модуль рекомендаций можно добавить на страницу сведений о заказе, чтобы предложить другие продукты для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="74f89-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="74f89-124">**Модули маркетинга** — любой модуль маркетинга можно добавить на страницу сведений о заказах для отображения маркетингового содержимого.</span><span class="sxs-lookup"><span data-stu-id="74f89-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="74f89-125">Добавление модуля сведений о заказе на страницу</span><span class="sxs-lookup"><span data-stu-id="74f89-125">Add an order details module to a page</span></span>

<span data-ttu-id="74f89-126">Чтобы добавить модуль сведений о заказе на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="74f89-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="74f89-127">Перейдите к пункту **Шаблоны** , выберите **Создать** , чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="74f89-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="74f89-128">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя **Шаблон сведений о заказе** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-129">В ячейке **Содержание** выберите многоточие ( **...** ), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="74f89-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74f89-130">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-131">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие ( **...** ), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="74f89-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74f89-132">В диалоговом окне **Добавить модуль** выберите модуль **Сведения о заказе** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-133">Выберите **Сохранить** , затем выберите **Предварительный просмотр** , чтобы просмотреть шаблон.</span><span class="sxs-lookup"><span data-stu-id="74f89-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="74f89-134">Модуль сведений о заказе не должен обрабатываться, поскольку ему требуется контекст номера подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="74f89-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="74f89-135">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать** , чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="74f89-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="74f89-136">Перейдите к разделу **Страницы** , выберите **Создать** , чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="74f89-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="74f89-137">В диалоговом окне **Выбор шаблона** выберите **Шаблон сведений о заказе**.</span><span class="sxs-lookup"><span data-stu-id="74f89-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="74f89-138">В поле **Имя страницы** введите **Страница сведений о заказе** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-139">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие ( **...** ), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="74f89-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74f89-140">В диалоговом окне **Добавить модуль** выберите модуль **Сведения о заказе** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-141">На панели свойств для модуля сведений о заказе выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="74f89-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="74f89-142">В поле **Текст заголовка** в диалоговом окне **Заголовок** введите текст заголовка **Сведения о заказе** , затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74f89-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="74f89-143">Выберите **Сохранить** , затем выберите **Предварительный просмотр** , чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="74f89-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="74f89-144">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать** , чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="74f89-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74f89-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="74f89-145">Additional resources</span></span>

[<span data-ttu-id="74f89-146">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="74f89-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="74f89-147">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="74f89-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="74f89-148">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="74f89-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="74f89-149">Модуль платежа</span><span class="sxs-lookup"><span data-stu-id="74f89-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="74f89-150">Модуль адреса доставки</span><span class="sxs-lookup"><span data-stu-id="74f89-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="74f89-151">Модуль параметров доставки</span><span class="sxs-lookup"><span data-stu-id="74f89-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="74f89-152">Модуль подарочных сертификатов</span><span class="sxs-lookup"><span data-stu-id="74f89-152">Gift card module</span></span>](add-giftcard.md)
