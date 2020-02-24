---
title: Модуль корзины
description: В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025444"
---
# <a name="cart-module"></a><span data-ttu-id="f77b0-103">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="f77b0-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f77b0-104">В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f77b0-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f77b0-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f77b0-105">Overview</span></span>

<span data-ttu-id="f77b0-106">Модуль карусели используется для отображения элементов, которые были добавлены в корзину перед тем, как клиент переходит к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="f77b0-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="f77b0-107">Например, он включает в себя все номенклатуры, добавленные в корзину и сводку заказа.</span><span class="sxs-lookup"><span data-stu-id="f77b0-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="f77b0-108">Он также позволяет клиенту применять коды рекламных акций или удалять их.</span><span class="sxs-lookup"><span data-stu-id="f77b0-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f77b0-109">Модуль корзины поддерживает оформление заказа после входа в систему и оформление заказа для клиента-гостя.</span><span class="sxs-lookup"><span data-stu-id="f77b0-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="f77b0-110">Он также поддерживает ссылку **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="f77b0-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="f77b0-111">Можно настроить маршрут для этой ссылки в **Параметры сайта \> Расширения \> Маршруты**.</span><span class="sxs-lookup"><span data-stu-id="f77b0-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="f77b0-112">Модуль корзины обрабатывает данные на основе идентификатора корзины.</span><span class="sxs-lookup"><span data-stu-id="f77b0-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="f77b0-113">Идентификатор корзины — это cookie-файл браузера, доступный на всем сайте.</span><span class="sxs-lookup"><span data-stu-id="f77b0-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f77b0-114">Свойства и слоты модуля корзины</span><span class="sxs-lookup"><span data-stu-id="f77b0-114">Cart module properties and slots</span></span>

<span data-ttu-id="f77b0-115">В модуле корзины есть свойство **Заголовок**, для которого можно задать такие значения как **Корзина** и **Товары в корзине**.</span><span class="sxs-lookup"><span data-stu-id="f77b0-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f77b0-116">Модули, которые могут быть использованы в модуле корзины</span><span class="sxs-lookup"><span data-stu-id="f77b0-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f77b0-117">**Блок текста** — этот модуль поддерживает настраиваемые сообщения в модуле корзины.</span><span class="sxs-lookup"><span data-stu-id="f77b0-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f77b0-118">Сообщения выдаются системой управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="f77b0-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f77b0-119">Любое сообщение может быть добавлено, например "По вопросам, связанным с заказом, обращайтесь по телефону 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="f77b0-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f77b0-120">**Выбор магазина** — этот модуль отображает список ближайших магазинов, в которых номенклатура доступна для получения.</span><span class="sxs-lookup"><span data-stu-id="f77b0-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f77b0-121">Он позволяет пользователям вводить местоположение для поиска ближайших магазинов.</span><span class="sxs-lookup"><span data-stu-id="f77b0-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="f77b0-122">Модуль выбора магазина встроен в интерфейс прикладного программирования (API) геокодирования карт Bing для преобразования местоположения, введенного клиентом, в широту и долготу.</span><span class="sxs-lookup"><span data-stu-id="f77b0-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="f77b0-123">Требуется ключ API карт Bing, который должен быть добавлен на страницу общих параметров розничной торговли в Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="f77b0-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="f77b0-124">Этот модуль поддерживает два свойства, **Радиус поиска** и **Ссылка на условия предоставления услуг**.</span><span class="sxs-lookup"><span data-stu-id="f77b0-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="f77b0-125">Свойство **Радиус поиска** определяет радиус поиска для магазинов в милях.</span><span class="sxs-lookup"><span data-stu-id="f77b0-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="f77b0-126">Если значение не указано, используется радиус поиска по умолчанию в 50 миль.</span><span class="sxs-lookup"><span data-stu-id="f77b0-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="f77b0-127">Если используется карта Bing или какая-либо внешняя служба, свойство **Ссылка на условия предоставления услуг** можно использовать для ссылки на условия предоставления услуг.</span><span class="sxs-lookup"><span data-stu-id="f77b0-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="f77b0-128">Ссылка на условия предоставления услуг должна быть указана для службы карт Bing.</span><span class="sxs-lookup"><span data-stu-id="f77b0-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="f77b0-129">Настройки модуля корзины</span><span class="sxs-lookup"><span data-stu-id="f77b0-129">Cart module settings</span></span>

