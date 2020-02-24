---
title: Модуль карусели
description: В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025789"
---
# <a name="carousel-module"></a><span data-ttu-id="b834c-103">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="b834c-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b834c-104">В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b834c-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b834c-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b834c-105">Overview</span></span>

<span data-ttu-id="b834c-106">Модуль карусели используется для помещения во вращающийся карусельный баннер нескольких рекламных элементов (включая форматированные изображения), которые могут просматривать клиенты.</span><span class="sxs-lookup"><span data-stu-id="b834c-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="b834c-107">Например, розничный продавец может использовать модуль карусели на домашней странице для демонстрации нескольких новых продуктов или рекламных акций.</span><span class="sxs-lookup"><span data-stu-id="b834c-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="b834c-108">Можно добавлять модули блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="b834c-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="b834c-109">Затем свойства модуля карусели определяют способ отображения этих модулей.</span><span class="sxs-lookup"><span data-stu-id="b834c-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="b834c-110">Примеры модулей карусели в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="b834c-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="b834c-111">На домашней странице можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="b834c-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="b834c-112">На странице сведений о продукте можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="b834c-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="b834c-113">Карусель может использоваться на любой странице маркетинга для продвижения нескольких рекламных акций или продуктов.</span><span class="sxs-lookup"><span data-stu-id="b834c-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="b834c-114">Свойства модуля карусели</span><span class="sxs-lookup"><span data-stu-id="b834c-114">Carousel module properties</span></span>

| <span data-ttu-id="b834c-115">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="b834c-115">Property name</span></span>             | <span data-ttu-id="b834c-116">Стоимость</span><span class="sxs-lookup"><span data-stu-id="b834c-116">Value</span></span>                 | <span data-ttu-id="b834c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b834c-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b834c-118">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="b834c-118">Autoplay</span></span>                  | <span data-ttu-id="b834c-119">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="b834c-119">**True** or **False**</span></span> | <span data-ttu-id="b834c-120">Если установлено значение **True**, переход между элементами в карусели происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="b834c-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="b834c-121">Если установлено значение **False**, переход будет выполняться только в том случае, если клиент использует клавиатуру или мышь для перемещения от одного элемента к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="b834c-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="b834c-122">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="b834c-122">Slide transition interval</span></span> | <span data-ttu-id="b834c-123">Значение в секундах</span><span class="sxs-lookup"><span data-stu-id="b834c-123">A value in seconds</span></span>    | <span data-ttu-id="b834c-124">Интервал для переходов между элементами.</span><span class="sxs-lookup"><span data-stu-id="b834c-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="b834c-125">Тип перехода</span><span class="sxs-lookup"><span data-stu-id="b834c-125">Transition type</span></span>           | <span data-ttu-id="b834c-126">**Сдвиг** или **Исчезание**</span><span class="sxs-lookup"><span data-stu-id="b834c-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="b834c-127">Эффект перехода между элементами.</span><span class="sxs-lookup"><span data-stu-id="b834c-127">The transition effect between items.</span></span> |
| <span data-ttu-id="b834c-128">Скрыть флиппер карусели</span><span class="sxs-lookup"><span data-stu-id="b834c-128">Hide carousel flipper</span></span>     | <span data-ttu-id="b834c-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="b834c-129">**True** or **False**</span></span> | <span data-ttu-id="b834c-130">Если значение задано как **True**, флиппер карусели и индикатор последовательности скрыты.</span><span class="sxs-lookup"><span data-stu-id="b834c-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="b834c-131">Разрешить отклонить карусель</span><span class="sxs-lookup"><span data-stu-id="b834c-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="b834c-132">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="b834c-132">**True** or **False**</span></span> | <span data-ttu-id="b834c-133">Если установлено значение **True**, пользовали могут отменить карусель.</span><span class="sxs-lookup"><span data-stu-id="b834c-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="b834c-134">Добавление модуля карусели на страницу</span><span class="sxs-lookup"><span data-stu-id="b834c-134">Add a carousel module to a page</span></span>

<span data-ttu-id="b834c-135">Чтобы добавить модуль карусели на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b834c-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b834c-136">Создайте шаблон страницы с именем **шаблон карусели**.</span><span class="sxs-lookup"><span data-stu-id="b834c-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="b834c-137">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="b834c-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="b834c-138">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="b834c-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="b834c-139">Используйте только что созданный шаблон карусели для создания страницы с именем **страница карусели**.</span><span class="sxs-lookup"><span data-stu-id="b834c-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="b834c-140">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="b834c-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="b834c-141">В области справа задайте значение **Ширина** как **Заполнить экран**.</span><span class="sxs-lookup"><span data-stu-id="b834c-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="b834c-142">В области **Структура страницы** добавьте модуль карусели в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="b834c-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="b834c-143">Добавьте модуль блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="b834c-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="b834c-144">Задайте свойства модуля блока содержимого, задав **Заголовок**, **Ссылка**, **Макет** и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="b834c-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="b834c-145">Добавьте и настройте другой модуль блока содержимого.</span><span class="sxs-lookup"><span data-stu-id="b834c-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="b834c-146">Настройте дополнительные свойства модуля карусели по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="b834c-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="b834c-147">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="b834c-147">Save and preview the page.</span></span> <span data-ttu-id="b834c-148">На странице должна отображаться карусель с двумя модулями внутри (модуль главного имиджевого баннера и модуль компонента).</span><span class="sxs-lookup"><span data-stu-id="b834c-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="b834c-149">Для получения нужного эффекта можно изменить дополнительные свойства модулей карусели, главного имиджевого баннера и компонента.</span><span class="sxs-lookup"><span data-stu-id="b834c-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="b834c-150">Завершите редактирование страницы и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="b834c-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b834c-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b834c-151">Additional resources</span></span>

[<span data-ttu-id="b834c-152">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="b834c-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b834c-153">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="b834c-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b834c-154">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="b834c-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b834c-155">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="b834c-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b834c-156">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="b834c-156">Video player module</span></span>](add-video-player.md)
