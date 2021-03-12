---
title: Модуль "гармошка"
description: В этом разделе описываются модули гармошки, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 28cb9d2e450ff1c05d4faa5cac343e03ef051437
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986112"
---
# <a name="accordion-module"></a><span data-ttu-id="da697-103">Модуль "гармошка"</span><span class="sxs-lookup"><span data-stu-id="da697-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da697-104">В этом разделе описываются модули гармошки, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da697-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da697-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="da697-105">Overview</span></span>

<span data-ttu-id="da697-106">Модули "гармошка" являются модулями, аналогичными контейнерам, которые используются для упорядочения информации или модулей на странице путем создания свертываемых функций, аналогичных кассовым ящикам.</span><span class="sxs-lookup"><span data-stu-id="da697-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="da697-107">Модуль "гармошка" может использоваться на любой странице.</span><span class="sxs-lookup"><span data-stu-id="da697-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="da697-108">Внутри каждого модуля "гармошка" можно добавить один или несколько модулей элементов гармошки.</span><span class="sxs-lookup"><span data-stu-id="da697-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="da697-109">Каждый модуль элемента "гармошка" представляет собой свертываемый кассовый ящик.</span><span class="sxs-lookup"><span data-stu-id="da697-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="da697-110">Внутри каждого модуля элемента "гармошка" можно добавить один или несколько модулей.</span><span class="sxs-lookup"><span data-stu-id="da697-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="da697-111">Нет никаких ограничений на типы модулей, которые могут быть добавлены в модуль элемента "гармошка".</span><span class="sxs-lookup"><span data-stu-id="da697-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="da697-112">На следующем рисунке показан пример модуля "гармошка", который используется для упорядочения информации на странице часто задаваемых вопросов о магазине.</span><span class="sxs-lookup"><span data-stu-id="da697-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Пример модуля "гармошка"](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="da697-114">Свойства модуля "гармошка"</span><span class="sxs-lookup"><span data-stu-id="da697-114">Accordion module properties</span></span>

| <span data-ttu-id="da697-115">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="da697-115">Property name</span></span> | <span data-ttu-id="da697-116">Значения</span><span class="sxs-lookup"><span data-stu-id="da697-116">Values</span></span> | <span data-ttu-id="da697-117">описание</span><span class="sxs-lookup"><span data-stu-id="da697-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="da697-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="da697-118">Heading</span></span> | <span data-ttu-id="da697-119">Текст</span><span class="sxs-lookup"><span data-stu-id="da697-119">Text</span></span> | <span data-ttu-id="da697-120">Это свойство задает необязательный заголовок текста для модуля "гармошка".</span><span class="sxs-lookup"><span data-stu-id="da697-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="da697-121">Развернуть все</span><span class="sxs-lookup"><span data-stu-id="da697-121">Expand All</span></span> | <span data-ttu-id="da697-122">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="da697-122">**True** or **False**</span></span> | <span data-ttu-id="da697-123">Если для параметра установлено значение **Истина**, функция развертывания/свертывания включена, поэтому все элементы в модуле "гармошка" могут быть развернуты и свернуты.</span><span class="sxs-lookup"><span data-stu-id="da697-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="da697-124">Стиль взаимодействия</span><span class="sxs-lookup"><span data-stu-id="da697-124">Interaction Style</span></span> | <span data-ttu-id="da697-125">**Независимый** или **Развернуть только один элемент**</span><span class="sxs-lookup"><span data-stu-id="da697-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="da697-126">Это свойство определяет стиль взаимодействия для элементов "гармошка".</span><span class="sxs-lookup"><span data-stu-id="da697-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="da697-127">Если задано значение **Независимый**, то каждый элемент "гармошка" может быть развернут или свернут независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="da697-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="da697-128">Если для параметра установлено значение **Развернуть только один элемент**, только один элемент может быть развернут за один раз.</span><span class="sxs-lookup"><span data-stu-id="da697-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="da697-129">При развертывании элемента сворачиваются ранее развернутые элементы.</span><span class="sxs-lookup"><span data-stu-id="da697-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="da697-130">Свойства модуля элемента "гармошка"</span><span class="sxs-lookup"><span data-stu-id="da697-130">Accordion item module properties</span></span>

