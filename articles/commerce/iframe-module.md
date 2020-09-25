---
title: Модуль iFrame
description: В этом разделе описывается модуль iFrame, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647031"
---
# <a name="iframe-module"></a><span data-ttu-id="1e9f5-103">Модуль iFrame</span><span class="sxs-lookup"><span data-stu-id="1e9f5-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1e9f5-104">В этом разделе описывается модуль iFrame, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1e9f5-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="1e9f5-105">Overview</span></span>

<span data-ttu-id="1e9f5-106">Модуль iFrame предоставляет iFrame (встраиваемый кадр), который содержит внешнее содержимое на сайте.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="1e9f5-107">Например, его можно использовать для размещения видео YouTube или средства просмотра PDF-файлов на любой странице сайта.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="1e9f5-108">Для модуля iFrame требуется целевой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="1e9f5-109">Затем содержимое целевой страницы размещается в HTML-элементе **iFrame**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="1e9f5-110">Внешние URL-адреса должны быть включены в список разрешенных (называемый также "разрешенным списком") в соответствии с директивами политики безопасности содержимого (CSP) сайта.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="1e9f5-111">Для содержимого iFrame URL-адреса должны быть разрешены с помощью директивы **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="1e9f5-112">Дополнительные сведения см. в разделе [Управление политикой безопасности содержимого (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="1e9f5-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="1e9f5-113">На следующем изображении показаны примеры модулей iFrame, демонстрирующих отображение внешних видеозаписей на страницах сайта.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Пример модулей iFrame, демонстрирующих внешние видеозаписи](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="1e9f5-115">Свойства модуля iFrame</span><span class="sxs-lookup"><span data-stu-id="1e9f5-115">Iframe module properties</span></span>

| <span data-ttu-id="1e9f5-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="1e9f5-116">Property name</span></span>             | <span data-ttu-id="1e9f5-117">значение</span><span class="sxs-lookup"><span data-stu-id="1e9f5-117">Value</span></span>                 | <span data-ttu-id="1e9f5-118">описание</span><span class="sxs-lookup"><span data-stu-id="1e9f5-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="1e9f5-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e9f5-119">Heading</span></span> | <span data-ttu-id="1e9f5-120">Текст</span><span class="sxs-lookup"><span data-stu-id="1e9f5-120">Text</span></span> | <span data-ttu-id="1e9f5-121">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-121">The heading for the module.</span></span> |
| <span data-ttu-id="1e9f5-122">Целевой URL-адрес</span><span class="sxs-lookup"><span data-stu-id="1e9f5-122">Target URL</span></span> | <span data-ttu-id="1e9f5-123">URL</span><span class="sxs-lookup"><span data-stu-id="1e9f5-123">URL</span></span> | <span data-ttu-id="1e9f5-124">URL-адрес, размещенный в модуле.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="1e9f5-125">Высота</span><span class="sxs-lookup"><span data-stu-id="1e9f5-125">Height</span></span> | <span data-ttu-id="1e9f5-126">Число или процент</span><span class="sxs-lookup"><span data-stu-id="1e9f5-126">Number or percentage</span></span> | <span data-ttu-id="1e9f5-127">Высота модуля в точках или в процентах.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="1e9f5-128">Например, значение **100** будет обрабатываться как число пикселей, а значение **100%** будет обработано как процент.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="1e9f5-129">Метка Aria</span><span class="sxs-lookup"><span data-stu-id="1e9f5-129">Aria label</span></span> | <span data-ttu-id="1e9f5-130">Текст</span><span class="sxs-lookup"><span data-stu-id="1e9f5-130">Text</span></span> | <span data-ttu-id="1e9f5-131">Для обеспечения специальных возможностей можно задать метку доступных полнофункциональных интернет-приложений (ARIA).</span><span class="sxs-lookup"><span data-stu-id="1e9f5-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="1e9f5-132">Добавление модуля iFrame на страницу</span><span class="sxs-lookup"><span data-stu-id="1e9f5-132">Add an iframe module to a page</span></span>

<span data-ttu-id="1e9f5-133">Чтобы добавить модуль iFrame на страницу для отображения внешнего видео, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="1e9f5-134">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1e9f5-135">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон маркетинга**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e9f5-136">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1e9f5-137">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="1e9f5-138">В диалоговом окне **Выбор шаблона** выберите **Шаблон маркетинга**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="1e9f5-139">В поле **Имя страницы** введите **Страница маркетинга**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e9f5-140">В слоте **Главный** новой страницы выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e9f5-141">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1e9f5-142">В области свойства модуля установите значение **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="1e9f5-143">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e9f5-144">В диалоговом окне **Добавить модуль** выберите модуль **iFrame**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1e9f5-145">В области свойства модуля задайте значение **Целевой URL-адрес** для внешнего URL-адреса видео.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="1e9f5-146">Задайте другие свойства, такие как **Заголовок** и **Высота**, как требуется.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="1e9f5-147">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1e9f5-148">Перейдите на страницу маркетинга на своем сайте.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="1e9f5-149">Вы увидите, что видео отображается в модуле iFrame.</span><span class="sxs-lookup"><span data-stu-id="1e9f5-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="1e9f5-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e9f5-150">Additional resources</span></span>

[<span data-ttu-id="1e9f5-151">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="1e9f5-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1e9f5-152">Управление политикой безопасности содержимого (CSP)</span><span class="sxs-lookup"><span data-stu-id="1e9f5-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)