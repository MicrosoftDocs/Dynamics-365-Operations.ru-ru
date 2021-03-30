---
title: Модуль блока текста
description: В этом разделе описываются модули блока текста, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206399"
---
# <a name="text-block-module"></a><span data-ttu-id="8d14f-103">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="8d14f-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d14f-104">В этом разделе описываются модули блока текста, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d14f-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8d14f-105">Модуль блока текста — это модуль, который используется для добавления текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d14f-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="8d14f-106">Это содержимое может быть информационным или рекламным.</span><span class="sxs-lookup"><span data-stu-id="8d14f-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="8d14f-107">Модули блока текста управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="8d14f-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="8d14f-108">Это самостоятельные модули, которые не зависят от контекста страницы или других модулей.</span><span class="sxs-lookup"><span data-stu-id="8d14f-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="8d14f-109">Примеры модулей блока текста в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="8d14f-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="8d14f-110">Модули блока текста могут использоваться следующими способами:</span><span class="sxs-lookup"><span data-stu-id="8d14f-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="8d14f-111">Для демонстрации особенностей продукта на странице сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="8d14f-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="8d14f-112">Для информационных целей на любой странице.</span><span class="sxs-lookup"><span data-stu-id="8d14f-112">For informational purposes on any page.</span></span> <span data-ttu-id="8d14f-113">Например, они могут объяснить преимущества программ лояльности, описать политики отгрузки и возврата, отвечать на часто задаваемые вопросы или предоставить содержимое "О нас".</span><span class="sxs-lookup"><span data-stu-id="8d14f-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="8d14f-114">Для добавления пользовательских сообщений на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="8d14f-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="8d14f-115">(Например, "Бесплатная доставка для заказов свыше 50 долларов США").</span><span class="sxs-lookup"><span data-stu-id="8d14f-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="8d14f-116">Для уведомлений об отказе от ответственности и контактной информации на страницах сведений о продуктах, страницах корзины, страницах оформления заказа и других страницах (например, "Доставка и возвраты производятся в соответствии с политиками магазина").</span><span class="sxs-lookup"><span data-stu-id="8d14f-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="8d14f-117">На следующем рисунке показан пример модуля блока текста, используемый на главной странице.</span><span class="sxs-lookup"><span data-stu-id="8d14f-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Пример модуля блока текста](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="8d14f-119">Свойства модуля блока текста</span><span class="sxs-lookup"><span data-stu-id="8d14f-119">Text block module properties</span></span>

| <span data-ttu-id="8d14f-120">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="8d14f-120">Property name</span></span>     | <span data-ttu-id="8d14f-121">значение</span><span class="sxs-lookup"><span data-stu-id="8d14f-121">Value</span></span>                                            | <span data-ttu-id="8d14f-122">описание</span><span class="sxs-lookup"><span data-stu-id="8d14f-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="8d14f-123">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="8d14f-123">Rich text</span></span>         | <span data-ttu-id="8d14f-124">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="8d14f-124">Rich text</span></span>                                        | <span data-ttu-id="8d14f-125">Текст абзаца.</span><span class="sxs-lookup"><span data-stu-id="8d14f-125">Paragraph text.</span></span> <span data-ttu-id="8d14f-126">Поддерживаются некоторые основные возможности форматированного текста, такие как жирный шрифт, подчеркнутый текст и курсив.</span><span class="sxs-lookup"><span data-stu-id="8d14f-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="8d14f-127">Настраиваемое имя класса</span><span class="sxs-lookup"><span data-stu-id="8d14f-127">Custom class name</span></span> | <span data-ttu-id="8d14f-128">Имя класса каскадных таблиц стилей (CSS)</span><span class="sxs-lookup"><span data-stu-id="8d14f-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="8d14f-129">Имя настраиваемого класса CSS, предоставляемого разработчиком для форматирования данного модуля.</span><span class="sxs-lookup"><span data-stu-id="8d14f-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="8d14f-130">Имя класса должно быть определено в пакете тем.</span><span class="sxs-lookup"><span data-stu-id="8d14f-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="8d14f-131">Размер шрифта</span><span class="sxs-lookup"><span data-stu-id="8d14f-131">Font size</span></span>         | <span data-ttu-id="8d14f-132">**Малый**, **Средний**, **Большой** или **Очень большой**</span><span class="sxs-lookup"><span data-stu-id="8d14f-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="8d14f-133">Размер шрифта содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d14f-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="8d14f-134">Добавление модуля блока текста на страницу</span><span class="sxs-lookup"><span data-stu-id="8d14f-134">Add a text block module to a page</span></span>

<span data-ttu-id="8d14f-135">Чтобы добавить модуль блока текста на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d14f-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8d14f-136">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="8d14f-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="8d14f-137">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблона содержимого**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="8d14f-138">В ячейке **Содержание** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d14f-139">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d14f-140">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="8d14f-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="8d14f-141">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="8d14f-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="8d14f-142">В диалоговом окне **Выбор шаблона** выберите **Шаблон содержимого**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="8d14f-143">В поле **Имя страницы** введите **Страница содержимого**, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="8d14f-144">В слоте **Главный** новой страницы выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d14f-145">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d14f-146">В области свойств модуля контейнера задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="8d14f-147">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d14f-148">В диалоговом окне **Добавить модуль** выберите модуль **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="8d14f-149">В области свойств модуля блока текста добавьте текст в поле **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="8d14f-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="8d14f-150">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="8d14f-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="8d14f-151">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="8d14f-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d14f-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d14f-152">Additional resources</span></span>

[<span data-ttu-id="8d14f-153">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="8d14f-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8d14f-154">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="8d14f-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="8d14f-155">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="8d14f-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8d14f-156">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="8d14f-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="8d14f-157">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="8d14f-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]