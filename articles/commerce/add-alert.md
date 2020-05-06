---
title: Модуль рекламного баннера
description: В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269782"
---
# <a name="promo-banner-module"></a><span data-ttu-id="72ed7-103">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="72ed7-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72ed7-104">В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72ed7-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="72ed7-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="72ed7-105">Overview</span></span>

<span data-ttu-id="72ed7-106">Модули рекламного баннера используются для отображения на странице встроенных информационных сообщений.</span><span class="sxs-lookup"><span data-stu-id="72ed7-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="72ed7-107">Они могут использоваться для отображения рекламных акций на уровне всего сайта, которые появляются на всех страницах сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="72ed7-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="72ed7-108">Модули рекламного баннера поддерживают текстовое сообщение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="72ed7-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="72ed7-109">Если в модуль рекламного баннера добавлены несколько сообщений, они становятся вращающимися баннерами, которые позволяют клиентам циклически переключаться между всеми сообщениями.</span><span class="sxs-lookup"><span data-stu-id="72ed7-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="72ed7-110">Модули рекламного баннера управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="72ed7-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="72ed7-111">Примеры использования рекламных баннеров в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="72ed7-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="72ed7-112">Рекламные баннеры можно использовать в заголовке сайта, чтобы показать рекламные акции или сообщения на уровне сайта, как в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="72ed7-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="72ed7-113">"Ежегодная распродажа заканчивается через 10 дней"</span><span class="sxs-lookup"><span data-stu-id="72ed7-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="72ed7-114">"Большая экономия на распродаже в связи с началом учебного года.</span><span class="sxs-lookup"><span data-stu-id="72ed7-114">"Save big with back to school sale.</span></span> <span data-ttu-id="72ed7-115">Покупайте сейчас."</span><span class="sxs-lookup"><span data-stu-id="72ed7-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="72ed7-116">Свойства модуля рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="72ed7-116">Promo banner module properties</span></span>

| <span data-ttu-id="72ed7-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="72ed7-117">Property name</span></span>             | <span data-ttu-id="72ed7-118">Value</span><span class="sxs-lookup"><span data-stu-id="72ed7-118">Value</span></span>                              | <span data-ttu-id="72ed7-119">Описание</span><span class="sxs-lookup"><span data-stu-id="72ed7-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="72ed7-120">Сообщения баннера</span><span class="sxs-lookup"><span data-stu-id="72ed7-120">Banner messages</span></span>           | <span data-ttu-id="72ed7-121">Текст и ссылки</span><span class="sxs-lookup"><span data-stu-id="72ed7-121">Text and links</span></span>                     | <span data-ttu-id="72ed7-122">Массив текста и ссылок.</span><span class="sxs-lookup"><span data-stu-id="72ed7-122">An array of text and links.</span></span> |
| <span data-ttu-id="72ed7-123">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="72ed7-123">Autoplay</span></span>                  | <span data-ttu-id="72ed7-124">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="72ed7-124">**True** or **False**</span></span>              | <span data-ttu-id="72ed7-125">Значение, указывающее, будут ли сообщения автоматически циклически переключаться, если настроено несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="72ed7-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="72ed7-126">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="72ed7-126">Slide transition interval</span></span> | <span data-ttu-id="72ed7-127">Число миллисекунд (мс)</span><span class="sxs-lookup"><span data-stu-id="72ed7-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="72ed7-128">Интервал, используемый для циклического переключения между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="72ed7-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="72ed7-129">Разрешить закрытие</span><span class="sxs-lookup"><span data-stu-id="72ed7-129">Allow dismiss</span></span>             | <span data-ttu-id="72ed7-130">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="72ed7-130">**True** or **False**</span></span>              | <span data-ttu-id="72ed7-131">Если установлено значение **True**, клиент может закрыть оповещение.</span><span class="sxs-lookup"><span data-stu-id="72ed7-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="72ed7-132">Показать карусельный флиппер</span><span class="sxs-lookup"><span data-stu-id="72ed7-132">Show carousel flipper</span></span>     | <span data-ttu-id="72ed7-133">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="72ed7-133">**True** or **False**</span></span>              | <span data-ttu-id="72ed7-134">Значение, указывающее, следует ли показывать карусельные флипперы, чтобы клиенты могли вручную циклически переключать несколько элементов баннеров.</span><span class="sxs-lookup"><span data-stu-id="72ed7-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="72ed7-135">Выравнивание текста</span><span class="sxs-lookup"><span data-stu-id="72ed7-135">Text alignment</span></span>            | <span data-ttu-id="72ed7-136">**По правому краю**, **По левому краю** или **По центру**</span><span class="sxs-lookup"><span data-stu-id="72ed7-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="72ed7-137">Выравнивание текста в модуле рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="72ed7-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="72ed7-138">Ссылка</span><span class="sxs-lookup"><span data-stu-id="72ed7-138">Link</span></span>                      | <span data-ttu-id="72ed7-139">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="72ed7-139">A URL</span></span>                              | <span data-ttu-id="72ed7-140">URL-адрес для необязательной ссылки.</span><span class="sxs-lookup"><span data-stu-id="72ed7-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="72ed7-141">Добавление модуля рекламного баннера на страницу</span><span class="sxs-lookup"><span data-stu-id="72ed7-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="72ed7-142">Чтобы добавить модуль рекламного баннера на страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="72ed7-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="72ed7-143">Выберите **Создать** для создания шаблона страницы.</span><span class="sxs-lookup"><span data-stu-id="72ed7-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="72ed7-144">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон рекламного баннера**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="72ed7-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="72ed7-145">В разделе **Структура страницы** добавьте модуль **Страница по умолчанию** в слот **Содержание**.</span><span class="sxs-lookup"><span data-stu-id="72ed7-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="72ed7-146">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="72ed7-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="72ed7-147">Используйте только что созданный шаблон для создания страницы с именем **страница рекламного баннера**.</span><span class="sxs-lookup"><span data-stu-id="72ed7-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="72ed7-148">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="72ed7-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="72ed7-149">В области справа задайте значение **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="72ed7-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="72ed7-150">В области **Структура страницы** добавьте модуль рекламного баннера в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="72ed7-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="72ed7-151">В настройках модуля баннера добавьте одно или несколько сообщений баннера.</span><span class="sxs-lookup"><span data-stu-id="72ed7-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="72ed7-152">У каждого сообщения может быть текст вместе со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="72ed7-152">Each message can have text together with a link.</span></span> <span data-ttu-id="72ed7-153">Если требуется дополнительно настроить модуль, можно изменить другие свойства.</span><span class="sxs-lookup"><span data-stu-id="72ed7-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="72ed7-154">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="72ed7-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="72ed7-155">В верхней части страницы должно отобразиться оповещение с добавленным текстом.</span><span class="sxs-lookup"><span data-stu-id="72ed7-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="72ed7-156">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="72ed7-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="72ed7-157">Рекламный баннер обычно используется в слоте заголовков страницы или слоте подзаголовка.</span><span class="sxs-lookup"><span data-stu-id="72ed7-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="72ed7-158">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72ed7-158">Additional resources</span></span>

[<span data-ttu-id="72ed7-159">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="72ed7-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="72ed7-160">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="72ed7-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="72ed7-161">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="72ed7-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="72ed7-162">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="72ed7-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="72ed7-163">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="72ed7-163">Video player module</span></span>](add-video-player.md)
