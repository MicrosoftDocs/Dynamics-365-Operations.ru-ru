---
title: Модуль меню навигации
description: В этом разделе описываются модули меню навигации, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761418"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="31a48-103">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="31a48-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="31a48-104">В этом разделе описываются модули меню навигации, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31a48-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31a48-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="31a48-105">Overview</span></span>

<span data-ttu-id="31a48-106">Основной целью модулей меню навигации является предоставление пользователям сайта возможности просмотра продуктов и страниц сайта в соответствии с иерархией навигации канала, определенной в Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="31a48-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="31a48-107">Элементы, настроенные в модуле меню навигации, отображаются как навигация заголовка сайта.</span><span class="sxs-lookup"><span data-stu-id="31a48-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="31a48-108">Модули меню навигации также поддерживают статические пункты меню, связанные с другими страницами сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="31a48-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="31a48-109">Модуль меню навигации может быть добавлен в модуль заголовка страницы.</span><span class="sxs-lookup"><span data-stu-id="31a48-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="31a48-110">В теме Fabrikam меню навигации отображаются два уровня по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31a48-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="31a48-111">В начальной теме меню навигации отображаются три уровня по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31a48-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="31a48-112">Чтобы изменить число уровней, в теме требуется расширение представления.</span><span class="sxs-lookup"><span data-stu-id="31a48-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="31a48-113">На следующем рисунке показан пример меню навигации для сайта Fabrikam с двумя уровнями иерархии категорий и некоторыми статическими пунктами меню.</span><span class="sxs-lookup"><span data-stu-id="31a48-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="31a48-114">![Пример модуля меню навигации](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="31a48-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="31a48-115">Свойства модуля меню навигации</span><span class="sxs-lookup"><span data-stu-id="31a48-115">Navigation menu module properties</span></span>

| <span data-ttu-id="31a48-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="31a48-116">Property name</span></span>             | <span data-ttu-id="31a48-117">значение</span><span class="sxs-lookup"><span data-stu-id="31a48-117">Value</span></span>                 | <span data-ttu-id="31a48-118">описание</span><span class="sxs-lookup"><span data-stu-id="31a48-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="31a48-119">Источник</span><span class="sxs-lookup"><span data-stu-id="31a48-119">Source</span></span>                  | <span data-ttu-id="31a48-120">**Retail**, **Ручная разработка**, **Retail и ручная разработка**</span><span class="sxs-lookup"><span data-stu-id="31a48-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="31a48-121">Значение **Retail** позволяет использовать иерархию навигации канала из Commerce Headquarters для отображения в меню навигации.</span><span class="sxs-lookup"><span data-stu-id="31a48-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="31a48-122">Значение **Ручная разработка** позволяет выполнять создание статических пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="31a48-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="31a48-123">Значение **Retail и ручная разработка** разрешает комбинацию обоих типов.</span><span class="sxs-lookup"><span data-stu-id="31a48-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="31a48-124">Отображение изображений категорий</span><span class="sxs-lookup"><span data-stu-id="31a48-124">Show category images</span></span> | <span data-ttu-id="31a48-125">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="31a48-125">**True** or **False**</span></span>    | <span data-ttu-id="31a48-126">Если этот параметр включен, это свойство отображает изображения категорий в меню навигации, как определено в Commerce Headquarters для каждой категории.</span><span class="sxs-lookup"><span data-stu-id="31a48-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="31a48-127">Добавлено в Commerce выпуска 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="31a48-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="31a48-128">Статический пункт меню</span><span class="sxs-lookup"><span data-stu-id="31a48-128">Static menu item</span></span>| <span data-ttu-id="31a48-129">Массив значений</span><span class="sxs-lookup"><span data-stu-id="31a48-129">Array of values</span></span>| <span data-ttu-id="31a48-130">Статические пункты меню, связывающие имя пункта меню со ссылкой на статическую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="31a48-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="31a48-131">Можно создавать пункты меню под другими пунктами меню.</span><span class="sxs-lookup"><span data-stu-id="31a48-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="31a48-132">По умолчанию статические меню появляются на корневом уровне и будут добавлены в иерархию навигации канала, если она существует.</span><span class="sxs-lookup"><span data-stu-id="31a48-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="31a48-133">На следующем рисунке показан пример изображения категории, которое отображается в меню навигации для сайта Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="31a48-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="31a48-134">![Пример модуля меню навигации с изображениями категорий](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="31a48-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="31a48-135">Добавление модуля меню навигации в модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="31a48-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="31a48-136">Сведения о добавлении модуля меню навигации в модуль заголовка см. в разделе [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="31a48-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31a48-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="31a48-137">Additional resources</span></span>

[<span data-ttu-id="31a48-138">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="31a48-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="31a48-139">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="31a48-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="31a48-140">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="31a48-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="31a48-141">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="31a48-141">Header module</span></span>](author-header-module.md)