| <span data-ttu-id="da697-131">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="da697-131">Property name</span></span> | <span data-ttu-id="da697-132">Значения</span><span class="sxs-lookup"><span data-stu-id="da697-132">Values</span></span> | <span data-ttu-id="da697-133">описание</span><span class="sxs-lookup"><span data-stu-id="da697-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="da697-134">Должность</span><span class="sxs-lookup"><span data-stu-id="da697-134">Title</span></span> | <span data-ttu-id="da697-135">Текст</span><span class="sxs-lookup"><span data-stu-id="da697-135">Text</span></span> | <span data-ttu-id="da697-136">Это свойство задает текст названия для модуля элемента "гармошка".</span><span class="sxs-lookup"><span data-stu-id="da697-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="da697-137">Выбрав область заголовка, пользователи могут разворачивать или сворачивать раздел.</span><span class="sxs-lookup"><span data-stu-id="da697-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="da697-138">Развернуть по умолчанию</span><span class="sxs-lookup"><span data-stu-id="da697-138">Expand by default</span></span> | <span data-ttu-id="da697-139">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="da697-139">**True** or **False**</span></span> | <span data-ttu-id="da697-140">Если для этого параметра установлено значение **Истина**, при загрузке страницы элемент "гармошка" разворачивается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da697-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="da697-141">Добавление модуля "гармошка" на страницу вопросов и ответов</span><span class="sxs-lookup"><span data-stu-id="da697-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="da697-142">Чтобы добавить модуль "гармошка" на страницу вопросов и ответов и задать необходимые свойства в построителе сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da697-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="da697-143">Перейдите **Страницы** и используйте маркетинговый шаблон Fabrikam (или любой другой шаблон без ограничений), чтобы создать страницу с именем **Store FAQ**.</span><span class="sxs-lookup"><span data-stu-id="da697-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="da697-144">В слоте **Главный** **Страницы по умолчанию** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="da697-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="da697-145">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da697-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="da697-146">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="da697-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="da697-147">В диалоговом окне **Добавить модуль** выберите модуль **Гармошка**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da697-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="da697-148">На панели свойств модуля "гармошка" выберите **Заголовок** рядом с символом карандаша.</span><span class="sxs-lookup"><span data-stu-id="da697-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="da697-149">В диалоговом окне **Заголовок** в поле **Текст заголовка** введите **Часто задаваемые вопросы**.</span><span class="sxs-lookup"><span data-stu-id="da697-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="da697-150">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="da697-150">Then select **OK**.</span></span>
1. <span data-ttu-id="da697-151">На панели свойств модуля "гармошка" установите флажок **Развернуть все**, а затем в поле **Стиль взаимодействия** выберите **Независимый**.</span><span class="sxs-lookup"><span data-stu-id="da697-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="da697-152">В ячейке **Гармошка** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="da697-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="da697-153">В диалоговом окне **Добавить модуль** выберите модуль **Элемент "гармошка"**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da697-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="da697-154">В области свойства модуля элемента "гармошка" в области **Название** введите текст названия (например, **Как работают возвраты?**).</span><span class="sxs-lookup"><span data-stu-id="da697-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="da697-155">В ячейке **Элемент "гармошка"** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="da697-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="da697-156">В диалоговом окне **Добавить модуль** выберите модуль **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da697-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="da697-157">В области свойств модуля блока текста введите абзац текста (например, **Возвраты должны обрабатываться центром обработки вызовов. Обратитесь по телефону 1-800-FABRIKAM по поводу возврата. Для продуктов предусмотрена политика возврата 30 дней. Возвраты должны быть инициированы в течение этого временного интервала.**).</span><span class="sxs-lookup"><span data-stu-id="da697-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="da697-158">Добавьте в ячейку **Гармошка** несколько дополнительных модулей элемента "гармошка".</span><span class="sxs-lookup"><span data-stu-id="da697-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="da697-159">В каждом модуле элемента "гармошка" добавьте модуль блока текста с содержимым.</span><span class="sxs-lookup"><span data-stu-id="da697-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="da697-160">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="da697-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="da697-161">На странице будет показан модуль "гармошка" с добавленным содержимым.</span><span class="sxs-lookup"><span data-stu-id="da697-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="da697-162">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="da697-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da697-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da697-163">Additional resources</span></span>

[<span data-ttu-id="da697-164">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="da697-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="da697-165">Модуль контейнера</span><span class="sxs-lookup"><span data-stu-id="da697-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="da697-166">Модуль вкладок</span><span class="sxs-lookup"><span data-stu-id="da697-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="da697-167">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="da697-167">Text block module</span></span>](add-content-rich-block.md)
