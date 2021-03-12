---
title: Настройка навигации по сайту
description: В этом разделе описывается создание настраиваемой иерархии переходов в Интернете для организации продуктов для просмотра на веб-сайте Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d45f116acc19130e09108a246d276bb4b62a1e6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972915"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="954e5-103">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="954e5-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="954e5-104">В этом разделе описывается создание настраиваемой иерархии переходов в Интернете для организации продуктов для просмотра на веб-сайте Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="954e5-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="954e5-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="954e5-105">Overview</span></span>

<span data-ttu-id="954e5-106">Интернет-магазины обычно позволяют пользователям находить и просматривать продукты путем перехода по категориям продуктов.</span><span class="sxs-lookup"><span data-stu-id="954e5-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="954e5-107">Эта возможность обычно предоставляется на вкладках в верхней части страницы или в левой области переходов.</span><span class="sxs-lookup"><span data-stu-id="954e5-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="954e5-108">В Dynamics 365 Commerce можно создавать и управлять иерархической структурой навигации по категориям и продуктам, включенным в различные категории.</span><span class="sxs-lookup"><span data-stu-id="954e5-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="954e5-109">Создание навигационной иерархии канала</span><span class="sxs-lookup"><span data-stu-id="954e5-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="954e5-110">Чтобы создать навигационную иерархию канала торговли, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="954e5-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="954e5-111">Перейдите в раздел **Retail и Commerce \> Продукты и категории \> Управление категориями и продуктами**.</span><span class="sxs-lookup"><span data-stu-id="954e5-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="954e5-112">Выберите **Иерархии категорий**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="954e5-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="954e5-113">Имя иерархии.</span><span class="sxs-lookup"><span data-stu-id="954e5-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="954e5-114">Самая верхняя создаваемая вами категория является корневым узлом категорий.</span><span class="sxs-lookup"><span data-stu-id="954e5-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="954e5-115">Она не будет отображаться на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="954e5-115">It won't be shown on your site.</span></span> <span data-ttu-id="954e5-116">Чтобы создать иерархию категорий, в которой на сайте отображается единственный узел верхнего уровня, создайте и назовите категорию как дочерний элемент корневой категории.</span><span class="sxs-lookup"><span data-stu-id="954e5-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="954e5-117">Выберите **Создать узел категории** и назовите категорию.</span><span class="sxs-lookup"><span data-stu-id="954e5-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="954e5-118">Продолжайте создавать родственные и дочерние категории по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="954e5-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="954e5-119">Теперь можно назначить продукты для каждой категории, созданной под категорией верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="954e5-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="954e5-120">Настройка порядка категорий</span><span class="sxs-lookup"><span data-stu-id="954e5-120">Customize the order of categories</span></span>

<span data-ttu-id="954e5-121">По умолчанию определяемые категории будут отображаться в алфавитном порядке на сайте.</span><span class="sxs-lookup"><span data-stu-id="954e5-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="954e5-122">Однако можно также настроить порядок отображения категорий.</span><span class="sxs-lookup"><span data-stu-id="954e5-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="954e5-123">Назначение типа иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="954e5-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="954e5-124">Перейдите в раздел **Retail и Commerce \> Продукты и категории \> Управление категориями и продуктами**.</span><span class="sxs-lookup"><span data-stu-id="954e5-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="954e5-125">Выберите **Иерархии категорий**.</span><span class="sxs-lookup"><span data-stu-id="954e5-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="954e5-126">В область действий на вкладке **Иерархия категорий** в группе **Настройка** выберите **Связать тип иерархии**.</span><span class="sxs-lookup"><span data-stu-id="954e5-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="954e5-127">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="954e5-127">Select **New**.</span></span>
1. <span data-ttu-id="954e5-128">В поле **Тип иерархии категорий** выберите **Навигационная иерархия канала**.</span><span class="sxs-lookup"><span data-stu-id="954e5-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="954e5-129">В поле **Иерархия категорий** выберите созданную ранее иерархию навигации канала.</span><span class="sxs-lookup"><span data-stu-id="954e5-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="954e5-130">Публикация новых или обновленных иерархий навигации</span><span class="sxs-lookup"><span data-stu-id="954e5-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="954e5-131">Чтобы сделать иерархию навигации доступной для интернет-магазина, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="954e5-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="954e5-132">Перейдите в раздел **Retail и Commerce \> Настройка канала \> Категории каналов и атрибуты продуктов**.</span><span class="sxs-lookup"><span data-stu-id="954e5-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="954e5-133">В дереве слева выберите свой интернет-магазин.</span><span class="sxs-lookup"><span data-stu-id="954e5-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="954e5-134">Выберите **Опубликовать обновления канала**.</span><span class="sxs-lookup"><span data-stu-id="954e5-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="954e5-135">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="954e5-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="954e5-136">В списке найдите и выберите **Задание 1040**.</span><span class="sxs-lookup"><span data-stu-id="954e5-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="954e5-137">Выберите **Запустить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="954e5-137">Select **Run now**.</span></span>
1. <span data-ttu-id="954e5-138">Повторите шаги 5 и 6 для заданий 1070 и 1150.</span><span class="sxs-lookup"><span data-stu-id="954e5-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="954e5-139">Отображение категорий на сайте</span><span class="sxs-lookup"><span data-stu-id="954e5-139">Show categories on your site</span></span>

