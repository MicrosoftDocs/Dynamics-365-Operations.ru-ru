---
title: Модуль заголовка
description: В этом разделе описываются модули заголовка, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697283"
---
# <a name="header-module"></a><span data-ttu-id="b5555-103">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="b5555-103">Header module</span></span>

<span data-ttu-id="b5555-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="b5555-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="b5555-105">В этом разделе описываются модули заголовка, а также описывается, как создавать их в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5555-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5555-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="b5555-106">Overview</span></span>

<span data-ttu-id="b5555-107">Модуль заголовка — это специальный контейнер, который используется для размещения всех модулей, которые будут отображаться в заголовке страницы.</span><span class="sxs-lookup"><span data-stu-id="b5555-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="b5555-108">Например, он может содержать эмблему сайта, ссылки на иерархию навигации, ссылки на другие страницы сайта и панель поиска.</span><span class="sxs-lookup"><span data-stu-id="b5555-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="b5555-109">Модуль заголовка автоматически оптимизируется для устройства, на котором просматривается сайт (то есть, для настольного устройства или мобильного устройства).</span><span class="sxs-lookup"><span data-stu-id="b5555-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="b5555-110">Например, на мобильном устройстве панель навигации свернута в кнопку **Меню** (которая иногда называется *меню гамбургер*)</span><span class="sxs-lookup"><span data-stu-id="b5555-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="b5555-111">Свойства заголовка</span><span class="sxs-lookup"><span data-stu-id="b5555-111">Properties of a header</span></span>

<span data-ttu-id="b5555-112">Как и в случае универсальных контейнеров, модуль заголовка поддерживает свойства **заголовок** и **ширина**.</span><span class="sxs-lookup"><span data-stu-id="b5555-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="b5555-113">В модуле заголовка имеется несколько слотов.</span><span class="sxs-lookup"><span data-stu-id="b5555-113">A header module has multiple slots.</span></span> <span data-ttu-id="b5555-114">Например, существуют гнезда для информационного сообщения, меню навигации, эмблемы, панели поиска, значка корзины, значка списка желаний и информации об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b5555-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="b5555-115">Каждый слот поддерживает конкретный набор модулей.</span><span class="sxs-lookup"><span data-stu-id="b5555-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="b5555-116">Модули, доступные в модуле заголовка</span><span class="sxs-lookup"><span data-stu-id="b5555-116">Modules that are available in a header module</span></span>

