---
title: Отправка файлов, отличных от изображений и видео
description: В этом разделе описывается, как отправлять двоичные файлы, отличные от изображений и видеозаписей в конфигуратор сайтов Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995778"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="51222-103">Отправка файлов, отличных от изображений и видео</span><span class="sxs-lookup"><span data-stu-id="51222-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51222-104">В этом разделе описывается, как отправлять файлы, отличные от изображений и видеозаписей в конфигуратор сайтов Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51222-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="51222-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="51222-105">Overview</span></span>

<span data-ttu-id="51222-106">Библиотека мультимедиа конфигуратора сайтов Commerce поддерживает отправку двоичных активов, отличных от изображений или видео.</span><span class="sxs-lookup"><span data-stu-id="51222-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="51222-107">Например, может потребоваться отправить файлы Microsoft Excel, Microsoft Word, Microsoft PowerPoint или PDF.</span><span class="sxs-lookup"><span data-stu-id="51222-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="51222-108">Поддерживаются следующие типы документов:</span><span class="sxs-lookup"><span data-stu-id="51222-108">The following document types are supported:</span></span>
- <span data-ttu-id="51222-109">7Z</span><span class="sxs-lookup"><span data-stu-id="51222-109">7Z</span></span>
- <span data-ttu-id="51222-110">AVI</span><span class="sxs-lookup"><span data-stu-id="51222-110">AVI</span></span>
- <span data-ttu-id="51222-111">CS</span><span class="sxs-lookup"><span data-stu-id="51222-111">CS</span></span>
- <span data-ttu-id="51222-112">CSS</span><span class="sxs-lookup"><span data-stu-id="51222-112">CSS</span></span>
- <span data-ttu-id="51222-113">DOC</span><span class="sxs-lookup"><span data-stu-id="51222-113">DOC</span></span>
- <span data-ttu-id="51222-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="51222-114">DOCX</span></span>
- <span data-ttu-id="51222-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="51222-115">EPUB</span></span>
- <span data-ttu-id="51222-116">GIF</span><span class="sxs-lookup"><span data-stu-id="51222-116">GIF</span></span>
- <span data-ttu-id="51222-117">INDD</span><span class="sxs-lookup"><span data-stu-id="51222-117">INDD</span></span>
- <span data-ttu-id="51222-118">JAR</span><span class="sxs-lookup"><span data-stu-id="51222-118">JAR</span></span>
- <span data-ttu-id="51222-119">JPG</span><span class="sxs-lookup"><span data-stu-id="51222-119">JPG</span></span>
- <span data-ttu-id="51222-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="51222-120">JPEG</span></span>
- <span data-ttu-id="51222-121">JS</span><span class="sxs-lookup"><span data-stu-id="51222-121">JS</span></span>
- <span data-ttu-id="51222-122">MP3</span><span class="sxs-lookup"><span data-stu-id="51222-122">MP3</span></span>
- <span data-ttu-id="51222-123">MP4</span><span class="sxs-lookup"><span data-stu-id="51222-123">MP4</span></span>
- <span data-ttu-id="51222-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="51222-124">MPEG</span></span>
- <span data-ttu-id="51222-125">MPG</span><span class="sxs-lookup"><span data-stu-id="51222-125">MPG</span></span>
- <span data-ttu-id="51222-126">ODP</span><span class="sxs-lookup"><span data-stu-id="51222-126">ODP</span></span>
- <span data-ttu-id="51222-127">ODS</span><span class="sxs-lookup"><span data-stu-id="51222-127">ODS</span></span>
- <span data-ttu-id="51222-128">ODT</span><span class="sxs-lookup"><span data-stu-id="51222-128">ODT</span></span>
- <span data-ttu-id="51222-129">PDF</span><span class="sxs-lookup"><span data-stu-id="51222-129">PDF</span></span>
- <span data-ttu-id="51222-130">PNG</span><span class="sxs-lookup"><span data-stu-id="51222-130">PNG</span></span>
- <span data-ttu-id="51222-131">PPT</span><span class="sxs-lookup"><span data-stu-id="51222-131">PPT</span></span>
- <span data-ttu-id="51222-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="51222-132">PPTX</span></span>
- <span data-ttu-id="51222-133">PS</span><span class="sxs-lookup"><span data-stu-id="51222-133">PS</span></span>
- <span data-ttu-id="51222-134">QXP</span><span class="sxs-lookup"><span data-stu-id="51222-134">QXP</span></span>
- <span data-ttu-id="51222-135">RAR</span><span class="sxs-lookup"><span data-stu-id="51222-135">RAR</span></span>
- <span data-ttu-id="51222-136">RTF</span><span class="sxs-lookup"><span data-stu-id="51222-136">RTF</span></span>
- <span data-ttu-id="51222-137">SVG</span><span class="sxs-lookup"><span data-stu-id="51222-137">SVG</span></span>
- <span data-ttu-id="51222-138">TAR</span><span class="sxs-lookup"><span data-stu-id="51222-138">TAR</span></span>
- <span data-ttu-id="51222-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="51222-139">TGZ</span></span>
- <span data-ttu-id="51222-140">TXT</span><span class="sxs-lookup"><span data-stu-id="51222-140">TXT</span></span>
- <span data-ttu-id="51222-141">WMV</span><span class="sxs-lookup"><span data-stu-id="51222-141">WMV</span></span>
- <span data-ttu-id="51222-142">XLS</span><span class="sxs-lookup"><span data-stu-id="51222-142">XLS</span></span>
- <span data-ttu-id="51222-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="51222-143">XLSX</span></span>
- <span data-ttu-id="51222-144">XML</span><span class="sxs-lookup"><span data-stu-id="51222-144">XML</span></span>
- <span data-ttu-id="51222-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="51222-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="51222-146">Отправить файл</span><span class="sxs-lookup"><span data-stu-id="51222-146">Upload a file</span></span>

<span data-ttu-id="51222-147">Чтобы отправить файл в конфигуратор сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="51222-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="51222-148">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="51222-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="51222-149">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="51222-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="51222-150">В проводнике выберите один или несколько файлов, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="51222-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="51222-151">В диалоговом окне **Отправить элементы мультимедиа** введите требуемые заголовок, описание и метаданные ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="51222-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="51222-152">Чтобы опубликовать файлы сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="51222-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="51222-153">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="51222-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51222-154">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51222-154">Additional resources</span></span>

[<span data-ttu-id="51222-155">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="51222-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="51222-156">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="51222-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="51222-157">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="51222-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="51222-158">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="51222-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="51222-159">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="51222-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="51222-160">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="51222-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
