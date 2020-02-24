---
title: Модуль видеопроигрывателя
description: В этом разделе описываются модули видеопроигрывателя, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025675"
---
# <a name="video-player-module"></a><span data-ttu-id="fde0a-103">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="fde0a-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fde0a-104">В этом разделе описываются модули видеопроигрывателя, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fde0a-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fde0a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="fde0a-105">Overview</span></span>

<span data-ttu-id="fde0a-106">Для поддержки воспроизведения видео используется модуль видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="fde0a-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="fde0a-107">Он может быть добавлен на любую страницу при условии, что видеоконтент загружен и доступен в системе управления контентом (CMS).</span><span class="sxs-lookup"><span data-stu-id="fde0a-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="fde0a-108">Модуль видеопроигрывателя поддерживает файлы MP4.</span><span class="sxs-lookup"><span data-stu-id="fde0a-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="fde0a-109">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="fde0a-109">Video player module</span></span>

<span data-ttu-id="fde0a-110">Модуль видеопроигрывателя может использоваться для демонстрации видеороликов на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="fde0a-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="fde0a-111">Он поддерживает все возможности воспроизведения, такие как воспроизведение, приостановка, режим полного размера, описания аудио и скрытые субтитры.</span><span class="sxs-lookup"><span data-stu-id="fde0a-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="fde0a-112">Модуль видеопроигрывателя также поддерживает настройку скрытых субтитров для соответствия стандартам специальных возможностей Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fde0a-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="fde0a-113">Например, можно настроить размер шрифта и цвет фона.</span><span class="sxs-lookup"><span data-stu-id="fde0a-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="fde0a-114">Модуль видеопроигрывателя также поддерживает второстепенные звуковые дорожки.</span><span class="sxs-lookup"><span data-stu-id="fde0a-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="fde0a-115">При отправке видео в CMS также может быть загружена второстепенная аудиодорожка.</span><span class="sxs-lookup"><span data-stu-id="fde0a-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="fde0a-116">Модуль видеопроигрывателя может воспроизводить второстепенную звуковую дорожку, если пользователь ее выбирает.</span><span class="sxs-lookup"><span data-stu-id="fde0a-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="fde0a-117">Примеры модулей видеопроигрывателя в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="fde0a-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="fde0a-118">Обучающие видеоматериалы на страницах с подробными сведениями о продуктах или на маркетинговых страницах</span><span class="sxs-lookup"><span data-stu-id="fde0a-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="fde0a-119">Рекламные видеоматериалы или видеозаписи о политиках на любой странице маркетинга</span><span class="sxs-lookup"><span data-stu-id="fde0a-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="fde0a-120">Маркетинговые видеоматериалы, отражающие характеристики продукции на страницах с подробными сведениями о продуктах или на маркетинговых страницах</span><span class="sxs-lookup"><span data-stu-id="fde0a-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="fde0a-121">Свойства модуля видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="fde0a-121">Video player module properties</span></span>

