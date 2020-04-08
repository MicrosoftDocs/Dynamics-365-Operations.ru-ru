---
title: Модуль корзины
description: В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154025"
---
# <a name="cart-module"></a><span data-ttu-id="f64ec-103">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="f64ec-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f64ec-104">В этом разделе описываются модули корзины, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f64ec-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f64ec-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f64ec-105">Overview</span></span>

<span data-ttu-id="f64ec-106">Модуль корзины отображает элементы, которые были добавлены в корзину перед тем, как клиент переходит к оформлению заказа.</span><span class="sxs-lookup"><span data-stu-id="f64ec-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="f64ec-107">Модуль также показывает сводку заказа и позволяет клиенту применять коды рекламных акций или удалять их.</span><span class="sxs-lookup"><span data-stu-id="f64ec-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f64ec-108">Модуль корзины поддерживает оформление заказа после входа в систему и оформление заказа для клиента-гостя.</span><span class="sxs-lookup"><span data-stu-id="f64ec-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="f64ec-109">Он также поддерживает ссылку **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="f64ec-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="f64ec-110">Можно настроить маршрут для этой ссылки в **Параметры сайта \> Расширения \> Маршруты**.</span><span class="sxs-lookup"><span data-stu-id="f64ec-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="f64ec-111">Модуль корзины отображает данные на основе идентификатора корзины, который представляет собой файл cookie браузера, доступный на всем сайте.</span><span class="sxs-lookup"><span data-stu-id="f64ec-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f64ec-112">Свойства и слоты модуля корзины</span><span class="sxs-lookup"><span data-stu-id="f64ec-112">Cart module properties and slots</span></span>

