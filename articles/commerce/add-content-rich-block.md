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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415173"
---
# <a name="text-block-module"></a><span data-ttu-id="adfc2-103">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="adfc2-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adfc2-104">В этом разделе описываются модули блока текста, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="adfc2-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="adfc2-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="adfc2-105">Overview</span></span>

<span data-ttu-id="adfc2-106">Модуль блока текста — это модуль, который используется для добавления текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="adfc2-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="adfc2-107">Это содержимое может быть информационным или рекламным.</span><span class="sxs-lookup"><span data-stu-id="adfc2-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="adfc2-108">Модули блока текста управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="adfc2-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="adfc2-109">Это самостоятельные модули, которые не зависят от контекста страницы или других модулей.</span><span class="sxs-lookup"><span data-stu-id="adfc2-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="adfc2-110">Примеры модулей блока текста в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="adfc2-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="adfc2-111">Модули блока текста могут использоваться следующими способами:</span><span class="sxs-lookup"><span data-stu-id="adfc2-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="adfc2-112">Для демонстрации особенностей продукта на странице сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="adfc2-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="adfc2-113">Для информационных целей на любой странице.</span><span class="sxs-lookup"><span data-stu-id="adfc2-113">For informational purposes on any page.</span></span> <span data-ttu-id="adfc2-114">Например, они могут объяснить преимущества программ лояльности, описать политики отгрузки и возврата, отвечать на часто задаваемые вопросы или предоставить содержимое "О нас".</span><span class="sxs-lookup"><span data-stu-id="adfc2-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="adfc2-115">Для добавления пользовательских сообщений на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="adfc2-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="adfc2-116">(Например, "Бесплатная доставка для заказов свыше 50 долларов США").</span><span class="sxs-lookup"><span data-stu-id="adfc2-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="adfc2-117">Для уведомлений об отказе от ответственности и контактной информации на страницах сведений о продуктах, страницах корзины, страницах оформления заказа и других страницах (например, "Доставка и возвраты производятся в соответствии с политиками магазина").</span><span class="sxs-lookup"><span data-stu-id="adfc2-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="adfc2-118">На следующем рисунке показан пример модуля блока текста, используемый на главной странице.</span><span class="sxs-lookup"><span data-stu-id="adfc2-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Пример модуля блока текста](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="adfc2-120">Свойства модуля блока текста</span><span class="sxs-lookup"><span data-stu-id="adfc2-120">Text block module properties</span></span>

| <span data-ttu-id="adfc2-121">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="adfc2-121">Property name</span></span>     | <span data-ttu-id="adfc2-122">значение</span><span class="sxs-lookup"><span data-stu-id="adfc2-122">Value</span></span>                                            | <span data-ttu-id="adfc2-123">описание</span><span class="sxs-lookup"><span data-stu-id="adfc2-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="adfc2-124">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="adfc2-124">Rich text</span></span>         | <span data-ttu-id="adfc2-125">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="adfc2-125">Rich text</span></span>                                        | <span data-ttu-id="adfc2-126">Текст абзаца.</span><span class="sxs-lookup"><span data-stu-id="adfc2-126">Paragraph text.</span></span> <span data-ttu-id="adfc2-127">Поддерживаются некоторые основные возможности форматированного текста, такие как жирный шрифт, подчеркнутый текст и курсив.</span><span class="sxs-lookup"><span data-stu-id="adfc2-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="adfc2-128">Настраиваемое имя класса</span><span class="sxs-lookup"><span data-stu-id="adfc2-128">Custom class name</span></span> | <span data-ttu-id="adfc2-129">Имя класса каскадных таблиц стилей (CSS)</span><span class="sxs-lookup"><span data-stu-id="adfc2-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="adfc2-130">Имя настраиваемого класса CSS, предоставляемого разработчиком для форматирования данного модуля.</span><span class="sxs-lookup"><span data-stu-id="adfc2-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="adfc2-131">Имя класса должно быть определено в пакете тем.</span><span class="sxs-lookup"><span data-stu-id="adfc2-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="adfc2-132">Размер шрифта</span><span class="sxs-lookup"><span data-stu-id="adfc2-132">Font size</span></span>         | <span data-ttu-id="adfc2-133">**Малый**, **Средний**, **Большой** или **Очень большой**</span><span class="sxs-lookup"><span data-stu-id="adfc2-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="adfc2-134">Размер шрифта содержимого.</span><span class="sxs-lookup"><span data-stu-id="adfc2-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="adfc2-135">Добавление модуля блока текста на страницу</span><span class="sxs-lookup"><span data-stu-id="adfc2-135">Add a text block module to a page</span></span>

<span data-ttu-id="adfc2-136">Чтобы добавить модуль блока текста на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="adfc2-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="adfc2-137">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="adfc2-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="adfc2-138">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблона содержимого**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="adfc2-139">В ячейке **Содержание** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adfc2-140">В диалоговом окне **Добавить модуль** выберите модуль **Страница по умолчанию**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adfc2-141">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="adfc2-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="adfc2-142">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="adfc2-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="adfc2-143">В диалоговом окне **Выбор шаблона** выберите **Шаблон содержимого**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="adfc2-144">В поле **Имя страницы** введите **Страница содержимого**, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="adfc2-145">В слоте **Главный** новой страницы выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adfc2-146">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adfc2-147">В области свойств модуля контейнера задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="adfc2-148">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adfc2-149">В диалоговом окне **Добавить модуль** выберите модуль **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="adfc2-150">В области свойств модуля блока текста добавьте текст в поле **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="adfc2-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="adfc2-151">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="adfc2-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="adfc2-152">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="adfc2-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adfc2-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="adfc2-153">Additional resources</span></span>

[<span data-ttu-id="adfc2-154">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="adfc2-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="adfc2-155">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="adfc2-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="adfc2-156">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="adfc2-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="adfc2-157">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="adfc2-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="adfc2-158">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="adfc2-158">Video player module</span></span>](add-video-player.md)

