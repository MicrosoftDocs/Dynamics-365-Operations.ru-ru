---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411231"
---
# <a name="header-module"></a><span data-ttu-id="bbdab-103">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="bbdab-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bbdab-104">В этом разделе описываются модули заголовка, а также описывается, как создавать заголовки страниц в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bbdab-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bbdab-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="bbdab-105">Overview</span></span>

<span data-ttu-id="bbdab-106">В Dynamics 365 Commerce заголовок страницы состоит из нескольких модулей, таких как заголовок, меню переходов, поиск, рекламный баннер и согласие на файлы cookie.</span><span class="sxs-lookup"><span data-stu-id="bbdab-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="bbdab-107">Модуль заголовка включает логотип сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта, символ корзины, список желаемого, параметры входа и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="bbdab-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="bbdab-108">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (другими словами, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="bbdab-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="bbdab-109">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="bbdab-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="bbdab-110">На следующем рисунке показан пример модуля заголовка на главной странице.</span><span class="sxs-lookup"><span data-stu-id="bbdab-110">The following image shows an example of a header module on a home page.</span></span>

![Пример модуля заголовка](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="bbdab-112">Свойства модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="bbdab-112">Properties of a header module</span></span>

<span data-ttu-id="bbdab-113">Модуль заголовка поддерживает свойства **Изображение логотипа**, **Ссылка на логотип** и **Ссылки на мою учетную запись**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="bbdab-114">Свойства **Изображение логотипа** и **Ссылка на логотип** используются для определения логотипа на странице.</span><span class="sxs-lookup"><span data-stu-id="bbdab-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="bbdab-115">Дополнительные сведения см. в разделе [Добавление логотипа](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="bbdab-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="bbdab-116">Свойство **Ссылки на мою учетную запись** можно использовать для определения страниц учетной записи, для которых владелец сайта хочет показывать быстрые ссылки в заголовке.</span><span class="sxs-lookup"><span data-stu-id="bbdab-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="bbdab-117">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="bbdab-117">Modules that are available in a header module</span></span>

<span data-ttu-id="bbdab-118">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="bbdab-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="bbdab-119">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="bbdab-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="bbdab-120">Иерархия навигации по каналу может быть настроена в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bbdab-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bbdab-121">В меню навигации есть свойство **Источник навигации**, которое используется для указания пунктов меню навигации Retail Server и статических пунктов меню в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="bbdab-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="bbdab-122">Если в качестве источника указан статический пункт меню, могут быть предоставлены относительные ссылки на другие страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="bbdab-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="bbdab-123">Сконфигурированные элементы затем отображаются в виде навигации заголовка.</span><span class="sxs-lookup"><span data-stu-id="bbdab-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="bbdab-124">**Поиск** — модуль поиска позволяет пользователям вводить искомые термины для поиска продуктов.</span><span class="sxs-lookup"><span data-stu-id="bbdab-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="bbdab-125">URL-адрес страницы поиска по умолчанию и параметры запроса поиска должны быть указаны в **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="bbdab-126">В модуле поиска есть свойства, позволяющие запретить кнопку поиска или метку при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bbdab-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="bbdab-127">В модуле поиска также поддерживаются параметры автоматического предложения, такие как продукт, ключевое слово и результаты поиска категорий.</span><span class="sxs-lookup"><span data-stu-id="bbdab-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="bbdab-128">**Значок корзины** — модуль "значок корзины" представляет значок корзины, который отображает количество номенклатур в корзине в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="bbdab-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="bbdab-129">Дополнительные сведения см. в разделе [Модуль значка корзины](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="bbdab-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="bbdab-130">Создание модуля заголовка для страницы</span><span class="sxs-lookup"><span data-stu-id="bbdab-130">Create a header module for a page</span></span>

<span data-ttu-id="bbdab-131">Чтобы создать модуль заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bbdab-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="bbdab-132">Перейдите к разделу **Фрагменты страниц**, выберите **Создать**, чтобы создать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="bbdab-132">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="bbdab-133">В диалоговом окне **Создание фрагмента страницы** выберите модуль **Контейнер**, введите имя для фрагмента страницы, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-133">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-134">Выберите ячейку **Контейнер по умолчанию**, а затем в области свойств справа задайте значение свойства **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="bbdab-135">В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-136">В диалоговом окне **Добавление модуля** выберите модули **Рекламный баннер** и **Согласие на файлы cookie**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-137">В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-138">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-139">Выберите ячейку **Контейнер**, а затем в области свойств справа задайте значение свойства **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="bbdab-140">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-141">В диалоговом окне **Добавить модуль** выберите модуль **Заголовок**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-142">В ячейке **Меню навигации** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-143">В диалоговом окне **Добавить модуль** выберите модуль **Меню навигации**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-144">В области свойств модуля меню навигации настройте свойства.</span><span class="sxs-lookup"><span data-stu-id="bbdab-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="bbdab-145">В ячейке **Поиск** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-146">В диалоговом окне **Добавить модуль** выберите модуль **Поиск**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-147">В области свойств модуля поиска настройте свойства.</span><span class="sxs-lookup"><span data-stu-id="bbdab-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="bbdab-148">В ячейке **Значок корзины** модуля поля заголовка нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbdab-149">В диалоговом окне **Добавить модуль** выберите модуль **Значок корзины**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbdab-150">В области свойств модуля значка корзины настройте свойства.</span><span class="sxs-lookup"><span data-stu-id="bbdab-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="bbdab-151">Если необходимо, чтобы значок корзины отображал сводку корзины (также называемую мини-корзиной), когда пользователь наводит на него указатель мыши, установите флажок **Показывать мини-корзину**.</span><span class="sxs-lookup"><span data-stu-id="bbdab-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="bbdab-152">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="bbdab-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bbdab-153">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="bbdab-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="bbdab-154">В слоте **Заголовок** модуля **Страница по умолчанию** добавьте созданный фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="bbdab-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="bbdab-155">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="bbdab-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbdab-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bbdab-156">Additional resources</span></span>

[<span data-ttu-id="bbdab-157">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="bbdab-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bbdab-158">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="bbdab-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bbdab-159">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="bbdab-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bbdab-160">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="bbdab-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bbdab-161">Модуль значка корзины</span><span class="sxs-lookup"><span data-stu-id="bbdab-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bbdab-162">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="bbdab-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bbdab-163">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="bbdab-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bbdab-164">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="bbdab-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bbdab-165">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="bbdab-165">Footer module</span></span>](author-footer-module.md)