<span data-ttu-id="f64ec-113">В модуле корзины есть свойство **Заголовок**, для которого можно задать такие значения как **Корзина** и **Товары в корзине**.</span><span class="sxs-lookup"><span data-stu-id="f64ec-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f64ec-114">Модули, которые могут быть использованы в модуле корзины</span><span class="sxs-lookup"><span data-stu-id="f64ec-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f64ec-115">**Блок текста** — этот модуль поддерживает настраиваемые сообщения в модуле корзины.</span><span class="sxs-lookup"><span data-stu-id="f64ec-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f64ec-116">Сообщения выдаются системой управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="f64ec-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f64ec-117">Любое сообщение может быть добавлено, например "По вопросам, связанным с заказом, обращайтесь по телефону 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="f64ec-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f64ec-118">**Выбор магазина** — этот модуль отображает список ближайших магазинов, в которых номенклатура доступна для получения.</span><span class="sxs-lookup"><span data-stu-id="f64ec-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f64ec-119">Он позволяет пользователям вводить местоположение для поиска ближайших магазинов.</span><span class="sxs-lookup"><span data-stu-id="f64ec-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="f64ec-120">Дополнительные сведения об этом модуле см. в разделе [Модуль выбора магазина](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="f64ec-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="f64ec-121">Настройки модуля корзины</span><span class="sxs-lookup"><span data-stu-id="f64ec-121">Cart module settings</span></span>

<span data-ttu-id="f64ec-122">Модули корзины имеют следующие настройки, которые могут быть настроены в **Параметры сайта \> Расширения**:</span><span class="sxs-lookup"><span data-stu-id="f64ec-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="f64ec-123">**Максимальное количество** — это свойство используется для указания максимального количества каждой номенклатуры, которое может быть добавлено в корзину.</span><span class="sxs-lookup"><span data-stu-id="f64ec-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f64ec-124">Например, розничная сеть может решить, что в одну проводку можно продать только 10 шт. каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="f64ec-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f64ec-125">**Проверка запасов** — когда задано значение **True**, номенклатура добавляется в корзину только после того, как модуль поля покупки проверит, что товар есть на складе.</span><span class="sxs-lookup"><span data-stu-id="f64ec-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="f64ec-126">Данная проверка запасов выполняется для сценариев, в которых номенклатура будет отгружена, и для сценариев, в которых она будет получена в магазине.</span><span class="sxs-lookup"><span data-stu-id="f64ec-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="f64ec-127">Если для данного параметра установлено значение **False**, проверка запасов не выполняется до того, как номенклатура добавляется в корзину и заказ размещается.</span><span class="sxs-lookup"><span data-stu-id="f64ec-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="f64ec-128">**Буфер запасов** — это свойство используется для указания номера буфера для запасов.</span><span class="sxs-lookup"><span data-stu-id="f64ec-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="f64ec-129">Запасы поддерживаются в реальном времени, и когда многие клиенты размещают заказы, может быть трудно обеспечить точную инвентаризацию запасов.</span><span class="sxs-lookup"><span data-stu-id="f64ec-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="f64ec-130">Когда проверка запасов выполняется, если запасы меньше суммы буфера, продукт рассматривается как отсутствующий в запасах.</span><span class="sxs-lookup"><span data-stu-id="f64ec-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="f64ec-131">Таким образом, когда продажи выполняются быстро по нескольким каналам, так что инвентаризация запасов не полностью синхронизирована, существует меньше риска, что номенклатура, отсутствующая на складе, будет продана.</span><span class="sxs-lookup"><span data-stu-id="f64ec-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="f64ec-132">**Назад к покупкам** — это свойство используется для указания маршрута для ссылки **Назад к покупкам**.</span><span class="sxs-lookup"><span data-stu-id="f64ec-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="f64ec-133">Маршрут может быть настроен на уровне сайта, что позволяет розничным продавцам вернуть клиента на домашнюю страницу или на любую другую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="f64ec-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="f64ec-134">Взаимодействие Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="f64ec-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="f64ec-135">Модуль корзины извлекает информацию о продукции с помощью интерфейсов API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f64ec-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="f64ec-136">Идентификатор корзины из cookie-файла браузера используется для получения всей информации о продукте из Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f64ec-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f64ec-137">Добавление модуля корзины на страницу</span><span class="sxs-lookup"><span data-stu-id="f64ec-137">Add a cart module to a page</span></span>

<span data-ttu-id="f64ec-138">Чтобы добавить модуль корзины на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f64ec-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f64ec-139">Создайте фрагмент с именем **Фрагмент корзины** и добавьте модуль корзины в новый фрагмент.</span><span class="sxs-lookup"><span data-stu-id="f64ec-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="f64ec-140">Добавьте заголовок к модулю корзины.</span><span class="sxs-lookup"><span data-stu-id="f64ec-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="f64ec-141">Добавьте модуль выбора магазина в модуль корзины.</span><span class="sxs-lookup"><span data-stu-id="f64ec-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="f64ec-142">Сохраните фрагмент, завершите редактирование, затем опубликуйте фрагмент.</span><span class="sxs-lookup"><span data-stu-id="f64ec-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="f64ec-143">Создайте шаблон с именем **Шаблон корзины** и добавьте фрагмент корзины, который только что был создан.</span><span class="sxs-lookup"><span data-stu-id="f64ec-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="f64ec-144">Сохраните шаблон, завершите редактирование, затем опубликуйте шаблон.</span><span class="sxs-lookup"><span data-stu-id="f64ec-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="f64ec-145">Создайте страницу, в которой используется новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="f64ec-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="f64ec-146">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="f64ec-146">Save and preview the page.</span></span>
1. <span data-ttu-id="f64ec-147">Завершите редактирование страницы, затем опубликуйте страницу.</span><span class="sxs-lookup"><span data-stu-id="f64ec-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f64ec-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f64ec-148">Additional resources</span></span>

[<span data-ttu-id="f64ec-149">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="f64ec-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f64ec-150">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="f64ec-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f64ec-151">Модуль выбора магазина</span><span class="sxs-lookup"><span data-stu-id="f64ec-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="f64ec-152">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="f64ec-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f64ec-153">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="f64ec-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f64ec-154">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="f64ec-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f64ec-155">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="f64ec-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f64ec-156">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="f64ec-156">Footer module</span></span>](author-footer-module.md)
