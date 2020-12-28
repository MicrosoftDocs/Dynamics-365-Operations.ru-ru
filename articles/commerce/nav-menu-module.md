---
title: Модуль меню навигации
description: В этом разделе описываются модули меню навигации, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "4415374"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="1ea53-103">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="1ea53-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ea53-104">В этом разделе описываются модули меню навигации, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1ea53-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1ea53-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="1ea53-105">Overview</span></span>

<span data-ttu-id="1ea53-106">Основной целью модулей меню навигации является предоставление пользователям сайта возможности просмотра продуктов и страниц сайта в соответствии с иерархией навигации канала, определенной в Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1ea53-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="1ea53-107">Элементы, настроенные в модуле меню навигации, отображаются как навигация заголовка сайта.</span><span class="sxs-lookup"><span data-stu-id="1ea53-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="1ea53-108">Модули меню навигации также поддерживают статические пункты меню, связанные с другими страницами сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="1ea53-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="1ea53-109">Модуль меню навигации может быть добавлен в модуль заголовка страницы.</span><span class="sxs-lookup"><span data-stu-id="1ea53-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="1ea53-110">В теме Fabrikam меню навигации отображаются два уровня по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ea53-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="1ea53-111">В начальной теме меню навигации отображаются три уровня по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1ea53-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="1ea53-112">Чтобы изменить число уровней, в теме требуется расширение представления.</span><span class="sxs-lookup"><span data-stu-id="1ea53-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="1ea53-113">На следующем рисунке показан пример меню навигации для сайта Fabrikam с двумя уровнями иерархии категорий и некоторыми статическими пунктами меню.</span><span class="sxs-lookup"><span data-stu-id="1ea53-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="1ea53-114">![Пример модуля меню навигации](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="1ea53-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="1ea53-115">Свойства модуля меню навигации</span><span class="sxs-lookup"><span data-stu-id="1ea53-115">Navigation menu module properties</span></span>

| <span data-ttu-id="1ea53-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="1ea53-116">Property name</span></span>             | <span data-ttu-id="1ea53-117">значение</span><span class="sxs-lookup"><span data-stu-id="1ea53-117">Value</span></span>                 | <span data-ttu-id="1ea53-118">описание</span><span class="sxs-lookup"><span data-stu-id="1ea53-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="1ea53-119">Источник</span><span class="sxs-lookup"><span data-stu-id="1ea53-119">Source</span></span>                  | <span data-ttu-id="1ea53-120">**Retail**, **Ручная разработка**, **Retail и ручная разработка**</span><span class="sxs-lookup"><span data-stu-id="1ea53-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="1ea53-121">Значение **Retail** позволяет использовать иерархию навигации канала из Commerce Headquarters для отображения в меню навигации.</span><span class="sxs-lookup"><span data-stu-id="1ea53-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="1ea53-122">Значение **Ручная разработка** позволяет выполнять создание статических пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="1ea53-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="1ea53-123">Значение **Retail и ручная разработка** разрешает комбинацию обоих типов.</span><span class="sxs-lookup"><span data-stu-id="1ea53-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="1ea53-124">Отображение изображений категорий</span><span class="sxs-lookup"><span data-stu-id="1ea53-124">Show category images</span></span> | <span data-ttu-id="1ea53-125">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="1ea53-125">**True** or **False**</span></span>    | <span data-ttu-id="1ea53-126">Если этот параметр включен, это свойство отображает изображения категорий в меню навигации, как определено в Commerce Headquarters для каждой категории.</span><span class="sxs-lookup"><span data-stu-id="1ea53-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="1ea53-127">Добавлено в Commerce выпуска 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="1ea53-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="1ea53-128">Включение многоуровневого меню навигации</span><span class="sxs-lookup"><span data-stu-id="1ea53-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="1ea53-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="1ea53-129">**True** or **False**</span></span> | <span data-ttu-id="1ea53-130">Когда это свойство включено, в меню переходов может отображаться несколько уровней иерархии навигации.</span><span class="sxs-lookup"><span data-stu-id="1ea53-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="1ea53-131">Эта функция доступна только в выпуске Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="1ea53-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="1ea53-132">Число уровней</span><span class="sxs-lookup"><span data-stu-id="1ea53-132">Number of levels</span></span> | <span data-ttu-id="1ea53-133">целое число</span><span class="sxs-lookup"><span data-stu-id="1ea53-133">integer</span></span> | <span data-ttu-id="1ea53-134">Это свойство определяет число уровней, которые должны отображаться, если для свойства **Включение многоуровневого меню навигации** установлено значение **True**.</span><span class="sxs-lookup"><span data-stu-id="1ea53-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="1ea53-135">Статический пункт меню</span><span class="sxs-lookup"><span data-stu-id="1ea53-135">Static menu item</span></span>| <span data-ttu-id="1ea53-136">Массив значений</span><span class="sxs-lookup"><span data-stu-id="1ea53-136">Array of values</span></span>| <span data-ttu-id="1ea53-137">Статические пункты меню, связывающие имя пункта меню со ссылкой на статическую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="1ea53-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="1ea53-138">Можно создавать пункты меню под другими пунктами меню.</span><span class="sxs-lookup"><span data-stu-id="1ea53-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="1ea53-139">По умолчанию статические меню появляются на корневом уровне и будут добавлены в иерархию навигации канала, если она существует.</span><span class="sxs-lookup"><span data-stu-id="1ea53-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="1ea53-140">Показать корневое меню</span><span class="sxs-lookup"><span data-stu-id="1ea53-140">Show root menu</span></span> | <span data-ttu-id="1ea53-141">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="1ea53-141">**True** or **False**</span></span> | <span data-ttu-id="1ea53-142">Если это свойство включено, меню переходов может быть определено под пользовательским корневым каталогом (например, **Купить сейчас**).</span><span class="sxs-lookup"><span data-stu-id="1ea53-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="1ea53-143">Эта функция доступна только в выпуске Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="1ea53-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="1ea53-144">Корневое меню</span><span class="sxs-lookup"><span data-stu-id="1ea53-144">Root menu</span></span> | <span data-ttu-id="1ea53-145">строка</span><span class="sxs-lookup"><span data-stu-id="1ea53-145">string</span></span> | <span data-ttu-id="1ea53-146">Это свойство может использоваться для определения текста для пользовательского корневого элемента, если свойство **Показать корневое меню** имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="1ea53-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="1ea53-147">На следующем рисунке показан пример изображения категории, которое отображается в меню навигации для сайта Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="1ea53-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="1ea53-148">![Пример модуля меню навигации с изображениями категорий](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="1ea53-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="1ea53-149">Добавление модуля меню навигации в модуль заголовка</span><span class="sxs-lookup"><span data-stu-id="1ea53-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="1ea53-150">Сведения о добавлении модуля меню навигации в модуль заголовка см. в разделе [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="1ea53-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ea53-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1ea53-151">Additional resources</span></span>

[<span data-ttu-id="1ea53-152">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="1ea53-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1ea53-153">Модуль иерархической навигации</span><span class="sxs-lookup"><span data-stu-id="1ea53-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="1ea53-154">Модуль выбора сайта</span><span class="sxs-lookup"><span data-stu-id="1ea53-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="1ea53-155">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="1ea53-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1ea53-156">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="1ea53-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="1ea53-157">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="1ea53-157">Header module</span></span>](author-header-module.md)
