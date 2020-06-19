---
title: Модуль навигации
description: В этом разделе описываются модули навигации, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417400"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="f8eeb-103">Модуль навигации</span><span class="sxs-lookup"><span data-stu-id="f8eeb-103">Breadcrumb module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f8eeb-104">В этом разделе описываются модули навигации, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8eeb-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f8eeb-105">Overview</span></span>

<span data-ttu-id="f8eeb-106">Модули навигации используются для дополнительной навигации по страницам сайта.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="f8eeb-107">Обычно они отображаются в верхней части страницы, под заголовком.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="f8eeb-108">Хотя модули навигации могут быть добавлены на любую страницу, они чаще всего используются на страницах сведений о продуктах (PDP), чтобы показать иерархию категорий продуктов и обеспечить быстрый способ перемещения по сайту.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="f8eeb-109">Модуль навигации можно также использовать для отображения ссылки "Назад к результатам", когда пользователи открывают PDP из поиска или со страницы списка.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="f8eeb-110">Таким образом пользователи могут быстро вернуться на страницу отфильтрованного списка для продолжения покупок.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="f8eeb-111">На страницах с контекстом категории продукта, таких как страницы PDP и страницы категории, в модуле навигации отображается иерархия категорий.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="f8eeb-112">На страницах без контекста категорий в модуле навигации по умолчанию отображается **&lt;Корень сайта&gt; / &lt;Текущая страница&gt;**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="f8eeb-113">Модули навигации также можно настроить вручную на других типах страниц сайта, чтобы отобразить ссылки на отдельные страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="f8eeb-114">На следующем рисунке показан пример модуля навигации, который показывает иерархию категорий в PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Пример модуля навигации](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="f8eeb-116">Параметры модуля навигации</span><span class="sxs-lookup"><span data-stu-id="f8eeb-116">Breadcrumb module settings</span></span>

<span data-ttu-id="f8eeb-117">Модуль навигации основывается на параметре **Тип отображения навигации в PDP**, который определен в разделе **Параметры сайта \> Расширения** в построителе сайтов.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="f8eeb-118">Этот параметр имеет три возможных значения:</span><span class="sxs-lookup"><span data-stu-id="f8eeb-118">This setting has three possible values:</span></span>

- <span data-ttu-id="f8eeb-119">**Показать иерархию категорий** — если выбрано это значение, в модуле навигации будет отображаться полная иерархия категорий продукта, просматриваемого в PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="f8eeb-120">**Назад к результатам** — если выбрано это значение, в модуле навигации будет показана ссылка "Назад к результатам" в PDP, если пользователь открыл PDP из модуля, который разрешает ссылку "Назад к результатам".</span><span class="sxs-lookup"><span data-stu-id="f8eeb-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="f8eeb-121">Эта функция доступна при переходе пользователей со страниц категорий, поиска, списка и рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="f8eeb-122">Для поддержки этой функции в модулях "коллекция продуктов" и "результаты поиска" есть свойство с именем **Разрешить возврат к результатам к PDP**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="f8eeb-123">Это свойство позволяет гибко определить, какие модули должны поддерживать функцию ссылки "Назад к результатам" в PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="f8eeb-124">Например, если выбрано **Назад к результатам** для параметра **Типе отображения навигации в PDP** модуля навигации и **Разрешить возврат к результатам к PDP** и выбрано для модуля результатов поиска на странице поиска, ссылка "Назад к результатам" будет отображаться, когда пользователи переходят со страницы поиска в PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="f8eeb-125">**Показать иерархию категорий и вернуться к результатам** — это значение представляет собой комбинацию предыдущих двух значений.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="f8eeb-126">Если выбрано это значение, в модуле навигации будет отображаться полная иерархия категорий и ссылка "Назад к результатам" (если настроено) в PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="f8eeb-127">Свойства модуля навигации</span><span class="sxs-lookup"><span data-stu-id="f8eeb-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="f8eeb-128">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="f8eeb-128">Property name</span></span> | <span data-ttu-id="f8eeb-129">Значения</span><span class="sxs-lookup"><span data-stu-id="f8eeb-129">Values</span></span> | <span data-ttu-id="f8eeb-130">описание</span><span class="sxs-lookup"><span data-stu-id="f8eeb-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f8eeb-131">Корневой</span><span class="sxs-lookup"><span data-stu-id="f8eeb-131">Root</span></span> | <span data-ttu-id="f8eeb-132">Текст или ссылка</span><span class="sxs-lookup"><span data-stu-id="f8eeb-132">Text or link</span></span>| <span data-ttu-id="f8eeb-133">Это необязательное свойство указывает текст ссылки и цель ссылки для корневого сайта навигации.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="f8eeb-134">Если это свойство не настроено, корень не определен.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="f8eeb-135">Ссылка навигации</span><span class="sxs-lookup"><span data-stu-id="f8eeb-135">Breadcrumb link</span></span> | <span data-ttu-id="f8eeb-136">Связь</span><span class="sxs-lookup"><span data-stu-id="f8eeb-136">Link</span></span> | <span data-ttu-id="f8eeb-137">Это необязательное свойство задает ссылки для навигации, настроенной вручную, если эти ссылки являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="f8eeb-138">Ссылки отображаются в том порядке, в котором они перечислены.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="f8eeb-139">Добавление модуля навигации на новую страницу</span><span class="sxs-lookup"><span data-stu-id="f8eeb-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="f8eeb-140">Чтобы добавить модуль навигации на PDP и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f8eeb-141">Перейдите **Параметры сайта /> Расширения**, а затем выберите параметр **Типе отображения навигации в PDP**, выберите **Показать иерархию категорий и вернуться к результатам**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="f8eeb-142">Перейдите в раздел **Шаблоны** и выберите шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="f8eeb-143">В ячейке **Контейнер**, содержащей модуль поля покупки, нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f8eeb-144">В диалоговом окне **Добавить модуль** выберите модуль **Навигация**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f8eeb-145">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f8eeb-146">Перейдите в раздел **Страницы** и откройте PDP, использующую шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="f8eeb-147">Если PDP еще не существует, создайте ее.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="f8eeb-148">В ячейке **Контейнер**, содержащей модуль поля покупки, нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f8eeb-149">В диалоговом окне **Добавить модуль** выберите модуль **Навигация**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f8eeb-150">В области свойств ячейки **Навигации** в области **Корень** выберите **Текст ссылки**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="f8eeb-151">В диалоговом окне **Текст ссылки** введите **Домашняя страница**, а затем в **Цель ссылки** выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="f8eeb-152">В диалоговом окне **Добавление ссылки** выберите ссылку для корня навигации, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="f8eeb-153">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f8eeb-154">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="f8eeb-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8eeb-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8eeb-155">Additional resources</span></span>

[<span data-ttu-id="f8eeb-156">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="f8eeb-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f8eeb-157">Обзор целевой страницы категории и страницы результатов поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f8eeb-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="f8eeb-158">Модули семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="f8eeb-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="f8eeb-159">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="f8eeb-159">Buy box module</span></span>](add-buy-box.md)
