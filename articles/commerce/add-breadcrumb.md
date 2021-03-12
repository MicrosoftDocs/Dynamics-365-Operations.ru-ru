---
title: Модуль навигации
description: В этом разделе описываются модули навигации, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 1883281c62575ae0b48b6e584876185bb179b4f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986087"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="71653-103">Модуль навигации</span><span class="sxs-lookup"><span data-stu-id="71653-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71653-104">В этом разделе описываются модули навигации, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71653-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="71653-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="71653-105">Overview</span></span>

<span data-ttu-id="71653-106">Модули навигации используются для дополнительной навигации по страницам сайта.</span><span class="sxs-lookup"><span data-stu-id="71653-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="71653-107">Обычно они отображаются в верхней части страницы, под заголовком.</span><span class="sxs-lookup"><span data-stu-id="71653-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="71653-108">Хотя модули навигации могут быть добавлены на любую страницу, они чаще всего используются на страницах сведений о продуктах (PDP), чтобы показать иерархию категорий продуктов и обеспечить быстрый способ перемещения по сайту.</span><span class="sxs-lookup"><span data-stu-id="71653-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="71653-109">Модуль навигации можно также использовать для отображения ссылки "Назад к результатам", когда пользователи открывают PDP из поиска или со страницы списка.</span><span class="sxs-lookup"><span data-stu-id="71653-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="71653-110">Таким образом пользователи могут быстро вернуться на страницу отфильтрованного списка для продолжения покупок.</span><span class="sxs-lookup"><span data-stu-id="71653-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="71653-111">На страницах с контекстом категории продукта, таких как страницы PDP и страницы категории, в модуле навигации отображается иерархия категорий.</span><span class="sxs-lookup"><span data-stu-id="71653-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="71653-112">На страницах без контекста категорий в модуле навигации по умолчанию отображается **&lt;Корень сайта&gt; / &lt;Текущая страница&gt;**.</span><span class="sxs-lookup"><span data-stu-id="71653-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="71653-113">Модули навигации также можно настроить вручную на других типах страниц сайта, чтобы отобразить ссылки на отдельные страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="71653-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="71653-114">Модуль иерархической навигации доступен в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="71653-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="71653-115">На следующем рисунке показан пример модуля навигации, который показывает иерархию категорий в PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Пример модуля навигации](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="71653-117">Параметры модуля навигации</span><span class="sxs-lookup"><span data-stu-id="71653-117">Breadcrumb module settings</span></span>

<span data-ttu-id="71653-118">Модуль навигации основывается на параметре **Тип отображения навигации в PDP**, который определен в разделе **Параметры сайта \> Расширения** в построителе сайтов.</span><span class="sxs-lookup"><span data-stu-id="71653-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="71653-119">Этот параметр имеет три возможных значения:</span><span class="sxs-lookup"><span data-stu-id="71653-119">This setting has three possible values:</span></span>

