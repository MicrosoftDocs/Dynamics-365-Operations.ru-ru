---
title: Отправка видео
description: В этом разделе описывается, как отправить видео в конструктор сайта Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dd9e710f9a6ea593a0673e7902fadf84ca05cff
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594316"
---
# <a name="upload-videos"></a><span data-ttu-id="22196-103">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="22196-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22196-104">В этом разделе описывается, как отправить видео в конструктор сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22196-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="22196-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="22196-105">Overview</span></span>

<span data-ttu-id="22196-106">Библиотека мультимедиа конфигуратора сайта Commerce позволяет отправлять видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="22196-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="22196-107">Следует всегда отправлять версию видеозаписи с наивысшим битрейтом и разрешением, так как видео будет автоматически преобразовано в соответствии с разными окнами просмотра и их точками останова.</span><span class="sxs-lookup"><span data-stu-id="22196-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="22196-108">Сведения о видео, указанные при отправке</span><span class="sxs-lookup"><span data-stu-id="22196-108">Video information specified during upload</span></span>

<span data-ttu-id="22196-109">При отправке видео могут быть указаны следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="22196-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="22196-110">**Заголовок, описание, ключевые слова**: метаданные видео.</span><span class="sxs-lookup"><span data-stu-id="22196-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="22196-111">**Автоматически создавать скрытые субтитры**: определяет, следует ли автоматически создавать скрытые субтитры для видео.</span><span class="sxs-lookup"><span data-stu-id="22196-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="22196-112">**Скрытые субтитры**: определяет используемые скрытые субтитры.</span><span class="sxs-lookup"><span data-stu-id="22196-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="22196-113">**Обычный звук**: определяет стандартную звуковую дорожку, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="22196-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="22196-114">**Эскиз**: определяет миниатюру видео.</span><span class="sxs-lookup"><span data-stu-id="22196-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="22196-115">Если не указано, он будет создан автоматически.</span><span class="sxs-lookup"><span data-stu-id="22196-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="22196-116">**Описательный звук**: определяет описательную звуковую дорожку, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="22196-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="22196-117">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="22196-117">Upload a video</span></span>

<span data-ttu-id="22196-118">Чтобы отправить видео в конфигуратор сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="22196-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="22196-119">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="22196-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="22196-120">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="22196-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="22196-121">В окне проводника перейдите к одному или нескольким файлам видео, которые необходимо отправить, выберите их, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="22196-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="22196-122">В диалоговом окне **Отправить элемент мультимедиа** введите требуемый заголовок и альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="22196-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="22196-123">Введите необязательное описание и ключевые слова, затем выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="22196-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="22196-124">Если требуется опубликовать изображения сразу же после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="22196-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="22196-125">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="22196-125">Select **OK**.</span></span>

<span data-ttu-id="22196-126">При одновременной отправке нескольких типов активов (например, изображений и видеороликов) в диалоговом окне **Отправить элемент мультимедиа** можно будет указать только ключевые слова, должны ли файлы быть опубликованы сразу после отправки, и должны ли быть автоматически созданы скрытые субтитры для видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="22196-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="22196-127">Все активы будут иметь одинаковые ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="22196-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22196-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="22196-128">Additional resources</span></span>

[<span data-ttu-id="22196-129">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="22196-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="22196-130">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="22196-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="22196-131">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="22196-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="22196-132">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="22196-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="22196-133">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="22196-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="22196-134">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="22196-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
