---
title: Модуль компонента
description: В этом разделе описываются модули компонентов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785314"
---
# <a name="feature-module"></a><span data-ttu-id="a0a37-103">Модуль компонента</span><span class="sxs-lookup"><span data-stu-id="a0a37-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a0a37-104">В этом разделе описываются модули компонентов, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a0a37-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a0a37-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="a0a37-105">Overview</span></span>

<span data-ttu-id="a0a37-106">Модуль компонента используется для рекламы продуктов или рекламных акций с помощью комбинации изображений и текста.</span><span class="sxs-lookup"><span data-stu-id="a0a37-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="a0a37-107">Например, розничный продавец может добавить модуль компонента к странице сведений о продукте, чтобы выделить особенности продукта.</span><span class="sxs-lookup"><span data-stu-id="a0a37-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="a0a37-108">Модуль компонента управляется данными из системы управления содержимым (CMS).</span><span class="sxs-lookup"><span data-stu-id="a0a37-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="a0a37-109">Он является самостоятельным модулем, не зависящим от других модулей на странице.</span><span class="sxs-lookup"><span data-stu-id="a0a37-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="a0a37-110">Модуль компонента может быть размещен на любой странице сайта, где розничная сеть хочет выполнить маркетинг или рекламировать что-либо (например, продукты, продажи или особенности).</span><span class="sxs-lookup"><span data-stu-id="a0a37-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="a0a37-111">Примеры модулей компонентов в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="a0a37-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="a0a37-112">Модуль компонента может использоваться на следующих страницах:</span><span class="sxs-lookup"><span data-stu-id="a0a37-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="a0a37-113">Страница сведения о продукте для демонстрации особенностей продукта</span><span class="sxs-lookup"><span data-stu-id="a0a37-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="a0a37-114">Домашняя страница, чтобы рекламировать продукты</span><span class="sxs-lookup"><span data-stu-id="a0a37-114">The home page, to promote products</span></span>
- <span data-ttu-id="a0a37-115">Страница категории, чтобы выделить категорию продуктов</span><span class="sxs-lookup"><span data-stu-id="a0a37-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="a0a37-116">Свойства модуля компонента</span><span class="sxs-lookup"><span data-stu-id="a0a37-116">Feature module properties</span></span>

