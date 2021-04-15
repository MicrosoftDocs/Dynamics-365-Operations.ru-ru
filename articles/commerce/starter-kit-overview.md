---
title: Обзор библиотеки модулей
description: Этот раздел содержит обзор библиотеки модулей Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795341"
---
# <a name="module-library-overview"></a><span data-ttu-id="6e8bd-103">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="6e8bd-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e8bd-104">Этот раздел содержит обзор библиотеки модулей Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="6e8bd-105">Библиотека модулей Dynamics 365 Commerce представляет собой набор модулей, которые могут использоваться для создания веб-сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="6e8bd-106">Модули имеют как аспекты интерфейса пользователя, так и аспекты функционального поведения.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="6e8bd-107">Темы могут быть применены к модулям в библиотеке модулей для изменения их внешнего вида и поведения.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="6e8bd-108">В темах используются каскадные таблицы стилей (CSS).</span><span class="sxs-lookup"><span data-stu-id="6e8bd-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="6e8bd-109">Тема вымышленного сайта электронной коммерции под названием "Fabrikam" предоставляется в качестве части библиотеки модулей и может использоваться в качестве ссылки.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="6e8bd-110">Модули библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="6e8bd-110">Module library modules</span></span>

<span data-ttu-id="6e8bd-111">В библиотеке модулей представлены следующие типы модулей:</span><span class="sxs-lookup"><span data-stu-id="6e8bd-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="6e8bd-112">**Контейнерный модуль** — это простой модуль, который служит для размещения других модулей.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="6e8bd-113">Он управляет макетом модулей, которые находятся внутри него.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="6e8bd-114">**Маркетинговые модули** — модули маркетинга включают в модуля блока содержимого, блока текста, видеопроигрывателя и карусели.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="6e8bd-115">Все эти модули могут использоваться для демонстрации содержимого.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="6e8bd-116">Их можно разместить на любой странице, и они управляются данными из системы управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="6e8bd-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="6e8bd-117">**Модули заголовка и нижнего колонтитула** — модули заголовка и нижнего колонтитула отображаются в заголовке и нижнем колонтитуле всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="6e8bd-118">Эти модули могут быть настроены в качестве обязательных с помощью свойств.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="6e8bd-119">**Модули поиска** — продукты можно обнаружить, используя модуль поиска в заголовке.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="6e8bd-120">Результаты поиска отображаются на странице результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-120">Search results appear on the search results page.</span></span> <span data-ttu-id="6e8bd-121">Продукты также могут обнаруживаться на страницах категорий, являющихся выделенными страницами для каждой категории, поддерживаемой в иерархии навигации канала.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="6e8bd-122">Кроме того, модули уточнения могут использоваться для получения дальнейшей фильтрации результатов на страницах результатов поиска и категорий.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="6e8bd-123">**Модули страниц сведений о продукте** — страницы сведений о продукте используют несколько модулей для отображения информации о продукте.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="6e8bd-124">Модуль поля покупки позволяет клиентам просматривать продукты и добавлять их в корзину.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="6e8bd-125">В других модулях, таких как модуль технических спецификаций, отображаются подробные сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="6e8bd-126">Модуль оценок и отзывов может использоваться для просмотра и предоставления отзывов.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="6e8bd-127">**Модуль покупки в Интернете с получением в магазине** — этот модуль интегрирован с картами Bing.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="6e8bd-128">Он может использоваться для поиска ближайших магазинов, в которых клиенты могут забрать товары, которые они приобрели.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="6e8bd-129">**Модули покупки** — модули покупки включают в себя модуль корзины, который может использоваться для добавления номенклатур в корзину.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="6e8bd-130">Модуль оформления заказа фиксирует адрес отгрузки, параметры доставки и сведения о подарочном сертификате, программе лояльности и кредитной карте, чтобы заказ мог быть обработан.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="6e8bd-131">После размещения заказа можно использовать модуль подтверждения заказа для отображения подробных сведений подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="6e8bd-132">**Модули управления учетными записями** — модуль входа в систему позволяет клиентам войти в существующую учетную запись, а модуль регистрации позволяет им создать новую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="6e8bd-133">После создания учетной записи модуль истории заказов можно использовать для просмотра последних заказов, а для просмотра сведений о заказе можно использовать модуль сведений о заказе.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="6e8bd-134">**Модуль рекомендаций** — рекомендации отображаются с использованием модуля размещения продукта.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="6e8bd-135">Этот модуль поддерживает алгоритмические и редакционные списки, которые можно показать на любой странице.</span><span class="sxs-lookup"><span data-stu-id="6e8bd-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e8bd-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6e8bd-136">Additional resources</span></span>

[<span data-ttu-id="6e8bd-137">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="6e8bd-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6e8bd-138">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="6e8bd-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6e8bd-139">Модуль корзины</span><span class="sxs-lookup"><span data-stu-id="6e8bd-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6e8bd-140">Модуль оформления заказа</span><span class="sxs-lookup"><span data-stu-id="6e8bd-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6e8bd-141">Модуль подтверждения заказа</span><span class="sxs-lookup"><span data-stu-id="6e8bd-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6e8bd-142">Модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="6e8bd-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6e8bd-143">Модуль нижнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="6e8bd-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]