| <span data-ttu-id="fde0a-122">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="fde0a-122">Property name</span></span>         | <span data-ttu-id="fde0a-123">Стоимость</span><span class="sxs-lookup"><span data-stu-id="fde0a-123">Value</span></span>                               | <span data-ttu-id="fde0a-124">Описание</span><span class="sxs-lookup"><span data-stu-id="fde0a-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="fde0a-125">Автозапуск</span><span class="sxs-lookup"><span data-stu-id="fde0a-125">Auto play</span></span>             | <span data-ttu-id="fde0a-126">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-126">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-127">Когда установлено значение **True**, видео автоматически воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="fde0a-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="fde0a-128">Выключить звук</span><span class="sxs-lookup"><span data-stu-id="fde0a-128">Mute</span></span>                  | <span data-ttu-id="fde0a-129">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-129">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-130">Когда установлено значение **True**, звук видео автоматически отключается.</span><span class="sxs-lookup"><span data-stu-id="fde0a-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="fde0a-131">Для этого проигрывателя значение по умолчанию — **False**.</span><span class="sxs-lookup"><span data-stu-id="fde0a-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="fde0a-132">В браузере Chrome звук автоматически воспроизводимого видео по умолчанию отключен, и воспроизведение звука выполняется только в том случае, если видеозапись воспроизводится вручную пользователем.</span><span class="sxs-lookup"><span data-stu-id="fde0a-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="fde0a-133">Цикл</span><span class="sxs-lookup"><span data-stu-id="fde0a-133">Loop</span></span>                  | <span data-ttu-id="fde0a-134">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-134">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-135">Когда установлено значение **True**, видео повторяется циклически.</span><span class="sxs-lookup"><span data-stu-id="fde0a-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="fde0a-136">Источник</span><span class="sxs-lookup"><span data-stu-id="fde0a-136">Media</span></span>                 | <span data-ttu-id="fde0a-137">Имя и путь видеофайла</span><span class="sxs-lookup"><span data-stu-id="fde0a-137">Video file path and name</span></span> | <span data-ttu-id="fde0a-138">Видеофайл, воспроизводимый видеопроигрывателем.</span><span class="sxs-lookup"><span data-stu-id="fde0a-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="fde0a-139">Воспроизведение в полноэкранном режиме</span><span class="sxs-lookup"><span data-stu-id="fde0a-139">Play fullscreen</span></span>       | <span data-ttu-id="fde0a-140">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-140">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-141">Когда установлено значение **True**, видео воспроизводится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="fde0a-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="fde0a-142">Триггер приостановки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="fde0a-142">Play pause trigger</span></span>    | <span data-ttu-id="fde0a-143">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-143">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-144">Когда установлено значение **True**, на видео отображается кнопка воспроизведения/паузы.</span><span class="sxs-lookup"><span data-stu-id="fde0a-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="fde0a-145">Элементы управления видеопроигрывателем</span><span class="sxs-lookup"><span data-stu-id="fde0a-145">Video player controls</span></span> | <span data-ttu-id="fde0a-146">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-146">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-147">Когда установлено значение **True**, отображаются все элементы управления видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="fde0a-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="fde0a-148">К этим элементам управления относятся кнопки воспроизведения и паузы, индикатор хода выполнения и параметры скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="fde0a-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="fde0a-149">Скрыть изображение афиши</span><span class="sxs-lookup"><span data-stu-id="fde0a-149">Hide poster image</span></span>     | <span data-ttu-id="fde0a-150">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="fde0a-150">**True** or **False**</span></span>               | <span data-ttu-id="fde0a-151">Видео может иметь рамку афиши.</span><span class="sxs-lookup"><span data-stu-id="fde0a-151">A video can have a poster frame.</span></span> <span data-ttu-id="fde0a-152">Когда для этого свойства установлено значение **True**, рамка афиши скрывается.</span><span class="sxs-lookup"><span data-stu-id="fde0a-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="fde0a-153">Уровень максирования</span><span class="sxs-lookup"><span data-stu-id="fde0a-153">Mask level</span></span>            | <span data-ttu-id="fde0a-154">Число от **0** до **100**</span><span class="sxs-lookup"><span data-stu-id="fde0a-154">A number from **0** through **100**</span></span> | <span data-ttu-id="fde0a-155">Маска, применяемая к видео для стилизации.</span><span class="sxs-lookup"><span data-stu-id="fde0a-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="fde0a-156">Добавление модуля видеопроигрывателя на страницу</span><span class="sxs-lookup"><span data-stu-id="fde0a-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="fde0a-157">Перед созданием модуля видеопроигрывателя необходимо сначала отправить видео в библиотеку мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fde0a-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="fde0a-158">Чтобы добавить модуль видеопроигрывателя на новую страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fde0a-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fde0a-159">Создайте шаблон страницы с именем **шаблон видеопроигрывателя**.</span><span class="sxs-lookup"><span data-stu-id="fde0a-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="fde0a-160">В слоте **Главный** страницы по умолчанию добавьте модуль-контейнер.</span><span class="sxs-lookup"><span data-stu-id="fde0a-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="fde0a-161">В модуле-контейнере добавьте модули видеопроигрывателя и внутреннего видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="fde0a-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="fde0a-162">Завершите редактирование шаблона и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="fde0a-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="fde0a-163">Используйте созданный шаблон видеопроигрывателя для создания страницы с именем **страница видеопроигрывателя**.</span><span class="sxs-lookup"><span data-stu-id="fde0a-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="fde0a-164">В слоте **Главный** новой страницы добавьте модуль видеопроигрывателя.</span><span class="sxs-lookup"><span data-stu-id="fde0a-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="fde0a-165">В области свойств модуля видеопроигрыватель выберите **Добавить видео**.</span><span class="sxs-lookup"><span data-stu-id="fde0a-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="fde0a-166">В диалоговом окне **Выбор мультимедиа** выберите видео и нажмите **Отправить новый файл мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="fde0a-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="fde0a-167">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="fde0a-167">Save and preview the page.</span></span> <span data-ttu-id="fde0a-168">На странице должен отобразиться модуль видео.</span><span class="sxs-lookup"><span data-stu-id="fde0a-168">You should see the video module on the page.</span></span> <span data-ttu-id="fde0a-169">Можно изменить дополнительные настройки, чтобы настроить поведение модуля.</span><span class="sxs-lookup"><span data-stu-id="fde0a-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="fde0a-170">Завершите редактирование страницы и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="fde0a-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fde0a-171">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fde0a-171">Additional resources</span></span>

[<span data-ttu-id="fde0a-172">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="fde0a-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fde0a-173">Модуль рекламного баннера</span><span class="sxs-lookup"><span data-stu-id="fde0a-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="fde0a-174">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="fde0a-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fde0a-175">Модуль блока текста</span><span class="sxs-lookup"><span data-stu-id="fde0a-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fde0a-176">Модуль блока содержимого</span><span class="sxs-lookup"><span data-stu-id="fde0a-176">Content block module</span></span>](add-hero-module.md)
