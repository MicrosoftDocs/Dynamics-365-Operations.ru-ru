---
title: Модуль блока насыщенного содержимого
description: В этом разделе описываются модули блока насыщенного содержимого, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785429"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="40139-103">Модуль блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="40139-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="40139-104">В этом разделе описываются модули блока насыщенного содержимого, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40139-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40139-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="40139-105">Overview</span></span>

<span data-ttu-id="40139-106">Модуль блока насыщенного содержимого — это специальный контейнер, в который может быть помещен один или несколько элементов блока насыщенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="40139-107">Модули блока насыщенного содержимого используются для текстового содержимого на странице.</span><span class="sxs-lookup"><span data-stu-id="40139-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="40139-108">Это содержимое может быть информационным или рекламным.</span><span class="sxs-lookup"><span data-stu-id="40139-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="40139-109">Модули блока насыщенного содержимого управляются данными из системы управления контентом (CMS) и могут быть размещены на любой странице.</span><span class="sxs-lookup"><span data-stu-id="40139-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="40139-110">Это самостоятельные модули, которые не зависят от контекста страницы или других модулей.</span><span class="sxs-lookup"><span data-stu-id="40139-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="40139-111">Примеры модулей блока насыщенного содержимого в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="40139-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="40139-112">Модули блока насыщенного содержимого могут использоваться следующими способами:</span><span class="sxs-lookup"><span data-stu-id="40139-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="40139-113">Для демонстрации особенностей продукта на странице сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="40139-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="40139-114">Для информационных целей на любой странице.</span><span class="sxs-lookup"><span data-stu-id="40139-114">For informational purposes on any page.</span></span> <span data-ttu-id="40139-115">Например, они могут объяснить преимущества программ лояльности, описать политики отгрузки и возврата, отвечать на часто задаваемые вопросы или предоставить содержимое "О нас".</span><span class="sxs-lookup"><span data-stu-id="40139-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="40139-116">Для добавления пользовательских сообщений на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="40139-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="40139-117">(Например, "Бесплатная доставка для заказов свыше 50 долларов США").</span><span class="sxs-lookup"><span data-stu-id="40139-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="40139-118">Для уведомлений об отказе от ответственности и контактной информации на страницах сведений о продуктах, страницах корзины, страницах оформления заказа и других страницах (например, "Доставка и возвраты производятся в соответствии с политиками магазина").</span><span class="sxs-lookup"><span data-stu-id="40139-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="40139-119">Свойства модуля блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="40139-119">Content rich block module properties</span></span>

| <span data-ttu-id="40139-120">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="40139-120">Property name</span></span>     | <span data-ttu-id="40139-121">Стоимость</span><span class="sxs-lookup"><span data-stu-id="40139-121">Value</span></span>                                 | <span data-ttu-id="40139-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="40139-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="40139-123">Число столбцов</span><span class="sxs-lookup"><span data-stu-id="40139-123">Number of columns</span></span> | <span data-ttu-id="40139-124">Число от **1** до **4**</span><span class="sxs-lookup"><span data-stu-id="40139-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="40139-125">Число столбцов в блоке насыщенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="40139-126">Может быть не более четырех столбцов.</span><span class="sxs-lookup"><span data-stu-id="40139-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="40139-127">Ширина</span><span class="sxs-lookup"><span data-stu-id="40139-127">Width</span></span>             | <span data-ttu-id="40139-128">**Вписать в контейнер** или **Заполнить экран**</span><span class="sxs-lookup"><span data-stu-id="40139-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="40139-129">Если значение равно **Вписать в контейнер**, элементы внутри контейнера ограничиваются шириной контейнера.</span><span class="sxs-lookup"><span data-stu-id="40139-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="40139-130">Если установлено значение **Заполнить экран**, элементы не ограничиваются шириной контейнера, но могут быть переведены в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="40139-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="40139-131">Можно изменить значение для достижения требуемого макета.</span><span class="sxs-lookup"><span data-stu-id="40139-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="40139-132">Свойства модуля элемента блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="40139-132">Content rich block item module properties</span></span>

