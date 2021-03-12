---
title: Модуль рекламного баннера
description: В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: a77196be69bb71d917bf84c633199a3af3fbf478
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986037"
---
# <a name="promo-banner-module"></a><span data-ttu-id="345aa-103">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="345aa-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="345aa-104">В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="345aa-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="345aa-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="345aa-105">Overview</span></span>

<span data-ttu-id="345aa-106">Модули рекламного баннера используются для отображения на странице встроенных информационных сообщений.</span><span class="sxs-lookup"><span data-stu-id="345aa-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="345aa-107">Они могут использоваться для отображения рекламных акций на уровне всего сайта, которые появляются на всех страницах сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="345aa-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="345aa-108">Модули рекламного баннера поддерживают текстовое сообщение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="345aa-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="345aa-109">Если в модуль рекламного баннера добавлены несколько сообщений, они становятся вращающимися баннерами, которые позволяют клиентам циклически переключаться между всеми сообщениями.</span><span class="sxs-lookup"><span data-stu-id="345aa-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="345aa-110">Модули рекламного баннера управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="345aa-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="345aa-111">Примеры использования рекламных баннеров в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="345aa-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="345aa-112">Рекламные баннеры можно использовать в заголовке сайта, чтобы показать рекламные акции или сообщения на уровне сайта, как в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="345aa-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="345aa-113">"Ежегодная распродажа заканчивается через 10 дней"</span><span class="sxs-lookup"><span data-stu-id="345aa-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="345aa-114">"Большая экономия на распродаже в связи с началом учебного года.</span><span class="sxs-lookup"><span data-stu-id="345aa-114">"Save big with back to school sale.</span></span> <span data-ttu-id="345aa-115">Покупайте сейчас."</span><span class="sxs-lookup"><span data-stu-id="345aa-115">Shop Now."</span></span>

<span data-ttu-id="345aa-116">"Магазин для РАСПРОДАЖИ на День благодарения!"</span><span class="sxs-lookup"><span data-stu-id="345aa-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="345aa-117">На следующем рисунке показан пример рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="345aa-117">The following image shows an example of a promo banner.</span></span>

![Пример модуля рекламного баннера](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="345aa-119">Свойства модуля рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="345aa-119">Promo banner module properties</span></span>

| <span data-ttu-id="345aa-120">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="345aa-120">Property name</span></span>             | <span data-ttu-id="345aa-121">значение</span><span class="sxs-lookup"><span data-stu-id="345aa-121">Value</span></span>                              | <span data-ttu-id="345aa-122">описание</span><span class="sxs-lookup"><span data-stu-id="345aa-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="345aa-123">Сообщения баннера</span><span class="sxs-lookup"><span data-stu-id="345aa-123">Banner messages</span></span>           | <span data-ttu-id="345aa-124">Текст и ссылки</span><span class="sxs-lookup"><span data-stu-id="345aa-124">Text and links</span></span>                     | <span data-ttu-id="345aa-125">Массив текста и ссылок.</span><span class="sxs-lookup"><span data-stu-id="345aa-125">An array of text and links.</span></span> |
| <span data-ttu-id="345aa-126">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="345aa-126">Autoplay</span></span>                  | <span data-ttu-id="345aa-127">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="345aa-127">**True** or **False**</span></span>              | <span data-ttu-id="345aa-128">Значение, указывающее, будут ли сообщения автоматически циклически переключаться, если настроено несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="345aa-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="345aa-129">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="345aa-129">Slide transition interval</span></span> | <span data-ttu-id="345aa-130">Число миллисекунд (мс)</span><span class="sxs-lookup"><span data-stu-id="345aa-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="345aa-131">Интервал, используемый для циклического переключения между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="345aa-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="345aa-132">Разрешить закрытие</span><span class="sxs-lookup"><span data-stu-id="345aa-132">Allow dismiss</span></span>             | <span data-ttu-id="345aa-133">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="345aa-133">**True** or **False**</span></span>              | <span data-ttu-id="345aa-134">Если установлено значение **True**, клиент может закрыть оповещение.</span><span class="sxs-lookup"><span data-stu-id="345aa-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="345aa-135">Показать карусельный флиппер</span><span class="sxs-lookup"><span data-stu-id="345aa-135">Show carousel flipper</span></span>     | <span data-ttu-id="345aa-136">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="345aa-136">**True** or **False**</span></span>              | <span data-ttu-id="345aa-137">Значение, указывающее, следует ли показывать карусельные флипперы, чтобы клиенты могли вручную циклически переключать несколько элементов баннеров.</span><span class="sxs-lookup"><span data-stu-id="345aa-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="345aa-138">Выравнивание текста</span><span class="sxs-lookup"><span data-stu-id="345aa-138">Text alignment</span></span>            | <span data-ttu-id="345aa-139">**По правому краю**, **По левому краю** или **По центру**</span><span class="sxs-lookup"><span data-stu-id="345aa-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="345aa-140">Выравнивание текста в модуле рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="345aa-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="345aa-141">Ссылка</span><span class="sxs-lookup"><span data-stu-id="345aa-141">Link</span></span>                      | <span data-ttu-id="345aa-142">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="345aa-142">A URL</span></span>                              | <span data-ttu-id="345aa-143">URL-адрес для необязательной ссылки.</span><span class="sxs-lookup"><span data-stu-id="345aa-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="345aa-144">Добавление модуля рекламного баннера на страницу</span><span class="sxs-lookup"><span data-stu-id="345aa-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="345aa-145">Чтобы добавить модуль рекламного баннера на страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="345aa-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="345aa-146">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="345aa-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="345aa-147">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон рекламного баннера**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="345aa-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="345aa-148">В разделе **Структура страницы** добавьте модуль **Страница по умолчанию** в слот **Содержание**.</span><span class="sxs-lookup"><span data-stu-id="345aa-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="345aa-149">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="345aa-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="345aa-150">Используйте только что созданный шаблон для создания страницы с именем **страница рекламного баннера**.</span><span class="sxs-lookup"><span data-stu-id="345aa-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="345aa-151">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="345aa-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="345aa-152">В области справа задайте значение **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="345aa-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="345aa-153">В области **Структура страницы** добавьте модуль рекламного баннера в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="345aa-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="345aa-154">В настройках модуля баннера добавьте одно или несколько сообщений баннера.</span><span class="sxs-lookup"><span data-stu-id="345aa-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="345aa-155">У каждого сообщения может быть текст вместе со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="345aa-155">Each message can have text together with a link.</span></span> <span data-ttu-id="345aa-156">Если требуется дополнительно настроить модуль, можно изменить другие свойства.</span><span class="sxs-lookup"><span data-stu-id="345aa-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="345aa-157">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="345aa-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="345aa-158">В верхней части страницы должно отобразиться оповещение с добавленным текстом.</span><span class="sxs-lookup"><span data-stu-id="345aa-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="345aa-159">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="345aa-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="345aa-160">Рекламный баннер обычно используется в слоте заголовков страницы или слоте подзаголовка.</span><span class="sxs-lookup"><span data-stu-id="345aa-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="345aa-161">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="345aa-161">Additional resources</span></span>

[<span data-ttu-id="345aa-162">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="345aa-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="345aa-163">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="345aa-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="345aa-164">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="345aa-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="345aa-165">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="345aa-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="345aa-166">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="345aa-166">Video player module</span></span>](add-video-player.md)