- <span data-ttu-id="71653-120">**Показать иерархию категорий** — если выбрано это значение, в модуле навигации будет отображаться полная иерархия категорий продукта, просматриваемого в PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="71653-121">**Назад к результатам** — если выбрано это значение, в модуле навигации будет показана ссылка "Назад к результатам" в PDP, если пользователь открыл PDP из модуля, который разрешает ссылку "Назад к результатам".</span><span class="sxs-lookup"><span data-stu-id="71653-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="71653-122">Эта функция доступна при переходе пользователей со страниц категорий, поиска, списка и рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="71653-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="71653-123">Для поддержки этой функции в модулях "коллекция продуктов" и "результаты поиска" есть свойство с именем **Разрешить возврат к результатам к PDP**.</span><span class="sxs-lookup"><span data-stu-id="71653-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="71653-124">Это свойство позволяет гибко определить, какие модули должны поддерживать функцию ссылки "Назад к результатам" в PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="71653-125">Например, если выбрано **Назад к результатам** для параметра **Типе отображения навигации в PDP** модуля навигации и **Разрешить возврат к результатам к PDP** и выбрано для модуля результатов поиска на странице поиска, ссылка "Назад к результатам" будет отображаться, когда пользователи переходят со страницы поиска в PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="71653-126">**Показать иерархию категорий и вернуться к результатам** — это значение представляет собой комбинацию предыдущих двух значений.</span><span class="sxs-lookup"><span data-stu-id="71653-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="71653-127">Если выбрано это значение, в модуле навигации будет отображаться полная иерархия категорий и ссылка "Назад к результатам" (если настроено) в PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71653-128">Эти параметры доступны в выпуске Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="71653-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="71653-129">Если выполняется обновление из более ранней версии Dynamics 365 Commerce, необходимо вручную обновить файл appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="71653-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="71653-130">Инструкции по обновлению файла appsettings.json см. в разделе [Обновления SDK и библиотеки модулей](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="71653-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="71653-131">Свойства модуля навигации</span><span class="sxs-lookup"><span data-stu-id="71653-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="71653-132">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="71653-132">Property name</span></span> | <span data-ttu-id="71653-133">Значения</span><span class="sxs-lookup"><span data-stu-id="71653-133">Values</span></span> | <span data-ttu-id="71653-134">описание</span><span class="sxs-lookup"><span data-stu-id="71653-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="71653-135">Корневой</span><span class="sxs-lookup"><span data-stu-id="71653-135">Root</span></span> | <span data-ttu-id="71653-136">Текст или ссылка</span><span class="sxs-lookup"><span data-stu-id="71653-136">Text or link</span></span>| <span data-ttu-id="71653-137">Это необязательное свойство указывает текст ссылки и цель ссылки для корневого сайта навигации.</span><span class="sxs-lookup"><span data-stu-id="71653-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="71653-138">Если это свойство не настроено, корень не определен.</span><span class="sxs-lookup"><span data-stu-id="71653-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="71653-139">Ссылка навигации</span><span class="sxs-lookup"><span data-stu-id="71653-139">Breadcrumb link</span></span> | <span data-ttu-id="71653-140">Связь</span><span class="sxs-lookup"><span data-stu-id="71653-140">Link</span></span> | <span data-ttu-id="71653-141">Это необязательное свойство задает ссылки для навигации, настроенной вручную, если эти ссылки являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="71653-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="71653-142">Ссылки отображаются в том порядке, в котором они перечислены.</span><span class="sxs-lookup"><span data-stu-id="71653-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="71653-143">Добавление модуля навигации на новую страницу</span><span class="sxs-lookup"><span data-stu-id="71653-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="71653-144">Чтобы добавить модуль навигации на PDP и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="71653-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="71653-145">Перейдите в раздел **Параметры сайта \> Расширения**, затем для параметра **Тип отображения навигации в PDP** выберите **Показать иерархию категорий**.</span><span class="sxs-lookup"><span data-stu-id="71653-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="71653-146">Перейдите в раздел **Шаблоны** и выберите шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="71653-147">В ячейке **Контейнер**, содержащей модуль поля покупки, нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="71653-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="71653-148">В диалоговом окне **Добавить модуль** выберите модуль **Навигация**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="71653-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="71653-149">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="71653-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="71653-150">Перейдите в раздел **Страницы** и откройте PDP, использующую шаблон PDP.</span><span class="sxs-lookup"><span data-stu-id="71653-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="71653-151">Если PDP еще не существует, создайте ее.</span><span class="sxs-lookup"><span data-stu-id="71653-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="71653-152">В ячейке **Контейнер**, содержащей модуль поля покупки, нажмите многоточие (**…**), а затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="71653-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="71653-153">В диалоговом окне **Добавить модуль** выберите модуль **Навигация**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="71653-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="71653-154">В области свойств ячейки **Навигации** в области **Корень** выберите **Текст ссылки**.</span><span class="sxs-lookup"><span data-stu-id="71653-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="71653-155">В диалоговом окне **Текст ссылки** введите **Домашняя страница**, а затем в **Цель ссылки** выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="71653-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="71653-156">В диалоговом окне **Добавление ссылки** выберите ссылку для корня навигации, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="71653-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="71653-157">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="71653-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="71653-158">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="71653-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71653-159">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="71653-159">Additional resources</span></span>

[<span data-ttu-id="71653-160">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="71653-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="71653-161">Модуль меню навигации</span><span class="sxs-lookup"><span data-stu-id="71653-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="71653-162">Модуль выбора сайта</span><span class="sxs-lookup"><span data-stu-id="71653-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="71653-163">Обзор целевой страницы категории и страницы результатов поиска по умолчанию</span><span class="sxs-lookup"><span data-stu-id="71653-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="71653-164">Модули семейства продуктов</span><span class="sxs-lookup"><span data-stu-id="71653-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="71653-165">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="71653-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="71653-166">Обновления SDK и библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="71653-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
