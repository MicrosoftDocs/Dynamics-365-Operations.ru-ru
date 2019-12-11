---
title: Модуль подтверждения заказа
description: В этом разделе описываются модули подтверждения заказа, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698334"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="43f5a-103">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="43f5a-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="43f5a-104">В этом разделе описываются модули подтверждения заказа, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="43f5a-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="43f5a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="43f5a-105">Overview</span></span>

<span data-ttu-id="43f5a-106">Модуль подтверждения заказа используется для отображения сообщения подтверждения на странице подтверждения заказа после размещения заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="43f5a-107">В модуле подтверждение заказа отображается номер подтверждения заказа и адрес электронной почты клиента, который был указан во время оформления заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="43f5a-108">Когда заказ размещается во время оформления заказа, номер подтверждения заказа и адрес электронной почты клиента передаются на страницу подтверждения заказа в виде строки запроса в URL-адресе страницы.</span><span class="sxs-lookup"><span data-stu-id="43f5a-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="43f5a-109">Модуль подтверждения заказа получает эту информацию и отображает статус заказа на странице подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="43f5a-110">Модуль подтверждения заказа требует этот контекст страницы для предоставления статуса заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="43f5a-111">Свойства модуля подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="43f5a-111">Order confirmation module properties</span></span>

| <span data-ttu-id="43f5a-112">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="43f5a-112">Property name</span></span> | <span data-ttu-id="43f5a-113">Значения</span><span class="sxs-lookup"><span data-stu-id="43f5a-113">Values</span></span> | <span data-ttu-id="43f5a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="43f5a-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="43f5a-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43f5a-115">Heading</span></span>       | <span data-ttu-id="43f5a-116">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="43f5a-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="43f5a-117">Модуль подтверждения заказа может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="43f5a-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="43f5a-118">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="43f5a-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="43f5a-119">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="43f5a-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="43f5a-120">Модули, которые могут использоваться в модуле страницы подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="43f5a-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="43f5a-121">**Рекомендации** — модуль рекомендаций можно разместить на странице подтверждения заказа, чтобы предложить другие продукты для данного клиента.</span><span class="sxs-lookup"><span data-stu-id="43f5a-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="43f5a-122">**Маркетинг** — модуль маркетинга может добавлять маркетинговое содержимое на страницу подтверждение заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="43f5a-123">Создание модуля страницы подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="43f5a-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="43f5a-124">Создайте шаблон страницы с именем **шаблон подтверждения заказа**.</span><span class="sxs-lookup"><span data-stu-id="43f5a-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="43f5a-125">В слоте **Главный** страницы по умолчанию добавьте модуль подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="43f5a-126">В модуле подтверждения заказа добавьте модуль рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="43f5a-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="43f5a-127">Сохраните и просмотрите шаблон.</span><span class="sxs-lookup"><span data-stu-id="43f5a-127">Save and preview the template.</span></span> <span data-ttu-id="43f5a-128">Модуль подтверждения заказа не должен обрабатываться, поскольку ему требуется контекст номера подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="43f5a-129">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="43f5a-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="43f5a-130">Используйте только что созданный шаблон подтверждения заказа для создания страницы с именем **страница подтверждения заказа**.</span><span class="sxs-lookup"><span data-stu-id="43f5a-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="43f5a-131">Добавьте страницу по умолчанию в структуру страницы.</span><span class="sxs-lookup"><span data-stu-id="43f5a-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="43f5a-132">В слоте **Заголовок** добавьте фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="43f5a-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="43f5a-133">В слоте **Нижний колонтитул** добавьте фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="43f5a-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="43f5a-134">В слоте **Главный** добавьте модуль подтверждения заказа.</span><span class="sxs-lookup"><span data-stu-id="43f5a-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="43f5a-135">В области свойств модуля подтверждение заказа добавьте заголовок **Подтверждение заказа**.</span><span class="sxs-lookup"><span data-stu-id="43f5a-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="43f5a-136">Под модулем подтверждения заказа добавьте модуль рекомендаций и настройте его так, чтобы он использовал настройки **Новые** и **Лидеры продаж**.</span><span class="sxs-lookup"><span data-stu-id="43f5a-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="43f5a-137">Сохраните и просмотрите страницу, верните ее и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="43f5a-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43f5a-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43f5a-138">Additional resources</span></span>

[<span data-ttu-id="43f5a-139">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="43f5a-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="43f5a-140">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="43f5a-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="43f5a-141">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="43f5a-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="43f5a-142">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="43f5a-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="43f5a-143">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="43f5a-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="43f5a-144">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="43f5a-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="43f5a-145">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="43f5a-145">Footer module</span></span>](author-footer-module.md)
