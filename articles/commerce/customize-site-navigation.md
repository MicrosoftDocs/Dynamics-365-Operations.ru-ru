---
title: Настройка навигации по сайту
description: В этом разделе описывается создание настраиваемой иерархии переходов в Интернете для организации продуктов для просмотра на веб-сайте Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e1efb4a7484bd4626886c0f9aa40c3e4dfe304a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697482"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="f72a2-103">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="f72a2-103">Customize site navigation</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f72a2-104">В этом разделе описывается создание настраиваемой иерархии переходов в Интернете для организации продуктов для просмотра на веб-сайте Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f72a2-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="f72a2-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f72a2-105">Overview</span></span>

<span data-ttu-id="f72a2-106">Интернет-магазины обычно позволяют пользователям находить и просматривать продукты путем перехода по категориям продуктов.</span><span class="sxs-lookup"><span data-stu-id="f72a2-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="f72a2-107">Эта возможность обычно предоставляется на вкладках в верхней части страницы или в левой области переходов.</span><span class="sxs-lookup"><span data-stu-id="f72a2-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="f72a2-108">В Dynamics 365 Commerce можно создавать и управлять иерархической структурой навигации по категориям и продуктам, включенным в различные категории.</span><span class="sxs-lookup"><span data-stu-id="f72a2-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-retail-channel-navigation-hierarchy"></a><span data-ttu-id="f72a2-109">Создание навигационной иерархии канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="f72a2-109">Create a retail channel navigation hierarchy</span></span>

<span data-ttu-id="f72a2-110">Чтобы создать навигационную иерархию канала розничной торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f72a2-110">To create a retail channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f72a2-111">Перейдите в раздел **Retail \> Продукты и категории \> Управление категориями и продуктами**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-111">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="f72a2-112">Выберите **Иерархии категорий**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="f72a2-113">Имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="f72a2-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f72a2-114">Самая верхняя создаваемая вами категория является корневым узлом категорий.</span><span class="sxs-lookup"><span data-stu-id="f72a2-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="f72a2-115">Она не будет отображаться на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="f72a2-115">It won't be shown on your site.</span></span> <span data-ttu-id="f72a2-116">Чтобы создать иерархию категорий, в которой на сайте отображается единственный узел верхнего уровня, создайте и назовите категорию как дочерний элемент корневой категории.</span><span class="sxs-lookup"><span data-stu-id="f72a2-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="f72a2-117">Выберите **Создать узел категории** и назовите категорию.</span><span class="sxs-lookup"><span data-stu-id="f72a2-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="f72a2-118">Продолжайте создавать родственные и дочерние категории по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="f72a2-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="f72a2-119">Теперь можно назначить продукты для каждой категории, созданной под категорией верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f72a2-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="f72a2-120">Настройка порядка категорий</span><span class="sxs-lookup"><span data-stu-id="f72a2-120">Customize the order of categories</span></span>

