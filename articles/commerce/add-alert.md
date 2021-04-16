---
title: Модуль рекламного баннера
description: В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796254"
---
# <a name="promo-banner-module"></a><span data-ttu-id="9fab2-103">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="9fab2-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9fab2-104">В этом разделе описываются модули рекламного баннера, а также описывается, как добавлять их на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9fab2-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9fab2-105">Модули рекламного баннера используются для отображения на странице встроенных информационных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9fab2-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="9fab2-106">Они могут использоваться для отображения рекламных акций на уровне всего сайта, которые появляются на всех страницах сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="9fab2-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="9fab2-107">Модули рекламного баннера поддерживают текстовое сообщение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="9fab2-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="9fab2-108">Если в модуль рекламного баннера добавлены несколько сообщений, они становятся вращающимися баннерами, которые позволяют клиентам циклически переключаться между всеми сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9fab2-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="9fab2-109">Модули рекламного баннера управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="9fab2-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="9fab2-110">Примеры использования рекламных баннеров в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="9fab2-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="9fab2-111">Рекламные баннеры можно использовать в заголовке сайта, чтобы показать рекламные акции или сообщения на уровне сайта, как в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="9fab2-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="9fab2-112">"Ежегодная распродажа заканчивается через 10 дней"</span><span class="sxs-lookup"><span data-stu-id="9fab2-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="9fab2-113">"Большая экономия на распродаже в связи с началом учебного года.</span><span class="sxs-lookup"><span data-stu-id="9fab2-113">"Save big with back to school sale.</span></span> <span data-ttu-id="9fab2-114">Покупайте сейчас."</span><span class="sxs-lookup"><span data-stu-id="9fab2-114">Shop Now."</span></span>

<span data-ttu-id="9fab2-115">"Магазин для РАСПРОДАЖИ на День благодарения!"</span><span class="sxs-lookup"><span data-stu-id="9fab2-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="9fab2-116">На следующем рисунке показан пример рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="9fab2-116">The following image shows an example of a promo banner.</span></span>

