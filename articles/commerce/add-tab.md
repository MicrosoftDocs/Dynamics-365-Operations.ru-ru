---
title: Модуль вкладок
description: В этом разделе описываются модули вкладок, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621021"
---
# <a name="tab-module"></a><span data-ttu-id="837ad-103">Модуль вкладок</span><span class="sxs-lookup"><span data-stu-id="837ad-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="837ad-104">В этом разделе описываются модули вкладок, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="837ad-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="837ad-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="837ad-105">Overview</span></span>

<span data-ttu-id="837ad-106">Модули вкладок являются модулями, аналогичными контейнерам, которые используются для упорядочивания информации на странице сайта на вкладках.</span><span class="sxs-lookup"><span data-stu-id="837ad-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="837ad-107">Они могут использоваться на любой странице, где должны быть представлены данные на вкладках.</span><span class="sxs-lookup"><span data-stu-id="837ad-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="837ad-108">Внутри каждого модуля вкладок можно добавить один или несколько модулей элементов вкладок.</span><span class="sxs-lookup"><span data-stu-id="837ad-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="837ad-109">Каждый модуль элементов вкладок представляет собой одну вкладку. В каждом модуле элемента вкладок можно добавить один или несколько модулей.</span><span class="sxs-lookup"><span data-stu-id="837ad-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="837ad-110">Нет никаких ограничений на типы модулей, которые могут быть добавлены в модуль элемента вкладок.</span><span class="sxs-lookup"><span data-stu-id="837ad-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="837ad-111">На следующем рисунке показан пример модуля вкладок на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="837ad-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="837ad-112">В этом примере выбрана вкладка **Отгрузка**.</span><span class="sxs-lookup"><span data-stu-id="837ad-112">In this example, the **Shipping** tab selected.</span></span>

![Пример модуля вкладок](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="837ad-114">Свойства модуля вкладок</span><span class="sxs-lookup"><span data-stu-id="837ad-114">Tab module properties</span></span>

| <span data-ttu-id="837ad-115">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="837ad-115">Property name</span></span> | <span data-ttu-id="837ad-116">Значения</span><span class="sxs-lookup"><span data-stu-id="837ad-116">Values</span></span> | <span data-ttu-id="837ad-117">описание</span><span class="sxs-lookup"><span data-stu-id="837ad-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="837ad-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="837ad-118">Heading</span></span> | <span data-ttu-id="837ad-119">Текст</span><span class="sxs-lookup"><span data-stu-id="837ad-119">Text</span></span> | <span data-ttu-id="837ad-120">Это свойство задает необязательный заголовок текста для модуля вкладок.</span><span class="sxs-lookup"><span data-stu-id="837ad-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="837ad-121">Индекс активной вкладки</span><span class="sxs-lookup"><span data-stu-id="837ad-121">Active Tab Index</span></span> | <span data-ttu-id="837ad-122">Номер</span><span class="sxs-lookup"><span data-stu-id="837ad-122">Number</span></span> | <span data-ttu-id="837ad-123">Это свойство определяет вкладку, которая должна быть активной по умолчанию при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="837ad-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="837ad-124">Если значение не указано, первый элемент вкладки является активным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="837ad-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="837ad-125">Свойства модуля элемента вкладок</span><span class="sxs-lookup"><span data-stu-id="837ad-125">Tab item module properties</span></span>

| <span data-ttu-id="837ad-126">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="837ad-126">Property name</span></span> | <span data-ttu-id="837ad-127">Значения</span><span class="sxs-lookup"><span data-stu-id="837ad-127">Values</span></span> | <span data-ttu-id="837ad-128">описание</span><span class="sxs-lookup"><span data-stu-id="837ad-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="837ad-129">Должность</span><span class="sxs-lookup"><span data-stu-id="837ad-129">Title</span></span> | <span data-ttu-id="837ad-130">Текст</span><span class="sxs-lookup"><span data-stu-id="837ad-130">Text</span></span> | <span data-ttu-id="837ad-131">Это свойство задает текст названия для модуля элемента вкладок.</span><span class="sxs-lookup"><span data-stu-id="837ad-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="837ad-132">Добавление модуля вкладок на страницу</span><span class="sxs-lookup"><span data-stu-id="837ad-132">Add a tab module to a page</span></span>

<span data-ttu-id="837ad-133">Чтобы добавить модуль вкладок на страницу и задать свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="837ad-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="837ad-134">Используйте маркетинговый шаблон Fabrikam (или любой другой шаблон без ограничений), чтобы создать страницу с именем **Страница политик запасов**.</span><span class="sxs-lookup"><span data-stu-id="837ad-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="837ad-135">В слоте **Главный** **Страницы по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="837ad-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837ad-136">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="837ad-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="837ad-137">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="837ad-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837ad-138">В диалоговом окне **Добавить модуль** выберите модуль **Вкладка**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="837ad-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="837ad-139">На панели свойств модуля вкладок выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="837ad-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="837ad-140">В диалоговом окне **Заголовок** в поле **Текст заголовка** введите текст заголовка (например, **Политики**).</span><span class="sxs-lookup"><span data-stu-id="837ad-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="837ad-141">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="837ad-141">Then select **OK**.</span></span>
1. <span data-ttu-id="837ad-142">В ячейке **Вкладка** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="837ad-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837ad-143">В диалоговом окне **Добавить модуль** выберите модуль **Элемент вкладки**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="837ad-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="837ad-144">В области свойства модуля элемента вкладок в области **Название** введите текст названия (например, **Поставка**).</span><span class="sxs-lookup"><span data-stu-id="837ad-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="837ad-145">В ячейке **Элемент вкладки** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="837ad-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837ad-146">В диалоговом окне **Добавить модуль** выберите модуль **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="837ad-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="837ad-147">В области свойств модуля блока текста добавьте текст в поле **Форматированный текст**, введите абзац текста.</span><span class="sxs-lookup"><span data-stu-id="837ad-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="837ad-148">В ячейке **Вкладка** добавьте несколько дополнительных модулей элементов вкладок с заголовками.</span><span class="sxs-lookup"><span data-stu-id="837ad-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="837ad-149">В каждом модуле элемента вкладок добавьте модуль блока текста с содержимым.</span><span class="sxs-lookup"><span data-stu-id="837ad-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="837ad-150">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="837ad-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="837ad-151">На странице будет показан модуль вкладок, содержащий модули элемента вкладки, для которых было добавлено содержимое.</span><span class="sxs-lookup"><span data-stu-id="837ad-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="837ad-152">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="837ad-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="837ad-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="837ad-153">Additional resources</span></span>

[<span data-ttu-id="837ad-154">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="837ad-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="837ad-155">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="837ad-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="837ad-156">Модуль "гармошка"</span><span class="sxs-lookup"><span data-stu-id="837ad-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="837ad-157">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="837ad-157">Text block module</span></span>](add-content-rich-block.md)