<span data-ttu-id="f72a2-121">По умолчанию определяемые категории будут отображаться в алфавитном порядке на сайте.</span><span class="sxs-lookup"><span data-stu-id="f72a2-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="f72a2-122">Однако можно также настроить порядок отображения категорий.</span><span class="sxs-lookup"><span data-stu-id="f72a2-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="f72a2-123">Назначение типа иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="f72a2-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="f72a2-124">Перейдите в раздел **Retail \> Продукты и категории \> Управление категориями и продуктами**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-124">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="f72a2-125">Выберите **Иерархии категорий**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="f72a2-126">В область действий на вкладке **Иерархия категорий** в группе **Настройка** выберите **Связать тип иерархии**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="f72a2-127">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-127">Select **New**.</span></span>
1. <span data-ttu-id="f72a2-128">В поле **Тип иерархии категорий** выберите **Навигационная иерархия канала розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-128">In the **Category hierarchy type** field, select **Retail channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="f72a2-129">В поле **Иерархия категорий** выберите созданную ранее иерархию навигации канала.</span><span class="sxs-lookup"><span data-stu-id="f72a2-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="f72a2-130">Публикация новых или обновленных иерархий навигации</span><span class="sxs-lookup"><span data-stu-id="f72a2-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="f72a2-131">Чтобы сделать иерархию навигации доступной для интернет-магазина, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f72a2-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="f72a2-132">Перейдите в раздел **Retail \> Настройка канала \> Категории каналов и атрибуты продуктов**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-132">Go to **Retail \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="f72a2-133">В дереве слева выберите свой интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="f72a2-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="f72a2-134">Выберите **Опубликовать обновления канала**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="f72a2-135">Выберите **Розничная торговля \> ИТ розничной торговли \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-135">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="f72a2-136">В списке найдите и выберите **Задание 1040**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="f72a2-137">Выберите **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="f72a2-137">Select **Run now**.</span></span>
1. <span data-ttu-id="f72a2-138">Повторите шаги 5 и 6 для заданий 1070 и 1150.</span><span class="sxs-lookup"><span data-stu-id="f72a2-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="f72a2-139">Отображение категорий на сайте</span><span class="sxs-lookup"><span data-stu-id="f72a2-139">Show categories on your site</span></span>

<span data-ttu-id="f72a2-140">Чтобы отобразить иерархию категорий в интернет-магазине, необходимо добавить модуль меню переходов в соответствующее место в шаблоне или фрагменте.</span><span class="sxs-lookup"><span data-stu-id="f72a2-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="f72a2-141">Затем в модуле меню навигации будет показана иерархия переходов, при условии, что иерархия переходов розничной торговли была опубликована в канале, к которому привязан сайт.</span><span class="sxs-lookup"><span data-stu-id="f72a2-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your retail navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="f72a2-142">Модуль меню переходов, включенный в стартовый комплект магазина, позволяет пользователям перемещаться только по категориям, которые не имеют подкатегорий.</span><span class="sxs-lookup"><span data-stu-id="f72a2-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="f72a2-143">Если клиенты должны иметь возможность переходить к категориям, имеющим подкатегории, необходимо настроить модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="f72a2-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="f72a2-144">Добавление пользовательских параметров навигации</span><span class="sxs-lookup"><span data-stu-id="f72a2-144">Add custom navigation options</span></span>

<span data-ttu-id="f72a2-145">В меню переходов можно добавлять параметры навигации, которые не входят в иерархию категорий продуктов.</span><span class="sxs-lookup"><span data-stu-id="f72a2-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="f72a2-146">Например, в конце списка категорий продуктов можно добавить элемент **Свяжитесь с нами**, который указывает на страницу контактов, созданную для сайта.</span><span class="sxs-lookup"><span data-stu-id="f72a2-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="f72a2-147">Чтобы добавить пользовательские параметры навигации в меню навигации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f72a2-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="f72a2-148">В шаблоне или фрагменте, который необходимо настроить, выберите модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="f72a2-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="f72a2-149">В области свойств на вкладке **Данные** выберите **Добавить элемент**, чтобы создать новый элемент навигации в системе управления содержимым (CMS).</span><span class="sxs-lookup"><span data-stu-id="f72a2-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="f72a2-150">Введите текст ссылки и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f72a2-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="f72a2-151">Повторите шаги 2 и 3, чтобы добавить дополнительные параметры навигации.</span><span class="sxs-lookup"><span data-stu-id="f72a2-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="f72a2-152">После завершения сохраните шаблон или фрагмент и верните его.</span><span class="sxs-lookup"><span data-stu-id="f72a2-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f72a2-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f72a2-153">Additional resources</span></span>

[<span data-ttu-id="f72a2-154">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="f72a2-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f72a2-155">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="f72a2-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f72a2-156">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="f72a2-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f72a2-157">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="f72a2-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f72a2-158">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="f72a2-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="f72a2-159">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="f72a2-159">Create a page URL</span></span>](create-page-url.md)