![Пример модуля рекламного баннера](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="9fab2-118">Свойства модуля рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="9fab2-118">Promo banner module properties</span></span>

| <span data-ttu-id="9fab2-119">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9fab2-119">Property name</span></span>             | <span data-ttu-id="9fab2-120">значение</span><span class="sxs-lookup"><span data-stu-id="9fab2-120">Value</span></span>                              | <span data-ttu-id="9fab2-121">описание</span><span class="sxs-lookup"><span data-stu-id="9fab2-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="9fab2-122">Сообщения баннера</span><span class="sxs-lookup"><span data-stu-id="9fab2-122">Banner messages</span></span>           | <span data-ttu-id="9fab2-123">Текст и ссылки</span><span class="sxs-lookup"><span data-stu-id="9fab2-123">Text and links</span></span>                     | <span data-ttu-id="9fab2-124">Массив текста и ссылок.</span><span class="sxs-lookup"><span data-stu-id="9fab2-124">An array of text and links.</span></span> |
| <span data-ttu-id="9fab2-125">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="9fab2-125">Autoplay</span></span>                  | <span data-ttu-id="9fab2-126">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="9fab2-126">**True** or **False**</span></span>              | <span data-ttu-id="9fab2-127">Значение, указывающее, будут ли сообщения автоматически циклически переключаться, если настроено несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="9fab2-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="9fab2-128">Интервал смены слайдов</span><span class="sxs-lookup"><span data-stu-id="9fab2-128">Slide transition interval</span></span> | <span data-ttu-id="9fab2-129">Число миллисекунд (мс)</span><span class="sxs-lookup"><span data-stu-id="9fab2-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="9fab2-130">Интервал, используемый для циклического переключения между сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9fab2-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="9fab2-131">Разрешить закрытие</span><span class="sxs-lookup"><span data-stu-id="9fab2-131">Allow dismiss</span></span>             | <span data-ttu-id="9fab2-132">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="9fab2-132">**True** or **False**</span></span>              | <span data-ttu-id="9fab2-133">Если установлено значение **True**, клиент может закрыть оповещение.</span><span class="sxs-lookup"><span data-stu-id="9fab2-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="9fab2-134">Показать карусельный флиппер</span><span class="sxs-lookup"><span data-stu-id="9fab2-134">Show carousel flipper</span></span>     | <span data-ttu-id="9fab2-135">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="9fab2-135">**True** or **False**</span></span>              | <span data-ttu-id="9fab2-136">Значение, указывающее, следует ли показывать карусельные флипперы, чтобы клиенты могли вручную циклически переключать несколько элементов баннеров.</span><span class="sxs-lookup"><span data-stu-id="9fab2-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="9fab2-137">Выравнивание текста</span><span class="sxs-lookup"><span data-stu-id="9fab2-137">Text alignment</span></span>            | <span data-ttu-id="9fab2-138">**По правому краю**, **По левому краю** или **По центру**</span><span class="sxs-lookup"><span data-stu-id="9fab2-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="9fab2-139">Выравнивание текста в модуле рекламного баннера.</span><span class="sxs-lookup"><span data-stu-id="9fab2-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="9fab2-140">Ссылка</span><span class="sxs-lookup"><span data-stu-id="9fab2-140">Link</span></span>                      | <span data-ttu-id="9fab2-141">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9fab2-141">A URL</span></span>                              | <span data-ttu-id="9fab2-142">URL-адрес для необязательной ссылки.</span><span class="sxs-lookup"><span data-stu-id="9fab2-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="9fab2-143">Добавление модуля рекламного баннера на страницу</span><span class="sxs-lookup"><span data-stu-id="9fab2-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="9fab2-144">Чтобы добавить модуль рекламного баннера на страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9fab2-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9fab2-145">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="9fab2-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="9fab2-146">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон рекламного баннера**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9fab2-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9fab2-147">В разделе **Структура страницы** добавьте модуль **Страница по умолчанию** в слот **Содержание**.</span><span class="sxs-lookup"><span data-stu-id="9fab2-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="9fab2-148">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="9fab2-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="9fab2-149">Используйте только что созданный шаблон для создания страницы с именем **страница рекламного баннера**.</span><span class="sxs-lookup"><span data-stu-id="9fab2-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="9fab2-150">В слоте **Главный** новой страницы добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="9fab2-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="9fab2-151">В области справа задайте значение **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="9fab2-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="9fab2-152">В области **Структура страницы** добавьте модуль рекламного баннера в модуль контейнера.</span><span class="sxs-lookup"><span data-stu-id="9fab2-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="9fab2-153">В настройках модуля баннера добавьте одно или несколько сообщений баннера.</span><span class="sxs-lookup"><span data-stu-id="9fab2-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="9fab2-154">У каждого сообщения может быть текст вместе со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="9fab2-154">Each message can have text together with a link.</span></span> <span data-ttu-id="9fab2-155">Если требуется дополнительно настроить модуль, можно изменить другие свойства.</span><span class="sxs-lookup"><span data-stu-id="9fab2-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="9fab2-156">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="9fab2-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9fab2-157">В верхней части страницы должно отобразиться оповещение с добавленным текстом.</span><span class="sxs-lookup"><span data-stu-id="9fab2-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="9fab2-158">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="9fab2-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="9fab2-159">Рекламный баннер обычно используется в слоте заголовков страницы или слоте подзаголовка.</span><span class="sxs-lookup"><span data-stu-id="9fab2-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9fab2-160">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9fab2-160">Additional resources</span></span>

[<span data-ttu-id="9fab2-161">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="9fab2-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9fab2-162">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="9fab2-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="9fab2-163">Модуль текстового блока</span><span class="sxs-lookup"><span data-stu-id="9fab2-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9fab2-164">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="9fab2-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="9fab2-165">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="9fab2-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]