---
title: Настройка фокальных точек изображения
description: В этом разделе описывается, как настраивать фокальные точки изображения в конструкторе сайта Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 2c9bbd51f1fe9a19198a455eedd3ba744d54a165
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097071"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="55432-103">Настройка фокальных точек изображения</span><span class="sxs-lookup"><span data-stu-id="55432-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55432-104">В этом разделе описывается, как настраивать фокальные точки изображения в конструкторе сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55432-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="55432-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="55432-105">Overview</span></span>

<span data-ttu-id="55432-106">При отправке изображения в библиотеку мультимедиа конфигуратора сайта Commerce система пытается определить фокальную точку изображения.</span><span class="sxs-lookup"><span data-stu-id="55432-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="55432-107">Например, если на изображении имеется человек, система по умолчанию устанавливает фокальную точку на лицо данного человека.</span><span class="sxs-lookup"><span data-stu-id="55432-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="55432-108">В большинстве случаев автоматически задается фокальная точка хорошо подходит для всех окон просмотра, но иногда может потребоваться скорректировать фокальную точку, чтобы гарантировать, что конкретная часть изображения всегда видна.</span><span class="sxs-lookup"><span data-stu-id="55432-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="55432-109">Определение пользовательской фокальной точки для изображения</span><span class="sxs-lookup"><span data-stu-id="55432-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="55432-110">Чтобы определить пользовательскую фокальную точку для изображения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="55432-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="55432-111">В левой области навигации конфигуратора сайта Commerce выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="55432-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="55432-112">В главном окне выберите изображение, которое необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="55432-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="55432-113">На панели команд выберите **Правка**, чтобы извлечь файл.</span><span class="sxs-lookup"><span data-stu-id="55432-113">On the command bar, select **Edit** to check out the file.</span></span>
1. <span data-ttu-id="55432-114">Выберите изображение, чтобы перейти в **Режим правки**.</span><span class="sxs-lookup"><span data-stu-id="55432-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="55432-115">В области **Режим правки** выберите **Изменить фокальную точку**.</span><span class="sxs-lookup"><span data-stu-id="55432-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="55432-116">Поверх изображения появится циклический элемент управления фокальной точкой.</span><span class="sxs-lookup"><span data-stu-id="55432-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="55432-117">Выберите элемент управления фокальной точкой, чтобы переместить его в нужную фокальную точку.</span><span class="sxs-lookup"><span data-stu-id="55432-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="55432-118">Когда закончите, на панели команд выберите **Сохранить**, затем выберите **Завершить редактирование**.</span><span class="sxs-lookup"><span data-stu-id="55432-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55432-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="55432-119">Additional resources</span></span>

[<span data-ttu-id="55432-120">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="55432-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="55432-121">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="55432-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="55432-122">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="55432-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="55432-123">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="55432-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="55432-124">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="55432-124">Crop images</span></span>](dam-crop-images.md)
