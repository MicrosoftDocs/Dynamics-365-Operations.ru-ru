---
title: Модуль результатов поиска
description: В этом разделе описываются модули результатов поиска, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 645022000d8746db3793a8a8611ab8f17c7bcc6e
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117141"
---
# <a name="search-results-module"></a><span data-ttu-id="13b15-103">Модуль результатов поиска</span><span class="sxs-lookup"><span data-stu-id="13b15-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="13b15-104">В этом разделе описываются модули результатов поиска, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="13b15-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="13b15-105">Модуль результатов поиска возвращает результаты поиска продуктов и список подходящих уточнений для продуктов.</span><span class="sxs-lookup"><span data-stu-id="13b15-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="13b15-106">Модули результатов поиска на сайтах Dynamics 365 Commerce могут использоваться для отображения страниц в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="13b15-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="13b15-107">Результаты поиска, которые инициируются поиском пользователя</span><span class="sxs-lookup"><span data-stu-id="13b15-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="13b15-108">Результаты поиска, отображающие конкретный набор продуктов, например "Купить похожие"</span><span class="sxs-lookup"><span data-stu-id="13b15-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="13b15-109">Списки продуктов, относящихся к категории</span><span class="sxs-lookup"><span data-stu-id="13b15-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="13b15-110">Дополнительные сведения о категориях и страницах результатов поиска см. в разделе [Обзор целевой страницы категории по умолчанию и страницы результатов поиска](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="13b15-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="13b15-111">На следующем рисунке показан пример страницы результатов поиска для категории на сайте Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="13b15-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Пример страницы результатов поиска на сайте Fabrikam](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="13b15-113">Свойства модуля результатов поиска</span><span class="sxs-lookup"><span data-stu-id="13b15-113">Search results module properties</span></span>

<span data-ttu-id="13b15-114">В следующей таблице перечислены свойства модулей результатов поиска вместе со значениями и описаниями.</span><span class="sxs-lookup"><span data-stu-id="13b15-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="13b15-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="13b15-115">Property</span></span> | <span data-ttu-id="13b15-116">Значения</span><span class="sxs-lookup"><span data-stu-id="13b15-116">Values</span></span> | <span data-ttu-id="13b15-117">описание</span><span class="sxs-lookup"><span data-stu-id="13b15-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="13b15-118">Номенклатур на странице</span><span class="sxs-lookup"><span data-stu-id="13b15-118">Items per page</span></span> | <span data-ttu-id="13b15-119">Целое число</span><span class="sxs-lookup"><span data-stu-id="13b15-119">Integer</span></span> | <span data-ttu-id="13b15-120">Число номенклатур, которое должно отображаться на каждой странице.</span><span class="sxs-lookup"><span data-stu-id="13b15-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="13b15-121">Разрешить возврат на странице с описанием продукта</span><span class="sxs-lookup"><span data-stu-id="13b15-121">Allow back on PDP</span></span> | <span data-ttu-id="13b15-122">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="13b15-122">**True** or **False**</span></span> | <span data-ttu-id="13b15-123">Если это свойство имеет значение **True**, то когда пользователь выбирает продукт на странице результатов поиска, в иерархической навигации на странице сведений о продукте (PDP), которая будет открыта, отобразится ссылка "Назад к результатам".</span><span class="sxs-lookup"><span data-stu-id="13b15-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="13b15-124">Развернуть уточнения</span><span class="sxs-lookup"><span data-stu-id="13b15-124">Expand Refiners</span></span> | <span data-ttu-id="13b15-125">**Все**, **1**, **2**, **3** или **4**</span><span class="sxs-lookup"><span data-stu-id="13b15-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="13b15-126">Число лучших уточнений, которые должны быть развернуты при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="13b15-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="13b15-127">Например, если это свойство имеет значение **3**, будут развернуты первые три уточнения на странице.</span><span class="sxs-lookup"><span data-stu-id="13b15-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="13b15-128">Скрыть отображение иерархии категорий</span><span class="sxs-lookup"><span data-stu-id="13b15-128">Hide category hierarchy display</span></span> | <span data-ttu-id="13b15-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="13b15-129">**True** or **False**</span></span> | <span data-ttu-id="13b15-130">Если это свойство имеет значение **True**, иерархия категорий на странице будет скрыта.</span><span class="sxs-lookup"><span data-stu-id="13b15-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="13b15-131">Это свойство должно иметь значение **True**, если используется [модуль иерархической навигации](add-breadcrumb.md) для отображения иерархии категорий.</span><span class="sxs-lookup"><span data-stu-id="13b15-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="13b15-132">Включать атрибуты продукта в результаты поиска</span><span class="sxs-lookup"><span data-stu-id="13b15-132">Include product attributes in search results</span></span> | <span data-ttu-id="13b15-133">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="13b15-133">**True** or **False**</span></span> | <span data-ttu-id="13b15-134">Если это свойство имеет значение **True**, для продуктов в результатах поиска будут возвращаться атрибуты.</span><span class="sxs-lookup"><span data-stu-id="13b15-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="13b15-135">Хотя эти атрибуты могут отображаться на сайте Commerce, требуется расширение.</span><span class="sxs-lookup"><span data-stu-id="13b15-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="13b15-136">Показывать цены для назначений</span><span class="sxs-lookup"><span data-stu-id="13b15-136">Show affiliation prices</span></span> | <span data-ttu-id="13b15-137">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="13b15-137">**True** or **False**</span></span> | <span data-ttu-id="13b15-138">Если это свойство имеет значение **True**, цены назначения для продуктов будут отображаться в результатах поиска, когда вошедший пользователь перейдет на страницу.</span><span class="sxs-lookup"><span data-stu-id="13b15-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |
| <span data-ttu-id="13b15-139">Обновление панели уточнения</span><span class="sxs-lookup"><span data-stu-id="13b15-139">Update refiner panel</span></span> | <span data-ttu-id="13b15-140">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="13b15-140">**True** or **False**</span></span> | <span data-ttu-id="13b15-141">Если это свойство имеет значение **True**, при выборе уточнений панель уточнений будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="13b15-141">If this property is set to **True**, the refiner panel will be updated when refiners are selected.</span></span> <span data-ttu-id="13b15-142">В этом режиме некоторые уточнения с множественным выбором будут вести себя как уточнения с единичным выбором при обновлении панели уточнений.</span><span class="sxs-lookup"><span data-stu-id="13b15-142">In this mode, some multiple-selection refiners will behave like single-selection refiners when the refiner panel is updated.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="13b15-143">В Commerce версии 10.0.16 и последующих версиях конфигурацию **Показать цены назначений** можно использовать для отображения цен назначения на странице.</span><span class="sxs-lookup"><span data-stu-id="13b15-143">In the Commerce version 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>
>
> <span data-ttu-id="13b15-144">В Commerce версии 10.0.20 и более поздних конфигурацию **Обновление панели уточнений** можно использовать для обновления панели уточнений во время выбора уточнения.</span><span class="sxs-lookup"><span data-stu-id="13b15-144">In the Commerce version 10.0.20 release and later, the **Update refiner panel** configuration can be used to update the refiner panel during refiner selection.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="13b15-145">Поддерживаемые модули</span><span class="sxs-lookup"><span data-stu-id="13b15-145">Supported modules</span></span>

