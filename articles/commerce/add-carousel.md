---
title: Модуль карусели
description: В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620994"
---
# <a name="carousel-module"></a><span data-ttu-id="535e0-103">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="535e0-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="535e0-104">В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="535e0-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="535e0-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="535e0-105">Overview</span></span>

<span data-ttu-id="535e0-106">Модуль карусели используется для помещения во вращающийся карусельный баннер нескольких рекламных элементов (включая форматированные изображения), которые могут просматривать клиенты.</span><span class="sxs-lookup"><span data-stu-id="535e0-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="535e0-107">Например, розничный продавец может использовать модуль карусели на домашней странице для демонстрации нескольких новых продуктов или рекламных акций.</span><span class="sxs-lookup"><span data-stu-id="535e0-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="535e0-108">Можно добавлять модули блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="535e0-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="535e0-109">Затем свойства модуля карусели определяют способ отображения этих модулей.</span><span class="sxs-lookup"><span data-stu-id="535e0-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="535e0-110">Примеры модулей карусели в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="535e0-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="535e0-111">На домашней странице можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="535e0-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="535e0-112">На странице сведений о продукте можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="535e0-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="535e0-113">Карусель может использоваться на любой странице маркетинга для продвижения нескольких рекламных акций или продуктов.</span><span class="sxs-lookup"><span data-stu-id="535e0-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="535e0-114">На следующем рисунке показан пример модуля карусели, используемый на главной странице.</span><span class="sxs-lookup"><span data-stu-id="535e0-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="535e0-115">Этот модуль карусели содержит несколько элементов блоков содержимого.</span><span class="sxs-lookup"><span data-stu-id="535e0-115">This carousel module contains multiple content block items.</span></span>

![Пример модуля карусели](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="535e0-117">Свойства модуля карусели</span><span class="sxs-lookup"><span data-stu-id="535e0-117">Carousel module properties</span></span>

| <span data-ttu-id="535e0-118">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="535e0-118">Property name</span></span>             | <span data-ttu-id="535e0-119">значение</span><span class="sxs-lookup"><span data-stu-id="535e0-119">Value</span></span>                 | <span data-ttu-id="535e0-120">описание</span><span class="sxs-lookup"><span data-stu-id="535e0-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="535e0-121">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="535e0-121">Autoplay</span></span>                  | <span data-ttu-id="535e0-122">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="535e0-122">**True** or **False**</span></span> | <span data-ttu-id="535e0-123">Если установлено значение **True**, переход между элементами в карусели происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="535e0-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="535e0-124">Если установлено значение **False**, переход будет выполняться только в том случае, если клиент использует клавиатуру или мышь для перемещения от одного элемента к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="535e0-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="535e0-125">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="535e0-125">Slide transition interval</span></span> | <span data-ttu-id="535e0-126">Значение в секундах</span><span class="sxs-lookup"><span data-stu-id="535e0-126">A value in seconds</span></span>    | <span data-ttu-id="535e0-127">Интервал для переходов между элементами.</span><span class="sxs-lookup"><span data-stu-id="535e0-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="535e0-128">Тип перехода</span><span class="sxs-lookup"><span data-stu-id="535e0-128">Transition type</span></span>           | <span data-ttu-id="535e0-129">**Сдвиг** или **Исчезание**</span><span class="sxs-lookup"><span data-stu-id="535e0-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="535e0-130">Эффект перехода между элементами.</span><span class="sxs-lookup"><span data-stu-id="535e0-130">The transition effect between items.</span></span> |
| <span data-ttu-id="535e0-131">Скрыть флиппер карусели</span><span class="sxs-lookup"><span data-stu-id="535e0-131">Hide carousel flipper</span></span>     | <span data-ttu-id="535e0-132">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="535e0-132">**True** or **False**</span></span> | <span data-ttu-id="535e0-133">Если значение задано как **True**, флиппер карусели и индикатор последовательности скрыты.</span><span class="sxs-lookup"><span data-stu-id="535e0-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="535e0-134">Разрешить отклонить карусель</span><span class="sxs-lookup"><span data-stu-id="535e0-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="535e0-135">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="535e0-135">**True** or **False**</span></span> | <span data-ttu-id="535e0-136">Если установлено значение **True**, пользовали могут отменить карусель.</span><span class="sxs-lookup"><span data-stu-id="535e0-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="535e0-137">Добавление модуля карусели на страницу</span><span class="sxs-lookup"><span data-stu-id="535e0-137">Add a carousel module to a page</span></span>

<span data-ttu-id="535e0-138">Чтобы добавить модуль карусели на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="535e0-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="535e0-139">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="535e0-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="535e0-140">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон карусели**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="535e0-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="535e0-141">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="535e0-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="535e0-142">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="535e0-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="535e0-143">Используйте только что созданный шаблон карусели для создания страницы с именем **Страница карусели**.</span><span class="sxs-lookup"><span data-stu-id="535e0-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="535e0-144">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="535e0-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="535e0-145">В области справа задайте значение **Ширина** как **Заполнить экран**.</span><span class="sxs-lookup"><span data-stu-id="535e0-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="535e0-146">В области **Структура страницы** добавьте модуль карусели в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="535e0-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="535e0-147">Добавьте модуль блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="535e0-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="535e0-148">Задайте свойства модуля блока содержимого, задав **Заголовок**, **Ссылка**, **Макет** и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="535e0-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="535e0-149">Добавьте и настройте другой модуль блока содержимого.</span><span class="sxs-lookup"><span data-stu-id="535e0-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="535e0-150">Настройте дополнительные свойства модуля карусели по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="535e0-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="535e0-151">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="535e0-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="535e0-152">На странице должна отображаться карусель с двумя модулями внутри (модуль главного имиджевого баннера и модуль компонента).</span><span class="sxs-lookup"><span data-stu-id="535e0-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="535e0-153">Для получения нужного эффекта можно изменить дополнительные свойства модулей карусели, главного имиджевого баннера и компонента.</span><span class="sxs-lookup"><span data-stu-id="535e0-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="535e0-154">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="535e0-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="535e0-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="535e0-155">Additional resources</span></span>

[<span data-ttu-id="535e0-156">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="535e0-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="535e0-157">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="535e0-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="535e0-158">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="535e0-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="535e0-159">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="535e0-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="535e0-160">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="535e0-160">Video player module</span></span>](add-video-player.md)