<span data-ttu-id="954e5-140">Чтобы отобразить иерархию категорий в интернет-магазине, необходимо добавить модуль меню переходов в соответствующее место в шаблоне или фрагменте.</span><span class="sxs-lookup"><span data-stu-id="954e5-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="954e5-141">Затем в модуле меню навигации будет показана иерархия переходов, при условии, что иерархия переходов торговли была опубликована в канале, к которому привязан сайт.</span><span class="sxs-lookup"><span data-stu-id="954e5-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="954e5-142">Модуль меню переходов, включенный в библиотеку модулей, позволяет пользователям перемещаться только по категориям, которые не имеют подкатегорий.</span><span class="sxs-lookup"><span data-stu-id="954e5-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="954e5-143">Если клиенты должны иметь возможность переходить к категориям, имеющим подкатегории, необходимо настроить модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="954e5-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="954e5-144">Добавление пользовательских параметров навигации</span><span class="sxs-lookup"><span data-stu-id="954e5-144">Add custom navigation options</span></span>

<span data-ttu-id="954e5-145">В меню переходов можно добавлять параметры навигации, которые не входят в иерархию категорий продуктов.</span><span class="sxs-lookup"><span data-stu-id="954e5-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="954e5-146">Например, в конце списка категорий продуктов можно добавить элемент **Свяжитесь с нами**, который указывает на страницу контактов, созданную для сайта.</span><span class="sxs-lookup"><span data-stu-id="954e5-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="954e5-147">Чтобы добавить пользовательские параметры навигации в меню навигации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="954e5-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="954e5-148">В шаблоне или фрагменте, который необходимо настроить, выберите модуль меню переходов.</span><span class="sxs-lookup"><span data-stu-id="954e5-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="954e5-149">В области свойств на вкладке **Данные** выберите **Добавить элемент**, чтобы создать новый элемент навигации в системе управления содержимым (CMS).</span><span class="sxs-lookup"><span data-stu-id="954e5-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="954e5-150">Введите текст ссылки и URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="954e5-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="954e5-151">Повторите шаги 2 и 3, чтобы добавить дополнительные параметры навигации.</span><span class="sxs-lookup"><span data-stu-id="954e5-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="954e5-152">По завершении выберите **Сохранить**, чтобы сохранить шаблон или фрагмент, затем выберите **Завершить редактирование**, чтобы вернуть его.</span><span class="sxs-lookup"><span data-stu-id="954e5-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="954e5-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="954e5-153">Additional resources</span></span>

[<span data-ttu-id="954e5-154">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="954e5-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="954e5-155">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="954e5-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="954e5-156">Работа с предустановленными макетами</span><span class="sxs-lookup"><span data-stu-id="954e5-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="954e5-157">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="954e5-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="954e5-158">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="954e5-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="954e5-159">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="954e5-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="954e5-160">Работа с группами публикаций</span><span class="sxs-lookup"><span data-stu-id="954e5-160">Work with publish groups</span></span>](publish-groups.md)
