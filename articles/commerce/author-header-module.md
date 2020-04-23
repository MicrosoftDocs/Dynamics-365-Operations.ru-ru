---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261452"
---
# <a name="header-module"></a><span data-ttu-id="cf051-103">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="cf051-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cf051-104">В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf051-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf051-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="cf051-105">Overview</span></span>

<span data-ttu-id="cf051-106">В Dynamics 365 Commerce заголовок страницы состоит из нескольких модулей, таких как заголовок, меню переходов, поиск, рекламный баннер и согласие на файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="cf051-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="cf051-107">Модуль заголовка включает логотип сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта, символ корзины, список желаемого, параметры входа и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="cf051-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="cf051-108">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (другими словами, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="cf051-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="cf051-109">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="cf051-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="cf051-110">Свойства модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="cf051-110">Properties of a header module</span></span>

<span data-ttu-id="cf051-111">Модуль заголовка поддерживает свойства **Изображение логотипа**, **Ссылка на логотип** и **Ссылки на мою учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="cf051-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="cf051-112">Свойства **Изображение логотипа** и **Ссылка на логотип** используются для определения логотипа на странице.</span><span class="sxs-lookup"><span data-stu-id="cf051-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="cf051-113">Дополнительные сведения см. в разделе [Добавление логотипа](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="cf051-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="cf051-114">Свойство **Ссылки на мою учетную запись** можно использовать для определения страниц учетной записи, для которых владелец сайта хочет показывать быстрые ссылки в заголовке.</span><span class="sxs-lookup"><span data-stu-id="cf051-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="cf051-115">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="cf051-115">Modules that are available in a header module</span></span>

<span data-ttu-id="cf051-116">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="cf051-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="cf051-117">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="cf051-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="cf051-118">Иерархия навигации по каналу может быть настроена в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf051-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cf051-119">В меню навигации есть свойство **Источник навигации**, которое используется для указания пунктов меню навигации Retail Server и статических пунктов меню в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="cf051-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="cf051-120">Если в качестве источника указан статический пункт меню, могут быть предоставлены относительные ссылки на другие страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="cf051-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="cf051-121">Сконфигурированные элементы затем отображаются в виде навигации заголовка.</span><span class="sxs-lookup"><span data-stu-id="cf051-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="cf051-122">**Поиск** — модуль поиска позволяет пользователям вводить искомые термины для поиска продуктов.</span><span class="sxs-lookup"><span data-stu-id="cf051-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="cf051-123">URL-адрес страницы поиска по умолчанию и параметры запроса поиска должны быть указаны в **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="cf051-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="cf051-124">В модуле поиска есть свойства, позволяющие запретить кнопку поиска или метку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cf051-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="cf051-125">В модуле поиска также поддерживаются параметры автоматического предложения, такие как продукт, ключевое слово и результаты поиска категорий.</span><span class="sxs-lookup"><span data-stu-id="cf051-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="cf051-126">**Значок корзины** — модуль "значок корзины" представляет значок корзины, который отображает количество номенклатур в корзине в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="cf051-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="cf051-127">Дополнительные сведения см. в разделе [Модуль значка корзины](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="cf051-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="cf051-128">Создание модуля заголовка для страницы</span><span class="sxs-lookup"><span data-stu-id="cf051-128">Create a header module for a page</span></span>

<span data-ttu-id="cf051-129">Чтобы создать модуль заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cf051-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="cf051-130">Создайте фрагмент с именем **Фрагмент заголовка** и добавьте в него модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="cf051-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="cf051-131">В области свойств модуля контейнера задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="cf051-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="cf051-132">Добавление модулей рекламного баннера и согласия на файлы cookie в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="cf051-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="cf051-133">Добавьте еще один модуль контейнера во фрагмент и задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="cf051-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="cf051-134">Добавьте модуль заголовка во второй модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="cf051-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="cf051-135">В области **Меню навигация** модуля заголовка добавьте модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="cf051-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="cf051-136">В области свойств модуля меню переходов настройте свойства модуля меню навигации.</span><span class="sxs-lookup"><span data-stu-id="cf051-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="cf051-137">В области **Поиск** модуля заголовка добавьте модуль поиска.</span><span class="sxs-lookup"><span data-stu-id="cf051-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="cf051-138">В области свойств модуля поиска настройте свойства модуля поиска.</span><span class="sxs-lookup"><span data-stu-id="cf051-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="cf051-139">В области **Значок корзины** модуля заголовка добавьте модуль значка корзины.</span><span class="sxs-lookup"><span data-stu-id="cf051-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="cf051-140">В области свойств модуля значка корзины настройте свойства модуля значка корзины.</span><span class="sxs-lookup"><span data-stu-id="cf051-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="cf051-141">Если необходимо, чтобы значок корзины отображал мини-корзину при наведении на него указателя, выберите **True** для параметра **Показывать мини-корзину**.</span><span class="sxs-lookup"><span data-stu-id="cf051-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="cf051-142">Сохраните фрагмент страницы, завершите редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="cf051-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="cf051-143">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="cf051-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="cf051-144">В области **Основной** на странице по умолчанию добавьте фрагмент страницы заголовка, содержащий модуль заголовка, к заголовку.</span><span class="sxs-lookup"><span data-stu-id="cf051-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="cf051-145">Сохраните шаблон, завершите редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="cf051-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf051-146">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cf051-146">Additional resources</span></span>

[<span data-ttu-id="cf051-147">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="cf051-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cf051-148">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="cf051-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cf051-149">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="cf051-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cf051-150">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="cf051-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cf051-151">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="cf051-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="cf051-152">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="cf051-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cf051-153">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="cf051-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cf051-154">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="cf051-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="cf051-155">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="cf051-155">Footer module</span></span>](author-footer-module.md)