<span data-ttu-id="13b15-146">Модуль результатов поиска поддерживает [модуль быстрого просмотра](quick-view-module.md), который позволяет пользователям просматривать сведения о продукте и добавлять номенклатуры в корзину со страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="13b15-146">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="13b15-147">Добавление модуля результатов поиска на страницу категорий</span><span class="sxs-lookup"><span data-stu-id="13b15-147">Add a search results module to a category page</span></span>

<span data-ttu-id="13b15-148">Чтобы добавить модуль результатов поиска на страницу категории, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="13b15-148">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="13b15-149">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="13b15-149">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="13b15-150">В диалоговом окне **Создать шаблон** введите имя **Результаты поиска**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-150">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="13b15-151">В ячейке **Содержание** выберите многоточие (...), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="13b15-151">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13b15-152">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-152">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13b15-153">В слоте **Главный** модуля **Страница по умолчанию** выберите многоточие (...), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="13b15-153">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13b15-154">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-154">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13b15-155">В ячейке **Контейнер** выберите многоточие (...), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="13b15-155">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13b15-156">В диалоговом окне **Добавить модуль** выберите модуль **Навигация**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-156">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13b15-157">В области свойств **Иерархическая навигация** введите значение **1** для **Мин. число вхождений**.</span><span class="sxs-lookup"><span data-stu-id="13b15-157">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="13b15-158">В ячейке **Контейнер** выберите многоточие (...), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="13b15-158">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="13b15-159">В диалоговом окне **Добавить модуль** выберите модуль **Результаты поиска**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-159">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="13b15-160">В области свойства **Результаты поиска** введите значение **1** для параметра **Мин. число вхождений**, затем задайте любые другие необходимые свойства для модуля результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="13b15-160">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="13b15-161">Настроив эти свойства в шаблоне, вы гарантируете, что все настройки конкретной страницы категорий будут автоматически включать эти параметры.</span><span class="sxs-lookup"><span data-stu-id="13b15-161">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="13b15-162">Выберите **Завершить редактирование**, а затем нажмите кнопку **Опубликовать**, чтобы опубликовать шаблон.</span><span class="sxs-lookup"><span data-stu-id="13b15-162">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="13b15-163">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="13b15-163">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="13b15-164">В диалоговом окне **Выбор шаблона** выберите созданный вами шаблон **Результаты поиска**, введите **Страница категории** для параметра **Имя страницы**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="13b15-164">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="13b15-165">Так как все значения заданы в шаблоне, страница готова к публикации.</span><span class="sxs-lookup"><span data-stu-id="13b15-165">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="13b15-166">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="13b15-166">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13b15-167">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13b15-167">Additional resources</span></span>

[<span data-ttu-id="13b15-168">Обзор целевой страницы категории и страницы результатов поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="13b15-168">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="13b15-169">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="13b15-169">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13b15-170">Модуль быстрого просмотра</span><span class="sxs-lookup"><span data-stu-id="13b15-170">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