| <span data-ttu-id="40139-133">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="40139-133">Property name</span></span> | <span data-ttu-id="40139-134">Стоимость</span><span class="sxs-lookup"><span data-stu-id="40139-134">Value</span></span>          | <span data-ttu-id="40139-135">Описание</span><span class="sxs-lookup"><span data-stu-id="40139-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="40139-136">Абзац</span><span class="sxs-lookup"><span data-stu-id="40139-136">Paragraph</span></span>     | <span data-ttu-id="40139-137">Текст абзаца</span><span class="sxs-lookup"><span data-stu-id="40139-137">Paragraph text</span></span> | <span data-ttu-id="40139-138">Текст, сопровождающий каждый элемент блока насыщенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="40139-139">Поддерживаются некоторые основные возможности форматированного текста, такие как жирный шрифт, подчеркнутый текст и курсив.</span><span class="sxs-lookup"><span data-stu-id="40139-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="40139-140">Добавление модуля блока насыщенного содержимого на страницу</span><span class="sxs-lookup"><span data-stu-id="40139-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="40139-141">Чтобы добавить модуль блока насыщенного содержимого на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40139-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="40139-142">Создайте шаблон страницы с именем **Шаблон содержимого**.</span><span class="sxs-lookup"><span data-stu-id="40139-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="40139-143">В слоте **Главный** страницы по умолчанию добавьте модуль блока насыщенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="40139-144">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="40139-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="40139-145">Используйте только что созданный шаблон содержимого для создания страницы с именем **Страница содержимого**.</span><span class="sxs-lookup"><span data-stu-id="40139-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="40139-146">В слоте **Главный** новой страницы добавьте модуль блока насыщенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="40139-147">В свойствах модуля блока насыщенного содержимого установите число столбцов равное **2**.</span><span class="sxs-lookup"><span data-stu-id="40139-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="40139-148">В модуле блока насыщенного содержимого выберите **Добавить модуль** и добавьте элемент блока насыщенного содержимого (например, **item1**).</span><span class="sxs-lookup"><span data-stu-id="40139-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="40139-149">В новом элементе блока насыщенного содержимого добавьте текст абзаца.</span><span class="sxs-lookup"><span data-stu-id="40139-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="40139-150">В модуле блока насыщенного содержимого выберите **Добавить модуль** и добавьте элемент блока насыщенного содержимого (например, **item2**).</span><span class="sxs-lookup"><span data-stu-id="40139-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="40139-151">В новом элементе блока насыщенного содержимого добавьте текст абзаца.</span><span class="sxs-lookup"><span data-stu-id="40139-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="40139-152">Сохраните страницу и просмотрите изменения.</span><span class="sxs-lookup"><span data-stu-id="40139-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="40139-153">В представлении из двух столбцов должны отобразиться два блока форматированного текста.</span><span class="sxs-lookup"><span data-stu-id="40139-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="40139-154">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="40139-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="40139-155">Если добавить третий элемент блока насыщенного содержимого, он будет расположен под двумя добавленными ранее элементами.</span><span class="sxs-lookup"><span data-stu-id="40139-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="40139-156">Изменяя число столбцов и элементов в контейнере, можно получить различные макеты для текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="40139-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40139-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="40139-157">Additional resources</span></span>

[<span data-ttu-id="40139-158">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="40139-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="40139-159">Модуль оповещения</span><span class="sxs-lookup"><span data-stu-id="40139-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="40139-160">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="40139-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="40139-161">Модуль размещения содержимого</span><span class="sxs-lookup"><span data-stu-id="40139-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="40139-162">Модуль компонента</span><span class="sxs-lookup"><span data-stu-id="40139-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="40139-163">Модуль главного имиджевого баннера</span><span class="sxs-lookup"><span data-stu-id="40139-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="40139-164">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="40139-164">Video player module</span></span>](add-video-player.md)

