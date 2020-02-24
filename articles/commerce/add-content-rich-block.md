---
title: Модуль блока текста
description: В этом разделе описываются модули блока текста, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025605"
---
# <a name="text-block-module"></a><span data-ttu-id="a19d9-103">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="a19d9-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a19d9-104">В этом разделе описываются модули блока текста, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a19d9-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a19d9-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="a19d9-105">Overview</span></span>

<span data-ttu-id="a19d9-106">Модуль блока текста — это модуль, который используется для добавления текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="a19d9-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="a19d9-107">Это содержимое может быть информационным или рекламным.</span><span class="sxs-lookup"><span data-stu-id="a19d9-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="a19d9-108">Модули блока текста управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="a19d9-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="a19d9-109">Это самостоятельные модули, которые не зависят от контекста страницы или других модулей.</span><span class="sxs-lookup"><span data-stu-id="a19d9-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="a19d9-110">Примеры модулей блока текста в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="a19d9-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="a19d9-111">Модули блока текста могут использоваться следующими способами:</span><span class="sxs-lookup"><span data-stu-id="a19d9-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="a19d9-112">Для демонстрации особенностей продукта на странице сведений о продукте</span><span class="sxs-lookup"><span data-stu-id="a19d9-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="a19d9-113">Для информационных целей на любой странице.</span><span class="sxs-lookup"><span data-stu-id="a19d9-113">For informational purposes on any page.</span></span> <span data-ttu-id="a19d9-114">Например, они могут объяснить преимущества программ лояльности, описать политики отгрузки и возврата, отвечать на часто задаваемые вопросы или предоставить содержимое "О нас".</span><span class="sxs-lookup"><span data-stu-id="a19d9-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="a19d9-115">Для добавления пользовательских сообщений на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="a19d9-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="a19d9-116">(Например, "Бесплатная доставка для заказов свыше 50 долларов США").</span><span class="sxs-lookup"><span data-stu-id="a19d9-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="a19d9-117">Для уведомлений об отказе от ответственности и контактной информации на страницах сведений о продуктах, страницах корзины, страницах оформления заказа и других страницах (например, "Доставка и возвраты производятся в соответствии с политиками магазина").</span><span class="sxs-lookup"><span data-stu-id="a19d9-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="a19d9-118">Свойства модуля блока текста</span><span class="sxs-lookup"><span data-stu-id="a19d9-118">Text block module properties</span></span>

| <span data-ttu-id="a19d9-119">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a19d9-119">Property name</span></span>     | <span data-ttu-id="a19d9-120">Value</span><span class="sxs-lookup"><span data-stu-id="a19d9-120">Value</span></span>                                            | <span data-ttu-id="a19d9-121">Описание</span><span class="sxs-lookup"><span data-stu-id="a19d9-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="a19d9-122">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="a19d9-122">Rich text</span></span>         | <span data-ttu-id="a19d9-123">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="a19d9-123">Rich text</span></span>                                        | <span data-ttu-id="a19d9-124">Текст абзаца.</span><span class="sxs-lookup"><span data-stu-id="a19d9-124">Paragraph text.</span></span> <span data-ttu-id="a19d9-125">Поддерживаются некоторые основные возможности форматированного текста, такие как жирный шрифт, подчеркнутый текст и курсив.</span><span class="sxs-lookup"><span data-stu-id="a19d9-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="a19d9-126">Настраиваемое имя класса</span><span class="sxs-lookup"><span data-stu-id="a19d9-126">Custom class name</span></span> | <span data-ttu-id="a19d9-127">Имя класса каскадных таблиц стилей (CSS)</span><span class="sxs-lookup"><span data-stu-id="a19d9-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="a19d9-128">Имя настраиваемого класса CSS, предоставляемого разработчиком для форматирования данного модуля.</span><span class="sxs-lookup"><span data-stu-id="a19d9-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="a19d9-129">Имя класса должно быть определено в пакете тем.</span><span class="sxs-lookup"><span data-stu-id="a19d9-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="a19d9-130">Размер шрифта</span><span class="sxs-lookup"><span data-stu-id="a19d9-130">Font size</span></span>         | <span data-ttu-id="a19d9-131">**Малый**, **Средний**, **Большой** или **Очень большой**</span><span class="sxs-lookup"><span data-stu-id="a19d9-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="a19d9-132">Размер шрифта содержимого.</span><span class="sxs-lookup"><span data-stu-id="a19d9-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="a19d9-133">Добавление модуля блока текста на страницу</span><span class="sxs-lookup"><span data-stu-id="a19d9-133">Add a text block module to a page</span></span>

<span data-ttu-id="a19d9-134">Чтобы добавить модуль блока текста на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a19d9-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a19d9-135">Создайте шаблон страницы с именем **Шаблон содержимого**.</span><span class="sxs-lookup"><span data-stu-id="a19d9-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="a19d9-136">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="a19d9-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="a19d9-137">Завершите редактирование шаблона и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="a19d9-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="a19d9-138">Используйте только что созданный шаблон содержимого для создания страницы с именем **Страница содержимого**.</span><span class="sxs-lookup"><span data-stu-id="a19d9-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="a19d9-139">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="a19d9-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="a19d9-140">В области свойств модуля контейнера задайте для свойства **Ширина** **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="a19d9-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="a19d9-141">Добавьте модуль блока текста в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="a19d9-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="a19d9-142">В области свойств модуля блока текста добавьте текст в поле **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="a19d9-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="a19d9-143">Завершите редактирование страницы и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="a19d9-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a19d9-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a19d9-144">Additional resources</span></span>

[<span data-ttu-id="a19d9-145">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="a19d9-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a19d9-146">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="a19d9-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="a19d9-147">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="a19d9-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a19d9-148">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="a19d9-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="a19d9-149">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="a19d9-149">Video player module</span></span>](add-video-player.md)

