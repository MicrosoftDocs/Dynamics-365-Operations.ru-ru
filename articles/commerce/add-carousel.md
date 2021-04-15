---
title: Модуль карусели
description: В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797895"
---
# <a name="carousel-module"></a><span data-ttu-id="5a300-103">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="5a300-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a300-104">В этом разделе описываются модули карусели, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a300-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5a300-105">Модуль карусели используется для помещения во вращающийся карусельный баннер нескольких рекламных элементов (включая форматированные изображения), которые могут просматривать клиенты.</span><span class="sxs-lookup"><span data-stu-id="5a300-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="5a300-106">Например, розничный продавец может использовать модуль карусели на домашней странице для демонстрации нескольких новых продуктов или рекламных акций.</span><span class="sxs-lookup"><span data-stu-id="5a300-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="5a300-107">Можно добавлять модули блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="5a300-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="5a300-108">Затем свойства модуля карусели определяют способ отображения этих модулей.</span><span class="sxs-lookup"><span data-stu-id="5a300-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="5a300-109">Примеры модулей карусели в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="5a300-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="5a300-110">На домашней странице можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="5a300-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="5a300-111">На странице сведений о продукте можно использовать карусель, в которой есть несколько рекламных модулей.</span><span class="sxs-lookup"><span data-stu-id="5a300-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="5a300-112">Карусель может использоваться на любой странице маркетинга для продвижения нескольких рекламных акций или продуктов.</span><span class="sxs-lookup"><span data-stu-id="5a300-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="5a300-113">На следующем рисунке показан пример модуля карусели, используемый на главной странице.</span><span class="sxs-lookup"><span data-stu-id="5a300-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="5a300-114">Этот модуль карусели содержит несколько элементов блоков содержимого.</span><span class="sxs-lookup"><span data-stu-id="5a300-114">This carousel module contains multiple content block items.</span></span>

![Пример модуля карусели](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="5a300-116">Свойства модуля карусели</span><span class="sxs-lookup"><span data-stu-id="5a300-116">Carousel module properties</span></span>

| <span data-ttu-id="5a300-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="5a300-117">Property name</span></span>             | <span data-ttu-id="5a300-118">значение</span><span class="sxs-lookup"><span data-stu-id="5a300-118">Value</span></span>                 | <span data-ttu-id="5a300-119">описание</span><span class="sxs-lookup"><span data-stu-id="5a300-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5a300-120">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="5a300-120">Autoplay</span></span>                  | <span data-ttu-id="5a300-121">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5a300-121">**True** or **False**</span></span> | <span data-ttu-id="5a300-122">Если установлено значение **True**, переход между элементами в карусели происходит автоматически.</span><span class="sxs-lookup"><span data-stu-id="5a300-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="5a300-123">Если установлено значение **False**, переход будет выполняться только в том случае, если клиент использует клавиатуру или мышь для перемещения от одного элемента к другому элементу.</span><span class="sxs-lookup"><span data-stu-id="5a300-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="5a300-124">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="5a300-124">Slide transition interval</span></span> | <span data-ttu-id="5a300-125">Значение в секундах</span><span class="sxs-lookup"><span data-stu-id="5a300-125">A value in seconds</span></span>    | <span data-ttu-id="5a300-126">Интервал для переходов между элементами.</span><span class="sxs-lookup"><span data-stu-id="5a300-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="5a300-127">Тип перехода</span><span class="sxs-lookup"><span data-stu-id="5a300-127">Transition type</span></span>           | <span data-ttu-id="5a300-128">**Сдвиг** или **Исчезание**</span><span class="sxs-lookup"><span data-stu-id="5a300-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="5a300-129">Эффект перехода между элементами.</span><span class="sxs-lookup"><span data-stu-id="5a300-129">The transition effect between items.</span></span> |
| <span data-ttu-id="5a300-130">Скрыть флиппер карусели</span><span class="sxs-lookup"><span data-stu-id="5a300-130">Hide carousel flipper</span></span>     | <span data-ttu-id="5a300-131">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5a300-131">**True** or **False**</span></span> | <span data-ttu-id="5a300-132">Если значение задано как **True**, флиппер карусели и индикатор последовательности скрыты.</span><span class="sxs-lookup"><span data-stu-id="5a300-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="5a300-133">Разрешить отклонить карусель</span><span class="sxs-lookup"><span data-stu-id="5a300-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="5a300-134">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="5a300-134">**True** or **False**</span></span> | <span data-ttu-id="5a300-135">Если установлено значение **True**, пользовали могут отменить карусель.</span><span class="sxs-lookup"><span data-stu-id="5a300-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="5a300-136">Добавление модуля карусели на страницу</span><span class="sxs-lookup"><span data-stu-id="5a300-136">Add a carousel module to a page</span></span>

<span data-ttu-id="5a300-137">Чтобы добавить модуль карусели на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5a300-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5a300-138">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="5a300-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="5a300-139">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон карусели**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5a300-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="5a300-140">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="5a300-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="5a300-141">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="5a300-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="5a300-142">Используйте только что созданный шаблон карусели для создания страницы с именем **Страница карусели**.</span><span class="sxs-lookup"><span data-stu-id="5a300-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="5a300-143">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="5a300-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="5a300-144">В области справа задайте значение **Ширина** как **Заполнить экран**.</span><span class="sxs-lookup"><span data-stu-id="5a300-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="5a300-145">В области **Структура страницы** добавьте модуль карусели в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="5a300-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="5a300-146">Добавьте модуль блока содержимого в модуль карусели.</span><span class="sxs-lookup"><span data-stu-id="5a300-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="5a300-147">Задайте свойства модуля блока содержимого, задав **Заголовок**, **Ссылка**, **Макет** и другие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a300-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="5a300-148">Добавьте и настройте другой модуль блока содержимого.</span><span class="sxs-lookup"><span data-stu-id="5a300-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="5a300-149">Настройте дополнительные свойства модуля карусели по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5a300-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="5a300-150">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="5a300-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="5a300-151">На странице должна отображаться карусель с двумя модулями внутри (модуль главного имиджевого баннера и модуль компонента).</span><span class="sxs-lookup"><span data-stu-id="5a300-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="5a300-152">Для получения нужного эффекта можно изменить дополнительные свойства модулей карусели, главного имиджевого баннера и компонента.</span><span class="sxs-lookup"><span data-stu-id="5a300-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="5a300-153">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="5a300-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a300-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5a300-154">Additional resources</span></span>

[<span data-ttu-id="5a300-155">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="5a300-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5a300-156">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="5a300-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5a300-157">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="5a300-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="5a300-158">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="5a300-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="5a300-159">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="5a300-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]