| <span data-ttu-id="a0a37-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="a0a37-117">Property name</span></span>     | <span data-ttu-id="a0a37-118">Значения</span><span class="sxs-lookup"><span data-stu-id="a0a37-118">Values</span></span> | <span data-ttu-id="a0a37-119">Описание</span><span class="sxs-lookup"><span data-stu-id="a0a37-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="a0a37-120">Изображение</span><span class="sxs-lookup"><span data-stu-id="a0a37-120">Image</span></span>             | <span data-ttu-id="a0a37-121">Файл изображения</span><span class="sxs-lookup"><span data-stu-id="a0a37-121">Image file</span></span> | <span data-ttu-id="a0a37-122">Изображение может использоваться для продвижения продукта или акции.</span><span class="sxs-lookup"><span data-stu-id="a0a37-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="a0a37-123">Можно отправить изображение в коллекцию изображений или использовать существующее изображение.</span><span class="sxs-lookup"><span data-stu-id="a0a37-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="a0a37-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a0a37-124">Heading</span></span>           | <span data-ttu-id="a0a37-125">Текст заголовка и метка заголовка (**H1**, **H2**, **H3**, **H4**, **H5** или **H6**)</span><span class="sxs-lookup"><span data-stu-id="a0a37-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a0a37-126">Каждый модуль компонента может иметь заголовок.</span><span class="sxs-lookup"><span data-stu-id="a0a37-126">Every feature module can have a heading.</span></span> <span data-ttu-id="a0a37-127">По умолчанию для заголовка используется тег заголовков **H2**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a0a37-128">Однако тег можно изменить для соответствия требованиям к специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="a0a37-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a0a37-129">Абзац</span><span class="sxs-lookup"><span data-stu-id="a0a37-129">Paragraph</span></span>         | <span data-ttu-id="a0a37-130">Текст абзаца</span><span class="sxs-lookup"><span data-stu-id="a0a37-130">Paragraph text</span></span> | <span data-ttu-id="a0a37-131">Модули компонентов поддерживают текст абзаца в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="a0a37-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="a0a37-132">Поддерживаются некоторые основные возможности форматированного текста, такие как жирный шрифт, подчеркнутый текст, курсив и гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="a0a37-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="a0a37-133">Некоторые из этих возможностей могут быть переопределены темой страницы, применяемой к модулю.</span><span class="sxs-lookup"><span data-stu-id="a0a37-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="a0a37-134">Ссылка</span><span class="sxs-lookup"><span data-stu-id="a0a37-134">Link</span></span>              | <span data-ttu-id="a0a37-135">Текст ссылки, URL-адрес ссылки, метка доступных полнофункциональных интернет-приложений (ARIA) и **Открыть ссылку в новой вкладке**</span><span class="sxs-lookup"><span data-stu-id="a0a37-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="a0a37-136">Модули компонентов поддерживают одну или несколько ссылок "призыва к действию".</span><span class="sxs-lookup"><span data-stu-id="a0a37-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="a0a37-137">При добавлении ссылки требуются текст ссылки, URL-адрес и метка ARIA.</span><span class="sxs-lookup"><span data-stu-id="a0a37-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="a0a37-138">Метки ARIA должны быть описательными для соответствия требованиям специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="a0a37-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="a0a37-139">Ссылки можно настроить таким образом, чтобы они открывались на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="a0a37-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="a0a37-140">Размещение изображения</span><span class="sxs-lookup"><span data-stu-id="a0a37-140">Image placement</span></span>   | <span data-ttu-id="a0a37-141">**Справа**, **Слева**, **Сверху** или **Снизу**</span><span class="sxs-lookup"><span data-stu-id="a0a37-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="a0a37-142">Это свойство определяет положение изображения относительно текста.</span><span class="sxs-lookup"><span data-stu-id="a0a37-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="a0a37-143">Например, если выбрано значение **Справа**, изображение отображается справа от текста.</span><span class="sxs-lookup"><span data-stu-id="a0a37-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="a0a37-144">Размер столбца изображения</span><span class="sxs-lookup"><span data-stu-id="a0a37-144">Image column size</span></span> | <span data-ttu-id="a0a37-145">Значение от **1** до **12**</span><span class="sxs-lookup"><span data-stu-id="a0a37-145">A value from **1** through **12**</span></span> | <span data-ttu-id="a0a37-146">Это свойство определяет размер изображения относительно текста.</span><span class="sxs-lookup"><span data-stu-id="a0a37-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="a0a37-147">Размер выражается как число столбцов на странице.</span><span class="sxs-lookup"><span data-stu-id="a0a37-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="a0a37-148">На странице имеется 12 столбцов.</span><span class="sxs-lookup"><span data-stu-id="a0a37-148">There are 12 columns on a page.</span></span> <span data-ttu-id="a0a37-149">По умолчанию изображение и текст имеют одинаковый размер (по шесть столбцов каждый).</span><span class="sxs-lookup"><span data-stu-id="a0a37-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="a0a37-150">Однако при необходимости размер можно скорректировать.</span><span class="sxs-lookup"><span data-stu-id="a0a37-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="a0a37-151">Добавление модуля компонента на новую страницу</span><span class="sxs-lookup"><span data-stu-id="a0a37-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="a0a37-152">Чтобы добавить модуль компонента на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0a37-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a0a37-153">Перейдите к пункту **Шаблоны** и создайте шаблон страницы с именем **Шаблон компонента**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="a0a37-154">В слоте **Главный** страницы по умолчанию добавьте модуль компонента.</span><span class="sxs-lookup"><span data-stu-id="a0a37-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="a0a37-155">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="a0a37-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="a0a37-156">Используйте только что созданный шаблон компонента для создания страницы с именем **страница компонента**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="a0a37-157">В слоте **Главный** страницы по умолчанию выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a0a37-158">В диалоговом окне **Добавление модуля** в списке **Выберите модули** выберите модуль компонента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="a0a37-159">В структуре дерева слева выберите модуль компонента.</span><span class="sxs-lookup"><span data-stu-id="a0a37-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="a0a37-160">В области свойств справа выберите **Добавить изображение**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="a0a37-161">Затем выберите существующее изображение или отправьте новое изображение.</span><span class="sxs-lookup"><span data-stu-id="a0a37-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="a0a37-162">Выберите **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-162">Select **Heading**.</span></span>
1. <span data-ttu-id="a0a37-163">В диалоговом окне **Заголовок** добавьте текст заголовка, выберите уровень заголовка, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="a0a37-164">В разделе **Форматированный текст** добавьте нужный текст.</span><span class="sxs-lookup"><span data-stu-id="a0a37-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="a0a37-165">Выберите **Добавить ссылку действия**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="a0a37-166">В диалоговом окне **Ссылка действия** добавьте текст ссылки, URL-адрес ссылки и метку ARIA для ссылки, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0a37-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="a0a37-167">Сохраните страницу и просмотрите изменения.</span><span class="sxs-lookup"><span data-stu-id="a0a37-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="a0a37-168">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="a0a37-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0a37-169">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0a37-169">Additional resources</span></span>

[<span data-ttu-id="a0a37-170">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="a0a37-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a0a37-171">Модуль оповещения</span><span class="sxs-lookup"><span data-stu-id="a0a37-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="a0a37-172">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="a0a37-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a0a37-173">Модуль блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="a0a37-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a0a37-174">Модуль размещения содержимого</span><span class="sxs-lookup"><span data-stu-id="a0a37-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="a0a37-175">Модуль главного имиджевого баннера</span><span class="sxs-lookup"><span data-stu-id="a0a37-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="a0a37-176">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="a0a37-176">Video player module</span></span>](add-video-player.md)