<span data-ttu-id="f77b0-130">Модули корзины имеют следующие настройки, которые могут быть настроены в **Параметры сайта \> Расширения**:</span><span class="sxs-lookup"><span data-stu-id="f77b0-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="f77b0-131">**Максимальное количество** — это свойство используется для указания максимального количества каждой номенклатуры, которое может быть добавлено в корзину.</span><span class="sxs-lookup"><span data-stu-id="f77b0-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f77b0-132">Например, розничная сеть может решить, что в одну проводку можно продать только 10 шт. каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="f77b0-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f77b0-133">**Проверка запасов** — когда задано значение **True**, номенклатура добавляется в корзину только после того, как модуль поля покупки проверит, что товар есть на складе.</span><span class="sxs-lookup"><span data-stu-id="f77b0-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="f77b0-134">Данная проверка запасов выполняется как для сценариев, в которых номенклатура будет отгружена, так и для сценариев, в которых она будет получена в магазине.</span><span class="sxs-lookup"><span data-stu-id="f77b0-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="f77b0-135">Если для данного параметра установлено значение **False**, проверка запасов не выполняется до того, как номенклатура добавляется в корзину и заказ размещается.</span><span class="sxs-lookup"><span data-stu-id="f77b0-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="f77b0-136">**Буфер запасов** — это свойство используется для указания номера буфера для запасов.</span><span class="sxs-lookup"><span data-stu-id="f77b0-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="f77b0-137">Запасы поддерживаются в реальном времени, и когда многие клиенты размещают заказы, может быть трудно обеспечить точную инвентаризацию запасов.</span><span class="sxs-lookup"><span data-stu-id="f77b0-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="f77b0-138">Когда проверка запасов выполняется, если запасы меньше суммы буфера, продукт рассматривается как отсутствующий в запасах.</span><span class="sxs-lookup"><span data-stu-id="f77b0-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="f77b0-139">Таким образом, когда продажи выполняются быстро по нескольким каналам, так что инвентаризация запасов не полностью синхронизирована, существует меньше риска, что номенклатура, отсутствующая на складе, будет продана.</span><span class="sxs-lookup"><span data-stu-id="f77b0-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="f77b0-140">**Назад к покупкам** — это свойство используется для указания маршрута для ссылки **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="f77b0-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="f77b0-141">Этот маршрут можно настроить на уровне сайта.</span><span class="sxs-lookup"><span data-stu-id="f77b0-141">This route can be configured at the site level.</span></span> <span data-ttu-id="f77b0-142">За счет данной конфигурации розничные продавцы перенаправляют клиентов обратно на домашнюю страницу или на любую другую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="f77b0-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="f77b0-143">Взаимодействие Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="f77b0-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="f77b0-144">Модуль корзины извлекает информацию о продукции с помощью интерфейсов API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f77b0-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="f77b0-145">Идентификатор корзины из cookie-файла браузера используется для получения всей информации о продукте из Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f77b0-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f77b0-146">Добавление модуля корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="f77b0-146">Add a cart module to a page</span></span>

<span data-ttu-id="f77b0-147">Чтобы добавить модуль корзины на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f77b0-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f77b0-148">Создайте фрагмент с именем **Фрагмент корзины** и добавьте в него модуль корзины.</span><span class="sxs-lookup"><span data-stu-id="f77b0-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="f77b0-149">Добавьте заголовок к модулю корзины.</span><span class="sxs-lookup"><span data-stu-id="f77b0-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="f77b0-150">Добавьте модуль выбора магазина в модуль корзины.</span><span class="sxs-lookup"><span data-stu-id="f77b0-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="f77b0-151">Сохраните фрагмент, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="f77b0-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="f77b0-152">Создайте шаблон с именем **Шаблон корзины** и добавьте фрагмент корзины, который только что был создан.</span><span class="sxs-lookup"><span data-stu-id="f77b0-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="f77b0-153">Сохраните шаблон, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="f77b0-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="f77b0-154">Создайте страницу, в которой используется новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="f77b0-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="f77b0-155">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="f77b0-155">Save and preview the page.</span></span>
1. <span data-ttu-id="f77b0-156">Завершите редактирование страницы и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="f77b0-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f77b0-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f77b0-157">Additional resources</span></span>

[<span data-ttu-id="f77b0-158">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="f77b0-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f77b0-159">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="f77b0-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f77b0-160">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="f77b0-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f77b0-161">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="f77b0-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f77b0-162">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="f77b0-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f77b0-163">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="f77b0-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f77b0-164">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="f77b0-164">Footer module</span></span>](author-footer-module.md)
