---
title: Модуль вкладок
description: В этом разделе описываются модули вкладок, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209235"
---
# <a name="tab-module"></a><span data-ttu-id="f5f21-103">Модуль вкладок</span><span class="sxs-lookup"><span data-stu-id="f5f21-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5f21-104">В этом разделе описываются модули вкладок, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5f21-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f5f21-105">Модули вкладок являются модулями, аналогичными контейнерам, которые используются для упорядочивания информации на странице сайта на вкладках.</span><span class="sxs-lookup"><span data-stu-id="f5f21-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="f5f21-106">Они могут использоваться на любой странице, где должны быть представлены данные на вкладках.</span><span class="sxs-lookup"><span data-stu-id="f5f21-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="f5f21-107">Внутри каждого модуля вкладок можно добавить один или несколько модулей элементов вкладок.</span><span class="sxs-lookup"><span data-stu-id="f5f21-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="f5f21-108">Каждый модуль элементов вкладок представляет собой одну вкладку. В каждом модуле элемента вкладок можно добавить один или несколько модулей.</span><span class="sxs-lookup"><span data-stu-id="f5f21-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="f5f21-109">Нет никаких ограничений на типы модулей, которые могут быть добавлены в модуль элемента вкладок.</span><span class="sxs-lookup"><span data-stu-id="f5f21-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="f5f21-110">На следующем рисунке показан пример модуля вкладок на странице сайта.</span><span class="sxs-lookup"><span data-stu-id="f5f21-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="f5f21-111">В этом примере выбрана вкладка **Отгрузка**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-111">In this example, the **Shipping** tab selected.</span></span>

![Пример модуля вкладок](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="f5f21-113">Свойства модуля вкладок</span><span class="sxs-lookup"><span data-stu-id="f5f21-113">Tab module properties</span></span>

| <span data-ttu-id="f5f21-114">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="f5f21-114">Property name</span></span> | <span data-ttu-id="f5f21-115">Значения</span><span class="sxs-lookup"><span data-stu-id="f5f21-115">Values</span></span> | <span data-ttu-id="f5f21-116">описание</span><span class="sxs-lookup"><span data-stu-id="f5f21-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f5f21-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f5f21-117">Heading</span></span> | <span data-ttu-id="f5f21-118">Текст</span><span class="sxs-lookup"><span data-stu-id="f5f21-118">Text</span></span> | <span data-ttu-id="f5f21-119">Это свойство задает необязательный заголовок текста для модуля вкладок.</span><span class="sxs-lookup"><span data-stu-id="f5f21-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="f5f21-120">Индекс активной вкладки</span><span class="sxs-lookup"><span data-stu-id="f5f21-120">Active Tab Index</span></span> | <span data-ttu-id="f5f21-121">Номер</span><span class="sxs-lookup"><span data-stu-id="f5f21-121">Number</span></span> | <span data-ttu-id="f5f21-122">Это свойство определяет вкладку, которая должна быть активной по умолчанию при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="f5f21-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="f5f21-123">Если значение не указано, первый элемент вкладки является активным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5f21-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="f5f21-124">Свойства модуля элемента вкладок</span><span class="sxs-lookup"><span data-stu-id="f5f21-124">Tab item module properties</span></span>

| <span data-ttu-id="f5f21-125">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="f5f21-125">Property name</span></span> | <span data-ttu-id="f5f21-126">Значения</span><span class="sxs-lookup"><span data-stu-id="f5f21-126">Values</span></span> | <span data-ttu-id="f5f21-127">описание</span><span class="sxs-lookup"><span data-stu-id="f5f21-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f5f21-128">Должность</span><span class="sxs-lookup"><span data-stu-id="f5f21-128">Title</span></span> | <span data-ttu-id="f5f21-129">Текст</span><span class="sxs-lookup"><span data-stu-id="f5f21-129">Text</span></span> | <span data-ttu-id="f5f21-130">Это свойство задает текст названия для модуля элемента вкладок.</span><span class="sxs-lookup"><span data-stu-id="f5f21-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="f5f21-131">Добавление модуля вкладок на страницу</span><span class="sxs-lookup"><span data-stu-id="f5f21-131">Add a tab module to a page</span></span>

<span data-ttu-id="f5f21-132">Чтобы добавить модуль вкладок на страницу и задать свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f5f21-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="f5f21-133">Используйте маркетинговый шаблон Fabrikam (или любой другой шаблон без ограничений), чтобы создать страницу с именем **Страница политик запасов**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="f5f21-134">В слоте **Главный** **Страницы по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5f21-135">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5f21-136">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5f21-137">В диалоговом окне **Добавить модуль** выберите модуль **Вкладка**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5f21-138">На панели свойств модуля вкладок выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="f5f21-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="f5f21-139">В диалоговом окне **Заголовок** в поле **Текст заголовка** введите текст заголовка (например, **Политики**).</span><span class="sxs-lookup"><span data-stu-id="f5f21-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="f5f21-140">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-140">Then select **OK**.</span></span>
1. <span data-ttu-id="f5f21-141">В ячейке **Вкладка** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5f21-142">В диалоговом окне **Добавить модуль** выберите модуль **Элемент вкладки**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5f21-143">В области свойства модуля элемента вкладок в области **Название** введите текст названия (например, **Поставка**).</span><span class="sxs-lookup"><span data-stu-id="f5f21-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="f5f21-144">В ячейке **Элемент вкладки** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f5f21-145">В диалоговом окне **Добавить модуль** выберите модуль **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f5f21-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f5f21-146">В области свойств модуля блока текста добавьте текст в поле **Форматированный текст**, введите абзац текста.</span><span class="sxs-lookup"><span data-stu-id="f5f21-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="f5f21-147">В ячейке **Вкладка** добавьте несколько дополнительных модулей элементов вкладок с заголовками.</span><span class="sxs-lookup"><span data-stu-id="f5f21-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="f5f21-148">В каждом модуле элемента вкладок добавьте модуль блока текста с содержимым.</span><span class="sxs-lookup"><span data-stu-id="f5f21-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="f5f21-149">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="f5f21-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f5f21-150">На странице будет показан модуль вкладок, содержащий модули элемента вкладки, для которых было добавлено содержимое.</span><span class="sxs-lookup"><span data-stu-id="f5f21-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="f5f21-151">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="f5f21-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5f21-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5f21-152">Additional resources</span></span>

[<span data-ttu-id="f5f21-153">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="f5f21-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f5f21-154">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="f5f21-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f5f21-155">Модуль гармошек</span><span class="sxs-lookup"><span data-stu-id="f5f21-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="f5f21-156">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="f5f21-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]