<span data-ttu-id="b5555-117">Следующие модули, которые могут быть использованы в модуле заголовка:</span><span class="sxs-lookup"><span data-stu-id="b5555-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="b5555-118">**Меню навигации** — меню навигации представляет собой иерархию навигации по каналам и другие статические навигационные ссылки.</span><span class="sxs-lookup"><span data-stu-id="b5555-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="b5555-119">Иерархия навигации по каналу может быть настроена в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="b5555-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="b5555-120">Сконфигурированные элементы затем отображаются в виде навигации заголовка.</span><span class="sxs-lookup"><span data-stu-id="b5555-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="b5555-121">Кроме того, можно настроить статические ссылки навигации, а также указать относительные ссылки на другие страницы сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="b5555-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="b5555-122">Сам заголовок может быть выровнен по левому краю, по правому или по центру.</span><span class="sxs-lookup"><span data-stu-id="b5555-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="b5555-123">**Значок корзины** — значок корзины представляет собой специальный значок, представляющий корзину.</span><span class="sxs-lookup"><span data-stu-id="b5555-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="b5555-124">Он отображается в заголовке и указывает количество номенклатур в корзине.</span><span class="sxs-lookup"><span data-stu-id="b5555-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="b5555-125">Ссылка на страницу корзины должна сопровождаться значком корзины, чтобы клиенты могли быть перенаправлены на страницу корзины при взаимодействии со значком.</span><span class="sxs-lookup"><span data-stu-id="b5555-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="b5555-126">**Значок списка желаний** — значок списка желаемых товаров отображается в заголовке и указывает число номенклатур, добавленных в список желаний клиента.</span><span class="sxs-lookup"><span data-stu-id="b5555-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="b5555-127">Ссылка на страницу списка желаний должна сопровождаться этим значком, чтобы клиенты могли быть перенаправлены на страницу списка желаний при взаимодействии со значком.</span><span class="sxs-lookup"><span data-stu-id="b5555-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="b5555-128">**Модуль входа** — в заголовке отображается модуль входа в систему.</span><span class="sxs-lookup"><span data-stu-id="b5555-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="b5555-129">Клиенты могут либо войти в учетную запись, либо зарегистрировать учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b5555-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="b5555-130">Если клиент уже выполнил вход, модуль можно настроить так, чтобы он отображал ссылки на страницу учетной записи, страницу журнала заказов или другую страницу.</span><span class="sxs-lookup"><span data-stu-id="b5555-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="b5555-131">**Модуль эмблемы** — в этом модуле отображается эмблема, представляющая розничного продавца и торговую марку.</span><span class="sxs-lookup"><span data-stu-id="b5555-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="b5555-132">Это изображение, имеющее ссылку.</span><span class="sxs-lookup"><span data-stu-id="b5555-132">It's an image that has a link.</span></span> <span data-ttu-id="b5555-133">Ссылка обычно настраивается таким образом, чтобы она перенаправлялась на домашнюю страницу. Поэтому клиенты могут быстро вернуться на домашнюю страницу с любой страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="b5555-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="b5555-134">**Оповещение** — оповещение отображается в заголовке и используется для отображения встроенного сообщения, которое применяется ко всем страницам сайта.</span><span class="sxs-lookup"><span data-stu-id="b5555-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="b5555-135">Например, оповещение может содержать сообщение "Ежегодная распродажа заканчивается через 2 дня".</span><span class="sxs-lookup"><span data-stu-id="b5555-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="b5555-136">**Панель поиска** — панель поиска позволяет пользователям вводить искомые термины, чтобы они могли выполнять поиск продуктов.</span><span class="sxs-lookup"><span data-stu-id="b5555-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="b5555-137">Модуль должен быть настроен с URL-адресом страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="b5555-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="b5555-138">Можно настроить параметр строки запроса (значение по умолчанию — **"q"**).</span><span class="sxs-lookup"><span data-stu-id="b5555-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="b5555-139">Панель поиска содержит ячейку автоматического предложения, в которую следует добавить модуль автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="b5555-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="b5555-140">**Автозаполнение** — автоматически предлагаемые результаты отображаются в модуле автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="b5555-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="b5555-141">Эти результаты могут быть ключевыми словами, продуктами или категориями, в которых искомый термин будет найден.</span><span class="sxs-lookup"><span data-stu-id="b5555-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="b5555-142">Создание модуля заголовка</span><span class="sxs-lookup"><span data-stu-id="b5555-142">Create a header module</span></span>

<span data-ttu-id="b5555-143">Чтобы создать модуль заголовка, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b5555-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="b5555-144">Создайте фрагмент страницы, содержащий модуль заголовка.</span><span class="sxs-lookup"><span data-stu-id="b5555-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="b5555-145">Добавьте модули в гнезда в модуле заголовка.</span><span class="sxs-lookup"><span data-stu-id="b5555-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="b5555-146">Обновите настройки для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="b5555-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="b5555-147">Сохраните фрагмент страницы.</span><span class="sxs-lookup"><span data-stu-id="b5555-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="b5555-148">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="b5555-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="b5555-149">Чтобы гарантировать, что заголовок появляется на каждой странице, выполните следующие действия в каждом шаблоне страниц, созданном для сайта.</span><span class="sxs-lookup"><span data-stu-id="b5555-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b5555-150">На странице по умолчанию добавьте фрагмент страницы, содержащий модуль заголовка, к заголовку в главном слоте.</span><span class="sxs-lookup"><span data-stu-id="b5555-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="b5555-151">Сохраните шаблон.</span><span class="sxs-lookup"><span data-stu-id="b5555-151">Save the template.</span></span> 
1. <span data-ttu-id="b5555-152">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="b5555-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5555-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5555-153">Additional resources</span></span>

[<span data-ttu-id="b5555-154">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="b5555-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5555-155">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="b5555-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b5555-156">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="b5555-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b5555-157">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="b5555-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5555-158">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="b5555-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b5555-159">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="b5555-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b5555-160">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="b5555-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b5555-161">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="b5555-161">Footer module</span></span>](author-footer-module.md)
