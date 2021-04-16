---
title: Отправка изображений
description: В этом разделе описывается, как отправить изображения в конструктор сайта Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799237"
---
# <a name="upload-images"></a><span data-ttu-id="f2a26-103">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="f2a26-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2a26-104">В этом разделе описывается, как отправить изображения в конструктор сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2a26-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="f2a26-105">Библиотека мультимедиа конструктора сайта Commerce позволяет отправлять изображения либо по одному, либо в пакетном режиме с помощью папок.</span><span class="sxs-lookup"><span data-stu-id="f2a26-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="f2a26-106">Следует всегда отправлять версию изображения с наивысшим разрешением и качеством, так как компонент изменения размера изображения будет автоматически оптимизировать изображение для разных экранов и их точек останова.</span><span class="sxs-lookup"><span data-stu-id="f2a26-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="f2a26-107">Сведения об изображении, указанные при отправке</span><span class="sxs-lookup"><span data-stu-id="f2a26-107">Image information specified during upload</span></span>

<span data-ttu-id="f2a26-108">При отправке изображения могут быть указаны следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="f2a26-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="f2a26-109">**Заголовок, альтернативный текст, описание, ключевые слова**: метаданные изображения или изображений.</span><span class="sxs-lookup"><span data-stu-id="f2a26-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="f2a26-110">Заголовок и альтернативный текст — это обязательные значения.</span><span class="sxs-lookup"><span data-stu-id="f2a26-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="f2a26-111">**Выберите категорию**:</span><span class="sxs-lookup"><span data-stu-id="f2a26-111">**Select category**:</span></span>
    - <span data-ttu-id="f2a26-112">**Нет**: используется для повествовательного изображения или изображений электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="f2a26-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="f2a26-113">**Продукт, категория, клиент, сотрудник, каталог**: используется для многоканального изображения или изображений Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2a26-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="f2a26-114">**Публикация активов после отправки**: если этот флажок установлен, изображение или изображения публикуются сразу после отправки.</span><span class="sxs-lookup"><span data-stu-id="f2a26-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="f2a26-115">Активы изображений с назначенной категорией также автоматически помечаются категорией как ключевым словом, чтобы облегчить поиск активов определенной категории.</span><span class="sxs-lookup"><span data-stu-id="f2a26-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="f2a26-116">Соглашения об именовании для многоканальных изображений</span><span class="sxs-lookup"><span data-stu-id="f2a26-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="f2a26-117">Если библиотека мультимедиа настроена как серверное многоканальное изображение, можно использовать категории изображений, чтобы указать категорию, к которой принадлежит отправленное изображение.</span><span class="sxs-lookup"><span data-stu-id="f2a26-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="f2a26-118">Имеется также соглашение об именах, которое следует соблюдать, чтобы обеспечить, что изображения правильно извлекаются другими каналами, например, POS-терминалом.</span><span class="sxs-lookup"><span data-stu-id="f2a26-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="f2a26-119">Соглашение об именах по умолчанию основано на категории:</span><span class="sxs-lookup"><span data-stu-id="f2a26-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="f2a26-120">Изображения каталога должны иметь имя "**/Catalogs/\{КодЯзыка\}/\{ИмяКаталога\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="f2a26-121">Изображения категорий должны иметь имя "**/Categories/\{ИмяКатегории\}.png**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="f2a26-122">Изображения клиентов должны иметь имя "**/Customers/\{НомерКлиента\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="f2a26-123">Изображения сотрудников должны иметь имя "**/Workers/\{НомерСотрудника\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="f2a26-124">Изображения продуктов должны иметь имя "**/Products/\{НомерПродукта\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="f2a26-125">001 — это последовательность изображения, которая может быть равна 001, 002, 003, 004 или 005</span><span class="sxs-lookup"><span data-stu-id="f2a26-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="f2a26-126">Изображения вариантов продуктов должны иметь имя "**/Products/\{НомерПродукта\} \^ \{Стиль\} \^ \{Размер\} \^ \{Цвет\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="f2a26-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="f2a26-127">Например: 93039 \^ \^ 2 \^ Черный \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="f2a26-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="f2a26-128">Отправка изображения</span><span class="sxs-lookup"><span data-stu-id="f2a26-128">Upload an image</span></span>

<span data-ttu-id="f2a26-129">Чтобы отправить изображение в конфигуратор сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2a26-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="f2a26-130">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f2a26-131">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="f2a26-132">В окне проводника перейдите к одному или нескольким файлам изображений, которые необходимо отправить, выберите их, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="f2a26-133">В диалоговом окне **Отправить элемент мультимедиа** введите требуемый заголовок и альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="f2a26-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="f2a26-134">Введите необязательное описание и ключевые слова, затем выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f2a26-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="f2a26-135">Если требуется опубликовать изображения сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f2a26-136">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="f2a26-137">Отправка папки с изображениями</span><span class="sxs-lookup"><span data-stu-id="f2a26-137">Upload a folder of images</span></span>

<span data-ttu-id="f2a26-138">Для пакетной отправки папки изображений в конфигуратор сайта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2a26-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="f2a26-139">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f2a26-140">На панели команд выберите пункт **Отправить \> Отправить папку**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="f2a26-141">В окне проводника перейдите к папке, которую необходимо отправить, выберите ее, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="f2a26-142">В диалоговом окне **Отправить элемент мультимедиа** введите дополнительные ключевые слова и выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f2a26-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="f2a26-143">Если требуется опубликовать изображения в папке сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f2a26-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2a26-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2a26-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2a26-145">Additional resources</span></span>

[<span data-ttu-id="f2a26-146">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="f2a26-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f2a26-147">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="f2a26-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="f2a26-148">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="f2a26-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="f2a26-149">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="f2a26-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f2a26-150">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="f2a26-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="f2a26-151">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="f2a26-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
