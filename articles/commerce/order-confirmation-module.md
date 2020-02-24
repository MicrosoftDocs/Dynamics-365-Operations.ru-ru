---
title: Модуль сведений о заказе
description: В этом разделе описываются модули сведений о заказе, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026025"
---
# <a name="order-details-module"></a><span data-ttu-id="e1947-103">Модуль сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="e1947-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e1947-104">В этом разделе описываются модули сведений о заказе, а также описывается, как использовать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1947-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e1947-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="e1947-105">Overview</span></span>

<span data-ttu-id="e1947-106">После размещения заказа можно использовать модуль сведений о заказе для отображения подробных сведений подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="e1947-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="e1947-107">Здесь отображается код подтверждения заказа, контактная информация заказа и другие сведения о заказе, такие как купленные номенклатуры, сведения о платежах и методе отгрузки.</span><span class="sxs-lookup"><span data-stu-id="e1947-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="e1947-108">Свойства модуля подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="e1947-108">Order confirmation module properties</span></span>

| <span data-ttu-id="e1947-109">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e1947-109">Property name</span></span>  | <span data-ttu-id="e1947-110">Значения</span><span class="sxs-lookup"><span data-stu-id="e1947-110">Values</span></span> | <span data-ttu-id="e1947-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e1947-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e1947-112">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e1947-112">Heading</span></span>        | <span data-ttu-id="e1947-113">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="e1947-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e1947-114">Модуль подтверждения заказа может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="e1947-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="e1947-115">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="e1947-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e1947-116">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="e1947-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e1947-117">Контактный номер</span><span class="sxs-lookup"><span data-stu-id="e1947-117">Contact number</span></span> | <span data-ttu-id="e1947-118">Текст</span><span class="sxs-lookup"><span data-stu-id="e1947-118">Text</span></span> | <span data-ttu-id="e1947-119">Для вопросов, касающихся заказов, может быть указан номер контакта.</span><span class="sxs-lookup"><span data-stu-id="e1947-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="e1947-120">Модули, которые могут использоваться на странице сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="e1947-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="e1947-121">При создании страницы сведений о заказе в дополнение к модулю сведений о заказе можно добавлять другие соответствующие модули.</span><span class="sxs-lookup"><span data-stu-id="e1947-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="e1947-122">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="e1947-122">Here are some examples:</span></span>

- <span data-ttu-id="e1947-123">**Модуль рекомендаций** — модуль рекомендаций можно добавить на страницу сведений о заказе, чтобы предложить другие продукты для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="e1947-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="e1947-124">**Модули маркетинга** — любой модуль маркетинга можно добавить на страницу сведений о заказах для отображения маркетингового содержимого.</span><span class="sxs-lookup"><span data-stu-id="e1947-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="e1947-125">Создание модуля страницы сведений о заказе</span><span class="sxs-lookup"><span data-stu-id="e1947-125">Create an order details page module</span></span>

1. <span data-ttu-id="e1947-126">Создайте шаблон страницы с именем **Шаблон сведений о заказе**.</span><span class="sxs-lookup"><span data-stu-id="e1947-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="e1947-127">В слоте **Главный** страницы по умолчанию добавьте модуль сведений о заказе.</span><span class="sxs-lookup"><span data-stu-id="e1947-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="e1947-128">В модуле сведений о заказе добавьте модуль рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="e1947-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="e1947-129">Сохраните и просмотрите шаблон.</span><span class="sxs-lookup"><span data-stu-id="e1947-129">Save and preview the template.</span></span> <span data-ttu-id="e1947-130">Модуль сведений о заказе не должен обрабатываться, поскольку ему требуется контекст номера подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="e1947-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="e1947-131">Завершите редактирование шаблона и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="e1947-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="e1947-132">Используйте только что созданный шаблон сведений о заказе для создания страницы с именем **страница сведений о заказе**.</span><span class="sxs-lookup"><span data-stu-id="e1947-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="e1947-133">Добавьте страницу по умолчанию в структуру страницы.</span><span class="sxs-lookup"><span data-stu-id="e1947-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="e1947-134">В слоте **Заголовок** добавьте фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="e1947-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="e1947-135">В слоте **Нижний колонтитул** добавьте фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="e1947-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="e1947-136">В слоте **Главный** добавьте модуль сведений о заказе.</span><span class="sxs-lookup"><span data-stu-id="e1947-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="e1947-137">В области свойств модуля сведений о заказе добавьте заголовок **Сведения о заказе**.</span><span class="sxs-lookup"><span data-stu-id="e1947-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="e1947-138">Под модулем сведений о заказе добавьте модуль рекомендаций и настройте его так, чтобы он использовал настройки **Новые** и **Лидеры продаж**.</span><span class="sxs-lookup"><span data-stu-id="e1947-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="e1947-139">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="e1947-139">Save and preview the page.</span></span>
1. <span data-ttu-id="e1947-140">Завершите редактирование страницы и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="e1947-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1947-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1947-141">Additional resources</span></span>

[<span data-ttu-id="e1947-142">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="e1947-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e1947-143">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="e1947-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e1947-144">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="e1947-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e1947-145">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="e1947-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e1947-146">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="e1947-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e1947-147">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="e1947-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e1947-148">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="e1947-148">Footer module</span></span>](author-footer-module.md)
