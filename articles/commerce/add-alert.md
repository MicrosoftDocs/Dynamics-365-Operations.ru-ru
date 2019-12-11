---
title: Модуль оповещения
description: В этом разделе описываются модули оповещений, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785360"
---
# <a name="alert-module"></a><span data-ttu-id="d46ab-103">Модуль оповещения</span><span class="sxs-lookup"><span data-stu-id="d46ab-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d46ab-104">В этом разделе описываются модули оповещений, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d46ab-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d46ab-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d46ab-105">Overview</span></span>

<span data-ttu-id="d46ab-106">Модуль оповещения используется для отображения на странице встроенных информационных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d46ab-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="d46ab-107">Модули оповещения поддерживают текстовое сообщение и ссылку.</span><span class="sxs-lookup"><span data-stu-id="d46ab-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="d46ab-108">Они могут использоваться для отображения рекламных акций на уровне всего сайта, которые появляются на всех страницах сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="d46ab-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="d46ab-109">Модули оповещения управляются данными из системы управления контентом (CMS) и их можно разместить на любой странице.</span><span class="sxs-lookup"><span data-stu-id="d46ab-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="d46ab-110">Примеры модулей оповещений в электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="d46ab-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="d46ab-111">Модули оповещения могут использоваться в заголовке сайта, чтобы указать рекламные акции или сообщения на уровне всего сайта.</span><span class="sxs-lookup"><span data-stu-id="d46ab-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="d46ab-112">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="d46ab-112">Here are some examples:</span></span>

<span data-ttu-id="d46ab-113">"Ежегодная распродажа заканчивается через 10 дней"</span><span class="sxs-lookup"><span data-stu-id="d46ab-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="d46ab-114">"Большая экономия на распродаже в связи с началом учебного года.</span><span class="sxs-lookup"><span data-stu-id="d46ab-114">"Save big with back to school sale.</span></span> <span data-ttu-id="d46ab-115">Покупайте сейчас."</span><span class="sxs-lookup"><span data-stu-id="d46ab-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="d46ab-116">Свойства модуля оповещения</span><span class="sxs-lookup"><span data-stu-id="d46ab-116">Alert module properties</span></span>

| <span data-ttu-id="d46ab-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="d46ab-117">Property name</span></span>  | <span data-ttu-id="d46ab-118">Стоимость</span><span class="sxs-lookup"><span data-stu-id="d46ab-118">Value</span></span>                              | <span data-ttu-id="d46ab-119">Описание</span><span class="sxs-lookup"><span data-stu-id="d46ab-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="d46ab-120">Текст</span><span class="sxs-lookup"><span data-stu-id="d46ab-120">Text</span></span>           | <span data-ttu-id="d46ab-121">Текст</span><span class="sxs-lookup"><span data-stu-id="d46ab-121">Text</span></span>                               | <span data-ttu-id="d46ab-122">Текстовое сообщение, отображаемое в модуле оповещения.</span><span class="sxs-lookup"><span data-stu-id="d46ab-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="d46ab-123">Выравнивание текста</span><span class="sxs-lookup"><span data-stu-id="d46ab-123">Text alignment</span></span> | <span data-ttu-id="d46ab-124">**По правому краю**, **По левому краю** или **По центру**</span><span class="sxs-lookup"><span data-stu-id="d46ab-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="d46ab-125">Значение, определяющее выравнивание текста в модуле оповещения.</span><span class="sxs-lookup"><span data-stu-id="d46ab-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="d46ab-126">Закрыть оповещение</span><span class="sxs-lookup"><span data-stu-id="d46ab-126">Dismiss alert</span></span>  | <span data-ttu-id="d46ab-127">**True** или **False**</span><span class="sxs-lookup"><span data-stu-id="d46ab-127">**True** or **False**</span></span>              | <span data-ttu-id="d46ab-128">Если установлено значение **True**, клиент может закрыть оповещение.</span><span class="sxs-lookup"><span data-stu-id="d46ab-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="d46ab-129">Ссылка</span><span class="sxs-lookup"><span data-stu-id="d46ab-129">Link</span></span>           | <span data-ttu-id="d46ab-130">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d46ab-130">URL</span></span>                                | <span data-ttu-id="d46ab-131">URL-адрес для необязательной ссылки.</span><span class="sxs-lookup"><span data-stu-id="d46ab-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="d46ab-132">Добавление модуля оповещения на страницу</span><span class="sxs-lookup"><span data-stu-id="d46ab-132">Add an alert module to a page</span></span> 

<span data-ttu-id="d46ab-133">Чтобы добавить модуль оповещения на страницу и задать необходимые свойства, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d46ab-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d46ab-134">Создайте шаблон страницы с именем **шаблон оповещения**.</span><span class="sxs-lookup"><span data-stu-id="d46ab-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="d46ab-135">В слоте **Главный** страницы по умолчанию добавьте модуль оповещения.</span><span class="sxs-lookup"><span data-stu-id="d46ab-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="d46ab-136">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="d46ab-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="d46ab-137">Используйте только что созданный шаблон оповещения для создания страницы с именем **страница оповещения**.</span><span class="sxs-lookup"><span data-stu-id="d46ab-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="d46ab-138">В слоте **Главный** новой страницы добавьте модуль оповещения.</span><span class="sxs-lookup"><span data-stu-id="d46ab-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="d46ab-139">В настройках модуля оповещения введите текст оповещения.</span><span class="sxs-lookup"><span data-stu-id="d46ab-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="d46ab-140">Если требуется дополнительно настроить модуль оповещений, можно изменить другие свойства.</span><span class="sxs-lookup"><span data-stu-id="d46ab-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="d46ab-141">Сохраните и просмотрите страницу.</span><span class="sxs-lookup"><span data-stu-id="d46ab-141">Save and preview the page.</span></span> <span data-ttu-id="d46ab-142">В верхней части страницы должно отобразиться оповещение с добавленным текстом.</span><span class="sxs-lookup"><span data-stu-id="d46ab-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="d46ab-143">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="d46ab-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d46ab-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d46ab-144">Additional resources</span></span>

[<span data-ttu-id="d46ab-145">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="d46ab-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d46ab-146">Модуль карусели</span><span class="sxs-lookup"><span data-stu-id="d46ab-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d46ab-147">Модуль блока насыщенного содержимого</span><span class="sxs-lookup"><span data-stu-id="d46ab-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d46ab-148">Модуль размещения содержимого</span><span class="sxs-lookup"><span data-stu-id="d46ab-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="d46ab-149">Модуль компонента</span><span class="sxs-lookup"><span data-stu-id="d46ab-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="d46ab-150">Модуль главного имиджевого баннера</span><span class="sxs-lookup"><span data-stu-id="d46ab-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="d46ab-151">Модуль видеопроигрывателя</span><span class="sxs-lookup"><span data-stu-id="d46ab-151">Video player module</span></span>](add-video-player.md)
