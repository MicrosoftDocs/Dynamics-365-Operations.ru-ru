---
title: Отправка файлов, отличных от изображений и видео
description: В этом разделе описывается, как отправлять двоичные файлы, отличные от изображений и видеозаписей в конфигуратор сайтов Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799261"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="6be6a-103">Отправка файлов, отличных от изображений и видео</span><span class="sxs-lookup"><span data-stu-id="6be6a-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6be6a-104">В этом разделе описывается, как отправлять файлы, отличные от изображений и видеозаписей в конфигуратор сайтов Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6be6a-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="6be6a-105">Библиотека мультимедиа конфигуратора сайтов Commerce поддерживает отправку двоичных активов, отличных от изображений или видео.</span><span class="sxs-lookup"><span data-stu-id="6be6a-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="6be6a-106">Например, может потребоваться отправить файлы Microsoft Excel, Microsoft Word, Microsoft PowerPoint или PDF.</span><span class="sxs-lookup"><span data-stu-id="6be6a-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="6be6a-107">Поддерживаются следующие типы документов:</span><span class="sxs-lookup"><span data-stu-id="6be6a-107">The following document types are supported:</span></span>
- <span data-ttu-id="6be6a-108">7Z</span><span class="sxs-lookup"><span data-stu-id="6be6a-108">7Z</span></span>
- <span data-ttu-id="6be6a-109">AVI</span><span class="sxs-lookup"><span data-stu-id="6be6a-109">AVI</span></span>
- <span data-ttu-id="6be6a-110">CS</span><span class="sxs-lookup"><span data-stu-id="6be6a-110">CS</span></span>
- <span data-ttu-id="6be6a-111">CSS</span><span class="sxs-lookup"><span data-stu-id="6be6a-111">CSS</span></span>
- <span data-ttu-id="6be6a-112">DOC</span><span class="sxs-lookup"><span data-stu-id="6be6a-112">DOC</span></span>
- <span data-ttu-id="6be6a-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="6be6a-113">DOCX</span></span>
- <span data-ttu-id="6be6a-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="6be6a-114">EPUB</span></span>
- <span data-ttu-id="6be6a-115">GIF</span><span class="sxs-lookup"><span data-stu-id="6be6a-115">GIF</span></span>
- <span data-ttu-id="6be6a-116">INDD</span><span class="sxs-lookup"><span data-stu-id="6be6a-116">INDD</span></span>
- <span data-ttu-id="6be6a-117">JAR</span><span class="sxs-lookup"><span data-stu-id="6be6a-117">JAR</span></span>
- <span data-ttu-id="6be6a-118">JPG</span><span class="sxs-lookup"><span data-stu-id="6be6a-118">JPG</span></span>
- <span data-ttu-id="6be6a-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="6be6a-119">JPEG</span></span>
- <span data-ttu-id="6be6a-120">JS</span><span class="sxs-lookup"><span data-stu-id="6be6a-120">JS</span></span>
- <span data-ttu-id="6be6a-121">MP3</span><span class="sxs-lookup"><span data-stu-id="6be6a-121">MP3</span></span>
- <span data-ttu-id="6be6a-122">MP4</span><span class="sxs-lookup"><span data-stu-id="6be6a-122">MP4</span></span>
- <span data-ttu-id="6be6a-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="6be6a-123">MPEG</span></span>
- <span data-ttu-id="6be6a-124">MPG</span><span class="sxs-lookup"><span data-stu-id="6be6a-124">MPG</span></span>
- <span data-ttu-id="6be6a-125">ODP</span><span class="sxs-lookup"><span data-stu-id="6be6a-125">ODP</span></span>
- <span data-ttu-id="6be6a-126">ODS</span><span class="sxs-lookup"><span data-stu-id="6be6a-126">ODS</span></span>
- <span data-ttu-id="6be6a-127">ODT</span><span class="sxs-lookup"><span data-stu-id="6be6a-127">ODT</span></span>
- <span data-ttu-id="6be6a-128">PDF</span><span class="sxs-lookup"><span data-stu-id="6be6a-128">PDF</span></span>
- <span data-ttu-id="6be6a-129">PNG</span><span class="sxs-lookup"><span data-stu-id="6be6a-129">PNG</span></span>
- <span data-ttu-id="6be6a-130">PPT</span><span class="sxs-lookup"><span data-stu-id="6be6a-130">PPT</span></span>
- <span data-ttu-id="6be6a-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="6be6a-131">PPTX</span></span>
- <span data-ttu-id="6be6a-132">PS</span><span class="sxs-lookup"><span data-stu-id="6be6a-132">PS</span></span>
- <span data-ttu-id="6be6a-133">QXP</span><span class="sxs-lookup"><span data-stu-id="6be6a-133">QXP</span></span>
- <span data-ttu-id="6be6a-134">RAR</span><span class="sxs-lookup"><span data-stu-id="6be6a-134">RAR</span></span>
- <span data-ttu-id="6be6a-135">RTF</span><span class="sxs-lookup"><span data-stu-id="6be6a-135">RTF</span></span>
- <span data-ttu-id="6be6a-136">SVG</span><span class="sxs-lookup"><span data-stu-id="6be6a-136">SVG</span></span>
- <span data-ttu-id="6be6a-137">TAR</span><span class="sxs-lookup"><span data-stu-id="6be6a-137">TAR</span></span>
- <span data-ttu-id="6be6a-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="6be6a-138">TGZ</span></span>
- <span data-ttu-id="6be6a-139">TXT</span><span class="sxs-lookup"><span data-stu-id="6be6a-139">TXT</span></span>
- <span data-ttu-id="6be6a-140">WMV</span><span class="sxs-lookup"><span data-stu-id="6be6a-140">WMV</span></span>
- <span data-ttu-id="6be6a-141">XLS</span><span class="sxs-lookup"><span data-stu-id="6be6a-141">XLS</span></span>
- <span data-ttu-id="6be6a-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="6be6a-142">XLSX</span></span>
- <span data-ttu-id="6be6a-143">XML</span><span class="sxs-lookup"><span data-stu-id="6be6a-143">XML</span></span>
- <span data-ttu-id="6be6a-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="6be6a-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="6be6a-145">Отправить файл</span><span class="sxs-lookup"><span data-stu-id="6be6a-145">Upload a file</span></span>

<span data-ttu-id="6be6a-146">Чтобы отправить файл в конфигуратор сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6be6a-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6be6a-147">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="6be6a-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="6be6a-148">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="6be6a-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="6be6a-149">В проводнике выберите один или несколько файлов, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="6be6a-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="6be6a-150">В диалоговом окне **Отправить элементы мультимедиа** введите требуемые заголовок, описание и метаданные ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="6be6a-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="6be6a-151">Чтобы опубликовать файлы сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="6be6a-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="6be6a-152">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6be6a-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6be6a-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6be6a-153">Additional resources</span></span>

[<span data-ttu-id="6be6a-154">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="6be6a-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="6be6a-155">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="6be6a-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="6be6a-156">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="6be6a-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="6be6a-157">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="6be6a-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="6be6a-158">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="6be6a-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="6be6a-159">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="6be6a-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
