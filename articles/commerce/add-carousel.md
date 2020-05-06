---
title: Модуль карусели
description: В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269736"
---
# <a name="carousel-module"></a><span data-ttu-id="682d8-103">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="682d8-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="682d8-104">В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="682d8-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="682d8-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="682d8-105">Overview</span></span>

<span data-ttu-id="682d8-106">Модуль карусели используется для помещения во вращающийся карусельный баннер нескольких рекламных элементов (включая форматированные изображения), которые могут просматривать клиенты.</span><span class="sxs-lookup"><span data-stu-id="682d8-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="682d8-107">Например, розничный продавец может использовать модуль карусели на домашней странице для демонстрации нескольких новых продуктов или рекламных акций.</span><span class="sxs-lookup"><span data-stu-id="682d8-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="682d8-108">Можно добавлять модули блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="682d8-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="682d8-109">Затем свойства модуля карусели определяют способ отображения этих модулей.</span><span class="sxs-lookup"><span data-stu-id="682d8-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="682d8-110">Примеры модулей карусели в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="682d8-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="682d8-111">На домашней странице можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="682d8-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="682d8-112">На странице сведений о продукте можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="682d8-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="682d8-113">Карусель может использоваться на любой странице маркетинга для продвижения нескольких рекламных акций или продуктов.</span><span class="sxs-lookup"><span data-stu-id="682d8-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="682d8-114">Свойства модуля карусели</span><span class="sxs-lookup"><span data-stu-id="682d8-114">Carousel module properties</span></span>

| <span data-ttu-id="682d8-115">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="682d8-115">Property name</span></span>             | <span data-ttu-id="682d8-116">Стоимость</span><span class="sxs-lookup"><span data-stu-id="682d8-116">Value</span></span>                 | <span data-ttu-id="682d8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="682d8-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="682d8-118">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="682d8-118">Autoplay</span></span>                  | <span data-ttu-id="682d8-119">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="682d8-119">**True** or **False**</span></span> | <span data-ttu-id="682d8-120">Если установлено значение **True**, переход между элементами в карусели происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="682d8-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="682d8-121">Если установлено значение **False**, переход будет выполняться только в том случае, если клиент использует клавиатуру или мышь для перемещения от одного элемента к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="682d8-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="682d8-122">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="682d8-122">Slide transition interval</span></span> | <span data-ttu-id="682d8-123">Значение в секундах</span><span class="sxs-lookup"><span data-stu-id="682d8-123">A value in seconds</span></span>    | <span data-ttu-id="682d8-124">Интервал для переходов между элементами.</span><span class="sxs-lookup"><span data-stu-id="682d8-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="682d8-125">Тип перехода</span><span class="sxs-lookup"><span data-stu-id="682d8-125">Transition type</span></span>           | <span data-ttu-id="682d8-126">**Сдвиг** или **Исчезание**</span><span class="sxs-lookup"><span data-stu-id="682d8-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="682d8-127">Эффект перехода между элементами.</span><span class="sxs-lookup"><span data-stu-id="682d8-127">The transition effect between items.</span></span> |
| <span data-ttu-id="682d8-128">Скрыть флиппер карусели</span><span class="sxs-lookup"><span data-stu-id="682d8-128">Hide carousel flipper</span></span>     | <span data-ttu-id="682d8-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="682d8-129">**True** or **False**</span></span> | <span data-ttu-id="682d8-130">Если значение задано как **True**, флиппер карусели и индикатор последовательности скрыты.</span><span class="sxs-lookup"><span data-stu-id="682d8-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="682d8-131">Разрешить отклонить карусель</span><span class="sxs-lookup"><span data-stu-id="682d8-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="682d8-132">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="682d8-132">**True** or **False**</span></span> | <span data-ttu-id="682d8-133">Если установлено значение **True**, пользовали могут отменить карусель.</span><span class="sxs-lookup"><span data-stu-id="682d8-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="682d8-134">Добавление модуля карусели на страницу</span><span class="sxs-lookup"><span data-stu-id="682d8-134">Add a carousel module to a page</span></span>

<span data-ttu-id="682d8-135">Чтобы добавить модуль карусели на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="682d8-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="682d8-136">Выберите **Создать** для создания шаблона страницы.</span><span class="sxs-lookup"><span data-stu-id="682d8-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="682d8-137">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон карусели**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="682d8-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="682d8-138">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="682d8-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="682d8-139">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="682d8-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="682d8-140">Используйте только что созданный шаблон карусели для создания страницы с именем **Страница карусели**.</span><span class="sxs-lookup"><span data-stu-id="682d8-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="682d8-141">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="682d8-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="682d8-142">В области справа задайте значение **Ширина** как **Заполнить экран**.</span><span class="sxs-lookup"><span data-stu-id="682d8-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="682d8-143">В области **Структура страницы** добавьте модуль карусели в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="682d8-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="682d8-144">Добавьте модуль блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="682d8-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="682d8-145">Задайте свойства модуля блока содержимого, задав **Заголовок**, **Ссылка**, **Макет** и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="682d8-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="682d8-146">Добавьте и настройте другой модуль блока содержимого.</span><span class="sxs-lookup"><span data-stu-id="682d8-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="682d8-147">Настройте дополнительные свойства модуля карусели по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="682d8-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="682d8-148">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="682d8-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="682d8-149">На странице должна отображаться карусель с двумя модулями внутри (модуль главного имиджевого баннера и модуль компонента).</span><span class="sxs-lookup"><span data-stu-id="682d8-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="682d8-150">Для получения нужного эффекта можно изменить дополнительные свойства модулей карусели, главного имиджевого баннера и компонента.</span><span class="sxs-lookup"><span data-stu-id="682d8-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="682d8-151">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="682d8-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="682d8-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="682d8-152">Additional resources</span></span>

[<span data-ttu-id="682d8-153">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="682d8-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="682d8-154">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="682d8-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="682d8-155">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="682d8-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="682d8-156">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="682d8-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="682d8-157">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="682d8-157">Video player module</span></span>](add-video-player.md)
