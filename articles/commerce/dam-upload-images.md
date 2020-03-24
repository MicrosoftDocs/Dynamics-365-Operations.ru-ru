---
title: Отправка изображений
description: В этом разделе описывается, как отправить изображения в конструктор сайта Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097073"
---
# <a name="upload-images"></a><span data-ttu-id="90279-103">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="90279-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90279-104">В этом разделе описывается, как отправить изображения в конструктор сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="90279-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="90279-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="90279-105">Overview</span></span>

<span data-ttu-id="90279-106">Библиотека мультимедиа конструктора сайта Commerce позволяет отправлять изображения либо по одному, либо в пакетном режиме с помощью папок.</span><span class="sxs-lookup"><span data-stu-id="90279-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="90279-107">Следует всегда отправлять версию изображения с наивысшим разрешением и качеством, так как компонент изменения размера изображения будет автоматически оптимизировать изображение для разных экранов и их точек останова.</span><span class="sxs-lookup"><span data-stu-id="90279-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="90279-108">Сведения об изображении, указанные при отправке</span><span class="sxs-lookup"><span data-stu-id="90279-108">Image information specified during upload</span></span>

<span data-ttu-id="90279-109">При отправке изображения могут быть указаны следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="90279-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="90279-110">**Заголовок, альтернативный текст, описание, ключевые слова**: метаданные изображения или изображений.</span><span class="sxs-lookup"><span data-stu-id="90279-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="90279-111">Заголовок и альтернативный текст — это обязательные значения.</span><span class="sxs-lookup"><span data-stu-id="90279-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="90279-112">**Выберите категорию**:</span><span class="sxs-lookup"><span data-stu-id="90279-112">**Select category**:</span></span>
    - <span data-ttu-id="90279-113">**Нет**: используется для повествовательного изображения или изображений электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="90279-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="90279-114">**Продукт, категория, клиент, сотрудник, каталог**: используется для многоканального изображения или изображений Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="90279-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="90279-115">**Публикация активов после отправки**: если этот флажок установлен, изображение или изображения публикуются сразу после отправки.</span><span class="sxs-lookup"><span data-stu-id="90279-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="90279-116">Активы изображений с назначенной категорией также автоматически помечаются категорией как ключевым словом, чтобы облегчить поиск активов определенной категории.</span><span class="sxs-lookup"><span data-stu-id="90279-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="90279-117">Соглашения об именовании для многоканальных изображений</span><span class="sxs-lookup"><span data-stu-id="90279-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="90279-118">Если библиотека мультимедиа настроена как серверное многоканальное изображение, можно использовать категории изображений, чтобы указать категорию, к которой принадлежит отправленное изображение.</span><span class="sxs-lookup"><span data-stu-id="90279-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="90279-119">Имеется также соглашение об именах, которое следует соблюдать, чтобы обеспечить, что изображения правильно извлекаются другими каналами, например, POS-терминалом.</span><span class="sxs-lookup"><span data-stu-id="90279-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="90279-120">Соглашение об именах по умолчанию основано на категории:</span><span class="sxs-lookup"><span data-stu-id="90279-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="90279-121">Изображения каталога должны иметь имя "**/Catalogs/\{КодЯзыка\}/\{ИмяКаталога\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="90279-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="90279-122">Изображения категорий должны иметь имя "**/Categories/\{ИмяКатегории\}.png**"</span><span class="sxs-lookup"><span data-stu-id="90279-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="90279-123">Изображения клиентов должны иметь имя "**/Customers/\{НомерКлиента\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="90279-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="90279-124">Изображения сотрудников должны иметь имя "**/Workers/\{НомерСотрудника\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="90279-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="90279-125">Изображения продуктов должны иметь имя "**/Products/\{НомерПродукта\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="90279-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="90279-126">001 — это последовательность изображения, которая может быть равна 001, 002, 003, 004 или 005</span><span class="sxs-lookup"><span data-stu-id="90279-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="90279-127">Изображения вариантов продуктов должны иметь имя "**/Products/\{НомерПродукта\}\_\{Размер\}\_\{Цвет\}\_\{Стиль\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="90279-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="90279-128">Отправка изображения</span><span class="sxs-lookup"><span data-stu-id="90279-128">Upload an image</span></span>

<span data-ttu-id="90279-129">Чтобы отправить изображение в конфигуратор сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90279-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90279-130">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="90279-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="90279-131">На панели команд выберите пункт **Отправить \> Отправить элементы мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="90279-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="90279-132">В окне проводника перейдите к одному или нескольким файлам изображений, которые необходимо отправить, выберите их, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="90279-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="90279-133">В диалоговом окне **Отправить элемент мультимедиа** введите требуемый заголовок и альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="90279-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="90279-134">Введите необязательное описание и ключевые слова, затем выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="90279-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="90279-135">Если требуется опубликовать изображения сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="90279-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="90279-136">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90279-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="90279-137">Отправка папки с изображениями</span><span class="sxs-lookup"><span data-stu-id="90279-137">Upload a folder of images</span></span>

<span data-ttu-id="90279-138">Для пакетной отправки папки изображений в конфигуратор сайта выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90279-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90279-139">В левой области переходов выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="90279-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="90279-140">На панели команд выберите пункт **Отправить \> Отправить папку**.</span><span class="sxs-lookup"><span data-stu-id="90279-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="90279-141">В окне проводника перейдите к папке, которую необходимо отправить, выберите ее, затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="90279-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="90279-142">В диалоговом окне **Отправить элемент мультимедиа** введите дополнительные ключевые слова и выберите категорию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="90279-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="90279-143">Если требуется опубликовать изображения в папке сразу после отправки, установите флажок **Опубликовать элементы мультимедиа после отправки**.</span><span class="sxs-lookup"><span data-stu-id="90279-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="90279-144">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="90279-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90279-145">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="90279-145">Additional resources</span></span>

[<span data-ttu-id="90279-146">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="90279-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="90279-147">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="90279-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="90279-148">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="90279-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="90279-149">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="90279-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="90279-150">Настройка фокальных точек изображения</span><span class="sxs-lookup"><span data-stu-id="90279-150">Customize image focal points</span></span>](dam-custom-focal-point.md)
