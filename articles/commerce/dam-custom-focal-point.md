---
title: Настройка фокальных точек изображения
description: В этом разделе описывается, как настраивать фокальные точки изображения в конструкторе сайта Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
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
ms.openlocfilehash: 962caff0e8e41487231c6075fa7b2df2a59dca48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799309"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="3192d-103">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="3192d-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3192d-104">В этом разделе описывается, как настраивать фокальные точки изображения в конструкторе сайта Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3192d-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="3192d-105">При отправке изображения в библиотеку мультимедиа конфигуратора сайта Commerce система пытается определить фокальную точку изображения.</span><span class="sxs-lookup"><span data-stu-id="3192d-105">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="3192d-106">Например, если на изображении имеется человек, система по умолчанию устанавливает фокальную точку на лицо данного человека.</span><span class="sxs-lookup"><span data-stu-id="3192d-106">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="3192d-107">В большинстве случаев автоматически задается фокальная точка хорошо подходит для всех окон просмотра, но иногда может потребоваться скорректировать фокальную точку, чтобы гарантировать, что конкретная часть изображения всегда видна.</span><span class="sxs-lookup"><span data-stu-id="3192d-107">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="3192d-108">Определение пользовательской фокальной точки для изображения</span><span class="sxs-lookup"><span data-stu-id="3192d-108">Define a custom focal point for an image</span></span>

<span data-ttu-id="3192d-109">Чтобы определить пользовательскую фокальную точку для изображения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3192d-109">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="3192d-110">В левой области навигации конфигуратора сайта Commerce выберите **Библиотека мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="3192d-110">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="3192d-111">В главном окне выберите изображение, которое необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="3192d-111">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="3192d-112">На панели команд выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="3192d-112">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="3192d-113">Выберите изображение, чтобы перейти в **Режим правки**.</span><span class="sxs-lookup"><span data-stu-id="3192d-113">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="3192d-114">В области **Режим правки** выберите **Изменить фокальную точку**.</span><span class="sxs-lookup"><span data-stu-id="3192d-114">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="3192d-115">Поверх изображения появится циклический элемент управления фокальной точкой.</span><span class="sxs-lookup"><span data-stu-id="3192d-115">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="3192d-116">Выберите элемент управления фокальной точкой, чтобы переместить его в нужную фокальную точку.</span><span class="sxs-lookup"><span data-stu-id="3192d-116">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="3192d-117">Когда закончите, на панели команд выберите **Сохранить**, затем выберите **Завершить редактирование**.</span><span class="sxs-lookup"><span data-stu-id="3192d-117">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3192d-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3192d-118">Additional resources</span></span>

[<span data-ttu-id="3192d-119">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="3192d-119">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3192d-120">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="3192d-120">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3192d-121">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="3192d-121">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="3192d-122">Отправка файлов</span><span class="sxs-lookup"><span data-stu-id="3192d-122">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="3192d-123">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="3192d-123">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3192d-124">Отправка и предоставление статических файлов</span><span class="sxs-lookup"><span data-stu-id="3192d-124">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
