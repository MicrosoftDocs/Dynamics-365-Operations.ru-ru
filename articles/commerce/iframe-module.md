---
title: Модуль iFrame
description: В этом разделе описывается модуль iFrame, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993377"
---
# <a name="iframe-module"></a><span data-ttu-id="2cac6-103">Модуль iFrame</span><span class="sxs-lookup"><span data-stu-id="2cac6-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2cac6-104">В этом разделе описывается модуль iFrame, а также описывается, как добавить его на страницы сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2cac6-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2cac6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2cac6-105">Overview</span></span>

<span data-ttu-id="2cac6-106">Модуль iFrame предоставляет iFrame (встраиваемый кадр), который содержит внешнее содержимое на сайте.</span><span class="sxs-lookup"><span data-stu-id="2cac6-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="2cac6-107">Например, его можно использовать для размещения видео YouTube или средства просмотра PDF-файлов на любой странице сайта.</span><span class="sxs-lookup"><span data-stu-id="2cac6-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="2cac6-108">Для модуля iFrame требуется целевой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2cac6-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="2cac6-109">Затем содержимое целевой страницы размещается в HTML-элементе **iFrame**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="2cac6-110">Внешние URL-адреса должны быть включены в список разрешенных в соответствии с директивами политики безопасности содержимого (CSP) сайта.</span><span class="sxs-lookup"><span data-stu-id="2cac6-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="2cac6-111">Для содержимого iFrame URL-адреса должны быть разрешены с помощью директивы **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="2cac6-112">Дополнительные сведения см. в разделе [Управление политикой безопасности содержимого (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="2cac6-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2cac6-113">Модуль iFrame доступен в выпуске Dynamics 365 Commerce 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="2cac6-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="2cac6-114">На следующем изображении показаны примеры модулей iFrame, демонстрирующих отображение внешних видеозаписей на страницах сайта.</span><span class="sxs-lookup"><span data-stu-id="2cac6-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Пример модулей iFrame, демонстрирующих внешние видеозаписи](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="2cac6-116">Свойства модуля iFrame</span><span class="sxs-lookup"><span data-stu-id="2cac6-116">Iframe module properties</span></span>

| <span data-ttu-id="2cac6-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="2cac6-117">Property name</span></span>             | <span data-ttu-id="2cac6-118">значение</span><span class="sxs-lookup"><span data-stu-id="2cac6-118">Value</span></span>                 | <span data-ttu-id="2cac6-119">описание</span><span class="sxs-lookup"><span data-stu-id="2cac6-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2cac6-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2cac6-120">Heading</span></span> | <span data-ttu-id="2cac6-121">Текст</span><span class="sxs-lookup"><span data-stu-id="2cac6-121">Text</span></span> | <span data-ttu-id="2cac6-122">Заголовок модуля.</span><span class="sxs-lookup"><span data-stu-id="2cac6-122">The heading for the module.</span></span> |
| <span data-ttu-id="2cac6-123">Целевой URL-адрес</span><span class="sxs-lookup"><span data-stu-id="2cac6-123">Target URL</span></span> | <span data-ttu-id="2cac6-124">URL</span><span class="sxs-lookup"><span data-stu-id="2cac6-124">URL</span></span> | <span data-ttu-id="2cac6-125">URL-адрес, размещенный в модуле.</span><span class="sxs-lookup"><span data-stu-id="2cac6-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="2cac6-126">Высота</span><span class="sxs-lookup"><span data-stu-id="2cac6-126">Height</span></span> | <span data-ttu-id="2cac6-127">Число или процент</span><span class="sxs-lookup"><span data-stu-id="2cac6-127">Number or percentage</span></span> | <span data-ttu-id="2cac6-128">Высота модуля в точках или в процентах.</span><span class="sxs-lookup"><span data-stu-id="2cac6-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="2cac6-129">Например, значение **100** будет обрабатываться как число пикселей, а значение **100%** будет обработано как процент.</span><span class="sxs-lookup"><span data-stu-id="2cac6-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="2cac6-130">Метка Aria</span><span class="sxs-lookup"><span data-stu-id="2cac6-130">Aria label</span></span> | <span data-ttu-id="2cac6-131">Текст</span><span class="sxs-lookup"><span data-stu-id="2cac6-131">Text</span></span> | <span data-ttu-id="2cac6-132">Для обеспечения специальных возможностей можно задать метку доступных полнофункциональных интернет-приложений (ARIA).</span><span class="sxs-lookup"><span data-stu-id="2cac6-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="2cac6-133">Добавление модуля iFrame на страницу</span><span class="sxs-lookup"><span data-stu-id="2cac6-133">Add an iframe module to a page</span></span>

<span data-ttu-id="2cac6-134">Чтобы добавить модуль iFrame на страницу для отображения внешнего видео, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2cac6-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="2cac6-135">Перейдите к пункту **Шаблоны**, выберите **Создать**, чтобы создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="2cac6-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2cac6-136">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон маркетинга**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2cac6-137">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="2cac6-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2cac6-138">Перейдите к разделу **Страницы**, выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="2cac6-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2cac6-139">В диалоговом окне **Выбор шаблона** выберите **Шаблон маркетинга**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="2cac6-140">В поле **Имя страницы** введите **Страница маркетинга**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2cac6-141">В слоте **Главный** новой страницы выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cac6-142">В диалоговом окне **Добавить модуль** выберите модуль **Контейнер**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cac6-143">В области свойства модуля установите значение **Ширина** как **Вписать в контейнер**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2cac6-144">В ячейке **Контейнер** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2cac6-145">В диалоговом окне **Добавить модуль** выберите модуль **iFrame**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2cac6-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2cac6-146">В области свойства модуля задайте значение **Целевой URL-адрес** для внешнего URL-адреса видео.</span><span class="sxs-lookup"><span data-stu-id="2cac6-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="2cac6-147">Задайте другие свойства, такие как **Заголовок** и **Высота**, как требуется.</span><span class="sxs-lookup"><span data-stu-id="2cac6-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="2cac6-148">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="2cac6-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2cac6-149">Перейдите на страницу маркетинга на своем сайте.</span><span class="sxs-lookup"><span data-stu-id="2cac6-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="2cac6-150">Вы увидите, что видео отображается в модуле iFrame.</span><span class="sxs-lookup"><span data-stu-id="2cac6-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="2cac6-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2cac6-151">Additional resources</span></span>

[<span data-ttu-id="2cac6-152">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="2cac6-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2cac6-153">Управление политикой безопасности содержимого (CSP)</span><span class="sxs-lookup"><span data-stu-id="2cac6-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
