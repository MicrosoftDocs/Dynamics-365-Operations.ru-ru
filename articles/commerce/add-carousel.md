---
title: Модуль карусели
description: В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785245"
---
# <a name="carousel-module"></a><span data-ttu-id="ea009-103">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="ea009-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ea009-104">В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea009-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ea009-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ea009-105">Overview</span></span>

<span data-ttu-id="ea009-106">Модуль карусели используется для помещения в карусель нескольких рекламных элементов, которые могут просматривать клиенты.</span><span class="sxs-lookup"><span data-stu-id="ea009-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="ea009-107">Это специальный контейнерный модуль, в котором размещаются другие модули.</span><span class="sxs-lookup"><span data-stu-id="ea009-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="ea009-108">Например, розничный продавец может использовать модуль карусели на домашней странице для демонстрации нескольких новых продуктов или рекламных акций.</span><span class="sxs-lookup"><span data-stu-id="ea009-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="ea009-109">Можно добавлять модули главного имиджевого баннера и компонентов в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="ea009-110">Затем свойства модуля карусели определяют способ отображения этих модулей.</span><span class="sxs-lookup"><span data-stu-id="ea009-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="ea009-111">Примеры модулей карусели в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="ea009-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="ea009-112">На домашней странице можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="ea009-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="ea009-113">На странице сведений о продукте можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="ea009-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="ea009-114">Карусель может использоваться на любой странице маркетинга для продвижения нескольких рекламных акций или продуктов.</span><span class="sxs-lookup"><span data-stu-id="ea009-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="ea009-115">Свойства модуля карусели</span><span class="sxs-lookup"><span data-stu-id="ea009-115">Carousel module properties</span></span>

| <span data-ttu-id="ea009-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="ea009-116">Property name</span></span>             | <span data-ttu-id="ea009-117">Стоимость</span><span class="sxs-lookup"><span data-stu-id="ea009-117">Value</span></span>                                | <span data-ttu-id="ea009-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ea009-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="ea009-119">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="ea009-119">Autoplay</span></span>                  | <span data-ttu-id="ea009-120">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="ea009-120">**True** or **False**</span></span>                | <span data-ttu-id="ea009-121">Если установлено значение **True**, переход между элементами в карусели происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="ea009-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="ea009-122">Если установлено значение **False**, переход будет выполняться только в том случае, если клиент использует клавиатуру или мышь для перемещения от одного элемента к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="ea009-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="ea009-123">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="ea009-123">Slide transition interval</span></span> | <span data-ttu-id="ea009-124">Значение в секундах</span><span class="sxs-lookup"><span data-stu-id="ea009-124">A value in seconds</span></span>                   | <span data-ttu-id="ea009-125">Интервал для переходов между элементами.</span><span class="sxs-lookup"><span data-stu-id="ea009-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="ea009-126">Анимация перехода</span><span class="sxs-lookup"><span data-stu-id="ea009-126">Transition animation</span></span>      | <span data-ttu-id="ea009-127">**Сдвиг** или **Исчезание**</span><span class="sxs-lookup"><span data-stu-id="ea009-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="ea009-128">Эффект перехода.</span><span class="sxs-lookup"><span data-stu-id="ea009-128">The transition effect.</span></span> |
| <span data-ttu-id="ea009-129">Ширина</span><span class="sxs-lookup"><span data-stu-id="ea009-129">Width</span></span>                     | <span data-ttu-id="ea009-130">**Вписать в контейнер** или **Заполнить экран**</span><span class="sxs-lookup"><span data-stu-id="ea009-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="ea009-131">Если значение равно **Вписать в контейнер**, элементы внутри модуля карусели ограничиваются шириной модуля карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="ea009-132">Если установлено значение **Заполнить экран**, элементы не ограничиваются шириной карусели, но могут быть переведены в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="ea009-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="ea009-133">Можно изменить значение для достижения требуемого макета.</span><span class="sxs-lookup"><span data-stu-id="ea009-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="ea009-134">Добавление модуля карусели на страницу</span><span class="sxs-lookup"><span data-stu-id="ea009-134">Add a carousel module to a page</span></span>

<span data-ttu-id="ea009-135">Чтобы добавить модуль карусели на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea009-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ea009-136">Создайте шаблон страницы с именем **шаблон карусели**.</span><span class="sxs-lookup"><span data-stu-id="ea009-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="ea009-137">В слоте **Главный** страницы по умолчанию добавьте модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="ea009-138">Добавьте модуль главного имиджевого баннера в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="ea009-139">Добавьте модуль компонента в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="ea009-140">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="ea009-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="ea009-141">Используйте только что созданный шаблон карусели для создания страницы с именем **страница карусели**.</span><span class="sxs-lookup"><span data-stu-id="ea009-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="ea009-142">В слоте **Главный** новой страницы добавьте модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="ea009-143">Установите для свойства **Ширина** модуля карусели значение **Заполнять экран**.</span><span class="sxs-lookup"><span data-stu-id="ea009-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="ea009-144">Задайте для свойства **Анимация перехода** значение **Сдвиг**.</span><span class="sxs-lookup"><span data-stu-id="ea009-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="ea009-145">Добавьте модуль главного имиджевого баннера в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="ea009-146">В модуле главного имиджевого баннера добавьте изображение и заголовок, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ea009-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="ea009-147">Добавьте модуль компонента в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="ea009-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="ea009-148">В модуле компонента добавьте изображение, заголовок и абзац текста.</span><span class="sxs-lookup"><span data-stu-id="ea009-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="ea009-149">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="ea009-149">Save and preview the page.</span></span> <span data-ttu-id="ea009-150">На странице должна отображаться карусель с двумя модулями внутри (модуль главного имиджевого баннера и модуль компонента).</span><span class="sxs-lookup"><span data-stu-id="ea009-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="ea009-151">Для получения нужного эффекта можно изменить дополнительные свойства модулей карусели, главного имиджевого баннера и компонента.</span><span class="sxs-lookup"><span data-stu-id="ea009-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="ea009-152">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="ea009-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea009-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ea009-153">Additional resources</span></span>

[<span data-ttu-id="ea009-154">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="ea009-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ea009-155">Модуль оповещения</span><span class="sxs-lookup"><span data-stu-id="ea009-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="ea009-156">Модуль блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="ea009-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ea009-157">Модуль размещения содержимого</span><span class="sxs-lookup"><span data-stu-id="ea009-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="ea009-158">Модуль компонента</span><span class="sxs-lookup"><span data-stu-id="ea009-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="ea009-159">Модуль главного имиджевого баннера</span><span class="sxs-lookup"><span data-stu-id="ea009-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="ea009-160">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="ea009-160">Video player module</span></span>](add-video-player.md)
