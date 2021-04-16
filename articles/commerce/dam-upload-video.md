---
title: Отправка видео
description: В этом разделе описывается, как отправить видео в конструктор сайта Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799213"
---
# <a name="upload-videos"></a><span data-ttu-id="162fd-103">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="162fd-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="162fd-104">В этом разделе описывается, как отправить видео в конструктор сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="162fd-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="162fd-105">Библиотека мультимедиа конфигуратора сайта Commerce позволяет отправлять видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="162fd-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="162fd-106">Следует всегда отправлять версию видеозаписи с наивысшим битрейтом и разрешением, так как видео будет автоматически преобразовано в соответствии с разными окнами просмотра и их точками останова.</span><span class="sxs-lookup"><span data-stu-id="162fd-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="162fd-107">Сведения о видео, указанные при отправке</span><span class="sxs-lookup"><span data-stu-id="162fd-107">Video information specified during upload</span></span>

<span data-ttu-id="162fd-108">При отправке видео могут быть указаны следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="162fd-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="162fd-109">**Заголовок, описание, ключевые слова**: метаданные видео.</span><span class="sxs-lookup"><span data-stu-id="162fd-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="162fd-110">**Автоматически создавать скрытые субтитры**: определяет, следует ли автоматически создавать скрытые субтитры для видео.</span><span class="sxs-lookup"><span data-stu-id="162fd-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="162fd-111">**Скрытые субтитры**: определяет используемые скрытые субтитры.</span><span class="sxs-lookup"><span data-stu-id="162fd-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="162fd-112">**Обычный звук**: определяет стандартную звуковую дорожку, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="162fd-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="162fd-113">**Эскиз**: определяет миниатюру видео.</span><span class="sxs-lookup"><span data-stu-id="162fd-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="162fd-114">Если не указано, он будет создан автоматически.</span><span class="sxs-lookup"><span data-stu-id="162fd-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="162fd-115">**Описательный звук**: определяет описательную звуковую дорожку, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="162fd-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="162fd-116">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="162fd-116">Upload a video</span></span>

<span data-ttu-id="162fd-117">Чтобы отправить видео в конфигуратор сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="162fd-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="162fd-118">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="162fd-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="162fd-119">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="162fd-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="162fd-120">В окне проводника перейдите к одному или нескольким файлам видео, которые необходимо отправить, выберите их, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="162fd-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="162fd-121">В диалоговом окне **Отправить элемент мультимедиа** введите требуемый заголовок и альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="162fd-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="162fd-122">Введите необязательное описание и ключевые слова, затем выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="162fd-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="162fd-123">Если требуется опубликовать изображения сразу же после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="162fd-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="162fd-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="162fd-124">Select **OK**.</span></span>

<span data-ttu-id="162fd-125">При одновременной отправке нескольких типов активов (например, изображений и видеороликов) в диалоговом окне **Отправить элемент мультимедиа** можно будет указать только ключевые слова, должны ли файлы быть опубликованы сразу после отправки, и должны ли быть автоматически созданы скрытые субтитры для видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="162fd-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="162fd-126">Все активы будут иметь одинаковые ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="162fd-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="162fd-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="162fd-127">Additional resources</span></span>

[<span data-ttu-id="162fd-128">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="162fd-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="162fd-129">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="162fd-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="162fd-130">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="162fd-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="162fd-131">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="162fd-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="162fd-132">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="162fd-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="162fd-133">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="162fd-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
